---
title: Administrar aplicaciones virtuales de App-V 5.0 con la consola de administración
description: Administrar aplicaciones virtuales de App-V 5.0 con la consola de administración
author: dansimp
ms.assetid: e9280dbd-782b-493a-b495-daab25247795
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: 7a71f7c0fd82f8ef9d1efd5b978591b6838a648a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814870"
---
# <span data-ttu-id="b4889-103">Administrar aplicaciones virtuales de App-V 5.0 con la consola de administración</span><span class="sxs-lookup"><span data-stu-id="b4889-103">Administering App-V 5.0 Virtual Applications by Using the Management Console</span></span>


<span data-ttu-id="b4889-104">Use el servidor de administración de Microsoft Application Virtualization (App-V) 5,0 para administrar paquetes, grupos de conexión y acceso al paquete en su entorno.</span><span class="sxs-lookup"><span data-stu-id="b4889-104">Use the Microsoft Application Virtualization (App-V) 5.0 management server to manage packages, connection groups, and package access in your environment.</span></span> <span data-ttu-id="b4889-105">El servidor publica los iconos de la aplicación, los accesos directos y las asociaciones de tipos de archivo en los equipos autorizados que ejecutan el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b4889-105">The server publishes application icons, shortcuts, and file type associations to authorized computers that run the App-V 5.0 client.</span></span> <span data-ttu-id="b4889-106">Uno o varios servidores de administración suelen compartir un almacén de datos común para la información de configuración y del paquete.</span><span class="sxs-lookup"><span data-stu-id="b4889-106">One or more management servers typically share a common data store for configuration and package information.</span></span>

<span data-ttu-id="b4889-107">El servidor de administración usa grupos de servicios de dominio de Active Directory (AD DS) para administrar la autorización del usuario y tiene instalado SQL Server para administrar la base de datos y el almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="b4889-107">The management server uses Active Directory Domain Services (AD DS) groups to manage user authorization and has SQL Server installed to manage the database and data store.</span></span>

<span data-ttu-id="b4889-108">Debido a que los servidores de administración transmiten las aplicaciones a los usuarios finales a petición, estos servidores son ideales para las configuraciones del sistema que tienen LAN fiables de alto ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="b4889-108">Because the management servers stream applications to end users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span> <span data-ttu-id="b4889-109">El servidor de administración consta de los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="b4889-109">The management server consists of the following components:</span></span>

-   <span data-ttu-id="b4889-110">Servidor de administración: Use el servidor de administración para administrar paquetes y grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="b4889-110">Management Server – Use the management server to manage packages and connection groups.</span></span>

-   <span data-ttu-id="b4889-111">Publishing Server: Use el servidor de publicación para implementar paquetes en equipos que ejecuten el cliente de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b4889-111">Publishing Server – Use the publishing server to deploy packages to computers that run the App-V 5.0 client.</span></span>

-   <span data-ttu-id="b4889-112">Base de datos de administración: Use la base de datos de administración para administrar el acceso al paquete y para publicar la sincronización del servidor con el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="b4889-112">Management Database - Use the management database to manage the package access and to publish the server’s synchronization with the management server.</span></span>

## <span data-ttu-id="b4889-113">Tareas de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="b4889-113">Management Console tasks</span></span>


<span data-ttu-id="b4889-114">Las tareas más comunes que puede realizar con la consola de administración de App-V 5,0 son:</span><span class="sxs-lookup"><span data-stu-id="b4889-114">The most common tasks that you can perform with the App-V 5.0 Management console are:</span></span>

-   [<span data-ttu-id="b4889-115">Cómo conectarse a la consola de administración</span><span class="sxs-lookup"><span data-stu-id="b4889-115">How to Connect to the Management Console</span></span>](how-to-connect-to-the-management-console-beta.md)

-   [<span data-ttu-id="b4889-116">Cómo agregar o actualizar paquetes mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="b4889-116">How to Add or Upgrade Packages by Using the Management Console</span></span>](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)

