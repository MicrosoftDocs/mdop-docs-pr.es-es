---
title: Planificación de la migración desde versiones anteriores
description: Planificación de la migración desde versiones anteriores
author: dansimp
ms.assetid: 62967bf1-542f-41b0-838f-c62f3430ac73
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9b239e09da06270b30b401151cf12e817e2cf8d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815930"
---
# <span data-ttu-id="422ac-103">Planificación de la migración desde versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="422ac-103">Planning for Migration from Previous Versions</span></span>


<span data-ttu-id="422ac-104">Antes de intentar actualizar a Microsoft Application Virtualization 4.5 o versiones posteriores, cualquier versión anterior a 4.1 debe actualizarse a la versión 4.1.</span><span class="sxs-lookup"><span data-stu-id="422ac-104">Before attempting to upgrade to Microsoft Application Virtualization4.5 or later versions, any version prior to4.1 must be upgraded to version4.1.</span></span> <span data-ttu-id="422ac-105">Debe planear la actualización de los clientes en primer lugar y, a continuación, actualizar los componentes del servidor.</span><span class="sxs-lookup"><span data-stu-id="422ac-105">You should plan to upgrade your clients first, and then upgrade the server components.</span></span> <span data-ttu-id="422ac-106">Los clientes que se hayan actualizado a 4.5 seguirán funcionando con servidores de virtualización de aplicaciones que aún no se hayan actualizado.</span><span class="sxs-lookup"><span data-stu-id="422ac-106">Clients that have been upgraded to4.5 will continue to work with Application Virtualization servers that have not yet been upgraded.</span></span> <span data-ttu-id="422ac-107">Los servidores que se han actualizado a 4.5 no admiten versiones anteriores del cliente.</span><span class="sxs-lookup"><span data-stu-id="422ac-107">Earlier versions of the client are not supported on servers that have been upgraded to4.5.</span></span> <span data-ttu-id="422ac-108">Para obtener más información sobre cómo actualizar los componentes del sistema, vea [implementación de Application Virtualization y consideraciones](application-virtualization-deployment-and-upgrade-considerations.md)sobre la actualización.</span><span class="sxs-lookup"><span data-stu-id="422ac-108">For more information about upgrading the system components, see [Application Virtualization Deployment and Upgrade Considerations](application-virtualization-deployment-and-upgrade-considerations.md).</span></span>

<span data-ttu-id="422ac-109">Para ayudar a garantizar una migración correcta, los componentes del sistema de virtualización de aplicaciones deben actualizarse en el siguiente orden:</span><span class="sxs-lookup"><span data-stu-id="422ac-109">To help ensure a successful migration, the Application Virtualization system components should be upgraded in the following order:</span></span>

1.  **<span data-ttu-id="422ac-110">Clientes de Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="422ac-110">Microsoft Application Virtualization Clients.</span></span>** <span data-ttu-id="422ac-111">Para obtener instrucciones paso a paso para la actualización, vea [Cómo actualizar el cliente de virtualización de aplicaciones](how-to-upgrade-the-application-virtualization-client.md).</span><span class="sxs-lookup"><span data-stu-id="422ac-111">For step-by-step upgrade instructions, see [How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md).</span></span>

2.  **<span data-ttu-id="422ac-112">Base de datos y servidores de virtualización de aplicaciones de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="422ac-112">Microsoft Application Virtualization Servers and Database.</span></span>** <span data-ttu-id="422ac-113">Para obtener instrucciones paso a paso para la actualización, consulte [Cómo actualizar los servidores y los componentes del sistema](how-to-upgrade-the-servers-and-system-components.md).</span><span class="sxs-lookup"><span data-stu-id="422ac-113">For step-by-step upgrade instructions, see [How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md).</span></span>

    <span data-ttu-id="422ac-114">**Nota:**  Si tiene más de un servidor que comparte el acceso a la base de datos de virtualización de la aplicación, todos esos servidores deben estar desconectados mientras se actualiza la base de datos.</span><span class="sxs-lookup"><span data-stu-id="422ac-114">**Note** If you have more than one server sharing access to the Application Virtualization database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="422ac-115">Debe seguir las prácticas normales de negocios para la actualización de la base de datos, pero es muy aconsejable que pruebe la actualización de la base de datos con una copia de seguridad de la base de datos en primer lugar en un servidor de prueba.</span><span class="sxs-lookup"><span data-stu-id="422ac-115">You should follow your normal business practices for the database upgrade, but it is highly advisable that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="422ac-116">Después, seleccione uno de los servidores para la primera actualización, que actualizará el esquema de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="422ac-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="422ac-117">Una vez que la base de datos de producción se ha actualizado correctamente, puede actualizar los otros servidores.</span><span class="sxs-lookup"><span data-stu-id="422ac-117">After the production database has been successfully upgraded, you can upgrade the other servers.</span></span>

     

