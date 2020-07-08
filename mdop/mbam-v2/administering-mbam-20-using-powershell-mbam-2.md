---
title: Administración de MBAM 2.0 con PowerShell
description: Administración de MBAM 2.0 con PowerShell
author: dansimp
ms.assetid: d785a8df-0a8c-4d70-abd2-93a762b4f3de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 736943e707b5d033b8ba6c26641393f02f0cdaf8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823501"
---
# Administración de MBAM 2.0 con PowerShell


Administración y supervisión de Microsoft BitLocker (MBAM) proporciona el siguiente conjunto de cmdlets de Windows PowerShell. Los administradores pueden usar estos cmdlets de PowerShell para realizar diversas tareas de servidor de supervisión y administración de Microsoft BitLocker desde la línea de comandos en lugar de desde el sitio web de administración de MBAM.

## Cómo administrar MBAM con PowerShell


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
<td align="left"><p>Install-Mbam</p></td>
<td align="left"><p>Instala las características de MBAM que proporcionan políticas avanzadas, cifrado, recuperación de claves y reporting de cumplimiento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Desinstalar-Mbam</p></td>
<td align="left"><p>Elimina las características de MBAM que proporcionan Directivas avanzadas, cifrado, recuperación de claves y herramientas de creación de informes de cumplimiento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Solicita una clave de recuperación de MBAM que permitirá a los usuarios desbloquear un equipo o una unidad cifrada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Proporciona a los usuarios una contraseña de propietario de TPM que pueden usar para desbloquear un módulo de plataforma segura (TPM) cuando el TPM ha bloqueado y ya no aceptan su PIN.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Operaciones para MBAM 2.0](operations-for-mbam-20-mbam-2.md)

 

 





