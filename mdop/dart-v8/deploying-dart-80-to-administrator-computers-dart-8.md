---
title: Implementación de DaRT 8.0 en equipos de administrador
description: Implementación de DaRT 8.0 en equipos de administrador
author: dansimp
ms.assetid: f918ead8-742e-464a-8bf6-1fcedde66cae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0ab001f612f2257ecbd77c39319cc99c17d36197
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824121"
---
# <span data-ttu-id="a0966-103">Implementación de DaRT 8.0 en equipos de administrador</span><span class="sxs-lookup"><span data-stu-id="a0966-103">Deploying DaRT 8.0 to Administrator Computers</span></span>


<span data-ttu-id="a0966-104">Antes de comenzar con la implementación de Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0, revise los requisitos de su entorno.</span><span class="sxs-lookup"><span data-stu-id="a0966-104">Before you begin the deployment of Microsoft Diagnostics and Recovery Toolset (DaRT) 8.0, review the requirements for your environment.</span></span> <span data-ttu-id="a0966-105">Esto incluye los requisitos de hardware para instalar DaRT 8,0.</span><span class="sxs-lookup"><span data-stu-id="a0966-105">This includes the hardware requirements for installing DaRT 8.0.</span></span> <span data-ttu-id="a0966-106">Para obtener más información sobre los requisitos de hardware y software de DaRT, consulte [dart 8,0 configuraciones admitidas](dart-80-supported-configurations-dart-8.md).</span><span class="sxs-lookup"><span data-stu-id="a0966-106">For more information about DaRT hardware and software requirements, see [DaRT 8.0 Supported Configurations](dart-80-supported-configurations-dart-8.md).</span></span>

<span data-ttu-id="a0966-107">Los temas de esta sección se pueden usar para ayudarle a implementar DaRT en su empresa en función de su entorno y su estrategia de implementación.</span><span class="sxs-lookup"><span data-stu-id="a0966-107">The topics in this section can be used to help you deploy DaRT in your enterprise based on your environment and deployment strategy.</span></span>

## <span data-ttu-id="a0966-108">Implementar DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="a0966-108">Deploy DaRT 8.0</span></span>


<span data-ttu-id="a0966-109">Puede usar el archivo de Windows Installer para que DaRT Instale DaRT en un equipo que usará para crear primero la imagen de recuperación de DaRT y, después, para solucionar y corregir los equipos de los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="a0966-109">You can use the Windows Installer file for DaRT to install DaRT on a computer that you will use to first create the DaRT recovery image and then troubleshoot and fix end-user computers.</span></span> <span data-ttu-id="a0966-110">Con frecuencia, en toda una organización, puede instalar en el equipo administrador solo la funcionalidad de DaRT que necesita para crear una imagen de recuperación de DaRT.</span><span class="sxs-lookup"><span data-stu-id="a0966-110">Frequently, across an organization, you might install on the administrator computer only the DaRT functionality that you need to create a DaRT recovery image.</span></span> <span data-ttu-id="a0966-111">A continuación, en un equipo de administrador del servicio de asistencia, es posible que solo Instale la funcionalidad de DaRT que necesita para solucionar un problema de equipo, como el visor de conexión remota DaRT y el analizador de bloqueos.</span><span class="sxs-lookup"><span data-stu-id="a0966-111">Then, on a help desk administrator’s computer, you might install only the DaRT functionality that you must have to troubleshoot a problem computer, such as the DaRT Remote Connection Viewer and the Crash Analyzer.</span></span>

<span data-ttu-id="a0966-112">Además de ejecutar manualmente el archivo de Windows Installer para instalar DaRT, también puede instalar DaRT en el símbolo del sistema para admitir sistemas de implementación de software empresarial, como SystemCenterConfigurationManager2012.</span><span class="sxs-lookup"><span data-stu-id="a0966-112">In addition to manually running the Windows Installer file to install DaRT, you can also install DaRT at the command prompt to support enterprise software deployment systems such as SystemCenterConfigurationManager2012.</span></span>

[<span data-ttu-id="a0966-113">Cómo implantar DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="a0966-113">How to Deploy DaRT 8.0</span></span>](how-to-deploy-dart-80-dart-8.md)

## <span data-ttu-id="a0966-114">Cambiar, reparar o quitar DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="a0966-114">Change, repair, or remove DaRT 8.0</span></span>


<span data-ttu-id="a0966-115">Puede cambiar, reparar o quitar la instalación de DaRT haciendo doble clic en el archivo de instalación de DaRT y, después, haciendo clic en el botón que corresponde a la acción que desea realizar o mediante el panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="a0966-115">You can change, repair, or remove the DaRT installation by double-clicking the DaRT installation file and then clicking the button that corresponds to the action that you want to perform or through the Windows Control Panel.</span></span>

[<span data-ttu-id="a0966-116">Cómo cambiar, reparar o quitar DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="a0966-116">How to Change, Repair, or Remove DaRT 8.0</span></span>](how-to-change-repair-or-remove-dart-80-dart-8.md)

## <span data-ttu-id="a0966-117">Cómo obtener DaRT 8,0</span><span class="sxs-lookup"><span data-stu-id="a0966-117">How to get DaRT 8.0</span></span>


<span data-ttu-id="a0966-118">Para obtener el software de DaRT, consulte [Cómo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span><span class="sxs-lookup"><span data-stu-id="a0966-118">To get the DaRT software, see [How to Get MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).</span></span>

## <span data-ttu-id="a0966-119">Otros recursos para implementar el DaRT 8,0 en equipos de administración</span><span class="sxs-lookup"><span data-stu-id="a0966-119">Other resources for deploying the DaRT 8.0 to administrator computers</span></span>


[<span data-ttu-id="a0966-120">Implementación de DaRT 8.0</span><span class="sxs-lookup"><span data-stu-id="a0966-120">Deploying DaRT 8.0</span></span>](deploying-dart-80-dart-8.md)

 

 





