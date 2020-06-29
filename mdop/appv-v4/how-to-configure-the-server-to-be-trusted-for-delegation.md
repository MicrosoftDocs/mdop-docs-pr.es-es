---
title: Cómo configurar el servidor para que sea de confianza para delegación
description: Cómo configurar el servidor para que sea de confianza para delegación
author: dansimp
ms.assetid: d8d11588-17c0-4bcb-a7e6-86b5e4ba7e1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7164b3046671853216b870d68e651fed4fd84695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817750"
---
# <span data-ttu-id="db204-103">Cómo configurar el servidor para que sea de confianza para delegación</span><span class="sxs-lookup"><span data-stu-id="db204-103">How to Configure the Server to be Trusted for Delegation</span></span>


<span data-ttu-id="db204-104">Al instalar el software servidor de administración de Microsoft Application Virtualization (App-V), puede elegir instalarlo mediante una arquitectura de sistema distribuido.</span><span class="sxs-lookup"><span data-stu-id="db204-104">When you install the Microsoft Application Virtualization (App-V) Management Server software, you can choose to install it by using a distributed system architecture.</span></span> <span data-ttu-id="db204-105">Si instala la consola, el servicio Web de administración y la base de datos en diferentes equipos, debe configurar el servidor de Internet Information Services (IIS) para que sea de confianza para la delegación.</span><span class="sxs-lookup"><span data-stu-id="db204-105">If you install the console, the Management Web Service, and the database on different computers, you must configure the Internet Information Services (IIS) server to be trusted for delegation.</span></span> <span data-ttu-id="db204-106">Esto es necesario porque el servicio Web de administración intentará conectar con el almacén de datos de App-V usando las credenciales del administrador de App-V que usa la consola.</span><span class="sxs-lookup"><span data-stu-id="db204-106">This is necessary because the Management Web Service will attempt to connect to the App-V data store by using the credentials of the App-V administrator who is using the console.</span></span> <span data-ttu-id="db204-107">El servidor de base de datos en el que está instalado el almacén de datos no aceptará las credenciales del administrador del servidor IIS a menos que el servidor IIS esté configurado para ser de confianza para la delegación, por lo que el servicio Web de administración no podrá conectarse al almacén de datos de App-V.</span><span class="sxs-lookup"><span data-stu-id="db204-107">The database server on which the data store is installed will not accept the administrator’s credentials from the IIS server unless the IIS server is configured to be trusted for delegation, and so the Management Web Service will not be able to connect to the App-V data store.</span></span>

<span data-ttu-id="db204-108">**Nota:**  Si instala el software de servidor de administración de App-V en un solo servidor y coloca el almacén de datos en un servidor independiente, hay una situación en la que debe configurar el servidor para que sea de confianza para la delegación, aunque el servicio Web de administración y la consola de administración estén en el mismo servidor.</span><span class="sxs-lookup"><span data-stu-id="db204-108">**Note** If you install the App-V Management Server software on a single server and place the data store on a separate server, there is one situation in which you must still configure the server to be trusted for delegation even though the Management Web Service and Management Console are on the same server.</span></span> <span data-ttu-id="db204-109">Esta situación se produce si necesita conectarse al servicio Web de administración en la consola con la opción **usar credenciales alternativas** .</span><span class="sxs-lookup"><span data-stu-id="db204-109">This situation occurs if you need to connect to the Management Web Service in the console by using the **Use Alternate Credentials** option.</span></span>

 

