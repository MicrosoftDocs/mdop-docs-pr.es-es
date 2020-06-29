---
title: Delegar el acceso al entorno de producción
description: Delegar el acceso al entorno de producción
author: dansimp
ms.assetid: c1ebae2e-909b-4e64-b368-b7d3cc67b1eb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4667a23f1584d7aab6143860721e326da6407afb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821011"
---
# <span data-ttu-id="9be46-103">Delegar el acceso al entorno de producción</span><span class="sxs-lookup"><span data-stu-id="9be46-103">Delegate Access to the Production Environment</span></span>


<span data-ttu-id="9be46-104">Puede cambiar el acceso a objetos de directiva de grupo (GPO) en el entorno de producción, reemplazando los permisos existentes en esos GPO.</span><span class="sxs-lookup"><span data-stu-id="9be46-104">You can change access to Group Policy Objects (GPOs) in the production environment, replacing any existing permissions on those GPOs.</span></span> <span data-ttu-id="9be46-105">Puede configurar permisos en el nivel de dominio para permitir o impedir que los usuarios editen, eliminen o modifiquen la seguridad de los GPO en el entorno de producción cuando no usen la carpeta de **control de cambios** en la consola de administración de directivas de grupo (GPMC).</span><span class="sxs-lookup"><span data-stu-id="9be46-105">You can configure permissions at the domain level to either allow or prevent users from editing, deleting, or modifying the security of GPOs in the production environment when they are not using the **Change Control** folder in the Group Policy Management Console (GPMC).</span></span>

**<span data-ttu-id="9be46-106">Nota</span><span class="sxs-lookup"><span data-stu-id="9be46-106">Note</span></span>**  
-   <span data-ttu-id="9be46-107">Delegar el acceso al entorno de producción no afecta la capacidad de los usuarios para vincular GPO.</span><span class="sxs-lookup"><span data-stu-id="9be46-107">Delegating access to the production environment does not affect users’ ability to link GPOs.</span></span>

-   <span data-ttu-id="9be46-108">Cuando se controlan o implementan los GPO, se quita el acceso de cualquier otra cuenta, excepto las que tengan permisos de **lectura** y **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="9be46-108">When GPOs are controlled or deployed, access for any other accounts except those with **Read** and **Apply** permissions is removed.</span></span>

 

<span data-ttu-id="9be46-109">Para completar este procedimiento, se requiere una cuenta de usuario que tenga los permisos necesarios en administración avanzada de directivas de grupo (AGPM) o el rol administrador de AGPM (control total).</span><span class="sxs-lookup"><span data-stu-id="9be46-109">A user account that has either the necessary permissions in Advanced Group Policy Management (AGPM) or the role of AGPM Administrator (Full Control) is required to complete this procedure.</span></span> <span data-ttu-id="9be46-110">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="9be46-110">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="9be46-111">Para cambiar el acceso a los GPO en el entorno de producción</span><span class="sxs-lookup"><span data-stu-id="9be46-111">To change access to GPOs in the production environment</span></span>**

1.  <span data-ttu-id="9be46-112">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="9be46-112">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="9be46-113">Haga clic en la pestaña **delegación de producción** .</span><span class="sxs-lookup"><span data-stu-id="9be46-113">Click the **Production Delegation** tab.</span></span>

3.  <span data-ttu-id="9be46-114">Para agregar permisos para un usuario o grupo que no tiene acceso al entorno de producción, o para reemplazar los permisos de un usuario o grupo que tiene acceso:</span><span class="sxs-lookup"><span data-stu-id="9be46-114">To add permissions for a user or group that does not have access to the production environment, or to replace the permissions for a user or group that does have access:</span></span>

    1.  <span data-ttu-id="9be46-115">Haga clic en **Agregar**, seleccione un usuario o grupo y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9be46-115">Click **Add**, select a user or group, and then click **OK**.</span></span>

    2.  <span data-ttu-id="9be46-116">Seleccione los permisos para delegar a ese usuario o grupo en el entorno de producción y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9be46-116">Select permissions to delegate to that user or group for the production environment, and then click **OK**.</span></span>

4.  <span data-ttu-id="9be46-117">Para quitar todos los permisos en el entorno de producción de un usuario o grupo, seleccione el usuario o el grupo, haga clic en **quitar**y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="9be46-117">To remove all permissions to the production environment for a user or group, select the user or group, click **Remove**, and then click **OK**.</span></span>

