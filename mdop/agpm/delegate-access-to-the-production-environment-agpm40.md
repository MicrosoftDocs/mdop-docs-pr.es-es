---
title: Delegar el acceso al entorno de producción
description: Delegar el acceso al entorno de producción
author: dansimp
ms.assetid: 4c670581-8c47-41ea-80eb-02846ff1ec1f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a3920a8ba5835cbbcb8a74f0af4e3ca1e1c5f43f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818730"
---
# Delegar el acceso al entorno de producción


En administración avanzada de directivas de grupo (AGPM), puede cambiar el acceso a objetos de directiva de grupo (GPO) en el entorno de producción del dominio, sustituyendo los permisos existentes en esos GPO. Puede configurar permisos en el nivel de dominio para permitir o impedir que los usuarios editen, eliminen o modifiquen la seguridad de los GPO en el entorno de producción cuando no usen la carpeta de **control de cambios** en la consola de administración de directivas de grupo (GPMC).

**Nota**  
-   Cambiar la forma en que se delega el acceso al entorno de producción no afecta la capacidad de los usuarios para vincular GPO.

-   Cuando se controlan o implementan los GPO, se quita el acceso de cualquier otra cuenta, excepto las que tengan permisos de **lectura** y **aplicación** .

 

Para completar este procedimiento, se requiere una cuenta de usuario que tenga el rol de administrador de AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para cambiar el acceso a los GPO en el entorno de producción del dominio**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  Haga clic en la pestaña **delegación de producción** .

3.  Para agregar permisos para un usuario o grupo que no tiene acceso al entorno de producción, o para reemplazar los permisos de un usuario o grupo que tiene acceso:

    1.  Haga clic en **Agregar**, seleccione un usuario o grupo y, a continuación, haga clic en **Aceptar**.

    2.  Seleccione los permisos para delegar a ese usuario o grupo en el entorno de producción y, a continuación, haga clic en **Aceptar**.

4.  Para quitar todos los permisos en el entorno de producción de un usuario o grupo, seleccione el usuario o el grupo, haga clic en **quitar**y, a continuación, haga clic en **Aceptar**.

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener permiso de **modificación de seguridad** para el dominio.

-   Los permisos para la cuenta del servicio AGPM no se pueden cambiar en la pestaña **delegación de producción** .

-   De forma predeterminada, las siguientes cuentas tienen permisos para los GPO en el entorno de producción:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Cuenta</th>
    <th align="left">Permisos predeterminados para GPO</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>&lt;Cuenta de servicio AGPM&gt;</p></td>
    <td align="left"><p>Editar configuración, eliminar, modificar seguridad</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Usuarios autenticados</p></td>
    <td align="left"><p>Leer, aplicar</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administradores de dominio</p></td>
    <td align="left"><p>Editar configuración, eliminar, modificar seguridad</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administradores de empresa</p></td>
    <td align="left"><p>Editar configuración, eliminar, modificar seguridad</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Controladores de dominio empresariales</p></td>
    <td align="left"><p>Leer</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Sistema</p></td>
    <td align="left"><p>Editar configuración, eliminar, modificar seguridad</p></td>
    </tr>
    </tbody>
    </table>

     

-   Se debe restringir la pertenencia al grupo propietarios del creador de directivas de grupo, Soit no se usa para burlar la administración de AGPM de acceso a los GPO. (En la **consola de administración de directivas de grupo**, haga clic en **objetos de directiva de grupo** en el bosque y el dominio en el que desee administrar los GPO, haga clic en **delegación**y configure las opciones para satisfacer las necesidades de su organización).

### Referencias adicionales

-   [Configuración de Administración avanzada de directivas de grupo](configuring-advanced-group-policy-management-agpm40.md)

 

 





