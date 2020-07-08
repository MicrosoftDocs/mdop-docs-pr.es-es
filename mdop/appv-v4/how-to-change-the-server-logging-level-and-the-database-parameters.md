---
title: Cómo cambiar el nivel de registro de servidor y los parámetros de la base de datos
description: Cómo cambiar el nivel de registro de servidor y los parámetros de la base de datos
author: dansimp
ms.assetid: e3ebaee5-6c4c-4aa8-9766-c5aeb00f477a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bb35ac09c5e23f4847662171b68284f868e66dee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818031"
---
# Cómo cambiar el nivel de registro de servidor y los parámetros de la base de datos


Puede usar los procedimientos siguientes para cambiar el nivel de registro y los parámetros del registro de base de datos de la consola de administración del servidor de virtualización de aplicaciones.

Los siguientes niveles de registro están disponibles:

-   Solo transacción

-   Errores graves

-   Errores

-   Advertencias/errores

-   Información, advertencias o errores

-   Detallado

**Nota:**  Debido al tamaño del archivo de registro producido al usar el modo **detallado** , se recomienda no ejecutar servidores de producción con este nivel de conjunto de registro.

 

Los parámetros de registro de base de datos determinan el tipo de controlador de base de datos, las credenciales de acceso y la ubicación de la base de datos.

**Para cambiar el nivel de registro de los servidores de administración**

1.  Haga clic en el nodo **grupos de servidores** para mostrar los grupos de servidores.

2.  Haga clic con el botón secundario en el grupo de servidores y seleccione **propiedades**.

3.  En el cuadro de diálogo **propiedades** , seleccione la ficha **registro** .

4.  En el cuadro de diálogo **propiedades del grupo de servidores** , seleccione el servidor y haga clic en **Editar**.

5.  En el cuadro de diálogo **Agregar/editar módulo de registro** , seleccione el nivel de registro en la lista desplegable **tipo de evento** .

6.  Haga clic en **Aceptar**.

7.  En el cuadro de diálogo **propiedades del grupo de servidores** , haga clic en **Aceptar** o **aplicar**.

**Para cambiar el nivel de registro de los servidores de streaming**

1.  Edite el siguiente valor de la clave del registro para cambiar el nivel de registro:

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\DistributionServer\\LogLevel

2.  Seleccione uno de los siguientes valores para establecer el nivel de registro.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Valor</th>
    <th align="left">Nivel de registro</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>,0</p></td>
    <td align="left"><p>Solo transacciones</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>uno</p></td>
    <td align="left"><p>Errores graves</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>1</p></td>
    <td align="left"><p>Errores</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>2</p></td>
    <td align="left"><p>Advertencias/errores</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>cuatro</p></td>
    <td align="left"><p>Información, advertencias o errores</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>4</p></td>
    <td align="left"><p>Detallado</p></td>
    </tr>
    </tbody>
    </table>

     

**Para cambiar los parámetros del registro de base de datos**

1.  Haga clic en el nodo **grupos de servidores** para mostrar los grupos de servidores.

2.  Haga clic con el botón secundario en el grupo de servidores y seleccione **propiedades**.

3.  En el cuadro de diálogo **propiedades** , seleccione la ficha **registro** .

4.  En el cuadro de diálogo **propiedades del grupo de servidores** , seleccione el servidor y haga clic en **Editar**.

5.  En el cuadro de diálogo **Agregar/editar módulo de registro** , seleccione un controlador de base de datos en la lista desplegable **controlador de base de datos** .

6.  Escriba un **nombre de host DNS**.

7.  Haga clic en la casilla **determinar el puerto de forma dinámica** o escriba un número de puerto en el campo **Puerto** .

8.  Escriba un **nombre de servicio** en el campo correspondiente.

9.  Haga clic en **Aceptar**.

10. En el cuadro de diálogo **propiedades del grupo de servidores** , haga clic en **Aceptar** o **aplicar**.

## Temas relacionados


[Cómo personalizar un sistema de virtualización de aplicaciones en la consola de administración de servidor](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

 

 





