---
title: Uso de Windows PowerShell para administrar MBAM 2.5
description: Uso de Windows PowerShell para administrar MBAM 2.5
author: dansimp
ms.assetid: 64668e76-2cba-433d-8d2d-50df0a4b2997
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 8db305bfbdf79723da2b186dd5cc00406a4089cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812735"
---
# Uso de Windows PowerShell para administrar MBAM 2.5


En este tema se describen los cmdlets de Windows PowerShell para administración y supervisión de Microsoft BitLocker (MBAM) que se relacionan con la recuperación de equipos o unidades cuando los usuarios se bloquean.

Para conocer los cmdlets que usa para configurar las características del servidor de MBAM, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

## <a href="" id="cmdlets-for-recovering-computers-or-drives-that-are-managed-by-mbam-"></a>Cmdlets para recuperar equipos o unidades administrados por MBAM


Use los siguientes cmdlets de Windows PowerShell para recuperar equipos o unidades administrados por MBAM.

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
<td align="left"><p>Get-MbamBitLockerRecoveryKey</p></td>
<td align="left"><p>Solicita una clave de recuperación de MBAM que permite a los usuarios desbloquear un equipo o una unidad cifrada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Get-MbamTPMOwnerPassword</p></td>
<td align="left"><p>Proporciona a los usuarios una contraseña de propietario de TPM que pueden usar para desbloquear un módulo de plataforma segura (TPM) cuando el TPM ha bloqueado y ya no aceptan su PIN.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-cmdlet-help"></a> Ayuda del cmdlet MBAM


La ayuda de Windows PowerShell para cmdlets de MBAM está disponible en los siguientes formatos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato de ayuda de Windows PowerShell</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>En un símbolo del sistema de Windows PowerShell, escriba <strong> </strong> &lt; <em> cmdlet Get-Help</em>&gt;</p></td>
<td align="left"><p>Para cargar los cmdlets de Windows PowerShell más recientes, siga las instrucciones de <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"> configuración de las características de servidor de MBAM 2,5 mediante Windows PowerShell</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>En TechNet como páginas web</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>En el centro de descarga como un archivo. docx de Word</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>En el centro de descarga como un archivo. pdf</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 



## Temas relacionados


[Administración de funciones de MBAM 2.5](administering-mbam-25-features.md)

[Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





