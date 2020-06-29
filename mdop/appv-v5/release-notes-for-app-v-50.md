---
title: Notas de la versión de App-V 5.0
description: Notas de la versión de App-V 5.0
author: dansimp
ms.assetid: 68a6a5a1-4b3c-4c09-b00c-9ca4237695d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e49f6072d738b45afe25de24f2ee9a2d09d64a2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813319"
---
# <span data-ttu-id="328ec-103">Notas de la versión de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="328ec-103">Release Notes for App-V 5.0</span></span>


**<span data-ttu-id="328ec-104">Para buscar un problema específico en estas notas de la versión, presione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="328ec-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="328ec-105">Lea estas notas de la versión minuciosamente antes de instalar App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="328ec-105">Read these release notes thoroughly before you install App-V 5.0.</span></span>

<span data-ttu-id="328ec-106">Estas notas de la versión contienen información necesaria para instalar correctamente App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="328ec-106">These release notes contain information that is required to successfully install App-V 5.0.</span></span> <span data-ttu-id="328ec-107">Las notas de la versión también contienen información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="328ec-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="328ec-108">Si hay una diferencia entre estas notas de la versión y otra documentación de App-V 5,0, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="328ec-108">If there is a difference between these release notes and other App-V 5.0 documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="328ec-109">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="328ec-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="328ec-110">Acerca de la documentación del producto</span><span class="sxs-lookup"><span data-stu-id="328ec-110">About the Product Documentation</span></span>


<span data-ttu-id="328ec-111">Para obtener información sobre la documentación de App-V 5,0, consulte la página de inicio de App-V 5,0 en Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="328ec-111">For information about App-V 5.0 documentation, see the App-V 5.0 home page on Microsoft TechNet.</span></span>

## <span data-ttu-id="328ec-112">Enviar comentarios</span><span class="sxs-lookup"><span data-stu-id="328ec-112">Provide Feedback</span></span>


<span data-ttu-id="328ec-113">Nos interesan tus comentarios en App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="328ec-113">We are interested in your feedback on App-V 5.0.</span></span> <span data-ttu-id="328ec-114">Puedes enviar tus comentarios a <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="328ec-114">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="328ec-115">**Nota:**  Esta dirección de correo electrónico no es un canal de soporte técnico, pero tus comentarios nos ayudarán a planificar futuros cambios en nuestra documentación y versiones de productos.</span><span class="sxs-lookup"><span data-stu-id="328ec-115">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="328ec-116">Para obtener la información más reciente acerca de MDOP y recursos de aprendizaje adicionales, consulte la página [experiencia de información de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="328ec-116">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="328ec-117">Para obtener más información sobre las nuevas actualizaciones o para proporcionar comentarios, síganos en [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="328ec-117">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="328ec-118">Problemas conocidos con App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="328ec-118">Known Issues with App-V 5.0</span></span>


<span data-ttu-id="328ec-119">Esta sección contiene notas de la versión sobre los problemas conocidos con App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="328ec-119">This section contains release notes about the known issues with App-V 5.0.</span></span>

### <span data-ttu-id="328ec-120">No se puede terminar de agregar paquetes al usar cmdlets de servidor de PowerShell</span><span class="sxs-lookup"><span data-stu-id="328ec-120">Unable to terminate adding packages when using server PowerShell cmdlets</span></span>

<span data-ttu-id="328ec-121">Al agregar un paquete con PowerShell, no hay ningún método para salir de la adición de paquetes nuevos.</span><span class="sxs-lookup"><span data-stu-id="328ec-121">When you add a package using PowerShell, there is no method to exit adding new packages.</span></span>

<span data-ttu-id="328ec-122">SOLUCIÓN alternativa: para dejar de agregar paquetes, pulse **entrar** después de agregar el paquete final.</span><span class="sxs-lookup"><span data-stu-id="328ec-122">WORKAROUND: To stop adding packages, press **enter** after you have added the final package.</span></span>

### <a href="" id="-------------app-v-5-0-client-rejects-packages-from-servers-whose-ssl-certificate-has-been-revoked"></a> <span data-ttu-id="328ec-123">El cliente de App-V 5,0 rechaza paquetes de servidores cuyo certificado SSL ha sido revocado</span><span class="sxs-lookup"><span data-stu-id="328ec-123">App-V 5.0 client rejects packages from servers whose SSL certificate has been revoked</span></span>

<span data-ttu-id="328ec-124">Al usar el protocolo HTTPS, el cliente de App-V 5,0 rechazará de forma predeterminada los paquetes de los servidores cuyo certificado SSL se haya revocado.</span><span class="sxs-lookup"><span data-stu-id="328ec-124">When using the HTTPS protocol, the App-V 5.0 client will by default reject packages from servers whose SSL certificate has been revoked.</span></span> <span data-ttu-id="328ec-125">Este comportamiento se puede desactivar mediante la configuración modificando la configuración **VerifyCertificateRevocationList** .</span><span class="sxs-lookup"><span data-stu-id="328ec-125">This behavior can be turned off through configuration by modifying the **VerifyCertificateRevocationList** setting.</span></span> <span data-ttu-id="328ec-126">La aplicación de una nueva configuración para esta configuración no surtirá efecto hasta que se reinicie el servicio App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="328ec-126">Applying new configuration for this setting will not take effect until the App-V 5.0 service is restarted.</span></span>

<span data-ttu-id="328ec-127">SOLUCIÓN alternativa: reinicie el servicio de 5,0 de App-V.</span><span class="sxs-lookup"><span data-stu-id="328ec-127">WORKAROUND: Restart the App-V 5.0 service.</span></span>

## <span data-ttu-id="328ec-128">Información de copyright de notas de versión</span><span class="sxs-lookup"><span data-stu-id="328ec-128">Release Notes Copyright Information</span></span>


<span data-ttu-id="328ec-129">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune y WindowsPowerShell son marcas comerciales del grupo de empresas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="328ec-129">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="328ec-130">El resto de marcas comerciales pertenecen a sus respectivos dueños.</span><span class="sxs-lookup"><span data-stu-id="328ec-130">All other trademarks are property of their respective owners.</span></span>








## <span data-ttu-id="328ec-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="328ec-131">Related topics</span></span>


[<span data-ttu-id="328ec-132">Acerca de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="328ec-132">About App-V 5.0</span></span>](about-app-v-50.md)

 

 





