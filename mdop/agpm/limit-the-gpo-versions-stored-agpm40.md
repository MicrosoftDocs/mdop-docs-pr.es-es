---
title: Limitar las versiones de GPO almacenados
description: Limitar las versiones de GPO almacenados
author: dansimp
ms.assetid: d802c7b6-f303-4b23-aefd-f19f1300b0ff
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: df6f6df2e2b1bae2cd972b67b76c27905622a723
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820620"
---
# Limitar las versiones de GPO almacenados


De forma predeterminada, todas las versiones de cada objeto de directiva de grupo (GPO) controlado se conservan en el archivo en el servidor de AGPM. Sin embargo, puede limitar el número de versiones que se conservan para cada GPO y eliminar las versiones anteriores cuando se supere ese límite. Cuando se eliminan versiones de GPO, un registro de la versión permanece en el historial del GPO, pero la versión de GPO en sí se elimina del archivo.

Para completar este procedimiento, debe tener una cuenta de usuario con el rol de administrador de AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para limitar el número de versiones de GPO almacenadas**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En el panel de detalles, haga clic en la pestaña **servidor de AGPM** .

3.  Active la casilla **Eliminar versiones anteriores de cada GPO del archivo** y escriba el número máximo de versiones de GPO para almacenar para cada GPO, sin incluir la versión actual. Para conservar solo la versión actual, escriba 0. El máximo no debe ser mayor que 999.

    **Importante**  Solo las versiones de GPO mostradas en la pestaña **versiones únicas** de la ventana **historial** recuenton el límite.

     

4.  Haga clic en el botón **aplicar** .

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener los permisos **Mostrar contenido** y **modificar opciones** para el dominio.

-   Para evitar que se elimine una versión de GPO, márquelo en el historial como no apto para la eliminación. Para ello, haga clic con el botón secundario en la versión del historial del GPO y haga clic en no **eliminar**.

### Referencias adicionales

-   [Administración del archivo](managing-the-archive-agpm40.md)

 

 