-   [<span data-ttu-id="b4889-117">Cómo configurar el acceso a los paquetes mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="b4889-117">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

-   [<span data-ttu-id="b4889-118">Cómo publicar un paquete mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="b4889-118">How to Publish a Package by Using the Management Console</span></span>](how-to-publish-a-package-by-using-the-management-console-50.md)

-   [<span data-ttu-id="b4889-119">Cómo eliminar un paquete de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="b4889-119">How to Delete a Package in the Management Console</span></span>](how-to-delete-a-package-in-the-management-console-beta.md)

-   [<span data-ttu-id="b4889-120">Cómo agregar o quitar un administrador mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="b4889-120">How to Add or Remove an Administrator by Using the Management Console</span></span>](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)

-   [<span data-ttu-id="b4889-121">Cómo registrar y anular el registro de un servidor de publicación mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="b4889-121">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console.md)

-   [<span data-ttu-id="b4889-122">Cómo crear un archivo de configuración personalizado mediante el uso de la consola de administración de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b4889-122">How to Create a Custom Configuration File by Using the App-V 5.0 Management Console</span></span>](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)

-   [<span data-ttu-id="b4889-123">Cómo transferir configuraciones y acceso a otra versión de un paquete mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="b4889-123">How to Transfer Access and Configurations to Another Version of a Package by Using the Management Console</span></span>](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console.md)

-   [<span data-ttu-id="b4889-124">Cómo personalizar las extensiones de aplicaciones virtuales de un grupo AD específico mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="b4889-124">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console.md)

-   [<span data-ttu-id="b4889-125">Configurar aplicaciones y extensiones de aplicaciones virtuales predeterminadas en la consola de administración</span><span class="sxs-lookup"><span data-stu-id="b4889-125">Configure Applications and Default Virtual Application Extensions in Management Console</span></span>](configure-applications-and-default-virtual-application-extensions-in-management-console.md)

<span data-ttu-id="b4889-126">Los elementos principales de la consola de administración de App-V 5,0 son:</span><span class="sxs-lookup"><span data-stu-id="b4889-126">The main elements of the App-V 5.0 Management Console are:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b4889-127">Pestaña de consola de administración</span><span class="sxs-lookup"><span data-stu-id="b4889-127">Management Console tab</span></span></th>
<th align="left"><span data-ttu-id="b4889-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4889-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4889-129">Introducción</span><span class="sxs-lookup"><span data-stu-id="b4889-129">Overview</span></span></p></td>
<td align="left"><p></p>
<ul>
<li><p><strong><span data-ttu-id="b4889-130">Secuenciador de App-V </strong> - Seleccione esta opción para revisar la información general sobre el uso del secuenciador de 5,0 de App-v.</span><span class="sxs-lookup"><span data-stu-id="b4889-130">App-V Sequencer</strong> - Select this option to review general information about using the App-V 5.0 sequencer.</span></span></p></li>
<li><p><strong><span data-ttu-id="b4889-131">Biblioteca de paquetes </strong> de aplicaciones: Seleccione esta opción para abrir la <strong> </strong> Página paquetes de la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="b4889-131">Application Packages Library</strong> – Select this option to open the <strong>PACKAGES</strong> page of the Management Console.</span></span> <span data-ttu-id="b4889-132">Use esta página para revisar los paquetes que se han agregado al servidor.</span><span class="sxs-lookup"><span data-stu-id="b4889-132">Use this page to review packages that have been added to the server.</span></span> <span data-ttu-id="b4889-133">También puede administrar los grupos de conexión, así como agregar o actualizar paquetes.</span><span class="sxs-lookup"><span data-stu-id="b4889-133">You can also manage the connection groups, as well as add or upgrade packages.</span></span></p></li>
<li><p><strong><span data-ttu-id="b4889-134">SERVIDORES </strong> : Seleccione esta opción para abrir la <strong> </strong> Página servidores de la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="b4889-134">SERVERS</strong> – Select this option to open the <strong>SERVERS</strong> page of the Management Console.</span></span> <span data-ttu-id="b4889-135">Use esta página para revisar la lista de servidores que se han registrado con la infraestructura de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b4889-135">Use this page to review the list of servers that have been registered with your App-V 5.0 infrastructure.</span></span></p></li>
<li><p><strong><span data-ttu-id="b4889-136">CLIENTES </strong> : Seleccione esta opción para revisar la información general sobre los clientes de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b4889-136">CLIENTS</strong> – Select this option to review general information about App-V 5.0 clients.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4889-137">Ficha paquetes</span><span class="sxs-lookup"><span data-stu-id="b4889-137">Packages tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4889-138">Use la <strong> </strong> pestaña Paquetes para agregar o actualizar paquetes.</span><span class="sxs-lookup"><span data-stu-id="b4889-138">Use the <strong>PACKAGES</strong> tab to add or upgrade packages.</span></span> <span data-ttu-id="b4889-139">También puede administrar grupos de conexión haciendo clic en <strong> grupos de conexión </strong> .</span><span class="sxs-lookup"><span data-stu-id="b4889-139">You can also manage connection groups by clicking <strong>CONNECTION GROUPS</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b4889-140">Pestaña servidores</span><span class="sxs-lookup"><span data-stu-id="b4889-140">Servers tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4889-141">Use la <strong> </strong> pestaña servidores para registrar un nuevo servidor.</span><span class="sxs-lookup"><span data-stu-id="b4889-141">Use the <strong>SERVERS</strong> tab to register a new server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b4889-142">Ficha administradores</span><span class="sxs-lookup"><span data-stu-id="b4889-142">Administrators tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="b4889-143">Use la <strong> pestaña administradores </strong> para registrar, agregar o quitar administradores en el entorno de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="b4889-143">Use the <strong>ADMINISTRATORS</strong> tab to register, add, or remove administrators in your App-V 5.0 environment.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <a href="" id="other-resources-for-this-app-v-5-0-deployment-"></a><span data-ttu-id="b4889-144">Otros recursos para esta implementación de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="b4889-144">Other resources for this App-V 5.0 deployment</span></span>


-   [<span data-ttu-id="b4889-145">Guía del administrador de Microsoft Application Virtualization 5,0</span><span class="sxs-lookup"><span data-stu-id="b4889-145">Microsoft Application Virtualization 5.0 Administrator's Guide</span></span>](microsoft-application-virtualization-50-administrators-guide.md)

-   [<span data-ttu-id="b4889-146">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="b4889-146">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





