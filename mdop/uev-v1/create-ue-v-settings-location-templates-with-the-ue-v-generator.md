---
title: Crear plantillas de ubicación de configuración de UE-V con el generador de UE-V
description: Crear plantillas de ubicación de configuración de UE-V con el generador de UE-V
author: dansimp
ms.assetid: b8e50e2f-0cc6-4f74-bb48-c471fefdc7d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ef7e3e5d00a95b9fcfc426207ce04f928cc0ebbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826641"
---
# <span data-ttu-id="98081-103">Crear plantillas de ubicación de configuración de UE-V con el generador de UE-V</span><span class="sxs-lookup"><span data-stu-id="98081-103">Create UE-V Settings Location Templates with the UE-V Generator</span></span>


<span data-ttu-id="98081-104">Virtualización de la experiencia del usuario de Microsoft (UE-V) usa *las plantillas de ubicación de configuración* para mover la configuración de la aplicación entre equipos de usuario.</span><span class="sxs-lookup"><span data-stu-id="98081-104">Microsoft User Experience Virtualization (UE-V) uses *settings location templates* to roam application settings between user computers.</span></span> <span data-ttu-id="98081-105">Se incluyen algunas plantillas de ubicación de configuración estándar con la virtualización de la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="98081-105">Some standard settings location templates are included with User Experience Virtualization.</span></span> <span data-ttu-id="98081-106">También puede crear, editar o validar plantillas de ubicación de configuración personalizadas con el generador de UE-V.</span><span class="sxs-lookup"><span data-stu-id="98081-106">You can also create, edit, or validate custom settings location templates with the UE-V Generator.</span></span>

<span data-ttu-id="98081-107">El generador de UE-V supervisa una aplicación para descubrir y capturar las ubicaciones donde la aplicación almacena su configuración.</span><span class="sxs-lookup"><span data-stu-id="98081-107">The UE-V Generator monitors an application to discover and capture the locations where the application stores its settings.</span></span> <span data-ttu-id="98081-108">La aplicación que se está supervisando debe ser una aplicación tradicional.</span><span class="sxs-lookup"><span data-stu-id="98081-108">The application that is being monitored must be a traditional application.</span></span> <span data-ttu-id="98081-109">El generador de UE-V no puede crear una plantilla de ubicación de configuración a partir de los siguientes tipos de aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="98081-109">The UE-V Generator cannot create a settings location template from the following application types:</span></span>

-   <span data-ttu-id="98081-110">Aplicaciones virtualizadas</span><span class="sxs-lookup"><span data-stu-id="98081-110">Virtualized applications</span></span>

-   <span data-ttu-id="98081-111">Aplicación ofrecida a través de servicios de Terminal Server</span><span class="sxs-lookup"><span data-stu-id="98081-111">Application offered through terminal services</span></span>

-   <span data-ttu-id="98081-112">Aplicaciones Java</span><span class="sxs-lookup"><span data-stu-id="98081-112">Java applications</span></span>

-   <span data-ttu-id="98081-113">Aplicaciones para Windows 8</span><span class="sxs-lookup"><span data-stu-id="98081-113">Windows 8 applications</span></span>

<span data-ttu-id="98081-114">**Nota:**  Las plantillas de UE-V no se pueden crear desde aplicaciones virtualizadas o aplicaciones de servicios de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="98081-114">**Note** UE-V templates cannot be created from virtualized applications or terminal services applications.</span></span> <span data-ttu-id="98081-115">Sin embargo, la configuración sincronizada con las plantillas se puede aplicar a esas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="98081-115">However, settings synchronized using the templates can be applied to those applications.</span></span> <span data-ttu-id="98081-116">Para crear plantillas que admitan la infraestructura de escritorio virtual (VDI) y las aplicaciones de servicios de Terminal Server, abra una versión de Windows Installer (. msi) de la aplicación con el generador de UE-V.</span><span class="sxs-lookup"><span data-stu-id="98081-116">To create templates that support Virtual Desktop Infrastructure (VDI) and terminal services applications, open a Windows Installer File (.msi) version of the application with UE-V Generator.</span></span>

 

