---
title: Cómo modificar la configuración del cliente de App-V 5.0 mediante la plantilla ADMX y la directiva de grupo
description: Cómo modificar la configuración del cliente de App-V 5.0 mediante la plantilla ADMX y la directiva de grupo
author: dansimp
ms.assetid: 79d03a2b-2586-4ca7-bbaa-bdeb0a694279
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cd257691bf223baa5e2919d83fdbf53d34f271ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813839"
---
# <span data-ttu-id="77b42-103">Cómo modificar la configuración del cliente de App-V 5.0 mediante la plantilla ADMX y la directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="77b42-103">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>


<span data-ttu-id="77b42-104">Use la plantilla App-V 5,0 ADMX para configurar la configuración del cliente de App-V 5,0 con la plantilla ADMX y la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="77b42-104">Use the App-V 5.0 ADMX template to configure App-V 5.0 client settings using the ADMX Template and Group Policy.</span></span>

**<span data-ttu-id="77b42-105">Para modificar la configuración de cliente de App-V 5,0 con la Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="77b42-105">To modify App-V 5.0 client configuration using Group Policy</span></span>**

1.  <span data-ttu-id="77b42-106">Para modificar la configuración del cliente de App-V 5,0, busque los archivos de **ADMXTemplate** que están disponibles con App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="77b42-106">To modify the App-V 5.0 client configuration, locate the **ADMXTemplate** files that are available with App-V 5.0.</span></span>

    <span data-ttu-id="77b42-107">**Nota:**  Use el siguiente vínculo para descargar las plantillas de App-V 5,0 **ADMX**: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .</span><span class="sxs-lookup"><span data-stu-id="77b42-107">**Note** Use the following link to download the App-V 5.0 **ADMX Templates**: <https://go.microsoft.com/fwlink/p/?LinkId=393941>.</span></span>

     

2.  <span data-ttu-id="77b42-108">En el equipo donde administra la Directiva de grupo, generalmente el controlador de dominio, copie el archivo template **. ADMX** en el siguiente directorio: \*\* &lt; unidad de instalación &gt; \ \ Windows \ \ PolicyDefinitions\*\*.</span><span class="sxs-lookup"><span data-stu-id="77b42-108">On the computer where you manage group Policy, typically the domain controller, copy the template **.admx** file to the following directory: **&lt;Installation Drive&gt; \\ Windows \\ PolicyDefinitions**.</span></span>

    <span data-ttu-id="77b42-109">A continuación, en el mismo equipo, copie el archivo **. ADML** en el siguiente directorio: \*\* &lt; InstallationDrive &gt; \ \ Windows \ \ PolicyDefinitions \ \ en-\*\* es.</span><span class="sxs-lookup"><span data-stu-id="77b42-109">Next, on the same computer, copy the **.adml** file to the following directory: **&lt;InstallationDrive&gt; \\ Windows \\ PolicyDefinitions \\ en-US**.</span></span>

3.  <span data-ttu-id="77b42-110">Una vez que haya copiado los archivos, abra la consola de administración de directivas de grupo para modificar las directivas asociadas a los clientes de **Computer Configuration**App-V 5,0 examinar  /  **las directivas**de configuración  /  del equipo sistema de**plantillas administrativas**  /  **System**  /  **: V**.</span><span class="sxs-lookup"><span data-stu-id="77b42-110">After you have copied the files open the Group Policy Management Console, to modify the policies associated with your App-V 5.0 clients browse to **Computer Configuration** / **Policies** / **Administrative Templates** / **System** / **App-V**.</span></span>

    <span data-ttu-id="77b42-111">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="77b42-111">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="77b42-112">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="77b42-112">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="77b42-113">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="77b42-113">Got an App-V issue?</span></span>** <span data-ttu-id="77b42-114">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="77b42-114">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="77b42-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="77b42-115">Related topics</span></span>


[<span data-ttu-id="77b42-116">Implementación de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="77b42-116">Deploying App-V 5.0</span></span>](deploying-app-v-50.md)

[<span data-ttu-id="77b42-117">Información acerca de la configuración de cliente</span><span class="sxs-lookup"><span data-stu-id="77b42-117">About Client Configuration Settings</span></span>](about-client-configuration-settings.md)

 

 





