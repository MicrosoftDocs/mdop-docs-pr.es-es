---
title: Introducción a App-V 5.1
description: Introducción a App-V 5.1
author: dansimp
ms.assetid: 49a20e1f-0566-4e53-a417-1521393fc974
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ff10f12bc672a24f2837f50bfb1f0033ede3e46f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814550"
---
# Introducción a App-V 5.1


Microsoft Application Virtualization (App-V) 5,1 permite a los administradores implementar, actualizar y admitir aplicaciones como servicios en tiempo real, según sea el caso. Las aplicaciones individuales se transforman de productos instalados de forma local en servicios administrados de forma centralizada y están disponibles dondequiera que lo necesite, sin necesidad de preconfigurar equipos ni de cambiar la configuración del sistema operativo.

App-V consta de los siguientes elementos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de administración de App-V</p></td>
<td align="left"><ul>
<li><p>Proporciona una ubicación central para administrar la infraestructura de App-V, que proporciona aplicaciones virtuales al cliente de escritorio de App-V y al cliente de servicios de escritorio remoto (anteriormente Terminal Services).</p></li>
<li><p>Usa Microsoft SQL Server® para su almacén de datos, en la que uno o varios servidores de administración de App-V pueden compartir un único almacén de datos de SQL Server.</p></li>
<li><p>Autentica las solicitudes y proporciona seguridad, medición, supervisión y recopilación de datos. El servidor usa Active Directory y herramientas de soporte para administrar usuarios y aplicaciones.</p></li>
<li><p>Tiene un sitio de administración que le permite configurar la infraestructura de App-V desde cualquier equipo. Puede Agregar y quitar aplicaciones, manipular accesos directos, asignar permisos de acceso a usuarios y grupos, y crear grupos de conexión.</p></li>
<li><p>Permite la comunicación entre la consola de administración web de App-V y la tienda de datos de SQL Server. Estos componentes se pueden instalar en un único equipo servidor o en uno o más equipos independientes, en función de la arquitectura del sistema requerida.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de publicación de App-V</p></td>
<td align="left"><ul>
<li><p>Proporciona clientes de App-V con aplicaciones tituladas para el usuario específico.</p></li>
<li><p>Hospeda el paquete de aplicación virtual para la transmisión por secuencias.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Cliente de escritorio de App-V</p></td>
<td align="left"><ul>
<li><p>Recupera aplicaciones virtuales</p></li>
<li><p>Publica las aplicaciones en los clientes.</p></li>
<li><p>Configura y administra automáticamente entornos virtuales en tiempo de ejecución en puntos de conexión de Windows.</p></li>
<li><p>Almacena la configuración de la aplicación virtual específica del usuario, como cambios de archivo y registro, en cada perfil de usuario&#39;s.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente de servicios de escritorio remoto (RDS) de App-V</p></td>
<td align="left"><p>Permite que los servidores host de sesión de escritorio remoto usen las funciones del cliente de escritorio de App-V para sesiones de escritorio compartidas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Secuenciador de App-V</p></td>
<td align="left"><ul>
<li><p>Es una herramienta basada en un asistente que se usa para transformar las aplicaciones tradicionales en aplicaciones virtuales.</p></li>
<li><p>Genera la aplicación "paquete", que consta de:</p>
<ol>
<li><p>un archivo de aplicación de secuencia (APPV)</p></li>
<li><p>un archivo de Windows Installer (MSI) que se puede implementar en clientes configurados para un funcionamiento independiente</p></li>
<li><p>Varios archivos XML, entre los que se incluyen Report.XML, PackageName_DeploymentConfig.XML y PackageName_UserConfig.XML. Los archivos XML UserConfig y DeploymentConfig se usan para configurar cambios personalizados en el comportamiento predeterminado del paquete.</p></li>
</ol></li>
</ul></td>
</tr>
</tbody>
</table>

 

Para obtener más información sobre estos elementos, consulte [arquitectura de alto nivel para App-V 5,1](high-level-architecture-for-app-v-51.md).

Si es nuevo en este producto, le recomendamos que lea la documentación minuciosamente. Antes de implementarlo en un entorno de producción, también le recomendamos que valide el plan de implementación en un entorno de red de prueba. También puede considerar tomar una clase sobre tecnologías relevantes. Para obtener más información sobre las oportunidades de aprendizaje de Microsoft, consulte la descripción general de aprendizaje de Microsoft en <https://go.microsoft.com/fwlink/p/?LinkId=80347> .

**Nota:**  Una versión descargable de esta guía del administrador no está disponible. Sin embargo, puede obtener información sobre un modo especial de la biblioteca de TechNet que le permite seleccionar artículos, agruparlos en una colección e imprimirlos o exportarlos a un archivo en <https://go.microsoft.com/fwlink/?LinkId=272491> ( https://go.microsoft.com/fwlink/?LinkId=272491) .

 

Esta sección de la guía del administrador de la 5,1 de App-V incluye información de alto nivel sobre App-V 5,1 para proporcionarle una comprensión básica del producto antes de comenzar con el plan de implementación.

## Introducción a App-V 5,1


-   [Acerca de App-V 5.1](about-app-v-51.md)

    Proporciona una descripción general de App-V 5,1 y cómo se puede usar en su organización.

-   [Evaluación de App-V 5.1](evaluating-app-v-51.md)

    Proporciona información sobre cómo puede evaluar mejor App-V 5,1 para usarlo en su organización.

-   [Arquitectura de alto nivel de App-V 5.1](high-level-architecture-for-app-v-51.md)

    Proporciona una descripción de las características de App-V 5,1 y cómo funcionan conjuntamente.

-   [Accesibilidad para App-V 5.1](accessibility-for-app-v-51.md)

    Proporciona información sobre características y servicios que hacen que este producto y la documentación correspondiente sean más accesibles para las personas con discapacidades.

## <a href="" id="other-resources-for-this-product-"></a>Otros recursos para este producto


-   [Guía del administrador de Microsoft Application Virtualization 5,1](microsoft-application-virtualization-51-administrators-guide.md)

-   [Planificación de App-V 5.1](planning-for-app-v-51.md)

-   [Implementación de App-V 5.1](deploying-app-v-51.md)

-   [Operaciones de App-V 5.1](operations-for-app-v-51.md)

-   [Resolución de problemas de App-V 5.1](troubleshooting-app-v-51.md)

-   [Referencia técnica de App-V 5.1](technical-reference-for-app-v-51.md)






 

 





