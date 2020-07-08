---
title: Novedades de AGPM 4.0 SP1
description: Novedades de AGPM 4.0 SP1
author: dansimp
ms.assetid: c6a3d94a-13c3-44e6-a466-c3011879999e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca1ee4a1c2eb943a25246dc31b127eaf72ff5fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818151"
---
# Novedades de AGPM 4.0 SP1


Este contenido de "Novedades" describe las mejoras y las configuraciones admitidas para la administración avanzada de directivas de grupo (AGPM) 4,0 de Microsoft. Si hay una diferencia entre este contenido y otra documentación de AGPM, este contenido debe considerarse autoritario y debe reemplazar el contenido incluido en este producto.

## <a href="" id="what-s-new"></a>Novedades


AGPM 4,0 SP1 admite las siguientes mejoras:

### Extensiones de cliente nuevas y modificadas

Se han agregado o cambiado extensiones de cliente de la Directiva de grupo (CSE) para que AGPM admita las nuevas directivas de grupo en Windows 8 y Windows Server 2012. Estas directivas de Grupo permiten a los administradores de directivas de grupo administrar y realizar un seguimiento de la configuración específica de la Directiva de grupo de Windows 8 que cambian entre dos objetos de directiva de grupo (GPO) o plantillas. También puede crear GPO personalizados, con la configuración específica de Windows 8, y configurar y guardar los GPO como una plantilla. Para ver las CSE, use los informes de configuración y de diferencias que están disponibles en el cliente AGPM 4,0 SP1.

Las extensiones del cliente de directiva de grupo nuevas y modificadas son:

-   **Directiva de acceso central:** Permite a los administradores de la Directiva de grupo especificar directivas de acceso central en servidores de directivas de grupo, por ejemplo, servidores de archivos. La Directiva de acceso central es una directiva de autorización que se especifica mediante un elemento de GPO y que se aplica a los destinos de directiva para facilitar el acceso centralizado y el control de los recursos. Estas directivas de acceso centralizado se deben configurar en un equipo cliente de directiva de grupo desde Active Directory. Una directiva de grupo distribuye el conocimiento de una directiva de acceso central aplicable a los equipos que deben exigirlo.

-   **Cambios en la Directiva de resolución de nombres:** Permite a los administradores de la Directiva de grupo establecer la configuración de la seguridad DNS y DirectAccess en equipos cliente DNS. Se han agregado nuevas pestañas para configurar la configuración del servidor DNS genérico y la configuración de la codificación.

-   **Cambios de preferencias de directiva de Grupo:** Agrega compatibilidad para la configuración y administración de la configuración de Internet Explorer 10 que se agregó para Windows 8.

-   **Conexiones de escritorio y aplicaciones remotas:** Permite a los administradores de directivas de grupo especificar la dirección URL de conexión predeterminada que se usa para las conexiones de escritorio y de aplicaciones remotas.

-   **Opciones de inicio de Windows to Go:** Permite a los administradores de directivas de grupo configurar si el equipo arrancará en Windows to go si un dispositivo USB que contiene un área de trabajo de Windows to go está conectado.

-   **Opciones de hibernación de Windows to Go:** Permite a los administradores de directivas de grupo configurar si un equipo puede usar el estado de suspensión de hibernación (S4) cuando el equipo se inicia desde un área de trabajo de Windows to go.

### Comentarios de los clientes y Resumen de revisiones

AGPM 4,0 SP1 incluye un resumen de correcciones para resolver los problemas encontrados desde la versión de AGPM 4,0. AGPM 4,0 SP1 contiene las últimas revisiones hasta el Hotfix 1 de 4,0 administración avanzada de directivas de grupo de Microsoft (incluido).

### La configuración y los informes de diferencias muestran las nuevas extensiones de directiva de grupo

Las nuevas extensiones de directiva de grupo se han agregado a los informes de diferencias y configuración.

### Cambios de instalación y soporte técnico

Los cambios y la compatibilidad con el instalador de AGPM 4,0 SP1 son:

-   Si instala AGPM 4,0 SP1 en Windows 8 o Windows Server 2012, el instalador de AGPM verifica que se instale el software previo requerido (consola de administración de directivas de grupo y .NET 3,5 Framework). Si estos requisitos previos no están instalados, la instalación de AGPM 4,0 SP1 está bloqueada.

-   Al instalar AGPM 4,0 SP1, la activación de WCF, la activación no HTTP y el servicio de activación de procesos de Windows se habilitan automáticamente.

-   En los sistemas operativos Windows Vista, Windows 7 y Windows 8, descargue la versión adecuada del kit de herramientas de administración de sistemas remoto para su sistema operativo antes de instalar AGPM 4,0 SP1.

-   Se admite la compatibilidad con versiones anteriores de sistemas operativos compatibles.

