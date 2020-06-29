---
title: Administración de MBAM 1.0 mediante el uso de PowerShell
description: Administración de MBAM 1.0 mediante el uso de PowerShell
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825140"
---
# Administración de MBAM 1.0 mediante el uso de PowerShell


Administración y supervisión de Microsoft BitLocker (MBAM) proporciona el siguiente conjunto de cmdlets de Windows PowerShell. Los administradores pueden usar estos cmdlets de PowerShell para realizar varias tareas de servidor MBAM desde el símbolo del sistema en lugar de desde el sitio web de administración de MBAM.

## Cómo administrar MBAM mediante PowerShell


Use los cmdlets de PowerShell que se describen aquí para administrar MBAM.

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
<td align="left"><p>Add-MbamHardwareType</p></td>
<td align="left"><p>Agrega un nuevo modelo de hardware al inventario de hardware de MBAM. Este cmdlet también puede especificar si el hardware es compatible o no compatible con el cifrado de unidad BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Solicita una clave de recuperación de MBAM que permitirá a un usuario desbloquear un equipo o una unidad cifrada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-MbamHardwareType</p></td>
<td align="left"><p>Obtiene un inventario de hardware maestro que contiene datos que indican si los modelos de hardware son compatibles o incompatibles con el cifrado de unidad BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Proporciona una contraseña de propietario de TPM para que un usuario pueda administrar su acceso de TPM (módulo de plataforma segura). Ayuda a los usuarios cuando el TPM ha bloqueado y ya no acepta su PIN.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Install-Mbam</p></td>
<td align="left"><p>Instala características de MBAM que proporcionan directivas de grupo avanzadas, cifrado, recuperación de claves y herramientas de creación de informes de cumplimiento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Remove-MbamHardwareType</p></td>
<td align="left"><p>Quita los modelos de hardware del inventario de hardware.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Set-MbamHardwareType</p></td>
<td align="left"><p>Permite la administración de un inventario de hardware maestro para designar si los modelos de hardware son compatibles o incompatibles con el cifrado de BitLocker.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Desinstalar-Mbam</p></td>
<td align="left"><p>Elimina las características de MBAM instaladas anteriormente que proporcionan Directivas avanzadas, cifrado, recuperación de claves y herramientas de creación de informes de cumplimiento.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Operaciones para MBAM 1.0](operations-for-mbam-10.md)

 

 