**<span data-ttu-id="98081-117">Ubicaciones excluidas</span><span class="sxs-lookup"><span data-stu-id="98081-117">Excluded Locations</span></span>**

<span data-ttu-id="98081-118">El proceso de descubrimiento excluye las ubicaciones que normalmente almacenan los archivos de software de la aplicación que no se mueven de un equipo a otro.</span><span class="sxs-lookup"><span data-stu-id="98081-118">The discovery process excludes locations which commonly store application software files that do not roam well between user computers or environments.</span></span> <span data-ttu-id="98081-119">Se excluyen los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="98081-119">The following are excluded:</span></span>

-   <span data-ttu-id="98081-120">HKEY \ _CURRENT \ _USER claves de registro y archivos en los que el usuario que ha iniciado sesión no puede escribir valores</span><span class="sxs-lookup"><span data-stu-id="98081-120">HKEY\_CURRENT\_USER registry keys and files to which the logged-on user cannot write values</span></span>

-   <span data-ttu-id="98081-121">HKEY \ _CURRENT \ _USER claves de registro y archivos asociados con la funcionalidad básica del sistema operativo Windows</span><span class="sxs-lookup"><span data-stu-id="98081-121">HKEY\_CURRENT\_USER registry keys and files associated with the core functionality of the Windows operating system</span></span>

-   <span data-ttu-id="98081-122">Todas las claves del registro que se encuentran en la sección HKEY \ _LOCAL \ _MACHINE</span><span class="sxs-lookup"><span data-stu-id="98081-122">All registry keys located in the HKEY\_LOCAL\_MACHINE hive</span></span>

-   <span data-ttu-id="98081-123">Archivos ubicados en los directorios archivos de programa</span><span class="sxs-lookup"><span data-stu-id="98081-123">Files located in Program Files directories</span></span>

-   <span data-ttu-id="98081-124">Archivos que se encuentran en los usuarios \ \ \ [nombre de usuario \] \ \ AppData \ \ LocalLow</span><span class="sxs-lookup"><span data-stu-id="98081-124">Files located in Users \\ \[User name\] \\ AppData \\ LocalLow</span></span>

-   <span data-ttu-id="98081-125">Archivos del sistema operativo Windows ubicados en% systemroot%</span><span class="sxs-lookup"><span data-stu-id="98081-125">Windows operating system files located in %systemroot%</span></span>

<span data-ttu-id="98081-126">Si se necesitan claves de registro y archivos almacenados en estas ubicaciones excluidas para poder mover la configuración de la aplicación, los administradores pueden agregar manualmente las ubicaciones a la plantilla de ubicación de configuración durante el proceso de creación de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="98081-126">If registry keys and files stored in these excluded locations are required in order to roam application settings, administrators can manually add the locations to the settings location template during the template creation process.</span></span>

## <span data-ttu-id="98081-127">Crear plantillas de UE-V</span><span class="sxs-lookup"><span data-stu-id="98081-127">Create UE-V templates</span></span>


<span data-ttu-id="98081-128">Use el generador de UE-V para crear plantillas de ubicación de configuración para las aplicaciones de línea de negocio u otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="98081-128">Use the UE-V Generator to create settings location templates for line-of-business applications or other applications.</span></span> <span data-ttu-id="98081-129">Una vez creada la plantilla de una aplicación, puede implementarla en los equipos para que los usuarios puedan mover la configuración de esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="98081-129">After the template for an application is created, you can deploy the template to computers so users can roam the settings for that application.</span></span>

**<span data-ttu-id="98081-130">Para crear una plantilla de ubicación de configuración de UE-V con el generador de UE-V</span><span class="sxs-lookup"><span data-stu-id="98081-130">To create a UE-V settings location template with the UE-V Generator</span></span>**

1.  <span data-ttu-id="98081-131">Haga clic en **Inicio**, en **todos los programas**, en **Virtualización**de la experiencia del usuario de Microsoft y, por último, en **Microsoft User Experience Virtualization generator**.</span><span class="sxs-lookup"><span data-stu-id="98081-131">Click **Start**, click **All Programs**, click **Microsoft User Experience Virtualization**, and then click **Microsoft User Experience Virtualization Generator**.</span></span>

