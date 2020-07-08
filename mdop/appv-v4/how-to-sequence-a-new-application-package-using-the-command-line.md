---
title: Cómo secuenciar un nuevo paquete de aplicación mediante la línea de comandos
description: Cómo secuenciar un nuevo paquete de aplicación mediante la línea de comandos
author: dansimp
ms.assetid: de72912b-d9e7-45b5-a601-12528f1a4cac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2dd638a7e4765cedbf1d8050626fb8cc54b2ce8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816680"
---
# Cómo secuenciar un nuevo paquete de aplicación mediante la línea de comandos


Puede usar una línea de comandos para ordenar una nueva aplicación. Usar una línea de comandos es útil cuando tiene que crear un gran número de aplicaciones virtuales o cuando necesita crear aplicaciones secuenciadas de forma periódica.

**Importante**  
La secuencia de la línea de comandos solo permite la secuenciación predeterminada. Si necesita cambiar la configuración de instalación predeterminada de la aplicación que está transformando, debe modificar manualmente la aplicación virtual o actualizar la aplicación virtual mediante el secuenciador de Application Virtualization (App-V). Para obtener más información sobre cómo actualizar una aplicación virtual mediante el secuenciador de App-V, vea [Cómo actualizar una aplicación virtual existente](how-to-upgrade-an-existing-virtual-application.md).



Use el procedimiento siguiente para crear una aplicación virtual mediante la línea de comandos.

**Para ordenar una aplicación con la línea de comandos**

1.  En el equipo que ejecuta el secuenciador de App-V, abra el símbolo del sistema seleccionando **Inicio**, **Ejecutar**y, a continuación, escriba **cmd**. Haga clic en **Aceptar**.

2.  Use el símbolo del sistema para especificar la ubicación en la que se instalará el secuenciador de App-V. Por ejemplo, en el símbolo del sistema, puede escribir lo siguiente: **CD c:\\Archivos de la aplicación SPRJ de virtualización**.

3.  En el símbolo del sistema, escriba el siguiente comando y reemplace el texto entre comillas por sus valores:

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **Nota**  
    Puede especificar parámetros adicionales mediante la línea de comandos, en función de la complejidad de la aplicación que esté transformando. Para obtener una lista completa de los parámetros que se pueden usar con el secuenciador de App-V, consulte [línea de comandos de Application Virtualization Sequencer](application-virtualization-sequencer-command-line.md).



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtoMSI</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtopackageroot</em></p></td>
<td align="left"><p>Specifies the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. Presione **entrar**.

## Temas relacionados


[Cómo administrar aplicaciones virtuales con la línea de comandos](how-to-manage-virtual-applications-using-the-command-line.md)









