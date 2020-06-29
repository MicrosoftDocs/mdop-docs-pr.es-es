---
title: Implementación de la ubicación de almacenamiento de configuración de UE-V 1.0
description: Implementación de la ubicación de almacenamiento de configuración de UE-V 1.0
author: dansimp
ms.assetid: b187d44d-649b-487e-98d3-a61ee2be8c2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c179be0882bc6a0efc0f11f21fc231f03b63b0fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826640"
---
# <span data-ttu-id="2a570-103">Implementación de la ubicación de almacenamiento de configuración de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2a570-103">Deploying the Settings Storage Location for UE-V 1.0</span></span>


<span data-ttu-id="2a570-104">La implementación de la virtualización de la experiencia del usuario de Microsoft (UE-V) requiere una ubicación de almacenamiento de configuración donde se almacena la configuración de usuario en un archivo de paquete de configuración.</span><span class="sxs-lookup"><span data-stu-id="2a570-104">Microsoft User Experience Virtualization (UE-V) deployment requires a settings storage location where the user settings are stored in a settings package file.</span></span> <span data-ttu-id="2a570-105">La ubicación de almacenamiento de configuración se puede configurar de una de las siguientes dos maneras:</span><span class="sxs-lookup"><span data-stu-id="2a570-105">The settings storage location can be configured in one of the following two ways:</span></span>

-   <span data-ttu-id="2a570-106">**Directorio principal de Active** Directory: si se define un directorio particular para el usuario en Active Directory, UE-V Agent usará esta ubicación para almacenar los paquetes de ubicación de configuración.</span><span class="sxs-lookup"><span data-stu-id="2a570-106">**Active Directory home directory** – if a home directory is defined for the user in Active Directory, the UE-V agent will use this location to store settings location packages.</span></span> <span data-ttu-id="2a570-107">UE-V Agent crea dinámicamente la carpeta de almacenamiento específica del usuario que se encuentra debajo de la raíz del directorio de inicio.</span><span class="sxs-lookup"><span data-stu-id="2a570-107">The UE-V agent dynamically creates the user-specific storage folder below the root of the home directory.</span></span> <span data-ttu-id="2a570-108">El agente solo usa el directorio de inicio de Active Directory si no se ha definido una ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="2a570-108">The agent only uses the home directory of the Active Directory if a settings storage location is not defined.</span></span>

-   <span data-ttu-id="2a570-109">**Crear un recurso compartido de almacenamiento de configuración** : el recurso de almacenamiento de configuración es un recurso compartido de red estándar accesible para los usuarios de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2a570-109">**Create a settings storage share** – the settings storage share is a standard network share that is accessible by UE-V users.</span></span>

## <span data-ttu-id="2a570-110">Implementar un recurso de almacenamiento de configuración de UE-V</span><span class="sxs-lookup"><span data-stu-id="2a570-110">Deploy a UE-V settings storage share</span></span>


<span data-ttu-id="2a570-111">Al crear el recurso compartido de almacenamiento de configuración, debe limitar el acceso a los usuarios que lo necesiten.</span><span class="sxs-lookup"><span data-stu-id="2a570-111">When you create the settings storage share, you should limit access only to users that need access.</span></span> <span data-ttu-id="2a570-112">Los permisos necesarios se muestran en las tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="2a570-112">The necessary permissions are shown in the tables below.</span></span>

**<span data-ttu-id="2a570-113">Para implementar el recurso compartido de red UE-V</span><span class="sxs-lookup"><span data-stu-id="2a570-113">To deploy the UE-V network share</span></span>**

1.  <span data-ttu-id="2a570-114">Cree un nuevo grupo de seguridad para usuarios de UE-V.</span><span class="sxs-lookup"><span data-stu-id="2a570-114">Create a new security group for UE-V users.</span></span>

2.  <span data-ttu-id="2a570-115">Cree una nueva carpeta en el equipo centralizado que almacenará los paquetes de configuración de UE-V y, a continuación, conceda a los usuarios de UE-V con permisos de grupo a la carpeta.</span><span class="sxs-lookup"><span data-stu-id="2a570-115">Create a new folder on the centrally located computer that will store the UE-V settings packages, and then grant the UE-V users with group permissions to the folder.</span></span> <span data-ttu-id="2a570-116">El administrador que admita UE-V necesitará permisos para esta carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="2a570-116">The administrator supporting UE-V will need permissions to this shared folder.</span></span>

3.  <span data-ttu-id="2a570-117">Establezca los siguientes permisos de nivel de uso compartido (SMB) para la carpeta de ubicación de almacenamiento de configuración:</span><span class="sxs-lookup"><span data-stu-id="2a570-117">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="2a570-118">Cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="2a570-118">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="2a570-119">Permisos recomendados</span><span class="sxs-lookup"><span data-stu-id="2a570-119">Recommended permissions</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2a570-120">Todos</span><span class="sxs-lookup"><span data-stu-id="2a570-120">Everyone</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2a570-121">No hay permisos</span><span class="sxs-lookup"><span data-stu-id="2a570-121">No Permissions</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2a570-122">Grupo de seguridad de los usuarios de UE-V</span><span class="sxs-lookup"><span data-stu-id="2a570-122">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2a570-123">Control total</span><span class="sxs-lookup"><span data-stu-id="2a570-123">Full Control</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

