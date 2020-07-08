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
# Soporte técnico para informe de cliente por HTTP


La versión 4,6 del cliente de App-V ahora admite el uso de comunicación HTTP al enviar datos de informes de cliente al servidor de publicación. Esta característica admite escenarios en los que un cliente ha implementado un servidor de publicación HTTP (S) personalizado que está configurado para recopilar y procesar datos del cliente.

Para obtener más información sobre los servidores de publicación HTTP, consulte <https://go.microsoft.com/fwlink/?LinkId=157426>

## Informes de cliente sobre HTTP


El cliente comienza a recopilar datos cuando recibe un atributo "Reporting =" TRUE "" en el XML de actualización de publicación del servidor de publicación. Cuando se recibe este atributo, el cliente envía los datos acumulados al servidor de publicación que envió la actualización de publicación. Los detalles de este proceso son los siguientes:

-   El cliente envía una solicitud HTTP GET al servidor de publicación para una actualización de publicación. El encabezado de este mensaje contiene un encabezado personalizado "AppV-OP: actualizar" que el servidor de publicación HTTP (S) personalizado usa para identificar el tipo de mensaje.

-   A continuación, el servidor de publicación envía el XML de respuesta de actualización de publicación que contiene un valor "Reporting =" TRUE "".

-   Después, el cliente envía una solicitud HTTP POST al servidor de publicación junto con los datos de informes que se han recopilado desde la actualización anterior. El encabezado de este mensaje contiene un encabezado personalizado "AppV-OP: Report" que usa el servidor de publicación HTTP (S) personalizado para identificar el tipo de mensaje.

El siguiente esquema proporciona detalles específicos del paquete y los datos de la aplicación que se envían al servidor.

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

 

 





