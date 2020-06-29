---
title: Acerca de la configuración dinámica de App-V 5.0
description: Acerca de la configuración dinámica de App-V 5.0
author: dansimp
ms.assetid: 88afaca1-68c5-45c4-a074-9371c56b5804
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0294a60570d6dea99193c8bd411639c4888ae6b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815031"
---
# <span data-ttu-id="b2868-103">Acerca de la configuración dinámica de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b2868-103">About App-V 5.0 Dynamic Configuration</span></span>


<span data-ttu-id="b2868-104">Puede usar la configuración dinámica para personalizar un paquete de App-V 5,0 para un usuario.</span><span class="sxs-lookup"><span data-stu-id="b2868-104">You can use the dynamic configuration to customize an App-V 5.0 package for a user.</span></span> <span data-ttu-id="b2868-105">Use la siguiente información para crear o editar un archivo de configuración dinámica existente.</span><span class="sxs-lookup"><span data-stu-id="b2868-105">Use the following information to create or edit an existing dynamic configuration file.</span></span>

<span data-ttu-id="b2868-106">Al editar el archivo de configuración dinámica, se personaliza cómo se ejecutará un paquete de App-V 5,0 para un usuario o un grupo.</span><span class="sxs-lookup"><span data-stu-id="b2868-106">When you edit the dynamic configuration file it customizes how an App-V 5.0 package will run for a user or group.</span></span> <span data-ttu-id="b2868-107">Esto ayuda a proporcionar un método más adecuado para la personalización de paquetes eliminando la necesidad de volver a ensecuenciar paquetes con la configuración deseada y proporciona una forma de mantener el contenido del paquete y la configuración personalizada de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="b2868-107">This helps to provide a more convenient method for package customization by removing the need to re-sequence packages using the desired settings, and provides a way to keep package content and custom settings independent.</span></span>

## <span data-ttu-id="b2868-108">Avanzada: configuración dinámica</span><span class="sxs-lookup"><span data-stu-id="b2868-108">Advanced: Dynamic Configuration</span></span>


<span data-ttu-id="b2868-109">Los paquetes de aplicaciones virtuales contienen un manifiesto que proporciona toda la información básica del paquete.</span><span class="sxs-lookup"><span data-stu-id="b2868-109">Virtual application packages contain a manifest that provides all the core information for the package.</span></span> <span data-ttu-id="b2868-110">Esta información incluye los valores predeterminados para la configuración del paquete y determina la configuración en el formato más básico (sin ninguna personalización adicional).</span><span class="sxs-lookup"><span data-stu-id="b2868-110">This information includes the defaults for the package settings and determines settings in the most basic form (with no additional customization).</span></span> <span data-ttu-id="b2868-111">Si desea ajustar estos valores predeterminados para un usuario o grupo en particular, puede crear y editar los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="b2868-111">If you want to adjust these defaults for a particular user or group, you can create and edit the following files:</span></span>

-   <span data-ttu-id="b2868-112">Archivo de configuración de usuario</span><span class="sxs-lookup"><span data-stu-id="b2868-112">User Configuration file</span></span>

-   <span data-ttu-id="b2868-113">Archivo de configuración de implementación</span><span class="sxs-lookup"><span data-stu-id="b2868-113">Deployment configuration file</span></span>

<span data-ttu-id="b2868-114">Los archivos. XML anteriores especifican la configuración de paquetes y permiten personalizar los paquetes sin afectar directamente a los paquetes.</span><span class="sxs-lookup"><span data-stu-id="b2868-114">The previous .xml files specify package settings and allow for packages to be customized without directly affecting the packages.</span></span> <span data-ttu-id="b2868-115">Cuando se crea un paquete, el secuenciador genera automáticamente los archivos de implementación y configuración de usuario. XML predeterminados con los datos del manifiesto del paquete.</span><span class="sxs-lookup"><span data-stu-id="b2868-115">When a package is created, the sequencer automatically generates default deployment and user configuration .xml files using the package manifest data.</span></span> <span data-ttu-id="b2868-116">Por lo tanto, estos archivos de configuración generados automáticamente simplemente reflejan los valores predeterminados del paquete de la manera en que se configuraron las cosas durante la secuenciación.</span><span class="sxs-lookup"><span data-stu-id="b2868-116">Therefore, these automatically generated configuration files simply reflect the default settings that the package innately as from how things were configured during sequencing.</span></span> <span data-ttu-id="b2868-117">Si aplica estos archivos de configuración a un paquete en el formulario generado por el secuenciador, los paquetes tendrán la misma configuración predeterminada que viene de su manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b2868-117">If you apply these configuration files to a package in the form generated by the sequencer, the packages will have the same default settings that came from their manifest.</span></span> <span data-ttu-id="b2868-118">Esto le proporciona una plantilla específica de paquete para empezar si se debe cambiar cualquiera de los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="b2868-118">This provides you with a package-specific template to get started if any of the defaults must be changed.</span></span>

<span data-ttu-id="b2868-119">**Nota:**  La siguiente información solo se puede usar para modificar los archivos de configuración generados por el secuenciador para personalizar paquetes con el fin de cumplir con requisitos específicos de grupo o usuario.</span><span class="sxs-lookup"><span data-stu-id="b2868-119">**Note** The following information can only be used to modify sequencer generated configuration files to customize packages to meet specific user or group requirements.</span></span>

 

### <span data-ttu-id="b2868-120">Contenido del archivo de configuración dinámica</span><span class="sxs-lookup"><span data-stu-id="b2868-120">Dynamic Configuration file contents</span></span>

<span data-ttu-id="b2868-121">Todas las adiciones, eliminaciones y actualizaciones de los archivos de configuración deben realizarse en relación con los valores predeterminados especificados por la información del manifiesto del paquete.</span><span class="sxs-lookup"><span data-stu-id="b2868-121">All of the additions, deletions, and updates in the configuration files need to be made in relation to the default values specified by the package's manifest information.</span></span> <span data-ttu-id="b2868-122">Revise la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="b2868-122">Review the following table:</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2868-123">Archivo Configuration. XML de usuario</span><span class="sxs-lookup"><span data-stu-id="b2868-123">User Configuration .xml file</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2868-124">Archivo Configuration. XML de implementación</span><span class="sxs-lookup"><span data-stu-id="b2868-124">Deployment Configuration .xml file</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2868-125">Manifiesto del paquete</span><span class="sxs-lookup"><span data-stu-id="b2868-125">Package Manifest</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="b2868-126">La tabla anterior representa cómo se leerán los archivos.</span><span class="sxs-lookup"><span data-stu-id="b2868-126">The previous table represents how the files will be read.</span></span> <span data-ttu-id="b2868-127">La primera entrada representa lo que se leerá en último lugar, por lo que su contenido tiene prioridad.</span><span class="sxs-lookup"><span data-stu-id="b2868-127">The first entry represents what will be read last, therefore, its content takes precedence.</span></span> <span data-ttu-id="b2868-128">Por lo tanto, todos los paquetes contienen de forma inherente la configuración predeterminada del manifiesto del paquete.</span><span class="sxs-lookup"><span data-stu-id="b2868-128">Therefore, all packages inherently contain and provide default settings from the package manifest.</span></span> <span data-ttu-id="b2868-129">Si se aplica un archivo Configuration. XML de implementación con una configuración personalizada, se anularán los valores predeterminados del manifiesto del paquete.</span><span class="sxs-lookup"><span data-stu-id="b2868-129">If a deployment configuration .xml file with customized settings is applied, it will override the package manifest defaults.</span></span> <span data-ttu-id="b2868-130">Si se aplica un archivo Configuration. XML de usuario con una configuración personalizada antes de ese, se reemplazará la configuración de implementación y los valores predeterminados del manifiesto del paquete.</span><span class="sxs-lookup"><span data-stu-id="b2868-130">If a user configuration .xml file with customized settings is applied prior to that, it will override both the deployment configuration and the package manifest defaults.</span></span>

<span data-ttu-id="b2868-131">En la siguiente lista se muestra más información sobre los dos tipos de archivo:</span><span class="sxs-lookup"><span data-stu-id="b2868-131">The following list displays more information about the two file types:</span></span>

-   <span data-ttu-id="b2868-132">**Archivo de configuración de usuario (UserConfig)** : permite especificar o modificar la configuración personalizada de un paquete.</span><span class="sxs-lookup"><span data-stu-id="b2868-132">**User Configuration File (UserConfig)** – Allows you to specify or modify custom settings for a package.</span></span> <span data-ttu-id="b2868-133">Esta configuración se aplicará a un usuario específico cuando el paquete se implemente en un equipo que ejecute el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b2868-133">These settings will be applied for a specific user when the package is deployed to a computer running the App-V 5.0 client.</span></span>

-   <span data-ttu-id="b2868-134">**Archivo de configuración de implementación (DeploymentConfig)** : permite especificar o modificar la configuración predeterminada de un paquete.</span><span class="sxs-lookup"><span data-stu-id="b2868-134">**Deployment Configuration File (DeploymentConfig)** – Allows you to specify or modify the default settings for a package.</span></span> <span data-ttu-id="b2868-135">Esta configuración se aplicará a todos los usuarios cuando se implemente un paquete en un equipo que ejecute el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b2868-135">These settings will be applied for all users when a package is deployed to a computer running the App-V 5.0 client.</span></span>

