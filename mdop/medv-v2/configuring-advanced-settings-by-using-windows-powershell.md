---
title: Establecimiento de la configuración avanzada con Windows PowerShell
description: Establecimiento de la configuración avanzada con Windows PowerShell
author: dansimp
ms.assetid: 437a31cc-2a11-456f-b448-b0b869fb53f7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 45a3ece3f76f6e982913aad2b25cfe0084542f32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827391"
---
# <span data-ttu-id="d173e-103">Establecimiento de la configuración avanzada con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="d173e-103">Configuring Advanced Settings by Using Windows PowerShell</span></span>


<span data-ttu-id="d173e-104">El paquete de área de trabajo MED-V que cree incluye un archivo de script de Windows PowerShell (. PS1) que puede editar antes de probar e implementar el paquete de área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="d173e-104">The MED-V workspace package that you create includes a Windows PowerShell script (.ps1) file that you can edit before you test and deploy your MED-V workspace package.</span></span> <span data-ttu-id="d173e-105">Esta sección proporciona información e instrucciones para ayudarle a administrar la configuración de MED-V con Windows PowerShell antes de implementar las áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="d173e-105">This section provides information and guidance to help you manage MED-V configuration settings by using Windows PowerShell before you deploy the MED-V workspaces.</span></span>

## <span data-ttu-id="d173e-106">Usar cmdlets de Windows PowerShell en MED-V</span><span class="sxs-lookup"><span data-stu-id="d173e-106">Using Windows PowerShell Cmdlets in MED-V</span></span>


<span data-ttu-id="d173e-107">Los siguientes cmdlets de Windows PowerShell están disponibles en Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:</span><span class="sxs-lookup"><span data-stu-id="d173e-107">The following Windows PowerShell cmdlets are available in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

**<span data-ttu-id="d173e-108">Nuevo: MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="d173e-108">New-MedvConfiguration</span></span>**

**<span data-ttu-id="d173e-109">Exportar-MedvConfiguration</span><span class="sxs-lookup"><span data-stu-id="d173e-109">Export-MedvConfiguration</span></span>**

**<span data-ttu-id="d173e-110">Nuevo: MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="d173e-110">New-MedvWorkspace</span></span>**

**<span data-ttu-id="d173e-111">Exportar-MedvWorkspace</span><span class="sxs-lookup"><span data-stu-id="d173e-111">Export-MedvWorkspace</span></span>**

<span data-ttu-id="d173e-112">Para acceder a los cmdlets de Windows PowerShell para MED-V, abra Windows PowerShell y escriba el siguiente comando para importar los módulos MED-V.</span><span class="sxs-lookup"><span data-stu-id="d173e-112">To access Windows PowerShell cmdlets for MED-V, open Windows PowerShell and type the following command to import the MED-V modules.</span></span>

``` syntax
Import-Module microsoft.medv
```

<span data-ttu-id="d173e-113">Una vez importados los módulos, puede obtener acceso a la ayuda en línea de los cmdlets con los comandos de ayuda de Windows PowerShell estándar, **Man** u **Get-Help**.</span><span class="sxs-lookup"><span data-stu-id="d173e-113">After the modules are imported, you can access inline help for the cmdlets by using the standard Windows PowerShell Help commands, **man** or **get-help**.</span></span> <span data-ttu-id="d173e-114">Por ejemplo, para acceder a una descripción del cmdlet **New-MedvConfiguration** , que incluye una lista completa de los parámetros disponibles, escriba el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="d173e-114">For example, to access a description of the **New-MedvConfiguration** cmdlet including a complete list of available parameters, type the following command.</span></span>

``` syntax
get-help New-MedvConfiguration
```

<span data-ttu-id="d173e-115">También puede ver ayuda sobre parámetros específicos.</span><span class="sxs-lookup"><span data-stu-id="d173e-115">You can also view help for specific parameters.</span></span> <span data-ttu-id="d173e-116">Por ejemplo, para ver la ayuda del parámetro VmMemory, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d173e-116">For example, to view help for the parameter VmMemory, type the following:</span></span>

``` syntax
get-help New-MedvConfiguration -parameter VmMemory
```

<span data-ttu-id="d173e-117">Para ver una lista de todas las opciones de configuración de MED-V y sus opciones predeterminadas, escriba el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="d173e-117">To view a list of all MED-V configuration settings and their defaults, type the following command.</span></span>

``` syntax
New-MedvConfiguration -ForceDefaults
```

<span data-ttu-id="d173e-118">Para ver una lista de todas las opciones de configuración de MED-V y sus valores actuales, escriba el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="d173e-118">To view a list of all MED-V configuration settings and their current values, type the following command.</span></span>

``` syntax
gwmi -Class "Setting” -Namespace "root/microsoft/medv”
```

## <span data-ttu-id="d173e-119">Crear un área de trabajo de MED-V con una configuración personalizada</span><span class="sxs-lookup"><span data-stu-id="d173e-119">Creating a MED-V Workspace with Custom Settings</span></span>