2.  <span data-ttu-id="98081-132">Haga clic en **crear una plantilla de ubicación de configuración**.</span><span class="sxs-lookup"><span data-stu-id="98081-132">Click **Create a settings location template**.</span></span>

3.  <span data-ttu-id="98081-133">Especifique la aplicación.</span><span class="sxs-lookup"><span data-stu-id="98081-133">Specify the application.</span></span> <span data-ttu-id="98081-134">Busque la ruta de acceso de archivo de la aplicación (. exe) o el acceso directo de la aplicación (. lnk) para el que desea crear una plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="98081-134">Browse to the file path of the application (.exe) or the application shortcut (.lnk) for which you want to create a settings location template.</span></span> <span data-ttu-id="98081-135">Especifique los argumentos de la línea de comandos, si los hay, y el directorio de trabajo, si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="98081-135">Specify the command line arguments, if any, and working directory, if any.</span></span> <span data-ttu-id="98081-136">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="98081-136">Click **Next** to continue.</span></span>

    <span data-ttu-id="98081-137">**Nota:**  Antes de iniciar la aplicación, el sistema muestra un mensaje para el **control de cuentas de usuario**.</span><span class="sxs-lookup"><span data-stu-id="98081-137">**Note** Before the application is started, the system displays a prompt for **User Account Control**.</span></span> <span data-ttu-id="98081-138">El permiso es necesario para supervisar el registro y las ubicaciones de archivos que la aplicación usa para almacenar la configuración.</span><span class="sxs-lookup"><span data-stu-id="98081-138">Permission is required to monitor the registry and file locations that the application uses to store settings.</span></span>

     

4.  <span data-ttu-id="98081-139">Una vez iniciada la aplicación, cierre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="98081-139">After the application starts, close the application.</span></span> <span data-ttu-id="98081-140">El generador de UE-V registra las ubicaciones en las que la aplicación almacena su configuración.</span><span class="sxs-lookup"><span data-stu-id="98081-140">The UE-V Generator records the locations where the application stores its settings.</span></span>

5.  <span data-ttu-id="98081-141">Una vez completado el proceso, haga clic en **siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="98081-141">After the process is complete, click **Next** to continue.</span></span>

6.  <span data-ttu-id="98081-142">Revise y seleccione las casillas situadas junto a las ubicaciones de los archivos de configuración y ubicaciones de configuración del registro que desea mover a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="98081-142">Review and select the check boxes next to the appropriate registry settings locations and settings file locations to roam for this application.</span></span> <span data-ttu-id="98081-143">La lista incluye las dos categorías siguientes para las ubicaciones de configuración:</span><span class="sxs-lookup"><span data-stu-id="98081-143">The list includes the following two categories for settings locations:</span></span>

    -   <span data-ttu-id="98081-144">**Estándar**: configuración de la aplicación que se almacena en el registro en las claves HKEY \ _CURRENT \ _USER o en las carpetas de archivos en \ \ **usuarios** \ \ \ [nombre de usuario \] \ \ **AppData**  \\  **roaming**.</span><span class="sxs-lookup"><span data-stu-id="98081-144">**Standard**: Application settings that are stored in the registry under the HKEY\_CURRENT\_USER keys or in the file folders under \\ **Users** \\ \[User name\] \\ **AppData** \\ **Roaming**.</span></span> <span data-ttu-id="98081-145">El generador de UE-V incluye esta configuración de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="98081-145">The UE-V Generator includes these settings by default.</span></span>

    -   <span data-ttu-id="98081-146">No **estándar**: configuración de la aplicación que se almacena fuera de las ubicaciones especificadas en procedimientos recomendados para el almacenamiento de datos de configuración (opcional).</span><span class="sxs-lookup"><span data-stu-id="98081-146">**Nonstandard**: Application settings that are stored outside the locations specified in the best practices for settings data storage (optional).</span></span> <span data-ttu-id="98081-147">Estos archivos y carpetas se incluyen en **usuarios** \ \ \ [nombre de usuario \] \ \ **AppData**  \\  **local**.</span><span class="sxs-lookup"><span data-stu-id="98081-147">These include files and folders under **Users** \\ \[User name\] \\ **AppData** \\ **Local**.</span></span> <span data-ttu-id="98081-148">Revise estas ubicaciones para determinar si desea incluirlas en la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="98081-148">Review these locations to determine whether to include them in the settings location template.</span></span> <span data-ttu-id="98081-149">Seleccione las casillas de verificación de ubicaciones para incluirlas.</span><span class="sxs-lookup"><span data-stu-id="98081-149">Select the locations check boxes to include them.</span></span>

    <span data-ttu-id="98081-150">Haz clic en **Siguiente** para continuar.</span><span class="sxs-lookup"><span data-stu-id="98081-150">Click **Next** to continue.</span></span>

