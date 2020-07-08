---
title: Novedades de App-V 5.0
description: Novedades de App-V 5.0
author: dansimp
ms.assetid: 79ff6e02-e926-4803-87d8-248a6b28099d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dabe264f033bd5c9897f07d931f799a42e6b72e9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813222"
---
# Novedades de App-V 5.0


Esta sección está deshabilitada para usuarios que ya están familiarizados con App-v y desean saber qué ha cambiado en App-V 5,0 si aún no está familiarizado con App-V, debe empezar por leer la [planificación de App-v 5,0](planning-for-app-v-50-rc.md).

## Cambios en la funcionalidad estándar


Las secciones siguientes contienen información sobre los cambios en la funcionalidad estándar de App-V 5,0.

### Cambios en los sistemas operativos compatibles

Para obtener más información, consulte [configuraciones admitidas de App-V 5,0](app-v-50-supported-configurations.md).

## Cambios en el secuenciador


Las secciones siguientes contienen información sobre los cambios en el secuenciador de 5,0 de App-V.

### Cambio específico en el secuenciador

En la siguiente tabla se muestra información sobre lo que ha cambiado con el secuenciador de 5,0 de App-V

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Característica secuenciador</th>
<th align="left">Funcionalidad de App-V 5,0 SPRJ</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Procesamiento de reinicio</p></td>
<td align="left"><p>Cuando una aplicación solicite un reinicio, debe permitir que la aplicación reinicie el equipo que ejecuta el secuenciador. El equipo que ejecuta el secuenciador se reiniciará y el secuenciador se reanudará en el modo de supervisión.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Especificar el directorio de aplicación virtual</p></td>
<td align="left"><p>El directorio de aplicación virtual es un parámetro obligatorio. Para obtener los mejores resultados, debe coincidir con el directorio de instalación del instalador de la aplicación. Esto da como resultado un rendimiento más óptimo y una compatibilidad de aplicaciones.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Editar métodos abreviados de teclado/FTAs</p></td>
<td align="left"><p>La página de accesos directos/FTA está en la <strong> </strong> Página edición avanzada después de que el Asistente de secuencias haya finalizado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Pestaña Historial de cambios</p></td>
<td align="left"><p>Se ha quitado la pestaña historial de cambios de App-V 5,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pestaña OSD</p></td>
<td align="left"><p>Se ha quitado la ficha OSD para App-V 5,0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Pestaña Servicios virtuales</p></td>
<td align="left"><p>Se ha quitado la pestaña de servicios virtuales de App-V 5,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pestaña archivos/sistema de archivos virtual</p></td>
<td align="left"><p>Estas pestañas se combinan y le permiten modificar los archivos de paquete.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Pestaña Implementación</p></td>
<td align="left"><p>Ya no hay opciones para configurar la dirección URL del servidor en los paquetes. Debe configurarlo ahora con la configuración de implementación o el servidor de administración.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Herramienta de conversión de paquetes</p></td>
<td align="left"><p>Ahora puede usar PowerShell para convertir paquetes creados en versiones anteriores.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Complemento/middleware</p></td>
<td align="left"><p>Puede expandir paquetes primarios al secuenciar un complemento o una aplicación middleware. Los complementos y paquetes de middleware se deben conectar con los grupos de conexión de App-V 5,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Resultados de archivos</p></td>
<td align="left"><p>Los siguientes archivos se crean con App-V 5,0, Windows Installer (. msi),. appv, configuración de implementación, configuración de usuario y el Report.XML.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Paquetes de descriptores de seguridad/de compresión/MSI</p></td>
<td align="left"><p>La compresión y la creación de un archivo de Windows Installer (. msi) son automáticas para todos los paquetes y ya no puede invalidar los descriptores de seguridad.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Herramientas/opciones</p></td>
<td align="left"><p>Se ha quitado la ventana diagnósticos, así como otras opciones.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Unidad de instalación</p></td>
<td align="left"><p>Una unidad de instalación ya no es necesaria cuando se instala una aplicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OOS streaming</p></td>
<td align="left"><p>Si no se realiza ninguna optimización de flujo, los paquetes se muestran con errores de transmisión cuando los solicitan los equipos que ejecutan el cliente de App-V 5,0 hasta que se puedan iniciar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Q: &lt; /p&gt;</td>
<td align="left"><p>App-V 5,0 usa el sistema de archivos nativo y ya no necesita un Q:.</p></td>
</tr>
</tbody>
</table>

 

## Detección de errores de secuenciación


El secuenciador de 5,0 de App-V puede detectar problemas de secuencia comunes durante la secuencia. La página del **Informe de instalación** al final del asistente de secuenciación muestra mensajes de diagnóstico clasificados en **errores**, **advertencias**e **información** , según la gravedad del problema.

Para mostrar información más detallada sobre un evento, haga doble clic en el elemento que desea revisar en el informe. Se muestran los problemas de secuenciación, así como sugerencias sobre cómo resolver los problemas. La información del informe de preparación del sistema y el informe de instalación se resumirán cuando haya terminado de crear un paquete. En la siguiente lista se muestran los tipos de problemas disponibles en el informe:

-   Archivos excluidos.

-   Información del controlador.

-   Diferencias del sistema COM+.

-   Conflictos en paralelo (SxS).

-   Extensiones de Shell.

-   Información sobre los servicios no admitidos.

-   Distribuí.

## Grupos de conexión


La característica App-V, anteriormente conocida como la **composición de conjunto dinámico** , ahora se denomina **grupos de conexión** en App-V 5,0. Para obtener más información sobre cómo usar los grupos de conexión, consulte [administrar grupos de conexión](managing-connection-groups.md).

## Funcionalidad de licencias y medición


Se ha quitado la funcionalidad de licencias y aplicaciones en App-V 5,0. Las posiciones de licencias reales de su entorno dependen de la licencia de título de software específica y de los derechos de uso otorgados por los términos de licencia relacionados.

## Caché de aplicaciones y archivos


No hay ninguna caché de aplicaciones o archivos disponibles con App-V 5,0.






## Temas relacionados


[Acerca de App-V 5.0](about-app-v-50.md)

 

 