4.  <span data-ttu-id="2a570-124">Configure los siguientes permisos NTFS para la carpeta de ubicación de almacenamiento de configuración:</span><span class="sxs-lookup"><span data-stu-id="2a570-124">Set the following NTFS permissions for the settings storage location folder:</span></span>

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="2a570-125">Cuenta de usuario</span><span class="sxs-lookup"><span data-stu-id="2a570-125">User account</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="2a570-126">Permisos recomendados</span><span class="sxs-lookup"><span data-stu-id="2a570-126">Recommended permissions</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="2a570-127">Carpeta</span><span class="sxs-lookup"><span data-stu-id="2a570-127">Folder</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="2a570-128">Creador/propietario</span><span class="sxs-lookup"><span data-stu-id="2a570-128">Creator/Owner</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2a570-129">Control total</span><span class="sxs-lookup"><span data-stu-id="2a570-129">Full Control</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2a570-130">Solo subcarpetas y archivos</span><span class="sxs-lookup"><span data-stu-id="2a570-130">Subfolders and Files Only</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="2a570-131">Grupo de seguridad de los usuarios de UE-V</span><span class="sxs-lookup"><span data-stu-id="2a570-131">Security group of UE-V users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2a570-132">Listar carpeta/leer datos, crear carpetas/anexar datos</span><span class="sxs-lookup"><span data-stu-id="2a570-132">List Folder/Read Data, Create Folders/Append Data</span></span></p></td>
    <td align="left"><p><span data-ttu-id="2a570-133">Solo esta carpeta</span><span class="sxs-lookup"><span data-stu-id="2a570-133">This Folder Only</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

5.  <span data-ttu-id="2a570-134">Haga clic en **Aceptar** para cerrar los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2a570-134">Click **OK** to close the dialog boxes.</span></span>

<span data-ttu-id="2a570-135">Esta configuración de permisos permite a los usuarios crear carpetas para el almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="2a570-135">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="2a570-136">El agente UE-V crea y protege una `settingspackage` carpeta mientras se ejecuta en el contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="2a570-136">The UE-V agent creates and secures a `settingspackage` folder while running in the context of the user.</span></span> <span data-ttu-id="2a570-137">El usuario recibe el control total de su `settingspackage` carpeta.</span><span class="sxs-lookup"><span data-stu-id="2a570-137">The user receives full control to their `settingspackage` folder.</span></span> <span data-ttu-id="2a570-138">Otros usuarios no heredan el acceso a esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="2a570-138">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="2a570-139">No es necesario crear ni proteger directorios de usuario individuales, ya que el agente que se ejecuta en el contexto del usuario lo hará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2a570-139">You do not need to create and secure individual user directories, because this will be done automatically by the agent that runs in the context of the user.</span></span>

<span data-ttu-id="2a570-140">**Nota:**  Se puede configurar la seguridad adicional cuando se usa un servidor de Windows para el recurso de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="2a570-140">**Note** Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="2a570-141">UE-V se puede configurar para comprobar que el grupo de administradores local o el usuario actual es el propietario de la carpeta donde se almacenan los paquetes de configuración.</span><span class="sxs-lookup"><span data-stu-id="2a570-141">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="2a570-142">Para habilitar la seguridad adicional, siga este procedimiento:</span><span class="sxs-lookup"><span data-stu-id="2a570-142">To enable additional security complete the following:</span></span>

1.  <span data-ttu-id="2a570-143">Agregue una clave del registro **reg \ _DWORD** denominada "RepositoryOwnerCheckEnabled" a **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration.**</span><span class="sxs-lookup"><span data-stu-id="2a570-143">Add a **REG\_DWORD** registry key named "RepositoryOwnerCheckEnabled" to **HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\UEV\\Agent\\Configuration.**</span></span>

2.  <span data-ttu-id="2a570-144">Establezca el valor de la clave del registro en 1.</span><span class="sxs-lookup"><span data-stu-id="2a570-144">Set registry key value to 1.</span></span>

 

## <span data-ttu-id="2a570-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a570-145">Related topics</span></span>


[<span data-ttu-id="2a570-146">Implementación de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2a570-146">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

[<span data-ttu-id="2a570-147">Configuraciones admitidas para UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="2a570-147">Supported Configurations for UE-V 1.0</span></span>](supported-configurations-for-ue-v-10.md)

<span data-ttu-id="2a570-148">Implementar el almacenamiento central de configuración de virtualización de la experiencia de usuario paquetes de configuración y plantillas [instalar el generador de UE-V](installing-the-ue-v-generator.md)</span><span class="sxs-lookup"><span data-stu-id="2a570-148">Deploy the Central Storage for User Experience Virtualization Settings Templates and Settings Packages [Installing the UE-V Generator](installing-the-ue-v-generator.md)</span></span>

[<span data-ttu-id="2a570-149">Implementación del agente de UE-V</span><span class="sxs-lookup"><span data-stu-id="2a570-149">Deploying the UE-V Agent</span></span>](deploying-the-ue-v-agent.md)

 

 





