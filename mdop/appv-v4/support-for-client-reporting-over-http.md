---
title: Soporte técnico para informe de cliente por HTTP
description: Soporte técnico para informe de cliente por HTTP
author: dansimp
ms.assetid: 4a26ac80-1fb5-4c05-83de-4d06793f7bf2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4e1759bb4df39ac403e2837c4083275a8b3436f5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815290"
---
# <span data-ttu-id="a3a2f-103">Soporte técnico para informe de cliente por HTTP</span><span class="sxs-lookup"><span data-stu-id="a3a2f-103">Support for Client Reporting over HTTP</span></span>


<span data-ttu-id="a3a2f-104">La versión 4,6 del cliente de App-V ahora admite el uso de comunicación HTTP al enviar datos de informes de cliente al servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-104">Version 4.6 of the App-V client now supports the use of HTTP communication when sending client reporting data to the publishing server.</span></span> <span data-ttu-id="a3a2f-105">Esta característica admite escenarios en los que un cliente ha implementado un servidor de publicación HTTP (S) personalizado que está configurado para recopilar y procesar datos del cliente.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-105">This feature supports scenarios where a customer has implemented a custom HTTP(S) publishing server that is configured to collect and process client data.</span></span>

<span data-ttu-id="a3a2f-106">Para obtener más información sobre los servidores de publicación HTTP, consulte</span><span class="sxs-lookup"><span data-stu-id="a3a2f-106">For more information on HTTP publishing servers, see</span></span> <https://go.microsoft.com/fwlink/?LinkId=157426>

## <span data-ttu-id="a3a2f-107">Informes de cliente sobre HTTP</span><span class="sxs-lookup"><span data-stu-id="a3a2f-107">Client Reporting over HTTP</span></span>


<span data-ttu-id="a3a2f-108">El cliente comienza a recopilar datos cuando recibe un atributo "Reporting =" TRUE "" en el XML de actualización de publicación del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-108">The client starts collecting data when it receives a “REPORTING=”TRUE””attribute in the publishing refresh response XML from the publishing server.</span></span> <span data-ttu-id="a3a2f-109">Cuando se recibe este atributo, el cliente envía los datos acumulados al servidor de publicación que envió la actualización de publicación.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-109">When this attribute is received, the client sends any accumulated data to the publishing server that sent the publishing refresh.</span></span> <span data-ttu-id="a3a2f-110">Los detalles de este proceso son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="a3a2f-110">The details of this process are as follows:</span></span>

-   <span data-ttu-id="a3a2f-111">El cliente envía una solicitud HTTP GET al servidor de publicación para una actualización de publicación.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-111">The client sends an HTTP GET request to the publishing server for a publishing refresh.</span></span> <span data-ttu-id="a3a2f-112">El encabezado de este mensaje contiene un encabezado personalizado "AppV-OP: actualizar" que el servidor de publicación HTTP (S) personalizado usa para identificar el tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-112">The header of this message contains an “AppV-Op:Refresh” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

-   <span data-ttu-id="a3a2f-113">A continuación, el servidor de publicación envía el XML de respuesta de actualización de publicación que contiene un valor "Reporting =" TRUE "".</span><span class="sxs-lookup"><span data-stu-id="a3a2f-113">The publishing server then sends the publishing refresh response XML that contains a “REPORTING=”TRUE”” value.</span></span>

-   <span data-ttu-id="a3a2f-114">Después, el cliente envía una solicitud HTTP POST al servidor de publicación junto con los datos de informes que se han recopilado desde la actualización anterior.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-114">The client then sends an HTTP POST request to the publishing server along with the reporting data that has been gathered since the previous refresh.</span></span> <span data-ttu-id="a3a2f-115">El encabezado de este mensaje contiene un encabezado personalizado "AppV-OP: Report" que usa el servidor de publicación HTTP (S) personalizado para identificar el tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-115">The header of this message contains an “AppV-Op:Report” custom header that the custom HTTP(S) publishing server uses to identify the message type.</span></span>

<span data-ttu-id="a3a2f-116">El siguiente esquema proporciona detalles específicos del paquete y los datos de la aplicación que se envían al servidor.</span><span class="sxs-lookup"><span data-stu-id="a3a2f-116">The following schema gives specific details of the package and the application data that is sent to the server.</span></span>

```xml
<?xml version="1.0"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:element name="CLIENT_DATA">
        <xs:complexType>
            <xs:all>
                <xs:element ref="PKG_LIST" minOccurs="1" maxOccurs="1"/>
                <xs:element ref="APP_RECORDS" minOccurs="1" maxOccurs="1"/>
            </xs:all>
            <!-- no regex for Ver because we want to allow tags like "Beta" -->
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Host" type="xs:token" use="required"/>
            <xs:attribute name="CacheSize" type="xs:nonNegativeInteger" use="required"/>
            <xs:attribute name="CacheUsed" type="xs:nonNegativeInteger" use="required"/>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_LIST">
        <xs:complexType>
            <xs:choice>
                <xs:element ref="PKG_DATA" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
    </xs:element>

    <xs:element name="PKG_DATA">
        <xs:complexType>
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Guid" type="xs:token" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="VerGuid" type="xs:token" use="required"/>
            <xs:attribute name="Source" type="xs:normalizedString" use="required"/>
            <xs:attribute name="PctCached" use="required">
                <xs:simpleType>
                    <xs:restriction base="xs:nonNegativeInteger">
                        <xs:minInclusive value="0"/>
                        <xs:maxInclusive value="100"/>
                    </xs:restriction>
                </xs:simpleType>
            </xs:attribute>
        </xs:complexType>
    </xs:element>

    <xs:element name="APP_RECORDS">
         <xs:complexType>
            <xs:choice>
                <xs:element ref="APP_RECORD" minOccurs="0" maxOccurs="unbounded"/>
            </xs:choice>
        </xs:complexType>
   </xs:element>

    <xs:element name="APP_RECORD">
            <xs:attribute name="Name" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Ver" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Server" type="xs:normalizedString" use="required"/>
            <xs:attribute name="User" type="xs:normalizedString" use="required"/>
            <xs:attribute name="Launched" type="xs:dateTime" use="required"/>
            <xs:attribute name="Shutdown" type="xs:dateTime" use="optional"/>
    </xs:element>

</xs:schema>
```

 

 





