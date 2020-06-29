---
title: Cómo realizar tareas de DaRT mediante comandos de PowerShell
description: Cómo realizar tareas de DaRT mediante comandos de PowerShell
author: dansimp
ms.assetid: f5a5c5f9-d667-4c85-9e82-7baf0b2aec6e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fdf167ca81281da4e04dae10e34bad6122ec05aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822600"
---
# Cómo realizar tareas de DaRT mediante comandos de PowerShell


Microsoft Diagnostics and Recovery Toolset (DaRT) 10 proporciona el siguiente conjunto de cmdlets de Windows PowerShell. Los administradores pueden usar estos cmdlets de PowerShell para realizar diversas tareas de servidor de DaRT 10 desde el símbolo del sistema en lugar de hacerlo desde el Asistente para imágenes de recuperación de DaRT.

## Para administrar DaRT mediante comandos de PowerShell


Use los cmdlets de PowerShell que se describen aquí para administrar DaRT.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copy-DartImage</p></td>
<td align="left"><p>Graba un ISO en un CD, DVD o unidad USB.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Exportar-DartImage</p></td>
<td align="left"><p>Permite que el archivo WIM de origen, que contiene una imagen de DaRT, se convierta en un archivo ISO.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Nuevo: DartConfiguration</p></td>
<td align="left"><p>Crea un objeto de configuración de DaRT necesario para aplicar un conjunto de herramientas de DaRT a una imagen de Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Set-DartImage</p></td>
<td align="left"><p>Aplica un objeto DartConfiguration a una imagen de Windows montada. Esto incluye agregar todos los archivos, la configuración y las dependencias de paquetes.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Administración de DaRT 10 mediante PowerShell](administering-dart-10-using-powershell.md)

 

 





