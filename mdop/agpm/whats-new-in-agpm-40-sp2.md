---
title: Novedades de AGPM 4.0 SP2
description: Novedades de AGPM 4.0 SP2
author: dansimp
ms.assetid: 5c0dcab4-f27d-4153-8b8e-b280b080be51
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56369207780cf0795f16eda91f249a26270c4b47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818150"
---
# Novedades de AGPM 4.0 SP2


Este contenido describe las mejoras y las configuraciones admitidas para el Service Pack 2 de administración avanzada de directivas de grupo (AGPM) 4.0 de Microsoft. Si hay una diferencia entre este contenido y otra documentación de AGPM, tenga en cuenta que este contenido es autoritativo y asuma que reemplaza a la otra documentación.

## <a href="" id="what-s-new"></a>Novedades


AGPM 4.0 SP2 admite las siguientes características y funcionalidades.

### Compatibilidad con Windows 8.1 y Windows Server2012 R2

AGPM 4.0 SP2 agrega compatibilidad para los sistemas operativos Windows 8.1 y Windows Server2012 R2.

### Extensiones de cliente nuevas y modificadas

Las extensiones de cliente de la Directiva de grupo se han agregado o cambiado para que AGPM admita la nueva configuración de directiva en Windows 8.1. Esta configuración de directiva permite que los administradores de directivas de grupo administren y realicen un seguimiento de configuraciones de directiva específicas de Windows 8.1 que cambian entre dos objetos de directiva de grupo (GPO) o plantillas. Para ver las extensiones de cliente, use la configuración y los informes de diferencias que están disponibles en el cliente de AGPM.

Las extensiones del cliente de directiva de grupo nuevas y modificadas son:

-   **Especificar la configuración de las carpetas de trabajo** Si habilita esta configuración de Directiva, los administradores de TI podrán configurar las carpetas de trabajo para que se creen automáticamente. La característica carpetas de trabajo permite a los usuarios finales sincronizar los archivos de sus dispositivos de escritorio de Windows con los otros dispositivos. Use esta configuración de directiva para crear la relación de sincronización en los dispositivos de un usuario final y para configurar cómo identificar el servidor de archivos que almacena las carpetas de trabajo del usuario. Si selecciona la casilla de verificación **sincronización de provisionamiento automático** , se creará el perfil de sincronización sin la intervención del usuario y los datos comenzarán automáticamente la sincronización con el dispositivo del usuario. Si no activa la casilla de verificación **sincronización automática** , los usuarios deben proporcionar una entrada para iniciar la sincronización.

-   **Forzar la configuración automática para todos los usuarios**. Si habilita esta configuración de Directiva, los administradores de TI podrán determinar si deben crear la Asociación de carpetas de trabajo automáticamente en los dispositivos de usuario final sin la entrada de los usuarios finales. Si habilita esta configuración de Directiva, la sincronización se establecerá de acuerdo con la forma en que configure la configuración de directiva **especificar carpetas de trabajo** . Si establece la configuración de directiva **forzar la configuración automática de todos los usuarios** como **deshabilitada** o **no configurada**, la relación de las carpetas de trabajo se configurará según cómo establezca la opción de **aprovisionamiento automático** en la opción **especificar la configuración de las carpetas de trabajo** .

