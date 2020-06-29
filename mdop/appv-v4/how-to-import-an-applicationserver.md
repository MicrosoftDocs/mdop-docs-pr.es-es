---
title: Cómo importar una aplicación
description: Cómo importar una aplicación
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817401"
---
# <span data-ttu-id="5d52d-103">Cómo importar una aplicación</span><span class="sxs-lookup"><span data-stu-id="5d52d-103">How to Import an Application</span></span>


<span data-ttu-id="5d52d-104">Normalmente, las aplicaciones se importan para que estén disponibles para transmitirlas desde un servidor de administración de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5d52d-104">Typically, you import applications to make them available to stream from an Application Virtualization Management Server.</span></span> <span data-ttu-id="5d52d-105">También puede Agregar una aplicación de forma manual, pero debe proporcionar información precisa y detallada sobre la aplicación para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="5d52d-105">You can also add an application manually, but you must provide precise, detailed information about the application to do so.</span></span> <span data-ttu-id="5d52d-106">Para obtener más información, consulte [Cómo agregar una aplicación de forma manual](how-to-manually-add-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="5d52d-106">For more information, see [How to Manually Add an Application](how-to-manually-add-an-application.md).</span></span>

<span data-ttu-id="5d52d-107">**Nota:**  Para importar una aplicación, debe tener su archivo de descriptor de software abierto (OSD) secuencial o archivo SPRJ (SPRJ) disponible en el servidor.</span><span class="sxs-lookup"><span data-stu-id="5d52d-107">**Note** To import an application, you must have its sequenced Open Software Descriptor (OSD) file or its Sequencer Project (SPRJ) file available on the server.</span></span>

 

<span data-ttu-id="5d52d-108">Al importar una aplicación, debe asegurarse de que el servidor está configurado con un valor en el campo **ruta de contenido predeterminada** en la pestaña **General** del cuadro de diálogo **Opciones del sistema** (accesible haciendo clic con el botón derecho en el nodo **del sistema de virtualización de aplicaciones** en la consola de servidor de App-V).</span><span class="sxs-lookup"><span data-stu-id="5d52d-108">When importing an application, you should make sure the server is configured with a value in the **Default Content Path** field on the **General** tab of the **System Options** dialog (accessible by right-clicking the **Application Virtualization System** node in the App-V Server Console).</span></span> <span data-ttu-id="5d52d-109">El valor predeterminado de la ruta de contenido define dónde se importarán las aplicaciones y, durante el proceso de importación, este valor se usa para modificar las rutas definidas en el archivo de OSD para el archivo SFT y los accesos directos del icono.</span><span class="sxs-lookup"><span data-stu-id="5d52d-109">The default content path value defines where the applications will be imported, and during the import process, this value is used to modify the paths defined in the OSD file for the SFT file and for the icon shortcuts.</span></span> <span data-ttu-id="5d52d-110">En el archivo OSD, la ruta de acceso para el archivo SFT se especifica en la entrada HREF del código base y la ruta de los iconos se especifica en la entrada ACCESOs directos.</span><span class="sxs-lookup"><span data-stu-id="5d52d-110">In the OSD file, the path for the SFT file is specified in the CODEBASE HREF entry and the path for the icons is specified in the SHORTCUTS entry.</span></span>

<span data-ttu-id="5d52d-111">Durante el proceso de importación, el protocolo, el servidor y, si está presente, el puerto especificado en estas dos rutas en el archivo OSD se reemplazarán por el valor de la ruta de contenido predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5d52d-111">During the import process, the protocol, server, and, if present, port specified in these two paths in the OSD file will be replaced with the value from the default content path.</span></span> <span data-ttu-id="5d52d-112">En la tabla siguiente se muestra un ejemplo de cómo se verá afectada la ruta de acceso a la importación.</span><span class="sxs-lookup"><span data-stu-id="5d52d-112">The following table provides an example of how the import path will be affected.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="5d52d-113">Ruta de contenido predeterminada</span><span class="sxs-lookup"><span data-stu-id="5d52d-113">Default Content Path</span></span></th>
<th align="left"><span data-ttu-id="5d52d-114">CÓDIGO base de archivo OSD HREF</span><span class="sxs-lookup"><span data-stu-id="5d52d-114">OSD File CODEBASE HREF</span></span></th>
<th align="left"><span data-ttu-id="5d52d-115">Valor resultante</span><span class="sxs-lookup"><span data-stu-id="5d52d-115">Resulting Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="5d52d-116">\server\content &lt; /p&gt;</span><span class="sxs-lookup"><span data-stu-id="5d52d-116">\server\content&lt;/p&gt;</span></span></td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p><span data-ttu-id="5d52d-117">\server\content\myFolder\package.sft</span><span class="sxs-lookup"><span data-stu-id="5d52d-117">\server\content\myFolder\package.sft</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="5d52d-118">Para importar una aplicación</span><span class="sxs-lookup"><span data-stu-id="5d52d-118">To import an application</span></span>**

