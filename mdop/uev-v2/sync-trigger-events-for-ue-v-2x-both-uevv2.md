---
title: Eventos desencadenantes de sincronización para UE-V 2.x
description: Eventos desencadenantes de sincronización para UE-V 2.x
author: dansimp
ms.assetid: 4ed71a13-6a4f-4376-996f-74b126536bbc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f3e89a0370790e7f462b2f469792128dba033460
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826800"
---
# Eventos desencadenantes de sincronización para UE-V 2.x


Virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1 SP1 le permite sincronizar la configuración de la aplicación y de Windows en todos los dispositivos Unidos a un dominio. Los *eventos del desencadenador de sincronización* definen Cuándo UE-V Agent sincroniza esta configuración con la ubicación de almacenamiento de configuración. UE-V 2 presenta un nuevo *método de sincronización* denominado *SyncProvider*. Para obtener más información sobre la configuración del método de sincronización, vea [métodos de sincronización de UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).

## Eventos de activación de la UE-V 2 Sync


En la tabla siguiente se explican los eventos desencadenadores para las aplicaciones clásicas y la configuración de Windows.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Evento desencadenador de UE-V 2</strong></p></td>
<td align="left"><p><strong>SyncMethod = SyncProvider</strong></p></td>
<td align="left"><p><strong>SyncMethod = None</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Inicio de sesión de Windows</strong></p></td>
<td align="left"><ul>
<li><p>La configuración de la aplicación y de Windows se importa a la caché local desde la ubicación de almacenamiento de configuración.</p></li>
<li><p><a href="https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2" data-raw-source="[Asynchronous Windows settings](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings2)">Se aplica la configuración asincrónica de Windows </a> .</p></li>
<li><p>La configuración sincrónica de Windows se aplicará durante el siguiente inicio de sesión de Windows.</p></li>
<li><p>La configuración de la aplicación se aplicará cuando se inicie la aplicación.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>La configuración de la aplicación y de Windows se lee directamente desde la ubicación de almacenamiento de configuración.</p></li>
<li><p>Se aplica la configuración de Windows asincrónica y sincrónica.</p></li>
<li><p>La configuración de la aplicación se aplicará cuando se inicie la aplicación.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Cierre de sesión de Windows</strong></p></td>
<td align="left"><p>Almacenar los cambios localmente y en la caché y copiar la configuración de Windows asincrónica y sincrónica en el servidor de ubicación de almacenamiento de configuración, si está disponible</p></td>
<td align="left"><p>Almacenar los cambios en la ubicación de almacenamiento de configuración de Windows asincrónica y sincrónica</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Windows Connect (RDP)/desbloquear</strong></p></td>
<td align="left"><p>Sincronice cualquier configuración asincrónica de Windows desde la ubicación de almacenamiento de configuración a la caché local, si está disponible.</p>
<p>Aplicar la configuración de Windows en caché</p></td>
<td align="left"><p>Descargar y aplicar la configuración asincrónica de Windows desde la ubicación de almacenamiento de configuración</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Desconexión de Windows (RDP)/bloqueo</strong></p></td>
<td align="left"><p>Almacenar los cambios de la configuración asincrónica de Windows en la memoria caché local.</p>
<p>Sincronizar la configuración asincrónica de Windows de la memoria caché local con la ubicación de almacenamiento de configuración, si está disponible</p></td>
<td align="left"><p>Almacenar cambios de configuración de Windows asincrónicos en la ubicación de almacenamiento de configuración</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Inicio de la aplicación</strong></p></td>
<td align="left"><p>Aplicar la configuración de la aplicación desde la memoria caché local mientras se inicia la aplicación</p></td>
<td align="left"><p>Aplicar la configuración de la aplicación desde la ubicación de almacenamiento de configuración cuando se inicia la aplicación</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>La aplicación se cierra</strong></p></td>
<td align="left"><p>Almacenar los cambios de configuración de la aplicación en la memoria caché local y copiar la configuración en la ubicación de almacenamiento de configuración, si está disponible</p></td>
<td align="left"><p>Almacenar cualquier cambio de configuración de la aplicación en la ubicación de almacenamiento de configuración</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>La tarea programada del controlador de sincronización o "sincronizar ahora" se ejecuta desde el centro de configuración de la compañía</strong></p>
<p></p></td>
<td align="left"><p>La configuración de la aplicación y de Windows se sincroniza entre la ubicación de almacenamiento de configuración y la memoria caché local.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Los cambios de configuración no se almacenan en caché localmente hasta que se cierra una aplicación. Este desencadenador no exportará los cambios realizados en una aplicación que se esté ejecutando.</p>
<p>Para la configuración de Windows, esto significa que los cambios no se guardarán en la caché local y se exportarán hasta el siguiente bloqueo (asincrónico) o cierre de sesión (asincrónicos y sincrónicos).</p>
</div>
<div>

</div>
<p>La configuración se aplica en estos casos:</p>
<ul>
<li><p>La configuración asincrónica de Windows se aplica directamente.</p></li>
<li><p>La configuración de la aplicación se aplica cuando se inicia la aplicación.</p></li>
<li><p>La configuración asincrónica y sincrónica de Windows se aplica durante el siguiente inicio de sesión de Windows.</p></li>
<li><p>La configuración de la aplicación de Windows (AppX) se aplicará durante la siguiente actualización. <a href="https://technet.microsoft.com/library/dn458944.aspx" data-raw-source="[Monitor Application Settings](https://technet.microsoft.com/library/dn458944.aspx)">Para obtener más información, vea supervisar la configuración de la aplicación </a> .</p></li>
</ul></td>
<td align="left"><p>NA</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Configuración asincrónica actualizada en el almacén remoto *</strong></p></td>
<td align="left"><p>Cargar y aplicar la nueva configuración asincrónica desde la memoria caché.</p></td>
<td align="left"><p>Cargar y aplicar la configuración del servidor central</p></td>
</tr>
</tbody>
</table>








## Temas relacionados


[Referencia técnica de UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

[Cambiar la frecuencia de UE-V 2. x tareas programadas](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md)

[Elija el método de configuración de UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#config)









