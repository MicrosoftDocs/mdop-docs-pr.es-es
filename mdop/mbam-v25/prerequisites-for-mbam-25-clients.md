---
title: Requisitos previos para clientes MBAM 2.5
description: Requisitos previos para clientes MBAM 2.5
author: dansimp
ms.assetid: fc230679-9c84-4b99-a77c-bae7e7bf8145
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: ac5e211e5ea038f47db3d5e68155eb5af38aa231
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826970"
---
# Requisitos previos para clientes MBAM 2.5


Antes de instalar el software de cliente de MBAM en los equipos de los usuarios finales, asegúrese de que el entorno y los equipos cliente cumplan los siguientes requisitos previos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Como requisito previo</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>El dominio de la empresa debe contener al menos un controlador de dominio de Windows Server 2008 (o posterior).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>El equipo cliente debe haber iniciado sesión en la intranet de la empresa.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Solo para equipos cliente de Windows 7: cada cliente debe tener capacidad de módulo de plataforma segura (TPM) (TPM 1,2 o posterior).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Para equipos cliente con Windows 8,1, Windows 10 RTM o Windows 10 versión 1511 solamente: Si desea que MBAM pueda almacenar y administrar las claves de recuperación de TPM, el aprovisionamiento automático de TPM debe estar desactivado, y MBAM debe estar configurado como propietario de TPM antes de implementar MBAM.</p>
<p>Solo en el SP1 de MBAM 2,5, ya no necesita desactivar el aprovisionamiento automático de TPM, pero debe asegurarse de que los objetos de directiva de grupo de TPM estén establecidos en no custodiar TPM OwnerAuth a Active Directory.</p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md#bkmk-tpm" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm)">Consideraciones sobre seguridad de MBAM 2.5</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Para Windows 10, versión 1607 o posterior, solo Windows puede tomar posesión de TPM. En addiiton, Windows no conservará la contraseña de propietario de TPM al aprovisionar el TPM.</p>
<p>En MBAM 2,5 SP1, debe activar el aprovisionamiento automático.</p>
</p></td>
<td align="left"><p>Para obtener más información, consulta la <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)"> contraseña </a> de propietario de TPM.
</p></td>
</tr>
<tr class="even">
<td align="left"><p>El chip TPM debe estar activado en el BIOS y puede reestablecerse desde el sistema operativo.</p></td>
<td align="left"><p>Para obtener más información, consulta la documentación del BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>El disco duro del equipo debe tener al menos dos particiones y debe tener el formato del sistema de archivos NTFS.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>El disco duro del equipo debe tener un BIOS que sea compatible con el TPM y que admita dispositivos USB durante el inicio del equipo.</p></td>
<td align="left"><div class="alert">
<strong>Nota</strong><br/><p>Asegúrese de que el teclado, el vídeo o el ratón estén directamente conectados y no sean administrados mediante un teclado, un vídeo o un conmutador de ratón (KVM). Un conmutador KVM puede interferir con la capacidad del equipo de detectar la presencia física del hardware.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Si usas un proxy, debe estar visible en el contexto del sistema. MBAM se ejecuta en el contexto del sistema, no en el contexto del usuario.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



**Importante**  
Si se usó BitLocker sin MBAM, MBAM se puede instalar y usar la información del TPM existente.




## Temas relacionados


[Configuraciones admitidas de MBAM 2.5](mbam-25-supported-configurations.md)

[Planificación de implementación de MBAM 2.5](planning-to-deploy-mbam-25.md)


## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






