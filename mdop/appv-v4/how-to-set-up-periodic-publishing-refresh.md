---
title: Cómo configurar la actualización periódica de publicación
description: Cómo configurar la actualización periódica de publicación
author: dansimp
ms.assetid: c358c765-cb88-4881-b4e7-0a2e87304870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5bbea1c661d6cb5a78f0bb9de29538e0222cda6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816551"
---
# Cómo configurar la actualización periódica de publicación


Puede usar el siguiente procedimiento para configurar que el cliente actualice periódicamente la información de publicación de los servidores de App-V. Una vez configurado el cliente, la operación de actualización es automática. Esta configuración establece la configuración predeterminada del cliente para que todos los usuarios de este equipo vean la misma configuración.

**Nota:**  Una vez que haya realizado este procedimiento, la información de publicación se actualizará de acuerdo con la nueva configuración después de la primera actualización al iniciar sesión. Cuando se produce esta primera actualización, el servidor puede invalidar la configuración del equipo con una configuración diferente, en función de cómo esté configurada. La pestaña **Actualizar** del cuadro de diálogo **propiedades** muestra la configuración del equipo cliente configurada localmente y la configuración que el servidor de publicación podría haber configurado.

 

**Para actualizar periódicamente la información de publicación de los servidores de virtualización de aplicaciones**

1.  En el panel **ámbito** , haga clic en **servidores de publicación** .

2.  En el panel de **resultados** , haga clic con el botón derecho en el servidor deseado y seleccione **propiedades** en el menú emergente.

3.  En el cuadro de diálogo **propiedades** , en la pestaña **Actualizar** , seleccione la casilla de verificación **actualizar la configuración cada** y escriba un número que represente la frecuencia en el campo. A continuación, seleccione **minutos**, **horas**y **días** en el menú desplegable.

    **Nota:**  Esta configuración hará que el cliente actualice la información de publicación cada vez que transcurre el período configurado. Si el usuario no ha iniciado sesión cuando es el momento de realizar una actualización, la actualización se realizará la próxima vez que el usuario inicie sesión. A continuación, el temporizador vuelve a iniciarse para el siguiente período.

     

4.  Haga clic en **aplicar** para cambiar la configuración.

5.  Cuando termine de configurar el servidor, haga clic en **Aceptar** para salir del cuadro de diálogo y volver a la consola de administración del cliente de Application Virtualization.

## Temas relacionados


[Cómo configurar el cliente en la consola de administración del cliente de virtualización de aplicaciones](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





