---
title: Administrar aplicaciones virtuales de App-V 5.1 con la consola de administración
description: Administrar aplicaciones virtuales de App-V 5.1 con la consola de administración
author: dansimp
ms.assetid: a4d078aa-ec54-4fa4-9463-bfb3b971d724
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63ec965519bedef08b09c961dc5d1c90e1d8d694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814863"
---
# <span data-ttu-id="34499-103">Administrar aplicaciones virtuales de App-V 5.1 con la consola de administración</span><span class="sxs-lookup"><span data-stu-id="34499-103">Administering App-V 5.1 Virtual Applications by Using the Management Console</span></span>


<span data-ttu-id="34499-104">Use el servidor de administración de Microsoft Application Virtualization (App-V) 5,1 para administrar paquetes, grupos de conexión y acceso al paquete en su entorno.</span><span class="sxs-lookup"><span data-stu-id="34499-104">Use the Microsoft Application Virtualization (App-V) 5.1 management server to manage packages, connection groups, and package access in your environment.</span></span> <span data-ttu-id="34499-105">El servidor publica los iconos de la aplicación, los accesos directos y las asociaciones de tipos de archivo en los equipos autorizados que ejecutan el cliente de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="34499-105">The server publishes application icons, shortcuts, and file type associations to authorized computers that run the App-V 5.1 client.</span></span> <span data-ttu-id="34499-106">Uno o varios servidores de administración suelen compartir un almacén de datos común para la información de configuración y del paquete.</span><span class="sxs-lookup"><span data-stu-id="34499-106">One or more management servers typically share a common data store for configuration and package information.</span></span>

<span data-ttu-id="34499-107">El servidor de administración usa grupos de servicios de dominio de Active Directory (AD DS) para administrar la autorización del usuario y tiene instalado SQL Server para administrar la base de datos y el almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="34499-107">The management server uses Active Directory Domain Services (AD DS) groups to manage user authorization and has SQL Server installed to manage the database and data store.</span></span>

<span data-ttu-id="34499-108">Debido a que los servidores de administración transmiten las aplicaciones a los usuarios finales a petición, estos servidores son ideales para las configuraciones del sistema que tienen LAN fiables de alto ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="34499-108">Because the management servers stream applications to end users on demand, these servers are ideally suited for system configurations that have reliable, high-bandwidth LANs.</span></span> <span data-ttu-id="34499-109">El servidor de administración consta de los siguientes componentes:</span><span class="sxs-lookup"><span data-stu-id="34499-109">The management server consists of the following components:</span></span>

-   <span data-ttu-id="34499-110">Servidor de administración: Use el servidor de administración para administrar paquetes y grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="34499-110">Management Server – Use the management server to manage packages and connection groups.</span></span>

-   <span data-ttu-id="34499-111">Publishing Server: Use el servidor de publicación para implementar paquetes en equipos que ejecuten el cliente de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="34499-111">Publishing Server – Use the publishing server to deploy packages to computers that run the App-V 5.1 client.</span></span>

-   <span data-ttu-id="34499-112">Base de datos de administración: Use la base de datos de administración para administrar el acceso al paquete y para publicar la sincronización del servidor con el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="34499-112">Management Database - Use the management database to manage the package access and to publish the server’s synchronization with the management server.</span></span>

## <span data-ttu-id="34499-113">Tareas de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="34499-113">Management Console tasks</span></span>


<span data-ttu-id="34499-114">Las tareas más comunes que puede realizar con la consola de administración de App-V 5,1 son:</span><span class="sxs-lookup"><span data-stu-id="34499-114">The most common tasks that you can perform with the App-V 5.1 Management console are:</span></span>

-   [<span data-ttu-id="34499-115">Cómo conectarse a la consola de administración</span><span class="sxs-lookup"><span data-stu-id="34499-115">How to Connect to the Management Console</span></span>](how-to-connect-to-the-management-console-51.md)

