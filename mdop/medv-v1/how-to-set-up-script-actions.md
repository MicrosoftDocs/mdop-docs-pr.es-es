---
title: Cómo configurar las acciones de script
description: Cómo configurar las acciones de script
author: dansimp
ms.assetid: 367e28f1-d8c2-4845-a01b-2fff9128ccfd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bfa264be447a0a8560e4af16ccaadc2ec1db3f6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812390"
---
# <span data-ttu-id="22b16-103">Cómo configurar las acciones de script</span><span class="sxs-lookup"><span data-stu-id="22b16-103">How to Set Up Script Actions</span></span>


<span data-ttu-id="22b16-104">El editor de acciones de script permite al administrador crear acciones para realizarlas durante la configuración del área de trabajo de MED-V, así como para definir el orden en el que se realizan.</span><span class="sxs-lookup"><span data-stu-id="22b16-104">The script actions editor allows the administrator to create actions to be performed during MED-V workspace setup, as well as to define the order in which they are performed.</span></span>

<span data-ttu-id="22b16-105">A continuación se muestra una lista de las acciones que se pueden agregar al script de configuración de dominio:</span><span class="sxs-lookup"><span data-stu-id="22b16-105">The following is a list of actions that can be added to the domain setup script:</span></span>

-   <span data-ttu-id="22b16-106">**Reinicie Windows**— y reinicie Windows.</span><span class="sxs-lookup"><span data-stu-id="22b16-106">**Restart Windows**—Restart Windows.</span></span>

-   <span data-ttu-id="22b16-107">**Unirse al dominio**: si se une a un dominio, incluya esta acción y configure el nombre de usuario, la contraseña, el nombre de dominio completo, el nombre de dominio NetBIOS y la unidad organizativa (opcional).</span><span class="sxs-lookup"><span data-stu-id="22b16-107">**Join Domain**—If joining a domain, include this action and configure the user name, password, fully qualified domain name, NetBIOS domain name, and organization unit (optional).</span></span>

-   <span data-ttu-id="22b16-108">**Comprobar conectividad**: configurar un servidor para que se conecte con un recurso de red (como el servidor de dominio) y verifique que el área de trabajo de MED-V pueda conectarse a él.</span><span class="sxs-lookup"><span data-stu-id="22b16-108">**Check Connectivity**—Configure a server to connect to and verify that the MED-V workspace can connect to a network resource (such as the domain server).</span></span>

-   <span data-ttu-id="22b16-109">**Línea de comandos**: configure un script en el área de trabajo de MED-V y escriba una línea de comandos que incluya la ruta de acceso de la secuencia de comandos y los argumentos de la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="22b16-109">**Command Line**—Configure a script in the MED-V workspace, and enter a command line that includes the path of the script and the script arguments.</span></span>

-   <span data-ttu-id="22b16-110">**Cambiar nombre de equipo**: cambie el nombre del equipo de la máquina virtual según la configuración definida.</span><span class="sxs-lookup"><span data-stu-id="22b16-110">**Rename Computer**—Rename the virtual machine computer based on the defined settings.</span></span>

-   <span data-ttu-id="22b16-111">**Deshabilitar el inicio de sesión automático**: deshabilitar el inicio de sesión automático de Windows.</span><span class="sxs-lookup"><span data-stu-id="22b16-111">**Disable Auto-Logon**—Disable Windows Auto-Logon.</span></span> <span data-ttu-id="22b16-112">Esta acción debe agregarse al final de las secuencias de comandos que agregan el equipo al dominio.</span><span class="sxs-lookup"><span data-stu-id="22b16-112">This action should be added at the end of scripts that add the computer to the domain.</span></span>

## <a href="" id="how-to-set-up-script-actions-"></a><span data-ttu-id="22b16-113">Cómo configurar las acciones de script</span><span class="sxs-lookup"><span data-stu-id="22b16-113">How to Set Up Script Actions</span></span>


