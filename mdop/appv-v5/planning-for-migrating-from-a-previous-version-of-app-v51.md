---
title: Planificación para migrar desde una versión anterior de App-V
description: Planificación para migrar desde una versión anterior de App-V
author: dansimp
ms.assetid: 4a058047-9674-41bc-8050-c58c97a80a9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: d7f2496b355aee6a598fee44c84e7e8c0f755c4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813470"
---
# Planificación para migrar desde una versión anterior de App-V


Use la siguiente información para planear cómo migrar a Microsoft Application Virtualization (App-V) 5,1 desde versiones anteriores de App-V.

## Requisitos de migración


Antes de iniciar cualquier actualización, revise los siguientes requisitos:

-   Si está actualizando una versión anterior a App-V 4,6 SP2, actualice a la versión App-V 4,6 SP3 en primer lugar antes de actualizar a App-V 5,1 o posterior. En este escenario, actualice los clientes de App-V en primer lugar y, a continuación, actualice los componentes del servidor.
**Nota:** App-V 4,6 ha salido del soporte técnico estándar.

-   App-V 5,1 solo admite paquetes creados con App-V 5,0 o App-V 5,1, o paquetes que se han convertido al formato **. appv** .

-   Si está actualizando el servidor de App-V de App-V 5,0 SP1, consulte [acerca de App-v 5,1](about-app-v-51.md#bkmk-migrate-to-51) para obtener instrucciones.

## Ejecutar el cliente de App-V 5,1 de forma simultánea con App-V 4,6


Puede ejecutar el cliente de App-V 5,1 de forma simultánea en el mismo equipo que el cliente de App-V 4.6 SP3.

Al ejecutar los clientes coexistentes de App-V, puede hacer lo siguiente:

-   Convierta un paquete de App-V 4,6 SP3 al formato de App-V 5,1 y publique ambos paquetes cuando tenga ambos clientes ejecutándose.

-   Defina la Directiva de migración para el paquete convertido, lo que permite que el paquete de App-V 5,1 convertido asuma las asociaciones de tipo de archivo y los accesos directos del paquete de App-V 4,6.

### Escenarios de coexistencia compatibles

En la siguiente tabla se muestran los escenarios de coexistencia de App-V admitidos. Le recomendamos que instale las últimas actualizaciones disponibles de una versión determinada cuando esté ejecutando usuarios coexistentes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de cliente de App-V 4,6</th>
<th align="left">Tipo de cliente de App-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4,6 SP3</p></td>
<td align="left"><p>5.1 de App-V</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 SP3 RDS</p></td>
<td align="left"><p>App-V 5,1 RDS</p></td>
</tr>
</tbody>
</table>

 

### Requisitos para ejecutar clientes coexistentes

Para ejecutar los clientes coexistentes, debe hacer lo siguiente:

-   Instale el cliente de App-V 4.6 antes de instalar el cliente de App-V 5,1.

-   Habilite la opción **Habilitar modo de migración** de la Directiva de grupo, que se encuentra en el nodo de coexistencia de cliente **de App-V** &gt; **Client Coexistence** . Para implementar la plantilla. ADMX, consulte [Cómo descargar e implementar las plantillas de la Directiva de grupo de MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).

**Nota:**  Los paquetes de App-V 5,1 se pueden ejecutar en paralelo con los paquetes de App-V 4,6 Si tiene instalaciones coexistentes de App-V 5,1 y 4,6. Sin embargo, los paquetes de App-V 5,1 no pueden interactuar con paquetes de App-V 4,6 en el mismo entorno virtual.

 

### Descargas y documentación de clientes

La siguiente tabla proporciona vínculos a las descargas de los clientes de App-V 4,6 y a la documentación de TechNet acerca de las versiones. Entre las descargas se incluyen los clientes "normales" de App-V y RDS. La documentación de TechNet sobre el cliente de App-V se aplica a ambos clientes, a menos que se indique lo contrario.

<table>
<colgroup>
<col width="33%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión de App-V</th>
<th align="left">Vínculo a la documentación de TechNet</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4.6 SP3</p></td>
<td align="left"><p><a href="https://technet.microsoft.com/library/dn511019.aspx" data-raw-source="[About Microsoft Application Virtualization 4.6 SP3](https://technet.microsoft.com/library/dn511019.aspx)">Acerca de Microsoft Application Virtualization4.6SP3</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4.6 SP3</p></td>
<td align="left"><p><a href="about-app-v-51.md" data-raw-source="[About Microsoft Application Virtualization 5.1](about-app-v-51.md)">Acerca de Microsoft Application Virtualization 5,1</a></p></td>
</tr>
</tbody>
</table>

 

Para obtener más información sobre cómo configurar la coexistencia de clientes 5,1 de App-V, consulte:

-   [Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,1 en el mismo equipo](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

-   [Coexistencia y migración de App-V 5,0](https://technet.microsoft.com/windows/jj835811.aspx)

## <a href="" id="converting--previous-version--packages-using-the-package-converter-"></a>Conversión de paquetes "versión anterior" con el conversor de paquetes


Antes de migrar un paquete, creado con App-4.6 SP2 o una versión anterior, a App-V 5,1, revise los siguientes requisitos:

-   Debe convertir el paquete al formato de archivo **. appv** .

-   El convertidor de paquetes solo admite la conversión directa de paquetes que se crearon con App-V 4,5 y versiones posteriores. Para usar el convertidor de paquetes en un paquete que se creó con una versión anterior, debe usar una versión de App-V 4.5 o posterior del secuenciador para actualizar el paquete y, a continuación, puede realizar la conversión del paquete.

Para obtener más información sobre cómo usar el conversor de paquetes para convertir un paquete, consulte [Cómo convertir un paquete creado en una versión anterior de App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md). Después de convertir el archivo, puede implementarlo en equipos de destino que ejecuten el cliente de App-V 5,1.






## Temas relacionados


[Planificación de la implementación de App-V](planning-to-deploy-app-v51.md)

 

 





