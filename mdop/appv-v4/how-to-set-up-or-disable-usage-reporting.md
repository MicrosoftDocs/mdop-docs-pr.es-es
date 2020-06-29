---
title: Cómo configurar o deshabilitar el informe de uso
description: Cómo configurar o deshabilitar el informe de uso
author: dansimp
ms.assetid: 8587003a-128d-4b5d-ac70-5b9eddddd3dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f8f6c44d4060581f1ebe435875bc2f105cb93d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816550"
---
# Cómo configurar o deshabilitar el informe de uso


Puede usar los procedimientos siguientes en la consola de administración de Application Virtualization Server para especificar la duración (en meses) de la información de uso del sistema de virtualización de aplicaciones que desea almacenar en la base de datos.

**Nota:**  Para almacenar información de uso, debe seleccionar la casilla **registrar información de uso** en la pestaña **canalización del proveedor** . Para mostrar esta pestaña, haga clic con el botón secundario en la Directiva de proveedor en el panel de **resultados de directivas del proveedor** y seleccione **propiedades**.

 

**Para configurar los informes de uso**

1.  Haga clic con el botón derecho en el nodo del sistema de virtualización de aplicaciones en el panel izquierdo y seleccione **Opciones del sistema**.

2.  Seleccione la pestaña **base de datos** .

3.  Seleccione el botón **de radio mantener uso para (meses)** o **mantener todo el uso** .

4.  Si decide especificar la duración del uso en meses, escriba un número entre 1 y 120 (el valor predeterminado es de 6 meses). Si selecciona **mantener todo el uso**, la base de datos crecerá hasta que alcance el límite de tamaño especificado.

5.  Haga clic en **aplicar** o **Aceptar**.

**Para deshabilitar los informes de uso**

1.  Haga clic en el nodo **directivas de proveedor** .

2.  Haga clic con el botón secundario en **Directiva de proveedor** y seleccione **propiedades**.

3.  Seleccione la ficha **canalización del proveedor** .

4.  Desactive la casilla **registrar información de uso** .

5.  Haga clic en **aplicar** o **Aceptar**.

## Temas relacionados


[Cómo personalizar un sistema de virtualización de aplicaciones en la consola de administración de servidor](how-to-customize-an-application-virtualization-system-in-the-server-management-console.md)

[Cómo configurar o deshabilitar el tamaño de la base de datos](how-to-set-up-or-disable-database-size.md)

 

 