-   [<span data-ttu-id="34499-116">Cómo agregar o actualizar paquetes mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="34499-116">How to Add or Upgrade Packages by Using the Management Console</span></span>](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [<span data-ttu-id="34499-117">Cómo configurar el acceso a los paquetes mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="34499-117">How to Configure Access to Packages by Using the Management Console</span></span>](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [<span data-ttu-id="34499-118">Cómo publicar un paquete mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="34499-118">How to Publish a Package by Using the Management Console</span></span>](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [<span data-ttu-id="34499-119">Cómo eliminar un paquete de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="34499-119">How to Delete a Package in the Management Console</span></span>](how-to-delete-a-package-in-the-management-console-51.md)

-   [<span data-ttu-id="34499-120">Cómo agregar o quitar un administrador mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="34499-120">How to Add or Remove an Administrator by Using the Management Console</span></span>](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [<span data-ttu-id="34499-121">Cómo registrar y anular el registro de un servidor de publicación mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="34499-121">How to Register and Unregister a Publishing Server by Using the Management Console</span></span>](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [<span data-ttu-id="34499-122">Cómo crear un archivo de configuración personalizado mediante el uso de la consola de administración de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="34499-122">How to Create a Custom Configuration File by Using the App-V 5.1 Management Console</span></span>](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [<span data-ttu-id="34499-123">Cómo transferir configuraciones y acceso a otra versión de un paquete mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="34499-123">How to Transfer Access and Configurations to Another Version of a Package by Using the Management Console</span></span>](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [<span data-ttu-id="34499-124">Cómo personalizar las extensiones de aplicaciones virtuales de un grupo AD específico mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="34499-124">How to Customize Virtual Applications Extensions for a Specific AD Group by Using the Management Console</span></span>](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [<span data-ttu-id="34499-125">Cómo ver y configurar aplicaciones y extensiones de la aplicación virtual predeterminada mediante el uso de la consola de administración</span><span class="sxs-lookup"><span data-stu-id="34499-125">How to View and Configure Applications and Default Virtual Application Extensions by Using the Management Console</span></span>](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

<span data-ttu-id="34499-126">Los elementos principales de la consola de administración de App-V 5,1 son:</span><span class="sxs-lookup"><span data-stu-id="34499-126">The main elements of the App-V 5.1 Management Console are:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="34499-127">Pestaña de consola de administración</span><span class="sxs-lookup"><span data-stu-id="34499-127">Management Console tab</span></span></th>
<th align="left"><span data-ttu-id="34499-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="34499-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="34499-129">Ficha paquetes</span><span class="sxs-lookup"><span data-stu-id="34499-129">Packages tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="34499-130">Use la <strong> </strong> pestaña Paquetes para agregar o actualizar paquetes.</span><span class="sxs-lookup"><span data-stu-id="34499-130">Use the <strong>PACKAGES</strong> tab to add or upgrade packages.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="34499-131">Ficha grupos de conexión</span><span class="sxs-lookup"><span data-stu-id="34499-131">Connection Groups tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="34499-132">Use la <strong> pestaña grupos </strong> de conexión para administrar grupos de conexión.</span><span class="sxs-lookup"><span data-stu-id="34499-132">Use the <strong>CONNECTION GROUPS</strong> tab to manage connection groups.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="34499-133">Pestaña servidores</span><span class="sxs-lookup"><span data-stu-id="34499-133">Servers tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="34499-134">Use la <strong> </strong> pestaña servidores para registrar un nuevo servidor.</span><span class="sxs-lookup"><span data-stu-id="34499-134">Use the <strong>SERVERS</strong> tab to register a new server.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="34499-135">Ficha administradores</span><span class="sxs-lookup"><span data-stu-id="34499-135">Administrators tab</span></span></p></td>
<td align="left"><p><span data-ttu-id="34499-136">Use la <strong> pestaña administradores </strong> para registrar, agregar o quitar administradores en el entorno de App-V 5,1.</span><span class="sxs-lookup"><span data-stu-id="34499-136">Use the <strong>ADMINISTRATORS</strong> tab to register, add, or remove administrators in your App-V 5.1 environment.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="34499-137">**Importante**  JavaScript debe estar habilitado en el explorador que abre la consola de administración web.</span><span class="sxs-lookup"><span data-stu-id="34499-137">**Important** JavaScript must be enabled on the browser that opens the Web Management Console.</span></span>

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a><span data-ttu-id="34499-138">Otros recursos para esta implementación de App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="34499-138">Other resources for this App-V 5.1 deployment</span></span>


-   [<span data-ttu-id="34499-139">Guía del administrador de Microsoft Application Virtualization 5,1</span><span class="sxs-lookup"><span data-stu-id="34499-139">Microsoft Application Virtualization 5.1 Administrator's Guide</span></span>](microsoft-application-virtualization-51-administrators-guide.md)

-   [<span data-ttu-id="34499-140">Operaciones de App-V 5.1</span><span class="sxs-lookup"><span data-stu-id="34499-140">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





