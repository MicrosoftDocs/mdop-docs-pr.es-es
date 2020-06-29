---
title: Cómo configurar un usuario de dominio o un grupo
description: Cómo configurar un usuario de dominio o un grupo
author: dansimp
ms.assetid: 055aba81-a9c9-4b98-969d-775e603becf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c51da13808df657c1341572767c24860d9d5e8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827200"
---
# <span data-ttu-id="f7add-103">Cómo configurar un usuario de dominio o un grupo</span><span class="sxs-lookup"><span data-stu-id="f7add-103">How to Configure a Domain User or Group</span></span>


<span data-ttu-id="f7add-104">La configuración de implementación le permite controlar qué usuarios o grupos pueden acceder al área de trabajo de MED-V, así como el tiempo que se puede usar el área de trabajo de MED-V y si se puede usar sin conexión.</span><span class="sxs-lookup"><span data-stu-id="f7add-104">The deployment settings enable you to control which users or groups can access the MED-V workspace, as well as how long the MED-V workspace can be utilized and whether it can be used offline.</span></span> <span data-ttu-id="f7add-105">También puede configurar reglas adicionales para controlar el acceso entre el área de trabajo de MED-V y el host.</span><span class="sxs-lookup"><span data-stu-id="f7add-105">You can also configure additional rules to control access between the MED-V workspace and the host.</span></span>

<span data-ttu-id="f7add-106">Todos los permisos de área de trabajo de MED-V se configuran en el módulo **Directiva** , en la pestaña **implementación** .</span><span class="sxs-lookup"><span data-stu-id="f7add-106">All MED-V workspace permissions are configured in the **Policy** module, on the **Deployment** tab.</span></span>

<span data-ttu-id="f7add-107">Para permitir que los usuarios usen el área de trabajo de MED-V, primero debe agregar usuarios del dominio o grupos a permisos de área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="f7add-107">To allow users to utilize the MED-V workspace, you must first add domain users or groups to the MED-V workspace permissions.</span></span> <span data-ttu-id="f7add-108">Después, puede establecer permisos para cada usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="f7add-108">You can then set permissions for each user or group.</span></span>

## <span data-ttu-id="f7add-109">Cómo agregar un usuario o grupo de dominio</span><span class="sxs-lookup"><span data-stu-id="f7add-109">How to Add a Domain User or Group</span></span>


**<span data-ttu-id="f7add-110">Para agregar un usuario o grupo de dominio</span><span class="sxs-lookup"><span data-stu-id="f7add-110">To add a domain user or group</span></span>**

1.  <span data-ttu-id="f7add-111">En la ventana **usuarios/grupos** , haga clic en **Agregar.**</span><span class="sxs-lookup"><span data-stu-id="f7add-111">In the **Users / Groups** window, click **Add.**</span></span>

2.  <span data-ttu-id="f7add-112">En el cuadro de diálogo **Escriba los nombres de usuario o grupo** , seleccione usuarios o grupos del dominio mediante una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="f7add-112">In the **Enter User or Group names** dialog box, select domain users or groups by doing one of the following:</span></span>

    -   <span data-ttu-id="f7add-113">En el campo **Escriba los nombres de usuario o grupo** , escriba un usuario o grupo que exista en el dominio o como un grupo o usuario local en el equipo.</span><span class="sxs-lookup"><span data-stu-id="f7add-113">In the **Enter User or Group names** field, type a user or group that exists in the domain or as a local user or group on the computer.</span></span> <span data-ttu-id="f7add-114">A continuación, haga clic en **Comprobar nombres** para resolver el nombre completo.</span><span class="sxs-lookup"><span data-stu-id="f7add-114">Then click **Check Names** to resolve it to the full existent name.</span></span>

    -   <span data-ttu-id="f7add-115">Haga clic en **Buscar** para abrir el cuadro de diálogo **Seleccionar usuarios o grupos** estándar.</span><span class="sxs-lookup"><span data-stu-id="f7add-115">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="f7add-116">Después, seleccione usuarios o grupos del dominio.</span><span class="sxs-lookup"><span data-stu-id="f7add-116">Then select domain users or groups.</span></span>