7.  <span data-ttu-id="98081-151">Revise y edite las ubicaciones de las **propiedades**, las ubicaciones **del registro** y **los archivos** de la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="98081-151">Review and edit any **Properties**, **Registry** locations, and **Files** locations for the settings location template.</span></span>

    -   <span data-ttu-id="98081-152">Edite las propiedades siguientes en la ficha **propiedades** :</span><span class="sxs-lookup"><span data-stu-id="98081-152">Edit the following properties on the **Properties** tab:</span></span>

        -   <span data-ttu-id="98081-153">**Nombre**de la aplicación: el nombre de la aplicación escrito en la descripción de las propiedades de archivos de programa.</span><span class="sxs-lookup"><span data-stu-id="98081-153">**Application Name**: The application name written in the description of the program files properties.</span></span>

        -   <span data-ttu-id="98081-154">**Nombre del programa**: el nombre del programa que se toma de las propiedades del archivo del programa.</span><span class="sxs-lookup"><span data-stu-id="98081-154">**Program name**: The name of the program taken from the program file properties.</span></span> <span data-ttu-id="98081-155">Este nombre suele tener la extensión. exe.</span><span class="sxs-lookup"><span data-stu-id="98081-155">This name usually has the .exe extension.</span></span>

        -   <span data-ttu-id="98081-156">**Versión del producto**: número de versión del producto del archivo. exe de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="98081-156">**Product version**: The product version number of the .exe file of the application.</span></span> <span data-ttu-id="98081-157">Esta propiedad, junto con la versión del archivo, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="98081-157">This property, in conjunction with the File version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="98081-158">Esta propiedad acepta un número de versión principal.</span><span class="sxs-lookup"><span data-stu-id="98081-158">This property accepts a major version number.</span></span> <span data-ttu-id="98081-159">Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplicará a todas las versiones del producto.</span><span class="sxs-lookup"><span data-stu-id="98081-159">If this property is empty, the settings location template will apply to all versions of the product.</span></span>

        -   <span data-ttu-id="98081-160">**Versión**del archivo: el número de versión del archivo the.exe archivo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="98081-160">**File version**: The file version number of the.exe file of the application.</span></span> <span data-ttu-id="98081-161">Esta propiedad, junto con la versión del producto, ayuda a determinar qué aplicaciones se dirigen a través de la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="98081-161">This property, in conjunction with the Product version, helps determine which applications are targeted by the settings location template.</span></span> <span data-ttu-id="98081-162">Esta propiedad acepta un número de versión principal.</span><span class="sxs-lookup"><span data-stu-id="98081-162">This property accepts a major version number.</span></span> <span data-ttu-id="98081-163">Si esta propiedad está vacía, la plantilla de ubicación de configuración se aplicará a todas las versiones del programa.</span><span class="sxs-lookup"><span data-stu-id="98081-163">If this property is empty, the settings location template will apply to all versions of the program.</span></span>

        -   <span data-ttu-id="98081-164">**Nombre del autor** de la plantilla (opcional): el nombre del autor de la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="98081-164">**Template author name** (optional): The name of the settings location template author.</span></span>

        -   <span data-ttu-id="98081-165">**Correo electrónico del autor** de la plantilla (opcional): dirección de correo electrónico del autor de la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="98081-165">**Template author email** (optional): The email address of the settings location template author.</span></span>

    -   <span data-ttu-id="98081-166">La ficha **registro** enumera la **clave** y el **ámbito** de las ubicaciones del registro que se incluyen en la plantilla de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="98081-166">The **Registry** tab lists the **Key** and **Scope** of the registry locations that are included in the settings location template.</span></span> <span data-ttu-id="98081-167">Edite las ubicaciones del registro mediante el menú desplegable **tareas** .</span><span class="sxs-lookup"><span data-stu-id="98081-167">Edit the registry locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="98081-168">Las tareas incluyen agregar nuevas claves, editar el nombre o el ámbito de las claves existentes, eliminar claves y examinar el registro en el que se encuentran las claves.</span><span class="sxs-lookup"><span data-stu-id="98081-168">Tasks include adding new keys, editing the name or scope of existing keys, deleting keys, and browsing the registry where the keys are located.</span></span> <span data-ttu-id="98081-169">Use el ámbito **all settings** para incluir todas las opciones de configuración del registro en la clave especificada.</span><span class="sxs-lookup"><span data-stu-id="98081-169">Use the **All Settings** scope to include all the registry settings under the specified key.</span></span> <span data-ttu-id="98081-170">Use la **configuración y** las subclaves para incluir todas las opciones de configuración del registro bajo la clave, las subclaves y la configuración de subclave especificadas.</span><span class="sxs-lookup"><span data-stu-id="98081-170">Use the **All Settings and Subkeys** to include all the registry settings under the specified key, subkeys, and subkey settings.</span></span>

    -   <span data-ttu-id="98081-171">La pestaña **archivos** muestra la ruta de acceso del archivo y la máscara de archivo de las ubicaciones de archivo incluidas en la plantilla de ubicación configuración.</span><span class="sxs-lookup"><span data-stu-id="98081-171">The **Files** tab lists the file path and file mask of the file locations included in the settings location template.</span></span> <span data-ttu-id="98081-172">Edite las ubicaciones de los archivos por uso del menú desplegable **tareas** .</span><span class="sxs-lookup"><span data-stu-id="98081-172">Edit the file locations by use of the **Tasks** drop-down menu.</span></span> <span data-ttu-id="98081-173">Las tareas para ubicaciones de archivos incluyen la adición de nuevos archivos o ubicaciones de carpetas, la edición del ámbito de archivos o carpetas existentes, la eliminación de archivos o carpetas y la apertura de la ubicación seleccionada en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="98081-173">Tasks for file locations include adding new files or folder locations, editing the scope of existing files or folders, deleting files or folders, and opening the selected location in Windows Explorer.</span></span> <span data-ttu-id="98081-174">Deje la máscara de archivo vacía para incluir todos los archivos en la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="98081-174">Leave the file mask empty to include all files in the specified folder.</span></span>

