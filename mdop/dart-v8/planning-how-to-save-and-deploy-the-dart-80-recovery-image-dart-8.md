---
title: Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 8.0
description: Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 8.0
author: dansimp
ms.assetid: 939fbe17-0e30-4c85-8782-5b84d69442a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e5cca90c644eb3edf233564c474d2601d4227fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821241"
---
# Planificación de cómo guardar e implementar la imagen para recuperación de DaRT 8.0


Puede guardar e implementar la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 mediante los métodos siguientes. Cuando determine el método que va a usar, tenga en cuenta las ventajas y desventajas de cada uno. También debe tener en cuenta la infraestructura y el personal de soporte técnico. Si tiene una infraestructura pequeña, es posible que desee implementar DaRT 8,0 mediante medios extraíbles, ya que la imagen de recuperación siempre estará disponible si la instala en el disco duro local.

Si su organización usa servicios de dominio de Active Directory (AD DS), es posible que desee implementar imágenes de recuperación como servicio de red con Windows DS. Las imágenes de recuperación siempre están disponibles para cualquier equipo conectado. Puede implementar varias imágenes desde Windows DS y mantenerlas en un solo lugar.

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
<td align="left"><p><strong>Medios extraíbles</strong></p>
<p>La imagen de recuperación se escribe en un CD, DVD o unidad USB para que el personal de soporte técnico pueda tomar las herramientas de recuperación con ellas en el equipo inestable.</p></td>
<td align="left"><p>Admite escenarios en los que el registro de inicio maestro (MBR) está dañado y no puede tener acceso al disco duro y admite casos en los que no hay conexión de red.</p>
<p>Le permite crear varias imágenes de recuperación con diferentes herramientas para proporcionar diferentes niveles de soporte.</p>
<p>Proporciona una herramienta integrada para grabar imágenes de recuperación en medios extraíbles.</p></td>
<td align="left"><p>Requiere que el personal de soporte técnico esté físicamente en el equipo del usuario final para iniciar en DaRT.</p>
<p>Requiere tiempo y mantenimiento para crear varios medios con diferentes configuraciones para los equipos de 32 y 64 bits.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Desde una partición remota (de red)</strong></p>
<p>La imagen de recuperación está hospedada en un servidor de arranque de red como servicios de implementación de Windows (Windows DS), que permite a los usuarios o al personal de soporte técnico transmitirlos a equipos a petición.</p></td>
<td align="left"><p>Disponible para todos los equipos que tengan acceso al servidor de arranque de red.</p>
<p>Las imágenes de recuperación se hospedan en un servidor central, lo que permite actualizaciones centralizadas.</p>
<p>El personal de soporte técnico centralizado puede proporcionar reparaciones mediante conectividad remota.</p>
<p>No hay ningún requisito de almacenamiento local en los clientes.</p>
<p>Capacidad de crear varias imágenes de recuperación con diferentes herramientas para niveles de asistencia específicos.</p></td>
<td align="left"><p>La necesidad de proteger la infraestructura de Windows DS para garantizar que los usuarios habituales puedan iniciar solo la imagen de recuperación de DaRT y no con el proceso de creación de imágenes de sistema operativo completo.</p>
<p></p>
<p></p>
<p>Requiere que el equipo del usuario final esté conectado a la red en tiempo de ejecución.</p>
<p>Requiere que la imagen de recuperación se conecte a través de la red.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Desde una partición de recuperación de la unidad de disco duro local</strong></p>
<p>La imagen de recuperación se instala en una unidad de disco duro local, ya sea de forma manual o mediante sistemas electrónicos de distribución de software, como System Center Configuration Manager.</p></td>
<td align="left"><p>La imagen de recuperación siempre está disponible porque está preconfigurada en el equipo.</p>
<p>El personal de soporte técnico centralizado puede proporcionar asistencia a través de la conexión remota.</p>
<p>La imagen de recuperación se administra y se implementa de forma centralizada.</p>
<p>Se eliminan las solicitudes de clave de recuperación adicionales en equipos protegidos por el cifrado de unidad BitLocker de Windows.</p></td>
<td align="left"><p>Se necesita almacenamiento local.</p>
<p>Se recomienda una partición dedicada y sin cifrar para la ubicación de la imagen de recuperación con el fin de reducir el riesgo de una partición de inicio con error.</p>
<p>Al actualizar DaRT, debe actualizar todos los equipos de su empresa en lugar de solo una partición (en la red) o un dispositivo extraíble.</p>
<p>Se requiere una mayor consideración si implementa la imagen de recuperación después de que se haya habilitado BitLocker.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Planificación de la implementación de DaRT 8.0](planning-to-deploy-dart-80-dart-8.md)

 

 