<span data-ttu-id="db204-110">El tipo de delegación que puede usar depende del nivel funcional del dominio que haya configurado en la infraestructura de los servicios de dominio de Active Directory (ADDS).</span><span class="sxs-lookup"><span data-stu-id="db204-110">The type of delegation that you can use depends on the Domain Functional Level that you have configured in your Active Directory Domain Services (ADDS) infrastructure.</span></span> <span data-ttu-id="db204-111">En la siguiente tabla se enumeran los tipos de delegación que se pueden configurar para cada nivel funcional de dominio de App-V.</span><span class="sxs-lookup"><span data-stu-id="db204-111">The following table lists the types of delegation that can be configured for each Domain Functional Level for App-V.</span></span> <span data-ttu-id="db204-112">Instrucciones detalladas a continuación de la tabla.</span><span class="sxs-lookup"><span data-stu-id="db204-112">Detailed instructions follow the table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db204-113">Nivel funcional del dominio</span><span class="sxs-lookup"><span data-stu-id="db204-113">Domain Functional Level</span></span></th>
<th align="left"><span data-ttu-id="db204-114">Niveles de delegación disponibles</span><span class="sxs-lookup"><span data-stu-id="db204-114">Delegation Levels Available</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db204-115">Windows 2000 nativo</span><span class="sxs-lookup"><span data-stu-id="db204-115">Windows 2000 native</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="db204-116">Sin delegación (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="db204-116">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="db204-117">Delegación sin restricciones</span><span class="sxs-lookup"><span data-stu-id="db204-117">Unconstrained delegation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db204-118">Windows Server 2003, Windows Server 2008 o Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db204-118">Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="db204-119">Sin delegación (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="db204-119">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="db204-120">Delegación sin restricciones ¹</span><span class="sxs-lookup"><span data-stu-id="db204-120">Unconstrained delegation¹</span></span></p></li>
<li><p><span data-ttu-id="db204-121">Delegación restringida (usar solo protocolos Kerberos)</span><span class="sxs-lookup"><span data-stu-id="db204-121">Constrained delegation (Use Kerberos Only Protocols)</span></span></p></li>
<li><p><span data-ttu-id="db204-122">Delegación restringida (usar cualquier protocolo de autenticación) ¹</span><span class="sxs-lookup"><span data-stu-id="db204-122">Constrained delegation (Use any authentication protocol) ¹</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="db204-123">¹ no recomendado.</span><span class="sxs-lookup"><span data-stu-id="db204-123">¹ Not recommended.</span></span>

## <span data-ttu-id="db204-124">Para configurar la delegación no restringida cuando el nivel funcional del dominio es Windows 2000 nativo</span><span class="sxs-lookup"><span data-stu-id="db204-124">To configure unconstrained delegation when the Domain Functional Level is Windows 2000 native</span></span>


<span data-ttu-id="db204-125">En el controlador de dominio del dominio del servidor Web, complete los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="db204-125">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="db204-126">Haga clic en **Inicio**, **herramientas administrativas**y **usuarios y equipos de Active**Directory.</span><span class="sxs-lookup"><span data-stu-id="db204-126">Click **Start**, **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="db204-127">Expanda dominio y, a continuación, expanda la carpeta equipos.</span><span class="sxs-lookup"><span data-stu-id="db204-127">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="db204-128">En el panel derecho, haga clic con el botón secundario en el nombre del equipo del servidor Web y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="db204-128">In the right pane, right-click the computer name for the Web server, and then click **Properties**.</span></span>

4.  <span data-ttu-id="db204-129">En la pestaña **General** , asegúrese de que la casilla **confiar en el equipo para la delegación** está activada.</span><span class="sxs-lookup"><span data-stu-id="db204-129">On the **General** tab, ensure that the **Trust computer for delegation** check box is selected.</span></span>

5.  <span data-ttu-id="db204-130">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="db204-130">Click **OK**.</span></span>

## <span data-ttu-id="db204-131">Para configurar la delegación no restringida cuando el nivel funcional del dominio es Windows Server 2003, Windows Server 2008 o Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db204-131">To configure unconstrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="db204-132">En el controlador de dominio del dominio del servidor Web, complete los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="db204-132">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="db204-133">Haga clic en **Inicio**, seleccione **herramientas administrativas**y, a continuación, haga clic en **usuarios y equipos de Active**Directory.</span><span class="sxs-lookup"><span data-stu-id="db204-133">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="db204-134">Expanda dominio y expanda la carpeta equipos.</span><span class="sxs-lookup"><span data-stu-id="db204-134">Expand domain, and expand the Computers folder.</span></span>

3.  <span data-ttu-id="db204-135">En el panel derecho, haga clic con el botón secundario en el nombre del equipo del servidor Web, seleccione **propiedades**y, a continuación, haga clic en la pestaña **delegación** .</span><span class="sxs-lookup"><span data-stu-id="db204-135">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="db204-136">Haga clic para seleccionar **confiar en este equipo para la delegación a cualquier servicio (solo Kerberos)**.</span><span class="sxs-lookup"><span data-stu-id="db204-136">Click to select **Trust this computer for delegation to any service (Kerberos only)**.</span></span>

5.  <span data-ttu-id="db204-137">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="db204-137">Click **OK**.</span></span>

