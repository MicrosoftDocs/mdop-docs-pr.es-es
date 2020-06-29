---
title: Lista de comprobación de actualización de App-V
description: Lista de comprobación de actualización de App-V
author: dansimp
ms.assetid: 64e317d2-d260-4b67-8a49-ba9ac513087a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad856ce3067c327f3e604f9269ee384a66a1675a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819740"
---
# <span data-ttu-id="90799-103">Lista de comprobación de actualización de App-V</span><span class="sxs-lookup"><span data-stu-id="90799-103">App-V Upgrade Checklist</span></span>


<span data-ttu-id="90799-104">Antes de intentar actualizar a Microsoft Application Virtualization (App-V) 4,5 o versiones posteriores, cualquier versión anterior a App-V 4,1 debe actualizarse a App-V 4,1.</span><span class="sxs-lookup"><span data-stu-id="90799-104">Before trying to upgrade to Microsoft Application Virtualization (App-V) 4.5 or later versions, any version earlier than App-V 4.1 must be upgraded to App-V 4.1.</span></span> <span data-ttu-id="90799-105">Debe planear la actualización de los clientes en primer lugar y, a continuación, actualizar los componentes del servidor.</span><span class="sxs-lookup"><span data-stu-id="90799-105">You should plan to upgrade clients first, and then upgrade the server components.</span></span> <span data-ttu-id="90799-106">Los clientes de App-V que se han actualizado a App-V 4,5 siguen trabajando con servidores de App-V que aún no se han actualizado.</span><span class="sxs-lookup"><span data-stu-id="90799-106">App-V clients that have been upgraded to App-V 4.5 continue to work with App-V servers that have not yet been upgraded.</span></span> <span data-ttu-id="90799-107">Las versiones anteriores del cliente no son compatibles con los servidores que se han actualizado a App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="90799-107">Earlier versions of the client are not supported on servers that have been upgraded to App-V 4.5.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="90799-108">Paso</span><span class="sxs-lookup"><span data-stu-id="90799-108">Step</span></span></th>
<th align="left"><span data-ttu-id="90799-109">Referencia</span><span class="sxs-lookup"><span data-stu-id="90799-109">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90799-110">Actualice los clientes de App-V.</span><span class="sxs-lookup"><span data-stu-id="90799-110">Upgrade the App-V clients.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-client.md" data-raw-source="[How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)"><span data-ttu-id="90799-111">Cómo actualizar el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="90799-111">How to Upgrade the Application Virtualization Client</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="90799-112">Actualice los servidores y la base de datos de App-V.</span><span class="sxs-lookup"><span data-stu-id="90799-112">Upgrade the App-V servers and database.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="90799-113">Importante</span><span class="sxs-lookup"><span data-stu-id="90799-113">Important</span></span></strong><br/><p><span data-ttu-id="90799-114">Si tiene más de un servidor que comparte el acceso a la base de datos de App-V, todos los servidores deben estar desconectados mientras la base de datos se está actualizando.</span><span class="sxs-lookup"><span data-stu-id="90799-114">If you have more than one server sharing access to the App-V database, all those servers must be taken offline while the database is being upgraded.</span></span> <span data-ttu-id="90799-115">Debe seguir sus prácticas habituales de negocios para la actualización de la base de datos, pero le recomendamos que pruebe la actualización de la base de datos con una copia de seguridad de la base de datos en primer lugar en un servidor de prueba.</span><span class="sxs-lookup"><span data-stu-id="90799-115">You should follow your regular business practices for the database upgrade, but we recommend that you test the database upgrade by using a backup copy of the database first on a test server.</span></span> <span data-ttu-id="90799-116">Después, seleccione uno de los servidores para la primera actualización, que actualizará el esquema de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="90799-116">Then, you should select one of the servers for the first upgrade, which will upgrade the database schema.</span></span> <span data-ttu-id="90799-117">Una vez que la base de datos de producción se ha actualizado correctamente, puede actualizar el software de App-V en los otros servidores.</span><span class="sxs-lookup"><span data-stu-id="90799-117">After the production database has been successfully upgraded, you can upgrade the App-V software on the other servers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="90799-118">Cómo actualizar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="90799-118">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90799-119">Actualice el servicio Web de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="90799-119">Upgrade the App-V Management Web Service.</span></span></p>
<p><span data-ttu-id="90799-120">Este paso solo se aplica si el servicio Web de administración está en un servidor independiente, lo que requiere que ejecute el programa de instalación del servidor en ese servidor independiente para actualizar el servicio Web de administración.</span><span class="sxs-lookup"><span data-stu-id="90799-120">This step applies only if the Management Web Service is on a separate server, which would require that you run the server installer program on that separate server to upgrade the Management Web service.</span></span> <span data-ttu-id="90799-121">De lo contrario, el paso de actualización del servidor anterior actualizará automáticamente el servicio Web de administración.</span><span class="sxs-lookup"><span data-stu-id="90799-121">Otherwise, the previous server upgrade step will automatically upgrade the Management Web Service.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="90799-122">Cómo actualizar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="90799-122">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="90799-123">Actualice la consola de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="90799-123">Upgrade the App-V Management Console.</span></span></p>
<p><span data-ttu-id="90799-124">Este paso solo se aplica si la consola de administración está en un equipo independiente, lo que requiere que ejecute el programa de instalación de servidor en ese equipo diferente para actualizar la consola.</span><span class="sxs-lookup"><span data-stu-id="90799-124">This step applies only if the Management Console is on a separate computer, which would require that you run the server installer program on that separate computer to upgrade the console.</span></span> <span data-ttu-id="90799-125">De lo contrario, el paso de actualización del servidor anterior actualizará la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="90799-125">Otherwise, the previous server upgrade step will upgrade the Management Console.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)"><span data-ttu-id="90799-126">Cómo actualizar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="90799-126">How to Upgrade the Servers and System Components</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90799-127">Actualice el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="90799-127">Upgrade the App-V Sequencer.</span></span></p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-sequencer.md" data-raw-source="[How to Upgrade the Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)"><span data-ttu-id="90799-128">Cómo actualizar el cliente secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="90799-128">How to Upgrade the Application Virtualization Sequencer</span></span></a></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="90799-129">Consideraciones de actualización adicionales</span><span class="sxs-lookup"><span data-stu-id="90799-129">Additional Upgrade Considerations</span></span>


