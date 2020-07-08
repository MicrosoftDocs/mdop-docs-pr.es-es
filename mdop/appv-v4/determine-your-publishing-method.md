---
title: Determinar el método de publicación
description: Determinar el método de publicación
author: dansimp
ms.assetid: 1f2d0d39-5d65-457a-b826-4f45b00c8c85
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a6b19b12c28ab67e3250909cb32ddb8419f399a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821680"
---
# Determinar el método de publicación


Después de secuenciar una aplicación mediante Application Virtualization Sequencer, tendrá que *publicarla* para los usuarios. La publicación de la aplicación consiste en ofrecer los iconos, la información de definición del paquete y la ubicación del origen de contenido en cada equipo en el que se haya instalado el cliente de virtualización de aplicaciones. En la siguiente tabla se describen los métodos de publicación que se admiten al implementar la virtualización de aplicaciones mediante un sistema de distribución de software electrónico (ESD).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Ventajas</th>
<th align="left">Desventajas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Genere un archivo de Windows Installer durante la secuenciación, como una solución independiente.</p></td>
<td align="left"><ul>
<li><p>Es muy fácil de usar.</p></li>
<li><p>Paquete cargado en la caché de forma local en cada equipo.</p></li>
<li><p>Iconos que se muestran al usuario.</p></li>
<li><p>Similar a la implementación de software tradicional.</p></li>
<li><p>No es necesario que los servidores de streaming sean.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>No hay flexibilidad en la ubicación del contenido del paquete en los equipos, la misma ubicación en todos los equipos.</p></li>
<li><p>Debe usar solo agregar o quitar programas o msiexec para quitar aplicaciones.</p></li>
<li><p>Eliminación y sustitución con la nueva versión necesaria para la actualización de paquetes.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Genera un archivo de Windows Installer durante la secuenciación, que se usa con las propiedades de línea de comandos MODE, LOAD y OVERRIDEURL y el manifiesto del paquete.</p></td>
<td align="left"><ul>
<li><p>Fácil de usar, pero con flexibilidad añadida.</p></li>
<li><p>Iconos que se muestran al usuario.</p></li>
<li><p>SFT el archivo que contiene las aplicaciones puede colocarse en una ubicación de origen de transmisión, con clientes configurados para usar esa ubicación.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Flexibilidad limitada: solo se puede controlar la ubicación del contenido del paquete en tiempo de ejecución.</p></li>
<li><p>Debe usar solo agregar o quitar programas o msiexec para quitar la aplicación.</p></li>
<li><p>Eliminación y sustitución con la nueva versión necesaria para actualizar paquetes, a menos que use el servidor de streaming.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Ejecute los comandos de SFTMIME.</p></td>
<td align="left"><ul>
<li><p>Flexibilidad completa: control total de todas las funciones de administración de paquetes.</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Los comandos deben incluirse en scripts para usarlos con el sistema ESD.</p></li>
<li><p>Los comandos deben ejecutarse en cada equipo en el orden correcto.</p></li>
<li><p>Comprensión detallada del lenguaje de comandos y una planificación precisa.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Para obtener más información sobre cómo usar estos métodos de publicación, vea [Cómo publicar una aplicación virtual en el cliente](how-to-publish-a-virtual-application-on-the-client.md).

## Temas relacionados


[Determinar el método de streaming](determine-your-streaming-method.md)

[Escenario basado en distribución electrónica de software](electronic-software-distribution-based-scenario.md)

[Introducción a escenario basado en la distribución electrónica de software](electronic-software-distribution-based-scenario-overview.md)

[Cómo publicar una aplicación virtual en el cliente](how-to-publish-a-virtual-application-on-the-client.md)

[Referencia de comandos de SFTMIME](sftmime--command-reference.md)

 

 





