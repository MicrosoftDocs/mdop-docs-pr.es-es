---
title: Cómo implementar un área de trabajo de MED-V en una imagen de Windows 7
description: Cómo implementar un área de trabajo de MED-V en una imagen de Windows 7
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827281"
---
# <span data-ttu-id="5c922-103">Cómo implementar un área de trabajo de MED-V en una imagen de Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c922-103">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>


<span data-ttu-id="5c922-104">Puede instalar todos los componentes de MED-V en una imagen de Windows 7 que distribuya por toda la empresa, como lo haría en cualquier nueva instalación de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5c922-104">You can install all the MED-V components into a Windows 7 image that you distribute throughout your enterprise just as you would any new installation of Windows 7.</span></span> <span data-ttu-id="5c922-105">Después, el usuario final finaliza la instalación del área de trabajo MED-V haciendo clic en el acceso directo del menú **Inicio** que configuró para iniciar Med-v.</span><span class="sxs-lookup"><span data-stu-id="5c922-105">The end user then finishes the installation of the MED-V workspace by clicking a **Start** menu shortcut that you configure to start MED-V.</span></span> <span data-ttu-id="5c922-106">La configuración comienza por la primera vez que el usuario final sigue las instrucciones para completar la configuración.</span><span class="sxs-lookup"><span data-stu-id="5c922-106">First time setup starts and the end user follows the instructions to complete the configuration.</span></span>

<span data-ttu-id="5c922-107">La siguiente sección proporciona información e instrucciones para ayudarle a implementar el área de trabajo de MED-V en toda su empresa con una imagen de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5c922-107">The following section provides information and instructions to help you deploy the MED-V workspace throughout your enterprise by using a Windows 7 image.</span></span>

**<span data-ttu-id="5c922-108">Para implementar un área de trabajo de MED-V en una imagen de Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c922-108">To deploy a MED-V workspace in a Windows 7 image</span></span>**

1.  <span data-ttu-id="5c922-109">Crear una imagen estándar de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5c922-109">Create a standard image of Windows 7.</span></span> <span data-ttu-id="5c922-110">Para obtener más información, consulte [creación de una imagen estándar de Windows 7: guía paso a paso](https://go.microsoft.com/fwlink/?LinkId=204843) ( https://go.microsoft.com/fwlink/?LinkId=204843) .</span><span class="sxs-lookup"><span data-stu-id="5c922-110">For more information, see [Building a Standard Image of Windows 7: Step-by-Step Guide](https://go.microsoft.com/fwlink/?LinkId=204843) (https://go.microsoft.com/fwlink/?LinkId=204843).</span></span>

2.  <span data-ttu-id="5c922-111">En la imagen de Windows 7, instale Windows Virtual PC y las actualizaciones de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="5c922-111">In the Windows 7 image, install Windows Virtual PC and the Windows Virtual PC updates.</span></span> <span data-ttu-id="5c922-112">Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="5c922-112">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

3.  <span data-ttu-id="5c922-113">Instale el agente de host MED-V usando el archivo de instalación MED-V \ _HostAgent \ _Setup.</span><span class="sxs-lookup"><span data-stu-id="5c922-113">Install the MED-V Host Agent by using the MED-V\_HostAgent\_Setup installation file.</span></span> <span data-ttu-id="5c922-114">Para obtener más información, vea [Cómo instalar manualmente el agente de host MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="5c922-114">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

    <span data-ttu-id="5c922-115">**ADVERTENCIA**  Internet Explorer debe cerrarse antes de instalar el agente de host MED-V; de lo contrario, los conflictos pueden producirse posteriormente con el redireccionamiento de URL.</span><span class="sxs-lookup"><span data-stu-id="5c922-115">**Warning** Internet Explorer must be closed before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="5c922-116">También puede hacerlo especificando un reinicio del equipo durante una distribución.</span><span class="sxs-lookup"><span data-stu-id="5c922-116">You can also do this by specifying a computer restart during a distribution.</span></span>

     

4.  <span data-ttu-id="5c922-117">Copie los archivos de paquete del área de trabajo de MED-V en la imagen de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5c922-117">Copy the MED-V workspace package files to the Windows 7 image.</span></span> <span data-ttu-id="5c922-118">Los archivos de paquete del área de trabajo de MED-V son el instalador del área de trabajo de MED-V, el archivo. medv y el archivo setup.exe que ha creado con el **Empaquetador de área de trabajo de Med-v**.</span><span class="sxs-lookup"><span data-stu-id="5c922-118">The MED-V workspace package files are the MED-V workspace installer, .medv file, and setup.exe file that you created by using the **MED-V Workspace Packager**.</span></span>

    <span data-ttu-id="5c922-119">**Importante**  El archivo. medv y setup.exe debe estar en la misma carpeta que el instalador del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="5c922-119">**Important** The .medv and setup.exe file must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="5c922-120">A continuación, instale el área de trabajo de MED-V ejecutando setup.exe.</span><span class="sxs-lookup"><span data-stu-id="5c922-120">Then, install the MED-V workspace by running setup.exe.</span></span>

     

5.  <span data-ttu-id="5c922-121">Configure un acceso directo en el menú **Inicio** para abrir la instalación del paquete de área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="5c922-121">Configure a shortcut on the **Start** menu to open the MED-V workspace package installation.</span></span>

    <span data-ttu-id="5c922-122">Cree un acceso directo al menú **Inicio** para el setup.exe archivo que permita al usuario final iniciar una instalación de MED-V según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="5c922-122">Create a **Start** menu shortcut to the setup.exe file that lets the end user start a MED-V installation as required.</span></span>

6.  <span data-ttu-id="5c922-123">Con el proceso de implementación de imágenes estándar de su empresa, distribuya la imagen de Windows 7 a los equipos de su empresa que necesiten MED-V.</span><span class="sxs-lookup"><span data-stu-id="5c922-123">By using your company’s standard image deployment process, distribute the Windows 7 image to computers in your enterprise that require MED-V.</span></span>

<span data-ttu-id="5c922-124">Cuando el usuario final tiene que acceder a una aplicación publicada en el área de trabajo de MED-V, puede hacer clic en el acceso directo del menú **Inicio** para instalar el área de trabajo de Med-v.</span><span class="sxs-lookup"><span data-stu-id="5c922-124">When the end user has to access an application published in the MED-V workspace, they can click the **Start** menu shortcut to install the MED-V workspace.</span></span> <span data-ttu-id="5c922-125">Esto se inicia automáticamente la primera configuración y completa la configuración de MED-V.</span><span class="sxs-lookup"><span data-stu-id="5c922-125">This automatically starts first time setup and completes the configuration of MED-V.</span></span> <span data-ttu-id="5c922-126">Una vez completada la configuración, el usuario final puede acceder a las aplicaciones de MED-V en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="5c922-126">After first time setup is complete, the end user can access the MED-V applications on the **Start** menu.</span></span>

## <span data-ttu-id="5c922-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c922-127">Related topics</span></span>


[<span data-ttu-id="5c922-128">Introducción a la implementación MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="5c922-128">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="5c922-129">Cómo implementar un área de trabajo de MED-V a través de un sistema de distribución electrónica de Software</span><span class="sxs-lookup"><span data-stu-id="5c922-129">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 





