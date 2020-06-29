---
title: Registros de eventos de cliente
description: Registros de eventos de cliente
author: dansimp
ms.assetid: d5c2f270-db6a-45f1-8557-8c6fb28fd568
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7324d07bf018944fcbe24168bba2e9abea9cea41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824191"
---
# Registros de eventos de cliente

Los registros de eventos de MBAM se encuentran en visor de eventos: registros de aplicaciones y servicios – Microsoft – Windows – MBAM-Operational path.
La tabla siguiente contiene los identificadores de eventos que se pueden producir en el cliente de MBAM.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Id. de evento</th>
<th align="left">Canal</th>
<th align="left">Símbolo de evento</th>
<th align="left">Mensaje</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>uno</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>VolumeEnactmentSuccessful</p></td>
<td align="left"><p>Las directivas de MBAM se aplicaron correctamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>1</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>VolumeEnactmentFailed</p></td>
<td align="left"><p>Se produjo un error al aplicar las directivas de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>2</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>TransferStatusDataSuccessful</p></td>
<td align="left"><p>Los datos de estado de cifrado se enviaron correctamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>cuatro</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>TransferStatusDataFailed</p></td>
<td align="left"><p>Se produjo un error al enviar datos de estado de cifrado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4,8</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>SystemVolumeNotFound</p></td>
<td align="left"><p>Falta el volumen del sistema. SystemVolume es necesario para cifrar la unidad del sistema operativo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>99,999</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>TPMNotFound</p></td>
<td align="left"><p>Falta el hardware TPM. Se necesita TPM para cifrar la unidad del sistema operativo con cualquier protector de TPM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>base10</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>MachineHWExempted</p></td>
<td align="left"><p>El equipo está exento del cifrado. Estado del hardware de la máquina: excluido</p></td>
</tr>
<tr class="even">
<td align="left"><p>once</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>MachineHWUnknown</p></td>
<td align="left"><p>El equipo está exento del cifrado. Estado del hardware de la máquina: desconocido</p></td>
</tr>
<tr class="odd">
<td align="left"><p>2007</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>HWCheckFailed</p></td>
<td align="left"><p>Error al comprobar la exención de hardware.</p></td>
</tr>
<tr class="even">
<td align="left"><p>13</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>UserIsExempted</p></td>
<td align="left"><p>El usuario está exento del cifrado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>n°</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>UserIsWaiting</p></td>
<td align="left"><p>El usuario solicitó una exención.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,5</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>UserExemptionCheckFailed</p></td>
<td align="left"><p>Error en la comprobación de exención de usuario.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>apartado</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>UserPostponed</p></td>
<td align="left"><p>El usuario pospuso el proceso de cifrado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>apartado</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>TPMInitializationFailed</p></td>
<td align="left"><p>Error al inicializar TPM. El usuario rechazó los cambios de BIOS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>18</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>CoreServiceDown</p></td>
<td align="left"><p>No se puede conectar con el servicio de hardware y recuperación de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>19</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>CoreServiceUp</p></td>
<td align="left"><p>Se ha conectado correctamente al servicio de hardware y recuperación de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>veinte</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>PolicyMismatch</p></td>
<td align="left"><p>La Directiva MBAM está en conflicto o está dañada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>21Vianet</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>ConflictingOSVolumePolicies</p></td>
<td align="left"><p>Se detectaron conflictos de directivas de cifrado de volumen de so. Comprobar las directivas de BitLocker y MBAM relacionadas con los protectores de unidad de OS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>23</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>ConflictingFDDVolumePolicies</p></td>
<td align="left"><p>Se detectaron conflictos de directivas de cifrado de volumen de unidad de datos fijos. Comprobar las directivas de BitLocker y MBAM relacionadas con protectores de unidad FDD.</p></td>
</tr>
<tr class="even">
<td align="left"><p>,27</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>EncryptionFailedNoDra</p></td>
<td align="left"><p>Se produjo un error durante el cifrado. Es necesario un protector de agente de recuperación de datos (DRA) en el modo FIPS para equipos anteriores a Windows 8,1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>apartado</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>TpmOwnerAuthEscrowed</p></td>
<td align="left"><p>El TPM OwnerAuth se ha enviado a un depósito de garantía.</p></td>
</tr>
<tr class="even">
<td align="left"><p>32</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>RecoveryKeyEscrowed</p></td>
<td align="left"><p>La clave de recuperación de BitLocker para el volumen se ha enviado un depósito de garantía.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>0,30</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>RecoveryKeyReset</p></td>
<td align="left"><p>La clave de recuperación de BitLocker para el volumen se ha actualizado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>35</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>EnforcePolicyDateSet</p></td>
<td align="left"><p>Se ha establecido la fecha de cumplimiento de la fecha, la fecha, <em> &lt; &gt; </em> para el volumen</p></td>
</tr>
<tr class="odd">
<td align="left"><p>32</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>EnforcePolicyDateCleared</p></td>
<td align="left"><p>Se <em> &lt; ha borrado la fecha de cumplimiento de la fecha y la fecha &gt; </em> de la Directiva.</p></td>
</tr>
<tr class="even">
<td align="left"><p>33</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>TpmLockOutResetSucceeded</p></td>
<td align="left"><p>Se restableció correctamente el bloqueo de TPM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>34</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>TpmLockOutResetFailed</p></td>
<td align="left"><p>Error al restablecer el bloqueo de TPM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>35</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalSucceeded</p></td>
<td align="left"><p>OwnerAuth de TPM recuperados correctamente de los servicios de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>36</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>TpmOwnerAuthRetrievalFailed</p></td>
<td align="left"><p>Error al recuperar el TPM OwnerAuth de los servicios de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>37</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>WmiProviderDllSearchPathUpdateFailed</p></td>
<td align="left"><p>Error al actualizar la ruta de búsqueda de archivos DLL para el proveedor WMI.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>38</p></td>
<td align="left"><p>Administrador</p></td>
<td align="left"><p>TimedOutWaitingForWmiProvider</p></td>
<td align="left"><p>El agente se ha detenido: ha agotado el tiempo de espera para la instancia de proveedor WMI de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>39</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>RemovableDriveMounted</p></td>
<td align="left"><p>Se montó la unidad extraíble.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>40</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>RemovableDriveDismounted</p></td>
<td align="left"><p>Se desmontó la unidad extraíble.</p></td>
</tr>
<tr class="even">
<td align="left"><p>41</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>FailedToEnactEndpointUnreachable</p></td>
<td align="left"><p>Si se produce un error al conectarse al servicio de hardware y recuperación de MBAM no se pudieron aplicar al volumen las directivas de MBAM correctamente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>42</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>FailedToEnactLockedVolume</p></td>
<td align="left"><p>El estado de volumen bloqueado evitó que las directivas de MBAM se aplicaran correctamente al volumen.</p></td>
</tr>
<tr class="even">
<td align="left"><p>43</p></td>
<td align="left"><p>Funcionamiento</p></td>
<td align="left"><p>TransferStatusDataFailedEndpointUnreachable</p></td>
<td align="left"><p>Si se produce un error al conectarse al servicio de cumplimiento y estado de MBAM, no se podrán transferir los datos de estado de cifrado.</p></td>
</tr>
</tbody>
</table>

 


## Temas relacionados
[Referencia técnica de MBAM 2.5](technical-reference-for-mbam-25.md)

[Registros de eventos de servidor](server-event-logs.md)

 


## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