3.  <span data-ttu-id="f7add-117">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="f7add-117">Click **OK**.</span></span>

    <span data-ttu-id="f7add-118">Se agregan los usuarios o grupos del dominio.</span><span class="sxs-lookup"><span data-stu-id="f7add-118">The domain users or groups are added.</span></span>

    **<span data-ttu-id="f7add-119">Nota</span><span class="sxs-lookup"><span data-stu-id="f7add-119">Note</span></span>**  
    <span data-ttu-id="f7add-120">Los usuarios de dominios de confianza deben agregarse de forma manual.</span><span class="sxs-lookup"><span data-stu-id="f7add-120">Users from trusted domains should be added manually.</span></span>



~~~
**Warning**  
Do not run the management application from a computer that is part of a domain that is not trusted by the domain the server is installed on.
~~~



## <span data-ttu-id="f7add-121">Cómo quitar un usuario o grupo de dominio</span><span class="sxs-lookup"><span data-stu-id="f7add-121">How to Remove a Domain User or Group</span></span>


**<span data-ttu-id="f7add-122">Para quitar un usuario o grupo de dominio</span><span class="sxs-lookup"><span data-stu-id="f7add-122">To remove a domain user or group</span></span>**

1.  <span data-ttu-id="f7add-123">En la ventana **usuarios/grupos** , seleccione un usuario o un grupo.</span><span class="sxs-lookup"><span data-stu-id="f7add-123">In the **Users / Groups** window, select a user or group.</span></span>

2.  <span data-ttu-id="f7add-124">Haga clic en **quitar**.</span><span class="sxs-lookup"><span data-stu-id="f7add-124">Click **Remove**.</span></span>

    <span data-ttu-id="f7add-125">Se elimina el usuario o el grupo.</span><span class="sxs-lookup"><span data-stu-id="f7add-125">The user or group is deleted.</span></span>

## <span data-ttu-id="f7add-126">Cómo establecer permisos para un usuario o un grupo</span><span class="sxs-lookup"><span data-stu-id="f7add-126">How to Set Permissions for a User or a Group</span></span>


**<span data-ttu-id="f7add-127">Para establecer permisos para un usuario o un grupo</span><span class="sxs-lookup"><span data-stu-id="f7add-127">To set permissions for a user or a group</span></span>**

1.  <span data-ttu-id="f7add-128">Haga clic en el usuario o grupo para el que está configurando los permisos.</span><span class="sxs-lookup"><span data-stu-id="f7add-128">Click the user or group for which you are setting the permissions.</span></span>

2.  <span data-ttu-id="f7add-129">Configure las propiedades del área de trabajo de MED-V tal como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f7add-129">Configure the MED-V workspace properties as described in the following table.</span></span>

3.  <span data-ttu-id="f7add-130">En el menú **Directiva** , seleccione **confirmar**.</span><span class="sxs-lookup"><span data-stu-id="f7add-130">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="f7add-131">Propiedades de implementación de área de trabajo</span><span class="sxs-lookup"><span data-stu-id="f7add-131">Workspace Deployment Properties</span></span>**

<span data-ttu-id="f7add-132">Descripción *General* de la propiedad</span><span class="sxs-lookup"><span data-stu-id="f7add-132">Property Description *General*</span></span>

<span data-ttu-id="f7add-133">Habilitar área de trabajo para &lt; usuario o grupo&gt;</span><span class="sxs-lookup"><span data-stu-id="f7add-133">Enable Workspace for &lt;user or group&gt;</span></span>

<span data-ttu-id="f7add-134">Seleccione esta casilla para habilitar el área de trabajo de MED-V para este usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="f7add-134">Select this check box to enable the MED-V workspace for this user or group.</span></span>

<span data-ttu-id="f7add-135">El área de trabajo vence en esta fecha</span><span class="sxs-lookup"><span data-stu-id="f7add-135">Workspace expires on this date</span></span>

<span data-ttu-id="f7add-136">Seleccione esta casilla para asignar una fecha de expiración para el conjunto de permisos para este usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="f7add-136">Select this check box to assign an expiration date for the permissions set for this user or group.</span></span>

<span data-ttu-id="f7add-137">Cuando se selecciona, el cuadro de fecha está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f7add-137">When selected, the date box is enabled.</span></span> <span data-ttu-id="f7add-138">Establezca la fecha y los permisos vencerán al final de la fecha especificada.</span><span class="sxs-lookup"><span data-stu-id="f7add-138">Set the date, and permissions will expire at the end of the date specified.</span></span>

