---
title: Administrar las actualizaciones de Software para áreas de trabajo de MED-V
description: Administrar las actualizaciones de Software para áreas de trabajo de MED-V
author: dansimp
ms.assetid: a28d6dcd-cb9f-46ba-8dac-1d990837a3a3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 696238a2f5ad9b7e5120f75f6cd09d890d12519b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824811"
---
# <span data-ttu-id="0face-103">Administrar las actualizaciones de Software para áreas de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="0face-103">Managing Software Updates for MED-V Workspaces</span></span>


<span data-ttu-id="0face-104">Tiene varias opciones diferentes disponibles para proporcionar actualizaciones de software para las aplicaciones en el área de trabajo de MED-V implementada.</span><span class="sxs-lookup"><span data-stu-id="0face-104">You have several different options available to you for providing software updates for the applications in the deployed MED-V workspace.</span></span>

<span data-ttu-id="0face-105">**Nota:**  Para obtener información sobre cómo especificar las opciones de configuración que definen cómo el MED-V recibe actualizaciones automáticas, consulte [Administración de actualizaciones automáticas para áreas de trabajo de Med-v](managing-automatic-updates-for-med-v-workspaces.md).</span><span class="sxs-lookup"><span data-stu-id="0face-105">**Note** For information about how to specify the configuration settings that define how MED-V receives automatic updates, see [Managing Automatic Updates for MED-V Workspaces](managing-automatic-updates-for-med-v-workspaces.md).</span></span>

 

**<span data-ttu-id="0face-106">Actualización de software en un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="0face-106">Updating Software in a MED-V Workspace</span></span>**

1.  **<span data-ttu-id="0face-107">Uso de un sistema electrónico de distribución de software</span><span class="sxs-lookup"><span data-stu-id="0face-107">Using an Electronic Software Distribution System</span></span>**

    <span data-ttu-id="0face-108">Si su organización usa un sistema de sistema de distribución de software electrónico (ESD) para implementar software, puede usarlo para proporcionar actualizaciones de software para las aplicaciones en áreas de trabajo de MED-V, de la misma forma en que proporciona actualizaciones para aplicaciones en equipos físicos.</span><span class="sxs-lookup"><span data-stu-id="0face-108">If your organization uses an Electronic Software Distribution System (ESD) system to deploy software, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

2.  **<span data-ttu-id="0face-109">Uso de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="0face-109">Using Group Policy</span></span>**

    <span data-ttu-id="0face-110">Si su organización implementa software mediante una directiva de grupo, puede usarlo para proporcionar actualizaciones de software para las aplicaciones en áreas de trabajo de MED-V, de la misma forma en que proporciona actualizaciones para las aplicaciones en equipos físicos.</span><span class="sxs-lookup"><span data-stu-id="0face-110">If your organization deploys software by using Group Policy, you can use it to provide software updates for applications on MED-V workspaces just as you provide updates for applications on physical computers.</span></span>

3.  **<span data-ttu-id="0face-111">Usar la virtualización de aplicaciones (APP-V)</span><span class="sxs-lookup"><span data-stu-id="0face-111">Using Application Virtualization (APP-V)</span></span>**

    <span data-ttu-id="0face-112">Si usa MED-V junto con App-V, puede proporcionar actualizaciones de software para las aplicaciones en el área de trabajo de MED-V siguiendo los pasos que necesita App-V para actualizar el software.</span><span class="sxs-lookup"><span data-stu-id="0face-112">If you use MED-V together with App-V, you can provide software updates to applications in the MED-V workspace by following the steps that are required by App-V for updating software.</span></span> <span data-ttu-id="0face-113">Para obtener más información, consulte [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) ( https://go.microsoft.com/fwlink/?LinkId=122939) .</span><span class="sxs-lookup"><span data-stu-id="0face-113">For more information, see [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939).</span></span>

4.  **<span data-ttu-id="0face-114">Actualización de software en la imagen principal</span><span class="sxs-lookup"><span data-stu-id="0face-114">Updating Software in the Core Image</span></span>**

    <span data-ttu-id="0face-115">Aunque no se considere una recomendación de MED-V, puede instalar actualizaciones de software en las aplicaciones de la imagen principal.</span><span class="sxs-lookup"><span data-stu-id="0face-115">Although not considered a MED-V best practice, you can install software updates to applications on the core image.</span></span> <span data-ttu-id="0face-116">Después de instalar las actualizaciones, puede volver a implementar el área de trabajo de MED-V en su empresa de la misma manera en que lo implementó originalmente.</span><span class="sxs-lookup"><span data-stu-id="0face-116">After you have installed the updates, you can then redeploy the MED-V workspace back out to your enterprise just as you deployed it originally.</span></span>

    <span data-ttu-id="0face-117">**Importante**  No se recomienda este método de administración de actualizaciones de software.</span><span class="sxs-lookup"><span data-stu-id="0face-117">**Important** We do not recommend this method of managing software updates.</span></span> <span data-ttu-id="0face-118">Además, si actualiza el software en la imagen principal y vuelve a implementar el área de trabajo de MED-V en su empresa, la configuración debe volver a ejecutarse y todos los datos guardados en la máquina virtual se perderán.</span><span class="sxs-lookup"><span data-stu-id="0face-118">In addition, if you update software in the core image and redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="0face-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0face-119">Related topics</span></span>


[<span data-ttu-id="0face-120">Administrar las actualizaciones automáticas para áreas de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="0face-120">Managing Automatic Updates for MED-V Workspaces</span></span>](managing-automatic-updates-for-med-v-workspaces.md)

[<span data-ttu-id="0face-121">Cómo probar la publicación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="0face-121">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="0face-122">Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="0face-122">How to Publish and Unpublish an Application on the MED-V Workspace</span></span>](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





