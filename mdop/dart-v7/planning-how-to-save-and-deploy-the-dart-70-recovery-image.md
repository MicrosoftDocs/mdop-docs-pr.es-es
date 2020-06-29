---
title: Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 7.0
description: Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 7.0
author: dansimp
ms.assetid: d96e9363-6186-4fc3-9b83-ba15ed9694a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c292633949865d4b3f5053700f4219db3f1cf465
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822800"
---
# Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 7.0


Use la información de esta sección cuando planea guardar e implementar la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 7.

## Planear cómo guardar e implementar la imagen de recuperación de DaRT


Puede guardar e implementar la imagen de recuperación de DaRT mediante los siguientes métodos. Cuando determine el método que va a usar, tenga en cuenta las ventajas y desventajas de cada uno. Además, tenga en cuenta cómo desea usar DaRT en su empresa.

**Nota:**  Es posible que desee usar más de un método de su organización. Por ejemplo, puede arrancar en DaRT desde una partición remota para la mayoría de las situaciones y tener una unidad flash USB disponible en caso de que el equipo del usuario final no pueda conectarse a la red.

 

En la tabla siguiente se muestran algunas de las ventajas y desventajas de cada método de uso de DaRT en su organización.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método para arrancar DaRT</th>
<th align="left">Ventajas</th>
<th align="left">Desventajas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Desde un CD o DVD</p></td>
<td align="left"><p>Es compatible con escenarios en los que el registro de inicio maestro (MBR) está dañado y no se puede obtener acceso al disco duro. También admite casos en los que no hay conexión de red.</p>
<p>Esto está más familiarizado con los usuarios de versiones anteriores de DaRT, y se puede grabar un CD o DVD directamente desde el <strong> Asistente de imagen de recuperación de DART </strong> .</p></td>
<td align="left"><p>Requiere que la persona con acceso al CD o DVD se encuentre físicamente en el equipo del usuario final para iniciar en DaRT.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Desde una unidad flash USB (UFD)</p></td>
<td align="left"><p>Proporciona las mismas ventajas que el inicio desde un CD o DVD y también proporciona compatibilidad con equipos que no tienen unidad de CD o DVD.</p></td>
<td align="left"><p>Requiere formatear la UFD antes de poder usarla para arrancar DaRT. También requiere que alguien con acceso a la UFD esté físicamente en el equipo del usuario final para iniciar en DaRT.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Desde una partición remota (de red)</p></td>
<td align="left"><p>Le permite arrancar DaRT sin necesidad de un CD, DVD o UFD. También permite actualizaciones de DaRT fácilmente, ya que solo se puede actualizar una ubicación de archivo.</p></td>
<td align="left"><p>No funciona si el equipo del usuario final no está conectado a la red.</p>
<p>Ampliamente disponible para los usuarios finales y es posible que necesite otras consideraciones de seguridad al crear la imagen de recuperación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Desde una partición de recuperación</p></td>
<td align="left"><p>Le permite arrancar DaRT sin necesidad de un CD, DVD o UFD que incluya instancias en las que no haya conectividad de red.</p>
<p>Además, puede implementarse y administrarse como parte del proceso estándar de la imagen de Windows mediante herramientas de distribución automatizadas, como Microsoft Endpoint Configuration Manager.</p></td>
<td align="left"><p>Al actualizar DaRT, debe actualizar todos los equipos de su empresa en lugar de solo una partición (en la red) o un dispositivo (CD, DVD o UFD).</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Planificación de la implementación de DaRT 7.0](planning-to-deploy-dart-70.md)

 

 





