---
title: Cómo mover los sitios web de MBAM 2.5
description: Cómo mover los sitios web de MBAM 2.5
author: dansimp
ms.assetid: 71af9a54-c27b-408f-9d75-37c0d02e730e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa5bd8156810b3dccc1588b4dfd4cadd96fd22fb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825750"
---
# <span data-ttu-id="3b126-103">Cómo mover los sitios web de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="3b126-103">How to Move the MBAM 2.5 Websites</span></span>


<span data-ttu-id="3b126-104">Use estos procedimientos para mover los siguientes sitios web de MBAM de un equipo a otro, es decir, para mover las siguientes características del servidor a al servidor B:</span><span class="sxs-lookup"><span data-stu-id="3b126-104">Use these procedures to move the following MBAM websites from one computer to another, that is, to move the following features from Server A to Server B:</span></span>

-   <span data-ttu-id="3b126-105">Sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="3b126-105">Administration and Monitoring Website</span></span>

-   <span data-ttu-id="3b126-106">Portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="3b126-106">Self-Service Portal</span></span>

<span data-ttu-id="3b126-107">**Importante**  Durante la configuración de ambos sitios web, debe proporcionar la misma cadena de conexión, la dirección URL de los informes, las cuentas de grupo y la cuenta de dominio del grupo de aplicaciones de servicio web como las que está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="3b126-107">**Important** During the configuration of both websites, you must provide the same connection string, Reports URL, group accounts, and web service application pool domain account as the ones that you are currently using.</span></span> <span data-ttu-id="3b126-108">Si no usa los mismos valores, no podrá obtener acceso a algunos de los servidores.</span><span class="sxs-lookup"><span data-stu-id="3b126-108">If you don’t use the same values, you cannot access some of the servers.</span></span> <span data-ttu-id="3b126-109">Para obtener los valores actuales, use el cmdlet **Get-MbamWebApplication** de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3b126-109">To get the current values, use the **Get-MbamWebApplication** Windows PowerShell cmdlet.</span></span>

 

**<span data-ttu-id="3b126-110">Para mover el sitio web de administración y supervisión a otro servidor</span><span class="sxs-lookup"><span data-stu-id="3b126-110">To move the Administration and Monitoring Website to another server</span></span>**

1.  <span data-ttu-id="3b126-111">En el servidor B, instale el software de servidor MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="3b126-111">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="3b126-112">Para obtener instrucciones, consulte [Installing the MBAM 2,5 Server Software](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="3b126-112">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="3b126-113">En el servidor B, inicie el Asistente para la configuración del servidor de MBAM, haga clic en **Agregar nuevas características**y, a continuación, seleccione solo la característica **sitio web de administración y supervisión** .</span><span class="sxs-lookup"><span data-stu-id="3b126-113">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Administration and Monitoring Website** feature.</span></span>

    <span data-ttu-id="3b126-114">También puede usar el cmdlet **enable-MbamWebApplication** de Windows PowerShell para configurar el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="3b126-114">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="3b126-115">Para obtener instrucciones sobre cómo configurar el sitio web de administración y supervisión, consulte [Cómo configurar las aplicaciones Web de MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="3b126-115">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

**<span data-ttu-id="3b126-116">Para mover el portal de autoservicio a otro servidor</span><span class="sxs-lookup"><span data-stu-id="3b126-116">To move the Self-Service Portal to another server</span></span>**

1.  <span data-ttu-id="3b126-117">En el servidor B, instale el software de servidor MBAM 2,5.</span><span class="sxs-lookup"><span data-stu-id="3b126-117">On Server B, install the MBAM 2.5 Server software.</span></span> <span data-ttu-id="3b126-118">Para obtener instrucciones, consulte [Installing the MBAM 2,5 Server Software](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="3b126-118">For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="3b126-119">En el servidor B, inicie el Asistente para la configuración del servidor de MBAM, haga clic en **Agregar nuevas características**y, a continuación, seleccione solo la característica del **portal de autoservicio** .</span><span class="sxs-lookup"><span data-stu-id="3b126-119">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Self-Service Portal** feature.</span></span>

    <span data-ttu-id="3b126-120">Como alternativa, puede usar el cmdlet **enable-MbamWebApplication** de Windows PowerShell para configurar el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="3b126-120">Alternatively, you can use the **Enable-MbamWebApplication** Windows PowerShell cmdlet to configure the Self-Service Portal.</span></span>

    <span data-ttu-id="3b126-121">Para obtener instrucciones sobre cómo configurar el sitio web de administración y supervisión, consulte [Cómo configurar las aplicaciones Web de MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="3b126-121">For instructions on how to configure the Administration and Monitoring Website, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>

3.  <span data-ttu-id="3b126-122">Si los equipos cliente de su organización no tienen acceso a la red de entrega de contenido de Microsoft, también tendrá que mover los archivos JavaScript.</span><span class="sxs-lookup"><span data-stu-id="3b126-122">If the client computers in your organization do not have access to the Microsoft Content Delivery Network, you also have to move the JavaScript files.</span></span> <span data-ttu-id="3b126-123">Consulte [Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden obtener acceso a la red de entrega de contenido de Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="3b126-123">See [How to Configure the Self-Service Portal When Client Computers Cannot Access the Microsoft Content Delivery Network](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) for more information.</span></span>

4.  <span data-ttu-id="3b126-124">Personalizar el portal de autoservicio para su organización.</span><span class="sxs-lookup"><span data-stu-id="3b126-124">Customize the Self-Service Portal for your organization.</span></span> <span data-ttu-id="3b126-125">Use las instrucciones de [Personalización del portal de autoservicio para que su organización](customizing-the-self-service-portal-for-your-organization.md) Revise las personalizaciones actuales y para configurar ajustes personalizados en el portal de autoservidor en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="3b126-125">Use the instructions in [Customizing the Self-Service Portal for Your Organization](customizing-the-self-service-portal-for-your-organization.md) to review your current customizations and to configure custom settings on the Self-Server Portal on Server B.</span></span>



## <span data-ttu-id="3b126-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b126-126">Related topics</span></span>


[<span data-ttu-id="3b126-127">Cómo configurar las aplicaciones web de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="3b126-127">How to Configure the MBAM 2.5 Web Applications</span></span>](how-to-configure-the-mbam-25-web-applications.md)

[<span data-ttu-id="3b126-128">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3b126-128">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="3b126-129">Movimiento de funciones de MBAM 2.5 a otro servidor</span><span class="sxs-lookup"><span data-stu-id="3b126-129">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 

## <span data-ttu-id="3b126-130">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="3b126-130">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="3b126-131">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="3b126-131">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="3b126-132">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="3b126-132">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





