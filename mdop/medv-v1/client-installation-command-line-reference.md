---
title: Referencia de línea de comandos de instalación de cliente
description: Referencia de línea de comandos de instalación de cliente
author: dansimp
ms.assetid: 122a593d-3314-4e9b-858a-08a25ed00c32
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 708daf82699c63dfaa1f99ae595911cf6bad3737
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826730"
---
# Referencia de línea de comandos de instalación de cliente


**Para instalar MED-V desde la línea de comandos**

1.  Desde la línea de comandos, ejecute el paquete MED-V. msi seguido de cualquiera de los parámetros opcionales que se describen en la tabla siguiente.

2.  El paquete MED-V. msi se llama *MED-V\_x.msi*, donde *x* es el número de versión.

    Por ejemplo, *MED-V\_1.0.65.msi*.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parámetro</th>
<th align="left">Valor</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Quiet</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Instalación silenciosa</p></td>
</tr>
<tr class="even">
<td align="left"><p>/log &lt; ruta completa del archivo de registro&gt;</p></td>
<td align="left"><p>La ruta de acceso completa del archivo de registro.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>La ruta de acceso completa del directorio de instalación.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>VMSFOLDER</p></td>
<td align="left"><p>La ruta de acceso completa a la carpeta de la máquina virtual.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALL_ADMIN_TOOLS</p></td>
<td align="left"><p><strong>1,0</strong></p>
<p>Valor predeterminado: <strong> 0</strong></p></td>
<td align="left"><p>Instala las herramientas de administración de MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>START_AUTOMATICALLY</p></td>
<td align="left"><p><strong>1,0</strong></p>
<p>Valor predeterminado: <strong> 0</strong></p></td>
<td align="left"><p>Inicia automáticamente el cliente de MED-V cada vez que el usuario inicia sesión en Windows.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_ADDRESS</p></td>
<td align="left"><p>nombre de host o IP</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SERVER_PORT</p></td>
<td align="left"><p>puerto</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>SERVER_SSL</p></td>
<td align="left"><p><strong>1,0</strong></p>
<p>para <strong> https </strong> o <strong> http</strong></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>START_MEDV</p></td>
<td align="left"><p><strong>1,0</strong></p>
<p>Valor predeterminado: <strong> 1</strong></p></td>
<td align="left"><p>Inicia MED-V al finalizar la instalación de MED-V.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Se recomienda establecer START_MEDV = 0 en caso de que el sistema Instale MED-V.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>DESKTOP_SHORTCUT</p></td>
<td align="left"><p><strong>1,0</strong></p>
<p>Valor predeterminado: <strong> 1</strong></p></td>
<td align="left"><p>Crea un acceso directo en el escritorio, que inicia el cliente de MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>MINIMAL_RAM_REQUIRED</p></td>
<td align="left"><p>RAM en MB</p></td>
<td align="left"><p>Al instalar MED-V, comprueba si el equipo tiene la cantidad mínima de RAM especificada. Si no es así, la instalación se cancela.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SKIP_OS_CHECK</p></td>
<td align="left"><p><strong>1,0</strong></p></td>
<td align="left"><p>Omite la validación del sistema operativo.</p></td>
</tr>
</tbody>
</table>