### <span data-ttu-id="9be46-118">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="9be46-118">Additional considerations</span></span>

-   <span data-ttu-id="9be46-119">Para realizar este procedimiento, debe ser administrador de AGPM (control total) de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9be46-119">By default, you must be an AGPM Administrator (Full Control) to perform this procedure.</span></span> <span data-ttu-id="9be46-120">En concreto, debe tener permiso de **modificación de seguridad** para el dominio.</span><span class="sxs-lookup"><span data-stu-id="9be46-120">Specifically, you must have **Modify Security** permission for the domain.</span></span>

-   <span data-ttu-id="9be46-121">Los permisos para la cuenta del servicio AGPM no se pueden cambiar en la pestaña **delegación de producción** .</span><span class="sxs-lookup"><span data-stu-id="9be46-121">Permissions for the AGPM Service Account cannot be changed on the **Production Delegation** tab.</span></span>

-   <span data-ttu-id="9be46-122">De forma predeterminada, las siguientes cuentas tienen permisos para los GPO en el entorno de producción:</span><span class="sxs-lookup"><span data-stu-id="9be46-122">By default, the following accounts have permissions for GPOs in the production environment:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="9be46-123">Cuenta</span><span class="sxs-lookup"><span data-stu-id="9be46-123">Account</span></span></th>
    <th align="left"><span data-ttu-id="9be46-124">Permisos predeterminados para GPO</span><span class="sxs-lookup"><span data-stu-id="9be46-124">Default Permissions for GPOs</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9be46-125">&lt;Cuenta de servicio AGPM&gt;</span><span class="sxs-lookup"><span data-stu-id="9be46-125">&lt;AGPM Service Account&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9be46-126">Editar configuración, eliminar, modificar seguridad</span><span class="sxs-lookup"><span data-stu-id="9be46-126">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9be46-127">Usuarios autenticados</span><span class="sxs-lookup"><span data-stu-id="9be46-127">Authenticated Users</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9be46-128">Leer, aplicar</span><span class="sxs-lookup"><span data-stu-id="9be46-128">Read, Apply</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9be46-129">Administradores de dominio</span><span class="sxs-lookup"><span data-stu-id="9be46-129">Domain Admins</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9be46-130">Editar configuración, eliminar, modificar seguridad</span><span class="sxs-lookup"><span data-stu-id="9be46-130">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9be46-131">Administradores de empresa</span><span class="sxs-lookup"><span data-stu-id="9be46-131">Enterprise Admins</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9be46-132">Editar configuración, eliminar, modificar seguridad</span><span class="sxs-lookup"><span data-stu-id="9be46-132">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="9be46-133">Controladores de dominio empresariales</span><span class="sxs-lookup"><span data-stu-id="9be46-133">Enterprise Domain Controllers</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9be46-134">Leer</span><span class="sxs-lookup"><span data-stu-id="9be46-134">Read</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="9be46-135">Sistema</span><span class="sxs-lookup"><span data-stu-id="9be46-135">System</span></span></p></td>
    <td align="left"><p><span data-ttu-id="9be46-136">Editar configuración, eliminar, modificar seguridad</span><span class="sxs-lookup"><span data-stu-id="9be46-136">Edit Settings, Delete, Modify Security</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

-   <span data-ttu-id="9be46-137">Se debe restringir la pertenencia al grupo propietarios del creador de directivas de grupo, Soit no se usa para burlar la administración de AGPM de acceso a los GPO.</span><span class="sxs-lookup"><span data-stu-id="9be46-137">Membership in the Group Policy Creator Owners group should be restricted, soit is not used to circumvent AGPM management of access to GPOs.</span></span> <span data-ttu-id="9be46-138">(En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).</span><span class="sxs-lookup"><span data-stu-id="9be46-138">(In the **Group Policy Management Console**, click **Group Policy Objects** in the forest and domain in which you want to manage GPOs, click **Delegation**, and then configure the settings to meet the needs of your organization.)</span></span>

### <span data-ttu-id="9be46-139">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="9be46-139">Additional references</span></span>

-   [<span data-ttu-id="9be46-140">Configuración de Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="9be46-140">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 





