---
title: Cómo probar la publicación de aplicaciones
description: Cómo probar la publicación de aplicaciones
author: dansimp
ms.assetid: 17ba2e12-50a0-4f41-8300-f61f09db9f6c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 8dffb4f79ac89c7d419b27640f4f05364bd69e5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826911"
---
# <span data-ttu-id="0aa02-103">Cómo probar la publicación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="0aa02-103">How to Test Application Publishing</span></span>


<span data-ttu-id="0aa02-104">Después de que finalice la prueba de la primera configuración, puede comprobar que la funcionalidad de publicación de la aplicación funciona según lo esperado realizando las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="0aa02-104">After your test of first time setup finishes, you can verify that the application publishing functionality is working as expected by performing the following tasks.</span></span>

<a href="" id="bkmk-apppub"></a>**<span data-ttu-id="0aa02-105">Para probar la publicación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="0aa02-105">To test application publishing</span></span>**

1.  <span data-ttu-id="0aa02-106">Compruebe que las aplicaciones que especificó para su publicación sean visibles.</span><span class="sxs-lookup"><span data-stu-id="0aa02-106">Verify that the applications that you specified for publishing are visible.</span></span>

    <span data-ttu-id="0aa02-107">Haga clic en **Inicio** y, después, haga clic en **todos los programas** y busque las aplicaciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="0aa02-107">Click **Start** and then click **All Programs** and search for the specified applications.</span></span>

    <span data-ttu-id="0aa02-108">En algunos casos, es posible que la misma aplicación se haya instalado dos veces, una vez en el equipo host y una vez en el invitado.</span><span class="sxs-lookup"><span data-stu-id="0aa02-108">In some cases, you might have the same application installed two times, one time on the host computer and one time on the guest.</span></span> <span data-ttu-id="0aa02-109">Si una aplicación publicada que tiene el mismo nombre se publica en la misma ubicación en el menú **Inicio** de host, se distingue del acceso directo de la aplicación host agregando el nombre de la máquina virtual al nombre del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="0aa02-109">If a published application that has the same name is published to the same location on the host **Start** menu, it is distinguished from the host application shortcut by adding the virtual machine name to the shortcut name.</span></span> <span data-ttu-id="0aa02-110">Por ejemplo, en el caso de una máquina virtual denominada "MEDVHost1", una aplicación host podría ser "Bloc de notas" y una aplicación publicada podría ser "Notepad (MEDVHost1)".</span><span class="sxs-lookup"><span data-stu-id="0aa02-110">For example, for a virtual machine named “MEDVHost1”, a host application might be "Notepad" and a published application might be "Notepad (MEDVHost1)".</span></span>

2.  <span data-ttu-id="0aa02-111">Compruebe que las aplicaciones funcionan como se pretendía.</span><span class="sxs-lookup"><span data-stu-id="0aa02-111">Verify that the applications function as intended.</span></span>

    <span data-ttu-id="0aa02-112">En el equipo host, inicie las aplicaciones que publicó y compruebe que se abren en Windows XP SP3 en el invitado.</span><span class="sxs-lookup"><span data-stu-id="0aa02-112">On the host computer, start the applications that you published and verify that they open in Windows XP SP3 on the guest.</span></span> <span data-ttu-id="0aa02-113">La aplicación debe aparecer en una ventana de estilo Windows XP en el escritorio del equipo host.</span><span class="sxs-lookup"><span data-stu-id="0aa02-113">The application must appear in a Windows XP-style window on the host computer desktop.</span></span>