-   <span data-ttu-id="90799-130">Los paquetes de aplicaciones virtuales de la versión 4,2 no tendrán que volver a secuenciarse para usarlos con la versión 4,5.</span><span class="sxs-lookup"><span data-stu-id="90799-130">Any virtual application packages sequenced in version 4.2 will not have to be sequenced again for use with version 4.5.</span></span> <span data-ttu-id="90799-131">Sin embargo, considere la posibilidad de actualizar los paquetes virtuales al formato de Microsoft Application Virtualization 4,5 Si desea aplicar listas de control de acceso (ACL) predeterminadas o generar un archivo de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="90799-131">However, you should consider upgrading the virtual packages to the Microsoft Application Virtualization 4.5 format if you want to apply default access control lists (ACLs) or generate a Windows Installer file.</span></span> <span data-ttu-id="90799-132">Este es un proceso sencillo y solo requiere que el paquete de la aplicación virtual existente se abra y se guarde con el secuenciador App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="90799-132">This is a simple process and requires only that the existing virtual application package be opened and saved with the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="90799-133">Esto se puede automatizar mediante la interfaz de línea de comandos App-VSequencer.</span><span class="sxs-lookup"><span data-stu-id="90799-133">This can be automated by using the App-VSequencer command-line interface.</span></span> <span data-ttu-id="90799-134">Para obtener más información, vea [Cómo crear o actualizar aplicaciones virtuales con el secuenciador de App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)</span><span class="sxs-lookup"><span data-stu-id="90799-134">For more information, see [How to Create or Upgrade Virtual Applications Using the App-V Sequencer](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)</span></span>

