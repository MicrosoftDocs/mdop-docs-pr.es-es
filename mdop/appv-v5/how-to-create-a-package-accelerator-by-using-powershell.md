---
title: Cómo crear un acelerador de paquetes mediante el uso de PowerShell
description: Cómo crear un acelerador de paquetes mediante el uso de PowerShell
author: dansimp
ms.assetid: 8e527363-d961-4153-826a-446a4ad8d980
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4270db9a5f0603cff1f33e6244a5abb517572d97
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814295"
---
# Cómo crear un acelerador de paquetes mediante el uso de PowerShell


Los aceleradores de paquetes de App-V 5,0 automáticamente ordenan aplicaciones grandes y complejas. Además, cuando aplica un acelerador de paquetes de App-V 5,0, no siempre es necesario instalar manualmente una aplicación para crear el paquete virtualizado.

**Para crear un acelerador de paquetes**

1.  Instale el secuenciador de 5,0 de App-V. Para obtener más información sobre cómo instalar el secuenciador, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer-beta-gb18030.md).

2.  Para abrir una consola de PowerShell, haga clic en **iniciar** y escriba **PowerShell**. Haga clic con el botón derecho en **Windows PowerShell** y seleccione **Ejecutar como administrador**. Use el cmdlet **New-AppvPackageAccelerator** .

3.  Para crear un acelerador de paquetes, asegúrese de tener el paquete. appv para crear un acelerador desde, los archivos de instalación o los medios de instalación, y, opcionalmente, un archivo Léame para que los usuarios del acelerador usen. Los siguientes parámetros son necesarios para usar el cmdlet del acelerador de paquetes:

    -   **InstalledFilesPath** : especifica la ruta de instalación de la aplicación.

    -   **Instalador** : especifica la ruta de acceso a los medios del instalador de aplicaciones

    -   **InputPackagePath** : especifica la ruta de acceso al paquete. appv

    -   **Path** : especifica el directorio de salida del paquete.

    En el ejemplo siguiente se muestra cómo se puede crear un acelerador de paquetes con un paquete. appv y los medios de instalación:

    **New-AppvPackageAccelerator-InputPackagePath &lt; path al archivo. appv &gt; : ruta de acceso &lt; del instalador al archivo ejecutable de instalación &gt; -ruta &lt; de acceso de la ruta de acceso de salida&gt;**

    En la siguiente lista se muestran parámetros opcionales adicionales que se pueden usar con el cmdlet **New-AppvPackageAccelerator** :

    -   **AcceleratorDescriptionFile** : especifica la ruta de acceso a las instrucciones del acelerador de paquetes creado por el usuario. Las instrucciones del acelerador de paquetes son archivos de Descripción **. txt** o **. rtf** que se empaquetarán con el paquete creado con el acelerador de paquetes.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Administración de App-V mediante el uso de PowerShell](administering-app-v-by-using-powershell.md)

 

 