<span data-ttu-id="f7add-139">El trabajo sin conexión está restringido a</span><span class="sxs-lookup"><span data-stu-id="f7add-139">Offline work is restricted to</span></span>

<span data-ttu-id="f7add-140">Seleccione esta casilla para asignar un período de tiempo en el que se debe actualizar la Directiva para este usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="f7add-140">Select this check box to assign a time period in which the policy must be refreshed for this user or group.</span></span> <span data-ttu-id="f7add-141">Cuando se selecciona, el cuadro período de tiempo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f7add-141">When selected, the time period box is enabled.</span></span> <span data-ttu-id="f7add-142">Establezca el número de días u horas, y al final del período de tiempo especificado, el usuario o el grupo no se podrá conectar si la Directiva no se actualiza.</span><span class="sxs-lookup"><span data-stu-id="f7add-142">Set the number of days or hours, and at the end of the specified time period, the user or group will not be able to connect if the policy is not refreshed.</span></span>

<span data-ttu-id="f7add-143">Opciones de eliminación de área de trabajo</span><span class="sxs-lookup"><span data-stu-id="f7add-143">Workspace deletion options</span></span>

<span data-ttu-id="f7add-144">Haga clic para establecer las opciones de eliminación del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="f7add-144">Click to set the MED-V workspace deletion options.</span></span> <span data-ttu-id="f7add-145">Para obtener más información, vea [Cómo configurar las opciones de eliminación del área de trabajo de MED-V](how-to-set-med-v-workspace-deletion-options.md).</span><span class="sxs-lookup"><span data-stu-id="f7add-145">For more information, see [How to Set MED-V Workspace Deletion Options](how-to-set-med-v-workspace-deletion-options.md).</span></span>

*<span data-ttu-id="f7add-146">Transferencia de datos</span><span class="sxs-lookup"><span data-stu-id="f7add-146">Data Transfer</span></span>*

<span data-ttu-id="f7add-147">Compatibilidad del portapapeles entre el host y el área de trabajo</span><span class="sxs-lookup"><span data-stu-id="f7add-147">Support clipboard between host and Workspace</span></span>

<span data-ttu-id="f7add-148">Active esta casilla para habilitar la copia y pegado entre el área de trabajo de host y MED-V.</span><span class="sxs-lookup"><span data-stu-id="f7add-148">Select this check box to enable copying and pasting between the host and the MED-V workspace.</span></span>

<span data-ttu-id="f7add-149">Admitir la transferencia de archivos entre el host y el área de trabajo</span><span class="sxs-lookup"><span data-stu-id="f7add-149">Support file transfer between the host and Workspace</span></span>

<span data-ttu-id="f7add-150">Active esta casilla para habilitar la transferencia de archivos entre el host y el área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="f7add-150">Select this check box to enable transferring files between the host and MED-V workspace.</span></span> <span data-ttu-id="f7add-151">Seleccione una de las siguientes opciones en el cuadro **transferencia de archivos** :</span><span class="sxs-lookup"><span data-stu-id="f7add-151">Select one of the following options from the **File Transfer** box:</span></span>

-   <span data-ttu-id="f7add-152">**Ambos**: permite transferir archivos entre el host y el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="f7add-152">**Both**—Enable transferring files between the host and the MED-V workspace.</span></span>

-   <span data-ttu-id="f7add-153">**Hospedar en el área de trabajo**: permite la transferencia de archivos desde el host al área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="f7add-153">**Host to Workspace**—Enable transferring files from the host to the MED-V workspace.</span></span>

-   <span data-ttu-id="f7add-154">**Área de trabajo para hospedar**: permite transferir archivos desde el área de trabajo de MED-V al host.</span><span class="sxs-lookup"><span data-stu-id="f7add-154">**Workspace to Host**—Enable transferring files from the MED-V workspace to the host.</span></span>

**<span data-ttu-id="f7add-155">Nota</span><span class="sxs-lookup"><span data-stu-id="f7add-155">Note</span></span>**  
<span data-ttu-id="f7add-156">Si un usuario sin permisos intenta transferir archivos, aparece una ventana que le pide que escriba las credenciales de un usuario con permisos para realizar la transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="f7add-156">If a user without permissions attempts to transfer files, a window will appear prompting him to enter the credentials of a user with permissions to perform the file transfer.</span></span>