### Capacidad de actualizar o actualizar a AGPM 4,0 SP1 sin volver a especificar parámetros de configuración

Puede actualizar el cliente o servidor de AGPM a AGPM 4,0 SP1 solo de AGPM 4,0 sin que se le pida que vuelva a escribir los parámetros de configuración (denominado "actualización inteligente"), como se muestra en la tabla siguiente. Si va a actualizar a AGPM 4,0 SP1 desde otras versiones de AGPM, como se muestra en la tabla, debe usar la "actualización clásica", que requiere volver a introducir los parámetros de configuración. Como cada versión de AGPM está asociada a un sistema operativo en particular, consulte [elegir la versión de AGPM que se instalará](https://go.microsoft.com/fwlink/?LinkId=254350)y asegúrese de actualizar el sistema operativo según corresponda antes de realizar una actualización.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Versión de AGPM desde la que se puede actualizar</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3,0</strong></p></td>
<td align="left"><p><strong>4,0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>No aplicable</p></td>
<td align="left"><p>Actualización clásica</p></td>
<td align="left"><p>Actualización clásica</p></td>
<td align="left"><p>La instalación está bloqueada</p></td>
</tr>
<tr class="odd">
<td align="left"><p>3,0</p></td>
<td align="left"><p>No aplicable</p></td>
<td align="left"><p>No aplicable</p></td>
<td align="left"><p>Actualización clásica</p></td>
<td align="left"><p>La instalación está bloqueada</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0</p></td>
<td align="left"><p>No aplicable</p></td>
<td align="left"><p>No aplicable</p></td>
<td align="left"><p>No aplicable</p></td>
<td align="left"><p>Actualización inteligente</p></td>
</tr>
</tbody>
</table>

 

## Configuraciones admitidas


AGPM admite las configuraciones de la tabla siguiente. Aunque AGPM admite configuraciones mixtas, se recomienda encarecidamente que ejecute el servidor y el cliente de AGPM en la misma familia de sistemas operativos, por ejemplo, Windows 8 con Windows Server 2012, Windows 7 con Windows Server 2008 R2, etc.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configuraciones admitidas para el servidor AGPM 4,0 SP1</strong></p></td>
<td align="left"><p><strong>Configuraciones compatibles para clientes AGPM 4,0 SP1</strong></p></td>
<td align="left"><p><strong>Soporte técnico de AGPM 4,0 SP1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8 o Windows Server 2012</p></td>
<td align="left"><p>Windows 8 o Windows Server 2012</p></td>
<td align="left"><p>Se admite</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2 o Windows 7</p></td>
<td align="left"><p>Windows Server 2008 R2 o Windows 7</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2, Windows 7 o Windows 8 o Windows Server 2012</p></td>
<td align="left"><p>Windows Server 2008 o Windows Vista con Service Pack 1</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server 2008 R2, Windows 7 o Windows 8.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 o Windows Vista con Service Pack 1</p></td>
<td align="left"><p>Windows Server 2008 R2, Windows 7 o Windows 8 o Windows Server 2012</p></td>
<td align="left"><p>Se admite</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 o Windows Vista con Service Pack 1</p></td>
<td align="left"><p>Windows Server 2008 o Windows Vista con Service Pack 1</p></td>
<td align="left"><p>Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server 2008 R2 o Windows 7 o Windows 8</p></td>
</tr>
</tbody>
</table>

 

## Requisitos previos para instalar AGPM 4,0 SP1


La siguiente tabla describe el comportamiento en Windows 8 de los instaladores de cliente y de servidor de AGPM 4,0 SP1 cuando falta .NET 3,5 o la consola de administración de directivas de grupo en las herramientas de administración de servidor remoto (RSAT).

**Cliente AGPM 4,0 SP1**

**Servidor AGPM 4,0 SP1**

**Sistema operativo**

**.NET**

**RSAT**

**.NET**

**RSAT**

**Windows 8**

Si .NET 3,5 no está habilitado ni instalado, el instalador bloquea la instalación.

Si GPMC no está habilitado ni instalado en el sistema, el instalador bloquea la instalación.

Si .NET 3,5 no está habilitado ni instalado, el instalador bloquea la instalación.

Si GPMC no está habilitado ni instalado en el sistema, el instalador bloquea la instalación.

**Windows Server 2012**

Si .NET 3,5 no está habilitado ni instalado, el instalador bloquea la instalación.

Si la consola GPMC no está habilitada, el instalador la habilita durante la instalación.

Si .NET 3,5 no está habilitado ni instalado, el instalador bloquea la instalación.

Si la consola GPMC no está habilitada, el instalador la habilita durante la instalación.

 

## Temas relacionados


[Administración avanzada de directivas de grupo](index.md)

[Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP1](release-notes-for-microsoft-advanced-group-policy-management-40-sp1.md)

 

 





