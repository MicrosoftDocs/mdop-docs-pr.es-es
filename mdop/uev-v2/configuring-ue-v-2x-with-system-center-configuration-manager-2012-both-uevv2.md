---
title: Configuración de UE-V 2. x con System Center Configuration Manager 2012
description: Configuración de UE-V 2. x con System Center Configuration Manager 2012
author: dansimp
ms.assetid: 9a4e2a74-7646-4a77-b58f-2b4456487295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 2ff9ccc1a17db31471549ece37461558768c3a2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824410"
---
# <span data-ttu-id="9182c-103">Configuración de UE-V 2. x con System Center Configuration Manager 2012</span><span class="sxs-lookup"><span data-stu-id="9182c-103">Configuring UE-V 2.x with System Center Configuration Manager 2012</span></span>


<span data-ttu-id="9182c-104">Después de instalar la virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 o 2,1 SP1 y las características requeridas, UE-V debe estar configurado.</span><span class="sxs-lookup"><span data-stu-id="9182c-104">After you install Microsoft User Experience Virtualization (UE-V) 2.0, 2.1, or 2.1 SP1 and their required features, UE-V must be configured.</span></span> <span data-ttu-id="9182c-105">El paquete de configuración de UE-V proporciona a los administradores una manera de usar la característica de configuración de cumplimiento de System Center Configuration Manager 2012 SP1 o posterior para aplicar configuraciones coherentes en los sitios donde se instalan UE-V y Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9182c-105">The UE-V Configuration Pack provides a way for administrators to use the Compliance Settings feature of System Center Configuration Manager 2012 SP1 or later to apply consistent configurations across sites where UE-V and Configuration Manager are installed.</span></span>

## <span data-ttu-id="9182c-106">Características compatibles con el paquete de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="9182c-106">UE-V Configuration Pack supported features</span></span>


<span data-ttu-id="9182c-107">El paquete de configuración de UE-V incluye herramientas para realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="9182c-107">The UE-V Configuration Pack includes tools to perform the following tasks:</span></span>

-   <span data-ttu-id="9182c-108">Crear o actualizar las líneas de distribución de plantillas de la ubicación de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="9182c-108">Create or update UE-V settings location template distribution baselines.</span></span>

    -   <span data-ttu-id="9182c-109">Definir plantillas de UE-V para que se registren o no</span><span class="sxs-lookup"><span data-stu-id="9182c-109">Define UE-V templates to be registered or unregistered</span></span>

    -   <span data-ttu-id="9182c-110">Actualizar los elementos de configuración de la plantilla UE-V y las líneas de base como plantillas se agregan o actualizan</span><span class="sxs-lookup"><span data-stu-id="9182c-110">Update UE-V template configuration items and baselines as templates are added or updated</span></span>

    -   <span data-ttu-id="9182c-111">Distribuir y registrar plantillas de UE-V mediante el uso de correcciones de elementos de configuración estándar</span><span class="sxs-lookup"><span data-stu-id="9182c-111">Distribute and register UE-V templates using standard Configuration Item remediation</span></span>

