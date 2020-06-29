---
title: Requisitos previos de instalación de MED-V
description: Requisitos previos de instalación de MED-V
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824970"
---
# <span data-ttu-id="6e749-103">Requisitos previos de instalación de MED-V</span><span class="sxs-lookup"><span data-stu-id="6e749-103">MED-V Installation Prerequisites</span></span>


<span data-ttu-id="6e749-104">A continuación se enumeran los requisitos previos para instalar MED-V:</span><span class="sxs-lookup"><span data-stu-id="6e749-104">The following are prerequisites for installing MED-V:</span></span>

[<span data-ttu-id="6e749-105">Requisitos de Active Directory</span><span class="sxs-lookup"><span data-stu-id="6e749-105">Active Directory Requirements</span></span>](#bkmk-activedirectoryrequirements)

[<span data-ttu-id="6e749-106">Base de datos de informes</span><span class="sxs-lookup"><span data-stu-id="6e749-106">Report Database</span></span>](#bkmk-howtoinstallthereportdatabase)

[<span data-ttu-id="6e749-107">Configuración de software antivirus y de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="6e749-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

[<span data-ttu-id="6e749-108">Microsoft Virtual PC 2007 SP1</span><span class="sxs-lookup"><span data-stu-id="6e749-108">Microsoft Virtual PC 2007 SP1</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a><span data-ttu-id="6e749-109">Requisitos de Active Directory</span><span class="sxs-lookup"><span data-stu-id="6e749-109">Active Directory Requirements</span></span>


<span data-ttu-id="6e749-110">Al configurar el servidor de MED-V, si los usuarios no forman parte del mismo dominio al que pertenece el servidor, debe establecerse una confianza entre los dominios.</span><span class="sxs-lookup"><span data-stu-id="6e749-110">When configuring the MED-V server, if users are not part of the same domain the server belongs to, a trust must be set between the domains.</span></span>

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a><span data-ttu-id="6e749-111">Cómo instalar la base de datos de informes</span><span class="sxs-lookup"><span data-stu-id="6e749-111">How to Install the Report Database</span></span>


<span data-ttu-id="6e749-112">La base de datos de informes es necesaria para almacenar todos los registros del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="6e749-112">The report database is required for storing all MED-V workspace logs.</span></span> <span data-ttu-id="6e749-113">La base de datos de registro se usa para generar informes de MED-V.</span><span class="sxs-lookup"><span data-stu-id="6e749-113">The log database is then used for generating MED-V reports.</span></span> <span data-ttu-id="6e749-114">Para obtener información sobre los informes, vea [informes de MED-V](med-v-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="6e749-114">For information about reports, see [MED-V Reporting](med-v-reporting.md).</span></span>

<span data-ttu-id="6e749-115">SQL Server se puede instalar en el mismo servidor que el servidor de MED-V o en un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="6e749-115">SQL Server can be installed on the same server as the MED-V server or on a remote server.</span></span> <span data-ttu-id="6e749-116">Si va a instalar en un servidor remoto, consulte [instalar SQL Server en un servidor remoto](#bkmk-installingsqlserveronaremoteserver).</span><span class="sxs-lookup"><span data-stu-id="6e749-116">If installing on a remote server, see [Installing SQL Server on a Remote Server](#bkmk-installingsqlserveronaremoteserver).</span></span>

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a><span data-ttu-id="6e749-117">Instalar SQL Server en un servidor remoto</span><span class="sxs-lookup"><span data-stu-id="6e749-117">Installing SQL Server on a Remote Server</span></span>

**<span data-ttu-id="6e749-118">Para instalar SQL Server en un servidor remoto</span><span class="sxs-lookup"><span data-stu-id="6e749-118">To install SQL Server on a remote server</span></span>**

1.  <span data-ttu-id="6e749-119">Configure lo siguiente en el servidor remoto:</span><span class="sxs-lookup"><span data-stu-id="6e749-119">Configure the following on the remote server:</span></span>

    -   <span data-ttu-id="6e749-120">Nombre de instancia: instancia predeterminada</span><span class="sxs-lookup"><span data-stu-id="6e749-120">Instance name—Default instance</span></span>

    -   <span data-ttu-id="6e749-121">Modo de autenticación: modo mixto</span><span class="sxs-lookup"><span data-stu-id="6e749-121">Authentication mode—Mixed mode</span></span>

    -   <span data-ttu-id="6e749-122">Usuario: el usuario predeterminado creado es "SA"</span><span class="sxs-lookup"><span data-stu-id="6e749-122">User—The default user created is “sa”</span></span>

    -   <span data-ttu-id="6e749-123">Contraseña: contraseña deseada</span><span class="sxs-lookup"><span data-stu-id="6e749-123">Password—Desired password</span></span>

    -   <span data-ttu-id="6e749-124">Configuración de intercalación: predeterminada</span><span class="sxs-lookup"><span data-stu-id="6e749-124">Collation Settings—Default</span></span>

    -   <span data-ttu-id="6e749-125">Error en la configuración del informe de uso: predeterminado</span><span class="sxs-lookup"><span data-stu-id="6e749-125">Error in usage report settings—Default</span></span>

2.  <span data-ttu-id="6e749-126">Instale los siguientes archivos en el servidor MED-V:</span><span class="sxs-lookup"><span data-stu-id="6e749-126">Install the following files on the MED-V server:</span></span>

    -   <span data-ttu-id="6e749-127">Para instalar los requisitos previos para la colección de objetos del módulo de administración para Microsoft SQL Server2008, descargue el [cliente nativo de Microsoft SQL Server2008](https://go.microsoft.com/fwlink/?LinkId=164039) desde el centro de descarga de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6e749-127">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2008, download [Microsoft SQL Server2008 Native Client](https://go.microsoft.com/fwlink/?LinkId=164039) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="6e749-128">Para instalar los requisitos previos para la colección de objetos del módulo de administración para Microsoft SQL Server2005, descargue el [cliente nativo de Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=164038) desde el centro de descarga de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6e749-128">To install the prerequisites for the management pack objects collection for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Native Client](https://go.microsoft.com/fwlink/?LinkId=164038) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="6e749-129">Para instalar los archivos dll necesarios para Microsoft SQL Server2008, descargue la [recopilación de objetos de administración de Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=164041) desde el centro de descarga de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6e749-129">To install the required dll files for Microsoft SQL Server2008, download [Microsoft SQL Server 2008 Management Objects Collection](https://go.microsoft.com/fwlink/?LinkId=164041) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="6e749-130">Para instalar los archivos dll necesarios para Microsoft SQL Server2005, descargue los [objetos de administración de Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=164040) desde el centro de descarga de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6e749-130">To install the required dll files for Microsoft SQL Server2005, download [Microsoft SQL Server2005 Management Objects](https://go.microsoft.com/fwlink/?LinkId=164040) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="6e749-131">Para instalar los paquetes de instalación independientes que proporcionan valor adicional para SQL Server2008, descargue el [paquete de características de Microsoft SQL Server2008](https://go.microsoft.com/fwlink/?LinkId=163960) desde el centro de descarga de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6e749-131">To install the stand-alone install packages that provide additional value for SQL Server2008, download the [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) from the Microsoft Download Center.</span></span>

    -   <span data-ttu-id="6e749-132">Para instalar los paquetes de instalación independientes que proporcionan valor adicional para SQL Server2005, descargue el [Feature Pack para Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) desde el centro de descarga de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6e749-132">To install the stand-alone install packages that provide additional value for SQL Server2005, download the [Feature Pack for Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) from the Microsoft Download Center.</span></span>

    <span data-ttu-id="6e749-133">Para obtener más información sobre estos archivos, consulte [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) en el centro de descarga de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163960) o [Feature Pack para Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) en el centro de descarga de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163961) .</span><span class="sxs-lookup"><span data-stu-id="6e749-133">For more information about these files, see [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163960) or [Feature Pack for Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) on the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=163961).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="6e749-134">Configuración de software antivirus y de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="6e749-134">Antivirus/Backup Software Configuration</span></span>


<span data-ttu-id="6e749-135">Para evitar que la actividad antivirus afecte al rendimiento del escritorio virtual, se recomienda siempre que sea posible excluir los siguientes tipos de archivo de máquina virtual de cualquier procesamiento de copia de seguridad o antivirus que se ejecute en el host:</span><span class="sxs-lookup"><span data-stu-id="6e749-135">To prevent antivirus activity from affecting the performance of the virtual desktop, it is recommended where possible to exclude the following virtual machine file types from any antivirus or backup processing running on the host:</span></span>

-   <span data-ttu-id="6e749-136">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="6e749-136">\*.VMC</span></span>

-   <span data-ttu-id="6e749-137">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="6e749-137">\*.VUD</span></span>

-   <span data-ttu-id="6e749-138">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="6e749-138">\*.VSV</span></span>

-   <span data-ttu-id="6e749-139">\*. CKM</span><span class="sxs-lookup"><span data-stu-id="6e749-139">\*.CKM</span></span>

-   <span data-ttu-id="6e749-140">\*. EVHD</span><span class="sxs-lookup"><span data-stu-id="6e749-140">\*.EVHD</span></span>

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a><span data-ttu-id="6e749-141">Cómo instalar y configurar Microsoft Virtual PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="6e749-141">How to Install and Configure Microsoft Virtual PC2007 SP1</span></span>


<span data-ttu-id="6e749-142">**Importante**  Si Virtual PC para Windows existe en el equipo host, desinstálelo antes de instalar virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="6e749-142">**Important** If Virtual PC for Windows exists on the host computer, uninstall it before installing Virtual PC2007 SP1.</span></span>

 

**<span data-ttu-id="6e749-143">Para instalar Microsoft Virtual PC2007 SP1</span><span class="sxs-lookup"><span data-stu-id="6e749-143">To install Microsoft Virtual PC2007 SP1</span></span>**

1.  <span data-ttu-id="6e749-144">Descargue Virtual PC2007 SP1 desde el centro de descarga de Microsoft [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).</span><span class="sxs-lookup"><span data-stu-id="6e749-144">Download Virtual PC2007 SP1 from the Microsoft Download Center [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).</span></span>

2.  <span data-ttu-id="6e749-145">Ejecute el archivo de instalación en el equipo host y siga el asistente.</span><span class="sxs-lookup"><span data-stu-id="6e749-145">Run the installation file on the host computer, and follow the wizard.</span></span>

3.  <span data-ttu-id="6e749-146">Instale la actualización de virtual PC2007 SP1 en el equipo host en modo elevado.</span><span class="sxs-lookup"><span data-stu-id="6e749-146">Install Virtual PC2007 SP1 update on the host computer in elevated mode.</span></span>

    <span data-ttu-id="6e749-147">Para obtener más información, consulte [la descripción del paquete de revisiones para Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).</span><span class="sxs-lookup"><span data-stu-id="6e749-147">For more information, see [the description of the hotfix package for Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).</span></span>

    <span data-ttu-id="6e749-148">**Nota:**  La actualización de virtual PC2007 SP1 es necesaria para ejecutar virtual PC2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="6e749-148">**Note** The Virtual PC2007 SP1 update is required for running Virtual PC2007 SP1.</span></span>

     

## <span data-ttu-id="6e749-149">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e749-149">Related topics</span></span>


[<span data-ttu-id="6e749-150">Configuraciones admitidas</span><span class="sxs-lookup"><span data-stu-id="6e749-150">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

 

 





