---
title: Cómo actualizar un paquete de aplicaciones secuenciadas mediante la línea de comandos
description: Cómo actualizar un paquete de aplicaciones secuenciadas mediante la línea de comandos
author: dansimp
ms.assetid: 682fac46-c71d-4731-831b-81bfd5032764
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eade2ced43852419176f635918f0a6b7c3444aee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816490"
---
# Cómo actualizar un paquete de aplicaciones secuenciadas mediante la línea de comandos


Use el siguiente procedimiento para actualizar una aplicación virtual mediante una línea de comandos. Al actualizar un paquete de aplicación virtual existente mediante la línea de comandos, se elimina la versión original del archivo. SFT. Debe realizar una copia de seguridad del archivo. SFT asociado antes de actualizar el paquete mediante la línea de comandos.

**Para actualizar una aplicación virtual**

1.  En el equipo que ejecuta el secuenciador de Application Virtualization (App-V), para abrir el símbolo del sistema, seleccione **Inicio**, **Ejecutar**y escriba **cmd**. Haga clic en **Aceptar**.

2.  En el símbolo del sistema, especifique la ubicación donde está instalado el secuenciador de App-V. Por ejemplo, en el símbolo del sistema, puede escribir lo siguiente: **CD c:\\Archivos de la aplicación SPRJ de virtualización**.

3.  En el símbolo del sistema, escriba el siguiente comando y reemplace el texto entre comillas por sus valores:

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **Nota**  
    Puede especificar parámetros adicionales mediante la línea de comandos, en función de la complejidad de la aplicación que esté actualizando. Para obtener una lista completa de los parámetros que se pueden usar con el secuenciador de App-V, consulte [parámetros de la línea de comandos](command-line-parameters.md).



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
<td align="left"><p><em>pathtosourceSPRJ</em></p></td>
<td align="left"><p>Specifies the directory location of the virtual application to be upgraded.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtoUpgradeInstaller</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an upgrade to the application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodecodefolder</em></p></td>
<td align="left"><p>Specify the directory in which to unpack the SFT file.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. Presione **entrar**.

## Temas relacionados


[Cómo administrar aplicaciones virtuales con la línea de comandos](how-to-manage-virtual-applications-using-the-command-line.md)









