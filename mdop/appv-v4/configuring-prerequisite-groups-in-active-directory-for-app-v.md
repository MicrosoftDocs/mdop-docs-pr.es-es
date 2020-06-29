---
title: Configurar grupos de requisitos previos en Active Directory para App-V
description: Configurar grupos de requisitos previos en Active Directory para App-V
author: dansimp
ms.assetid: 0010d534-46c0-44a3-b5c1-621b4d5e2c31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa1ab6393dee20203b715311d4e1dfdc4c22c679
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821861"
---
# <span data-ttu-id="efd7a-103">Configurar grupos de requisitos previos en Active Directory para App-V</span><span class="sxs-lookup"><span data-stu-id="efd7a-103">Configuring Prerequisite Groups in Active Directory for App-V</span></span>


<span data-ttu-id="efd7a-104">Antes de instalar el servidor de administración de Microsoft Application Virtualization (App-V), debe crear los siguientes objetos en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="efd7a-104">Before you install the Microsoft Application Virtualization (App-V) Management Server, you must create the following objects in Active Directory.</span></span> <span data-ttu-id="efd7a-105">App-V usa grupos de Active Directory para controlar el acceso a las aplicaciones y a las funciones administrativas.</span><span class="sxs-lookup"><span data-stu-id="efd7a-105">App-V uses Active Directory groups to control access to applications and administrative functions.</span></span> <span data-ttu-id="efd7a-106">Usará estos grupos durante el proceso de instalación del servidor y al publicar aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="efd7a-106">You will use these groups during the server installation process and when publishing applications.</span></span>

## <span data-ttu-id="efd7a-107">Configuración de grupos de requisitos previos en Active Directory para la virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="efd7a-107">Configuring Prerequisite Groups in Active Directory for Application Virtualization</span></span>


<span data-ttu-id="efd7a-108">En esta tabla se enumeran los grupos de Active Directory necesarios para instalar App-V.</span><span class="sxs-lookup"><span data-stu-id="efd7a-108">This table lists the Active Directory groups that are required for installing App-V.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="efd7a-109">Objeto</span><span class="sxs-lookup"><span data-stu-id="efd7a-109">Object</span></span></th>
<th align="left"><span data-ttu-id="efd7a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="efd7a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="efd7a-111">Unidad organizativa (OU)</span><span class="sxs-lookup"><span data-stu-id="efd7a-111">Organizational Unit (OU)</span></span></p></td>
<td align="left"><p><span data-ttu-id="efd7a-112">Cree una OU en Active Directory para los grupos específicos necesarios para App-V.</span><span class="sxs-lookup"><span data-stu-id="efd7a-112">Create an OU in Active Directory for the specific groups required for App-V.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="efd7a-113">Grupo administrativo de App-V</span><span class="sxs-lookup"><span data-stu-id="efd7a-113">App-V Administrative Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="efd7a-114">Durante la instalación de App-V Management Server, debe seleccionar un grupo de Active Directory para usarlo como grupo de administradores de App-V para controlar el acceso administrativo a la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="efd7a-114">During installation of the App-V Management Server, you must select an Active Directory group to use as the App-V Administrators group to control administrative access to the Management Console.</span></span> <span data-ttu-id="efd7a-115">Cree un grupo de seguridad para los administradores de App-V y agregue a este grupo todos los usuarios que necesiten usar la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="efd7a-115">Create a security group for App-V administrators, and add to this group every user who needs to use the Management Console.</span></span> <span data-ttu-id="efd7a-116">No puede crear este grupo directamente desde el instalador de App-V Management Server.</span><span class="sxs-lookup"><span data-stu-id="efd7a-116">You cannot create this group directly from the App-V Management Server installer.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="efd7a-117">Grupo de usuarios de App-V</span><span class="sxs-lookup"><span data-stu-id="efd7a-117">App-V Users Group</span></span></p></td>
<td align="left"><p><span data-ttu-id="efd7a-118">App-V requiere que todas las cuentas de usuario que tengan acceso a las funciones de App-V sean miembros de una directiva de proveedor asociada a un único grupo para el acceso a la plataforma general.</span><span class="sxs-lookup"><span data-stu-id="efd7a-118">App-V requires that every User account that accesses App-V functions be a member of a provider policy associated with a single group for general platform access.</span></span> <span data-ttu-id="efd7a-119">Usar un grupo existente; por ejemplo, los usuarios del dominio, si todos los usuarios tienen acceso a App-V, o crear un grupo nuevo.</span><span class="sxs-lookup"><span data-stu-id="efd7a-119">Use an existing group; for example, Domain Users, if all users are to have access to App-V, or create a new group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="efd7a-120">Grupos de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="efd7a-120">Application Groups</span></span></p></td>
<td align="left"><p><span data-ttu-id="efd7a-121">App-V se asocia el derecho de usar una aplicación individual con un grupo de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="efd7a-121">App-V associates the right to use an individual application with an Active Directory group.</span></span> <span data-ttu-id="efd7a-122">Cree un grupo de Active Directory para cada aplicación y asigne los usuarios a estos grupos según sea necesario para controlar el acceso de los usuarios a las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="efd7a-122">Create an Active Directory group for each application, and assign users to these groups as needed to control user access to the applications.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="efd7a-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="efd7a-123">Related topics</span></span>


[<span data-ttu-id="efd7a-124">Requisitos de implementación de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="efd7a-124">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

[<span data-ttu-id="efd7a-125">Cómo configurar Windows Server 2008 para servidores de administración de App-V</span><span class="sxs-lookup"><span data-stu-id="efd7a-125">How to Configure Windows Server 2008 for App-V Management Servers</span></span>](how-to-configure-windows-server-2008-for-app-v-management-servers.md)

 

 





