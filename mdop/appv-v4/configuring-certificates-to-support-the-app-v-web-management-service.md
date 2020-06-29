---
title: Configuración de certificados para admitir el servicio de administración web de App-V
description: Configuración de certificados para admitir el servicio de administración web de App-V
author: dansimp
ms.assetid: b7960161-2c19-4cbf-a98a-d4b06f547dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 23839e6fad79c1f10eb2416941396ad3c6f04d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821890"
---
# <span data-ttu-id="541a6-103">Configuración de certificados para admitir el servicio de administración web de App-V</span><span class="sxs-lookup"><span data-stu-id="541a6-103">Configuring Certificates to Support the App-V Web Management Service</span></span>


<span data-ttu-id="541a6-104">El servicio de administración web de App-V debe estar configurado para admitir conexiones basadas en SSL para ayudar a proteger la comunicación.</span><span class="sxs-lookup"><span data-stu-id="541a6-104">The App-V Web Management Service must be configured to support SSL-based connections to help secure the communication.</span></span> <span data-ttu-id="541a6-105">Este proceso requiere que el servidor web o el equipo en el que está instalado el servicio de administración tenga un certificado emitido para el servicio o equipo.</span><span class="sxs-lookup"><span data-stu-id="541a6-105">This process requires that the Web server or computer on which the Management Service is installed has a certificate issued to the service or computer.</span></span>

<span data-ttu-id="541a6-106">En los siguientes escenarios se muestra cómo obtener un certificado para este propósito:</span><span class="sxs-lookup"><span data-stu-id="541a6-106">The following scenarios illustrate how to obtain a certificate for this purpose:</span></span>

1.  <span data-ttu-id="541a6-107">La infraestructura de la empresa ya tiene una infraestructura de clave pública (PKI) que emite automáticamente certificados para los equipos.</span><span class="sxs-lookup"><span data-stu-id="541a6-107">The company infrastructure already has a public key infrastructure (PKI) in place that automatically issues certificates to computers.</span></span>

2.  <span data-ttu-id="541a6-108">La infraestructura de la compañía ya tiene una PKI vigente, aunque no emite automáticamente certificados para equipos.</span><span class="sxs-lookup"><span data-stu-id="541a6-108">The company infrastructure already has a PKI in place, although it does not automatically issue certificates to computers.</span></span>

3.  <span data-ttu-id="541a6-109">La infraestructura de la compañía no tiene ninguna PKI vigente.</span><span class="sxs-lookup"><span data-stu-id="541a6-109">The company infrastructure has no PKI in place.</span></span>

<span data-ttu-id="541a6-110">En cada uno de los escenarios anteriores, el método para obtener un certificado es diferente, pero el resultado final es el mismo.</span><span class="sxs-lookup"><span data-stu-id="541a6-110">In each of the preceding scenarios, the method for obtaining a certificate is different, but the end result is the same.</span></span> <span data-ttu-id="541a6-111">El administrador debe asignar un certificado al sitio web predeterminado de IIS y configurar el servicio de administración web de App-V para requerir comunicaciones seguras.</span><span class="sxs-lookup"><span data-stu-id="541a6-111">The administrator must assign a certificate to the IIS Default Web Site and configure the App-V Web Management Service to require secure communications.</span></span>

<span data-ttu-id="541a6-112">**Importante**  El nombre del certificado debe coincidir con el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="541a6-112">**Important** The name of the certificate must match the name of the server.</span></span> <span data-ttu-id="541a6-113">Es recomendable usar nombres de dominio completos (FQDN) para el nombre común del certificado.</span><span class="sxs-lookup"><span data-stu-id="541a6-113">It is a best practice to use fully qualified domain names (FQDNs) for the common name of the certificate.</span></span>

 

<span data-ttu-id="541a6-114">App-V puede usar servidores IIS para admitir diferentes configuraciones de infraestructura.</span><span class="sxs-lookup"><span data-stu-id="541a6-114">App-V can use IIS servers to support different infrastructure configurations.</span></span> <span data-ttu-id="541a6-115">Para obtener más información sobre cómo configurar los servidores IIS para que admitan HTTPS, consulte <https://go.microsoft.com/fwlink/?LinkId=151972> .</span><span class="sxs-lookup"><span data-stu-id="541a6-115">For more information about configuring IIS servers to support HTTPS, see <https://go.microsoft.com/fwlink/?LinkId=151972>.</span></span>

## <span data-ttu-id="541a6-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="541a6-116">Related topics</span></span>


[<span data-ttu-id="541a6-117">Cómo instalar y configurar la consola de administración de App-V para un entorno más seguro</span><span class="sxs-lookup"><span data-stu-id="541a6-117">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)

 

 





