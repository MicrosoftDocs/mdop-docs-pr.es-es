---
title: Cómo cambiar el tamaño de la memoria caché de servidor
description: Cómo cambiar el tamaño de la memoria caché de servidor
author: dansimp
ms.assetid: 24e63744-21c3-458e-b137-9592f4fe785c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92e56a8a28f7a00d71805b497f9e404cca65919d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818030"
---
# Cómo cambiar el tamaño de la memoria caché de servidor


Puede usar el siguiente procedimiento para cambiar el tamaño de la caché de cualquier servidor directamente desde la consola de administración de Application Virtualization Server.

**Nota:**  Aunque puede cambiar el tamaño de la caché, a menos que su configuración le exija específicamente que cambie el tamaño, se recomienda que deje el tamaño de la caché configurado en los valores predeterminados.

 

**Para cambiar el tamaño de la caché del servidor**

1.  Haga clic en el nodo **grupos de servidores** en el panel izquierdo para expandir la lista de grupos de servidores.

2.  En el panel de **resultados** , haga doble clic en el grupo de servidores que desee para mostrar la lista de servidores del grupo.

3.  En el panel de **resultados** , haga clic con el botón secundario en el servidor deseado y seleccione **propiedades**.

4.  Seleccione la pestaña **avanzadas** .

5.  Escriba un valor en el campo **asignación de memoria máxima** para la caché del servidor y escriba un valor para el nivel de advertencia de umbral en el campo **asignación de memoria** de advertencia.

6.  Escriba un valor en el campo **tamaño máximo de bloque** . Este número debe ser mayor o igual que el tamaño máximo de bloque del paquete más grande que se transmitirá desde el servidor.

7.  Haz clic en **Aceptar**.

## Temas relacionados


[Cómo cambiar el puerto del servidor](how-to-change-the-server-port.md)

[Cómo administrar servidores en la consola de administración de servidor](how-to-manage-servers-in-the-server-management-console.md)

 

 





