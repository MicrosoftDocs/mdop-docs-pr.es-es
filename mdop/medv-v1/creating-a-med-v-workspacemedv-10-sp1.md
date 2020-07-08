---
title: Creación de un área de trabajo de MED-V
description: Creación de un área de trabajo de MED-V
author: dansimp
ms.assetid: 9578bb99-8a09-44c1-b88f-538901f16ad3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 189da6b28515f0d234c8a258138a27be7a7375d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824861"
---
# Creación de un área de trabajo de MED-V


Un área de trabajo de MED-V es el entorno de escritorio en el que los usuarios finales interactúan con la máquina virtual proporcionada por MED-V. El administrador crea y personaliza el área de trabajo de MED-V. Se compone de una imagen y la Directiva, que define las reglas y la funcionalidad del área de trabajo de MED-V. Se pueden crear varias áreas de trabajo de MED-V, cada una personalizada con su propia configuración, configuración y reglas. Se pueden asociar a un usuario, grupo o varios usuarios o grupos a cada área de trabajo de MED-V, por lo que el área de trabajo de MED-V solo está disponible para los equipos del usuario o grupo asociados.

## Cómo agregar un área de trabajo de MED-V


**Para agregar un área de trabajo de MED-V**

1.  Haga clic en el botón Administración de **directivas** para abrir el módulo de **directivas** .

    El módulo de **directivas** consiste en el menú de **áreas de trabajo** a la izquierda y las pestañas **General**, **máquina virtual**, **implementación**, **aplicaciones**, **Web**, **configuración de VM**, **red**y **rendimiento** .

2.  En el menú **Directiva** , seleccione **nuevo área de trabajo**, o haga clic en **Agregar** para crear un nuevo área de trabajo de MED-V.

3.  En la pestaña **General** , en el campo **nombre** , escriba el nombre del área de trabajo de MED-V.

4.  En el campo **Descripción** , escriba una descripción para el área de trabajo de MED-V.

5.  En el campo **información de contacto de soporte** técnico, escriba la información de contacto para soporte técnico.

    Para obtener más información sobre cómo configurar un área de trabajo de MED-V, consulte [configuración de directivas de área de trabajo de Med-v](configuring-med-v-workspace-policies.md).

## Cómo clonar un área de trabajo de MED-V


Un área de trabajo de MED-V se puede clonar para que pueda crear un área de trabajo de MED-V idéntica a un área de trabajo de MED-V existente.

**Para clonar un área de trabajo de MED-V**

1.  Haga clic en el área de trabajo de MED-V para duplicar.

2.  En el menú **Directiva** , seleccione **clonar área de trabajo**.

    Se crea un nuevo área de trabajo de MED-V con el nombre &lt; nombre de área de trabajo original Med-v &gt; .

## Cómo eliminar un área de trabajo de MED-V


**Para eliminar un área de trabajo de MED-V**

-   En el módulo de **directivas** , mientras el panel del área de trabajo está en el foco, haga clic en **quitar**.

## Temas relacionados


[Uso de la interfaz de usuario de la consola de administración de MED-V](using-the-med-v-management-console-user-interface.md)

 

 





