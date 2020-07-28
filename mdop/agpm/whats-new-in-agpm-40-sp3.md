---
title: Novedades de AGPM 4.0 SP3
description: Novedades de AGPM 4.0 SP3
author: dansimp
ms.assetid: df495d55-9fbf-4f7e-a7af-3905f4f8790e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 44e7dc6c5de75ae3a5e5def638974bae20ad2a1e
ms.sourcegitcommit: 594b6e431af98562e0b806e224d2c5c7e07d2c77
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/27/2020
ms.locfileid: "10895774"
---
# Novedades de AGPM 4.0 SP3


Este contenido describe las mejoras y las configuraciones admitidas para el Service Pack 3 de administración avanzada de directivas de grupo (AGPM) 4.0 de Microsoft. Si hay una diferencia entre este contenido y otra documentación de AGPM, tenga en cuenta que este contenido es autoritativo y asuma que reemplaza a la otra documentación.

## <a href="" id="what-s-new"></a>Novedades


AGPM 4.0 SP3 admite las siguientes características y funcionalidades.

### Soporte técnico para Windows10

AGPM 4.0 SP3 agrega compatibilidad para los sistemas operativos Windows10 y Windows Server 2016.

### Compatibilidad con PowerShell

AGPM 4.0 SP3 agrega compatibilidad para los cmdlets de PowerShell. Para obtener una lista de los cmdlets disponibles en AGPM 4.0 SP3, incluidas las descripciones y la sintaxis, consulte [Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://docs.microsoft.com/powershell/mdop/get-started?view=win-mdop2-ps).

### Comentarios de los clientes y Resumen de revisiones

AGPM 4,0 SP3 incluye un resumen de todas las revisiones hasta la administración avanzada de directivas de grupo de Microsoft 4,0 SP2 y cualquier corrección de los problemas encontrados desde AGPM 4,0 SP2.

### Posibilidad de actualizar a AGPM 4.0 SP3 sin volver a especificar parámetros de configuración

Puede actualizar el cliente de AGPM o el servidor AGPM a AGPM 4.0 SP3 sin que se le pida que vuelva a introducir los parámetros de configuración (llamados Smart upgrade) solo de AGPM 4.0 y versiones posteriores, como se muestra en la tabla siguiente. Si va a actualizar a AGPM 4.0 SP3 desde otras versiones de AGPM, como se muestra en la tabla, debe usar la actualización clásica, que requiere volver a introducir los parámetros de configuración. Como cada versión de AGPM está asociada a un sistema operativo en particular, consulte [elegir qué versión de AGPM instalar](https://go.microsoft.com/fwlink/?LinkId=254350) y asegurarse de que actualiza el sistema operativo según corresponda antes de actualizar AGPM.

**Actualizaciones admitidas por AGPM 4,0 SP3**

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Versión de AGPM desde la que se puede actualizar</strong></p></td>
<td align="left"><p><strong>2,5</strong></p></td>
<td align="left"><p><strong>3,0</strong></p></td>
<td align="left"><p><strong>4,0</strong></p></td>
<td align="left"><p><strong>4,0 SP1</strong></p></td>
<td align="left"><p><strong>4,0 SP2</strong></p></td>
<td align="left"><p><strong>4,0 SP3</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>2,5</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>Actualización clásica</p></td>
<td align="left"><p>Actualización clásica</p></td>
<td align="left"><p>La instalación está bloqueada</p></td>
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
<td align="left"><p>La instalación está bloqueada</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>Actualización inteligente</p></td>
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
<td align="left"><p>Actualización inteligente</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,0 SP2</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>No disponible</p></td>
<td align="left"><p>Actualización inteligente</p></td>
</tr>
</tbody>
</table>

 

## Configuraciones admitidas


AGPM 4.0 SP3 admite las configuraciones de la tabla siguiente. Aunque AGPM admite configuraciones mixtas, le recomendamos encarecidamente que ejecute el cliente AGPM y el servidor AGPM en la misma línea del sistema operativo, por ejemplo, Windows10 con Windows Server 2016, Windows 8,1 con Windows Server 2012 R2, etc.

**Configuración de directiva y sistemas operativos compatibles con el SP3 de AGPM 4.0**

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
<td align="left"><p>Windows Server 2019 o Windows 10</p></td>
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Compatible</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2016 o Windows 10</p></td>
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Compatible</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Se admite</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 o Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008 o vista con Service Pack 1 (SP1)</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>No se admite</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</p></td>
</tr>
</tbody>
</table>

 

## Requisitos previos para instalar AGPM 4.0 SP3

En la siguiente tabla se describe el comportamiento de los instaladores de cliente y de servidor de AGPM 4.0 SP3 cuando falta la versión 4.5.1 de .NET Framework, PowerShell 3,0 o la GPMC en las herramientas de administración remota del servidor.

| Cliente AGPM            |                                                                                                 |                                                                            | Servidor de AGPM                                                                     |                                                                                                 |                                                                                 |
|------------------------|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Sistema operativo       | .NET Framework                                                                                  | PowerShell                                                                 | Herramientas de administración remota del servidor                                              | .NET Framework                                                                                  | Herramientas de administración remota del servidor                                              |
| Windows 10             | Si .NET Framework 4.5.1 no está habilitado ni instalado, el instalador bloquea la instalación. | Si PowerShell 3,0 no está instalado, el instalador bloquea la instalación. | Si la GPMC no está habilitada ni instalada, el instalador bloquea la instalación. | Si .NET Framework 4.5.1 no está habilitado ni instalado, el instalador bloquea la instalación. | Si la GPMC no está habilitada ni instalada, el instalador bloquea la instalación. |
| Windows 8.1            | Si .NET Framework 4.5.1 no está habilitado ni instalado, el instalador bloquea la instalación. | Si PowerShell 3,0 no está instalado, el instalador bloquea la instalación. | Si la GPMC no está habilitada ni instalada, el instalador bloquea la instalación. | Si .NET Framework 4.5.1 no está habilitado ni instalado, el instalador bloquea la instalación. | Si la GPMC no está habilitada ni instalada, el instalador bloquea la instalación. |
| Windows Server2012R2 | Si .NET Framework 4.5.1 no está habilitado ni instalado, el instalador bloquea la instalación. | Si PowerShell 3,0 no está instalado, el instalador bloquea la instalación. | Si la GPMC no está habilitada, el instalador la habilita durante la instalación.   | Si .NET Framework 4.5.1 no está habilitado ni instalado, el instalador bloquea la instalación. | Si la GPMC no está habilitada, el instalador la habilita durante la instalación.   |

 

## Cómo obtener tecnologías de MDOP


AGPM 4,0 SP3 es parte del paquete de optimización de escritorio de Microsoft (MDOP) desde MDOP 2015. MDOP es parte de Microsoft Software Assurance. Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Temas relacionados


[Administración avanzada de directivas de grupo](index.md)

[Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0 SP3](release-notes-for-microsoft-advanced-group-policy-management-40-sp3.md)

[Elección de qué versión de AGPM ha de instalarse](choosing-which-version-of-agpm-to-install.md)

 

 





