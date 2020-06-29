---
title: Cómo agregar un servidor
description: Cómo agregar un servidor
author: dansimp
ms.assetid: 1f31678a-8edf-4d35-a812-e4a2abfd979b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d08b79bcbf34910ce357f39635431d11e3e99bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821390"
---
# Cómo agregar un servidor


Para ayudarle a administrar los servidores de administración de virtualización de aplicaciones de forma más eficaz, organícelas en grupos de servidores. Después de crear un grupo de servidores en la consola de administración de Application Virtualization Server, puede usar el siguiente procedimiento para agregar un servidor al grupo.

**Nota:**  Todos los servidores de un grupo de servidores deben estar conectados al mismo almacén de datos.

 

**Para agregar un servidor a un grupo**

1.  Haga clic en el nodo **grupos de servidores** en el panel izquierdo para expandir la lista de grupos de servidores.

2.  Haga clic con el botón secundario en el grupo de servidores que desee y seleccione **nuevo servidor de administración de virtualización de aplicaciones**.

3.  En el **Asistente para nuevo grupo de servidores**, escriba el **nombre para mostrar** y el **nombre de host DNS**.

4.  Deje los valores predeterminados en el campo **asignación de memoria máxima** para la caché del servidor y el campo de **asignación de memoria** de advertencia para especificar el nivel de advertencia de umbral.

5.  Haz clic en **Siguiente**.

6.  En el cuadro de diálogo **modo de seguridad de conexión** , active la casilla **usar seguridad mejorada** para seleccionar el modo de seguridad mejorada, si lo desea. Si es necesario, complete el **Asistente para certificados** o vea los certificados existentes.

7.  Haz clic en **Siguiente**.

8.  En el cuadro de diálogo **configuración de puerto de virt de aplicaciones** , seleccione el botón usar el **puerto predeterminado** o el botón de radio **Puerto personalizado de usuario** y escriba el número de Puerto personalizado.

9.  Haz clic en **Finalizar**.

## Temas relacionados


[Cómo crear un grupo de servidores](how-to-create-a-server-group.md)

[Cómo quitar un servidor](how-to-remove-a-server.md)

 

 