-   <span data-ttu-id="9182c-112">Cree o actualice un elemento de configuración de directiva de UE-V Agent para establecer o borrar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="9182c-112">Create or update a UE-V Agent policy configuration item to set or clear these settings.</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9182c-113">Tamaño máximo del paquete</span><span class="sxs-lookup"><span data-stu-id="9182c-113">Max package size</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9182c-114">Habilitar o deshabilitar la sincronización de aplicaciones de Windows</span><span class="sxs-lookup"><span data-stu-id="9182c-114">Enable/disable Windows app sync</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9182c-115">Esperar sincronización al iniciar la aplicación</span><span class="sxs-lookup"><span data-stu-id="9182c-115">Wait for sync on application start</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9182c-116">Configuración de retraso de importación</span><span class="sxs-lookup"><span data-stu-id="9182c-116">Setting import delay</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9182c-117">Sincronizar aplicaciones de Windows no enumeradas</span><span class="sxs-lookup"><span data-stu-id="9182c-117">Sync unlisted Windows apps</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9182c-118">Esperar sincronización al iniciar sesión</span><span class="sxs-lookup"><span data-stu-id="9182c-118">Wait for sync on logon</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9182c-119">Notificación de importación de configuración</span><span class="sxs-lookup"><span data-stu-id="9182c-119">Settings import notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9182c-120">Dirección URL de contacto de ti</span><span class="sxs-lookup"><span data-stu-id="9182c-120">IT contact URL</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9182c-121">Esperar el tiempo de espera de la sincronización</span><span class="sxs-lookup"><span data-stu-id="9182c-121">Wait for sync timeout</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9182c-122">Configuración ruta de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="9182c-122">Settings storage path</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9182c-123">Texto descriptivo de contacto de ti</span><span class="sxs-lookup"><span data-stu-id="9182c-123">IT contact descriptive text</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9182c-124">Ruta del catálogo de plantillas de configuración</span><span class="sxs-lookup"><span data-stu-id="9182c-124">Settings template catalog path</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9182c-125">Habilitación de la sincronización</span><span class="sxs-lookup"><span data-stu-id="9182c-125">Sync enablement</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9182c-126">Icono de bandeja habilitado</span><span class="sxs-lookup"><span data-stu-id="9182c-126">Tray icon enabled</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9182c-127">Iniciar o detener el servicio del agente de UE-V</span><span class="sxs-lookup"><span data-stu-id="9182c-127">Start/Stop UE-V agent service</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9182c-128">Método de sincronización</span><span class="sxs-lookup"><span data-stu-id="9182c-128">Sync method</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9182c-129">Notificación de primer uso</span><span class="sxs-lookup"><span data-stu-id="9182c-129">First use notification</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9182c-130">Definir qué aplicaciones de Windows van a ser la configuración de itinerancia</span><span class="sxs-lookup"><span data-stu-id="9182c-130">Define which Windows apps will roam settings</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9182c-131">Tiempo de espera de sincronización</span><span class="sxs-lookup"><span data-stu-id="9182c-131">Sync timeout</span></span></p></td>
    <td align="left"><p></p></td>
    <td align="left"><p></p></td>
    </tr>
    </tbody>
    </table>

     

-   <span data-ttu-id="9182c-132">Comprobar el cumplimiento mediante la confirmación de que se está ejecutando UE-V.</span><span class="sxs-lookup"><span data-stu-id="9182c-132">Verify compliance by confirming that UE-V is running.</span></span>

## <span data-ttu-id="9182c-133">Generar un elemento de configuración de directiva de UE-V Agent</span><span class="sxs-lookup"><span data-stu-id="9182c-133">Generate a UE-V Agent Policy Configuration Item</span></span>


<span data-ttu-id="9182c-134">Todas las directivas y la configuración de los agentes UE-V se distribuyen a través de un solo elemento de configuración que se genera con la herramienta UevAgentPolicyGenerator.exe.</span><span class="sxs-lookup"><span data-stu-id="9182c-134">All UE-V Agent policy and configuration is distributed through a single configuration item that is generated using the UevAgentPolicyGenerator.exe tool.</span></span> <span data-ttu-id="9182c-135">Esta herramienta lee la configuración deseada de un archivo de configuración XML y crea un CI que contiene la configuración de detección y corrección necesaria para que el equipo cumpla con las normas.</span><span class="sxs-lookup"><span data-stu-id="9182c-135">This tool reads the desired configuration from an XML configuration file and creates a CI containing the discovery and remediation settings needed to bring the machine into compliance.</span></span>

