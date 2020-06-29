---
title: Implementar funciones necesarias para UE-V 2.x
description: Implementar funciones necesarias para UE-V 2.x
author: dansimp
ms.assetid: 10399bb3-cc7b-4578-bc0c-2f6b597abe4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f2123ec75fb151a8f5b836b9b2522a9d6090b043
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824670"
---
# <span data-ttu-id="fa228-103">Implementar funciones necesarias para UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="fa228-103">Deploy Required Features for UE-V 2.x</span></span>


<span data-ttu-id="fa228-104">Todas las implementaciones de virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1 requieren estas características</span><span class="sxs-lookup"><span data-stu-id="fa228-104">All Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, and 2.1 SP1 deployments require these features</span></span>

-   <span data-ttu-id="fa228-105">[Implemente una ubicación de almacenamiento de configuración](#ssl) accesible para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="fa228-105">[Deploy a Settings Storage Location](#ssl) that is accessible to end users.</span></span>

    <span data-ttu-id="fa228-106">Este es un recurso compartido de red estándar que almacena y recupera la configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="fa228-106">This is a standard network share that stores and retrieves user settings.</span></span>

-   [<span data-ttu-id="fa228-107">Elegir el método de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="fa228-107">Choose the Configuration Method for UE-V</span></span>](#config)

    <span data-ttu-id="fa228-108">UE-V se puede implementar y configurar con herramientas de administración comunes, como la Directiva de grupo, el administrador de configuración o la infraestructura de administración de Windows y PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fa228-108">UE-V can be deployed and configured using common management tools including group policy, Configuration Manager, or Windows Management Infrastructure and Powershell.</span></span>

-   <span data-ttu-id="fa228-109">[Implementar un agente de UE-V](#agent) para instalarlo en todos los equipos que sincronizan la configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-109">[Deploy a UE-V Agent](#agent) to be installed on every computer that synchronizes settings.</span></span>

    <span data-ttu-id="fa228-110">Esto supervisa las aplicaciones registradas y el sistema operativo para los cambios de configuración y sincroniza esa configuración entre equipos.</span><span class="sxs-lookup"><span data-stu-id="fa228-110">This monitors registered applications and the operating system for any settings changes and synchronizes those settings between computers.</span></span>

<span data-ttu-id="fa228-111">En los temas de esta sección se describe cómo implementar estas características.</span><span class="sxs-lookup"><span data-stu-id="fa228-111">The topics in this section describe how to deploy these features.</span></span>

## <a href="" id="ssl"></a><span data-ttu-id="fa228-112">Implementar una ubicación de almacenamiento de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="fa228-112">Deploy a UE-V Settings Storage Location</span></span>


<span data-ttu-id="fa228-113">UE-V requiere una ubicación en la que almacenar la configuración de usuario en los archivos de paquete de configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-113">UE-V requires a location in which to store user settings in settings package files.</span></span> <span data-ttu-id="fa228-114">Puede configurar esta ubicación de almacenamiento de configuración de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="fa228-114">You can configure this settings storage location in one of these ways:</span></span>

-   <span data-ttu-id="fa228-115">Crear su propia ubicación de almacenamiento de configuración</span><span class="sxs-lookup"><span data-stu-id="fa228-115">Create your own settings storage location</span></span>

-   <span data-ttu-id="fa228-116">Usar Active Directory existente para la ubicación de almacenamiento de configuración</span><span class="sxs-lookup"><span data-stu-id="fa228-116">Use existing Active Directory for your settings storage location</span></span>

<span data-ttu-id="fa228-117">Si no crea una ubicación de almacenamiento de configuración, UE-V Agent usará Active Directory (AD) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fa228-117">If you don’t create a settings storage location, the UE-V Agent will use Active Directory (AD) by default.</span></span>

**<span data-ttu-id="fa228-118">Nota</span><span class="sxs-lookup"><span data-stu-id="fa228-118">Note</span></span>**  
<span data-ttu-id="fa228-119">Como cuestión de [rendimiento y planificación de capacidad](https://technet.microsoft.com/library/dn458932.aspx#capacity) y para reducir los problemas con la latencia de red, cree ubicaciones de almacenamiento de configuración en las mismas redes locales donde residen los equipos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="fa228-119">As a matter of [performance and capacity planning](https://technet.microsoft.com/library/dn458932.aspx#capacity) and to reduce problems with network latency, create settings storage locations on the same local networks where the users’ computers reside.</span></span> <span data-ttu-id="fa228-120">Recomendamos 20 MB de espacio en disco por usuario para la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-120">We recommend 20 MB of disk space per user for the settings storage location.</span></span>



### <span data-ttu-id="fa228-121">Crear una ubicación de almacenamiento de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="fa228-121">Create a UE-V Settings Storage Location</span></span>

<span data-ttu-id="fa228-122">Antes de definir la ubicación de almacenamiento de configuración, debe crear un directorio raíz con permisos de lectura y escritura para los usuarios que almacenan la configuración en el recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="fa228-122">Before you define the settings storage location, you must create a root directory with read/write permissions for users who store settings on the share.</span></span> <span data-ttu-id="fa228-123">El agente UE-V crea carpetas específicas de usuario en este directorio raíz.</span><span class="sxs-lookup"><span data-stu-id="fa228-123">The UE-V Agent creates user-specific folders under this root directory.</span></span>

<span data-ttu-id="fa228-124">La ubicación de almacenamiento de configuración se define mediante la configuración de la opción de configuración SettingsStoragePath, que se puede configurar mediante uno de estos métodos:</span><span class="sxs-lookup"><span data-stu-id="fa228-124">The settings storage location is defined by setting the SettingsStoragePath configuration option, which you can configure by using one of these methods:</span></span>

-   <span data-ttu-id="fa228-125">Al [implementar el agente de UE-V](#agent) con un parámetro de línea de comandos o en un script de proceso por lotes</span><span class="sxs-lookup"><span data-stu-id="fa228-125">When you [Deploy the UE-V Agent](#agent) through a command-line parameter or in a batch script</span></span>

-   <span data-ttu-id="fa228-126">Mediante la configuración de [Directiva de grupo](https://technet.microsoft.com/library/dn458893.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa228-126">Through [Group Policy](https://technet.microsoft.com/library/dn458893.aspx) settings</span></span>

-   <span data-ttu-id="fa228-127">Con [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) para UE-V</span><span class="sxs-lookup"><span data-stu-id="fa228-127">With the [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) for UE-V</span></span>

-   <span data-ttu-id="fa228-128">Después de la instalación de UE-V Agent, mediante [Windows PowerShell o el instrumental de administración de Windows (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa228-128">After installation of the UE-V Agent, by using [Windows PowerShell or Windows Management Instrumentation (WMI)](https://technet.microsoft.com/library/dn458937.aspx)</span></span>

<span data-ttu-id="fa228-129">La ruta de acceso debe estar en una ruta de acceso UNC (Convención de nomenclatura universal) del servidor y el recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="fa228-129">The path must be in a universal naming convention (UNC) path of the server and share.</span></span> <span data-ttu-id="fa228-130">Por ejemplo, **\\\\Server\\Settingsshare\\**.</span><span class="sxs-lookup"><span data-stu-id="fa228-130">For example, **\\\\Server\\Settingsshare\\**.</span></span> <span data-ttu-id="fa228-131">Esta opción de configuración admite el uso de variables para habilitar escenarios de sincronización específicos.</span><span class="sxs-lookup"><span data-stu-id="fa228-131">This configuration option supports the use of variables to enable specific synchronization scenarios.</span></span> <span data-ttu-id="fa228-132">Por ejemplo, puede usar las `%username%\%computername%` variables para conservar la experiencia de configuración de usuario final en estos escenarios:</span><span class="sxs-lookup"><span data-stu-id="fa228-132">For example, you can use the `%username%\%computername%` variables to preserve the end user settings experience in these scenarios:</span></span>

-   <span data-ttu-id="fa228-133">Usuarios finales que usan varios equipos físicos en su empresa</span><span class="sxs-lookup"><span data-stu-id="fa228-133">End users that use multiple physical computers in your enterprise</span></span>

-   <span data-ttu-id="fa228-134">Equipos empresariales que usan varios usuarios finales</span><span class="sxs-lookup"><span data-stu-id="fa228-134">Enterprise computers that are used by multiple end users</span></span>

<span data-ttu-id="fa228-135">UE-V Agent crea dinámicamente una ruta de almacenamiento de configuración específica de usuario, con una carpeta de sistema oculta denominada `SettingsPackages` , basada en la opción de configuración de **SettingsStoragePath**.</span><span class="sxs-lookup"><span data-stu-id="fa228-135">The UE-V Agent dynamically creates a user-specific settings storage path, with a hidden system folder named `SettingsPackages`, based on the configuration setting of **SettingsStoragePath**.</span></span> <span data-ttu-id="fa228-136">El agente Lee y escribe la configuración en esta ubicación, tal como se define en las plantillas de ubicación de configuración de UE-V registradas.</span><span class="sxs-lookup"><span data-stu-id="fa228-136">The agent reads and writes settings to this location as defined by the registered UE-V settings location templates.</span></span>

<span data-ttu-id="fa228-137">**La configuración de UE-V está determinada por la regla "última escritura gana":** Si la ubicación de almacenamiento de configuración es la misma para el usuario con varios equipos administrados, un agente de UE-V Lee y escribe en la ubicación de configuración independientemente de los agentes que se ejecutan en otros equipos.</span><span class="sxs-lookup"><span data-stu-id="fa228-137">**UE-V settings are determined by a "Last write wins" rule:** If the settings storage location is the same for user with multiple managed computers, one UE-V Agent reads and writes to the settings location independently of agents running on other computers.</span></span> <span data-ttu-id="fa228-138">Las últimas configuraciones y valores son los que se aplican cuando el siguiente agente Lee de la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-138">The last written settings and values are the ones applied when the next agent reads from the settings storage location.</span></span>

<span data-ttu-id="fa228-139">**Implementar la ubicación de almacenamiento de configuración:** Siga estos pasos para definir la ubicación de almacenamiento de configuración en lugar de usar el servicio de Active Directory existente.</span><span class="sxs-lookup"><span data-stu-id="fa228-139">**Deploy the settings storage location:** Follow these steps to define the settings storage location rather than using your existing Active Directory service.</span></span> <span data-ttu-id="fa228-140">Debe limitar el acceso al recurso de almacenamiento de configuración a los usuarios que lo requieren, tal y como se muestra en las tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="fa228-140">You should limit access to the settings storage share to those users that require it, as shown in the tables below.</span></span>

**<span data-ttu-id="fa228-141">Para implementar el recurso compartido de red UE-V</span><span class="sxs-lookup"><span data-stu-id="fa228-141">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="fa228-142">Cree un nuevo grupo de seguridad para usuarios de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa228-142">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="fa228-143">Cree una nueva carpeta en el equipo centralizado que almacena los paquetes de configuración de UE-V y, a continuación, conceda a los usuarios de UE-V acceso con permisos de grupo a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="fa228-143">Create a new folder on the centrally located computer that stores the UE-V settings packages, and then grant the UE-V users access with group permissions to the folder.</span></span> <span data-ttu-id="fa228-144">El administrador que admita UE-V debe tener permisos para esta carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="fa228-144">The administrator who supports UE-V must have permissions to this shared folder.</span></span>

3.  <span data-ttu-id="fa228-145">Establezca los siguientes permisos de bloque de mensajes de servidor (SMB) de nivel de recurso compartido para la carpeta de ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-145">Set the following share-level Server Message Block (SMB) permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="fa228-146">Cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="fa228-146">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="fa228-147">Permisos recomendados</span><span class="sxs-lookup"><span data-stu-id="fa228-147">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fa228-148">Todos</span><span class="sxs-lookup"><span data-stu-id="fa228-148">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa228-149">No hay permisos</span><span class="sxs-lookup"><span data-stu-id="fa228-149">No permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="fa228-150">Grupo de seguridad de los usuarios de UE-V</span><span class="sxs-lookup"><span data-stu-id="fa228-150">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa228-151">Control total</span><span class="sxs-lookup"><span data-stu-id="fa228-151">Full control</span></span></p></td>
    </tr>
    </tbody>
    </table>



4.  <span data-ttu-id="fa228-152">Establezca los siguientes permisos del sistema de archivos NTFS en la carpeta de ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-152">Set the following NTFS file system permissions for the settings storage location folder.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="fa228-153">Cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="fa228-153">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="fa228-154">Permisos recomendados</span><span class="sxs-lookup"><span data-stu-id="fa228-154">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="fa228-155">Carpeta</span><span class="sxs-lookup"><span data-stu-id="fa228-155">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="fa228-156">Creador/propietario</span><span class="sxs-lookup"><span data-stu-id="fa228-156">Creator/owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa228-157">Control total</span><span class="sxs-lookup"><span data-stu-id="fa228-157">Full control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa228-158">Solo subcarpetas y archivos</span><span class="sxs-lookup"><span data-stu-id="fa228-158">Subfolders and files only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="fa228-159">Grupo de seguridad de los usuarios de UE-V</span><span class="sxs-lookup"><span data-stu-id="fa228-159">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa228-160">Listar carpeta/leer datos, crear carpetas/anexar datos</span><span class="sxs-lookup"><span data-stu-id="fa228-160">List folder/read data, create folders/append data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="fa228-161">Solo esta carpeta</span><span class="sxs-lookup"><span data-stu-id="fa228-161">This folder only</span></span></p></td>
    </tr>
    </tbody>
    </table>



<span data-ttu-id="fa228-162">Con esta configuración, UE-V Agent crea y protege una carpeta Settingspackage mientras se ejecuta en el contexto del usuario y otorga a cada usuario permiso para crear carpetas para el almacenamiento de la configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-162">With this configuration, the UE-V Agent creates and secures a Settingspackage folder while it runs in the context of the user, and grants each user permission to create folders for settings storage.</span></span> <span data-ttu-id="fa228-163">Los usuarios reciben el control total de su carpeta Settingspackage, mientras que otros usuarios no pueden acceder a ella.</span><span class="sxs-lookup"><span data-stu-id="fa228-163">Users receive full control to their Settingspackage folder while other users cannot access it.</span></span>

**<span data-ttu-id="fa228-164">Nota</span><span class="sxs-lookup"><span data-stu-id="fa228-164">Note</span></span>**  
<span data-ttu-id="fa228-165">Si crea el recurso de almacenamiento de configuración en un equipo que ejecuta un sistema operativo Windows Server, configure UE-V para comprobar que el grupo de administradores local o el usuario actual es el propietario de la carpeta donde se almacenan los paquetes de configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-165">If you create the settings storage share on a computer running a Windows Server operating system, configure UE-V to verify that either the local Administrators group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="fa228-166">Para habilitar esta seguridad adicional, especifique esta configuración en el editor del registro de Windows Server:</span><span class="sxs-lookup"><span data-stu-id="fa228-166">To enable this additional security, specify this setting in the Windows Server Registry Editor:</span></span>

1.  <span data-ttu-id="fa228-167">Agregue una clave del registro **reg \ _DWORD** denominada **"RepositoryOwnerCheckEnabled"** a **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.</span><span class="sxs-lookup"><span data-stu-id="fa228-167">Add a **REG\_DWORD** registry key named **"RepositoryOwnerCheckEnabled"** to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration**.</span></span>

2.  <span data-ttu-id="fa228-168">Establezca el valor de la clave del registro en *1*.</span><span class="sxs-lookup"><span data-stu-id="fa228-168">Set the registry key value to *1*.</span></span>



### <span data-ttu-id="fa228-169">Usar Active Directory con UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fa228-169">Use Active Directory with UE-V 2.x</span></span>

<span data-ttu-id="fa228-170">El agente UE-V usa Active Directory (AD) de forma predeterminada si una ubicación de almacenamiento de configuración no está definida.</span><span class="sxs-lookup"><span data-stu-id="fa228-170">The UE-V Agent uses Active Directory (AD) by default if a settings storage location is not otherwise defined.</span></span> <span data-ttu-id="fa228-171">En estos casos, UE-V Agent crea dinámicamente la carpeta de almacenamiento de configuración en la raíz del directorio particular de AD de cada usuario.</span><span class="sxs-lookup"><span data-stu-id="fa228-171">In these cases, the UE-V Agent dynamically creates the settings storage folder under the root of the AD home directory of each user.</span></span> <span data-ttu-id="fa228-172">Sin embargo, si una configuración de directorio personalizada está configurada en AD, ese directorio se usa en su lugar.</span><span class="sxs-lookup"><span data-stu-id="fa228-172">But, if a custom directory setting is configured in AD, then that directory is used instead.</span></span>

## <a href="" id="config"></a><span data-ttu-id="fa228-173">Elija el método de configuración de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fa228-173">Choose the Configuration Method for UE-V 2.x</span></span>


<span data-ttu-id="fa228-174">Desea averiguar qué método de configuración usará para administrar UE-V después de la implementación, ya que este es el método de configuración que use para implementar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa228-174">You want to figure out which configuration method you'll use to manage UE-V after deployment since this will be the configuration method you use to deploy the UE-V Agent.</span></span> <span data-ttu-id="fa228-175">Normalmente, este es el método de configuración que ya usa en su entorno, como Windows PowerShell o Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fa228-175">Typically, this is the configuration method that you already use in your environment, such as Windows PowerShell or Configuration Manager.</span></span>

<span data-ttu-id="fa228-176">Puede configurar UE-V antes, durante o después de la instalación del agente de UE-V, según el método de configuración que use.</span><span class="sxs-lookup"><span data-stu-id="fa228-176">You can configure UE-V before, during, or after UE-V Agent installation, depending on the configuration method that you use.</span></span>

-   <span data-ttu-id="fa228-177">[Directiva de grupo](https://technet.microsoft.com/library/dn458893.aspx)**:** puede usar su infraestructura de directiva de grupo existente para configurar UE-v antes o después de la implementación del agente de UE-v.</span><span class="sxs-lookup"><span data-stu-id="fa228-177">[Group Policy](https://technet.microsoft.com/library/dn458893.aspx)**:** You can use your existing Group Policy infrastructure to configure UE-V before or after UE-V Agent deployment.</span></span> <span data-ttu-id="fa228-178">La plantilla de ADMX de la Directiva de grupo de UE-V habilita la administración centralizada de las opciones de configuración de agentes comunes de UE-V e incluye la configuración para configurar la sincronización de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa228-178">The UE-V Group Policy ADMX template enables the central management of common UE-V Agent configuration options, and it includes settings to configure UE-V synchronization.</span></span>

    <span data-ttu-id="fa228-179">**Instalar las plantillas ADMX de la Directiva de grupo de UE-V:** Plantillas ADMX de directiva de grupo para UE-V establecer la configuración de sincronización para el agente UE-V y habilitar la administración centralizada de las opciones de configuración del agente Common UE-V mediante una infraestructura de directiva de grupo existente.</span><span class="sxs-lookup"><span data-stu-id="fa228-179">**Installing the UE-V Group Policy ADMX Templates:** Group Policy ADMX templates for UE-V configure the synchronization settings for the UE-V Agent and enable the central management of common UE-V Agent configuration settings by using an existing Group Policy infrastructure.</span></span>

    <span data-ttu-id="fa228-180">Entre los sistemas operativos admitidos para el controlador de dominio que implementa los objetos de directiva de grupo se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="fa228-180">Supported operating systems for the domain controller that deploys the Group Policy Objects include the following:</span></span>

    <span data-ttu-id="fa228-181">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fa228-181">Windows Server 2008 R2</span></span>

    <span data-ttu-id="fa228-182">Windows Server 2012 y Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fa228-182">Windows Server 2012 and Windows Server 2012 R2</span></span>

-   <span data-ttu-id="fa228-183">[Administrador de configuración](https://technet.microsoft.com/library/dn458917.aspx)**:** el paquete de configuración de UE-V le permite usar la característica de configuración de cumplimiento de System Center Configuration Manager 2012 SP1 o posterior para aplicar configuraciones coherentes en los sitios donde se instalan UE-V y Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="fa228-183">[Configuration Manager](https://technet.microsoft.com/library/dn458917.aspx)**:** The UE-V Configuration Pack lets you use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

-   <span data-ttu-id="fa228-184">[Windows PowerShell y WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** puede usar los comandos de scripts para Windows PowerShell y Windows Management Instrumentation (WMI) con el fin de modificar las configuraciones después de instalar UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="fa228-184">[Windows PowerShell and WMI](https://technet.microsoft.com/library/dn458937.aspx)**:** You can use scripted commands for Windows PowerShell and Windows Management Instrumentation (WMI) to modify configurations after you install the UE-V Agent.</span></span>

    **<span data-ttu-id="fa228-185">Nota</span><span class="sxs-lookup"><span data-stu-id="fa228-185">Note</span></span>**  
    <span data-ttu-id="fa228-186">La modificación del registro puede provocar pérdida de datos o el equipo deja de responder.</span><span class="sxs-lookup"><span data-stu-id="fa228-186">Registry modification can result in data loss, or the computer becomes unresponsive.</span></span> <span data-ttu-id="fa228-187">Le recomendamos que use otros métodos de configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-187">We recommend that you use other configuration methods.</span></span>



-   <span data-ttu-id="fa228-188">**Instalación de la línea de comandos o del script por lotes:** Los parámetros que se usan al [implementar el agente de UE-v](#agent) tienen configurado muchos parámetros de UE-v.</span><span class="sxs-lookup"><span data-stu-id="fa228-188">**Command-line or Batch Script Installation:** Parameters that are used when you [Deploy the UE-V Agent](#agent) configure many UE-V settings.</span></span> <span data-ttu-id="fa228-189">Los sistemas electrónicos de distribución de software, como System Center 2012 Configuration Manager, usan estos parámetros para configurar sus clientes cuando implementan e instalan el software de agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa228-189">Electronic software distribution systems, such as System Center 2012 Configuration Manager, use these parameters to configure their clients when they deploy and install the UE-V Agent software.</span></span>

## <a href="" id="agent"></a><span data-ttu-id="fa228-190">Implementar el agente UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fa228-190">Deploy the UE-V 2.x Agent</span></span>


<span data-ttu-id="fa228-191">UE-V Agent es el núcleo de una implementación de UE-V y debe ejecutarse en todos los equipos que usan UE-V para sincronizar la configuración de Windows y de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fa228-191">The UE-V Agent is the core of a UE-V deployment and must run on each computer that uses UE-V to synchronize application and Windows settings.</span></span>

<span data-ttu-id="fa228-192">**Archivos de instalación de UE-V Agent:** Un único archivo de instalación, AgentSetup.exe, instala UE-V Agent en los sistemas operativos de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fa228-192">**UE-V Agent Installation Files:** A single installation file, AgentSetup.exe, installs the UE-V Agent on both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="fa228-193">Además, se proporcionan AgentSetupx86.msi o AgentSetupx64.msi archivos de Windows Installer específicos de la arquitectura, y puesto que son más pequeños, pueden simplificar las implementaciones del agente.</span><span class="sxs-lookup"><span data-stu-id="fa228-193">In addition, AgentSetupx86.msi or AgentSetupx64.msi architecture-specific Windows Installer files are provided, and since they are smaller, they might streamline the agent deployments.</span></span> <span data-ttu-id="fa228-194">Los [parámetros de la línea de comandos para el instalador de AgentSetup.exe](#params) son compatibles también con la instalación de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="fa228-194">The [command-line parameters for the AgentSetup.exe installer](#params) are supported for the Windows Installer installation as well.</span></span>

**<span data-ttu-id="fa228-195">Importante</span><span class="sxs-lookup"><span data-stu-id="fa228-195">Important</span></span>**  
<span data-ttu-id="fa228-196">Durante la instalación o desinstalación de un agente de UE-V, puede usar el archivo AgentSetup.exe o &lt; el &gt; archivo AgentSetup. msi, pero no ambos.</span><span class="sxs-lookup"><span data-stu-id="fa228-196">During UE-V Agent installation or uninstallation, you can either use the AgentSetup.exe file or the AgentSetup&lt;arch&gt;.msi file, but not both.</span></span> <span data-ttu-id="fa228-197">El mismo archivo debe usarse para desinstalar el agente de UE-V que se usó para instalar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa228-197">The same file must be used to uninstall the UE-V Agent that was used to install the UE-V Agent.</span></span>



### <span data-ttu-id="fa228-198">Para implementar el agente de UE-V</span><span class="sxs-lookup"><span data-stu-id="fa228-198">To Deploy the UE-V Agent</span></span>

<span data-ttu-id="fa228-199">Puede usar los siguientes métodos para implementar el agente de UE-V:</span><span class="sxs-lookup"><span data-stu-id="fa228-199">You can use the following methods to deploy the UE-V Agent:</span></span>

-   <span data-ttu-id="fa228-200">Un sistema de solución de distribución electrónica de software (ESD), como Configuration Manager, que puede instalar un archivo de Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="fa228-200">An electronic software distribution (ESD) solution system, such as Configuration Manager, that can install a Windows Installer (.msi) file.</span></span>

-   <span data-ttu-id="fa228-201">Un script de instalación que hace referencia al archivo de Windows Installer (. msi) que se almacena centralmente en un recurso compartido.</span><span class="sxs-lookup"><span data-stu-id="fa228-201">An installation script that references the Windows Installer (.msi) file that is stored centrally on a share.</span></span>

-   <span data-ttu-id="fa228-202">Un programa de instalación que se ejecuta manualmente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="fa228-202">An installation program that you run manually on the computer.</span></span>

<span data-ttu-id="fa228-203">Use el siguiente procedimiento para implementar UE-V Agent desde un recurso compartido de red.</span><span class="sxs-lookup"><span data-stu-id="fa228-203">Use the following procedure to deploy the UE-V Agent from a network share.</span></span>

**<span data-ttu-id="fa228-204">Para instalar y configurar el agente UE-V desde un recurso compartido de red</span><span class="sxs-lookup"><span data-stu-id="fa228-204">To install and configure the UE-V Agent from a network share</span></span>**

1.  <span data-ttu-id="fa228-205">Fase el archivo de instalación de UE-V Agent AgentSetup.exe en un recurso compartido de red en el que los usuarios tienen permiso de lectura.</span><span class="sxs-lookup"><span data-stu-id="fa228-205">Stage the UE-V Agent installation file AgentSetup.exe on a network share to which users have Read permission.</span></span>

2.  <span data-ttu-id="fa228-206">Implementar una secuencia de comandos en equipos de usuario que instala UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="fa228-206">Deploy a script to user computers that installs the UE-V Agent.</span></span> <span data-ttu-id="fa228-207">El script debe especificar la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-207">The script should specify the settings storage location.</span></span>

<span data-ttu-id="fa228-208">**Opciones de implementación:** Asegúrese de usar el formato de variable correcto al instalar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa228-208">**Deployment options:** Be sure to use the correct variable format when you install the UE-V Agent.</span></span> <span data-ttu-id="fa228-209">En la tabla siguiente se proporcionan ejemplos de opciones de implementación para usar el AgentSetup.exe o los archivos de Windows Installer (. msi).</span><span class="sxs-lookup"><span data-stu-id="fa228-209">The following table provides examples of deployment options for using the AgentSetup.exe or the Windows Installer (.msi) files.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="fa228-210">Tipo de implementación</span><span class="sxs-lookup"><span data-stu-id="fa228-210">Deployment type</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="fa228-211">Descripción de la implementación</span><span class="sxs-lookup"><span data-stu-id="fa228-211">Deployment description</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="fa228-212">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fa228-212">Example</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa228-213">Símbolo del sistema</span><span class="sxs-lookup"><span data-stu-id="fa228-213">Command prompt</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-214">Al instalar el agente de UE-V en un símbolo del sistema, use el <em> formato de variable% ^ username% </em> .</span><span class="sxs-lookup"><span data-stu-id="fa228-214">When you install the UE-V Agent at a command prompt, use the <em>%^username%</em> variable format.</span></span> <span data-ttu-id="fa228-215">Si las comillas son necesarias debido a los espacios en la ruta de almacenamiento de configuración, use un archivo de script por lotes para la implementación.</span><span class="sxs-lookup"><span data-stu-id="fa228-215">If quotation marks are required because of spaces in the settings storage path, use a batch script file for deployment.</span></span></p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa228-216">Script por lotes</span><span class="sxs-lookup"><span data-stu-id="fa228-216">Batch script</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-217">Cuando instale UE-V Agent desde un archivo de script por lotes, use el <em> formato de variable%% username%% </em> .</span><span class="sxs-lookup"><span data-stu-id="fa228-217">When you install the UE-V Agent from a batch script file, use the <em>%%username%%</em> variable format.</span></span> <span data-ttu-id="fa228-218">Si usa este método de instalación, debe escapar la variable con los%% caracteres.</span><span class="sxs-lookup"><span data-stu-id="fa228-218">If you use this installation method, you must escape the variable with the %% characters.</span></span> <span data-ttu-id="fa228-219">Sin este carácter, la secuencia de comandos amplía <em> la </em> variable username en el momento de la instalación, en lugar de hacerlo en tiempo de ejecución, lo que hace que UE-V use una sola ubicación de almacenamiento de configuración para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="fa228-219">Without this character, the script expands the <em>username</em> variable at installation time, rather than at run time, which causes UE-V to use a single settings storage location for all users.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa228-220">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa228-220">Windows PowerShell</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-221">Cuando instale UE-V Agent desde un símbolo del sistema de Windows PowerShell o un script de Windows PowerShell, use el <em> formato de variable% username% </em> .</span><span class="sxs-lookup"><span data-stu-id="fa228-221">When you install the UE-V Agent from a Windows PowerShell prompt or a Windows PowerShell script, use the <em>%username%</em> variable format.</span></span></p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa228-222">Distribución electrónica de software, como la implementación de la implementación de software de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="fa228-222">Electronic software distribution, such as deployment of Configuration Manager Software Deployment</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-223">Al instalar el agente de UE-V mediante el administrador de configuración, use el <em> formato de variable ^% username ^% </em> .</span><span class="sxs-lookup"><span data-stu-id="fa228-223">When you install the UE-V Agent by using Configuration Manager, use the <em>^%username^%</em> variable format.</span></span></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="fa228-224">Nota</span><span class="sxs-lookup"><span data-stu-id="fa228-224">Note</span></span>**  
<span data-ttu-id="fa228-225">La instalación del agente de UE-V requiere derechos de administrador, y el equipo requiere que se reinicie el equipo antes de que se pueda ejecutar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa228-225">The installation of the UE-V Agent requires administrator rights, and the computer requires a restart before the UE-V Agent can run.</span></span>



### <a href="" id="params"></a><span data-ttu-id="fa228-226">Parámetros de la línea de comandos para la implementación del agente de UE-V</span><span class="sxs-lookup"><span data-stu-id="fa228-226">Command-line parameters for UE-V Agent deployment</span></span>

<span data-ttu-id="fa228-227">Los parámetros de la línea de comandos de UE-V Agent son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="fa228-227">The command-line parameters of the UE-V Agent are as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="fa228-228">Parámetro de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="fa228-228">Command-line parameter</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="fa228-229">Definición</span><span class="sxs-lookup"><span data-stu-id="fa228-229">Definition</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="fa228-230">Notas</span><span class="sxs-lookup"><span data-stu-id="fa228-230">Notes</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa228-231">/Help o/h o/?</span><span class="sxs-lookup"><span data-stu-id="fa228-231">/help or /h or /?</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-232">Muestra el cuadro de diálogo de uso de AgentSetup.exe.</span><span class="sxs-lookup"><span data-stu-id="fa228-232">Displays the AgentSetup.exe usage dialog box.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa228-233">SettingsStoragePath</span><span class="sxs-lookup"><span data-stu-id="fa228-233">SettingsStoragePath</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-234">Indica la ruta de acceso UNC (Convención de nomenclatura universal) que define dónde se almacena la configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-234">Indicates the Universal Naming Convention (UNC) path that defines where settings are stored.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="fa228-235">Importante</span><span class="sxs-lookup"><span data-stu-id="fa228-235">Important</span></span></strong><br/><p><span data-ttu-id="fa228-236">Debe especificar un SettingsStoragePath en UE-V 2,1 y UE-V 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="fa228-236">You must specify a SettingsStoragePath in UE-V 2.1 and UE-V 2.1 SP1.</span></span> <span data-ttu-id="fa228-237">Puede establecer la cadena AdHomePath para especificar que el usuario&#39;la ruta de acceso de la Página principal de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fa228-237">You can set the AdHomePath string to specify that the user&#39;s Active Directory home path is used.</span></span> <span data-ttu-id="fa228-238">Por ejemplo, <code>SettingsStoragePath = \share\path|AdHomePath</code>.</span><span class="sxs-lookup"><span data-stu-id="fa228-238">For example, <code>SettingsStoragePath = \share\path|AdHomePath</code>.</span></span></p>
<p><span data-ttu-id="fa228-239">En UE-V 2,0, puede dejar el SettingsStoragePath en blanco para usar la ruta de acceso de la Página principal de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fa228-239">In UE-V 2.0, you can leave SettingsStoragePath blank to use the Active Directory home path instead.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="fa228-240">se aceptan las variables de entorno% username% o% COMPUTERNAME%.</span><span class="sxs-lookup"><span data-stu-id="fa228-240">%username% or %computername% environment variables are accepted.</span></span> <span data-ttu-id="fa228-241">El scripting puede requerir variables de escape.</span><span class="sxs-lookup"><span data-stu-id="fa228-241">Scripting can require escaped variables.</span></span></p>
<p><strong><span data-ttu-id="fa228-242">Valor predeterminado </strong> : &lt; ninguno&gt;</span><span class="sxs-lookup"><span data-stu-id="fa228-242">Default</strong>: &lt;none&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa228-243">SettingsStoragePathReg</span><span class="sxs-lookup"><span data-stu-id="fa228-243">SettingsStoragePathReg</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-244">Obtiene el valor de SettingsStoragePath del registro durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="fa228-244">Gets the SettingsStoragePath value from the registry during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-245">En el símbolo del sistema, escriba el siguiente ejemplo para forzar que UE-V use la ruta de acceso de la Página principal de Active Directory en lugar de un UNC específico.</span><span class="sxs-lookup"><span data-stu-id="fa228-245">At the command prompt, type the following example to force UE-V to use the Active Directory home path instead of a specific UNC.</span></span></p>
<p><code>msiexec.exe /i AgentSetupx64.msi acceptlicenseterms=true SettingsStoragePathReg=TRUE /quiet /norestart</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa228-246">SettingsTemplateCatalogPath</span><span class="sxs-lookup"><span data-stu-id="fa228-246">SettingsTemplateCatalogPath</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-247">Indica la ruta de acceso UNC (Convención de nomenclatura universal) que define la ubicación en la que se comprobó la configuración de nuevas plantillas de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-247">Indicates the Universal Naming Convention (UNC) path that defines the location that was checked for new settings location templates.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-248">Solo es necesario para las plantillas de ubicación de configuración personalizada</span><span class="sxs-lookup"><span data-stu-id="fa228-248">Only required for custom settings location templates</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa228-249">RegisterMSTemplates</span><span class="sxs-lookup"><span data-stu-id="fa228-249">RegisterMSTemplates</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-250">Especifica si se deben registrar las plantillas predeterminadas de Microsoft durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="fa228-250">Specifies whether the default Microsoft templates should be registered during installation.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-251">Verdadero | Valor</span><span class="sxs-lookup"><span data-stu-id="fa228-251">True | False</span></span></p>
<p><strong><span data-ttu-id="fa228-252">Valor predeterminado </strong> : verdadero</span><span class="sxs-lookup"><span data-stu-id="fa228-252">Default</strong>: True</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa228-253">SyncMethod</span><span class="sxs-lookup"><span data-stu-id="fa228-253">SyncMethod</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-254">Especifica qué método de sincronización debe usarse.</span><span class="sxs-lookup"><span data-stu-id="fa228-254">Specifies which synchronization method should be used.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-255">SyncProvider | Nada</span><span class="sxs-lookup"><span data-stu-id="fa228-255">SyncProvider | None</span></span></p>
<p><strong><span data-ttu-id="fa228-256">Valor predeterminado </strong> : SyncProvider</span><span class="sxs-lookup"><span data-stu-id="fa228-256">Default</strong>: SyncProvider</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa228-257">SyncTimeoutInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="fa228-257">SyncTimeoutInMilliseconds</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-258">Especifica el número de milisegundos que el equipo debe esperar antes de que se agote el tiempo de espera cuando recupera la configuración de usuario de la ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-258">Specifies the number of milliseconds that the computer waits before time-out when it retrieves user settings from the settings storage location.</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="fa228-259">Valor predeterminado </strong> : 2000 milisegundos</span><span class="sxs-lookup"><span data-stu-id="fa228-259">Default</strong>: 2000 milliseconds</span></span></p>
<p><span data-ttu-id="fa228-260">(espera hasta 2 segundos)</span><span class="sxs-lookup"><span data-stu-id="fa228-260">(wait up to 2 seconds)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa228-261">SyncEnabled</span><span class="sxs-lookup"><span data-stu-id="fa228-261">SyncEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-262">Especifica si la sincronización de UE-V está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="fa228-262">Specifies whether UE-V synchronization is enabled or disabled.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-263">Verdadero | Valor</span><span class="sxs-lookup"><span data-stu-id="fa228-263">True | False</span></span></p>
<p><strong><span data-ttu-id="fa228-264">Valor predeterminado </strong> : verdadero</span><span class="sxs-lookup"><span data-stu-id="fa228-264">Default</strong>: True</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa228-265">MaxPackageSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="fa228-265">MaxPackageSizeInBytes</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-266">Especifica el tamaño de archivo de un paquete de configuración en bytes cuando el agente de UE-V notifica que los archivos superan el umbral.</span><span class="sxs-lookup"><span data-stu-id="fa228-266">Specifies a settings package file size in bytes when the UE-V Agent reports that files exceed the threshold.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-267">&lt;su&gt;</span><span class="sxs-lookup"><span data-stu-id="fa228-267">&lt;size&gt;</span></span></p>
<p><strong><span data-ttu-id="fa228-268">Valor predeterminado </strong> : ninguno (no hay umbral de advertencia)</span><span class="sxs-lookup"><span data-stu-id="fa228-268">Default</strong>: none (no warning threshold)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa228-269">CEIPEnabled</span><span class="sxs-lookup"><span data-stu-id="fa228-269">CEIPEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-270">Especifica la configuración de participación en el programa para la mejora de la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="fa228-270">Specifies the setting for participation in the Customer Experience Improvement program.</span></span> <span data-ttu-id="fa228-271">Si se establece en <strong> true </strong> , la información del instalador se carga en el sitio del programa para la mejora de la experiencia del usuario de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fa228-271">If set to <strong>True</strong>, installer information is uploaded to the Microsoft Customer Experience Improvement Program site.</span></span> <span data-ttu-id="fa228-272">Si se establece en <strong> false </strong> , no se cargará ninguna información.</span><span class="sxs-lookup"><span data-stu-id="fa228-272">If set to <strong>False</strong>, no information is uploaded.</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-273">Verdadero | Valor</span><span class="sxs-lookup"><span data-stu-id="fa228-273">True | False</span></span></p>
<p><strong><span data-ttu-id="fa228-274">Valor predeterminado </strong> : falso</span><span class="sxs-lookup"><span data-stu-id="fa228-274">Default</strong>: False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa228-275">No restar</span><span class="sxs-lookup"><span data-stu-id="fa228-275">NoRestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-276">Es compatible con el aplazamiento del reinicio del equipo después de instalar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa228-276">Supports deferral of the restart of the computer after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa228-277">INSTALLFOLDER</span><span class="sxs-lookup"><span data-stu-id="fa228-277">INSTALLFOLDER</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-278">Permite establecer una carpeta de instalación diferente para el generador de UE-V Agent o UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa228-278">Enables a different installation folder to be set for the UE-V Agent or UE-V Generator.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa228-279">MUENABLED</span><span class="sxs-lookup"><span data-stu-id="fa228-279">MUENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-280">Permite que el programa de instalación acepte la opción que se va a incluir en el programa Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="fa228-280">Enables Setup to accept the option to be included in the Microsoft Update program.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fa228-281">ACCEPTLICENSETERMS</span><span class="sxs-lookup"><span data-stu-id="fa228-281">ACCEPTLICENSETERMS</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-282">Permite que UE-V se instale silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="fa228-282">Lets UE-V be installed silently.</span></span> <span data-ttu-id="fa228-283">Debe establecerse en <strong> true </strong> para instalar UE-v en modo silencioso y evitar el requisito de que el usuario acepte los términos de licencia de UE-v.</span><span class="sxs-lookup"><span data-stu-id="fa228-283">This must be set to <strong>True</strong> to install UE-V silently and bypass the requirement that the user accepts the UE-V license terms.</span></span> <span data-ttu-id="fa228-284">Si se establece en <strong> false </strong> o se deja vacío, el usuario recibe un mensaje de error y UE-V no está instalado.</span><span class="sxs-lookup"><span data-stu-id="fa228-284">If set to <strong>False</strong> or left empty, the user receives an error message and UE-V is not installed.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="fa228-285">Importante</span><span class="sxs-lookup"><span data-stu-id="fa228-285">Important</span></span></strong><br/><p><span data-ttu-id="fa228-286">Este parámetro es necesario para instalar UE-V en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="fa228-286">This parameter is required to install UE-V silently.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fa228-287">No restar</span><span class="sxs-lookup"><span data-stu-id="fa228-287">NORESTART</span></span></p></td>
<td align="left"><p><span data-ttu-id="fa228-288">Evita un reinicio obligatorio una vez instalado el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa228-288">Prevents a mandatory restart after the UE-V Agent is installed.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="fa228-289">Actualizar el agente de UE-V</span><span class="sxs-lookup"><span data-stu-id="fa228-289">Update the UE-V Agent</span></span>

<span data-ttu-id="fa228-290">Las actualizaciones para el software del agente UE-V se proporcionan a través de Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="fa228-290">Updates for the UE-V Agent software are provided through Microsoft Update.</span></span> <span data-ttu-id="fa228-291">Puede implementar las actualizaciones del agente de UE-V mediante sistemas de infraestructura de distribución de software para empresas (ESD).</span><span class="sxs-lookup"><span data-stu-id="fa228-291">You can deploy UE-V Agent updates by using Enterprise Software Distribution (ESD) infrastructure systems.</span></span>

<span data-ttu-id="fa228-292">Durante una actualización de UE-V Agent, se puede actualizar el grupo predeterminado de plantillas de ubicación de configuración para las aplicaciones comunes de Microsoft y la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="fa228-292">During a UE-V Agent upgrade, the default group of settings location templates for common Microsoft applications and Windows settings can be updated.</span></span>

### <span data-ttu-id="fa228-293">Actualizar el agente UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fa228-293">Upgrade the UE-V 2.x Agent</span></span>

<span data-ttu-id="fa228-294">El agente UE-V 2. x introduce muchas características nuevas y modifica el modo y el momento en que el agente carga el contenido en el recurso compartido de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-294">The UE-V 2.x Agent introduces many new features and modifies how and when the agent uploads content to the settings storage share.</span></span> <span data-ttu-id="fa228-295">El proceso de actualización automatiza estos cambios.</span><span class="sxs-lookup"><span data-stu-id="fa228-295">The upgrade process automates these changes.</span></span> <span data-ttu-id="fa228-296">Para actualizar el agente de UE-V, ejecute el paquete de instalación de UE-V Agent (AgentSetup.exe, AgentSetupx86.msi o AgentSetupx64.msi) en los equipos de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="fa228-296">To upgrade the UE-V Agent, run the UE-V Agent install package (AgentSetup.exe, AgentSetupx86.msi, or AgentSetupx64.msi) on users’ computers.</span></span>

**<span data-ttu-id="fa228-297">Nota</span><span class="sxs-lookup"><span data-stu-id="fa228-297">Note</span></span>**  
<span data-ttu-id="fa228-298">Al actualizar el agente de UE-V, debe usar el mismo tipo de instalador (el archivo. exe o el paquete. msi) que instaló el agente anterior de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa228-298">When you upgrade the UE-V Agent, you must use the same installer type (.exe file or .msi packet) that installed the previous UE-V Agent.</span></span> <span data-ttu-id="fa228-299">Por ejemplo, use la AgentSetup.exe UE-V 2 para actualizar los agentes de UE-V 1,0 que se instalaron con AgentSetup.exe.</span><span class="sxs-lookup"><span data-stu-id="fa228-299">For example, use the UE-V 2 AgentSetup.exe to upgrade UE-V 1.0 Agents that were installed by using AgentSetup.exe.</span></span>



<span data-ttu-id="fa228-300">Las siguientes configuraciones se conservan cuando se ejecuta el programa de configuración del agente:</span><span class="sxs-lookup"><span data-stu-id="fa228-300">The following configurations are preserved when the Agent Setup program runs:</span></span>

-   <span data-ttu-id="fa228-301">Configuración ruta de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="fa228-301">Settings storage path</span></span>

-   <span data-ttu-id="fa228-302">Configuración del Registro</span><span class="sxs-lookup"><span data-stu-id="fa228-302">Registry settings</span></span>

-   <span data-ttu-id="fa228-303">Tareas programadas (la configuración de intervalos se restablece a los valores predeterminados)</span><span class="sxs-lookup"><span data-stu-id="fa228-303">Scheduled tasks (Interval settings are reset to their defaults)</span></span>

**<span data-ttu-id="fa228-304">Nota</span><span class="sxs-lookup"><span data-stu-id="fa228-304">Note</span></span>**  
<span data-ttu-id="fa228-305">Un equipo con la configuración de UE-V 2. x las plantillas de ubicación registradas en el agente de UE-V 1,0 registran errores en el registro de eventos de Windows.</span><span class="sxs-lookup"><span data-stu-id="fa228-305">A computer with UE-V 2.x settings location templates that are registered in the UE-V 1.0 Agent register errors in the Windows Event Log.</span></span>



<span data-ttu-id="fa228-306">Puede usar Microsoft System Center 2012 Configuration Manager u otra herramienta de distribución de software empresarial para automatizar y distribuir la actualización del agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa228-306">You can use Microsoft System Center 2012 Configuration Manager or another enterprise software distribution tool to automate and distribute the UE-V Agent upgrade.</span></span>

<span data-ttu-id="fa228-307">**Recomendaciones:** Le recomendamos que actualice todos los agentes de UE-V 1,0 en un entorno informático, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="fa228-307">**Recommendations:** We recommend that you upgrade all of the UE-V 1.0 Agents in a computing environment, but it is not required.</span></span> <span data-ttu-id="fa228-308">UE-V 2. las plantillas de ubicación de configuración de UE pueden interactuar con un agente de UE-V 1,0 porque solo comparten la configuración de la ruta de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="fa228-308">UE-V 2.x settings location templates can interact with a UE-V 1.0 Agent because they only share the settings from the settings storage path.</span></span> <span data-ttu-id="fa228-309">Sin embargo, le recomendamos que mueva las implementaciones a una única versión de agente para simplificar la administración y para que sea compatible con UE-V.</span><span class="sxs-lookup"><span data-stu-id="fa228-309">We recommend, however, that you move the deployments to a single agent version to simplify management and to support UE-V.</span></span>

### <span data-ttu-id="fa228-310">Reparar el agente UE-V después de una actualización incorrecta</span><span class="sxs-lookup"><span data-stu-id="fa228-310">Repair the UE-V Agent after an unsuccessful upgrade</span></span>

<span data-ttu-id="fa228-311">Es posible que se produzcan errores después de intentar una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="fa228-311">You might experience errors after you attempt one of the following operations:</span></span>

-   <span data-ttu-id="fa228-312">Actualizar de UE-V 1,0 a UE-V 2</span><span class="sxs-lookup"><span data-stu-id="fa228-312">Upgrade from UE-V 1.0 to UE-V 2</span></span>

-   <span data-ttu-id="fa228-313">Actualice a una versión más reciente de Windows, por ejemplo, de Windows 7 a Windows 8 o de Windows 8 a Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="fa228-313">Upgrade to a newer version of Windows, for example, from Windows 7 to Windows 8 or from Windows 8 to Windows 8.1.</span></span>

-   <span data-ttu-id="fa228-314">Desinstalar el agente después de actualizar el agente de UE-V</span><span class="sxs-lookup"><span data-stu-id="fa228-314">Uninstall the agent after upgrading the UE-V Agent</span></span>

<span data-ttu-id="fa228-315">Para resolver cualquier problema, intente reparar el agente UE-V escribiendo este comando en un símbolo del sistema en el equipo en el que está instalado el agente.</span><span class="sxs-lookup"><span data-stu-id="fa228-315">To resolve any issues, attempt to repair the UE-V Agent by entering this command at a command prompt on the computer where the agent is installed.</span></span>

``` syntax
msiexec.exe /f "<path to msi file>" /quiet /norestart /l*v "%temp%\UE-VAgentInstaller.log
```

<span data-ttu-id="fa228-316">Puede volver a intentar realizar el proceso de desinstalación o actualizar instalando la versión más reciente de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="fa228-316">You can then retry the uninstall process or upgrade by installing the newer version of the UE-V Agent.</span></span>






## <span data-ttu-id="fa228-317">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fa228-317">Related topics</span></span>


[<span data-ttu-id="fa228-318">Preparar una implementación de UE-V 2. x</span><span class="sxs-lookup"><span data-stu-id="fa228-318">Prepare a UE-V 2.x Deployment</span></span>](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[<span data-ttu-id="fa228-319">Implementar UE-V 2. x para aplicaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="fa228-319">Deploy UE-V 2.x for Custom Applications</span></span>](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)