Para obtener más información sobre la característica carpetas de trabajo, consulte [Introducción a carpetas de trabajo](https://go.microsoft.com/fwlink/?LinkId=330444).

### Comentarios de los clientes y Resumen de revisiones

AGPM 4.0 SP2 incluye un resumen de las revisiones para solucionar los problemas encontrados desde la versión de AGPM 4.0 Service Pack1 (SP1). AGPM 4.0 SP2 contiene las últimas revisiones hasta el Service Pack 1 de Microsoft Advanced Group Management 4.0 Hotfix1. Para obtener más información, consulte el artículo [2873472](https://go.microsoft.com/fwlink/?LinkId=325400)de Knowledge base.

### Nuevas extensiones de directiva de grupo en la configuración y los informes de diferencias

Las nuevas extensiones de directiva de grupo se han agregado a los informes de diferencias y configuración.

### Cambios de instalación y soporte técnico

Los cambios y la compatibilidad con el instalador de AGPM 4.0 SP2 son:

-   Si instala AGPM 4.0 SP2 en el sistema operativo Windows 8 o Windows Server 2012 o en sistemas operativos posteriores, el instalador de AGPM verifica que se instale el software previo necesario (la consola de administración de directivas de grupo (GPMC) y Microsoft .NET Framework 3.5). Si no se instala este software necesario, la instalación de AGPM 4.0 SP2 está bloqueada.

-   Al instalar el servidor de AGPM, la activación de WCF, la activación no HTTP y el servicio de activación de procesos de Windows se habilitan automáticamente.

-   En el sistema operativo cliente vista y versiones posteriores, descargue la versión adecuada de las herramientas de administración remota del sistema para su sistema operativo antes de instalar AGPM 4.0 SP2.

-   AGPM 4.0 SP2 admite compatibilidad con versiones anteriores de sistemas operativos compatibles.

### Posibilidad de actualizar a AGPM 4.0 SP2 sin volver a escribir los parámetros de configuración

Puede actualizar el cliente de AGPM o el servidor AGPM a el SP2 de AGPM 4.0 sin que se le pida que vuelva a escribir los parámetros de configuración (denominado actualización inteligente) solo de AGPM 4.0 en adelante, como se muestra en la tabla siguiente. Si va a actualizar a AGPM 4.0 SP2 desde otras versiones de AGPM, como se muestra en la tabla, debe usar la actualización clásica, que requiere volver a introducir los parámetros de configuración. Como cada versión de AGPM está asociada a un sistema operativo en particular, consulte [elegir qué versión de AGPM instalar](https://go.microsoft.com/fwlink/?LinkId=254350) y asegurarse de que actualiza el sistema operativo según corresponda antes de actualizar AGPM.

**Actualizaciones admitidas por AGPM 4,0 SP2**

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Versión de AGPM desde la que se puede actualizar</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3,0</strong></p></td>
<td align="left"><p><strong>4,0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
<td align="left"><p><strong>4,0 SP2</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>Actualización clásica</p></td>
<td align="left"><p>Actualización clásica</p></td>
<td align="left"><p>La instalación está bloqueada</p></td>
<td align="left"><p>La instalación está bloqueada</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3,0</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>Actualización clásica</p></td>
<td align="left"><p>La instalación está bloqueada</p></td>
<td align="left"><p>La instalación está bloqueada</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>Actualización inteligente</p></td>
<td align="left"><p>Actualización inteligente</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4,0 SP1</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>Actualización inteligente</p></td>
</tr>
</tbody>
</table>

 

## Configuraciones admitidas


AGPM 4.0 SP2 admite las configuraciones de la tabla siguiente. Aunque AGPM admite configuraciones mixtas, le recomendamos encarecidamente que ejecute el cliente AGPM y el servidor AGPM en la misma línea del sistema operativo, por ejemplo, Windows 8.1 con Windows Server2012 R2, Windows 8 con Windows Server 2012, etc.

**Configuración de directiva y sistemas operativos compatibles con el SP2 de AGPM 4.0**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Configuraciones admitidas para el servidor de AGPM</strong></th>
<th align="left"><strong>Configuraciones admitidas para el cliente de AGPM</strong></th>
<th align="left"><strong>Compatibilidad con AGPM</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Se admite</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012, Windows 8.1 o Windows 8</p></td>
<td align="left"><p>Windows Server 2012 o Windows 8</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1 o Windows 8</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</p></td>
<td align="left"><p>Windows Server2008 o vista con Service Pack 1 (SP1)</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 o Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</p></td>
<td align="left"><p>No se admite</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Compatible pero no puede editar o modificar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1, Windows 8 o Windows7</p></td>
</tr>
</tbody>
</table>

 

## Requisitos previos para instalar AGPM 4.0 SP2


En la siguiente tabla se describe el comportamiento de los instaladores de cliente y de servidor de AGPM 4.0 SP2 en Windows 8.1 cuando falta la versión 3.5 de .NET Framework o la GPMC en las herramientas de administración remota del servidor.

**Cliente AGPM**

**Servidor de AGPM**

**Sistema operativo**

**.NET Framework**

**Herramientas de administración remota del servidor**

**.NET Framework**

**Herramientas de administración remota del servidor**

**Windows 8.1**

Si .NET Framework 3.5 no está habilitado ni instalado, el instalador bloquea la instalación.

Si la GPMC no está habilitada ni instalada, el instalador bloquea la instalación.

Si .NET Framework 3.5 no está habilitado ni instalado, el instalador bloquea la instalación.

Si la GPMC no está habilitada ni instalada, el instalador bloquea la instalación.

**Windows Server2012 R2**

Si .NET Framework 3.5 no está habilitado ni instalado, el instalador bloquea la instalación.

Si la GPMC no está habilitada, el instalador la habilita durante la instalación.

Si .NET Framework 3.5 no está habilitado ni instalado, el instalador bloquea la instalación.

Si la GPMC no está habilitada, el instalador la habilita durante la instalación.

 

## Cómo obtener tecnologías de MDOP


AGPM 4,0 SP2 forma parte del paquete de optimización de escritorio de Microsoft (MDOP). MDOP es parte de Microsoft Software Assurance. Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Temas relacionados


[Administración avanzada de directivas de grupo](index.md)

[Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP2](release-notes-for-microsoft-advanced-group-policy-management-40-sp2.md)

[Elección de qué versión de AGPM ha de instalarse](choosing-which-version-of-agpm-to-install.md)

 

 