-   <span data-ttu-id="90799-135">Una de las características de la 4,5 secuenciador es la capacidad de crear archivos de Windows Installer (. msi) como puntos de control para la interoperabilidad de paquetes de aplicaciones virtuales con sistemas ESD (Electronic Software Distribution), como Microsoft Endpoint Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="90799-135">One of the features of the 4.5 Sequencer is the ability to create Windows Installer (.msi) files as control points for virtual application package interoperability with electronic software distribution (ESD) systems, such as Microsoft Endpoint Configuration Manager.</span></span> <span data-ttu-id="90799-136">Los archivos anteriores de Windows Installer creados con la herramienta MSI para virtualización de aplicaciones que se instalaron en un cliente de App-V 4,1 o 4,2 que se actualiza posteriormente a App-V 4,5 seguirán funcionando, aunque no se pueden instalar en el cliente de App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="90799-136">Previous Windows Installer files created with the MSI tool for Application Virtualization that were installed on a App-V 4.1 or 4.2 client that is subsequently upgraded to App-V 4.5 will continue to work, although they cannot be installed on the App-V 4.5 client.</span></span> <span data-ttu-id="90799-137">Sin embargo, no se pueden quitar ni actualizar, a menos que se actualicen en el secuenciador de aplicaciones-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="90799-137">However, they cannot be removed or upgraded unless they are upgraded in the App-V 4.5 Sequencer.</span></span> <span data-ttu-id="90799-138">El paquete de App-V original anterior a 4,5 debe abrirse en el secuenciador de App-V 4,5 y, a continuación, se puede guardar como un archivo de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="90799-138">The original App-V package earlier than 4.5 has to be opened in the App-V 4.5 Sequencer and then saved as a Windows Installer File.</span></span>

    **<span data-ttu-id="90799-139">Nota</span><span class="sxs-lookup"><span data-stu-id="90799-139">Note</span></span>**  
    <span data-ttu-id="90799-140">Si el cliente de App-V 4,2 ya se ha actualizado a App-V 4,5, se puede incluir una solución alternativa para conservar los paquetes de la versión 4,2 en los clientes con la versión 4,5 y permitir que se administren.</span><span class="sxs-lookup"><span data-stu-id="90799-140">If the App-V 4.2 Client has already been upgraded to App-V 4.5, it is possible to script a workaround to preserve the version 4.2 packages on version 4.5 clients and allow them to be managed.</span></span> <span data-ttu-id="90799-141">Este script debe copiar dos archivos, msvcp71.dll y msvcr71.dll, a la carpeta de instalación de App-V y establecer los siguientes valores de clave del registro en la clave del registro: \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span><span class="sxs-lookup"><span data-stu-id="90799-141">This script must copy two files, msvcp71.dll and msvcr71.dll, to the App-V installation folder and set the following registry key values under the registry key:\[HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:</span></span>

    <span data-ttu-id="90799-142">"ClientVersion" = "4.2.1.20"</span><span class="sxs-lookup"><span data-stu-id="90799-142">"ClientVersion"="4.2.1.20"</span></span>

    <span data-ttu-id="90799-143">"GlobalDataDirectory" = "C:\\\\Documents y Settings\\\\All Users\\\\Documents\\\\" (una ubicación de escritura global)</span><span class="sxs-lookup"><span data-stu-id="90799-143">"GlobalDataDirectory"="C:\\\\Documents and Settings\\\\All Users\\\\Documents\\\\" (a globally writeable location)</span></span>



-   <span data-ttu-id="90799-144">Los archivos de Windows Installer generados por el secuenciador de App-V 4,5 muestran el mensaje de error "este paquete requiere el cliente de Microsoft Application Virtualization 4,5 o posterior" al intentar ejecutarlo en un cliente de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="90799-144">Windows Installer files generated by the App-V 4.5 Sequencer display the error message "This package requires Microsoft Application Virtualization Client 4.5 or later" when trying to run them on an App-V 4.6 Client.</span></span> <span data-ttu-id="90799-145">Abra el paquete antiguo con el secuenciador de App-V 4,5 SP1 o el secuenciador de App-V 4,6 y genere un nuevo archivo. msi para el paquete.</span><span class="sxs-lookup"><span data-stu-id="90799-145">Open the old package with either the App-V 4.5 SP1 Sequencer or the App-V 4.6 Sequencer and generate a new .msi file for the package.</span></span>

-   <span data-ttu-id="90799-146">Los informes de la versión 4,2 que se crearon y guardaron se sobrescribirán cuando el servidor se actualice a la versión 4,5.</span><span class="sxs-lookup"><span data-stu-id="90799-146">Any version 4.2 reports that were created and saved will be overwritten when the server is upgraded to version 4.5.</span></span> <span data-ttu-id="90799-147">Si tiene que mantener estos informes, debe guardar una copia de seguridad del archivo SftMMC. msc que se encuentra en la carpeta de la consola de administración de SoftGrid en el servidor y usar esa copia para reemplazar el nuevo SftMMC. msc instalado durante la actualización.</span><span class="sxs-lookup"><span data-stu-id="90799-147">If you have to keep these reports, you must save a backup copy of the SftMMC.msc file located in the SoftGrid Management Console folder on the server and use that copy to replace the new SftMMC.msc that is installed during the upgrade.</span></span>

-   <span data-ttu-id="90799-148">Para obtener más información sobre la actualización de versiones anteriores, vea [actualizar a Microsoft Application virtualization 4,5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .</span><span class="sxs-lookup"><span data-stu-id="90799-148">For additional information about upgrading from previous versions, see [Upgrading to Microsoft Application Virtualization 4.5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) (https://go.microsoft.com/fwlink/?LinkId=120358).</span></span>

## <a href="" id="app-v-4-6-client-package-support-"></a><span data-ttu-id="90799-149">Compatibilidad con paquetes de cliente de App-V 4,6</span><span class="sxs-lookup"><span data-stu-id="90799-149">App-V 4.6 Client Package Support</span></span>


<span data-ttu-id="90799-150">Puede implementar paquetes creados en versiones anteriores de App-V para los clientes de App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="90799-150">You can deploy packages created in previous versions of App-V to App-V 4.6 clients.</span></span> <span data-ttu-id="90799-151">Sin embargo, debe modificar el archivo. OSD asociado para que incluya la información adecuada sobre la arquitectura del chip y el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="90799-151">However, you must modify the associated .osd file so that it includes the appropriate operating system and chip architecture information.</span></span> <span data-ttu-id="90799-152">Se pueden usar los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="90799-152">The following values can be used:</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="90799-153">Valor del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="90799-153">OS Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90799-154">&lt;VALOR de SO = "Win2003TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="90799-154">&lt;OS VALUE=”Win2003TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="90799-155">&lt;VALOR de SO = "Win2003TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="90799-155">&lt;OS VALUE=”Win2003TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90799-156">&lt;VALOR de SO = "Win2008TS"/&gt;</span><span class="sxs-lookup"><span data-stu-id="90799-156">&lt;OS VALUE=”Win2008TS”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="90799-157">&lt;VALOR de SO = "Win2008TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="90799-157">&lt;OS VALUE=”Win2008TS64”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90799-158">&lt;VALOR de SO = "Win2008R2TS64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="90799-158">&lt;OS VALUE=”Win2008R2TS64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="90799-159">&lt;VALOR de SO = "Win7"/&gt;</span><span class="sxs-lookup"><span data-stu-id="90799-159">&lt;OS VALUE=”Win7”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90799-160">&lt;VALOR de SO = "Win764"/&gt;</span><span class="sxs-lookup"><span data-stu-id="90799-160">&lt;OS VALUE=”Win764”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="90799-161">&lt;VALOR de SO = "WinVista"/&gt;</span><span class="sxs-lookup"><span data-stu-id="90799-161">&lt;OS VALUE=”WinVista”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90799-162">&lt;VALOR de SO = "WinVista64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="90799-162">&lt;OS VALUE=”WinVista64”/&gt;</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="90799-163">&lt;OS VALUE = "WinXP"/&gt;</span><span class="sxs-lookup"><span data-stu-id="90799-163">&lt;OS VALUE=”WinXP”/&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90799-164">&lt;VALOR de SO = "WinXP64"/&gt;</span><span class="sxs-lookup"><span data-stu-id="90799-164">&lt;OS VALUE=”WinXP64”/&gt;</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="90799-165">Para ejecutar un paquete de 32 bits recién creado, debe secuenciar la aplicación en un equipo que ejecute un sistema operativo de 32 bits con App-V 4,6 Sequencer instalado.</span><span class="sxs-lookup"><span data-stu-id="90799-165">To run a newly created 32-bit package, you must sequence the application on a computer running a 32-bit operating system with the App-V 4.6 Sequencer installed.</span></span> <span data-ttu-id="90799-166">Una vez que haya realizado la secuencia de la aplicación, en la consola del secuenciador, haga clic en la pestaña **implementación** y especifique la arquitectura de chip y sistema operativo adecuado según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="90799-166">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab and then specify the appropriate operating system and chip architecture as required.</span></span>

**<span data-ttu-id="90799-167">Importante</span><span class="sxs-lookup"><span data-stu-id="90799-167">Important</span></span>**  
<span data-ttu-id="90799-168">Las aplicaciones que se ordenan en un equipo con un sistema operativo de 64 bits se deben implementar en equipos que ejecuten un sistema operativo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="90799-168">Applications sequenced on a computer running a 64-bit operating system must be deployed to computers running a 64-bit operating system.</span></span> <span data-ttu-id="90799-169">Los nuevos paquetes de 32 bits creados mediante el secuenciador de App-V 4,6 no se ejecutan en equipos que ejecutan el cliente de App-V 4,5.</span><span class="sxs-lookup"><span data-stu-id="90799-169">New 32-bit packages created by using the App-V 4.6 Sequencer do not run on computers running the App-V 4.5 client.</span></span>



<span data-ttu-id="90799-170">Para ejecutar nuevos paquetes de 64 bits en el cliente de App-V 4,6, debe secuenciar la aplicación en un equipo que ejecute el secuenciador de App-V 4,6 y que esté ejecutando un sistema operativo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="90799-170">To run new 64-bit packages on the App-V 4.6 Client, you must sequence the application on a computer running the App-V 4.6 Sequencer and that is running a 64-bit operating system.</span></span> <span data-ttu-id="90799-171">Una vez que haya realizado la secuencia de la aplicación, en la consola secuenciador, haga clic en la pestaña **implementación** y especifique la arquitectura de sistema operativo y de chips adecuada según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="90799-171">After you have sequenced the application, in the Sequencer console, click the **Deployment** tab, and then specify the appropriate operating system and chip architecture as required.</span></span>

<span data-ttu-id="90799-172">En la siguiente tabla se enumeran las versiones de cliente que ejecutarán los paquetes creados con las distintas versiones del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="90799-172">The following table lists which client versions will run packages created by using the various versions of the sequencer.</span></span>

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left"><span data-ttu-id="90799-173">Secuenciado mediante el secuenciador de aplicaciones-V 4,2</span><span class="sxs-lookup"><span data-stu-id="90799-173">Sequenced by using the App-V 4.2 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="90799-174">Secuenciado mediante el secuenciador de aplicaciones-V 4,5</span><span class="sxs-lookup"><span data-stu-id="90799-174">Sequenced by using the App-V 4.5 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="90799-175">Secuenciado mediante la aplicación de 32 bits de-V 4,6 Sequencer</span><span class="sxs-lookup"><span data-stu-id="90799-175">Sequenced by using the 32-bit App-V 4.6 Sequencer</span></span></th>
<th align="left"><span data-ttu-id="90799-176">Secuenciado mediante la aplicación de 64 bits de-V 4,6 Sequencer</span><span class="sxs-lookup"><span data-stu-id="90799-176">Sequenced by using the 64-bit App-V 4.6 Sequencer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90799-177">cliente de 4,2</span><span class="sxs-lookup"><span data-stu-id="90799-177">4.2 Client</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-178">Sí</span><span class="sxs-lookup"><span data-stu-id="90799-178">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-179">No</span><span class="sxs-lookup"><span data-stu-id="90799-179">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-180">No</span><span class="sxs-lookup"><span data-stu-id="90799-180">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-181">No</span><span class="sxs-lookup"><span data-stu-id="90799-181">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="90799-182">cliente de 4,5 ¹</span><span class="sxs-lookup"><span data-stu-id="90799-182">4.5 Client ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-183">Sí</span><span class="sxs-lookup"><span data-stu-id="90799-183">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-184">Sí</span><span class="sxs-lookup"><span data-stu-id="90799-184">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-185">No</span><span class="sxs-lookup"><span data-stu-id="90799-185">No</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-186">No</span><span class="sxs-lookup"><span data-stu-id="90799-186">No</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="90799-187">cliente 4,6 (32 bits)</span><span class="sxs-lookup"><span data-stu-id="90799-187">4.6 Client (32-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-188">Sí</span><span class="sxs-lookup"><span data-stu-id="90799-188">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-189">Sí</span><span class="sxs-lookup"><span data-stu-id="90799-189">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-190">Sí</span><span class="sxs-lookup"><span data-stu-id="90799-190">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-191">No</span><span class="sxs-lookup"><span data-stu-id="90799-191">No</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="90799-192">cliente 4,6 (64 bits)</span><span class="sxs-lookup"><span data-stu-id="90799-192">4.6 Client (64-bit)</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-193">Sí</span><span class="sxs-lookup"><span data-stu-id="90799-193">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-194">Sí</span><span class="sxs-lookup"><span data-stu-id="90799-194">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-195">Sí</span><span class="sxs-lookup"><span data-stu-id="90799-195">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="90799-196">Sí</span><span class="sxs-lookup"><span data-stu-id="90799-196">Yes</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="90799-197">¹ se aplica a todas las versiones del cliente de App-V 4,5, entre las que se incluyen App-V 4,5, App-V 4,5 CU1 y App-V 4,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="90799-197">¹Applies to all versions of the App-V 4.5 client, including App-V 4.5, App-V 4.5 CU1, and App-V 4.5 SP1.</span></span>









