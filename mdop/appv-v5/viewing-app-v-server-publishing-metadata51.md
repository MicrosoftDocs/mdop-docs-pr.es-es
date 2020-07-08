---
title: Visualización de metadatos de publicación del servidor de App-V
description: Visualización de metadatos de publicación del servidor de App-V
author: dansimp
ms.assetid: d5fa9eb5-647c-478d-8a4d-0ecda018bce6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 97c59301678280febe23b8061c08033a88ae49c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813231"
---
# Visualización de metadatos de publicación del servidor de App-V


Use este procedimiento para ver los metadatos de publicación, que pueden ayudarle a resolver problemas relacionados con la publicación. Para poder usar este procedimiento, debe usar el servidor de administración de App-V.

Este artículo contiene la siguiente información:

-   [Requisitos de App-V 5,1 para ver metadatos de publicación](#bkmk-51-reqs-pub-meta)

-   [Sintaxis para ver metadatos de publicación](#bkmk-syntax-view-pub-meta)

-   [Valores de consulta para el sistema operativo y la versión del cliente](#bkmk-values-query-pub-meta)

-   [Definición de metadatos de publicación](#bkmk-whatis-pub-metadata)

## <a href="" id="bkmk-51-reqs-pub-meta"></a>Requisitos de App-V 5,1 para ver metadatos de publicación


En App-V 5,1, debe proporcionar los siguientes valores en la dirección al consultar el servidor de publicación de App-V para obtener metadatos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Valor</th>
<th align="left">Detalles adicionales</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>ClientVersion</strong></p></td>
<td align="left"><p>Si omite el <strong> parámetro ClientVersion </strong> de la consulta, los metadatos excluyen las características nuevas de App-V 5,0 SP3.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Clientes</strong></p></td>
<td align="left"><p>Solo tiene que proporcionar este valor si selecciona sistemas operativos cliente específicos al realizar la secuencia del paquete. Si selecciona el valor predeterminado (todos los sistemas operativos), no especifique este valor en la consulta.</p>
<p>Si omite el <strong> </strong> parámetro de los clientes de la consulta, solo los paquetes que se secuenciaron para admitir cualquier sistema operativo aparecerán en los metadatos.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-syntax-view-pub-meta"></a>Sintaxis de consulta para ver metadatos de publicación


En la tabla siguiente se proporciona la sintaxis y los ejemplos de consulta.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión de App-V</th>
<th align="left">Sintaxis de la consulta</th>
<th align="left">Descripciones de parámetros</th>
<th align="left">Ejemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 5,0 SP3 y App-V 5,1</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/?ClientVersion=&lt;AppvClientVersion&gt;&amp;ClientOS=&lt;OSStringValue&gt;</code></p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parámetro</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>&lt;PubServer&gt;</p></td>
<td align="left"><p>Nombre del servidor de publicación de App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;Puerto de publicación #&gt;</p></td>
<td align="left"><p>Puerto en el servidor de publicación de App-V, que definió al configurar el servidor de publicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ClientVersion = &lt; AppvClientVersion&gt;</p></td>
<td align="left"><p>Versión del cliente de App-V. Consulte la tabla siguiente para obtener el valor correcto para usar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Clientes = &lt; OSStringValue&gt;</p></td>
<td align="left"><p>Sistema operativo del equipo en el que se ejecuta el cliente de App-V. Consulte la tabla siguiente para obtener el valor correcto para usar.</p></td>
</tr>
</tbody>
</table>
<p> </p>
<p>Para obtener el nombre del servidor de publicación y el número de puerto (http:// &lt; PubServer: número de &gt; Puerto de &lt; publicación # &gt; ) del cliente de App-V, consulte la configuración de la dirección URL del <strong> cmdlet de PowerShell Get-AppvPublishingServer </strong> .</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64" data-raw-source="http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;amp;clientos=WindowsClient_6.2_x64">http://pubsvr01:2718/?clientversion=5.0.10066.0&amp;clientos=WindowsClient_6.2_x64</a></code></p>
<p>En el ejemplo:</p>
<ul>
<li><p>Un Windows Server 2012 R2 denominado "pubsvr01" hospeda el servicio de publicación.</p></li>
<li><p>El cliente de Windows es Windows 8,1 64 bits.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 5,0 mediante App-V 5,0 SP2</p></td>
<td align="left"><p><code>http://&lt;PubServer&gt;:&lt;Publishing Port#&gt;/ </code></p>
<div class="alert">
<strong>Nota</strong><br/><p><strong>ClientVersion </strong> y los <strong> clientes </strong> solo se admiten en app-v 5,0 SP3 y app-v 5,1.</p>
</div>
<div>

</div></td>
<td align="left"><p>Consulte la información de App-V 5,0 SP3 y App-V 5,1.</p></td>
<td align="left"><p><code><a href="http://pubsvr01:2718" data-raw-source="http://pubsvr01:2718">http://pubsvr01:2718</a></code></p>
<p>En el ejemplo, un Windows Server 2012 R2 denominado "pubsvr01" hospeda los servicios de publicación y administración.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-values-query-pub-meta"></a>Valores de consulta para el sistema operativo y la versión del cliente


En la consulta de metadatos de publicación, escriba los valores de cadena que correspondan al sistema operativo del cliente y la versión que está usando.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Arquitectura</th>
<th align="left">Valor de cadena de cadena de operación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsClient_10.0_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsClient_10.0_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsClient_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsClient_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsClient_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsClient_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012R2</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsServer_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012R2</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsServer_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsServer_6.2_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsServer_6.2_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsClient_6.1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsClient_6.1_x86</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>WindowsServer_6.1_x64</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>WindowsServer_6.1_x86</p></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-whatis-pub-metadata"></a>Definición de metadatos de publicación


Cuando los paquetes se publican en un equipo que ejecuta el cliente de App-V, los metadatos se envían a ese equipo que indica qué paquetes y grupos de conexión se están publicando. El cliente de App-V realiza dos solicitudes independientes para lo siguiente:

-   Paquetes y grupos de conexión que tienen derecho al equipo cliente.

-   Paquetes y grupos de conexión que tienen derecho al usuario actual.

El servidor de publicación se comunica con el servidor de administración para determinar qué paquetes y grupos de conexión están disponibles para el solicitante. El servidor de publicación debe registrarse en el servidor de administración para que se generen los metadatos.

Puede ver los metadatos de cada solicitud en un explorador de Internet mediante una consulta que se encuentra en el contexto del usuario o equipo específico.






## Temas relacionados


[Referencia técnica de App-V 5.1](technical-reference-for-app-v-51.md)









