---
title: Determinación de por qué un dispositivo recibe un mensaje de no conformidad
description: Determinación de por qué un dispositivo recibe un mensaje de no conformidad
author: dansimp
ms.assetid: 793df330-a0ee-4759-b53a-95618ac74428
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/22/2017
ms.openlocfilehash: ce1d344676ebf4328506228f1bfa87c76e8036f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824571"
---
# Determinación de por qué un dispositivo recibe un mensaje de no conformidad


Los siguientes códigos de no cumplimiento son proporcionados por WMI y describen las razones por las que MBAM no cumple un determinado dispositivo.

Puede usar su método preferido para ver WMI. Si usa PowerShell, ejecute `gwmi -class mbam_volume -Namespace root\microsoft\mbam` desde un símbolo del sistema de PowerShell y busque ReasonsForNoncompliance.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Código de no conformidad</th>
<th align="left">Motivo del incumplimiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>,0</p></td>
<td align="left"><p>Intensidad de cifrado no AES 256.</p></td>
</tr>
<tr class="even">
<td align="left"><p>uno</p></td>
<td align="left"><p>La Directiva MBAM requiere que este volumen se Cifre, pero no lo está.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>1</p></td>
<td align="left"><p>La Directiva MBAM requiere que este volumen no se Cifre, pero sí.</p></td>
</tr>
<tr class="even">
<td align="left"><p>2</p></td>
<td align="left"><p>La Directiva MBAM requiere que este volumen use un protector TPM, pero no lo hace.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>cuatro</p></td>
<td align="left"><p>La Directiva MBAM requiere que este volumen use un protector de TPM + PIN, pero no lo hace.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4</p></td>
<td align="left"><p>La Directiva MBAM no permite que las máquinas que no sean de TPM se comuniquen como compatibles.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>6</p></td>
<td align="left"><p>El volumen tiene un protector de TPM pero el TPM no está visible (se arranca con la clave de recuperación después de deshabilitar TPM en el BIOS?).</p></td>
</tr>
<tr class="even">
<td align="left"><p>siete</p></td>
<td align="left"><p>La Directiva MBAM requiere que este volumen use un protector de contraseña, pero no tiene una.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4,8</p></td>
<td align="left"><p>La Directiva MBAM requiere que este volumen no use un protector de contraseña, pero tiene uno.</p></td>
</tr>
<tr class="even">
<td align="left"><p>99,999</p></td>
<td align="left"><p>La Directiva MBAM requiere que este volumen use un protector de desbloqueo automático, pero no tiene una.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>base10</p></td>
<td align="left"><p>La Directiva MBAM requiere que este volumen no use un protector de desbloqueo automático, pero tiene uno.</p></td>
</tr>
<tr class="even">
<td align="left"><p>once</p></td>
<td align="left"><p>Se detectó un conflicto de directiva que impide que MBAM informe de este volumen como compatible.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>2007</p></td>
<td align="left"><p>Se necesita un volumen del sistema para cifrar el volumen del sistema operativo, pero no está presente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>13</p></td>
<td align="left"><p>Se ha suspendido la protección del volumen.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>n°</p></td>
<td align="left"><p>Desbloqueo automático a menos que el volumen del sistema operativo esté cifrado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,5</p></td>
<td align="left"><p>La Directiva requiere una intensidad de cifrado mínima es XTS-AES-128 bit, la intensidad de cifrado real es más débil.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>apartado</p></td>
<td align="left"><p>La Directiva requiere una intensidad de cifrado mínima es XTS-AES-256 bit, la intensidad de cifrado real es más débil.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Referencia técnica de MBAM 2.5](technical-reference-for-mbam-25.md)

[Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





