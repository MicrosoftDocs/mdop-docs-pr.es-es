---
title: Cómo convertir un paquete creado en una versión anterior de App-V
description: Cómo convertir un paquete creado en una versión anterior de App-V
author: dansimp
ms.assetid: 3366d399-2891-491d-8de1-f8cfdf39bbab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 402e64e3bdbc55eea1edb91d070bb7ebb11c912b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814358"
---
# Cómo convertir un paquete creado en una versión anterior de App-V


Puede usar la utilidad de conversión de paquetes para actualizar paquetes de aplicaciones virtuales que se han creado con versiones anteriores de App-V.

**Nota**  
Si está ejecutando un equipo con una arquitectura de bits de 64, debe usar la versión x86 de PowerShell.



El convertidor de paquetes solo puede convertir directamente paquetes creados mediante el secuenciador de aplicaciones-V 4,5 o una versión posterior. Los paquetes que se hayan creado con una versión anterior a App-V 4,5 deben actualizarse al formato App-V 4,5 o App-V 4,6 antes de la conversión.

La siguiente información proporciona la dirección para convertir paquetes de aplicaciones virtuales existentes.

**Importante**  
Debe configurar el convertidor de paquetes para guardar siempre el archivo de ingredientes del paquete en una ubicación y un directorio seguros. Un administrador solo puede tener acceso a una ubicación segura. Además, al implementar el paquete, debe guardar el paquete en una ubicación segura o asegurarse de que ningún otro usuario pueda iniciar sesión durante el proceso de conversión.



**La carpeta de instalación de App-V 4,6 se redirige a la raíz del sistema de archivos virtual**

Al convertir paquetes de App-V 4,6 a 5,1, el paquete App-V 5,1 puede acceder a la unidad codificada que tenía que usar al crear paquetes 4,6. La letra de unidad será la que seleccionó como unidad de instalación en la máquina de secuenciación de 4,6. (La letra de unidad predeterminada es Q:\\.)

Antes de la aplicación-V 5,1, no se reconoció la carpeta raíz de 4,6 y los paquetes App-V 5,0 no podían acceder a ella. Ahora, los paquetes de App-V 5,1 pueden acceder a archivos codificados por su ruta de acceso completa o pueden enumerar archivos mediante programación en la raíz de instalación de App-V 4,6.

**Detalles técnicos:** El conversor de paquetes de App-V 5,1 guardará la carpeta raíz de instalación de App-V 4,6 y los nombres cortos de carpeta en el FilesystemMetadata.xml archivo del elemento filesystem. Cuando el cliente de App-V 5,1 crea el proceso virtual, se asignarán solicitudes de la raíz de instalación de App-V 4,6 a la raíz del sistema de archivos virtual.

**Introducción**

1.  Instale el secuenciador de App-V en un equipo de su entorno. Para obtener información sobre cómo instalar el secuenciador, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer-51beta-gb18030.md).

2.  

    Los siguientes cmdlets están disponibles:

    -   Prueba-AppvLegacyPackage: este cmdlet está diseñado para comprobar paquetes. Devolverá información acerca de los errores con el paquete, como los archivos **. SFT** que faltan, un origen no válido, errores de archivo **. OSD** o una versión de paquete no válida. Este cmdlet no analizará el archivo **. SFT** ni realizará ninguna validación en profundidad. Para obtener información sobre las opciones y la funcionalidad básica para este cmdlet, usando el cmdline de PowerShell, escriba `Test-AppvLegacyPackage -?` .

    -   ConvertFrom-AppvLegacyPackage: para convertir un paquete existente, escriba `ConvertFrom-AppvLegacyPackage c:\contentStore c:\convertedPackages` . En este comando, `c:\contentStore` representa la ubicación del paquete existente y `c:\convertedPackages` es el directorio de salida en el que se guardará el archivo de paquete de aplicación virtual de App-V 5,1 resultante. De forma predeterminada, si no especificas un nombre nuevo, el nombre del paquete anterior se usará para el nombre de archivo de App-V 5,1.

        Además, el convertidor de paquetes optimiza el rendimiento de los paquetes en App-V 5,1 al configurar el paquete en error de transmisión en el paquete de App-V.  Esto es más rendimiento que el bloque de características principal y descarga por completo el paquete. La **DownloadFullPackageOnFirstLaunch** Flag te permite convertir el paquete y configurar el paquete para que se descargue completamente de forma predeterminada.

        **Nota**  
        Antes de especificar el directorio de resultados, debe crear el directorio de resultados.



~~~
**Advanced Conversion Tips**

-   Piping - PowerShell supports piping. Piping allows you to call `dir c:\contentStore\myPackage | Test-AppvLegacyPackage`. In this example, the directory object that represents `myPackage` will be given as input to the `Test-AppvLegacyPackage` command and bound to the `-Source` parameter. Piping like this is especially useful when you want to batch commands together; for example, `dir .\ | Test-AppvLegacyPackage | ConvertFrom-AppvLegacyAppvPackage -Target .\ConvertedPackages`. This piped command would test the packages and then pass those objects on to actually be converted. You can also apply a filter on packages without errors or only specify a directory which contains an **.sprj** file or pipe them to another cmdlet that adds the filtered package to the server or publishes them to the App-V 5.1 client.

-   Batching - The PowerShell command enables batching. More specifically, the cmdlets support taking a string\[\] object for the `-Source` parameter which represents a list of directory paths. This allows you to enter `$packages = dir c:\contentStore` and then call `ConvertFrom-AppvLegacyAppvPackage-Source $packages -Target c:\ConvertedPackages` or to use piping and call `dir c:\ContentStore | ConvertFrom-AppvLegacyAppvPackage -Target C:\ConvertedPackages`.

-   Other functionality - PowerShell has other built-in functionality for features such as aliases, piping, lazy-binding, .NET object, and many others. All of these are usable in PowerShell and can help you create advanced scenarios for the Package Converter.

**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)