3.  **<span data-ttu-id="422ac-118">Servicio Web de administración de Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="422ac-118">Microsoft Application Virtualization Management Web Service.</span></span>** <span data-ttu-id="422ac-119">Este paso solo se aplica si el servicio Web de administración está en un servidor independiente, lo que requiere que ejecute el programa de instalación del servidor en ese servidor independiente para actualizar el servicio Web.</span><span class="sxs-lookup"><span data-stu-id="422ac-119">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Web service.</span></span> <span data-ttu-id="422ac-120">De lo contrario, el paso de actualización del servidor anterior actualizará automáticamente el servicio Web de administración.</span><span class="sxs-lookup"><span data-stu-id="422ac-120">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span>

4.  **<span data-ttu-id="422ac-121">Consola de administración de Microsoft Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="422ac-121">Microsoft Application Virtualization Management Console.</span></span>** <span data-ttu-id="422ac-122">Este paso solo se aplica si la consola de administración está en un equipo independiente, lo que requiere que ejecute el programa de instalación de servidor en ese equipo diferente para actualizar la consola.</span><span class="sxs-lookup"><span data-stu-id="422ac-122">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="422ac-123">De lo contrario, el paso de actualización del servidor anterior actualizará la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="422ac-123">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span>

5.  **<span data-ttu-id="422ac-124">Microsoft Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="422ac-124">Microsoft Application Virtualization Sequencer.</span></span>** <span data-ttu-id="422ac-125">Para obtener instrucciones paso a paso, vea [Cómo instalar Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span><span class="sxs-lookup"><span data-stu-id="422ac-125">For step-by-step instructions, see [How to Install the Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).</span></span> <span data-ttu-id="422ac-126">No será necesario reordenar los paquetes de aplicaciones virtuales de la versión 4.2 para usarlos con la versión 4.5.</span><span class="sxs-lookup"><span data-stu-id="422ac-126">Any virtual application packages sequenced in version4.2 will not have to be re-sequenced for use with version4.5.</span></span> <span data-ttu-id="422ac-127">Sin embargo, considere la posibilidad de actualizar los paquetes virtuales al formato Microsoft Application Virtualization 4.5 Si desea aplicar listas de control de acceso (ACL) predeterminadas o generar un archivo de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="422ac-127">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization4.5 format if you would like to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="422ac-128">Este es un proceso simple y solo requiere que el paquete de la aplicación virtual existente se abra y se guarde con el secuenciador de la versi 4.5.</span><span class="sxs-lookup"><span data-stu-id="422ac-128">This is a simple process and requires only that the existing virtual application package be opened and saved with the4.5 Sequencer.</span></span> <span data-ttu-id="422ac-129">Esto se puede automatizar usando la interfaz de línea de comandos de Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="422ac-129">This can be automated by using the Application Virtualization Sequencer command-line interface.</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="422ac-130">Compatibilidad con paquetes del cliente de App-V 4.6</span><span class="sxs-lookup"><span data-stu-id="422ac-130">App-V4.6 Client Package Support</span></span>


<span data-ttu-id="422ac-131">Puede implementar paquetes creados en versiones anteriores de App-V para aplicaciones-V 4.6 clientes.</span><span class="sxs-lookup"><span data-stu-id="422ac-131">You can deploy packages created in previous versions of App-V to App-V4.6 Clients.</span></span> <span data-ttu-id="422ac-132">Sin embargo, debe modificar el archivo **. OSD** asociado para que incluya la información adecuada sobre la arquitectura del chip y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="422ac-132">However, you must modify the associated **.osd** file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="422ac-133">Use los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="422ac-133">Use the following values.</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="422ac-134">Valor del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="422ac-134">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="422ac-135">&lt;VALOR de SO = "Win2003TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="422ac-135">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="422ac-136">&lt;VALOR de SO = "Win2003TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="422ac-136">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="422ac-137">&lt;VALOR de SO = "Win2008TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="422ac-137">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="422ac-138">&lt;VALOR de SO = "Win2008TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="422ac-138">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="422ac-139">&lt;VALOR de SO = "Win2008R2TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="422ac-139">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="422ac-140">&lt;VALOR de SO = "Win7"/&gt;</span><span class="sxs-lookup"><span data-stu-id="422ac-140">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="422ac-141">&lt;VALOR de SO = "Win764"/&gt;</span><span class="sxs-lookup"><span data-stu-id="422ac-141">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="422ac-142">&lt;VALOR de SO = "WinVista"/&gt;</span><span class="sxs-lookup"><span data-stu-id="422ac-142">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="422ac-143">&lt;VALOR de SO = "WinVista64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="422ac-143">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="422ac-144">&lt;OS VALUE = "WinXP"/&gt;</span><span class="sxs-lookup"><span data-stu-id="422ac-144">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="422ac-145">&lt;VALOR de SO = "WinXP64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="422ac-145">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="422ac-146">Para ejecutar un paquete de 32 bits recién creado, debe secuenciar la aplicación en un equipo que ejecute un sistema operativo de 32 bits con App-V 4.6 Sequencer instalado.</span><span class="sxs-lookup"><span data-stu-id="422ac-146">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V4.6 Sequencer installed.</span></span> <span data-ttu-id="422ac-147">Una vez que haya realizado la secuencia de la aplicación, en la consola del secuenciador, seleccione la pestaña **implementación** y, a continuación, especifique la arquitectura de sistema operativo y de chips adecuada según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="422ac-147">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="422ac-148">**Importante**  Las aplicaciones que se ordenan en un equipo con un sistema operativo de 64 bits se deben implementar en equipos que ejecuten un sistema operativo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="422ac-148">**Important** Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="422ac-149">Los nuevos paquetes de 32 de bits creados mediante el secuenciador de App-V 4.6 no se ejecutarán en equipos que ejecuten el cliente de App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="422ac-149">New 32-bit packages created by using the App-V4.6 Sequencer will not run on computers running the App-V 4.5 Client.</span></span>

 

<span data-ttu-id="422ac-150">Para ejecutar nuevos paquetes de 64 bits en el cliente de App-V 4.6, debe secuenciar la aplicación en un equipo que ejecute el secuenciador de App-V 4.6 y que esté ejecutando un sistema operativo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="422ac-150">To run new 64-bit packages on the App-V4.6 Client, you must sequence the application on a computer running the App-V4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="422ac-151">Una vez que haya realizado la secuencia de la aplicación, en la consola del secuenciador, seleccione la pestaña **implementación** y, a continuación, especifique la arquitectura de sistema operativo y de chips adecuada según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="422ac-151">After you have sequenced the application, in the Sequencer console, select the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="422ac-152">En la siguiente tabla se enumeran las versiones de cliente que ejecutarán los paquetes creados con las distintas versiones del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="422ac-152">The following table lists which client versions will run packages created by using the various versions of the Sequencer.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="422ac-153">Secuenciado mediante el secuenciador de aplicaciones-V 4,2</span><span class="sxs-lookup"><span data-stu-id="422ac-153">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="422ac-154">Secuenciado mediante el secuenciador de aplicaciones-V 4,5</span><span class="sxs-lookup"><span data-stu-id="422ac-154">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="422ac-155">Secuenciado mediante la aplicación de 32 bits de-V 4,6 Sequencer</span><span class="sxs-lookup"><span data-stu-id="422ac-155">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="422ac-156">Secuenciado mediante la aplicación de 64 bits de-V 4,6 Sequencer</span><span class="sxs-lookup"><span data-stu-id="422ac-156">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="422ac-157">Secuenciado mediante el secuenciador de aplicación de 32 bits-V 4,6 SP1</span><span class="sxs-lookup"><span data-stu-id="422ac-157">Sequenced by using the 32-bit App-V 4.6 SP1 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="422ac-158">Secuenciado mediante el secuenciador de aplicación de 64 bits-V 4,6 SP1</span><span class="sxs-lookup"><span data-stu-id="422ac-158">Sequenced by using the 64-bit App-V 4.6 SP1 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="422ac-159">cliente de 4,2</span><span class="sxs-lookup"><span data-stu-id="422ac-159">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-160">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-160">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-161">No</span><span class="sxs-lookup"><span data-stu-id="422ac-161">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-162">No</span><span class="sxs-lookup"><span data-stu-id="422ac-162">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-163">No</span><span class="sxs-lookup"><span data-stu-id="422ac-163">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-164">No</span><span class="sxs-lookup"><span data-stu-id="422ac-164">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-165">No</span><span class="sxs-lookup"><span data-stu-id="422ac-165">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="422ac-166">cliente de 4,5 ¹</span><span class="sxs-lookup"><span data-stu-id="422ac-166">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-167">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-167">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-168">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-168">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-169">No</span><span class="sxs-lookup"><span data-stu-id="422ac-169">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-170">No</span><span class="sxs-lookup"><span data-stu-id="422ac-170">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-171">No</span><span class="sxs-lookup"><span data-stu-id="422ac-171">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-172">No</span><span class="sxs-lookup"><span data-stu-id="422ac-172">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="422ac-173">cliente 4,6 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="422ac-173">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-174">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-174">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-175">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-175">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-176">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-176">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-177">No</span><span class="sxs-lookup"><span data-stu-id="422ac-177">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-178">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-179">No</span><span class="sxs-lookup"><span data-stu-id="422ac-179">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="422ac-180">cliente 4,6 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="422ac-180">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-181">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-181">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-182">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-182">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-183">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-184">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-185">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-185">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-186">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="422ac-187">Cliente de 4,6 SP1</span><span class="sxs-lookup"><span data-stu-id="422ac-187">4.6 SP1 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-188">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-189">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-190">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-191">No</span><span class="sxs-lookup"><span data-stu-id="422ac-191">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-192">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-192">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-193">No</span><span class="sxs-lookup"><span data-stu-id="422ac-193">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="422ac-194">Cliente de 4,6 SP1 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="422ac-194">4.6 SP1 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-195">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-196">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-196">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-197">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-197">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-198">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-198">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-199">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-199">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="422ac-200">Sí</span><span class="sxs-lookup"><span data-stu-id="422ac-200">Yes</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="422ac-201">¹ se aplica a todas las versiones del cliente de App-V 4.5, entre las que se incluyen App-V 4.5, App-V 4.5 CU1 y App-V 4.5 SP1.</span><span class="sxs-lookup"><span data-stu-id="422ac-201">¹Applies to all versions of the App-V4.5 Client, including App-V4.5, App-V4.5CU1 and App-V4.5 SP1.</span></span>

## <span data-ttu-id="422ac-202">Consideraciones de migración adicionales</span><span class="sxs-lookup"><span data-stu-id="422ac-202">Additional Migration Considerations</span></span>


<span data-ttu-id="422ac-203">Una de las características de App-V 4.5 Sequencer es la capacidad de crear archivos de Windows Installer (. msi) como puntos de control para la interoperabilidad de paquetes de aplicaciones virtuales con sistemas de distribución electrónica de software (ESD), como Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="422ac-203">One of the features of the App-V4.5 Sequencer is the ability to create Windows Installer files (.msi) as control points for virtual application package interoperability with electronic software distribution (ESD) systems such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="422ac-204">Los archivos anteriores de Windows Installer creados con la herramienta. msi para la virtualización de aplicaciones que se instalaron en un cliente de App-V 4.1 o 4.2 que posteriormente se actualizó a 4.5 seguirán funcionando, aunque no se pueden instalar en el cliente de la versión 4.5.</span><span class="sxs-lookup"><span data-stu-id="422ac-204">Previous Windows Installer files created with the .msi tool for Application Virtualization that were installed on a App-V4.1 or4.2 Client that is subsequently upgraded to4.5 continue to work, although they cannot be installed on the4.5 Client.</span></span> <span data-ttu-id="422ac-205">Sin embargo, no se pueden quitar ni actualizar, a menos que se actualicen en el secuenciador de la versión 4.5.</span><span class="sxs-lookup"><span data-stu-id="422ac-205">However, they cannot be removed or upgraded unless they are upgraded in the4.5 Sequencer.</span></span> <span data-ttu-id="422ac-206">El paquete de la aplicación virtual original anterior a la 4,5 tendría que estar abierto en el secuenciador de la versión 4.5 y, después, guardado como un archivo de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="422ac-206">The original pre-4.5 virtual application package would need to be opened in the4.5 Sequencer and then saved as a Windows Installer File.</span></span>

<span data-ttu-id="422ac-207">**Nota:**  Si el cliente de App-V 4.2 ya se ha actualizado a la versión 4.5, es posible usar el script como solución alternativa para preservar los paquetes 4.2 en los clientes de la versión 4.5 y permitir que sean administrados.</span><span class="sxs-lookup"><span data-stu-id="422ac-207">**Note** If the App-V4.2 Client has already been upgraded to4.5, it is possible to use script as a workaround to preserve the4.2 packages on4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="422ac-208">Este script debe copiar dos archivos, msvcp71.dll y msvcr71.dll, a la carpeta de instalación de App-V y establecer los siguientes valores de clave del registro en la clave del registro \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span><span class="sxs-lookup"><span data-stu-id="422ac-208">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key \[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

<span data-ttu-id="422ac-209">"ClientVersion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="422ac-209">"ClientVersion"="4.2.1.20"</span></span>

<span data-ttu-id="422ac-210">"GlobalDataDirectory" = "C:\\\\Documents y Settings\\\\All Users\\\\Documents\\\\" (una ubicación de escritura global)</span><span class="sxs-lookup"><span data-stu-id="422ac-210">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>

 

<span data-ttu-id="422ac-211">Los archivos de Windows Installer generados por el secuenciador de App-V 4,5 muestran el mensaje de error "este paquete requiere el cliente de Microsoft Application Virtualization 4,5 o posterior" cuando intenta ejecutarlo en un cliente de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="422ac-211">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when you try to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="422ac-212">Abra el paquete antiguo con el secuenciador de App-V 4,5 SP1 o el secuenciador de App-V 4,6 y genere un nuevo. msi para el paquete.</span><span class="sxs-lookup"><span data-stu-id="422ac-212">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi for the package.</span></span>

<span data-ttu-id="422ac-213">Cualquier informe 4.2 que se haya creado y guardado se sobrescribirá cuando el servidor se actualice a la versión 4.5.</span><span class="sxs-lookup"><span data-stu-id="422ac-213">Any4.2 reports that were created and saved will be overwritten when the server is upgraded to4.5.</span></span> <span data-ttu-id="422ac-214">Si necesita conservar estos informes, debe guardar una copia de seguridad del archivo SftMMC. msc que se encuentra en la carpeta de la consola de administración de SoftGrid en el servidor y usar esa copia para reemplazar el nuevo SftMMC. msc instalado durante la actualización.</span><span class="sxs-lookup"><span data-stu-id="422ac-214">If you need to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

<span data-ttu-id="422ac-215">Para obtener más información sobre la actualización de versiones anteriores, vea [actualizar a Microsoft Application virtualization 4,5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="422ac-215">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <span data-ttu-id="422ac-216">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="422ac-216">Related topics</span></span>


[<span data-ttu-id="422ac-217">Planificación de la implementación del sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="422ac-217">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





