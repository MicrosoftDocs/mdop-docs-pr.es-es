---
title: Implementación del catálogo de plantillas de configuración de UE-V 1.0
description: Implementación del catálogo de plantillas de configuración de UE-V 1.0
author: dansimp
ms.assetid: 0e6ab5ef-8eeb-40b4-be7b-a841bd83be96
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f342daa958607a077fa5eb2a27ec705c8d99e67f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826631"
---
# Implementación del catálogo de plantillas de configuración de UE-V 1.0


Las plantillas de ubicación de configuración personalizadas se pueden almacenar en una ruta de carpeta en equipos de virtualización de Microsoft User Experience (UE-V) o en un recurso compartido de red de bloque de mensajes de servidor (SMB). Una tarea programada en el equipo comprueba si hay plantillas nuevas o actualizadas de esta ubicación. La tarea comprueba esta ubicación una vez al día y actualiza su comportamiento de sincronización en función de las plantillas de esta carpeta. Las plantillas que se agregan o actualizan en esta carpeta desde la última comprobación son registradas por el agente de UE-V. UE-V Agent cancela el registro de las plantillas que se quitaron de esta carpeta. La tarea programada se ejecuta como sistema. Como mínimo, el recurso compartido de red debe conceder permisos para el grupo equipos del dominio. Además, conceda permisos de acceso a la carpeta de recursos compartidos de red a los administradores que administrarán las plantillas almacenadas. Para obtener más información sobre las plantillas de ubicación de configuración personalizadas, consulte [planificación de la implementación de plantillas personalizadas para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

**Para configurar el catálogo de plantillas de configuración para UE-V**

1.  Cree una nueva carpeta en el equipo en el que se guardará el catálogo de plantillas de configuración de UE-V.

2.  Establezca los siguientes permisos de nivel de uso compartido (SMB) para la carpeta de catálogos de plantillas de configuración.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Cuenta de usuario</strong></th>
    <th align="left"><strong>Recomendar permisos</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Todos</p></td>
    <td align="left"><p>No hay permisos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Equipos del dominio</p></td>
    <td align="left"><p>Niveles de permisos de lectura</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administradores</p></td>
    <td align="left"><p>Niveles de permisos de lectura y escritura</p></td>
    </tr>
    </tbody>
    </table>

     

3.  Configure los siguientes permisos NTFS para la carpeta del catálogo de plantillas de configuración.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Cuenta de usuario</th>
    <th align="left">Permisos recomendados</th>
    <th align="left">Aplicar a</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creador/propietario</p></td>
    <td align="left"><p>Control total</p></td>
    <td align="left"><p>Esta carpeta, subcarpetas y archivos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Equipos del dominio</p></td>
    <td align="left"><p>Mostrar el contenido de la carpeta y leer</p></td>
    <td align="left"><p>Esta carpeta, subcarpetas y archivos</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Todos</p></td>
    <td align="left"><p>No hay permisos</p></td>
    <td align="left"><p>No hay permisos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administradores</p></td>
    <td align="left"><p>Control total</p></td>
    <td align="left"><p>Esta carpeta, subcarpetas y archivos</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Haga clic en **Aceptar** para cerrar los cuadros de diálogo.

## Temas relacionados


[Implementación de UE-V 1.0](deploying-ue-v-10.md)

[Planificación de la implementación de la plantilla personalizada para UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

 

 





