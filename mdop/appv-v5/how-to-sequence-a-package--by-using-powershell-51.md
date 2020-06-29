---
title: Cómo hacer una secuencia de un paquete con PowerShell
description: Cómo hacer una secuencia de un paquete con PowerShell
author: dansimp
ms.assetid: 6134c6be-937d-4609-a516-92d49154b290
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1bc2933fdb64080dab3b514784e7f68b0236df9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813694"
---
# Cómo hacer una secuencia de un paquete con PowerShell


Use el siguiente procedimiento para crear un nuevo paquete de App-V 5,1 con PowerShell.

**Nota:**  Antes de usar este procedimiento, debe copiar los archivos de instalador asociados en el equipo que ejecuta el secuenciador y leer y comprender la sección Sequencer de [la planificación de la aplicación-V 5,1 secuenciador y la implementación de cliente](planning-for-the-app-v-51-sequencer-and-client-deployment.md).

 

**Para crear una nueva aplicación virtual con PowerShell**

1.  Instale el secuenciador de 5,1 de App-V. Para obtener más información sobre cómo instalar el secuenciador, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer-51beta-gb18030.md).

2.  Para abrir una consola de PowerShell, haga clic en **iniciar** y escriba **PowerShell**. Haga clic con el botón derecho en **Windows PowerShell** y seleccione **Ejecutar como administrador**.

3.  Con la consola de PowerShell, escriba lo siguiente: **Import-Module appvsequencer**.

4.  Para crear un paquete, use el cmdlet **New-AppvSequencerPackage** . Los siguientes parámetros son necesarios para crear un paquete:

    -   **Name** : especifica el nombre del paquete.

    -   **PrimaryVirtualApplicationDirectory** : especifica la ruta de acceso al directorio que se usará para instalar la aplicación. Esta ruta debe existir.

    -   **Instalador** : especifica la ruta de acceso al instalador de la aplicación asociada.

    -   **RutaDeAcceso** : especifica el directorio de salida del paquete.

    Por ejemplo:

    **New-AppvSequencerPackage: nombre &lt; del nombre de la ruta de acceso del paquete &gt; PrimaryVirtualApplicationDirectory &lt; a la raíz del paquete &gt; -ruta de acceso del instalador &lt; para el ejecutable del instalador &gt; -OutputPath &lt; Directorio de la ruta de acceso de salida&gt;**

    Espere a que el secuenciador cree el paquete. Crear un paquete con PowerShell puede tardar un tiempo. Si el paquete no se creó correctamente, se devolverá un error.

    En la siguiente lista se muestran parámetros opcionales adicionales que se pueden usar con **el cmdlet New-AppvSequencerPackage** :

    -   AcceleratorFilePath: especifica la ruta de acceso al archivo. cab de acelerador para generar un paquete.

    -   InstalledFilesPath: especifica la ruta en la que se guardan los archivos locales instalados de la aplicación.

    -   InstallMediaPath: especifica la ruta de acceso en la que se encuentran los medios de instalación

    -   TemplateFilePath: especifica la ruta de acceso a un archivo de plantilla si desea personalizar el proceso de secuenciación.

    -   FullLoad: especifica que el paquete debe descargarse completamente en el equipo que ejecuta la aplicación-V 5,1 para que pueda abrirse.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Administrar 5.1 de App-V mediante el uso de PowerShell](administering-app-v-51-by-using-powershell.md)

 

 