<span data-ttu-id="9182c-136">El archivo CAB del elemento de configuración de la Directiva UE-V Agent se crea con la herramienta de línea de comandos UevTemplateBaselineGenerator.exe, que tiene estos parámetros:</span><span class="sxs-lookup"><span data-stu-id="9182c-136">The UE-V Agent policy configuration item CAB file is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="9182c-137">Código de sitio del sitio &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="9182c-137">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="9182c-138">&lt;Nombre &gt; de nombre opcional: el valor predeterminado es "UE-V Agent Policy" si no está presente</span><span class="sxs-lookup"><span data-stu-id="9182c-138">PolicyName &lt;name&gt; Optional: Defaults to “UE-V Agent Policy” if not present</span></span>

-   <span data-ttu-id="9182c-139">&lt;La descripción &gt; de PolicyDescription es opcional: Si no está presente, se proporciona una descripción</span><span class="sxs-lookup"><span data-stu-id="9182c-139">PolicyDescription &lt;description&gt; Optional: A description is provided if not present</span></span>

-   <span data-ttu-id="9182c-140">CabFilePath &lt; ruta de acceso completa del elemento de configuración. Archivo CAB&gt;</span><span class="sxs-lookup"><span data-stu-id="9182c-140">CabFilePath &lt;full path to configuration item .CAB file&gt;</span></span>

-   <span data-ttu-id="9182c-141">ConfigurationFile &lt; ruta de acceso completa del archivo XML de configuración del agente&gt;</span><span class="sxs-lookup"><span data-stu-id="9182c-141">ConfigurationFile &lt;full path to agent configuration XML file&gt;</span></span>

<span data-ttu-id="9182c-142">**Nota:**  Puede que sea necesario cambiar la Directiva de ejecución de PowerShell para permitir que estas secuencias de comandos se ejecuten en su entorno.</span><span class="sxs-lookup"><span data-stu-id="9182c-142">**Note** It might be necessary to change the PowerShell execution policy to allow these scripts to run in your environment.</span></span> <span data-ttu-id="9182c-143">Realice estos pasos en la consola de Configuration Manager:</span><span class="sxs-lookup"><span data-stu-id="9182c-143">Perform these steps in the Configuration Manager console:</span></span>

1.  <span data-ttu-id="9182c-144">Seleccionar \*\* &gt; &gt; propiedades de configuración de cliente de administración\*\*</span><span class="sxs-lookup"><span data-stu-id="9182c-144">Select **Administration &gt; Client Settings &gt; Properties**</span></span>

2.  <span data-ttu-id="9182c-145">En la pestaña **agente de usuario** , establezca la Directiva de ejecución de **PowerShell** para **omitir**</span><span class="sxs-lookup"><span data-stu-id="9182c-145">In the **User Agent** tab, set the **PowerShell Execution Policy** to **Bypass**</span></span>

