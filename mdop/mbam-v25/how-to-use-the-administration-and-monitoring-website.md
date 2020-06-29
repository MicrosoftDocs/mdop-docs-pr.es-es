---
title: Cómo usar el sitio web de administración y supervisión
description: Cómo usar el sitio web de administración y supervisión
author: dansimp
ms.assetid: bb96a4e8-d4f4-4e6f-b7db-82d96998bfa6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9b9597e29a5a7a6236cb351d8d6d1f682edce3cf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813046"
---
# Cómo usar el sitio web de administración y supervisión


El sitio web de administración y supervisión, también conocido como soporte técnico, es una interfaz administrativa para el cifrado de unidad BitLocker. Use el sitio web para revisar los informes, recuperar las unidades de los usuarios finales y administrar los TPMs de los usuarios finales, tal y como se describe en las secciones siguientes.

**Nota:**  Si está usando MBAM en la topología independiente, verá todos los informes del sitio web de administración y supervisión. Si está usando la topología de integración de Configuration Manager, verá todos los informes en Configuration Manager, excepto el informe de auditoría de recuperación, que se sigue visualizando desde el sitio web de administración y supervisión. Para obtener más información sobre los informes, consulte [supervisión e informes de compatibilidad con BitLocker con MBAM 2,5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md).

 

## Roles necesarios para usar el sitio web de administración y supervisión


Para acceder a áreas específicas del sitio web de administración y supervisión, debe tener uno de los siguientes roles, que son grupos que ha creado en Active Directory. Puede usar cualquier nombre para estos grupos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Cuenta</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MBAM los usuarios avanzados del servicio de asistencia</p></td>
<td align="left"><p>Proporciona acceso a todas las áreas del sitio web de administración y supervisión. Los usuarios que tienen este rol solo tienen que escribir la clave de recuperación, y no el dominio del usuario final y el nombre de usuario, al ayudar a los usuarios finales a recuperar sus unidades. Si un usuario es miembro del grupo de usuarios del Departamento de soporte técnico de MBAM y del grupo de usuarios del Departamento de soporte técnico avanzado, los permisos del grupo usuarios del servicio de asistencia avanzada anularán los permisos del grupo MBAM de soporte técnico.</p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuarios de MBAM Helpdesk</p></td>
<td align="left"><p>Proporciona acceso a las áreas administrar TPM y recuperación de unidades del sitio web de administración y supervisión. Las personas que tienen este rol deben rellenar todos los campos, incluidos el dominio y el nombre de la cuenta del usuario final, cuando usan cualquiera de los dos áreas.</p>
<p>Si un usuario es miembro del grupo de usuarios del Departamento de soporte técnico de MBAM y del grupo de usuarios del Departamento de soporte técnico avanzado, los permisos del grupo usuarios del servicio de asistencia avanzada anularán los permisos del grupo MBAM de soporte técnico.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usuarios de informes de MBAM</p></td>
<td align="left"><p>Proporciona acceso a los informes en el <strong> </strong> área informes del sitio web de administración y supervisión.</p></td>
</tr>
</tbody>
</table>

 

## Tareas que puede realizar en el sitio web de administración y supervisión


En la tabla siguiente se resumen las tareas que puede realizar en el sitio web de administración y supervisión, y se proporcionan vínculos a más información sobre cada tarea.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Área del sitio web donde se accede a la tarea</th>
<th align="left">Descripción</th>
<th align="left">Para más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ver informes</p></td>
<td align="left"><p>Informes</p></td>
<td align="left"><p>Le permite ejecutar informes para supervisar el uso de BitLocker, el cumplimiento y la actividad de recuperación de claves. Los informes proporcionan datos sobre el cumplimiento de la empresa, los equipos individuales y los que solicitaron claves de recuperación o el paquete de OwnerAuth de TPM para un equipo específico.</p></td>
<td align="left"><p><a href="viewing-mbam-25-reports-for-the-stand-alone-topology.md" data-raw-source="[Viewing MBAM 2.5 Reports for the Stand-alone Topology](viewing-mbam-25-reports-for-the-stand-alone-topology.md)">Visualización de informes MBAM 2.5 para topología independiente</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Determinar el estado de cifrado de BitLocker de equipos perdidos o robados</p></td>
<td align="left"><p>Informes</p></td>
<td align="left"><p>Determine si un volumen se cifró si el equipo se ha perdido o ha sido robado.</p></td>
<td align="left"><p><a href="how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md" data-raw-source="[How to Determine BitLocker Encryption State of Lost Computers](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-25.md)">Cómo determinar el estado de cifrado de BitLocker de equipos perdidos</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Recuperar unidades perdidas</p></td>
<td align="left"><p>Recuperación de unidades</p></td>
<td align="left"><p>Recuperar unidades que son:</p>
<ul>
<li><p>En modo de recuperación</p></li>
<li><p>Se han movido</p></li>
<li><p>Están dañados</p></li>
</ul></td>
<td align="left"><ul>
<li><p><a href="how-to-recover-a-drive-in-recovery-mode-mbam-25.md" data-raw-source="[How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-25.md)">Cómo recuperar una unidad en modo de recuperación</a></p></li>
<li><p><a href="how-to-recover-a-moved-drive-mbam-25.md" data-raw-source="[How to Recover a Moved Drive](how-to-recover-a-moved-drive-mbam-25.md)">Cómo recuperar una unidad que se ha movido</a></p></li>
<li><p><a href="how-to-recover-a-corrupted-drive-mbam-25.md" data-raw-source="[How to Recover a Corrupted Drive](how-to-recover-a-corrupted-drive-mbam-25.md)">Cómo recuperar una unidad dañada</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Restablecer un bloqueo de TPM</p></td>
<td align="left"><p>Administrar TPM</p></td>
<td align="left"><p>Proporciona acceso a datos de TPM recopilados por el cliente de MBAM. En un bloqueo de TPM, use el sitio web de administración y supervisión para recuperar el archivo de contraseñas necesario para desbloquear el TPM.</p></td>
<td align="left"><p><a href="how-to-reset-a-tpm-lockout-mbam-25.md" data-raw-source="[How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-25.md)">Cómo restablecer un bloqueo de TPM</a></p></td>
</tr>
</tbody>
</table>

 


## Temas relacionados


[Realización de la administración de BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