<span data-ttu-id="b2868-136">Para personalizar la configuración de un paquete para un conjunto específico de usuarios de un equipo o para realizar cambios que se aplicarán a ubicaciones de usuarios locales, como HKCU, debe usar el archivo UserConfig.</span><span class="sxs-lookup"><span data-stu-id="b2868-136">To customize the settings for a package for a specific set of users on a computer or to make changes that will be applied to local user locations such as HKCU, the UserConfig file should be used.</span></span> <span data-ttu-id="b2868-137">Para modificar la configuración predeterminada de un paquete para todos los usuarios de un equipo o para realizar cambios que se aplicarán a ubicaciones globales como HKEY \ _LOCAL \ _MACHINE y la carpeta todos los usuarios, se debe usar el archivo DeploymentConfig.</span><span class="sxs-lookup"><span data-stu-id="b2868-137">To modify the default settings of a package for all users on a machine or to make changes that will be applied to global locations such as HKEY\_LOCAL\_MACHINE and the all users folder, the DeploymentConfig file should be used.</span></span>

<span data-ttu-id="b2868-138">El archivo UserConfig proporciona opciones de configuración que se pueden aplicar a un solo usuario sin afectar a ningún otro usuario de un cliente:</span><span class="sxs-lookup"><span data-stu-id="b2868-138">The UserConfig file provides configuration settings that can be applied to a single user without affecting any other users on a client:</span></span>

-   <span data-ttu-id="b2868-139">Extensiones que se integrarán en el sistema nativo por usuario:-accesos directos, asociaciones de tipo de archivo, protocolos de URL, AppPaths, clientes de software y COM</span><span class="sxs-lookup"><span data-stu-id="b2868-139">Extensions that will be integrated into the native system per user:- shortcuts, File-Type associations, URL Protocols, AppPaths, Software Clients and COM</span></span>

-   <span data-ttu-id="b2868-140">Subsistemas virtuales:-objetos de aplicaciones, variables de entorno, modificaciones de registro, servicios y fuentes</span><span class="sxs-lookup"><span data-stu-id="b2868-140">Virtual Subsystems:- Application Objects, Environment variables, Registry modifications, Services and Fonts</span></span>

-   <span data-ttu-id="b2868-141">Scripts (solo contexto de usuario)</span><span class="sxs-lookup"><span data-stu-id="b2868-141">Scripts (User context only)</span></span>

