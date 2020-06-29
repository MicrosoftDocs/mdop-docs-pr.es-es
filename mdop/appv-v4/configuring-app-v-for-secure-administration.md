---
title: Configuración de App-V para administración segura
description: Configuración de App-V para administración segura
author: dansimp
ms.assetid: 4543fa81-c8cc-4b10-83b7-060778eb1349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de70c1df734bbf1168fd7dacf9410d3451a8a3c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821901"
---
# <span data-ttu-id="97236-103">Configuración de App-V para administración segura</span><span class="sxs-lookup"><span data-stu-id="97236-103">Configuring App-V for Secure Administration</span></span>


<span data-ttu-id="97236-104">En un entorno donde sea importante proteger las operaciones administrativas, App-V permite la comunicación segura entre el servicio de administración web de App-V y la consola de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="97236-104">In an environment where securing administrative operations is important, App-V allows for secure communication between the App-V Web Management Service and the App-V Management Console.</span></span> <span data-ttu-id="97236-105">Dado que el servicio de administración es una aplicación basada en Web, requiere la protección de la aplicación de servidor de administración de App-V en el servidor Web que hospeda el servicio de administración.</span><span class="sxs-lookup"><span data-stu-id="97236-105">Because the Management Service is a Web-based application, it requires securing the App-V Management Server application on the Web server that hosts the Management Service.</span></span> <span data-ttu-id="97236-106">Tal y como se muestra en la siguiente ilustración, este proceso incluye el uso de HTTPS para la comunicación y la configuración del servidor IIS para permitir únicamente la autenticación integrada de Windows.</span><span class="sxs-lookup"><span data-stu-id="97236-106">As shown in the following illustration, this process includes using HTTPS for communication and configuring the IIS server to allow only Windows Integrated Authentication.</span></span>

![configuración de red del servicio Web de App-v](images/appvmgmtwebservice.gif)

<span data-ttu-id="97236-108">El servicio de administración web de App-V se instala como una aplicación basada en Web en IIS.</span><span class="sxs-lookup"><span data-stu-id="97236-108">The App-V Web Management Service is installed as a Web-based application on IIS.</span></span> <span data-ttu-id="97236-109">Para que el servicio de administración web admita conexiones seguras (SSL) entre la consola de administración de App-V y el servicio de administración web, tendrá que configurar el servidor IIS donde está instalado el servicio de administración web y configurar la consola de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="97236-109">For the Web Management Service to support secure (SSL) connections between the App-V Management Console and the Web Management Service, you will need to configure the IIS server where the Web Management Service is installed and configure the App-V Management Console.</span></span>

## <span data-ttu-id="97236-110">En esta sección</span><span class="sxs-lookup"><span data-stu-id="97236-110">In This Section</span></span>


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[<span data-ttu-id="97236-111">Configuración de certificados para admitir el servicio de administración web de App-V</span><span class="sxs-lookup"><span data-stu-id="97236-111">Configuring Certificates to Support the App-V Web Management Service</span></span>](configuring-certificates-to-support-the-app-v-web-management-service.md)  
<span data-ttu-id="97236-112">Proporciona información útil sobre la configuración de certificados para admitir conexiones SSL, para ayudar a proteger la comunicación del servicio de administración web de App-V.</span><span class="sxs-lookup"><span data-stu-id="97236-112">Provides helpful information about configuring certificates to support SSL-based connections, to help secure communication for the App-V Web Management Service.</span></span>

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[<span data-ttu-id="97236-113">Cómo instalar y configurar la consola de administración de App-V para un entorno más seguro</span><span class="sxs-lookup"><span data-stu-id="97236-113">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
<span data-ttu-id="97236-114">Proporciona un procedimiento paso a paso para conectarse a un servicio de administración web de App-V mediante una conexión segura.</span><span class="sxs-lookup"><span data-stu-id="97236-114">Provides a step-by-step procedure for connecting to an App-V Web Management Service by using a secure connection.</span></span>

 

 





