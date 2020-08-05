---
title: Elección de qué versión de AGPM ha de instalarse
description: Elección de qué versión de AGPM ha de instalarse
author: dansimp
ms.assetid: 31357d2a-bc23-4e15-93f4-0beda8ab7a7b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/05/2017
ms.openlocfilehash: f8a69fb323d9f47c5b906ac3abc6ec59376ee6f7
ms.sourcegitcommit: 0a7dee11289780336d9c24ebbf27c5c1ffee441c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/04/2020
ms.locfileid: "10905607"
---
# Elección de qué versión de AGPM ha de instalarse


Cada versión de MicrosoftAdvanced Group Policy Management (AGPM) admite versiones específicas del sistema operativo Windows. Le recomendamos encarecidamente que ejecute el cliente AGPM y el servidor AGPM en la misma línea de sistemas operativos. Por ejemplo, Windows 10 con Windows Server 2016, Windows 8.1 con Windows Server2012 R2, etc.

Le recomendamos que instale el servidor AGPM en la versión más reciente del sistema operativo del dominio. AGPM usa la consola de administración de directivas de grupo (GPMC) para realizar copias de seguridad y restaurar objetos de directiva de grupo (GPO). Como las versiones más recientes de la GPMC proporcionan opciones de directiva adicionales que no están disponibles en versiones anteriores, puede administrar más opciones de configuración con la versión más reciente del sistema operativo.

Todas las versiones de AGPM solo pueden administrar la configuración de la Directiva que se introdujo en la misma versión o una versión anterior del sistema operativo en el que se está ejecutando AGPM. Por ejemplo, si instala AGPM 4.0 SP2 en Windows Server 2012, puede administrar la configuración de directiva introducida en Windows Server 2012 o versiones anteriores, pero no puede administrar la configuración de la Directiva introducida más adelante, en Windows 8.1 o Windows Server2012 R2.

Si la versión de la GPMC en el servidor de AGPM es anterior a la versión de los equipos que los administradores usan para administrar la Directiva de grupo, el servidor de AGPM no podrá almacenar ninguna configuración de directiva que no esté disponible en la versión anterior de la GPMC. Para obtener una hoja de cálculo con la configuración de directiva de grupo incluida en Windows, consulta la [referencia de configuración de directiva de grupo para Windows y Windows Server](https://go.microsoft.com/fwlink/p/?LinkId=613627).

## SP3 DE AGPM 4.0


Si usa equipos que ejecutan Windows 10 para administrar GPO, debe usar AGPM 4,0 SP3. No puede instalar versiones anteriores de AGPM en equipos que ejecutan el sistema operativo Windows 10.

En la tabla 1 se enumeran los sistemas operativos en los que puede instalar AGPM 4.0 SP3 y la configuración de directiva que puede administrar mediante AGPM 4.0 SP3.

**Tabla 1: configuración de directiva y sistemas operativos compatibles con AGPM 4,0 SP3**

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
<td align="left"><p>Windows Server 2019 o Windows 10</p></td>
<td align="left"><p>Se admite</p></td>
</tr>
 <tr class="even">
<td align="left"><p>Windows Server 2019 o Windows 10</p></td>
<td align="left"><p>Windows Server 2019 o Windows 10</p></td>
<td align="left"><p>Se admite</p></td>
</tr>
<tr class="edd">
<td align="left"><p>Windows Server2012 R2</p></td>
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Compatible con las advertencias descritas en <a href="https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv" data-raw-source="[KB 4015786](https://support.microsoft.com/help/4015786/known-issues-managing-a-windows-10-group-policy-client-in-windows-serv)"> KB 4015786</a>
</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Windows Server2012 R2 o Windows 8.1</p></td>
<td align="left"><p>Se admite</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 o Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 o Windows 8,1</p></td>
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
<td align="left"><p>Windows Server 2012, Windows Server2008R2, Windows 8 o Windows7</p></td>
<td align="left"><p>No se admite</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 SP2


Si usa equipos que ejecutan Windows Server2012 R2 o Windows 8.1 para administrar GPO, debe usar AGPM 4.0 SP2. No puede instalar versiones anteriores de AGPM en equipos que ejecutan esos sistemas operativos.

En la tabla 1 se enumeran los sistemas operativos en los que puede instalar AGPM 4.0 SP2 y la configuración de directiva que puede administrar mediante AGPM 4.0 SP2.

**Tabla 2: configuración de directiva y sistemas operativos compatibles con el SP2 de AGPM 4.0**

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
<td align="left"><p>Windows Server2012 R2, Windows Server 2012 o Windows 8.1</p></td>
<td align="left"><p>Windows Server 2012 o Windows 8,1</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8.1</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008 o vista con Service Pack 1 (SP1)</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>No se admite</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2012 R2, Windows Server 2012, Windows Server2008R2, Windows 8.1 o Windows7</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0 SP1


En la tabla 2 se enumeran los sistemas operativos en los que puede instalar AGPM 4,0 SP1 y la configuración de directiva que puede administrar mediante AGPM 4.0 SP1.

**Tabla 3: configuración de directiva y sistemas operativos compatibles con AGPM 4.0 SP1**

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
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Se admite</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows 8,1</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012, Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o en Windows7</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server 2012, Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Se admite</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o en Windows7</p></td>
</tr>
</tbody>
</table>

 

## AGPM 4.0


En la tabla 3 se enumeran los sistemas operativos en los que puede instalar AGPM 4,0 y la configuración de directiva que puede administrar mediante AGPM 4.0.

**Tabla 4: configuración de directiva y sistemas operativos compatibles con AGPM 4.0**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistemas operativos compatibles para el servidor de AGPM</th>
<th align="left">Sistemas operativos compatibles para el cliente de AGPM</th>
<th align="left">Compatibilidad con AGPM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Se admite</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Compatible, pero no puede editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o en Windows7</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008R2 o Windows7</p></td>
<td align="left"><p>No se admite</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Windows Server2008 o Windows Vista con SP1</p></td>
<td align="left"><p>Compatible, pero no puede notificar o editar la configuración de directivas o los elementos de preferencias que solo existen en Windows Server2008R2 o Windows7</p></td>
</tr>
</tbody>
</table>

 

## Versiones de AGPM anteriores a AGPM 4.0


En la tabla 4 se enumeran los sistemas operativos en los que puede instalar las versiones de AGPM anteriores a AGPM 4.0. Si un sistema operativo no aparece en la lista, no puede instalar AGPM en ese sistema operativo.

**Tabla 5: sistemas operativos compatibles para las versiones de AGPM anteriores a AGPM 4.0**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Versión de AGPM que se puede instalar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Server2008</p></td>
<td align="left"><p>3,0</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Vista con SP1</p></td>
<td align="left"><p>3,0</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Vista sin ningún Service Pack instalado (32 bits)</p></td>
<td align="left"><p>2,5</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2003 (32 bits)</p></td>
<td align="left"><p>2,5</p></td>
</tr>
</tbody>
</table>

 

## Cómo obtener tecnologías de MDOP


AGPM 4,0 SP2 forma parte del paquete de optimización de escritorio de Microsoft (MDOP). MDOP es parte de Microsoft Software Assurance. Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Temas relacionados


[Administración avanzada de directivas de grupo](index.md)

 

 