**<span data-ttu-id="22b16-114">Para configurar acciones de script</span><span class="sxs-lookup"><span data-stu-id="22b16-114">To set up script actions</span></span>**

1.  <span data-ttu-id="22b16-115">En la pestaña **configuración de VM** , haga clic en editor de **scripts**.</span><span class="sxs-lookup"><span data-stu-id="22b16-115">On the **VM Setup** tab, click **Script Editor**.</span></span>

2.  <span data-ttu-id="22b16-116">En el cuadro de diálogo **acciones de script** , haga clic en **Agregar**y, en el submenú, haga clic en las acciones que desee.</span><span class="sxs-lookup"><span data-stu-id="22b16-116">In the **Script Actions** dialog box, click **Add**, and on the submenu, click the desired actions.</span></span>

3.  <span data-ttu-id="22b16-117">Configure las acciones según se describe en las tablas siguientes.</span><span class="sxs-lookup"><span data-stu-id="22b16-117">Configure the actions as described in the following tables.</span></span>

    <span data-ttu-id="22b16-118">**Nota:** 
     **Cambiar el nombre del equipo** está configurado en la pestaña **configuración de VM** . Para obtener más información, consulte [Cómo configurar las propiedades del patrón de nombre de equipo VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="22b16-118">**Note**
**Rename Computer** is configured in the **VM Settings** tab. For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

     

~~~
**Note**  
To rename a computer, Windows must be restarted. It is recommended to add a Restart Windows action following a Rename Computer action.
~~~



4. <span data-ttu-id="22b16-119">Establezca el orden de las acciones seleccionando una acción y haciendo clic en **arriba** o **abajo**.</span><span class="sxs-lookup"><span data-stu-id="22b16-119">Set the order of the actions by selecting an action and clicking **Up** or **Down**.</span></span>

5. <span data-ttu-id="22b16-120">Haz clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="22b16-120">Click **OK**.</span></span>

**<span data-ttu-id="22b16-121">Nota</span><span class="sxs-lookup"><span data-stu-id="22b16-121">Note</span></span>**  
<span data-ttu-id="22b16-122">Al ejecutar el script de dominio de unirse, para que el script funcione, el usuario que ha iniciado sesión en la máquina virtual del área de trabajo MED-V debe tener derechos de administrador local.</span><span class="sxs-lookup"><span data-stu-id="22b16-122">When running the Join Domain script, for the script to work, the user logged into the MED-V workspace virtual machine must have local administrator rights.</span></span>



**<span data-ttu-id="22b16-123">Nota</span><span class="sxs-lookup"><span data-stu-id="22b16-123">Note</span></span>**  
<span data-ttu-id="22b16-124">Cuando se ejecuta el script deshabilitar el inicio de sesión automático, se recomienda deshabilitar la cuenta de invitado local que se usa para el inicio de sesión automático una vez completada la configuración inicial.</span><span class="sxs-lookup"><span data-stu-id="22b16-124">When running the Disable Auto-Logon script, it is recommended to disable the local guest account used for the auto-logon once the initial setup is complete.</span></span>



### <a href="" id="bkmk-joindomainproperties"></a>

**<span data-ttu-id="22b16-125">Unirse a propiedades de dominio</span><span class="sxs-lookup"><span data-stu-id="22b16-125">Join Domain Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22b16-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="22b16-126">Property</span></span></th>
<th align="left"><span data-ttu-id="22b16-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="22b16-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22b16-128">Credenciales que se deben usar al unir la máquina virtual al dominio</span><span class="sxs-lookup"><span data-stu-id="22b16-128">Credentials to use when joining the VM to the domain</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-129">Seleccione una de las siguientes credenciales para usarla al unir la VM al dominio:</span><span class="sxs-lookup"><span data-stu-id="22b16-129">Select one of the following credentials to use when joining the VM to the domain:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="22b16-130">Use las credenciales de MED-V </strong> : las credenciales de usuario final.</span><span class="sxs-lookup"><span data-stu-id="22b16-130">Use MED-V credentials</strong>—The end-user credentials.</span></span></p></li>
<li><p><strong><span data-ttu-id="22b16-131">Use las credenciales siguientes </strong> : las credenciales especificadas; escriba un nombre de usuario y una contraseña en los campos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="22b16-131">Use the following credentials</strong>—The credentials specified; enter a user name and password in the corresponding fields.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="22b16-132">Nota</span><span class="sxs-lookup"><span data-stu-id="22b16-132">Note</span></span></strong><br/><p><span data-ttu-id="22b16-133">Las credenciales que escriba están visibles para todos los usuarios del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="22b16-133">The credentials you enter are visible to all MED-V workspace users.</span></span> <span data-ttu-id="22b16-134">No se recomienda proporcionar credenciales de administrador de dominio.</span><span class="sxs-lookup"><span data-stu-id="22b16-134">It is not recommended to provide domain administrator credentials.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22b16-135">Dominio al que unirse</span><span class="sxs-lookup"><span data-stu-id="22b16-135">Domain to join</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-136">Selecciona uno de los motivos siguientes:</span><span class="sxs-lookup"><span data-stu-id="22b16-136">Select one of the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="22b16-137">Use el nombre de dominio que se usa para iniciar el área de trabajo </strong> : Únase al dominio introducido por el usuario final al iniciar sesión en el cliente de MED-V.</span><span class="sxs-lookup"><span data-stu-id="22b16-137">Use the domain name utilized in starting the Workspace</strong>—Join the domain entered by the end user when logging into the MED-V client.</span></span></p>
<p><span data-ttu-id="22b16-138">Para definir la asignación de NetBIOS a nombres de dominio completos, haga clic en <strong> tabla global de asignación de dominios </strong> .</span><span class="sxs-lookup"><span data-stu-id="22b16-138">To define the mapping from NetBIOS to fully qualified domain names, click <strong>Global domain mapping table</strong>.</span></span> <span data-ttu-id="22b16-139">En la tabla de asignación de dominios global, haga clic en <strong> agregar </strong> , escriba un <strong> nombre de dominio NetBIOS </strong> y un <strong> nombre de dominio completo </strong> , y haga clic en <strong> Aceptar </strong> .</span><span class="sxs-lookup"><span data-stu-id="22b16-139">In the global domain mapping table, click <strong>Add</strong>, enter a <strong>NetBIOS domain name</strong> and a <strong>Fully qualified domain name</strong>, and click <strong>OK</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="22b16-140">Usar el siguiente nombre de dominio </strong> : Únase al dominio especificado; escriba un nombre de dominio y un nombre de dominio NetBIOS en los campos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="22b16-140">Use the following domain name</strong>—Join the domain specified; enter a domain name and NetBIOS domain name in the corresponding fields.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22b16-141">Unidad de organización</span><span class="sxs-lookup"><span data-stu-id="22b16-141">Organization Unit</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-142">Se puede especificar una unidad organizativa (OU) para unir el equipo a una unidad organizativa específica.</span><span class="sxs-lookup"><span data-stu-id="22b16-142">An organization unit (OU) may be specified to join the computer to a specific OU.</span></span> <span data-ttu-id="22b16-143">El formato debe seguir a un nombre distintivo de Uo: OU = organización de la &lt; organización &gt; , &lt; controlador &gt; de dominio (por ejemplo, ou = QATest, DC = Il, DC = MED-V, DC = com).</span><span class="sxs-lookup"><span data-stu-id="22b16-143">The format must follow an OU distinguished name: OU=&lt;Organization Unit&gt;,&lt;Domain Controller&gt; (for example, OU=QATest, DC=il, DC=MED-V, DC=com).</span></span></p>
<div class="alert">
<strong><span data-ttu-id="22b16-144">Advertencia</span><span class="sxs-lookup"><span data-stu-id="22b16-144">Warning</span></span></strong><br/><p><span data-ttu-id="22b16-145">Solo se admite una OU de un solo nivel, tal y como se muestra en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="22b16-145">Only a single level OU is supported as is shown in the example above.</span></span></p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-checkconnectivityproperties"></a>

**<span data-ttu-id="22b16-146">Comprobar propiedades de conectividad</span><span class="sxs-lookup"><span data-stu-id="22b16-146">Check Connectivity Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22b16-147">Propiedad</span><span class="sxs-lookup"><span data-stu-id="22b16-147">Property</span></span></th>
<th align="left"><span data-ttu-id="22b16-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="22b16-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22b16-149">Dirección IP</span><span class="sxs-lookup"><span data-stu-id="22b16-149">IP Address</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-150">La dirección IP del servidor con el que está comprobando la conexión.</span><span class="sxs-lookup"><span data-stu-id="22b16-150">The IP Address of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22b16-151">Port</span><span class="sxs-lookup"><span data-stu-id="22b16-151">Port</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-152">El puerto del servidor al que está comprobando la conexión.</span><span class="sxs-lookup"><span data-stu-id="22b16-152">The port of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22b16-153">Tiempo de espera agotado</span><span class="sxs-lookup"><span data-stu-id="22b16-153">Timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-154">Número de segundos que se espera una respuesta antes de que se agote el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="22b16-154">The number of seconds to wait for a response before timing out.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-commandlineproperties"></a>

**<span data-ttu-id="22b16-155">Propiedades de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="22b16-155">Command-Line Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22b16-156">Propiedad</span><span class="sxs-lookup"><span data-stu-id="22b16-156">Property</span></span></th>
<th align="left"><span data-ttu-id="22b16-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="22b16-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22b16-158">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="22b16-158">Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-159">La ruta de acceso de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="22b16-159">The path of the command line.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22b16-160">Argumentos</span><span class="sxs-lookup"><span data-stu-id="22b16-160">Arguments</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-161">Argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="22b16-161">Command-line arguments.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22b16-162">Esperar salida</span><span class="sxs-lookup"><span data-stu-id="22b16-162">Wait for exit</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-163">Seleccione la casilla de verificación para esperar una devolución antes de continuar con las acciones de script.</span><span class="sxs-lookup"><span data-stu-id="22b16-163">Select the check box to wait for a return before continuing with the script actions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22b16-164">Error en el error</span><span class="sxs-lookup"><span data-stu-id="22b16-164">Fail on error</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-165">Seleccione esta casilla si la respuesta es algo menos el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="22b16-165">Select this check box if the return is anything but the value specified.</span></span></p>
<p><span data-ttu-id="22b16-166">Escriba el valor que indicará el comando como un éxito.</span><span class="sxs-lookup"><span data-stu-id="22b16-166">Enter the value that will indicate the command as a success.</span></span></p>
<p><span data-ttu-id="22b16-167">Valor predeterminado: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="22b16-167">Default: <strong>0</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22b16-168">Realizar una sola vez</span><span class="sxs-lookup"><span data-stu-id="22b16-168">Perform only once</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-169">Seleccione esta casilla para ejecutar la línea de comandos solo una vez.</span><span class="sxs-lookup"><span data-stu-id="22b16-169">Select this check box to run the command line only once.</span></span> <span data-ttu-id="22b16-170">Si se produce un error en el script o se cancela, este comando no se volverá a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="22b16-170">If the script fails or is canceled, this command will not be performed again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22b16-171">Esta línea de comandos provoca el reinicio de las ventanas en el área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="22b16-171">This command line causes a restart of Windows in the Workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-172">Seleccione esta casilla si la línea de comandos provoca el reinicio después de la finalización.</span><span class="sxs-lookup"><span data-stu-id="22b16-172">Select this check box if the command line causes a restart after completion.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22b16-173">Permitir interacción</span><span class="sxs-lookup"><span data-stu-id="22b16-173">Allow interaction</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-174">Seleccione esta casilla si el comando necesitará la interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="22b16-174">Select this check box if the command will require user interaction.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22b16-175">Mensaje de progreso</span><span class="sxs-lookup"><span data-stu-id="22b16-175">Progress message</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-176">Mensaje que se mostrará al usuario mientras se ejecuta el comando.</span><span class="sxs-lookup"><span data-stu-id="22b16-176">Message to be displayed to the user while the command is running.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22b16-177">Mensaje de error</span><span class="sxs-lookup"><span data-stu-id="22b16-177">Failure message</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-178">Mensaje que se mostrará al usuario si se produce un error en el comando.</span><span class="sxs-lookup"><span data-stu-id="22b16-178">Message to be displayed to the user if the command fails.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="22b16-179">Al configurar la acción de línea de comandos, se pueden usar varias variables, tal y como se define en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="22b16-179">When configuring the command-line action, several variables can be used as defined in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="22b16-180">Parámetro</span><span class="sxs-lookup"><span data-stu-id="22b16-180">Parameter</span></span></th>
<th align="left"><span data-ttu-id="22b16-181">Valor</span><span class="sxs-lookup"><span data-stu-id="22b16-181">Value</span></span></th>
<th align="left"><span data-ttu-id="22b16-182">Descripción</span><span class="sxs-lookup"><span data-stu-id="22b16-182">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22b16-183">%MEDVUser%</span><span class="sxs-lookup"><span data-stu-id="22b16-183">%MEDVUser%</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-184">Un nombre de usuario autenticado.</span><span class="sxs-lookup"><span data-stu-id="22b16-184">An authenticated user name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-185">Nombre de usuario autenticado MED-V.</span><span class="sxs-lookup"><span data-stu-id="22b16-185">MED-V authenticated user name.</span></span> <span data-ttu-id="22b16-186">El nombre de usuario y la contraseña se pueden usar en el script de configuración de VM de dominio combinado.</span><span class="sxs-lookup"><span data-stu-id="22b16-186">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22b16-187">%MEDVPassword%</span><span class="sxs-lookup"><span data-stu-id="22b16-187">%MEDVPassword%</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-188">Una contraseña autenticada.</span><span class="sxs-lookup"><span data-stu-id="22b16-188">An authenticated password.</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-189">Contraseña autenticada MED-V.</span><span class="sxs-lookup"><span data-stu-id="22b16-189">MED-V authenticated password.</span></span> <span data-ttu-id="22b16-190">El nombre de usuario y la contraseña se pueden usar en el script de configuración de VM de dominio combinado.</span><span class="sxs-lookup"><span data-stu-id="22b16-190">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="22b16-191">%MEDVDomain%</span><span class="sxs-lookup"><span data-stu-id="22b16-191">%MEDVDomain%</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-192">Dominio configurado.</span><span class="sxs-lookup"><span data-stu-id="22b16-192">Configured domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-193">El dominio configurado en la autenticación de MED-V.</span><span class="sxs-lookup"><span data-stu-id="22b16-193">The domain configured in the MED-V authentication.</span></span> <span data-ttu-id="22b16-194">Puede usarse en el script de configuración de VM.</span><span class="sxs-lookup"><span data-stu-id="22b16-194">It can be used on the VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="22b16-195">%DesiredMachineName%</span><span class="sxs-lookup"><span data-stu-id="22b16-195">%DesiredMachineName%</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-196">Nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="22b16-196">Computer name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="22b16-197">El nombre de equipo único configurado en la aplicación de administración.</span><span class="sxs-lookup"><span data-stu-id="22b16-197">The unique computer name configured in the management application.</span></span> <span data-ttu-id="22b16-198">Puede usarse en el script de configuración de VM.</span><span class="sxs-lookup"><span data-stu-id="22b16-198">It can be used in the VM setup script.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="22b16-199">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22b16-199">Related topics</span></span>


[<span data-ttu-id="22b16-200">Cómo configurar la configuración de máquina virtual para un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="22b16-200">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="22b16-201">Cómo configurar las propiedades del patrón de nombre de equipo de VM</span><span class="sxs-lookup"><span data-stu-id="22b16-201">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

 

 