1.  <span data-ttu-id="5d52d-119">Haga clic con el botón derecho en el nodo **aplicaciones** en el panel izquierdo y seleccione **importar aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="5d52d-119">Right-click the **Applications** node in the left pane, and choose **Import Applications**.</span></span>

2.  <span data-ttu-id="5d52d-120">En el cuadro de diálogo **abrir** , vaya al archivo SPRJ o OSD de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d52d-120">In the **Open** dialog box, navigate to the application's SPRJ or OSD file.</span></span> <span data-ttu-id="5d52d-121">Resalte el archivo y haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="5d52d-121">Highlight the file and click **Open**.</span></span>

3.  <span data-ttu-id="5d52d-122">En el **Asistente para nueva aplicación**, asegúrese de que el cuadro **habilitado** está seleccionado para las aplicaciones que desea transmitir.</span><span class="sxs-lookup"><span data-stu-id="5d52d-122">In the **New Application Wizard**, be sure the **Enabled** box is selected for applications you want to stream.</span></span> <span data-ttu-id="5d52d-123">También puede escribir una descripción y comprobar las rutas de archivo y el servidor.</span><span class="sxs-lookup"><span data-stu-id="5d52d-123">There you can also enter a description and verify the server and file paths.</span></span> <span data-ttu-id="5d52d-124">Además, si ha configurado las licencias y los grupos de servidores, puede seleccionarlos.</span><span class="sxs-lookup"><span data-stu-id="5d52d-124">Also, if you have set up license and server groups, you can select those.</span></span>

4.  <span data-ttu-id="5d52d-125">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5d52d-125">Click **Next**.</span></span>

5.  <span data-ttu-id="5d52d-126">En la pantalla **accesos directos publicados** , seleccione las casillas de las ubicaciones en las que desea que aparezcan los accesos directos de la aplicación en los equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="5d52d-126">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers.</span></span>

6.  <span data-ttu-id="5d52d-127">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5d52d-127">Click **Next**.</span></span>

7.  <span data-ttu-id="5d52d-128">En la pantalla **asociaciones de archivos** , puede agregar nuevas asociaciones de archivo a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="5d52d-128">In the **File Associations** screen, you can add new file associations to this application.</span></span> <span data-ttu-id="5d52d-129">Para ello, haga clic en **Agregar**, escriba la extensión (sin un punto anterior), escriba una descripción y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5d52d-129">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

    <span data-ttu-id="5d52d-130">**Nota:**  Las aplicaciones que se ordenan con el secuenciador 4,0 rellenan el cuadro de diálogo **asociaciones de archivos** al importarlas o crearlas a través de la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="5d52d-130">**Note** Applications sequenced with Sequencer 4.0 populate the **File Associations** dialog box when you import or create them through the management console.</span></span> <span data-ttu-id="5d52d-131">Las aplicaciones con paquetes de versiones de Sequencer anteriores no.</span><span class="sxs-lookup"><span data-stu-id="5d52d-131">Applications with previous Sequencer version packages do not.</span></span>

     

8.  <span data-ttu-id="5d52d-132">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5d52d-132">Click **Next**.</span></span>

9.  <span data-ttu-id="5d52d-133">En la pantalla **permisos de acceso** , haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="5d52d-133">In the **Access Permissions** screen, click **Add**.</span></span>

10. <span data-ttu-id="5d52d-134">Complete el cuadro de diálogo **seleccionar grupos** .</span><span class="sxs-lookup"><span data-stu-id="5d52d-134">Complete the **Select Groups** dialog box.</span></span> <span data-ttu-id="5d52d-135">Cuando termine, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="5d52d-135">When you finish, click **OK**.</span></span>

11. <span data-ttu-id="5d52d-136">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="5d52d-136">Click **Next**.</span></span>

12. <span data-ttu-id="5d52d-137">En la pantalla **Resumen** , puede revisar la configuración de importación.</span><span class="sxs-lookup"><span data-stu-id="5d52d-137">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="5d52d-138">Haga clic en **Finalizar**, o haga clic en **atrás** para cambiar la importación o haga clic en **Cancelar** para cancelar la importación.</span><span class="sxs-lookup"><span data-stu-id="5d52d-138">Click **Finish**, or click **Back** to change the import or click **Cancel** to cancel the import.</span></span>

## <span data-ttu-id="5d52d-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d52d-139">Related topics</span></span>


[<span data-ttu-id="5d52d-140">Cómo administrar grupos de aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="5d52d-140">How to Manage Application Groups in the Server Management Console</span></span>](how-to-manage-application-groups-in-the-server-management-console.md)

[<span data-ttu-id="5d52d-141">Cómo administrar aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="5d52d-141">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

[<span data-ttu-id="5d52d-142">Cómo agregar manualmente una aplicación</span><span class="sxs-lookup"><span data-stu-id="5d52d-142">How to Manually Add an Application</span></span>](how-to-manually-add-an-application.md)

 

 





