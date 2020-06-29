---
title: Solución de problemas de actualizaciones de AGPM
description: Solución de problemas de actualizaciones de AGPM
author: dansimp
ms.assetid: 1abbf0c1-fd32-46a8-a3ba-c005f066523d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2089eac51803dca60da51f61ebdb112fbf0bda08
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818250"
---
# <span data-ttu-id="7c988-103">Solución de problemas de actualizaciones de AGPM</span><span class="sxs-lookup"><span data-stu-id="7c988-103">Troubleshooting AGPM Upgrades</span></span>

<span data-ttu-id="7c988-104">En esta sección se enumeran los problemas comunes que pueden surgir al actualizar el servidor de administración de directivas de grupo (AGPM) avanzado a una versión más reciente (por ejemplo, AGPM 4,0 a AGPM 4,3).</span><span class="sxs-lookup"><span data-stu-id="7c988-104">This section lists common issues that you may encounter when you upgrade your Advanced Group Policy Management (AGPM) server to a newer version (e.g. AGPM 4.0 to AGPM 4.3).</span></span> <span data-ttu-id="7c988-105">Para diagnosticar problemas que no se encuentran aquí, puede ser útil ver la [solución de problemas AGPM](troubleshooting-agpm-agpm40.md) o un administrador AGPM (control total) para usar el registro y el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="7c988-105">To diagnose issues not listed here, it may be helpful to view the [Troubleshooting AGPM](troubleshooting-agpm-agpm40.md) or for an AGPM Administrator (Full Control) to use logging and tracing.</span></span> <span data-ttu-id="7c988-106">Para obtener más información, vea [configurar el registro y el seguimiento](configure-logging-and-tracing-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="7c988-106">For more information, see [Configure Logging and Tracing](configure-logging-and-tracing-agpm40.md).</span></span>

## <span data-ttu-id="7c988-107">¿Qué problemas tienes?</span><span class="sxs-lookup"><span data-stu-id="7c988-107">What problems are you having?</span></span>

-   [<span data-ttu-id="7c988-108">Error al generar un informe de diferencias de GPO HTML (código de error 80004003)</span><span class="sxs-lookup"><span data-stu-id="7c988-108">Failed to generate a HTML GPO difference report (Error code 80004003)</span></span>](#bkmk-error-80004003)

### <a href="" id="bkmk-error-80004003"></a><span data-ttu-id="7c988-109">Error al generar un informe de diferencias de GPO HTML (código de error 80004003)</span><span class="sxs-lookup"><span data-stu-id="7c988-109">Failed to generate a HTML GPO difference report (Error code 80004003)</span></span>

-   <span data-ttu-id="7c988-110">**Causa**: ha instalado el paquete de actualización de AGPM con una cuenta incorrecta.</span><span class="sxs-lookup"><span data-stu-id="7c988-110">**Cause**: You have installed the AGPM upgrade package with an incorrect account.</span></span>

-   <span data-ttu-id="7c988-111">**Solución**: debe ser administrador de AGPM para poder corregir este problema.</span><span class="sxs-lookup"><span data-stu-id="7c988-111">**Solution**: You will need to be an AGPM administrator in order to fix this issue.</span></span>
    
    -   <span data-ttu-id="7c988-112">Asegúrese de que conoce el nombre de usuario & la contraseña de su **cuenta de servicio de AGPM**.</span><span class="sxs-lookup"><span data-stu-id="7c988-112">Ensure you know the username & password of your **AGPM service account**.</span></span>

    -   <span data-ttu-id="7c988-113">Inicie sesión en su servidor de AGPM de forma interactiva como su cuenta de servicio de AGPM.</span><span class="sxs-lookup"><span data-stu-id="7c988-113">Log onto your AGPM server interactively as your AGPM service account.</span></span>
        
        -   <span data-ttu-id="7c988-114">Esto es muy importante, ya que se producirá un error en la instalación si usas una cuenta diferente.</span><span class="sxs-lookup"><span data-stu-id="7c988-114">This is critically important, as the install will fail if you use a different account.</span></span>

    -   <span data-ttu-id="7c988-115">Cierre el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="7c988-115">Shutdown the AGPM service.</span></span>
    
    -   <span data-ttu-id="7c988-116">Instale el Hotfix requerido.</span><span class="sxs-lookup"><span data-stu-id="7c988-116">Install the required hotfix.</span></span>
    
    -   <span data-ttu-id="7c988-117">Conéctese a AGPM con un cliente de AGPM para comprobar que los informes de diferencias ya están funcionando.</span><span class="sxs-lookup"><span data-stu-id="7c988-117">Connect to AGPM using an AGPM client to test that your difference reports are now functioning.</span></span>
    
## <span data-ttu-id="7c988-118">Instalar el paquete de revisiones 1 para Microsoft Advanced Group Policy Management 4,0 SP3</span><span class="sxs-lookup"><span data-stu-id="7c988-118">Install Hotfix Package 1 for Microsoft Advanced Group Policy Management 4.0 SP3</span></span>
    
<span data-ttu-id="7c988-119">**Problema corregido en este Hotfix**: AGPM no puede generar informes de diferencias al controlar o administrar nuevos objetos de directiva de grupo (GPO).</span><span class="sxs-lookup"><span data-stu-id="7c988-119">**Issue fixed in this hotfix**: AGPM can't generate difference reports when it controls or manages new Group Policy Objects (GPOs).</span></span>

<span data-ttu-id="7c988-120">**Cómo obtener esta actualización**: Instale la última versión de Microsoft Desktop Optimization Pack ([lanzamiento de marzo de 2017 de servicio](https://www.microsoft.com/download/details.aspx?id=54967)).</span><span class="sxs-lookup"><span data-stu-id="7c988-120">**How to get this update**: Install the latest version of Microsoft Desktop Optimization Pack ([March 2017 Servicing Release](https://www.microsoft.com/download/details.aspx?id=54967)).</span></span> <span data-ttu-id="7c988-121">Para obtener más información, consulte [KB 4014009](https://support.microsoft.com/help/4014009/) .</span><span class="sxs-lookup"><span data-stu-id="7c988-121">See [KB 4014009](https://support.microsoft.com/help/4014009/) for more information.</span></span>

<span data-ttu-id="7c988-122">Más específicamente, puedes elegir descargar solo el primer archivo, `AGPM4.0SP1_Server_X64_KB4014009.exe` en la lista que aparece después de pulsar el botón Descargar.</span><span class="sxs-lookup"><span data-stu-id="7c988-122">More specifically, you can choose to download only the first file, `AGPM4.0SP1_Server_X64_KB4014009.exe`, from the list presented after pressing the download button.</span></span>
      
<span data-ttu-id="7c988-123">El vínculo de descarga del paquete de optimización de escritorio de Microsoft (lanzamiento de marzo de 2017 de servicio) se puede encontrar [aquí](https://www.microsoft.com/download/details.aspx?id=54967).</span><span class="sxs-lookup"><span data-stu-id="7c988-123">The download link to the Microsoft Desktop Optimization Pack (March 2017 Servicing Release) can be found [here](https://www.microsoft.com/download/details.aspx?id=54967).</span></span>
      
      
## <span data-ttu-id="7c988-124">Vínculo de referencia</span><span class="sxs-lookup"><span data-stu-id="7c988-124">Reference link</span></span>
https://support.microsoft.com/help/3127165/hotfix-package-1-for-microsoft-advanced-group-policy-management-4-0-sp
      
