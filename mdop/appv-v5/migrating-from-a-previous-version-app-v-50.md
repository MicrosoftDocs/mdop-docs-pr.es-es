---
title: Migrar desde una versión anterior
description: Migrar desde una versión anterior
author: dansimp
ms.assetid: a13cd353-b22a-48f7-af1e-5d54ede2a7e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a05bbd498cdb77a1ddf694b1aab6aeb42124775b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813558"
---
# Migrar desde una versión anterior


Con App-V 5,0 puede migrar la infraestructura de App-V 4,6 existente a la infraestructura más flexible, integrada y de administración de App-V 5,0 más sencilla.

Considere las siguientes secciones al planear la estrategia de migración:

**Nota:**  Para obtener más información sobre las diferencias entre App-V 4,6 y App-V 5,0, consulte las **diferencias entre App-v 4,6 y la sección App-v 5,0** de [acerca de App-v 5,0](about-app-v-50.md).

 

## Conversión de paquetes creados con una versión anterior de App-V


Use la utilidad de conversión de paquetes para actualizar paquetes de aplicaciones virtuales creados con versiones anteriores de App-V. El convertidor de paquetes usa PowerShell para convertir paquetes y puede ayudar a automatizar el proceso si tiene muchos paquetes que requieren conversión.

**Importante**  Después de convertir un paquete existente, debe probar el paquete antes de implementar el paquete para asegurarse de que el proceso de conversión se realizó correctamente.

 

**Qué debe saber antes de convertir paquetes existentes**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Problema</th>
<th align="left">Solución alternativa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Los scripts de paquetes no se convierten.</p></td>
<td align="left"><p>Pruebe el paquete convertido. Si es necesario, convierta el script.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Las invalidaciones de configuración del registro de paquetes no se convierten.</p></td>
<td align="left"><p>Pruebe el paquete convertido. Si es necesario, vuelva a agregar las invalidaciones del registro.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Los paquetes virtuales que usan DSC no se vinculan después de la conversión.</p></td>
<td align="left"><p>Vincule los paquetes usando grupos de conexión. Consulte <a href="managing-connection-groups.md" data-raw-source="[Managing Connection Groups](managing-connection-groups.md)"> Administración de grupos de conexión </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Los conflictos de variables de entorno se detectan durante la conversión.</p></td>
<td align="left"><p>Resuelva los conflictos en el <strong> archivo. OSD asociado </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Las rutas de código no modificables se detectan durante la conversión.</p></td>
<td align="left"><p>Las rutas de código no modificables son difíciles de convertir correctamente. El convertidor de paquetes detectará y devolverá paquetes con archivos que contienen rutas de código no modificables. Visualice el archivo con la ruta de acceso del código y determine si el paquete necesita el archivo. En ese caso, se recomienda volver a crear el paquete.</p></td>
</tr>
</tbody>
</table>

 

Al convertir un paquete, comprobar si hay errores en los archivos o en los accesos directos. Busque el elemento en el paquete de App-V 4,6. Es posible que se deba a una ruta de acceso no modificable. Convertir la ruta de acceso.

**Nota:**  Se recomienda usar el secuenciador App-V 5,0 para convertir aplicaciones críticas o aplicaciones que necesiten aprovechar las características. Vea [Cómo secuenciar una nueva aplicación con App-V 5,0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md).

Si un paquete convertido no se abre después de convertirlo, también se recomienda que vuelva a realizar la secuencia de la aplicación con el secuenciador de aplicaciones-V 5,0.

 

[Cómo convertir un paquete creado en una versión anterior de App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

## Migrar clientes


En la tabla siguiente se muestra el método recomendado para actualizar clientes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Actualizar el entorno a App-V 4.6 SP2</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Implementación de virtualización de aplicaciones y consideraciones de actualización </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Instale el cliente de App-V 5,0 con la coexistencia habilitada.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.0 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)">Cómo implementar el cliente de App-V 4,6 y App-V 5,0 en el mismo equipo </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Secuencia y lanzamiento de paquetes de aplicaciones-V 5,0. Según sea necesario, vuelva a publicar los paquetes de App-V 4,6.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)">Cómo secuencia una nueva aplicación con App-V 5,0 </a> .</p></td>
</tr>
</tbody>
</table>

 

**Importante**  Para poder usar el modo de coexistencia, debe estar ejecutando App-V 4.6 SP3. Además, al secuenciar un paquete, debe configurar la configuración de la autoridad de administración, que se encuentra en la **configuración del usuario** , en la sección **configuración de usuario** .

 

## Migrar la infraestructura completa de App-V 5,0 Server


No hay ningún método directo para actualizar a una infraestructura completa de App-V 5,0. Use la información de la siguiente sección para obtener información sobre cómo actualizar el servidor de App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Actualice su entorno a App-V 4.6 SP3.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Implementación de virtualización de aplicaciones y consideraciones de actualización </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Implemente la versión de App-V 5,0 del cliente.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)">Cómo implementar el cliente de App-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Instale App-V 5,0 Server.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-50-server-50sp3.md" data-raw-source="[How to Deploy the App-V 5.0 Server](how-to-deploy-the-app-v-50-server-50sp3.md)">Cómo implementar el servidor de App-V 5,0 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Migrar paquetes existentes.</p></td>
<td align="left"><p>Consulte la <strong> sección convertir paquetes creados con una versión anterior de App-V </strong> de este artículo.</p></td>
</tr>
</tbody>
</table>

 

## Tareas adicionales de migración


También puede realizar tareas adicionales de migración, como cambiar la configuración de los extremos, así como abrir un paquete creado con una versión anterior en un equipo que ejecute el cliente de App-V 5,0. Los vínculos siguientes proporcionan más información sobre cómo realizar estas tareas.

[Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.0 convertido para todos los usuarios de un equipo específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

[Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.0 para un usuario específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

[Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Cómo revertir puntos de extensión desde un paquete App-V 5.0 a un paquete de App-V 4.6 para un usuario específico](how-to-revert-extension-points-from-an-app-v-50-package-to-an-app-v-46-package-for-a-specific-user.md)







## Otros recursos para realizar tareas de migración de App-V


[Operaciones de App-V 5.0](operations-for-app-v-50.md)

[Un procedimiento simplificado para la actualización del servidor de administración de Microsoft App-V 5,1](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





