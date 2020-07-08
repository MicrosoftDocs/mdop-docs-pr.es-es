---
title: Arquitectura de alto nivel de App-V 5.1
description: Arquitectura de alto nivel de App-V 5.1
author: dansimp
ms.assetid: 90406361-55b8-40b7-85c0-449436789d4c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8044c6ae9af4673ec12b47cf3b8fa73a134d9cca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814519"
---
# Arquitectura de alto nivel de App-V 5.1


Use la siguiente información para que le resulte más fácil simplificar la implementación de Microsoft Application Virtualization (App-V) 5,1.

## Descripción general de la arquitectura


Una implementación típica de App-V 5,1 consta de los siguientes elementos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de administración de App-V 5,1</p></td>
<td align="left"><p>El servidor de administración de App-V 5,1 proporciona una funcionalidad de administración general para la infraestructura de App-V 5,1. Además, puede instalar más de una instancia del servidor de administración en su entorno, lo que ofrece las siguientes ventajas:</p>
<ul>
<li><p>Tolerancia a errores y alta disponibilidad: la instalación y la configuración del servidor de administración de App-V 5,1 en dos equipos diferentes puede ayudar en situaciones en las que uno de los servidores no está disponible o desconectado.</p>
<p>También puede ayudar a aumentar la disponibilidad de App-V 5,1 instalando el servidor de administración en varios equipos. En este escenario, también se debe tener en cuenta un equilibrador de carga de red para equilibrar las solicitudes del servidor.</p></li>
<li><p>Escalabilidad: puede agregar servidores de administración adicionales según sea necesario para admitir una carga elevada, por ejemplo, puede instalar varios servidores detrás de un equilibrador de carga.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de publicación de App-V 5,1</p></td>
<td align="left"><p>El servidor de publicación de App-V 5,1 proporciona una funcionalidad para el hospedaje de aplicaciones virtuales y la transmisión por secuencias. El servidor de publicación no requiere una conexión de base de datos y admite los siguientes protocolos:</p>
<ul>
<li><p>HTTP y HTTPS</p></li>
</ul>
<p>También puede mejorar la disponibilidad de App-V 5,1 instalando el servidor de publicación en varios equipos. También se debe tener en cuenta un equilibrador de carga de red para que las solicitudes del servidor estén equilibradas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Servidor de informes de App-V 5,1</p></td>
<td align="left"><p>El servidor de informes de App-V 5,1 permite que los usuarios autorizados ejecuten y vean informes existentes de App-V 5,1 e informes ad hoc que pueden ayudarle a administrar la infraestructura de App-V 5,1. El servidor de informes requiere una conexión a la base de datos de informes de App-V 5,1. También puede mejorar la disponibilidad de App-V 5,1 instalando el servidor de informes en varios equipos. También se debe tener en cuenta un equilibrador de carga de red para que las solicitudes del servidor estén equilibradas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente de App-V 5,1</p></td>
<td align="left"><p>El cliente de App-V 5,1 permite que los paquetes creados con App-V 5,1 se ejecuten en equipos de destino.</p></td>
</tr>
</tbody>
</table>

 

**Nota:**  Si está usando App-V 5,1 con distribución electrónica de software (ESD), no es necesario que use el servidor de administración de App-V 5,1; sin embargo, puede seguir usando la funcionalidad de creación de informes y transmisión de App-V 5,1.

 






## Temas relacionados


[Introducción a App-V 5.1](getting-started-with-app-v-51.md)

 

 





