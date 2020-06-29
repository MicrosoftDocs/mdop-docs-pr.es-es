---
title: Planificación de la implementación de App-V 5.1 con un sistema de distribución electrónica de software
description: Planificación de la implementación de App-V 5.1 con un sistema de distribución electrónica de software
author: dansimp
ms.assetid: c26602c2-5e8d-44e6-90df-adacc593607e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fde3f0ea4f1dec72b97143b4b27dd0b32a503b15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813399"
---
# Planificación de la implementación de App-V 5.1 con un sistema de distribución electrónica de software


Si está usando un sistema de distribución de software electrónico para implementar paquetes de App-V, revise las siguientes consideraciones de planeación. Para obtener información sobre el uso de System Center Configuration Manager para implementar App-V, consulte [Introducción a la administración de aplicaciones en Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816).

Revise las siguientes opciones de requisitos de componentes y arquitectura que se aplican al usar un ESD para implementar paquetes de App-V:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Opción o requisito de implementación</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>El servidor de administración de App-V, la base de datos de administración y el servidor de publicación no son necesarios.</p></td>
<td align="left"><p>Estas funciones son controladas por la solución ESD implementada.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Puede implementar el servidor de informes de App-V y la base de datos de informes en paralelo con el ESD.</p></td>
<td align="left"><p>La implementación en paralelo le permite recopilar datos y generar informes.</p>
<p>Si habilita el cliente de App-V para enviar información de informes y no usa el servidor de informes de App-V, los datos de informes se almacenan en archivos. XML asociados.</p></td>
</tr>
</tbody>
</table>

 






## Temas relacionados


[Planificación de la implementación de App-V](planning-to-deploy-app-v51.md)

 

 