<span data-ttu-id="d173e-120">Después de crear correctamente un paquete de área de trabajo MED-V con el Empaquetador de área de trabajo MED-V, se generará un script de Windows PowerShell en la carpeta especificada para guardar los archivos de Empaquetador.</span><span class="sxs-lookup"><span data-stu-id="d173e-120">After you successfully create a MED-V workspace package by using the MED-V Workspace Packager, a Windows PowerShell script is generated in the folder you specified for saving your packager files.</span></span> <span data-ttu-id="d173e-121">El contenido de esta secuencia de comandos muestra algunas de las opciones de configuración de MED-V disponibles que se pueden editar.</span><span class="sxs-lookup"><span data-stu-id="d173e-121">The contents of this script show some of the available MED-V configuration settings that you can edit.</span></span>

<span data-ttu-id="d173e-122">Siguiendo estos pasos, puede personalizar el script y, a continuación, ejecutarlo en Windows PowerShell para crear un área de trabajo de MED-V con la nueva configuración.</span><span class="sxs-lookup"><span data-stu-id="d173e-122">Following these steps, you can customize the script and then run it in Windows PowerShell to create a MED-V workspace with the new settings.</span></span>

<span data-ttu-id="d173e-123">**Importante**  Ejecute Windows PowerShell con credenciales administrativas y asegúrese de que la Directiva de ejecución de Windows PowerShell permita la ejecución de scripts.</span><span class="sxs-lookup"><span data-stu-id="d173e-123">**Important** Run Windows PowerShell with administrative credentials, and ensure that the Windows PowerShell execution policy allows the running of scripts.</span></span>

1.  <span data-ttu-id="d173e-124">Edite el script de Windows PowerShell generado por el Empaquetador de área de trabajo MED-V o cree un nuevo script con la configuración que desee.</span><span class="sxs-lookup"><span data-stu-id="d173e-124">Edit the Windows PowerShell script that was generated by the MED-V Workspace Packager, or author a new script with the configuration settings that you want.</span></span>

2.  <span data-ttu-id="d173e-125">Ejecute Windows PowerShell con credenciales administrativas y, en el símbolo del sistema, escriba el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="d173e-125">Run Windows PowerShell with administrative credentials and at the command prompt, type the following command.</span></span>

    ``` syntax
    & “.\<workspacename>.ps1”
    ```

    <span data-ttu-id="d173e-126">Este comando ejecuta el script de Windows PowerShell y ejecuta el cmdlet **New-MedvWorkspace** para generar un nuevo paquete de área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="d173e-126">This command runs the Windows PowerShell script and runs the **New-MedvWorkspace** cmdlet to generate a new MED-V workspace package.</span></span> <span data-ttu-id="d173e-127">Los nuevos archivos de empaquetado se guardan en la carpeta que especificó originalmente para almacenar los archivos de Empaquetador de área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="d173e-127">The new packager files are saved in the folder that you originally specified for storing your MED-V Workspace Packager files.</span></span> <span data-ttu-id="d173e-128">Para obtener ayuda adicional sobre este cmdlet, consulte la ayuda de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d173e-128">For additional help about this cmdlet, see the Windows PowerShell Help.</span></span>

 

## <span data-ttu-id="d173e-129">Exportar una configuración de MED-V a un archivo de registro</span><span class="sxs-lookup"><span data-stu-id="d173e-129">Exporting a MED-V Configuration to a Registry File</span></span>


<span data-ttu-id="d173e-130">Puede actualizar las opciones de configuración de MED-V después de instalar el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="d173e-130">You can update MED-V configuration settings after the MED-V workspace is installed.</span></span> <span data-ttu-id="d173e-131">Use el cmdlet **New-MedvConfiguration** para especificar los parámetros que quiere cambiar.</span><span class="sxs-lookup"><span data-stu-id="d173e-131">Use the **New-MedvConfiguration** cmdlet to specify the parameters that you want to change.</span></span> <span data-ttu-id="d173e-132">Por ejemplo, para crear un archivo de registro que cambie la configuración de memoria de la máquina virtual, escriba los comandos siguientes.</span><span class="sxs-lookup"><span data-stu-id="d173e-132">For example, to create a registry file that changes the virtual machine memory setting, type the following commands.</span></span>

``` syntax
New-MedvConfiguration  -VmMemory 1024 | Export-MedvConfiguration -Path c:\medvConfiguration\myConfig.reg
```

<span data-ttu-id="d173e-133">Puede importar el archivo de registro resultante del equipo host a un área de trabajo de MED-V para aplicar la nueva configuración.</span><span class="sxs-lookup"><span data-stu-id="d173e-133">You can import the resultant registry file from the host computer to a MED-V workspace to apply the new configuration settings.</span></span>

## <span data-ttu-id="d173e-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d173e-134">Related topics</span></span>


[<span data-ttu-id="d173e-135">Administrar opciones de configuración de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="d173e-135">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="d173e-136">Probar e implementar el paquete del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="d173e-136">Test And Deploy the MED-V Workspace Package</span></span>](test-and-deploy-the-med-v-workspace-package.md)

 

 