## <span data-ttu-id="db204-138">Para configurar la delegación restringida cuando el nivel funcional del dominio es Windows Server 2003, Windows Server 2008 o Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db204-138">To configure constrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="db204-139">En el controlador de dominio del dominio del servidor Web, complete los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="db204-139">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="db204-140">Haga clic en **Inicio**, seleccione **herramientas administrativas**y, a continuación, haga clic en **usuarios y equipos de Active**Directory.</span><span class="sxs-lookup"><span data-stu-id="db204-140">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="db204-141">Expanda dominio y, a continuación, expanda la carpeta equipos.</span><span class="sxs-lookup"><span data-stu-id="db204-141">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="db204-142">En el panel derecho, haga clic con el botón secundario en el nombre del equipo del servidor Web, seleccione **propiedades**y, a continuación, haga clic en la pestaña **delegación** .</span><span class="sxs-lookup"><span data-stu-id="db204-142">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="db204-143">Haga clic para seleccionar **confiar en este equipo para la delegación solo a los servicios especificados**.</span><span class="sxs-lookup"><span data-stu-id="db204-143">Click to select **Trust this computer for delegation to specified services only**.</span></span>

5.  <span data-ttu-id="db204-144">Asegúrese de que la selección de **usar solo Kerberos** está seleccionada y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="db204-144">Ensure that **Use Kerberos only** is selected, and then click **OK**.</span></span>

6.  <span data-ttu-id="db204-145">Haga clic en el botón **Agregar** .</span><span class="sxs-lookup"><span data-stu-id="db204-145">Click the **Add** button.</span></span> <span data-ttu-id="db204-146">En el cuadro de diálogo **Agregar servicios** , haga clic en **usuarios o equipos**y, a continuación, busque o escriba el nombre del Microsoft SQL Server que tiene el almacén de datos de App-V y para recibir las credenciales de usuario de IIS.</span><span class="sxs-lookup"><span data-stu-id="db204-146">In the **Add Services** dialog box, click **Users or Computers**, and then browse to or type the name of the Microsoft SQL server that has the App-V data store and is to receive the users credentials from IIS.</span></span> <span data-ttu-id="db204-147">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="db204-147">Click **OK**.</span></span>

7.  <span data-ttu-id="db204-148">En la lista **available Services** , seleccione el servicio MSSQLSvc que indica el número de puerto en el que Microsoft SQL Server acepta conexiones para la base de datos de App-V (el puerto predeterminado es 1433).</span><span class="sxs-lookup"><span data-stu-id="db204-148">In the **Available Services** list, select the MSSQLSvc service that lists port number on which the Microsoft SQL Server is accepting connections for the App-V database (the default port is 1433).</span></span> <span data-ttu-id="db204-149">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="db204-149">Click **OK**.</span></span>

### <span data-ttu-id="db204-150">Pasos adicionales para configurar IIS 7 para la delegación restringida</span><span class="sxs-lookup"><span data-stu-id="db204-150">Additional steps to configure IIS 7 for constrained delegation</span></span>

<span data-ttu-id="db204-151">Si está ejecutando el servicio Web de administración en un servidor IIS 7, debe completar los siguientes pasos para establecer la variable *useAppPoolCredentials* de IIS 7 en true.</span><span class="sxs-lookup"><span data-stu-id="db204-151">If you are running the Management Web Service on an IIS 7 server, you must complete the following steps to set the IIS 7 *useAppPoolCredentials* variable to True.</span></span>

1.  <span data-ttu-id="db204-152">Abra una ventana de símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="db204-152">Open an elevated Command Prompt window.</span></span> <span data-ttu-id="db204-153">Para abrir una ventana de símbolo del sistema con privilegios elevados, haga clic en **Inicio**, seleccione **todos los programas**, **accesorios**, haga clic con el botón derecho en **símbolo del sistema**y seleccione **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="db204-153">To open an elevated Command Prompt window, click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="db204-154">Vaya a%WINDIR%\\system32\\inetsrv.</span><span class="sxs-lookup"><span data-stu-id="db204-154">Navigate to %windir%\\system32\\inetsrv.</span></span>

3.  <span data-ttu-id="db204-155">Escriba **appcmd.exe set config-Section: System. WebServer/Security/Authentication/windowsAuthentication-useAppPoolCredentials: true**y, a continuación, presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="db204-155">Type **appcmd.exe set config -section:system.webServer/security/authentication/windowsAuthentication -useAppPoolCredentials:true**, and then press ENTER.</span></span>

 

 





