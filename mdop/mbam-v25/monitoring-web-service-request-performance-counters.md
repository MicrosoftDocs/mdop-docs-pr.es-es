---
title: Supervisión de contadores de rendimiento de solicitudes de servicio web
description: Supervisión de contadores de rendimiento de solicitudes de servicio web
author: dansimp
ms.assetid: bdb812a1-465a-4098-b4c0-cb99890d1b0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2db96e3375562b48d289ea5a21dc7e89b800d1ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823880"
---
# Supervisión de contadores de rendimiento de solicitudes de servicio web


Administración y supervisión de Microsoft BitLocker (MBAM) proporciona contadores de rendimiento que registran el rendimiento de las solicitudes que se envían a los siguientes servicios web:

-   **StatusReportingService. SVC** : servicio que recibe solicitudes de estado de cumplimiento.

-   **CoreService. SVC** : servicio que recibe solicitudes de intentos de recuperación de claves

## Contadores de rendimiento que proporciona MBAM


MBAM proporciona los siguientes contadores de rendimiento para cada uno de los métodos públicos que implementan sus servicios Web de StatusReportingService y CoreService:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de contador de rendimiento</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Número total de solicitudes</p></td>
<td align="left"><p>Proporciona un recuento incremental que se inicia desde cero cuando se inicia o se reinicia el servidor.</p>
<p>Proporciona una vista general de la actividad del sistema. Puede ser controlado por herramientas automatizadas para garantizar el estado del servidor y para validar que el contador se incremente continuamente a lo largo de un período de tiempo específico.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Solicitudes por segundo</p></td>
<td align="left"><p>Indica el rendimiento actual del servidor de MBAM, ya que admite la base de cliente de MBAM.</p>
<p>Permite a los administradores de sitios:</p>
<ul>
<li><p>Calcular el número promedio de solicitudes por segundo, en función del número de clientes MBAM y su frecuencia de informes.</p></li>
<li><p>Valide que el número de solicitudes por segundo se correlacione ampliamente con el número promedio calculado de solicitudes por segundo. Una varianza significativa puede indicar que el cliente de MBAM no está instalado en un porcentaje de la base de clientes o que un objeto de directiva de grupo MBAM no se ha implementado correctamente.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Duración de la solicitud</p></td>
<td align="left"><p>Registra la duración de las solicitudes en milisegundos.</p>
<p>Aunque este contador se actualiza con la duración de cada solicitud, muestras del monitor de rendimiento de Windows solo periódicamente (normalmente cada segundo), por lo que es posible que vea alguna variabilidad en el valor. Por este motivo, considere la posibilidad de usar el valor promedio que muestra el monitor de rendimiento.</p></td>
</tr>
</tbody>
</table>

 

## Resultados y recomendaciones de los contadores de rendimiento


A medida que agregue nuevos clientes de MBAM a un servidor de MBAM con capacidad reservada, esperará un aumento en el número de solicitudes por segundo. Este aumento será proporcional al número de equipos cliente nuevos. La duración media de la solicitud permanecerá relativamente estática. A medida que el servidor se acerque a su capacidad máxima, las solicitudes por segundo comienzan a redistribuirse y el promedio de duración de la solicitud comienza a ser más largo.

Si le preocupa si los servidores MBAM pueden admitir su base de clientes, considere la posibilidad de implementar MBAM en fases en diferentes colecciones de equipos cliente. Al implementar MBAM en cada colección de equipos cliente, le recomendamos que tome instantáneas de los contadores de rendimiento para ver el impacto relativo de la implementación en cada nueva colección de clientes. Si el número de solicitudes por segundo comienza a redistribuirse y se incrementa el promedio de duración de la solicitud, considere la posibilidad de mejorar la infraestructura del servidor de MBAM mediante uno de los siguientes procedimientos:

-   Mover la base de datos MBAM a un clúster de Microsoft SQL Server o SQL Server dedicado

-   Equilibrio de carga MBAM en varios servidores Web de servicios de información de Internet (IIS)

-   Implementar MBAM en hardware de servidor más eficaz

## Ver contadores de rendimiento


La herramienta recomendada para ver los contadores de rendimiento de MBAM es el monitor de rendimiento de Windows, que viene con Windows. Si está usando Windows PowerShell, no necesita habilitar los contadores antes de verlos, ya que el cmdlet **enable-WebApplication de** Windows PowerShell los registra automáticamente.

Para obtener instrucciones detalladas sobre cómo ver los contadores de rendimiento, consulte [Cómo ver los contadores de rendimiento de MBAM](https://go.microsoft.com/fwlink/?LinkId=393457).



## Temas relacionados


[Mantenimiento de MBAM 2.5](maintaining-mbam-25.md)

 

 


## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).


