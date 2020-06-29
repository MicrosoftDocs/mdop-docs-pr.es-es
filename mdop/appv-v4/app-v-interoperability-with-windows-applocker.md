---
title: Interoperabilidad de App-V con Windows AppLocker
description: Interoperabilidad de App-V con Windows AppLocker
author: dansimp
ms.assetid: 9a488034-607d-411c-b495-ff184c726f49
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6f67bb87c0a4474acee3c4982b65c930e86c4917
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822311"
---
# <span data-ttu-id="6f65e-103">Interoperabilidad de App-V con Windows AppLocker</span><span class="sxs-lookup"><span data-stu-id="6f65e-103">App-V Interoperability with Windows AppLocker</span></span>


<span data-ttu-id="6f65e-104">La versión 4,5 del cliente de Microsoft Application Virtualization (App-V) es compatible con la característica AppLocker de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6f65e-104">Version 4.5 SP1 of the Microsoft Application Virtualization (App-V) client supports the AppLocker feature of Windows 7.</span></span> <span data-ttu-id="6f65e-105">La característica AppLocker permite a los administradores de ti especificar qué aplicaciones están restringidas para su ejecución en equipos.</span><span class="sxs-lookup"><span data-stu-id="6f65e-105">The AppLocker feature enables IT administrators to specify which applications are restricted from running on computers.</span></span> <span data-ttu-id="6f65e-106">En este documento se describe cómo configurar las reglas de AppLocker para que funcionen con el entorno virtual de App-V y las aplicaciones virtualizadas.</span><span class="sxs-lookup"><span data-stu-id="6f65e-106">This document describes how to configure the AppLocker rules to work with the App-V virtual environment and virtualized applications.</span></span>

<span data-ttu-id="6f65e-107">**Nota:**  Windows AppLocker debe habilitarse primero antes de configurar las reglas de Windows AppLocker para las aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="6f65e-107">**Note** Windows AppLocker must first be enabled before configuring Windows AppLocker rules for virtual applications.</span></span> <span data-ttu-id="6f65e-108">Para obtener más información sobre cómo habilitar Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) ( https://go.microsoft.com/fwlink/?LinkId=156732) .</span><span class="sxs-lookup"><span data-stu-id="6f65e-108">For more information about enabling Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) (https://go.microsoft.com/fwlink/?LinkId=156732).</span></span>

 

## <span data-ttu-id="6f65e-109">Configuración de reglas de Windows AppLocker para aplicaciones virtuales</span><span class="sxs-lookup"><span data-stu-id="6f65e-109">Configuring Windows AppLocker Rules for Virtual Applications</span></span>


<span data-ttu-id="6f65e-110">Los administradores locales pueden crear reglas de Windows AppLocker que restringen la ejecución de programas ejecutables (archivos. exe), archivos de Windows Installer (archivos. msi y. msp) y scripts (archivos. PS,. bat,. cmd,. vbs y. js).</span><span class="sxs-lookup"><span data-stu-id="6f65e-110">Local administrators can create Windows AppLocker rules that restrict the running of program executables (.exe files), Windows Installer files (.msi and .msp files), and scripts (.ps, .bat, .cmd, .vbs and .js files).</span></span> <span data-ttu-id="6f65e-111">El administrador realiza esta acción usando un equipo de referencia que tiene el cliente de App-V instalado y que tiene todas las aplicaciones virtuales relevantes transmitidas a la memoria caché del cliente.</span><span class="sxs-lookup"><span data-stu-id="6f65e-111">The administrator does this by using a reference computer that has the App-V client installed and that has all the relevant virtual applications streamed to the client cache.</span></span> <span data-ttu-id="6f65e-112">Después, el administrador usa la sección Windows AppLocker del complemento de Microsoft Management Console (MMC) Directiva de seguridad local en el equipo de referencia para crear las reglas.</span><span class="sxs-lookup"><span data-stu-id="6f65e-112">The administrator then uses the Windows AppLocker section of the Local Security Policy Microsoft Management Console (MMC) snap-in on the reference computer to create the rules.</span></span>

<span data-ttu-id="6f65e-113">Al examinar para buscar una ruta de acceso de directorio o un archivo específico para el que desea crear una regla, puede acceder a la unidad de App-V usando la ruta de acceso al recurso compartido oculto.</span><span class="sxs-lookup"><span data-stu-id="6f65e-113">When you browse to find a directory path or specific file for which you want to create a rule, you can access the App-V drive by using the path to the hidden share.</span></span> <span data-ttu-id="6f65e-114">Por ejemplo, puedes ir a \\\\localhost\\Q $, donde la unidad de App-V es la unidad Q. Sin embargo, para crear la regla, debe editar la ruta de acceso para quitar la referencia a \\\\localhost\\Q $ y usar Q:\\ en su lugar.</span><span class="sxs-lookup"><span data-stu-id="6f65e-114">For example, you can browse to \\\\localhost\\Q$, where the App-V drive is drive Q. However, to create the rule, you must edit the path to remove the reference to \\\\localhost\\Q$ and use Q:\\ instead.</span></span> <span data-ttu-id="6f65e-115">Para poder acceder a los archivos de la aplicación, debe iniciar cada una de las aplicaciones en el equipo de referencia y es necesario disponer de derechos administrativos para ir a \\\\localhost\\Q $.</span><span class="sxs-lookup"><span data-stu-id="6f65e-115">You must start each application on the reference computer to access the application’s files, and administrative rights are required to browse to \\\\localhost\\Q$.</span></span>

 

 