**<span data-ttu-id="f7add-157">Importante</span><span class="sxs-lookup"><span data-stu-id="f7add-157">Important</span></span>**  
<span data-ttu-id="f7add-158">Para admitir la transferencia de archivos en Windows XP SP3, debe deshabilitar la sincronización de archivos sin conexión modificando el registro de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f7add-158">To support file transfer in Windows XP SP3, you must disable offline file synchronization by editing the registry as follows:</span></span>

`REG ADD HKLM\software\microsoft\windows\currentversion\netcache /V Enabled /T REG_DWORD /F /D 0`



<span data-ttu-id="f7add-159">Avanzado</span><span class="sxs-lookup"><span data-stu-id="f7add-159">Advanced</span></span>

<span data-ttu-id="f7add-160">Haga clic para establecer las opciones avanzadas de transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="f7add-160">Click to set the advanced file transfer options.</span></span> <span data-ttu-id="f7add-161">Para obtener más información, consulte [cómo establecer opciones avanzadas de transferencia de archivos](how-to-set-advanced-file-transfer-options.md).</span><span class="sxs-lookup"><span data-stu-id="f7add-161">For more information, see [How to Set Advanced File Transfer Options](how-to-set-advanced-file-transfer-options.md).</span></span>

*<span data-ttu-id="f7add-162">Control de dispositivo</span><span class="sxs-lookup"><span data-stu-id="f7add-162">Device Control</span></span>*

<span data-ttu-id="f7add-163">Habilitar la impresión en impresoras conectadas al host</span><span class="sxs-lookup"><span data-stu-id="f7add-163">Enable printing to printers connected to the host</span></span>

<span data-ttu-id="f7add-164">Active esta casilla para permitir que los usuarios impriman desde el área de trabajo de MED-V con la impresora de host.</span><span class="sxs-lookup"><span data-stu-id="f7add-164">Select this check box to enable users to print from the MED-V workspace using the host printer.</span></span>

**<span data-ttu-id="f7add-165">Nota</span><span class="sxs-lookup"><span data-stu-id="f7add-165">Note</span></span>**  
<span data-ttu-id="f7add-166">La impresión es realizada por las impresoras definidas en el host.</span><span class="sxs-lookup"><span data-stu-id="f7add-166">The printing is performed by the printers defined on the host.</span></span>



<span data-ttu-id="f7add-167">Habilitar el acceso a CD/DVD</span><span class="sxs-lookup"><span data-stu-id="f7add-167">Enable access to CD / DVD</span></span>

<span data-ttu-id="f7add-168">Active esta casilla para permitir el acceso a una unidad de CD o DVD desde este área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="f7add-168">Select this check box to allow access to a CD or DVD drive from this MED-V workspace.</span></span>



**<span data-ttu-id="f7add-169">Varias pertenencias</span><span class="sxs-lookup"><span data-stu-id="f7add-169">Multiple Memberships</span></span>**

1.  <span data-ttu-id="f7add-170">Si el usuario forma parte de un grupo y los permisos se aplican al usuario, así como al grupo del que forman parte, se aplicarán todos los permisos.</span><span class="sxs-lookup"><span data-stu-id="f7add-170">If the user is part of a group and permissions are applied to the user as well as to the group they are part of, all permissions are applied.</span></span>

2.  <span data-ttu-id="f7add-171">Si el usuario es miembro de dos grupos diferentes, se aplican los permisos menos restrictivos.</span><span class="sxs-lookup"><span data-stu-id="f7add-171">If the user is a member of two different groups, the least restrictive permissions are applied.</span></span>

## <span data-ttu-id="f7add-172">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f7add-172">Related topics</span></span>


[<span data-ttu-id="f7add-173">Uso de la interfaz de usuario de la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="f7add-173">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="f7add-174">Creación de un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="f7add-174">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="f7add-175">Cómo configurar las opciones de eliminación de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="f7add-175">How to Set MED-V Workspace Deletion Options</span></span>](how-to-set-med-v-workspace-deletion-options.md)

[<span data-ttu-id="f7add-176">Cómo configurar las opciones de transferencia de archivos avanzadas</span><span class="sxs-lookup"><span data-stu-id="f7add-176">How to Set Advanced File Transfer Options</span></span>](how-to-set-advanced-file-transfer-options.md)









