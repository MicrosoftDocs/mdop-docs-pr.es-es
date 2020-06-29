---
title: Cómo instalar el cliente de App-V mediante el uso de Setup.msi
description: Cómo instalar el cliente de App-V mediante el uso de Setup.msi
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817331"
---
# <span data-ttu-id="c9fe1-103">Cómo instalar el cliente de App-V mediante el uso de Setup.msi</span><span class="sxs-lookup"><span data-stu-id="c9fe1-103">How to Install the App-V Client by Using Setup.msi</span></span>


<span data-ttu-id="c9fe1-104">En este tema se describe cómo instalar el cliente de App-V con el programa setup.msi.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-104">This topic describes how to install the App-V client by using the setup.msi program.</span></span> <span data-ttu-id="c9fe1-105">Antes de instalar el cliente de App-V con el programa setup.msi, primero debe determinar si debe instalarse algún software previo y, después, debe instalarlo.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-105">Before you install the App-V client using the setup.msi program, you must first determine if any prerequisite software must be installed, and then you must install it.</span></span> <span data-ttu-id="c9fe1-106">Para instalar el software necesario, consulte la sección [instalación de software necesario](#prereq-sw) de este tema.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-106">To install the prerequisite software, see the [Installing Prerequisite Software](#prereq-sw) section of this topic.</span></span> <span data-ttu-id="c9fe1-107">Para instalar el software de cliente, vea el tema sobre cómo [instalar el cliente de App-V en la sección Setup.msi programa](#msi-setup) de este tema.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-107">To install the client software, see the [Installing the App-V Client Using the Setup.msi Program](#msi-setup) section of this topic.</span></span>

## <a href="" id="prereq-sw"></a><span data-ttu-id="c9fe1-108">Instalar el software necesario</span><span class="sxs-lookup"><span data-stu-id="c9fe1-108">Installing Prerequisite Software</span></span>


<span data-ttu-id="c9fe1-109">Puede usar los procedimientos siguientes para instalar el software necesario.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-109">You can use the following procedures to install the prerequisite software.</span></span> <span data-ttu-id="c9fe1-110">Puede crear un archivo de comandos y ejecutar los comandos desde el símbolo del sistema, o bien puede usar un lenguaje de scripts, como VBScript o Windows PowerShell, para ejecutar los comandos.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-110">You can create a command file and run the commands from the command prompt, or you can use a scripting language such as VBScript or Windows PowerShell to run the commands.</span></span>

<span data-ttu-id="c9fe1-111">**Nota:**  Las versiones x86 del siguiente software son necesarias para las versiones x86 y x64 del cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-111">**Note** The x86 versions of the following software are required for both x86 and x64 versions of the App-V client.</span></span>

 

**<span data-ttu-id="c9fe1-112">Para instalar Microsoft VisualC + + 2005SP1 Redistributable Package (x86)</span><span class="sxs-lookup"><span data-stu-id="c9fe1-112">To install Microsoft VisualC++2005SP1 Redistributable Package (x86)</span></span>**

1. <span data-ttu-id="c9fe1-113">Descargue el paquete de software [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) desde el centro de descarga de Microsoft ( <https://go.microsoft.com/fwlink/?LinkId=119961> ).</span><span class="sxs-lookup"><span data-stu-id="c9fe1-113">Download the [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) software package from the Microsoft Download Center (<https://go.microsoft.com/fwlink/?LinkId=119961>).</span></span> <span data-ttu-id="c9fe1-114">\ [Valor del token de plantilla \] para la versión 4,5 SP2 y posteriores del cliente de App-V, descargue vcredist\_x86.exe de la [actualización de seguridad ATL del paquete redistribuible de Microsoft Visual C++ 2005 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [valor de token de plantilla \]</span><span class="sxs-lookup"><span data-stu-id="c9fe1-114">\[Template Token Value\] For version 4.5 SP2 and later of the App-V client, download vcredist\_x86.exe from [Microsoft Visual C++ 2005 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=169360) (https://go.microsoft.com/fwlink/?LinkId=169360).\[Template Token Value\]</span></span>

2. <span data-ttu-id="c9fe1-115">Para instalar silenciosamente, use la opción de línea de comandos "/Q" con vcredist\_x86.exe, por ejemplo, **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-115">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

3. <span data-ttu-id="c9fe1-116">Para instalar el software mediante el archivo vcredist\_x86.msi, use la opción de la línea de comandos "/C/T: &lt; fullpathtofolder &gt; " para extraer los archivos vcredist.msi y vcredis1.cab de vcredist\_x86.exe a una carpeta temporal.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-116">To install the software by using the vcredist\_x86.msi file, use the command-line option “/C /T:&lt;fullpathtofolder&gt;” to extract the files vcredist.msi and vcredis1.cab from vcredist\_x86.exe to a temporary folder.</span></span> <span data-ttu-id="c9fe1-117">Para instalar silenciosamente, use la opción de línea de comandos/Quiet, por ejemplo, **msiexec/i vcredist.msi** /quiet.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-117">To install silently, use the command-line option /quiet—for example, **msiexec /i vcredist.msi** /quiet.</span></span>

### <span data-ttu-id="c9fe1-118">Para instalar Microsoft VisualC + + 2008SP1 Redistributable Package (x86)</span><span class="sxs-lookup"><span data-stu-id="c9fe1-118">To install Microsoft VisualC++2008SP1 Redistributable Package (x86)</span></span>

<span data-ttu-id="c9fe1-119">**Importante**  Para la versión 4.6 y posteriores del cliente de App-V, también debe instalar la actualización de seguridad ATL del paquete redistribuible Microsoft Visual C++ 2008 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-119">**Important** For version4.6 and later of the App-V client, you must also install the Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update.</span></span>

 

****

1.  <span data-ttu-id="c9fe1-120">Descargue el paquete de software de la [actualización de seguridad ATL del paquete redistribuible del Service Pack 1 de Microsoft Visual C++ 2008](https://go.microsoft.com/fwlink/?LinkId=150700) en el centro de descarga de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=150700) .</span><span class="sxs-lookup"><span data-stu-id="c9fe1-120">Download the [Microsoft Visual C++ 2008 Service Pack 1 Redistributable Package ATL Security Update](https://go.microsoft.com/fwlink/?LinkId=150700) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=150700).</span></span>

2.  <span data-ttu-id="c9fe1-121">Para instalar silenciosamente, use la opción de línea de comandos "/Q" con vcredist\_x86.exe, por ejemplo, **vcredist\_x86.exe/q**.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-121">To install silently, use the command-line option “/Q” with vcredist\_x86.exe—for example, **vcredist\_x86.exe /Q**.</span></span>

### <span data-ttu-id="c9fe1-122">Para instalar Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)</span><span class="sxs-lookup"><span data-stu-id="c9fe1-122">To install Microsoft Core XML Services (MSXML)6.0SP1 (x86)</span></span>

****

1.  <span data-ttu-id="c9fe1-123">Descargue el paquete de software [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) en el centro de descarga de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=63266) .</span><span class="sxs-lookup"><span data-stu-id="c9fe1-123">Download the [Microsoft Core XML Services (MSXML)6.0SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) software package from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=63266).</span></span>

2.  <span data-ttu-id="c9fe1-124">Para instalar silenciosamente, use la opción de línea de comandos/Quiet, por ejemplo, **msiexec/i msxml6\_x86.msi/Quiet**.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-124">To install silently, use the command-line option /quiet—for example, **msiexec /i msxml6\_x86.msi /quiet**.</span></span>

### <span data-ttu-id="c9fe1-125">Para instalar informes de errores de aplicaciones de Microsoft</span><span class="sxs-lookup"><span data-stu-id="c9fe1-125">To install Microsoft Application Error Reporting</span></span>

<span data-ttu-id="c9fe1-126">Al instalar informes de errores de aplicaciones de Microsoft, debe usar el parámetro *APPGUID* para especificar el código de producto de App-V.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-126">When installing Microsoft Application Error Reporting, you must use the *APPGUID* parameter to specify the App-V product code.</span></span> <span data-ttu-id="c9fe1-127">El código de producto es único para cada tipo de cliente de App-V y versión.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-127">The product code is unique for each App-V client type and version.</span></span> <span data-ttu-id="c9fe1-128">Seleccione el código de producto correcto en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-128">Select the correct product code from the following table.</span></span>

<span data-ttu-id="c9fe1-129">**Importante**  Para App-V 4.6 SP2 y versiones posteriores, ya no necesita instalar informes de errores de aplicaciones de Microsoft (dw20shared.msi).</span><span class="sxs-lookup"><span data-stu-id="c9fe1-129">**Important** For App-V4.6SP2 and later, you no longer need to install Microsoft Application Error Reporting (dw20shared.msi).</span></span> <span data-ttu-id="c9fe1-130">App-V ahora usa informe de errores de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-130">App-V now uses Microsoft Error Reporting.</span></span>

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c9fe1-131">Versión</span><span class="sxs-lookup"><span data-stu-id="c9fe1-131">Version</span></span></th>
<th align="left"><span data-ttu-id="c9fe1-132">Código de producto para cliente de escritorio</span><span class="sxs-lookup"><span data-stu-id="c9fe1-132">Product Code for Desktop Client</span></span></th>
<th align="left"><span data-ttu-id="c9fe1-133">Código de producto para el cliente para servicios de escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="c9fe1-133">Product Code for Client for Remote Desktop Services</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9fe1-134">App-V 4,5 CU1</span><span class="sxs-lookup"><span data-stu-id="c9fe1-134">App-V 4.5 CU1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span><span class="sxs-lookup"><span data-stu-id="c9fe1-135">FE495DBC-6D42-4698-B61F-86E655E0796D</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span><span class="sxs-lookup"><span data-stu-id="c9fe1-136">8A97C241-D92A-47DC-B360-E716C1AAA929</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9fe1-137">App-V 4,5 SP1</span><span class="sxs-lookup"><span data-stu-id="c9fe1-137">App-V 4.5 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-138">93468B43-C19D-44F9-8BCC-114076DB0443</span><span class="sxs-lookup"><span data-stu-id="c9fe1-138">93468B43-C19D-44F9-8BCC-114076DB0443</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span><span class="sxs-lookup"><span data-stu-id="c9fe1-139">0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9fe1-140">App-V 4,5 SP2</span><span class="sxs-lookup"><span data-stu-id="c9fe1-140">App-V 4.5 SP2</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span><span class="sxs-lookup"><span data-stu-id="c9fe1-141">C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span><span class="sxs-lookup"><span data-stu-id="c9fe1-142">ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9fe1-143">App-V 4,6 x86</span><span class="sxs-lookup"><span data-stu-id="c9fe1-143">App-V 4.6 x86</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span><span class="sxs-lookup"><span data-stu-id="c9fe1-144">9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-145">439FAC21-B423-41D4-8126-54F9FCB70039</span><span class="sxs-lookup"><span data-stu-id="c9fe1-145">439FAC21-B423-41D4-8126-54F9FCB70039</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9fe1-146">App-V 4,6 x64</span><span class="sxs-lookup"><span data-stu-id="c9fe1-146">App-V 4.6 x64</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span><span class="sxs-lookup"><span data-stu-id="c9fe1-147">E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span><span class="sxs-lookup"><span data-stu-id="c9fe1-148">D2977C18-D88A-47CB-AFD8-652DD36F4D0D</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9fe1-149">App-V 4,6 x86 ¹</span><span class="sxs-lookup"><span data-stu-id="c9fe1-149">App-V 4.6 x86 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span><span class="sxs-lookup"><span data-stu-id="c9fe1-150">40C3258B-F9D1-46DF-AE97-72C1F86F2427</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-151">9915D911-CC73-4122-AF4F-564F89454655</span><span class="sxs-lookup"><span data-stu-id="c9fe1-151">9915D911-CC73-4122-AF4F-564F89454655</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9fe1-152">App-V 4,6 x64 ¹</span><span class="sxs-lookup"><span data-stu-id="c9fe1-152">App-V 4.6 x64 ¹</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span><span class="sxs-lookup"><span data-stu-id="c9fe1-153">1650E31F-23B8-40B5-A60A-C5934F557E3B</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span><span class="sxs-lookup"><span data-stu-id="c9fe1-154">7580D918-C621-49E7-9877-3CC59F9BD1DA</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c9fe1-155">App-V 4,6 x86 SP1</span><span class="sxs-lookup"><span data-stu-id="c9fe1-155">App-V 4.6 x86 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span><span class="sxs-lookup"><span data-stu-id="c9fe1-156">DB9F70CD-29BC-480B-8BA2-C9C2232C4553</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-157">1354855A-2298-4C73-9022-EF0686C65991</span><span class="sxs-lookup"><span data-stu-id="c9fe1-157">1354855A-2298-4C73-9022-EF0686C65991</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c9fe1-158">App-V 4,6 x64 SP1</span><span class="sxs-lookup"><span data-stu-id="c9fe1-158">App-V 4.6 x64 SP1</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span><span class="sxs-lookup"><span data-stu-id="c9fe1-159">342C9BB8-65A0-46DE-AB7A-8031E151AF69</span></span></p></td>
<td align="left"><p><span data-ttu-id="c9fe1-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span><span class="sxs-lookup"><span data-stu-id="c9fe1-160">B2C6C8D5-FE76-4056-A326-EE5D633EA175</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="c9fe1-161">¹ versión de "idiomas" de aplicación-V.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-161">¹App-V “Languages” release.</span></span>

<span data-ttu-id="c9fe1-162">**Nota:**  Si necesita encontrar el código de producto, puede usar el Orca.exe editor de bases de datos o una herramienta similar para examinar los archivos de Windows Installer para buscar el valor de la propiedad *ProductCode* .</span><span class="sxs-lookup"><span data-stu-id="c9fe1-162">**Note** If you need to find the product code, you can use the Orca.exe database editor or a similar tool to examine Windows Installer files to find the value of the *ProductCode* property.</span></span> <span data-ttu-id="c9fe1-163">Para obtener más información sobre cómo usar Orca.exe, consulte [herramientas de desarrollo de Windows Installer](https://go.microsoft.com/fwlink/?LinkId=150008) ( https://go.microsoft.com/fwlink/?LinkId=150008) .</span><span class="sxs-lookup"><span data-stu-id="c9fe1-163">For more information about using Orca.exe, see [Windows Installer Development Tools](https://go.microsoft.com/fwlink/?LinkId=150008) (https://go.microsoft.com/fwlink/?LinkId=150008).</span></span>

 

****

1.  <span data-ttu-id="c9fe1-164">Busque el programa de instalación informes de errores de aplicaciones de Microsoft, dw20shared.msi, que se encuentra en la carpeta **Support\\Watson** de los medios de publicación.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-164">Locate the Microsoft Application Error Reporting install program, dw20shared.msi, which can be found in the **Support\\Watson** folder on the release media.</span></span>

2.  <span data-ttu-id="c9fe1-165">Para instalar el software, ejecute el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="c9fe1-165">To install the software, run the following command:</span></span>

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a><span data-ttu-id="c9fe1-166">Instalar el cliente de App-V con el programa Setup.msi</span><span class="sxs-lookup"><span data-stu-id="c9fe1-166">Installing the App-V Client by Using the Setup.msi Program</span></span>


<span data-ttu-id="c9fe1-167">Use el siguiente procedimiento para instalar el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-167">Use the following procedure to install the App-V client.</span></span> <span data-ttu-id="c9fe1-168">Asegúrese de que se ha instalado todo el software necesario.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-168">Ensure that any necessary prerequisite software has been installed.</span></span> <span data-ttu-id="c9fe1-169">\ [Valor del token de plantilla \] para la versión 4.6 y posteriores del cliente de App-V, el programa de setup.msi comprueba el sistema y si no está instalado el software necesario, genera un mensaje de error que indica que la instalación no puede continuar.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-169">\[Template Token Value\] For version4.6 and later of the App-V client, the setup.msi program checks the system and if prerequisite software is not installed, it generates an error message indicating that installation cannot continue.</span></span> <span data-ttu-id="c9fe1-170">\ [Valor del token de plantilla \]</span><span class="sxs-lookup"><span data-stu-id="c9fe1-170">\[Template Token Value\]</span></span>

**<span data-ttu-id="c9fe1-171">Para instalar el cliente de virtualización de aplicaciones con Setup.msi</span><span class="sxs-lookup"><span data-stu-id="c9fe1-171">To install the Application Virtualization Client by Using Setup.msi</span></span>**

1.  <span data-ttu-id="c9fe1-172">Asegúrese de que ha iniciado sesión con una cuenta que tiene derechos de administrador en el equipo.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-172">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="c9fe1-173">Abra una ventana del símbolo del sistema con derechos elevados y, a continuación, cambie el directorio a la carpeta que contiene los archivos de instalación.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-173">Open a Command Prompt window by using elevated rights, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="c9fe1-174">Al instalar la versión 4.6 o una versión posterior del cliente de App-V, debe usar el instalador correcto para el sistema operativo del equipo, 32 bits o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-174">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="c9fe1-175">La instalación no se realizará y aparecerá un mensaje de error si usa el instalador equivocado.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-175">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="c9fe1-176">Escriba la cadena de comando de instalación en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-176">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="c9fe1-177">Como alternativa, puede crear un archivo de comandos y ejecutarlo desde el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-177">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="c9fe1-178">También puede usar un lenguaje de scripts, como VBScript o Windows PowerShell, para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-178">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="c9fe1-179">En el siguiente ejemplo de línea de comandos se muestra cómo se puede usar setup.msi con un número de parámetros opcionales.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-179">The following command-line example shows how setup.msi can be used with a number of optional parameters.</span></span> <span data-ttu-id="c9fe1-180">Para obtener más información sobre estos parámetros, consulte [parámetros de la línea de comandos del instalador del cliente de virtualización de aplicaciones](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c9fe1-180">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="c9fe1-181">msiexec.exe/i "setup.msi" SWICACHESIZE = "10.240" SWIPUBSVRDISPLAY = "sistema de producción" SWIPUBSVRTYPE = "HTTP/Secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "/AppVirt/appsntype.xml" SWIPUBSVRREFRESH = "ON" SWIGLOBALDATA = "D:\\AppVirt\\Global", "=" "."}</span><span class="sxs-lookup"><span data-stu-id="c9fe1-181">msiexec.exe /i "setup.msi" SWICACHESIZE="10240" SWIPUBSVRDISPLAY="Production System" SWIPUBSVRTYPE="HTTP /secure" SWIPUBSVRHOST="PRODSYS" SWIPUBSVRPORT="443" SWIPUBSVRPATH="/AppVirt/appsntype.xml" SWIPUBSVRREFRESH="on" SWIGLOBALDATA="D:\\AppVirt\\Global" SWIUSERDATA="^% LOCALAPPDATA^%\\Windows\\Application Virtualization Client" SWIFSDRIVE="S" /q</span></span>**

    **<span data-ttu-id="c9fe1-182">Importante</span><span class="sxs-lookup"><span data-stu-id="c9fe1-182">Important</span></span>**  
    -   <span data-ttu-id="c9fe1-183">El modificador de Windows Installer "**/q**" se usa para hacer que esta sea una instalación silenciosa.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-183">The Windows Installer switch "**/q**" is used to make this a silent installation.</span></span>

    -   <span data-ttu-id="c9fe1-184">Los caracteres "" **%** en "**% HomeDrive%**" deben ir precedidos del **^** carácter de escape "".</span><span class="sxs-lookup"><span data-stu-id="c9fe1-184">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="c9fe1-185">En caso contrario, el shell de comandos de Windows establece el valor en el del usuario que realiza la instalación.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-185">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="c9fe1-186">Para activar el registro de instalación, use el modificador msiexec **/l\ \* v nombrearchivo. log**.</span><span class="sxs-lookup"><span data-stu-id="c9fe1-186">To turn on installation logging, use the msiexec switch **/l\*v filename.log**.</span></span>

     

## <span data-ttu-id="c9fe1-187">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c9fe1-187">Related topics</span></span>


[<span data-ttu-id="c9fe1-188">Cómo instalar el cliente mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="c9fe1-188">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