-   <span data-ttu-id="b2868-142">Administración de la autoridad (para controlar la coexistencia del paquete con App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="b2868-142">Managing Authority (for controlling co-existence of package with App-V 4.6)</span></span>

<span data-ttu-id="b2868-143">El archivo DeploymentConfig proporciona opciones de configuración en dos secciones, una en relación con el contexto de equipo y una en relación con el contexto de usuario que proporciona las mismas funciones que aparecen en la lista anterior de UserConfig:</span><span class="sxs-lookup"><span data-stu-id="b2868-143">The DeploymentConfig file provides configuration settings in two sections, one relative to the machine context and one relative to the user context providing the same capabilities listed in the UserConfig list above:</span></span>

-   <span data-ttu-id="b2868-144">Toda la configuración de UserConfig arriba</span><span class="sxs-lookup"><span data-stu-id="b2868-144">All UserConfig settings above</span></span>

-   <span data-ttu-id="b2868-145">Extensiones que solo se pueden aplicar globalmente a todos los usuarios</span><span class="sxs-lookup"><span data-stu-id="b2868-145">Extensions that can only be applied globally for all users</span></span>

-   <span data-ttu-id="b2868-146">Subsistemas virtuales que se pueden configurar para las ubicaciones de la máquina internacional, por ejemplo, el registro</span><span class="sxs-lookup"><span data-stu-id="b2868-146">Virtual Subsystems that can be configured for global machine locations e.g. registry</span></span>

-   <span data-ttu-id="b2868-147">Dirección URL de origen del producto</span><span class="sxs-lookup"><span data-stu-id="b2868-147">Product Source URL</span></span>

-   <span data-ttu-id="b2868-148">Scripts (solo en el contexto de equipo)</span><span class="sxs-lookup"><span data-stu-id="b2868-148">Scripts (Machine context only)</span></span>

-   <span data-ttu-id="b2868-149">Controles para finalizar procesos secundarios</span><span class="sxs-lookup"><span data-stu-id="b2868-149">Controls to Terminate Child Processes</span></span>

### <span data-ttu-id="b2868-150">Estructura de archivos</span><span class="sxs-lookup"><span data-stu-id="b2868-150">File structure</span></span>

<span data-ttu-id="b2868-151">La estructura del archivo de configuración dinámica de App-V 5,0 se explica en la siguiente sección.</span><span class="sxs-lookup"><span data-stu-id="b2868-151">The structure of the App-V 5.0 Dynamic Configuration file is explained in the following section.</span></span>

### <span data-ttu-id="b2868-152">Archivo de configuración de usuario dinámico</span><span class="sxs-lookup"><span data-stu-id="b2868-152">Dynamic User Configuration file</span></span>

<span data-ttu-id="b2868-153">**Header** : el encabezado de un archivo de configuración de usuario dinámico es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="b2868-153">**Header** - the header of a dynamic user configuration file is as follows:</span></span>

<span data-ttu-id="b2868-154">&lt;? XML version = "1.0" Encoding = "UTF-8"? &gt; &lt; UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="b2868-154">&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

<span data-ttu-id="b2868-155">El **PackageId** es el mismo valor que existe en el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b2868-155">The **PackageId** is the same value as exists in the Manifest file.</span></span>

<span data-ttu-id="b2868-156">**Cuerpo** : el cuerpo del archivo de configuración de usuario dinámico puede incluir todos los puntos de extensión de aplicación que se definen en el archivo de manifiesto, así como información para configurar aplicaciones virtuales.</span><span class="sxs-lookup"><span data-stu-id="b2868-156">**Body** - the body of the Dynamic User Configuration file can include all the app extension points that are defined in the Manifest file, as well as information to configure virtual applications.</span></span> <span data-ttu-id="b2868-157">Hay cuatro subsecciones permitidas en el cuerpo:</span><span class="sxs-lookup"><span data-stu-id="b2868-157">There are four subsections allowed in the body:</span></span>

1. <span data-ttu-id="b2868-158">**Aplicaciones** : todas las extensiones de aplicación que se encuentran en el archivo de manifiesto de un paquete se asignan con un identificador de aplicación, que también se define en el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b2868-158">**Applications** - All app-extensions that are contained in the Manifest file within a package are assigned with an Application ID, which is also defined in the manifest file.</span></span> <span data-ttu-id="b2868-159">Esto le permite habilitar o deshabilitar todas las extensiones para una aplicación determinada dentro de un paquete.</span><span class="sxs-lookup"><span data-stu-id="b2868-159">This allows you to enable or disable all the extensions for a given application within a package.</span></span> <span data-ttu-id="b2868-160">El **identificador** de la aplicación debe existir en el archivo de manifiesto o se omitirá.</span><span class="sxs-lookup"><span data-stu-id="b2868-160">The **Application ID** must exist in the Manifest file or it will be ignored.</span></span>

   <span data-ttu-id="b2868-161">&lt;UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="b2868-161">&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

   <span data-ttu-id="b2868-162">&lt;Aplicaciones&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-162">&lt;Applications&gt;</span></span>

   <span data-ttu-id="b2868-163">&lt;!--No se puede definir ninguna aplicación nueva en la Directiva.</span><span class="sxs-lookup"><span data-stu-id="b2868-163">&lt;!-- No new application can be defined in policy.</span></span> <span data-ttu-id="b2868-164">El cliente de AppV ignorará cualquier identificador de aplicación que no esté incluido en el archivo de manifiesto:&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-164">AppV Client will ignore any application ID that is not also in the Manifest file --&gt;</span></span>

   <span data-ttu-id="b2868-165">&lt;Application ID = "{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled = "false"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-165">&lt;Application Id="{a56fa627-c35f-4a01-9e79-7d36aed8225a}" Enabled="false"&gt;</span></span>

   <span data-ttu-id="b2868-166">&lt;/Application&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-166">&lt;/Application&gt;</span></span>

   <span data-ttu-id="b2868-167">&lt;/Applications&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-167">&lt;/Applications&gt;</span></span>

   <span data-ttu-id="b2868-168">…</span><span class="sxs-lookup"><span data-stu-id="b2868-168">…</span></span>

   <span data-ttu-id="b2868-169">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-169">&lt;/UserConfiguration&gt;</span></span>

2. <span data-ttu-id="b2868-170">**Subsistemas** : AppExtensions y otros subsistemas se organizan como subnodos debajo de los &lt; subsistemas &gt; :</span><span class="sxs-lookup"><span data-stu-id="b2868-170">**Subsystems** - AppExtensions and other subsystems are arranged as subnodes under the &lt;Subsystems&gt;:</span></span>

   <span data-ttu-id="b2868-171">&lt;UserConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="b2868-171">&lt;UserConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/userconfiguration"&gt>;</span></span>

   <span data-ttu-id="b2868-172">&lt;Subsistemas&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-172">&lt;Subsystems&gt;</span></span>

   <span data-ttu-id="b2868-173">..</span><span class="sxs-lookup"><span data-stu-id="b2868-173">..</span></span>

   <span data-ttu-id="b2868-174">&lt;/Subsystems&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-174">&lt;/Subsystems&gt;</span></span>

   <span data-ttu-id="b2868-175">..</span><span class="sxs-lookup"><span data-stu-id="b2868-175">..</span></span>

   <span data-ttu-id="b2868-176">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-176">&lt;/UserConfiguration&gt;</span></span>

   <span data-ttu-id="b2868-177">Cada subsistema se puede habilitar o deshabilitar mediante el atributo "**habilitado**".</span><span class="sxs-lookup"><span data-stu-id="b2868-177">Each subsystem can be enabled/disabled using the “**Enabled**” attribute.</span></span> <span data-ttu-id="b2868-178">A continuación se muestran los diversos subsistemas y ejemplos de uso.</span><span class="sxs-lookup"><span data-stu-id="b2868-178">Below are the various subsystems and usage samples.</span></span>

   **<span data-ttu-id="b2868-179">Prórroga</span><span class="sxs-lookup"><span data-stu-id="b2868-179">Extensions:</span></span>**

   <span data-ttu-id="b2868-180">Algunos subsistemas (subsistemas de extensión) controlan las extensiones.</span><span class="sxs-lookup"><span data-stu-id="b2868-180">Some subsystems (Extension Subsystems) control Extensions.</span></span> <span data-ttu-id="b2868-181">Esos subsistemas son:-accesos directos, asociaciones de tipo de archivo, protocolos de URL, AppPaths, clientes de software y COM</span><span class="sxs-lookup"><span data-stu-id="b2868-181">Those subsystems are:- shortcuts, File-Type associations, URL Protocols, AppPaths, Software Clients and COM</span></span>

   <span data-ttu-id="b2868-182">Los subsistemas de extensión se pueden habilitar y deshabilitar independientemente del contenido.</span><span class="sxs-lookup"><span data-stu-id="b2868-182">Extension Subsystems can be enabled and disabled independently of the content.</span></span>  <span data-ttu-id="b2868-183">Por lo tanto, si los accesos directos están habilitados, el cliente usará los accesos directos incluidos en el manifiesto de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b2868-183">Thus if Shortcuts are enabled, The client will use the shortcuts contained within the manifest by default.</span></span> <span data-ttu-id="b2868-184">Cada subsistema de extensión puede contener &lt; un &gt; nodo de extensiones.</span><span class="sxs-lookup"><span data-stu-id="b2868-184">Each Extension Subsystem can contain an &lt;Extensions&gt; node.</span></span> <span data-ttu-id="b2868-185">Si este elemento secundario está presente, el cliente omitirá el contenido en el archivo de manifiesto de ese subsistema y solo usará el contenido del archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="b2868-185">If this child element is present, the client will ignore the content in the Manifest file for that subsystem and only use the content in the configuration file.</span></span>

   <span data-ttu-id="b2868-186">Ejemplo de uso del subsistema de accesos directos:</span><span class="sxs-lookup"><span data-stu-id="b2868-186">Example using the shortcuts subsystem:</span></span>

   1.  <span data-ttu-id="b2868-187">Si el usuario lo definió en el archivo de configuración dinámica o de implementación:</span><span class="sxs-lookup"><span data-stu-id="b2868-187">If the user defined this in either the dynamic or deployment config file:</span></span>

                                    **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions&gt;**

                                                 ...

                                                **&lt;/Extensions&gt;**

                                    **&lt;/Shortcuts&gt;**

                         Content in the manifest will be ignored.   

   2.  <span data-ttu-id="b2868-188">Si el usuario ha definido solo lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b2868-188">If the user defined only the following:</span></span>

                                   **&lt;Shortcuts  Enabled="true"/&gt;**

                         Then the content in the Manifest will be integrated during publishing.

   3.  <span data-ttu-id="b2868-189">Si el usuario define lo siguiente</span><span class="sxs-lookup"><span data-stu-id="b2868-189">If the user defines the following</span></span>

                                  **&lt;Shortcuts  Enabled="true"&gt;**

                                                **&lt;Extensions/&gt;**

                                    **&lt;/Shortcuts&gt;**

   <span data-ttu-id="b2868-190">A continuación, se ignorarán todos los métodos abreviados dentro del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b2868-190">Then all the shortcuts within the manifest will still be ignored.</span></span> <span data-ttu-id="b2868-191">No habrá ningún acceso directo integrado.</span><span class="sxs-lookup"><span data-stu-id="b2868-191">There will be no shortcuts integrated.</span></span>

   <span data-ttu-id="b2868-192">Los subsistemas de extensión admitidos son:</span><span class="sxs-lookup"><span data-stu-id="b2868-192">The supported Extension Subsystems are:</span></span>

   <span data-ttu-id="b2868-193">**Métodos abreviados:** Esto controla los accesos directos que se integrarán en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="b2868-193">**Shortcuts:** This controls shortcuts that will be integrated into the local system.</span></span> <span data-ttu-id="b2868-194">A continuación se muestra un ejemplo con 2 métodos abreviados:</span><span class="sxs-lookup"><span data-stu-id="b2868-194">Below is a sample with 2 shortcuts:</span></span>

   <span data-ttu-id="b2868-195">&lt;Subsistemas&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-195">&lt;Subsystems&gt;</span></span>

   <span data-ttu-id="b2868-196">&lt;Accesos directos habilitado = "verdadero"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-196">&lt;Shortcuts Enabled="true"&gt;</span></span>

     <span data-ttu-id="b2868-197">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-197">&lt;Extensions&gt;</span></span>

       &lt;Extension Category="AppV.Shortcut"&gt;

         &lt;Shortcut&gt;

           &lt;File&gt;\[{Common Programs}\]\\Microsoft Contoso\\Microsoft ContosoApp Filler 2010.lnk&lt;/File&gt;

           &lt;Target&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/Target&gt;

           &lt;Icon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\inficon.exe&lt;/Icon&gt;

           &lt;Arguments /&gt;

           &lt;WorkingDirectory /&gt;

           &lt;AppUserModelId&gt;ContosoApp.Filler.3&lt;/AppUserModelId&gt;

           &lt;Description&gt;Fill out dynamic forms to gather and reuse information throughout the organization using Microsoft ContosoApp.&lt;/Description&gt;

           &lt;Hotkey&gt;0&lt;/Hotkey&gt;

           &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

           &lt;ApplicationId&gt;\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE&lt;/ApplicationId&gt;

         &lt;/Shortcut&gt;

     <span data-ttu-id="b2868-198">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-198">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="b2868-199">&lt;Extension Category = "AppV. Shortcut"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-199">&lt;Extension Category="AppV.Shortcut"&gt;</span></span>

       &lt;Shortcut&gt;

         &lt;File&gt;\[{AppData}\]\\Microsoft\\Contoso\\Recent\\Templates.LNK&lt;/File&gt;

         &lt;Target&gt;\[{AppData}\]\\Microsoft\\Templates&lt;/Target&gt;

         &lt;Icon /&gt;

         &lt;Arguments /&gt;

         &lt;WorkingDirectory /&gt;

         &lt;AppUserModelId /&gt;

         &lt;Description /&gt;

         &lt;Hotkey&gt;0&lt;/Hotkey&gt;

         &lt;ShowCommand&gt;1&lt;/ShowCommand&gt;

         &lt;!-- Note the ApplicationId is optional --&gt;

       &lt;/Shortcut&gt;

     <span data-ttu-id="b2868-200">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-200">&lt;/Extension&gt;</span></span>

    <span data-ttu-id="b2868-201">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-201">&lt;/Extensions&gt;</span></span>

   <span data-ttu-id="b2868-202">&lt;/Shortcuts&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-202">&lt;/Shortcuts&gt;</span></span>

   <span data-ttu-id="b2868-203">**Asociaciones de tipo de archivo:** Asocia tipos de archivo con programas para abrir de forma predeterminada y configurar el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b2868-203">**File-Type Associations:** Associates File-types with programs to open by default as well as setup the context menu.</span></span> <span data-ttu-id="b2868-204">(Los tipos MIME también se pueden configurar con este susbsystem).</span><span class="sxs-lookup"><span data-stu-id="b2868-204">(MIME types can also be setup using this susbsystem).</span></span> <span data-ttu-id="b2868-205">La Asociación de tipo de archivo de ejemplo se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="b2868-205">Sample File-type Association is below:</span></span>

   <span data-ttu-id="b2868-206">&lt;FileTypeAssociations Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-206">&lt;FileTypeAssociations Enabled="true"&gt;</span></span>

   <span data-ttu-id="b2868-207">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-207">&lt;Extensions&gt;</span></span>

     <span data-ttu-id="b2868-208">&lt;Extension Category = "AppV. FileTypeAssociation"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-208">&lt;Extension Category="AppV.FileTypeAssociation"&gt;</span></span>

       &lt;FileTypeAssociation&gt;

         &lt;FileExtension MimeAssociation="true"&gt;

         &lt;Name&gt;.docm&lt;/Name&gt;

         &lt;ProgId&gt;contosowordpad.DocumentMacroEnabled.12&lt;/ProgId&gt;

         &lt;PerceivedType&gt;document&lt;/PerceivedType&gt;

         &lt;ContentType&gt;application/vnd.ms-contosowordpad.document.macroEnabled.12&lt;/ContentType&gt;

         &lt;OpenWithList&gt;

           &lt;ApplicationName&gt;wincontosowordpad.exe&lt;/ApplicationName&gt;

         &lt;/OpenWithList&gt;

        &lt;OpenWithProgIds&gt;

           &lt;ProgId&gt;contosowordpad.8&lt;/ProgId&gt;

         &lt;/OpenWithProgIds&gt;

         &lt;ShellNew&gt;

           &lt;Command /&gt;

           &lt;DataBinary /&gt;

           &lt;DataText /&gt;

           &lt;FileName /&gt;

           &lt;NullFile&gt;true&lt;/NullFile&gt;

           &lt;ItemName /&gt;

           &lt;IconPath /&gt;

           &lt;MenuText /&gt;

           &lt;Handler /&gt;

         &lt;/ShellNew&gt;

       &lt;/FileExtension&gt;

       &lt;ProgId&gt;

          &lt;Name&gt;contosowordpad.DocumentMacroEnabled.12&lt;/Name&gt;

           &lt;DefaultIcon&gt;\[{Windows}\]\\Installer\\{90140000-0011-0000-0000-0000000FF1CE}\\contosowordpadicon.exe,15&lt;/DefaultIcon&gt;

           &lt;Description&gt;Blah Blah Blah&lt;/Description&gt;

           &lt;FriendlyTypeName&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,9182&lt;/FriendlyTypeName&gt;

           &lt;InfoTip&gt;\[{FOLDERID\_ProgramFilesX86}\]\\Microsoft Contoso 14\\res.dll,1424&lt;/InfoTip&gt;

           &lt;EditFlags&gt;0&lt;/EditFlags&gt;

           &lt;ShellCommands&gt;

             &lt;DefaultCommand&gt;Open&lt;/DefaultCommand&gt;

             &lt;ShellCommand&gt;

                &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

                &lt;Name&gt;Edit&lt;/Name&gt;

                &lt;FriendlyName&gt;&Edit&lt;/FriendlyName&gt;

                &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /vu "%1"&lt;/CommandLine&gt;

             &lt;/ShellCommand&gt;

             &lt;/ShellCommand&gt;

               &lt;ApplicationId&gt;{e56fa627-c35f-4a01-9e79-7d36aed8225a}&lt;/ApplicationId&gt;

               &lt;Name&gt;Open&lt;/Name&gt;

               &lt;FriendlyName&gt;&Open&lt;/FriendlyName&gt;

               &lt;CommandLine&gt;"\[{PackageRoot}\]\\Contoso\\WINcontosowordpad.EXE" /n "%1"&lt;/CommandLine&gt;

               &lt;DropTargetClassId /&gt;

               &lt;DdeExec&gt;

                 &lt;Application&gt;mscontosowordpad&lt;/Application&gt;

                 &lt;Topic&gt;ShellSystem&lt;/Topic&gt;

                 &lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;

                 &lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;

               &lt;/DdeExec&gt;

             &lt;/ShellCommand&gt;

           &lt;/ShellCommands&gt;

         &lt;/ProgId&gt;

        &lt;/FileTypeAssociation&gt;

      <span data-ttu-id="b2868-209">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-209">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="b2868-210">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-210">&lt;/Extensions&gt;</span></span>

     <span data-ttu-id="b2868-211">&lt;/FileTypeAssociations&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-211">&lt;/FileTypeAssociations&gt;</span></span>

   <span data-ttu-id="b2868-212">**Protocolos URL**: Esto controla los protocolos de dirección URL que se integran en el registro local del equipo cliente; por ejemplo, "mailto:".</span><span class="sxs-lookup"><span data-stu-id="b2868-212">**URL Protocols**: This controls the URL Protocols that are integrated into the local registry of the client machine e.g. “mailto:”.</span></span>

   <span data-ttu-id="b2868-213">&lt;URLProtocols Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-213">&lt;URLProtocols Enabled="true"&gt;</span></span>

   <span data-ttu-id="b2868-214">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-214">&lt;Extensions&gt;</span></span>

   <span data-ttu-id="b2868-215">&lt;Extension Category = "AppV. URLProtocol"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-215">&lt;Extension Category="AppV.URLProtocol"&gt;</span></span>

   <span data-ttu-id="b2868-216">&lt;URLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-216">&lt;URLProtocol&gt;</span></span>

     <span data-ttu-id="b2868-217">&lt;Nombre &gt; mailto &lt;&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-217">&lt;Name&gt;mailto&lt;/Name&gt;</span></span>

     <span data-ttu-id="b2868-218">&lt;ApplicationURLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-218">&lt;ApplicationURLProtocol&gt;</span></span>

     <span data-ttu-id="b2868-219">&lt;DefaultIcon &gt; \ [{ProgramFilesX86} \] \\microsoft Contoso\\Contoso\\contosomail.EXE,-9403 &lt; /DefaultIcon&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-219">&lt;DefaultIcon&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE,-9403&lt;/DefaultIcon&gt;</span></span>

     <span data-ttu-id="b2868-220">&lt;EditFlags &gt; 2 &lt; /EditFlags&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-220">&lt;EditFlags&gt;2&lt;/EditFlags&gt;</span></span>

     <span data-ttu-id="b2868-221">&lt;Texto&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-221">&lt;Description /&gt;</span></span>

     <span data-ttu-id="b2868-222">&lt;AppUserModelId&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-222">&lt;AppUserModelId /&gt;</span></span>

     <span data-ttu-id="b2868-223">&lt;FriendlyTypeName /&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-223">&lt;FriendlyTypeName /&gt;</span></span>

     <span data-ttu-id="b2868-224">&lt;Sugerencia&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-224">&lt;InfoTip /&gt;</span></span>

   <span data-ttu-id="b2868-225">&lt;SourceFilter /&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-225">&lt;SourceFilter /&gt;</span></span>

     <span data-ttu-id="b2868-226">&lt;ShellFolder&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-226">&lt;ShellFolder /&gt;</span></span>

     <span data-ttu-id="b2868-227">&lt;WebNavigableCLSID /&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-227">&lt;WebNavigableCLSID /&gt;</span></span>

     <span data-ttu-id="b2868-228">&lt;ExplorerFlags &gt; 2 &lt; /ExplorerFlags&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-228">&lt;ExplorerFlags&gt;2&lt;/ExplorerFlags&gt;</span></span>

     <span data-ttu-id="b2868-229">&lt;Identificado&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-229">&lt;CLSID /&gt;</span></span>

     <span data-ttu-id="b2868-230">&lt;ShellCommands&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-230">&lt;ShellCommands&gt;</span></span>

     <span data-ttu-id="b2868-231">&lt;DefaultCommand &gt; abrir &lt; /DefaultCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-231">&lt;DefaultCommand&gt;open&lt;/DefaultCommand&gt;</span></span>

     <span data-ttu-id="b2868-232">&lt;ShellCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-232">&lt;ShellCommand&gt;</span></span>

     <span data-ttu-id="b2868-233">&lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationID&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-233">&lt;ApplicationId&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationId&gt;</span></span>

     <span data-ttu-id="b2868-234">&lt;Nombre &gt; abierto &lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-234">&lt;Name&gt;open&lt;/Name&gt;</span></span>

     <span data-ttu-id="b2868-235">&lt;CommandLine &gt; \ [{ProgramFilesX86} \\microsoft Contoso\\Contoso\\contosomail.EXE "-c OEP. Nota/m "%1" &lt; /commandLine&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-235">&lt;CommandLine&gt;\[{ProgramFilesX86}\\Microsoft Contoso\\Contoso\\contosomail.EXE" -c OEP.Note /m "%1"&lt;/CommandLine&gt;</span></span>

     <span data-ttu-id="b2868-236">&lt;DropTargetClassId /&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-236">&lt;DropTargetClassId /&gt;</span></span>

     <span data-ttu-id="b2868-237">&lt;Descriptivo&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-237">&lt;FriendlyName /&gt;</span></span>

     <span data-ttu-id="b2868-238">&lt;&gt;0 &lt; /Extended&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-238">&lt;Extended&gt;0&lt;/Extended&gt;</span></span>

     <span data-ttu-id="b2868-239">&lt;LegacyDisable &gt; 0 &lt; /LegacyDisable&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-239">&lt;LegacyDisable&gt;0&lt;/LegacyDisable&gt;</span></span>

     <span data-ttu-id="b2868-240">&lt;SuppressionPolicy &gt; 2 &lt; /SuppressionPolicy&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-240">&lt;SuppressionPolicy&gt;2&lt;/SuppressionPolicy&gt;</span></span>

      <span data-ttu-id="b2868-241">&lt;DdeExec&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-241">&lt;DdeExec&gt;</span></span>

     <span data-ttu-id="b2868-242">&lt;NoActivateHandler /&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-242">&lt;NoActivateHandler /&gt;</span></span>

     <span data-ttu-id="b2868-243">&lt;Application &gt; contosomail &lt; /Application&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-243">&lt;Application&gt;contosomail&lt;/Application&gt;</span></span>

     <span data-ttu-id="b2868-244">&lt;Tema &gt; ShellSystem &lt; /topic&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-244">&lt;Topic&gt;ShellSystem&lt;/Topic&gt;</span></span>

     <span data-ttu-id="b2868-245">&lt;IfExec &gt; \ [SHELLNOOP \] &lt; /IfExec&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-245">&lt;IfExec&gt;\[SHELLNOOP\]&lt;/IfExec&gt;</span></span>

     <span data-ttu-id="b2868-246">&lt;DdeCommand &gt; \ [SetForeground \] \ [ShellNewDatabase "%1" \] &lt; /DdeCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-246">&lt;DdeCommand&gt;\[SetForeground\]\[ShellNewDatabase "%1"\]&lt;/DdeCommand&gt;</span></span>

     <span data-ttu-id="b2868-247">&lt;/DdeExec&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-247">&lt;/DdeExec&gt;</span></span>

     <span data-ttu-id="b2868-248">&lt;/ShellCommand&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-248">&lt;/ShellCommand&gt;</span></span>

     <span data-ttu-id="b2868-249">&lt;/ShellCommands&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-249">&lt;/ShellCommands&gt;</span></span>

     <span data-ttu-id="b2868-250">&lt;/ApplicationURLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-250">&lt;/ApplicationURLProtocol&gt;</span></span>

     <span data-ttu-id="b2868-251">&lt;/URLProtocol&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-251">&lt;/URLProtocol&gt;</span></span>

     <span data-ttu-id="b2868-252">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-252">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="b2868-253">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-253">&lt;/Extension&gt;</span></span>

     <span data-ttu-id="b2868-254">&lt;/URLProtocols&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-254">&lt;/URLProtocols&gt;</span></span>

   <span data-ttu-id="b2868-255">**Clientes de software**: permite que la aplicación se registre como un cliente de correo electrónico, un lector de noticias, un reproductor multimedia y haga que la aplicación esté visible en la interfaz de usuario de configuración de acceso y programas predeterminados del equipo.</span><span class="sxs-lookup"><span data-stu-id="b2868-255">**Software Clients**: Allows the app to register as an Email client, news reader, media player and makes the app visible in the Set Program Access and Computer Defaults UI.</span></span> <span data-ttu-id="b2868-256">En la mayoría de los casos solo deberás habilitarlo y deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="b2868-256">In most cases you should only need to enable and disable it.</span></span> <span data-ttu-id="b2868-257">También hay un control para habilitar y deshabilitar el cliente de correo electrónico específicamente si desea que los otros clientes sigan habilitados, excepto el cliente.</span><span class="sxs-lookup"><span data-stu-id="b2868-257">There is also a control to enable and disable the email client specifically if you want the other clients still enabled except for that client.</span></span>

   <span data-ttu-id="b2868-258">&lt;SoftwareClients Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-258">&lt;SoftwareClients Enabled="true"&gt;</span></span>

     <span data-ttu-id="b2868-259">&lt;ClientConfiguration EmailEnabled = "falso"/&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-259">&lt;ClientConfiguration EmailEnabled="false" /&gt;</span></span>

   <span data-ttu-id="b2868-260">&lt;/SoftwareClients&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-260">&lt;/SoftwareClients&gt;</span></span>

   <span data-ttu-id="b2868-261">AppPaths:-Si una aplicación por ejemplo contoso.exe se registra con un nombre de AppPath "MyApp", le permite escribir "MyApp" en el menú ejecutar y se abrirá contoso.exe.</span><span class="sxs-lookup"><span data-stu-id="b2868-261">AppPaths:- If an application for example contoso.exe is registered with an apppath name of “myapp”, it allows you type “myapp” under the run menu and it will open contoso.exe.</span></span>

   <span data-ttu-id="b2868-262">&lt;AppPaths Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-262">&lt;AppPaths Enabled="true"&gt;</span></span>

   <span data-ttu-id="b2868-263">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-263">&lt;Extensions&gt;</span></span>

   <span data-ttu-id="b2868-264">&lt;Extension Category = "AppV. AppPath"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-264">&lt;Extension Category="AppV.AppPath"&gt;</span></span>

   <span data-ttu-id="b2868-265">&lt;AppPath&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-265">&lt;AppPath&gt;</span></span>

     <span data-ttu-id="b2868-266">&lt;ApplicationId &gt; \ [{ProgramFilesX86} \] \\microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationID&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-266">&lt;ApplicationId&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationId&gt;</span></span>

     <span data-ttu-id="b2868-267">&lt;Nombre &gt;contosomail.exe&lt; /Name&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-267">&lt;Name&gt;contosomail.exe&lt;/Name&gt;</span></span>

     <span data-ttu-id="b2868-268">&lt;ApplicationPath &gt; \ [{ProgramFilesX86} \] \\microsoft Contoso\\Contoso\\contosomail.EXE&lt; /ApplicationPath&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-268">&lt;ApplicationPath&gt;\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE&lt;/ApplicationPath&gt;</span></span>

     <span data-ttu-id="b2868-269">&lt;PATHEnvironmentVariablePrefix /&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-269">&lt;PATHEnvironmentVariablePrefix /&gt;</span></span>

     <span data-ttu-id="b2868-270">&lt;CanAcceptUrl &gt; falso &lt; /CanAcceptUrl&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-270">&lt;CanAcceptUrl&gt;false&lt;/CanAcceptUrl&gt;</span></span>

     <span data-ttu-id="b2868-271">&lt;SaveUrl /&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-271">&lt;SaveUrl /&gt;</span></span>

   <span data-ttu-id="b2868-272">&lt;/AppPath&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-272">&lt;/AppPath&gt;</span></span>

   <span data-ttu-id="b2868-273">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-273">&lt;/Extension&gt;</span></span>

   <span data-ttu-id="b2868-274">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-274">&lt;/Extensions&gt;</span></span>

   <span data-ttu-id="b2868-275">&lt;/AppPaths&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-275">&lt;/AppPaths&gt;</span></span>

   <span data-ttu-id="b2868-276">**Com**: permite a una aplicación registrar servidores com locales.</span><span class="sxs-lookup"><span data-stu-id="b2868-276">**COM**: Allows an Application register Local COM servers.</span></span> <span data-ttu-id="b2868-277">El modo puede ser integración, aislado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="b2868-277">Mode can be Integration, Isolated or Off.</span></span> <span data-ttu-id="b2868-278">Cuando ISOL.</span><span class="sxs-lookup"><span data-stu-id="b2868-278">When Isol.</span></span>

   <span data-ttu-id="b2868-279">&lt;Modo COM = "aislado"/&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-279">&lt;COM Mode="Isolated"/&gt;</span></span>

   <span data-ttu-id="b2868-280">**Otras opciones de configuración**:</span><span class="sxs-lookup"><span data-stu-id="b2868-280">**Other Settings**:</span></span>

   <span data-ttu-id="b2868-281">Además de las extensiones, se pueden habilitar/deshabilitar otros subsistemas y editarlos:</span><span class="sxs-lookup"><span data-stu-id="b2868-281">In addition to Extensions, other subsystems can be enabled/disabled and edited:</span></span>

   <span data-ttu-id="b2868-282">**Objetos de núcleo virtual**:</span><span class="sxs-lookup"><span data-stu-id="b2868-282">**Virtual Kernel Objects**:</span></span>

   <span data-ttu-id="b2868-283">&lt;Objects Enabled = "false"/&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-283">&lt;Objects Enabled="false" /&gt;</span></span>

   <span data-ttu-id="b2868-284">**Registro virtual**: se usa si desea establecer un registro en el registro virtual dentro de HKCU</span><span class="sxs-lookup"><span data-stu-id="b2868-284">**Virtual Registry**: Used if you want to set a registry in the Virtual Registry within HKCU</span></span>

   <span data-ttu-id="b2868-285">&lt;Registro habilitado = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-285">&lt;Registry Enabled="true"&gt;</span></span>

   <span data-ttu-id="b2868-286">&lt;Incluir&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-286">&lt;Include&gt;</span></span>

   <span data-ttu-id="b2868-287">&lt;Ruta de la clave = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\ABC"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-287">&lt;Key Path="\\REGISTRY\\USER\\\[{AppVCurrentUserSID}\]\\Software\\ABC"&gt;</span></span>

   <span data-ttu-id="b2868-288">&lt;Value Type = "REG \ _SZ" Name = "bar" Data = "Nuevovalor"/&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-288">&lt;Value Type="REG\_SZ" Name="Bar" Data="NewValue" /&gt;</span></span>

    <span data-ttu-id="b2868-289">&lt;/Key&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-289">&lt;/Key&gt;</span></span>

     <span data-ttu-id="b2868-290">&lt;Ruta de la clave = "\\REGISTRY\\USER\\\ [{AppVCurrentUserSID} \] \\Software\\EmptyKey"/&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-290">&lt;Key Path="\\REGISTRY\\USER\\\[{AppVCurrentUserSID}\]\\Software\\EmptyKey" /&gt;</span></span>

    <span data-ttu-id="b2868-291">&lt;/Include&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-291">&lt;/Include&gt;</span></span>

   <span data-ttu-id="b2868-292">&lt;Borrar&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-292">&lt;Delete&gt;</span></span>

     <span data-ttu-id="b2868-293">&lt;/Registry&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-293">&lt;/Registry&gt;</span></span>

   **<span data-ttu-id="b2868-294">Sistema de archivos virtual</span><span class="sxs-lookup"><span data-stu-id="b2868-294">Virtual File System</span></span>**

         &lt;FileSystem Enabled="true" /&gt;

   **<span data-ttu-id="b2868-295">Fuentes virtuales</span><span class="sxs-lookup"><span data-stu-id="b2868-295">Virtual Fonts</span></span>**

         &lt;Fonts Enabled="false" /&gt;

   **<span data-ttu-id="b2868-296">Variables de entorno virtual</span><span class="sxs-lookup"><span data-stu-id="b2868-296">Virtual Environment Variables</span></span>**

   <span data-ttu-id="b2868-297">&lt;EnvironmentVariables Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-297">&lt;EnvironmentVariables Enabled="true"&gt;</span></span>

   <span data-ttu-id="b2868-298">&lt;Incluir&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-298">&lt;Include&gt;</span></span>

          &lt;Variable Name="UserPath" Value="%path%;%UserProfile%" /&gt;

          &lt;Variable Name="UserLib" Value="%UserProfile%\\ABC" /&gt;

          &lt;/Include&gt;

         &lt;Delete&gt;

          &lt;Variable Name="lib" /&gt;

           &lt;/Delete&gt;

           &lt;/EnvironmentVariables&gt;

   **<span data-ttu-id="b2868-299">Servicios virtuales</span><span class="sxs-lookup"><span data-stu-id="b2868-299">Virtual services</span></span>**

         &lt;Services Enabled="false" /&gt;

3. <span data-ttu-id="b2868-300">**Userscripts** : los scripts se pueden usar para configurar o modificar el entorno virtual, así como para ejecutar scripts en el momento de la implementación o desinstalación, antes de que se ejecute una aplicación o se pueden usar para "limpiar" el entorno después de que la aplicación finalice.</span><span class="sxs-lookup"><span data-stu-id="b2868-300">**UserScripts** – Scripts can be used to setup or alter the virtual environment as well as execute scripts at time of deployment or removal, before an application executes, or they can be used to “clean up” the environment after the application terminates.</span></span> <span data-ttu-id="b2868-301">Para ver un script de ejemplo, haga referencia a un archivo de configuración de usuario de ejemplo generado por el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="b2868-301">Please reference a sample User configuration file that is output by the sequencer to see a sample script.</span></span> <span data-ttu-id="b2868-302">La sección de scripts que se muestra a continuación proporciona más información sobre los diversos desencadenadores que se pueden usar.</span><span class="sxs-lookup"><span data-stu-id="b2868-302">The Scripts section below provides more information on the various triggers that can be used.</span></span>

4. <span data-ttu-id="b2868-303">**ManagingAuthority** : se puede usar cuando dos versiones de su paquete están coexistentes en la misma máquina, una implementada en App-v 4,6 y la otra implementada en App-v 5,0.</span><span class="sxs-lookup"><span data-stu-id="b2868-303">**ManagingAuthority** – Can be used when 2 versions of your package are co-existing on the same machine, one deployed to App-V 4.6 and the other deployed on App-V 5.0.</span></span> <span data-ttu-id="b2868-304">Para permitir que App-V vNext tome el control de App-V 4,6 puntos de extensión para el paquete nombrado, escriba lo siguiente en el archivo UserConfig (donde PackageName es el GUID del paquete en App-V 4,6:</span><span class="sxs-lookup"><span data-stu-id="b2868-304">To Allow App-V vNext to take over App-V 4.6 extension points for the named package enter the following in the UserConfig file (where PackageName is the Package GUID in App-V 4.6:</span></span>

   <span data-ttu-id="b2868-305">&lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = "032630c0-b8e2-417c-Acef-76fc5297fe81"/&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-305">&lt;ManagingAuthority TakeoverExtensionPointsFrom46="true" PackageName="032630c0-b8e2-417c-acef-76fc5297fe81" /&gt;</span></span>

### <span data-ttu-id="b2868-306">Archivo de configuración de implementación dinámica</span><span class="sxs-lookup"><span data-stu-id="b2868-306">Dynamic Deployment Configuration file</span></span>

<span data-ttu-id="b2868-307">**Header** : el encabezado de un archivo de configuración de implementación es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="b2868-307">**Header** - The header of a Deployment Configuration file is as follows:</span></span>

<span data-ttu-id="b2868-308">&lt;? XML version = "1.0" Encoding = "UTF-8"? &gt; &lt; DeploymentConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="b2868-308">&lt;?xml version="1.0" encoding="utf-8"?&gt;&lt;DeploymentConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt>;</span></span>

<span data-ttu-id="b2868-309">El **PackageId** es el mismo valor que existe en el archivo de manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b2868-309">The **PackageId** is the same value as exists in the manifest file.</span></span>

<span data-ttu-id="b2868-310">**Cuerpo** : el cuerpo del archivo de configuración de implementación incluye dos secciones:</span><span class="sxs-lookup"><span data-stu-id="b2868-310">**Body** - The body of the deployment configuration file includes two sections:</span></span>

-   <span data-ttu-id="b2868-311">Sección de configuración de usuario: permite el mismo contenido que el archivo de configuración de usuario descrito en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="b2868-311">User Configuration section –allows the same content as the User Configuration file described in the previous section.</span></span> <span data-ttu-id="b2868-312">Cuando el paquete se publique para un usuario, cualquier valor de configuración de appextensions en esta sección reemplazará la configuración correspondiente en el manifiesto dentro del paquete, a menos que se proporcione también un archivo de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="b2868-312">When the package is published to a user, any appextensions configuration settings in this section will override corresponding settings in the Manifest within the package unless a user configuration file is also provided.</span></span> <span data-ttu-id="b2868-313">Si también se proporciona un archivo UserConfig, se usará en lugar de la configuración de usuario en el archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="b2868-313">If a UserConfig file is also provided, it will be used instead of the User settings in the deployment configuration file.</span></span> <span data-ttu-id="b2868-314">Si el paquete se publica globalmente, solo se utilizará el contenido del archivo de configuración de implementación en combinación con el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="b2868-314">If the package is published globally, then only the contents of the deployment configuration file will be used in combination with the manifest.</span></span>

-   <span data-ttu-id="b2868-315">Sección de configuración de la máquina: contiene información que se puede configurar solo para un equipo completo, no para un usuario específico en el equipo.</span><span class="sxs-lookup"><span data-stu-id="b2868-315">Machine Configuration section–contains information that can be configured only for an entire machine, not for a specific user on the machine.</span></span> <span data-ttu-id="b2868-316">Por ejemplo, HKEY \ _LOCAL \ _MACHINE claves de registro en el VFS.</span><span class="sxs-lookup"><span data-stu-id="b2868-316">For example, HKEY\_LOCAL\_MACHINE registry keys in the VFS.</span></span>

<span data-ttu-id="b2868-317">&lt;DeploymentConfiguration **PackageId**= "1F8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName = "Reserved" xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt> ;</span><span class="sxs-lookup"><span data-stu-id="b2868-317">&lt;DeploymentConfiguration **PackageId**="1f8488bf-2257-46b4-b27f-09c9dbaae707" DisplayName="Reserved" xmlns="<https://schemas.microsoft.com/appv/2010/deploymentconfiguration"&gt>;</span></span>

<span data-ttu-id="b2868-318">&lt;UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-318">&lt;UserConfiguration&gt;</span></span>

  <span data-ttu-id="b2868-319">..</span><span class="sxs-lookup"><span data-stu-id="b2868-319">..</span></span>

<span data-ttu-id="b2868-320">&lt;/UserConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-320">&lt;/UserConfiguration&gt;</span></span>

<span data-ttu-id="b2868-321">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-321">&lt;MachineConfiguration&gt;</span></span>

<span data-ttu-id="b2868-322">..</span><span class="sxs-lookup"><span data-stu-id="b2868-322">..</span></span>

<span data-ttu-id="b2868-323">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-323">&lt;/MachineConfiguration&gt;</span></span>

<span data-ttu-id="b2868-324">..</span><span class="sxs-lookup"><span data-stu-id="b2868-324">..</span></span>

<span data-ttu-id="b2868-325">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-325">&lt;/MachineConfiguration&gt;</span></span>

<span data-ttu-id="b2868-326">&lt;/DeploymentConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-326">&lt;/DeploymentConfiguration&gt;</span></span>

<span data-ttu-id="b2868-327">**Configuración de usuario** : Use la sección anterior del **archivo de configuración de usuario dinámico** para obtener información sobre la configuración que se proporciona en la sección configuración de usuario del archivo de configuración de implementación.</span><span class="sxs-lookup"><span data-stu-id="b2868-327">**User Configuration** - use the previous **Dynamic User Configuration file** section for information on settings that are provided in the user configuration section of the Deployment Configuration file.</span></span>

<span data-ttu-id="b2868-328">Configuración de la máquina: la sección de configuración del equipo del archivo de configuración de implementación se usa para configurar información que solo se puede establecer para un equipo completo, no para un usuario específico en el equipo.</span><span class="sxs-lookup"><span data-stu-id="b2868-328">Machine Configuration - the Machine configuration section of the Deployment Configuration File is used to configure information that can be set only for an entire machine, not for a specific user on the computer.</span></span> <span data-ttu-id="b2868-329">Por ejemplo, HKEY \ _LOCAL \ _MACHINE claves de registro en el registro virtual.</span><span class="sxs-lookup"><span data-stu-id="b2868-329">For example, HKEY\_LOCAL\_MACHINE registry keys in the Virtual Registry.</span></span> <span data-ttu-id="b2868-330">Hay cuatro subsecciones permitidas en este elemento</span><span class="sxs-lookup"><span data-stu-id="b2868-330">There are four subsections allowed in under this element</span></span>

1.  <span data-ttu-id="b2868-331">**Subsistemas** : AppExtensions y otros subsistemas se organizan como subnodos en &lt; subsistemas &gt; :</span><span class="sxs-lookup"><span data-stu-id="b2868-331">**Subsystems** - AppExtensions and other subsystems are arranged as subnodes under &lt;Subsystems&gt;:</span></span>

    <span data-ttu-id="b2868-332">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-332">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="b2868-333">&lt;Subsistemas&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-333">&lt;Subsystems&gt;</span></span>

      <span data-ttu-id="b2868-334">..</span><span class="sxs-lookup"><span data-stu-id="b2868-334">..</span></span>

      <span data-ttu-id="b2868-335">&lt;/Subsystems&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-335">&lt;/Subsystems&gt;</span></span>

    <span data-ttu-id="b2868-336">..</span><span class="sxs-lookup"><span data-stu-id="b2868-336">..</span></span>

    <span data-ttu-id="b2868-337">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-337">&lt;/MachineConfiguration&gt;</span></span>

    <span data-ttu-id="b2868-338">En la siguiente sección se muestran los diversos subsistemas y ejemplos de uso.</span><span class="sxs-lookup"><span data-stu-id="b2868-338">The following section displays the various subsystems and usage samples.</span></span>

    <span data-ttu-id="b2868-339">**Extensiones**:</span><span class="sxs-lookup"><span data-stu-id="b2868-339">**Extensions**:</span></span>

    <span data-ttu-id="b2868-340">Algunos subsistemas (subsistemas de extensión) controlan las extensiones que solo se pueden aplicar a todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="b2868-340">Some subsystems (Extension Subsystems) control Extensions which can only apply to all users.</span></span> <span data-ttu-id="b2868-341">El subsistema es una función de aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2868-341">The subsystem is application capabilities.</span></span> <span data-ttu-id="b2868-342">Como esto solo se puede aplicar a todos los usuarios, el paquete debe publicarse globalmente para que este tipo de extensión se integre en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="b2868-342">Because this can only apply to all users, the package must be published globally in order for this type of extension to be integrated into the local system.</span></span> <span data-ttu-id="b2868-343">Las mismas reglas para los controles y la configuración que se aplican a las extensiones de la configuración de usuario también se aplican a las de la sección MachineConfiguration.</span><span class="sxs-lookup"><span data-stu-id="b2868-343">The same rules for controls and settings that apply to the Extensions in the User Configuration also apply to those in the MachineConfiguration section.</span></span>

    <span data-ttu-id="b2868-344">**Capacidades**de la aplicación: usadas por programas predeterminados en la interfaz del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="b2868-344">**Application Capabilities**: Used by default programs in windows operating system Interface.</span></span> <span data-ttu-id="b2868-345">Permite que una aplicación se registre como capaz de abrir determinadas extensiones de archivo, como un caso de la ranura del explorador de Internet del menú Inicio, como capaz de abrir determinados tipos MIME de Windows.</span><span class="sxs-lookup"><span data-stu-id="b2868-345">Allows an application to register itself as capable of opening certain file extensions, as a contender for the start menu internet browser slot, as capable of opening certain windows MIME types.</span></span><span data-ttu-id="b2868-346">Esta extensión también hace que la aplicación virtual esté visible en la interfaz de usuario de programas predeterminados.</span><span class="sxs-lookup"><span data-stu-id="b2868-346"> This extension also makes the virtual application visible in the Set Default Programs UI.:</span></span>

    <span data-ttu-id="b2868-347">&lt;ApplicationCapabilities Enabled = "true"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-347">&lt;ApplicationCapabilities Enabled="true"&gt;</span></span>

      <span data-ttu-id="b2868-348">&lt;Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-348">&lt;Extensions&gt;</span></span>

       <span data-ttu-id="b2868-349">&lt;Extension Category = "AppV. ApplicationCapabilities"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-349">&lt;Extension Category="AppV.ApplicationCapabilities"&gt;</span></span>

        &lt;ApplicationCapabilities&gt;

         &lt;ApplicationId&gt;\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe&lt;/ApplicationId&gt;

         &lt;Reference&gt;

          &lt;Name&gt;LitView Browser&lt;/Name&gt;

          &lt;Path&gt;SOFTWARE\\LitView\\Browser\\Capabilities&lt;/Path&gt;

         &lt;/Reference&gt;

       <span data-ttu-id="b2868-350">&lt;CapabilityGroup&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-350">&lt;CapabilityGroup&gt;</span></span>

        &lt;Capabilities&gt;

         &lt;Name&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12345&lt;/Name&gt;

         &lt;Description&gt;@\[{ProgramFilesX86}\]\\LitView\\LitViewBrowser.exe,-12346&lt;/Description&gt;

         &lt;Hidden&gt;0&lt;/Hidden&gt;

         &lt;EMailSoftwareClient&gt;Lit View E-Mail Client&lt;/EMailSoftwareClient&gt;

         &lt;FileAssociationList&gt;

          &lt;FileAssociation Extension=".htm" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".html" ProgID="LitViewHTML" /&gt;

          &lt;FileAssociation Extension=".shtml" ProgID="LitViewHTML" /&gt;

         &lt;/FileAssociationList&gt;

         &lt;MIMEAssociationList&gt;

          &lt;MIMEAssociation Type="audio/mp3" ProgID="LitViewHTML" /&gt;

          &lt;MIMEAssociation Type="audio/mpeg" ProgID="LitViewHTML" /&gt;

         &lt;/MIMEAssociationList&gt;

        &lt;URLAssociationList&gt;

          &lt;URLAssociation Scheme="http" ProgID="LitViewHTML.URL.http" /&gt;

         &lt;/URLAssociationList&gt;

         &lt;/Capabilities&gt;

      <span data-ttu-id="b2868-351">&lt;/CapabilityGroup&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-351">&lt;/CapabilityGroup&gt;</span></span>

       <span data-ttu-id="b2868-352">&lt;/ApplicationCapabilities&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-352">&lt;/ApplicationCapabilities&gt;</span></span>

      <span data-ttu-id="b2868-353">&lt;/Extension&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-353">&lt;/Extension&gt;</span></span>

    <span data-ttu-id="b2868-354">&lt;/Extensions&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-354">&lt;/Extensions&gt;</span></span>

    <span data-ttu-id="b2868-355">&lt;/ApplicationCapabilities&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-355">&lt;/ApplicationCapabilities&gt;</span></span>

    <span data-ttu-id="b2868-356">**Otras opciones de configuración**:</span><span class="sxs-lookup"><span data-stu-id="b2868-356">**Other Settings**:</span></span>

    <span data-ttu-id="b2868-357">Además de las extensiones, se pueden editar otros subsistemas:</span><span class="sxs-lookup"><span data-stu-id="b2868-357">In addition to Extensions, other subsystems can be edited:</span></span>

    <span data-ttu-id="b2868-358">**Registro virtual en todo el equipo**: se usa cuando desea establecer una clave del registro en el registro virtual en HKEY \ _Local \ _Machine</span><span class="sxs-lookup"><span data-stu-id="b2868-358">**Machine Wide Virtual Registry**: Used when you want to set a registry key in the virtual registry within HKEY\_Local\_Machine</span></span>

    <span data-ttu-id="b2868-359">&lt;Registro&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-359">&lt;Registry&gt;</span></span>

    <span data-ttu-id="b2868-360">&lt;Incluir&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-360">&lt;Include&gt;</span></span>

      <span data-ttu-id="b2868-361">&lt;Ruta de la clave = "\\REGISTRY\\Machine\\Software\\ABC"&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-361">&lt;Key Path="\\REGISTRY\\Machine\\Software\\ABC"&gt;</span></span>

        &lt;Value Type="REG\_SZ" Name="Bar" Data="Baz" /&gt;

       <span data-ttu-id="b2868-362">&lt;/Key&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-362">&lt;/Key&gt;</span></span>

      <span data-ttu-id="b2868-363">&lt;Ruta de la clave = "\\REGISTRY\\Machine\\Software\\EmptyKey"/&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-363">&lt;Key Path="\\REGISTRY\\Machine\\Software\\EmptyKey" /&gt;</span></span>

     <span data-ttu-id="b2868-364">&lt;/Include&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-364">&lt;/Include&gt;</span></span>

    <span data-ttu-id="b2868-365">&lt;Borrar&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-365">&lt;Delete&gt;</span></span>

    <span data-ttu-id="b2868-366">&lt;/Registry&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-366">&lt;/Registry&gt;</span></span>

    **<span data-ttu-id="b2868-367">Objetos de núcleo virtual de todo el equipo</span><span class="sxs-lookup"><span data-stu-id="b2868-367">Machine Wide Virtual Kernel Objects</span></span>**

    <span data-ttu-id="b2868-368">&lt;Objeto&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-368">&lt;Objects&gt;</span></span>

    <span data-ttu-id="b2868-369">&lt;NotIsolate&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-369">&lt;NotIsolate&gt;</span></span>

       <span data-ttu-id="b2868-370">&lt;Object name = "testObject"/&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-370">&lt;Object Name="testObject" /&gt;</span></span>

     <span data-ttu-id="b2868-371">&lt;/NotIsolate&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-371">&lt;/NotIsolate&gt;</span></span>

    <span data-ttu-id="b2868-372">&lt;/Objects&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-372">&lt;/Objects&gt;</span></span>

2.  <span data-ttu-id="b2868-373">**ProductSourceURLOptOut**: indica si la dirección URL del paquete se puede modificar globalmente a través de PackageSourceRoot (para admitir escenarios de sucursales).</span><span class="sxs-lookup"><span data-stu-id="b2868-373">**ProductSourceURLOptOut**: Indicates whether the URL for the package can be modified globally through PackageSourceRoot (to support branch office scenarios).</span></span> <span data-ttu-id="b2868-374">El valor predeterminado es falso y el cambio de configuración surte efecto en el próximo inicio.</span><span class="sxs-lookup"><span data-stu-id="b2868-374">Default is false and the setting change takes effect on the next launch.</span></span>  

    <span data-ttu-id="b2868-375">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-375">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="b2868-376">..</span><span class="sxs-lookup"><span data-stu-id="b2868-376">..</span></span> 

      <span data-ttu-id="b2868-377">&lt;ProductSourceURLOptOut Enabled = "true"/&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-377">&lt;ProductSourceURLOptOut Enabled="true" /&gt;</span></span>

      <span data-ttu-id="b2868-378">..</span><span class="sxs-lookup"><span data-stu-id="b2868-378">..</span></span>

    <span data-ttu-id="b2868-379">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-379">&lt;/MachineConfiguration&gt;</span></span>

3.  <span data-ttu-id="b2868-380">**MachineScripts** : el paquete se puede configurar para que ejecute los scripts en el momento de la implementación, publicación o desinstalación.</span><span class="sxs-lookup"><span data-stu-id="b2868-380">**MachineScripts** – Package can be configured to execute scripts at time of deployment, publishing or removal.</span></span> <span data-ttu-id="b2868-381">Para ver un script de ejemplo, haga referencia a un archivo de configuración de implementación generado por el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="b2868-381">Please reference a sample deployment configuration file that is generated by the sequencer to see a sample script.</span></span> <span data-ttu-id="b2868-382">La sección de scripts que se muestra a continuación proporciona más información sobre los diversos desencadenadores que se pueden usar</span><span class="sxs-lookup"><span data-stu-id="b2868-382">The Scripts section below provides more information on the various triggers that can be used</span></span>

4.  <span data-ttu-id="b2868-383">**TerminateChildProcess**:-se puede especificar un ejecutable de aplicación, cuyos procesos secundarios finalizarán cuando se termine el proceso exe de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b2868-383">**TerminateChildProcess**:- An application executable can be specified, whose child processes will be terminated when the application exe process is terminated.</span></span>

    <span data-ttu-id="b2868-384">&lt;MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-384">&lt;MachineConfiguration&gt;</span></span>

      <span data-ttu-id="b2868-385">..</span><span class="sxs-lookup"><span data-stu-id="b2868-385">..</span></span>   

      <span data-ttu-id="b2868-386">&lt;TerminateChildProcesses&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-386">&lt;TerminateChildProcesses&gt;</span></span>

        &lt;Application Path="\[{PackageRoot}\]\\Contoso\\ContosoApp.EXE" /&gt;

        &lt;Application Path="\[{PackageRoot}\]\\LitView\\LitViewBrowser.exe" /&gt;

        &lt;Application Path="\[{ProgramFilesX86}\]\\Microsoft Contoso\\Contoso\\contosomail.EXE" /&gt;

      <span data-ttu-id="b2868-387">&lt;/TerminateChildProcesses&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-387">&lt;/TerminateChildProcesses&gt;</span></span>

      <span data-ttu-id="b2868-388">..</span><span class="sxs-lookup"><span data-stu-id="b2868-388">..</span></span>

    <span data-ttu-id="b2868-389">&lt;/MachineConfiguration&gt;</span><span class="sxs-lookup"><span data-stu-id="b2868-389">&lt;/MachineConfiguration&gt;</span></span>

### <span data-ttu-id="b2868-390">Scripts</span><span class="sxs-lookup"><span data-stu-id="b2868-390">Scripts</span></span>

<span data-ttu-id="b2868-391">En la tabla siguiente se describen los diversos eventos de script y el contexto en el que se pueden ejecutar.</span><span class="sxs-lookup"><span data-stu-id="b2868-391">The following table describes the various script events and the context under which they can be run.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b2868-392">Tiempo de ejecución de script</span><span class="sxs-lookup"><span data-stu-id="b2868-392">Script Execution Time</span></span></th>
<th align="left"><span data-ttu-id="b2868-393">Puede especificarse en la configuración de implementación</span><span class="sxs-lookup"><span data-stu-id="b2868-393">Can be specified in Deployment Configuration</span></span></th>
<th align="left"><span data-ttu-id="b2868-394">Se puede especificar en configuración de usuario</span><span class="sxs-lookup"><span data-stu-id="b2868-394">Can be specified in User Configuration</span></span></th>
<th align="left"><span data-ttu-id="b2868-395">Puede ejecutarse en el entorno virtual del paquete</span><span class="sxs-lookup"><span data-stu-id="b2868-395">Can run in the Virtual Environment of the package</span></span></th>
<th align="left"><span data-ttu-id="b2868-396">Puede ejecutarse en el contexto de una aplicación específica</span><span class="sxs-lookup"><span data-stu-id="b2868-396">Can be run in the context of a specific application</span></span></th>
<th align="left"><span data-ttu-id="b2868-397">Se ejecuta en el contexto sistema o usuario: (configuración de implementación, configuración de usuario)</span><span class="sxs-lookup"><span data-stu-id="b2868-397">Runs in system/user context: (Deployment Configuration, User Configuration)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2868-398">AddPackage</span><span class="sxs-lookup"><span data-stu-id="b2868-398">AddPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-399">X</span><span class="sxs-lookup"><span data-stu-id="b2868-399">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b2868-400">(SISTEMA, N/A)</span><span class="sxs-lookup"><span data-stu-id="b2868-400">(SYSTEM, N/A)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2868-401">PublishPackage</span><span class="sxs-lookup"><span data-stu-id="b2868-401">PublishPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-402">X</span><span class="sxs-lookup"><span data-stu-id="b2868-402">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-403">X</span><span class="sxs-lookup"><span data-stu-id="b2868-403">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b2868-404">(Sistema, usuario)</span><span class="sxs-lookup"><span data-stu-id="b2868-404">(SYSTEM, User)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2868-405">UnpublishPackage</span><span class="sxs-lookup"><span data-stu-id="b2868-405">UnpublishPackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-406">X</span><span class="sxs-lookup"><span data-stu-id="b2868-406">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-407">X</span><span class="sxs-lookup"><span data-stu-id="b2868-407">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b2868-408">(Sistema, usuario)</span><span class="sxs-lookup"><span data-stu-id="b2868-408">(SYSTEM, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2868-409">RemovePackage</span><span class="sxs-lookup"><span data-stu-id="b2868-409">RemovePackage</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-410">X</span><span class="sxs-lookup"><span data-stu-id="b2868-410">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b2868-411">(SISTEMA, N/A)</span><span class="sxs-lookup"><span data-stu-id="b2868-411">(SYSTEM, N/A)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2868-412">StartProcess</span><span class="sxs-lookup"><span data-stu-id="b2868-412">StartProcess</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-413">X</span><span class="sxs-lookup"><span data-stu-id="b2868-413">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-414">X</span><span class="sxs-lookup"><span data-stu-id="b2868-414">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-415">X</span><span class="sxs-lookup"><span data-stu-id="b2868-415">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-416">X</span><span class="sxs-lookup"><span data-stu-id="b2868-416">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-417">(Usuario, usuario)</span><span class="sxs-lookup"><span data-stu-id="b2868-417">(User, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2868-418">ExitProcess</span><span class="sxs-lookup"><span data-stu-id="b2868-418">ExitProcess</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-419">X</span><span class="sxs-lookup"><span data-stu-id="b2868-419">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-420">X</span><span class="sxs-lookup"><span data-stu-id="b2868-420">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b2868-421">X</span><span class="sxs-lookup"><span data-stu-id="b2868-421">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-422">(Usuario, usuario)</span><span class="sxs-lookup"><span data-stu-id="b2868-422">(User, User)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b2868-423">StartVirtualEnvironment</span><span class="sxs-lookup"><span data-stu-id="b2868-423">StartVirtualEnvironment</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-424">X</span><span class="sxs-lookup"><span data-stu-id="b2868-424">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-425">X</span><span class="sxs-lookup"><span data-stu-id="b2868-425">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-426">X</span><span class="sxs-lookup"><span data-stu-id="b2868-426">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b2868-427">(Usuario, usuario)</span><span class="sxs-lookup"><span data-stu-id="b2868-427">(User, User)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b2868-428">TerminateVirtualEnvironment</span><span class="sxs-lookup"><span data-stu-id="b2868-428">TerminateVirtualEnvironment</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-429">X</span><span class="sxs-lookup"><span data-stu-id="b2868-429">X</span></span></p></td>
<td align="left"><p><span data-ttu-id="b2868-430">X</span><span class="sxs-lookup"><span data-stu-id="b2868-430">X</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="b2868-431">(Usuario, usuario)</span><span class="sxs-lookup"><span data-stu-id="b2868-431">(User, User)</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="b2868-432">Crear un archivo de configuración dinámica con un archivo de manifiesto de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="b2868-432">Create a Dynamic Configuration file using an App-V 5.0 Manifest file</span></span>

<span data-ttu-id="b2868-433">Puede crear el archivo de configuración dinámica con uno de estos tres métodos: manualmente, usando la consola de administración de App-V 5,0 o secuenciando un paquete, que se generará con dos archivos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b2868-433">You can create the Dynamic Configuration file using one of three methods: either manually, using the App-V 5.0 Management Console or sequencing a package, which will be generated with 2 sample files.</span></span>

<span data-ttu-id="b2868-434">Para obtener más información sobre cómo crear el archivo con la consola de administración de App-V 5,0, consulte [Cómo crear un archivo de configuración personalizado con la consola de administración de App-v 5,0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).</span><span class="sxs-lookup"><span data-stu-id="b2868-434">For more information about how to create the file using the App-V 5.0 Management Console see, [How to Create a Custom Configuration File by Using the App-V 5.0 Management Console](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).</span></span>

<span data-ttu-id="b2868-435">Para crear el archivo manualmente, la información anterior de las secciones anteriores se puede combinar en un solo archivo.</span><span class="sxs-lookup"><span data-stu-id="b2868-435">To create the file manually, the information above in previous sections can be combined into a single file.</span></span> <span data-ttu-id="b2868-436">Le recomendamos que use los archivos generados por el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="b2868-436">We recommend you use files generated by the sequencer.</span></span>






## <span data-ttu-id="b2868-437">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2868-437">Related topics</span></span>


[<span data-ttu-id="b2868-438">Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="b2868-438">How to Apply the Deployment Configuration File by Using PowerShell</span></span>](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

[<span data-ttu-id="b2868-439">Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="b2868-439">How to Apply the User Configuration File by Using PowerShell</span></span>](how-to-apply-the-user-configuration-file-by-using-powershell.md)

[<span data-ttu-id="b2868-440">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b2868-440">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





