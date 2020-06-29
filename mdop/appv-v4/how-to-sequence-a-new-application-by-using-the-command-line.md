---
title: Cómo secuenciar una nueva aplicación mediante el uso de la línea de comandos
description: Cómo secuenciar una nueva aplicación mediante el uso de la línea de comandos
author: dansimp
ms.assetid: c3b5c842-6a91-4d0a-9a22-c7b8d1aeb09a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea7b1222dc00a0a4649cb342ac1ba41338484889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816690"
---
# Cómo secuenciar una nueva aplicación mediante el uso de la línea de comandos


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
    Puede especificar parámetros adicionales mediante la línea de comandos, en función de la complejidad de la aplicación que esté transformando. Para obtener una lista completa de los parámetros que se pueden usar con el secuenciador de App-V, consulta parámetros de la [línea de comandos Sequencer](sequencer-command-line-parameters.md).



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
<td align="left"><p>Specify the package root directory.</p></td>
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


[Cómo crear o actualizar aplicaciones virtuales con el secuenciador de App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[Códigos de error de línea de comandos de secuenciador](sequencer-command-line-error-codes.md)

[Parámetros de línea de comandos del secuenciador](sequencer-command-line-parameters.md)