3.  <span data-ttu-id="0aa02-114">Si procede, compruebe que las funciones de redireccionamiento de documentos son las previstas.</span><span class="sxs-lookup"><span data-stu-id="0aa02-114">If applicable, verify that document redirection functions as intended.</span></span>

    <span data-ttu-id="0aa02-115">Si una aplicación publicada en el invitado tiene que abrir una carpeta en la unidad del sistema host, asegúrese de que puede abrir la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="0aa02-115">If a published application on the guest has to open a folder on the host system drive, ensure that it can open the specified folder.</span></span>

    <span data-ttu-id="0aa02-116">**Importante**  Dado que Windows Virtual PC no es compatible con la creación de un recurso compartido desde una carpeta que ya está compartida, el redireccionamiento no se realiza en ningún documento que se abra desde una carpeta compartida, como una carpeta Mis documentos ubicada en la red.</span><span class="sxs-lookup"><span data-stu-id="0aa02-116">**Important** Because Windows Virtual PC does not support creating a share from a folder that is already shared, redirection does not occur for any documents that open from a shared folder, such as a My Documents folder that is located on the network.</span></span> <span data-ttu-id="0aa02-117">Para obtener más información, consulte [solución de problemas de operaciones](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="0aa02-117">For more information, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="0aa02-118">Una vez que haya comprobado que las aplicaciones publicadas están instaladas y funcionan correctamente, puede comprobar si las aplicaciones se pueden agregar o quitar del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="0aa02-118">After you have verified that published applications are installed and functioning correctly, you can test whether applications can be added or removed from the MED-V workspace.</span></span>

**<span data-ttu-id="0aa02-119">Para comprobar que se puede Agregar o quitar una aplicación</span><span class="sxs-lookup"><span data-stu-id="0aa02-119">To test that an application can be added or removed</span></span>**

1.  <span data-ttu-id="0aa02-120">Agregar o quitar una aplicación del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="0aa02-120">Add or remove an application from the MED-V workspace.</span></span>

    <span data-ttu-id="0aa02-121">Para obtener información sobre cómo agregar y quitar aplicaciones de un área de trabajo de MED-V, consulte [administrar las aplicaciones implementadas en áreas de trabajo de Med-v](managing-applications-deployed-to-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="0aa02-121">For information about how to add and remove applications from a MED-V workspace, see [Managing Applications Deployed to MED-V Workspaces](managing-applications-deployed-to-med-v-workspaces.md).</span></span>

2.  <span data-ttu-id="0aa02-122">Si agregó una aplicación, repita los pasos de [para probar la publicación de aplicaciones](#bkmk-apppub) para comprobar que la nueva aplicación funciona como se pretende.</span><span class="sxs-lookup"><span data-stu-id="0aa02-122">If you added an application, repeat the steps in [To Test Application Publishing](#bkmk-apppub) to verify that the new application functions as intended.</span></span>

3.  <span data-ttu-id="0aa02-123">Si ha quitado una aplicación, haga clic en **Inicio** y, a continuación, haga clic en **todos los programas** y compruebe que las aplicaciones que quitó ya no aparecen en la lista.</span><span class="sxs-lookup"><span data-stu-id="0aa02-123">If you removed an application, click **Start** and then click **All Programs** and verify that any applications that you removed are no longer listed.</span></span>

<span data-ttu-id="0aa02-124">**Nota:**  Si tiene algún problema al comprobar la configuración de la publicación de la aplicación, vea [solución de problemas de operaciones](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="0aa02-124">**Note** If you encounter any problems when verifying your application publication settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="0aa02-125">Una vez que haya completado las pruebas de publicación de aplicaciones, puede probar otras configuraciones de área de trabajo de MED-V para comprobar que funcionan según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="0aa02-125">After you have completed testing application publishing, you can test other MED-V workspace configurations to verify that they function as intended.</span></span>

<span data-ttu-id="0aa02-126">Una vez que haya completado la prueba de su paquete de área de trabajo MED-V y haya comprobado que funciona como se espera, puede implementar el área de trabajo de MED-V en su empresa.</span><span class="sxs-lookup"><span data-stu-id="0aa02-126">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="0aa02-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0aa02-127">Related topics</span></span>

[<span data-ttu-id="0aa02-128">Cómo comprobar el redireccionamiento de la dirección URL</span><span class="sxs-lookup"><span data-stu-id="0aa02-128">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="0aa02-129">Cómo comprobar la configuración de instalación de primera vez</span><span class="sxs-lookup"><span data-stu-id="0aa02-129">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="0aa02-130">Implementación del paquete del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="0aa02-130">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 





