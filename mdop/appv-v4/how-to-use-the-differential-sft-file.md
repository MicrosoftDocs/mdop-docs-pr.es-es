---
title: Cómo usar el archivo SFT diferencial
description: Cómo usar el archivo SFT diferencial
author: dansimp
ms.assetid: 607e30fd-2f0e-4e2f-b669-0b3f010aebb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 85cc45f9665569d77fcf275db6dbc080eb919229
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816390"
---
# <span data-ttu-id="a46f3-103">Cómo usar el archivo SFT diferencial</span><span class="sxs-lookup"><span data-stu-id="a46f3-103">How to Use the Differential SFT File</span></span>


<span data-ttu-id="a46f3-104">Al secuenciar una aplicación, el secuenciador de Microsoft Application Virtualization (App-V) crea archivos SFT (. SFT) para almacenar toda la información de configuración y el contenido de los archivos de la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="a46f3-104">When sequencing an application, the Microsoft Application Virtualization (App-V) Sequencer creates SFT files (.sft) to store all of the virtual application’s files content and configuration information.</span></span> <span data-ttu-id="a46f3-105">En la versión 4.5 de App-V, se ha introducido el archivo de SFT diferencial (. dsft).</span><span class="sxs-lookup"><span data-stu-id="a46f3-105">In version4.5 of App-V, the Differential SFT (.dsft) file has been introduced.</span></span> <span data-ttu-id="a46f3-106">Después de usar el secuenciador para crear una actualización de un paquete existente, puede optar por generar este archivo para almacenar solo las diferencias entre el paquete de aplicación secuencial original y la nueva versión.</span><span class="sxs-lookup"><span data-stu-id="a46f3-106">After using the Sequencer to create an upgrade for an existing package, you can choose to generate this file to store only the differences between the original sequenced application package and the new version.</span></span> <span data-ttu-id="a46f3-107">Por lo tanto, es mucho más pequeño que el archivo SFT completo para la nueva versión de la aplicación y reduce el impacto de enviar actualizaciones de paquetes a través de conexiones de red con poco ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="a46f3-107">It is therefore much smaller than the full SFT file would be for the new version of the application and reduces the impact of sending package updates over low-bandwidth network connections.</span></span> <span data-ttu-id="a46f3-108">Sin embargo, su uso solo se admite en determinadas situaciones limitadas.</span><span class="sxs-lookup"><span data-stu-id="a46f3-108">However, its use is supported only in certain restricted situations.</span></span> <span data-ttu-id="a46f3-109">Esta característica estaba pensada para usarse específicamente donde se utiliza un sistema de distribución de software electrónico (ESD) para administrar un grupo de usuarios con un servidor de archivos local a través de una conexión de ancho de banda bajo y no se usan servidores de streaming de App-V.</span><span class="sxs-lookup"><span data-stu-id="a46f3-109">This feature was intended to be used specifically where you are using an electronic software distribution (ESD) system to manage a group of users with a local file server over a low-bandwidth connection and you are not using App-V streaming servers.</span></span>

<span data-ttu-id="a46f3-110">No es necesario usar el archivo SFT diferencial si está usando la configuración Manager2007 para administrar los usuarios, ya que Configuration Manager tiene compatibilidad con implementaciones con poco ancho de banda ya integradas.</span><span class="sxs-lookup"><span data-stu-id="a46f3-110">You do not need to use the Differential SFT file if you are using Configuration Manager2007 to manage the users, because Configuration Manager has support for low-bandwidth deployments already built in.</span></span> <span data-ttu-id="a46f3-111">Tampoco es necesario si usa la administración de Application Virtualization (App-V) o los servidores de streaming con la actualización activa porque el cliente solo recuperará las diferencias entre las versiones de paquete nuevas y anteriores.</span><span class="sxs-lookup"><span data-stu-id="a46f3-111">It is also not required if you are using Application Virtualization (App-V) Management or Streaming Servers with Active Upgrade because the client will retrieve only the differences between the old and new package versions.</span></span>

<span data-ttu-id="a46f3-112">El procedimiento siguiente muestra cómo usar el mkdiffpkg.exe que está incluido en la instalación del secuenciador para crear el archivo SFT diferencial, después de completar la actualización del paquete de aplicación virtual y para implementar el archivo SFT diferencial.</span><span class="sxs-lookup"><span data-stu-id="a46f3-112">The following procedure shows how to use the mkdiffpkg.exe that is included in the Sequencer installation to create the Differential SFT file, after completing the upgrade of the virtual application package, and to deploy the Differential SFT file.</span></span> <span data-ttu-id="a46f3-113">Completar este procedimiento ayuda a garantizar que si el paquete se descarga de alguna manera en el equipo cliente, la próxima vez que el usuario intente ejecutar la aplicación, el cliente volverá a la URL de invalidación, que está configurada para transmitir el paquete completo V2. SFT del recurso compartido de archivos local.</span><span class="sxs-lookup"><span data-stu-id="a46f3-113">Completing this procedure helps ensure that if the package is somehow unloaded from the client computer, the next time the user tries to run the application, the client will fall back to the override URL, which is set to stream the full package V2.sft from the local file share.</span></span> <span data-ttu-id="a46f3-114">Esto evitará que el usuario no haya podido iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a46f3-114">This will avoid any failure for the user when starting the application.</span></span> <span data-ttu-id="a46f3-115">Si todo el cliente se daña o se desinstala, se recomienda que el sistema de ESD esté configurado para implementar la versión completa del paquete actualizado, V2. SFT, al cliente.</span><span class="sxs-lookup"><span data-stu-id="a46f3-115">If the entire client becomes corrupted or is uninstalled, it is recommended that the ESD system be configured to deploy the full version of the upgraded package, V2.sft, to the client.</span></span>