<a href="" id="create"></a>**<span data-ttu-id="9182c-146">Crear el primer elemento de configuración de directiva de UE-V</span><span class="sxs-lookup"><span data-stu-id="9182c-146">Create the First UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="9182c-147">Copie el archivo de configuración de configuración predeterminado del directorio de instalación de UE-V config Pack en una ubicación visible para la consola de administración de ConfigMgr:</span><span class="sxs-lookup"><span data-stu-id="9182c-147">Copy the default settings configuration file from the UE-V Config Pack installation directory to a location visible to your ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\AgentConfiguration.xml c:\<target path>
    ```

    <span data-ttu-id="9182c-148">El archivo de configuración predeterminado contiene cinco secciones:</span><span class="sxs-lookup"><span data-stu-id="9182c-148">The default configuration file contains five sections:</span></span>

    <a href="" id="computer-policy"></a>**<span data-ttu-id="9182c-149">Directiva de equipo</span><span class="sxs-lookup"><span data-stu-id="9182c-149">Computer Policy</span></span>**  
    <span data-ttu-id="9182c-150">Todas las configuraciones de nivel de equipo UE-V.</span><span class="sxs-lookup"><span data-stu-id="9182c-150">All UE-V machine level settings.</span></span> <span data-ttu-id="9182c-151">El atributo DesiredState se puede</span><span class="sxs-lookup"><span data-stu-id="9182c-151">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="9182c-152">**Establecer** que el valor se asigne en el registro</span><span class="sxs-lookup"><span data-stu-id="9182c-152">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="9182c-153">**Borrar** para quitar la configuración</span><span class="sxs-lookup"><span data-stu-id="9182c-153">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="9182c-154">**No administrados** para dejar el elemento de configuración en su estado actual</span><span class="sxs-lookup"><span data-stu-id="9182c-154">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="9182c-155">No quitar líneas de esta sección.</span><span class="sxs-lookup"><span data-stu-id="9182c-155">Do not remove lines from this section.</span></span> <span data-ttu-id="9182c-156">En su lugar, establezca el DesiredState en ' Unmanaged ' si no desea que Configuration Manager modifique los valores actuales o predeterminados.</span><span class="sxs-lookup"><span data-stu-id="9182c-156">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="currentcomputeruserpolicy"></a>**<span data-ttu-id="9182c-157">CurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="9182c-157">CurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="9182c-158">Toda la configuración del nivel de usuario de UE-V.</span><span class="sxs-lookup"><span data-stu-id="9182c-158">All UE-V user level settings.</span></span> <span data-ttu-id="9182c-159">Estas entradas invalidan la configuración del equipo de un usuario.</span><span class="sxs-lookup"><span data-stu-id="9182c-159">These entries override the machine settings for a user.</span></span> <span data-ttu-id="9182c-160">El atributo DesiredState se puede</span><span class="sxs-lookup"><span data-stu-id="9182c-160">The DesiredState attribute can be</span></span>

    -   <span data-ttu-id="9182c-161">**Establecer** que el valor se asigne en el registro</span><span class="sxs-lookup"><span data-stu-id="9182c-161">**Set** to have the value assigned in the registry</span></span>

    -   <span data-ttu-id="9182c-162">**Borrar** para quitar la configuración</span><span class="sxs-lookup"><span data-stu-id="9182c-162">**Clear** to remove the setting</span></span>

    -   <span data-ttu-id="9182c-163">**No administrados** para dejar el elemento de configuración en su estado actual</span><span class="sxs-lookup"><span data-stu-id="9182c-163">**Unmanaged** to have the configuration item left at its current state</span></span>

    <span data-ttu-id="9182c-164">No quitar líneas de esta sección.</span><span class="sxs-lookup"><span data-stu-id="9182c-164">Do not remove lines from this section.</span></span> <span data-ttu-id="9182c-165">En su lugar, establezca el DesiredState en ' Unmanaged ' si no desea que Configuration Manager modifique los valores actuales o predeterminados.</span><span class="sxs-lookup"><span data-stu-id="9182c-165">Instead, set the DesiredState to ‘Unmanaged’ if you do not want Configuration Manager to alter current or default values.</span></span>

    <a href="" id="services"></a>**<span data-ttu-id="9182c-166">Servicios</span><span class="sxs-lookup"><span data-stu-id="9182c-166">Services</span></span>**  
    <span data-ttu-id="9182c-167">Las entradas de esta sección controlan la operación del servicio.</span><span class="sxs-lookup"><span data-stu-id="9182c-167">Entries in this section control service operation.</span></span> <span data-ttu-id="9182c-168">El archivo de configuración predeterminado contiene una sola entrada para el UevAgentService.</span><span class="sxs-lookup"><span data-stu-id="9182c-168">The default configuration file contains a single entry for the UevAgentService.</span></span> <span data-ttu-id="9182c-169">El atributo DesiredState se puede establecer en **Running** o **Stopped**.</span><span class="sxs-lookup"><span data-stu-id="9182c-169">The DesiredState attribute can be set to **Running** or **Stopped**.</span></span>

    <a href="" id="windows8appscomputerpolicy"></a>**<span data-ttu-id="9182c-170">Windows8AppsComputerPolicy</span><span class="sxs-lookup"><span data-stu-id="9182c-170">Windows8AppsComputerPolicy</span></span>**  
    <span data-ttu-id="9182c-171">Toda la configuración de sincronización de aplicaciones de Windows en el nivel de equipo.</span><span class="sxs-lookup"><span data-stu-id="9182c-171">All machine level Windows app synchronization settings.</span></span> <span data-ttu-id="9182c-172">A cada PackageFamilyName enumerado en esta sección se le puede asignar una DesiredState de</span><span class="sxs-lookup"><span data-stu-id="9182c-172">Each PackageFamilyName listed in this section can be assigned a DesiredState of</span></span>

    -   <span data-ttu-id="9182c-173">**Habilitado** para que la configuración sea móvil</span><span class="sxs-lookup"><span data-stu-id="9182c-173">**Enabled** to have settings roam</span></span>

    -   <span data-ttu-id="9182c-174">**Deshabilitado** para evitar la configuración de itinerancia</span><span class="sxs-lookup"><span data-stu-id="9182c-174">**Disabled** to prevent settings from roaming</span></span>

    -   <span data-ttu-id="9182c-175">**Desactivado** para que se elimine la entrada del control UE-V</span><span class="sxs-lookup"><span data-stu-id="9182c-175">**Cleared** to have the entry removed from UE-V control</span></span>

    <span data-ttu-id="9182c-176">Se pueden agregar líneas adicionales a esta sección basándose en la lista de aplicaciones de Windows instaladas que se pueden ver con el cmdlet de PowerShell GetAppxPackage.</span><span class="sxs-lookup"><span data-stu-id="9182c-176">Additional lines can be added to this section based on the list of installed Windows apps that can be viewed using the PowerShell cmdlet GetAppxPackage.</span></span>

    <a href="" id="windows8appscurrentcomputeruserpolicy"></a>**<span data-ttu-id="9182c-177">Windows8AppsCurrentComputerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="9182c-177">Windows8AppsCurrentComputerUserPolicy</span></span>**  
    <span data-ttu-id="9182c-178">Es idéntico a la Windows8AppsComputerPolicy con una configuración que suplanta la configuración del equipo para un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="9182c-178">Identical to the Windows8AppsComputerPolicy with settings that override machine settings for an individual user.</span></span>

2.  <span data-ttu-id="9182c-179">Edite el archivo de configuración cambiando los campos estado y valor que desee.</span><span class="sxs-lookup"><span data-stu-id="9182c-179">Edit the configuration file by changing the desired state and value fields.</span></span>

3.  <span data-ttu-id="9182c-180">Ejecute este comando en un equipo que ejecute la consola de administración de ConfigMgr:</span><span class="sxs-lookup"><span data-stu-id="9182c-180">Run this command on a machine running the ConfigMgr Admin Console:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevAgentPolicyGenerator.exe –Site ABC –CabFilePath "C:\MyCabFiles\UevPolicyItem.cab" –ConfigurationFile "c:\AgentConfiguration.xml"
    ```

