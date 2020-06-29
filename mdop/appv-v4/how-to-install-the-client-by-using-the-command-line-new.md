---
title: Cómo instalar el cliente mediante el uso de la línea de comandos
description: Cómo instalar el cliente mediante el uso de la línea de comandos
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817321"
---
# <span data-ttu-id="41d20-103">Cómo instalar el cliente mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="41d20-103">How to Install the Client by Using the Command Line</span></span>


<span data-ttu-id="41d20-104">En los temas de esta sección se incluyen procedimientos para instalar el cliente de escritorio de Application Virtualization (App-V) o el cliente de App-V para servicios de escritorio remoto (anteriormente servicios de Terminal Server) con setup.exe o setup.msi.</span><span class="sxs-lookup"><span data-stu-id="41d20-104">The topics in this section include procedures to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span> <span data-ttu-id="41d20-105">Los derechos administrativos son necesarios para ejecutar el programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="41d20-105">Administrative rights are required to run either setup program.</span></span>

<span data-ttu-id="41d20-106">Puede usar parámetros opcionales de la línea de comandos para aplicar valores de configuración específicos al cliente de App-V durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="41d20-106">You can use optional command-line parameters to apply specific configuration settings to the App-V client during the installation.</span></span> <span data-ttu-id="41d20-107">Para obtener más información sobre el uso de parámetros, consulte [parámetros de la línea de comandos del instalador de cliente de virtualización de aplicaciones](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="41d20-107">For more information about using parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span> <span data-ttu-id="41d20-108">Si ha aplicado la configuración del registro a un equipo antes de implementar un cliente, por ejemplo, mediante la Directiva de grupo, se conservan estas opciones de configuración y se aplican los parámetros adicionales de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="41d20-108">If you have applied registry settings to a computer before deploying a client—for example, by using Group Policy—these settings are retained and any additional command line parameters are applied.</span></span> <span data-ttu-id="41d20-109">Los valores del parámetro de la línea de comandos reemplazarán cualquier valor existente para la misma configuración.</span><span class="sxs-lookup"><span data-stu-id="41d20-109">Command line parameter values will replace any existing value for the same setting.</span></span>

<span data-ttu-id="41d20-110">**Nota:**  Al instalar el cliente de App-V para usarlo con una caché de solo lectura, por ejemplo, con una implementación de servidor VDI, debe establecer el parámetro *AUTOLOADTARGET* en None para evitar que el cliente intente actualizar aplicaciones cuando la caché es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41d20-110">**Note** When you install the App-V client to use with a read-only cache, for example with a VDI server implementation, you must set the *AUTOLOADTARGET* parameter to NONE to prevent the client from trying to update applications when the cache is read-only.</span></span>

 

<span data-ttu-id="41d20-111">Para obtener más información sobre la configuración de estos valores de parámetro después de la instalación, consulte [Cómo configurar la configuración del registro del cliente de App-v con la línea de comandos](https://go.microsoft.com/fwlink/?LinkId=169355) ( https://go.microsoft.com/fwlink/?LinkId=169355) en la guía de operaciones de Application Virtualization (App-v).</span><span class="sxs-lookup"><span data-stu-id="41d20-111">For more information about setting these parameter values after installation, see [How to Configure the App-V Client Registry Settings by Using the Command Line](https://go.microsoft.com/fwlink/?LinkId=169355) (https://go.microsoft.com/fwlink/?LinkId=169355) in the Application Virtualization (App-V) Operations Guide.</span></span>

<span data-ttu-id="41d20-112">**Nota:**  Si una opción de configuración en el equipo del usuario depende de la ruta de instalación del cliente, tenga en cuenta que el cliente de Application Virtualization (App-V) 4.5 copia sus archivos de instalación en una carpeta diferente de la de versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="41d20-112">**Note** If a configuration setting on the user’s computer depends on the client installation path, note that the Application Virtualization (App-V)4.5 client copies its installation files to a different folder than previous versions did.</span></span> <span data-ttu-id="41d20-113">De forma predeterminada, una nueva instalación del cliente de App-V 4.5 copiará sus archivos de instalación en la carpeta \\Archivos de Programa\\microsoft Application Virtualization Client.</span><span class="sxs-lookup"><span data-stu-id="41d20-113">By default, a new installation of the App-V4.5 client will copy its installation files to the \\Program Files\\Microsoft Application Virtualization Client folder.</span></span> <span data-ttu-id="41d20-114">Si ya está instalada una versión anterior del cliente, la ejecución del instalador del cliente de App-V 4,5 realizará una actualización del cliente existente mediante la carpeta de instalación existente.</span><span class="sxs-lookup"><span data-stu-id="41d20-114">If an earlier version of the client is already installed, running the App-V 4.5 client installer will perform an upgrade of the existing client using the existing installation folder.</span></span>

 

<span data-ttu-id="41d20-115">\ [Valor del token de plantilla \]</span><span class="sxs-lookup"><span data-stu-id="41d20-115">\[Template Token Value\]</span></span>

<span data-ttu-id="41d20-116">**Nota:**  Para la versión 4.6 de App-V y versiones posteriores, cuando el cliente de App-V está instalado, SFTLDR.DLL se copia en el directorio Windows\\system32.</span><span class="sxs-lookup"><span data-stu-id="41d20-116">**Note** For App-V version4.6 and later, when the App-V client is installed, SFTLDR.DLL is copied to the Windows\\system32 directory.</span></span> <span data-ttu-id="41d20-117">Si el cliente de App-V está instalado en un sistema de 64 bits, SFTLDR\_WOW64.DLL se copia en el directorio Windows\\SysWOW64.</span><span class="sxs-lookup"><span data-stu-id="41d20-117">If the App-V client is installed on a 64-bit system, SFTLDR\_WOW64.DLL is copied to the Windows\\SysWOW64 directory.</span></span>

 

<span data-ttu-id="41d20-118">\ [Valor del token de plantilla \]</span><span class="sxs-lookup"><span data-stu-id="41d20-118">\[Template Token Value\]</span></span>

## <span data-ttu-id="41d20-119">En esta sección</span><span class="sxs-lookup"><span data-stu-id="41d20-119">In This Section</span></span>


<span data-ttu-id="41d20-120">En los temas siguientes, se describe cómo instalar el cliente de escritorio de Application Virtualization (App-V) o el cliente de App-V para servicios de escritorio remoto (anteriormente servicios de Terminal Server) usando setup.exe o setup.msi.</span><span class="sxs-lookup"><span data-stu-id="41d20-120">The following topics describe how to install either the Application Virtualization (App-V) Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services) by using either setup.exe or setup.msi.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[<span data-ttu-id="41d20-121">Cómo instalar el cliente de App-V mediante el uso de Setup.exe</span><span class="sxs-lookup"><span data-stu-id="41d20-121">How to Install the App-V Client by Using Setup.exe</span></span>](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
<span data-ttu-id="41d20-122">Proporciona un procedimiento paso a paso para instalar el cliente de App-V con el programa setup.exe.</span><span class="sxs-lookup"><span data-stu-id="41d20-122">Provides a step-by-step procedure for installing the App-V client by using the setup.exe program.</span></span>

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[<span data-ttu-id="41d20-123">Cómo instalar el cliente de App-V mediante el uso de Setup.msi</span><span class="sxs-lookup"><span data-stu-id="41d20-123">How to Install the App-V Client by Using Setup.msi</span></span>](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
<span data-ttu-id="41d20-124">Proporciona procedimientos paso a paso para instalar cualquier software necesario y también el cliente de App-V mediante el programa de setup.msi.</span><span class="sxs-lookup"><span data-stu-id="41d20-124">Provides step-by-step procedures for installing any prerequisite software and also the App-V client by using the setup.msi program.</span></span>

## <span data-ttu-id="41d20-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="41d20-125">Related topics</span></span>


[<span data-ttu-id="41d20-126">Parámetros de línea de comandos de instalador de cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="41d20-126">Application Virtualization Client Installer Command-Line Parameters</span></span>](application-virtualization-client-installer-command-line-parameters.md)

[<span data-ttu-id="41d20-127">Cómo instalar manualmente el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="41d20-127">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="41d20-128">Cómo publicar una aplicación virtual en el cliente</span><span class="sxs-lookup"><span data-stu-id="41d20-128">How to Publish a Virtual Application on the Client</span></span>](how-to-publish-a-virtual-application-on-the-client.md)

[<span data-ttu-id="41d20-129">Cómo desinstalar el cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="41d20-129">How to Uninstall the App-V Client</span></span>](how-to-uninstall-the-app-v-client.md)

 

 





