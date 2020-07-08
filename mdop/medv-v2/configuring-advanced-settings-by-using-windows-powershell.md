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
# Establecimiento de la configuración avanzada con Windows PowerShell


El paquete de área de trabajo MED-V que cree incluye un archivo de script de Windows PowerShell (. PS1) que puede editar antes de probar e implementar el paquete de área de trabajo de MED-V. Esta sección proporciona información e instrucciones para ayudarle a administrar la configuración de MED-V con Windows PowerShell antes de implementar las áreas de trabajo de MED-V.

## Usar cmdlets de Windows PowerShell en MED-V


Los siguientes cmdlets de Windows PowerShell están disponibles en Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:

**Nuevo: MedvConfiguration**

**Exportar-MedvConfiguration**

**Nuevo: MedvWorkspace**

**Exportar-MedvWorkspace**

Para acceder a los cmdlets de Windows PowerShell para MED-V, abra Windows PowerShell y escriba el siguiente comando para importar los módulos MED-V.

``` syntax
Import-Module microsoft.medv
```

Una vez importados los módulos, puede obtener acceso a la ayuda en línea de los cmdlets con los comandos de ayuda de Windows PowerShell estándar, **Man** u **Get-Help**. Por ejemplo, para acceder a una descripción del cmdlet **New-MedvConfiguration** , que incluye una lista completa de los parámetros disponibles, escriba el siguiente comando.

``` syntax
get-help New-MedvConfiguration
```

También puede ver ayuda sobre parámetros específicos. Por ejemplo, para ver la ayuda del parámetro VmMemory, escriba lo siguiente:

``` syntax
get-help New-MedvConfiguration -parameter VmMemory
```

Para ver una lista de todas las opciones de configuración de MED-V y sus opciones predeterminadas, escriba el siguiente comando.

``` syntax
New-MedvConfiguration -ForceDefaults
```

Para ver una lista de todas las opciones de configuración de MED-V y sus valores actuales, escriba el siguiente comando.

``` syntax
gwmi -Class "Setting” -Namespace "root/microsoft/medv”
```

## Crear un área de trabajo de MED-V con una configuración personalizada


Después de crear correctamente un paquete de área de trabajo MED-V con el Empaquetador de área de trabajo MED-V, se generará un script de Windows PowerShell en la carpeta especificada para guardar los archivos de Empaquetador. El contenido de esta secuencia de comandos muestra algunas de las opciones de configuración de MED-V disponibles que se pueden editar.

Siguiendo estos pasos, puede personalizar el script y, a continuación, ejecutarlo en Windows PowerShell para crear un área de trabajo de MED-V con la nueva configuración.

**Importante**  Ejecute Windows PowerShell con credenciales administrativas y asegúrese de que la Directiva de ejecución de Windows PowerShell permita la ejecución de scripts.

1.  Edite el script de Windows PowerShell generado por el Empaquetador de área de trabajo MED-V o cree un nuevo script con la configuración que desee.

2.  Ejecute Windows PowerShell con credenciales administrativas y, en el símbolo del sistema, escriba el siguiente comando.

    ``` syntax
    & “.\<workspacename>.ps1”
    ```

    Este comando ejecuta el script de Windows PowerShell y ejecuta el cmdlet **New-MedvWorkspace** para generar un nuevo paquete de área de trabajo MED-V. Los nuevos archivos de empaquetado se guardan en la carpeta que especificó originalmente para almacenar los archivos de Empaquetador de área de trabajo de MED-V. Para obtener ayuda adicional sobre este cmdlet, consulte la ayuda de Windows PowerShell.

 

## Exportar una configuración de MED-V a un archivo de registro


Puede actualizar las opciones de configuración de MED-V después de instalar el área de trabajo de MED-V. Use el cmdlet **New-MedvConfiguration** para especificar los parámetros que quiere cambiar. Por ejemplo, para crear un archivo de registro que cambie la configuración de memoria de la máquina virtual, escriba los comandos siguientes.

``` syntax
New-MedvConfiguration  -VmMemory 1024 | Export-MedvConfiguration -Path c:\medvConfiguration\myConfig.reg
```

Puede importar el archivo de registro resultante del equipo host a un área de trabajo de MED-V para aplicar la nueva configuración.

## Temas relacionados


[Administrar opciones de configuración de área de trabajo de MED-V](managing-med-v-workspace-configuration-settings.md)

[Probar e implementar el paquete del área de trabajo de MED-V](test-and-deploy-the-med-v-workspace-package.md)

 

 