4.  <span data-ttu-id="9182c-181">Importar el archivo CAB con la consola de ConfigMgr o la importación de PowerShell CMConfigurationItem</span><span class="sxs-lookup"><span data-stu-id="9182c-181">Import the CAB file using ConfigMgr console or PowerShell Import-CMConfigurationItem</span></span>

**<span data-ttu-id="9182c-182">Actualizar un elemento de configuración de directiva de UE-V</span><span class="sxs-lookup"><span data-stu-id="9182c-182">Update a UE-V Policy Configuration Item</span></span>**

1.  <span data-ttu-id="9182c-183">Edite el archivo de configuración cambiando los campos estado y valor que desee.</span><span class="sxs-lookup"><span data-stu-id="9182c-183">Edit the configuration file by changing the desired state and value fields.</span></span>

2.  <span data-ttu-id="9182c-184">Ejecute el comando del paso 3 en [crear el primer elemento de configuración de directiva de UE-V](#create).</span><span class="sxs-lookup"><span data-stu-id="9182c-184">Run the command from Step 3 in [Create the First UE-V Policy Configuration Item](#create).</span></span> <span data-ttu-id="9182c-185">Si cambió el nombre con el parámetro PolicyName, asegúrese de que escribe el mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="9182c-185">If you changed the name with the PolicyName parameter, make sure you enter the same name.</span></span>

3.  <span data-ttu-id="9182c-186">Reimporte el archivo CAB.</span><span class="sxs-lookup"><span data-stu-id="9182c-186">Reimport the CAB file.</span></span> <span data-ttu-id="9182c-187">Se actualizará la versión de ConfigMgr.</span><span class="sxs-lookup"><span data-stu-id="9182c-187">The version in ConfigMgr will be updated.</span></span>

## <span data-ttu-id="9182c-188">Generar una línea base de plantilla de UE-V</span><span class="sxs-lookup"><span data-stu-id="9182c-188">Generate a UE-V Template Baseline</span></span>
<span data-ttu-id="9182c-189">Las plantillas de UE-V se distribuyen con una línea base que contiene varios elementos de configuración.</span><span class="sxs-lookup"><span data-stu-id="9182c-189">UE-V templates are distributed using a baseline containing multiple configuration items.</span></span> <span data-ttu-id="9182c-190">Cada elemento de configuración contiene los scripts de detección y corrección necesarios para instalar una plantilla de UE-V.</span><span class="sxs-lookup"><span data-stu-id="9182c-190">Each configuration item contains the discovery and remediation scripts needed to install one UE-V template.</span></span> <span data-ttu-id="9182c-191">La plantilla real UE-V se incrusta en el script de corrección para la distribución mediante la funcionalidad de elemento de configuración estándar.</span><span class="sxs-lookup"><span data-stu-id="9182c-191">The actual UE-V template is embedded within the remediation script for distribution using standard Configuration Item functionality.</span></span>

<span data-ttu-id="9182c-192">La línea base de la plantilla UE-V se crea con la herramienta de línea de comandos UevTemplateBaselineGenerator.exe, que tiene estos parámetros:</span><span class="sxs-lookup"><span data-stu-id="9182c-192">The UE-V template baseline is created using the UevTemplateBaselineGenerator.exe command line tool, which has these parameters:</span></span>

-   <span data-ttu-id="9182c-193">Código de sitio del sitio &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="9182c-193">Site &lt;site code&gt;</span></span>

-   <span data-ttu-id="9182c-194">&lt;Nombre &gt; de BaselineName (opcional: el valor predeterminado es "UE-V template Distributing Baseline" si no está presente)</span><span class="sxs-lookup"><span data-stu-id="9182c-194">BaselineName &lt;name&gt; (Optional: defaults to “UE-V Template Distribution Baseline” if not present)</span></span>

-   <span data-ttu-id="9182c-195">&lt;Descripción &gt; de BaselineDescription (opcional: se proporciona una descripción si no está presente)</span><span class="sxs-lookup"><span data-stu-id="9182c-195">BaselineDescription &lt;description&gt; (Optional: a description is provided if not present)</span></span>

-   <span data-ttu-id="9182c-196">&lt;Carpeta de plantillas de TemplateFolder UE-V&gt;</span><span class="sxs-lookup"><span data-stu-id="9182c-196">TemplateFolder &lt;UE-V template folder&gt;</span></span>

-   <span data-ttu-id="9182c-197">Registrar &lt; lista de archivos de plantilla separada por comas&gt;</span><span class="sxs-lookup"><span data-stu-id="9182c-197">Register &lt;comma separated template file list&gt;</span></span>

-   <span data-ttu-id="9182c-198">Eliminar la &lt; lista de plantillas separadas por comas&gt;</span><span class="sxs-lookup"><span data-stu-id="9182c-198">Unregister &lt;comma separated template list&gt;</span></span>

-   <span data-ttu-id="9182c-199">CabFilePath &lt; ruta de acceso completa al archivo CAB de línea base que se va a generar&gt;</span><span class="sxs-lookup"><span data-stu-id="9182c-199">CabFilePath &lt;Full path to baseline CAB file to generate&gt;</span></span>

<span data-ttu-id="9182c-200">El resultado es un archivo CAB de línea base que está listo para importarlo a Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9182c-200">The result is a baseline CAB file that is ready for import into Configuration Manager.</span></span> <span data-ttu-id="9182c-201">Si, en una fecha futura, actualiza o agrega una plantilla, puede volver a ejecutar el comando con el mismo nombre de línea base.</span><span class="sxs-lookup"><span data-stu-id="9182c-201">If at a future date, you update or add a template, you can rerun the command using the same baseline name.</span></span> <span data-ttu-id="9182c-202">Importar el archivo CAB genera actualizaciones de versión de CI en las plantillas modificadas.</span><span class="sxs-lookup"><span data-stu-id="9182c-202">Importing the CAB results in CI version updates on the changed templates.</span></span>

### <a href="" id="create2"></a><span data-ttu-id="9182c-203">Crear la primera línea base de la plantilla UE-V</span><span class="sxs-lookup"><span data-stu-id="9182c-203">Create the First UE-V Template Baseline</span></span>

1.  <span data-ttu-id="9182c-204">Cree un conjunto "maestro" de plantillas de UE-V en una ubicación de carpeta estable visible para el equipo que ejecuta la consola de administración de ConfigMgr.</span><span class="sxs-lookup"><span data-stu-id="9182c-204">Create a “master” set of UE-V templates in a stable folder location visible to the machine running your ConfigMgr Admin Console.</span></span> <span data-ttu-id="9182c-205">A medida que se agregan o se actualizan las plantillas, esta carpeta es el lugar donde se extraen para su distribución.</span><span class="sxs-lookup"><span data-stu-id="9182c-205">As templates are added or updated, this folder is where they are pulled for distribution.</span></span> <span data-ttu-id="9182c-206">La lista inicial de plantillas se puede copiar desde un equipo con UE-V instalado.</span><span class="sxs-lookup"><span data-stu-id="9182c-206">The initial list of templates can be copied from a machine with UE-V installed.</span></span> <span data-ttu-id="9182c-207">La ubicación predeterminada de la plantilla es C:\\Archivos de Programa\\microsoft User Experience Virtualization\\Templates.</span><span class="sxs-lookup"><span data-stu-id="9182c-207">The default template location is C:\\Program Files\\Microsoft User Experience Virtualization\\Templates.</span></span>

2.  <span data-ttu-id="9182c-208">Cree un archivo de text.bat donde pueda agregar el comando generador de plantillas.</span><span class="sxs-lookup"><span data-stu-id="9182c-208">Create a text.bat file where you can add the template generator command.</span></span> <span data-ttu-id="9182c-209">Esto es opcional, pero hará que la regeneración sea más sencilla si guarda los parámetros de comando.</span><span class="sxs-lookup"><span data-stu-id="9182c-209">This is optional, but will make regeneration simpler if you save the command parameters.</span></span>

3.  <span data-ttu-id="9182c-210">Agregue el comando y los parámetros al archivo. bat que generará la línea base.</span><span class="sxs-lookup"><span data-stu-id="9182c-210">Add the command and parameters to the .bat file that will generate the baseline.</span></span> <span data-ttu-id="9182c-211">En el ejemplo siguiente se crea una línea base que distribuye el Bloc de notas y la calculadora:</span><span class="sxs-lookup"><span data-stu-id="9182c-211">The following example creates a baseline that distributes Notepad and Calculator:</span></span>

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevTemplateBaselineGenerator.exe –Site "ABC" –TemplateFolder "C:\ProductionUevTemplates" –Register "MicrosoftNotepad.xml, MicrosoftCalculator.xml" –CabFilePath "C:\MyCabFiles\UevTemplateBaseline.cab"
    ```

4.  <span data-ttu-id="9182c-212">Ejecute el archivo. bat para crear UevTemplateBaseline.cab listo para importarlo a Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="9182c-212">Run the .bat file to create UevTemplateBaseline.cab ready for import into Configuration Manager.</span></span>

### <span data-ttu-id="9182c-213">Actualizar una línea base de la plantilla UE-V</span><span class="sxs-lookup"><span data-stu-id="9182c-213">Update a UE-V Template Baseline</span></span>

<span data-ttu-id="9182c-214">El generador de plantillas usa la versión de la plantilla para determinar si se debe actualizar una plantilla.</span><span class="sxs-lookup"><span data-stu-id="9182c-214">The template generator uses the template version to determine if a template should be updated.</span></span> <span data-ttu-id="9182c-215">Si hace que una plantilla cambie y actualiza la versión, el generador de línea base compara la plantilla de la carpeta maestra con la plantilla contenida en el CI en el servidor de ConfigMgr.</span><span class="sxs-lookup"><span data-stu-id="9182c-215">If you make a template change and update the version, the baseline generator compares the template in your master folder with the template contained in the CI on the ConfigMgr server.</span></span> <span data-ttu-id="9182c-216">Si se encuentra una diferencia, la línea base generada y las versiones modificada de CI se actualizan.</span><span class="sxs-lookup"><span data-stu-id="9182c-216">If a difference is found, the generated baseline and modified CI versions are updated.</span></span>

<span data-ttu-id="9182c-217">Para distribuir una nueva plantilla del Bloc de notas, debe seguir estos pasos:</span><span class="sxs-lookup"><span data-stu-id="9182c-217">To distribute a new Notepad template, you would perform these steps:</span></span>

1.  <span data-ttu-id="9182c-218">Actualice la plantilla y la versión de la plantilla que se encuentran en el &lt; &gt; elemento de versión de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="9182c-218">Update the template and template version located in the &lt;Version&gt; element of the template.</span></span>

2.  <span data-ttu-id="9182c-219">Copie la plantilla en el directorio de plantillas maestras.</span><span class="sxs-lookup"><span data-stu-id="9182c-219">Copy the template to your master template directory.</span></span>

3.  <span data-ttu-id="9182c-220">Ejecute el comando en el archivo. bat que creó en el paso 3 en [crear la primera línea base de la plantilla UE-V](#create2).</span><span class="sxs-lookup"><span data-stu-id="9182c-220">Run the command in the .bat file that you created in Step 3 in [Create the First UE-V Template Baseline](#create2).</span></span>

4.  <span data-ttu-id="9182c-221">Importe el archivo CAB generado en ConfigMgr con la consola o importación de PowerShell-CMBaseline.</span><span class="sxs-lookup"><span data-stu-id="9182c-221">Import the generated CAB file into ConfigMgr using the console or PowerShell Import-CMBaseline.</span></span>

## <span data-ttu-id="9182c-222">Obtener el paquete de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="9182c-222">Get the UE-V Configuration Pack</span></span>


<span data-ttu-id="9182c-223">El paquete de configuración de UE-V para Configuration Manager 2012 SP1 o versiones posteriores puede descargarse [aquí](https://go.microsoft.com/fwlink/?LinkId=317263).</span><span class="sxs-lookup"><span data-stu-id="9182c-223">The UE-V Configuration Pack for Configuration Manager 2012 SP1 or later can be downloaded [here](https://go.microsoft.com/fwlink/?LinkId=317263).</span></span>






## <span data-ttu-id="9182c-224">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9182c-224">Related topics</span></span>


[<span data-ttu-id="9182c-225">Administrar configuraciones para UE-V 2.x</span><span class="sxs-lookup"><span data-stu-id="9182c-225">Manage Configurations for UE-V 2.x</span></span>](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