8.  <span data-ttu-id="98081-175">Haga clic en **crear** y guarde la plantilla de ubicación de configuración en el equipo.</span><span class="sxs-lookup"><span data-stu-id="98081-175">Click **Create** and save the settings location template on the computer.</span></span>

9.  <span data-ttu-id="98081-176">Haga clic en **cerrar** para cerrar el Asistente para plantillas de configuración.</span><span class="sxs-lookup"><span data-stu-id="98081-176">Click **Close** to close the Settings Template Wizard.</span></span> <span data-ttu-id="98081-177">Salga de la aplicación de generación de UE-V.</span><span class="sxs-lookup"><span data-stu-id="98081-177">Exit the UE-V Generator application.</span></span>

    <span data-ttu-id="98081-178">Una vez que haya creado la plantilla de ubicación de configuración para una aplicación, debe probar la plantilla.</span><span class="sxs-lookup"><span data-stu-id="98081-178">After you have created the settings location template for an application, you should test the template.</span></span> <span data-ttu-id="98081-179">Implemente la plantilla en un entorno de laboratorio antes de ponerlo en producción en la empresa.</span><span class="sxs-lookup"><span data-stu-id="98081-179">Deploy the template in a lab environment before putting it into production in the enterprise.</span></span>

## <span data-ttu-id="98081-180">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="98081-180">Related topics</span></span>


[<span data-ttu-id="98081-181">Trabajo con plantillas personalizadas de UE-V y el generador de UE-V</span><span class="sxs-lookup"><span data-stu-id="98081-181">Working with Custom UE-V Templates and the UE-V Generator</span></span>](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

[<span data-ttu-id="98081-182">Operaciones de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="98081-182">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





