---
title: Métodos de sincronización para UE-V 2.x
description: Métodos de sincronización para UE-V 2.x
author: dansimp
ms.assetid: af0ae894-dfdc-41d2-927b-c2ab1b355ffe
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a163442e2ab3dbd777aca133b13b0086cdb8ae1a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823580"
---
# Métodos de sincronización para UE-V 2.x


El agente de Microsoft User Experience Virtualization (UE-V) 2,0, 2,1 y 2,1 SP1 le permite sincronizar la configuración de Windows y de la aplicación de los usuarios con la ubicación de almacenamiento de configuración. La configuración del *método de sincronización* define cómo UE-V Agent carga y descarga esa configuración en la ubicación de almacenamiento de configuración. UE-V 2. x introduce una nueva SyncMethod denominada *SyncProvider*. Para obtener más información sobre los eventos desencadenadores que inician la sincronización de la configuración de la aplicación y de Windows, consulte [sincronizar eventos desencadenadores para UE-V 2. x](sync-trigger-events-for-ue-v-2x-both-uevv2.md).

## Configuración de SyncMethod


En esta tabla se explican los cambios de SyncMethod de UE-V v 1.0 a v 2.0 a v 2.1, así como la configuración de cada configuración:

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configuración de SyncMethod</strong></p></td>
<td align="left"><p><strong>V 1.0</strong></p></td>
<td align="left"><p><strong>V 2.0</strong></p></td>
<td align="left"><p><strong>V 2.1 y V 2.1 SP1</strong></p></td>
<td align="left"><p><strong>Descripción</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncProvider</p></td>
<td align="left"><p>n/d</p></td>
<td align="left"><p>Predeterminado</p></td>
<td align="left"><p>Predeterminado</p></td>
<td align="left"><p>Los cambios de configuración para una aplicación específica o para la configuración de escritorio global de Windows se guardan de forma local en una carpeta de caché. Estos cambios se sincronizan con la ubicación de almacenamiento de configuración cuando tiene lugar un evento de activación de sincronización. Al presionar los cambios se guardarán los cambios locales en la ruta de almacenamiento de configuración.</p>
<p>Esta configuración predeterminada es la norma Gold para equipos. Esta opción intenta sincronizar la configuración y se agota el tiempo de espera después de un breve retraso para garantizar que el inicio de la aplicación o del sistema operativo no se retrase durante un período de tiempo prolongado.</p>
<p>Esta funcionalidad también está vinculada a la tarea programada: aplicación de controlador de sincronización. El administrador controla la frecuencia de la tarea programada. De forma predeterminada, los equipos sincronizan su configuración cada 30 minutos después de iniciar sesión.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>OfflineFiles</p></td>
<td align="left"><p>Predeterminado</p></td>
<td align="left"><p>En desuso</p></td>
<td align="left"><p>En desuso</p></td>
<td align="left"><p>Se comporta de la misma manera que SyncProvider en V 2.0.</p>
<p>Si los archivos sin conexión están habilitados y la carpeta está anclada, UE-V desanclará esta carpeta y se sincronizará directamente con el directorio central SMB.</p>
<p><strong>Nota: </strong> en V 1.0 si desea usar UE-V en una sociedad corporativa desconectada (también conocido como un viaje con un equipo portátil), la guía consiste en usar archivos sin conexión para asegurarse de que la configuración se ha movido.Hemos recibido suficientes comentarios de los clientes para que la activación de archivos sin conexión sea un bloqueo empresarial no trivial. Por tanto, en UE-V 2, hemos creado un motor de sincronización estrechamente acoplado para almacenar los datos de forma local y sincronizar la configuración con el servidor central. Este área de características no reemplaza los archivos sin conexión ni el redireccionamiento de carpetas.</p>
<p>UE-V 2 no funciona bien con las carpetas sin conexión, de modo que la orientación no es establecer la ruta de almacenamiento de configuración en una carpeta anclada sin conexión o CSC.</p></td>
</tr>
<tr class="even">
<td align="left"><p>External</p></td>
<td align="left"><p>n/d</p></td>
<td align="left"><p>n/d</p></td>
<td align="left"><p>Se admite</p></td>
<td align="left"><p>Nuevo en UE-V 2,1, este método de configuración especifica que si la configuración de UE-V se escribe en una carpeta local en el equipo del usuario, cualquier motor de sincronización externo (como OneDrive para la empresa, carpetas de trabajo, SharePoint o Dropbox) se puede usar para aplicar esta configuración a los diferentes equipos a los que los usuarios tienen acceso.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Esta configuración está diseñada para la experiencia de infraestructura de escritorio virtual (VDI) y la de aplicaciones transmitidas principalmente. Esta configuración debe usarse en los cuadros de Windows Server que se usan en un centro de recursos, donde la conexión siempre estará disponible.</p>
<p>Los cambios de configuración se guardan directamente en el servidor. Si la conexión de red a la ruta de almacenamiento de configuración no está disponible, los cambios de configuración se almacenarán en caché en el dispositivo y se sincronizarán la próxima vez que se ejecute el proveedor de sincronización. Si no se encuentra la ruta de almacenamiento de configuración y el perfil de usuario se quita de un entorno de VDI agrupado al cerrar sesión, se perderán estos cambios de configuración y el usuario deberá volver a aplicar el cambio cuando el equipo pueda volver a la ruta de almacenamiento de configuración.</p>
<p>Las aplicaciones y el sistema operativo esperarán indefinidamente a que la ubicación esté presente. Esto podría provocar que el tiempo de inicio de sesión de un sistema operativo o la carga de la aplicación aumente significativamente si no se encuentra la ubicación.</p></td>
</tr>
</tbody>
</table>

 

Puede configurar el método de sincronización de las siguientes maneras:

-   Al [implementar el agente de UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) con un parámetro de línea de comandos o en un script de proceso por lotes

-   Mediante la configuración de [Directiva de grupo](https://technet.microsoft.com/library/dn458893.aspx)

-   Con [System Center Configuration Pack](https://technet.microsoft.com/library/dn458917.aspx) para UE-V

-   Después de la instalación de UE-V Agent, mediante [Windows PowerShell o el instrumental de administración de Windows (WMI)](https://technet.microsoft.com/library/dn458937.aspx)






## Temas relacionados


[Implementar funciones necesarias para UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md#ssl)

[Implementar funciones necesarias para UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md#config)

[Referencia técnica de UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





