---
title: Implementación de la ubicación de almacenamiento de configuración de UE-V 1.0
description: Implementación de la ubicación de almacenamiento de configuración de UE-V 1.0
author: dansimp
ms.assetid: b187d44d-649b-487e-98d3-a61ee2be8c2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c179be0882bc6a0efc0f11f21fc231f03b63b0fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826640"
---
# Implementación de la ubicación de almacenamiento de configuración de UE-V 1.0


La implementación de la virtualización de la experiencia del usuario de Microsoft (UE-V) requiere una ubicación de almacenamiento de configuración donde se almacena la configuración de usuario en un archivo de paquete de configuración. La ubicación de almacenamiento de configuración se puede configurar de una de las siguientes dos maneras:

-   **Directorio principal de Active** Directory: si se define un directorio particular para el usuario en Active Directory, UE-V Agent usará esta ubicación para almacenar los paquetes de ubicación de configuración. UE-V Agent crea dinámicamente la carpeta de almacenamiento específica del usuario que se encuentra debajo de la raíz del directorio de inicio. El agente solo usa el directorio de inicio de Active Directory si no se ha definido una ubicación de almacenamiento de configuración.

-   **Crear un recurso compartido de almacenamiento de configuración** : el recurso de almacenamiento de configuración es un recurso compartido de red estándar accesible para los usuarios de UE-V.

## Implementar un recurso de almacenamiento de configuración de UE-V


Al crear el recurso compartido de almacenamiento de configuración, debe limitar el acceso a los usuarios que lo necesiten. Los permisos necesarios se muestran en las tablas siguientes.

**Para implementar el recurso compartido de red UE-V**

1.  Cree un nuevo grupo de seguridad para usuarios de UE-V.

2.  Cree una nueva carpeta en el equipo centralizado que almacenará los paquetes de configuración de UE-V y, a continuación, conceda a los usuarios de UE-V con permisos de grupo a la carpeta. El administrador que admita UE-V necesitará permisos para esta carpeta compartida.

3.  Establezca los siguientes permisos de nivel de uso compartido (SMB) para la carpeta de ubicación de almacenamiento de configuración:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Cuenta de usuario</strong></th>
    <th align="left"><strong>Permisos recomendados</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Todos</p></td>
    <td align="left"><p>No hay permisos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Grupo de seguridad de los usuarios de UE-V</p></td>
    <td align="left"><p>Control total</p></td>
    </tr>
    </tbody>
    </table>

     

4.  Configure los siguientes permisos NTFS para la carpeta de ubicación de almacenamiento de configuración:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong>Cuenta de usuario</strong></th>
    <th align="left"><strong>Permisos recomendados</strong></th>
    <th align="left"><strong>Carpeta</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creador/propietario</p></td>
    <td align="left"><p>Control total</p></td>
    <td align="left"><p>Solo subcarpetas y archivos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Grupo de seguridad de los usuarios de UE-V</p></td>
    <td align="left"><p>Listar carpeta/leer datos, crear carpetas/anexar datos</p></td>
    <td align="left"><p>Solo esta carpeta</p></td>
    </tr>
    </tbody>
    </table>

     

5.  Haga clic en **Aceptar** para cerrar los cuadros de diálogo.

Esta configuración de permisos permite a los usuarios crear carpetas para el almacenamiento de configuración. El agente UE-V crea y protege una `settingspackage` carpeta mientras se ejecuta en el contexto del usuario. El usuario recibe el control total de su `settingspackage` carpeta. Otros usuarios no heredan el acceso a esta carpeta. No es necesario crear ni proteger directorios de usuario individuales, ya que el agente que se ejecuta en el contexto del usuario lo hará automáticamente.

**Nota:**  Se puede configurar la seguridad adicional cuando se usa un servidor de Windows para el recurso de almacenamiento de configuración. UE-V se puede configurar para comprobar que el grupo de administradores local o el usuario actual es el propietario de la carpeta donde se almacenan los paquetes de configuración. Para habilitar la seguridad adicional, siga este procedimiento:

1.  Agregue una clave del registro **reg \ _DWORD** denominada "RepositoryOwnerCheckEnabled" a **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration.**

2.  Establezca el valor de la clave del registro en 1.

 

## Temas relacionados


[Implementación de UE-V 1.0](deploying-ue-v-10.md)

[Configuraciones admitidas para UE-V 1.0](supported-configurations-for-ue-v-10.md)

Implementar el almacenamiento central de configuración de virtualización de la experiencia de usuario paquetes de configuración y plantillas [instalar el generador de UE-V](installing-the-ue-v-generator.md)

[Implementación del agente de UE-V](deploying-the-ue-v-agent.md)

 

 