<span data-ttu-id="a46f3-116">Para obtener más información sobre cómo actualizar un paquete, consulte "Cómo actualizar una aplicación virtual existente" en la guía de operaciones de App-V 4.5 en</span><span class="sxs-lookup"><span data-stu-id="a46f3-116">For more information about upgrading a package, see “How to Upgrade an Existing Virtual Application” in the App-V4.5 Operations Guide at</span></span> <https://go.microsoft.com/fwlink/?LinkId=133129>

<span data-ttu-id="a46f3-117">**Nota:**  Como requisito previo, todos los equipos de los usuarios a los que se dirige el ESD deben tener el archivo v1. SFT cargado completamente en su caché local, y la transmisión de archivos debe estar habilitada en todos los equipos.</span><span class="sxs-lookup"><span data-stu-id="a46f3-117">**Note** As a prerequisite, all user computers being targeted by the ESD must have the V1.sft file fully loaded into their local cache, and file streaming must be enabled on all computers.</span></span>

 

**<span data-ttu-id="a46f3-118">Para usar el archivo SFT diferencial</span><span class="sxs-lookup"><span data-stu-id="a46f3-118">To use the Differential SFT file</span></span>**

1.  <span data-ttu-id="a46f3-119">Inicie sesión en el equipo del secuenciador con una cuenta que tenga derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="a46f3-119">Log on to the Sequencer computer by using an account with administrator rights.</span></span> <span data-ttu-id="a46f3-120">Abra el paquete original (V1) para la actualización en el secuenciador y, a continuación, actualice el paquete a la nueva versión (V2) y guárdelo como un nuevo V2. SFT.</span><span class="sxs-lookup"><span data-stu-id="a46f3-120">Open the original package (V1) for upgrade in the Sequencer, and then upgrade the package to the new version (V2) and save it as a new V2.sft.</span></span>

2.  <span data-ttu-id="a46f3-121">Abra una ventana de comandos en la carpeta de instalación de App-V 4.5 Sequencer y ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="a46f3-121">Open a command window in the App-V4.5 Sequencer installation folder, and run the following command:</span></span>

    `“mkdiffpkg.exe V2.sft V2.dsft”`

3.  <span data-ttu-id="a46f3-122">Con el sistema ESD u otro proceso de copia de archivos, copie el archivo de contenido completo del paquete V2, V2. SFT, a un recurso compartido de archivos local al que puedan acceder los equipos del usuario en una conexión de red bien conectada.</span><span class="sxs-lookup"><span data-stu-id="a46f3-122">Using the ESD system or other file copy process, copy the full V2 package content file, V2.sft, to a local file share that is accessible to the user computers on a well-connected network connection.</span></span>

4.  <span data-ttu-id="a46f3-123">Con el sistema ESD, coloca una copia del archivo SFT diferencial, V2. dsft, en cada equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="a46f3-123">Using the ESD system, place a copy of the Differential SFT file, V2.dsft, on each user computer.</span></span>

5.  <span data-ttu-id="a46f3-124">Para importar el archivo V2. dsft, ejecute el siguiente comando de SFTMIME en cada equipo de usuario:</span><span class="sxs-lookup"><span data-stu-id="a46f3-124">To import the V2.dsft file, run the following SFTMIME command on each user computer:</span></span>

    `“SFTMIME load package:<package name> /SFTPATH <path to V2.dsft>”`

6.  <span data-ttu-id="a46f3-125">Ejecute el siguiente comando SFTMIME en cada equipo del usuario para configurar la dirección URL de reemplazo para que apunte al archivo V2. SFT:</span><span class="sxs-lookup"><span data-stu-id="a46f3-125">Run the following SFTMIME command on each user computer to set the override URL to point to the V2.sft file:</span></span>

    `“SFTMIME configure package:<package name> /OverrideURL FILE://<network path to V2.sft>”`

**<span data-ttu-id="a46f3-126">Nota</span><span class="sxs-lookup"><span data-stu-id="a46f3-126">Note</span></span>**  
-   <span data-ttu-id="a46f3-127">Los archivos de SFT diferencial deben aplicarse a los clientes en el orden correcto.</span><span class="sxs-lookup"><span data-stu-id="a46f3-127">Differential SFT files must be applied to clients in the correct order.</span></span> <span data-ttu-id="a46f3-128">Por ejemplo, V2. dsft debe aplicarse a una aplicación v1 antes de que se aplique V3. dsft.</span><span class="sxs-lookup"><span data-stu-id="a46f3-128">For example, V2.dsft must be applied to a V1 application before V3.dsft is applied.</span></span>

-   <span data-ttu-id="a46f3-129">La función **generar paquete de Microsoft Windows Installer (MSI)** en el secuenciador no se puede usar con el archivo SFT diferencial.</span><span class="sxs-lookup"><span data-stu-id="a46f3-129">The **Generate Microsoft Windows Installer (MSI) Package** capability in the Sequencer cannot be used with the Differential SFT file.</span></span>

 

## <span data-ttu-id="a46f3-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a46f3-130">Related topics</span></span>


[<span data-ttu-id="a46f3-131">Cómo crear o actualizar aplicaciones virtuales con el secuenciador de App-V</span><span class="sxs-lookup"><span data-stu-id="a46f3-131">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





