---
title: Cómo asignar las credenciales correctas para Windows Vista
description: Cómo asignar las credenciales correctas para Windows Vista
author: dansimp
ms.assetid: cc11d2af-a350-4d16-ba7b-f9c1d89e14b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 111dafea505133f123cf8531a2891a452e725ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821370"
---
# Cómo asignar las credenciales correctas para Windows Vista


Use el siguiente procedimiento para configurar el cliente de escritorio de App-V para obtener las credenciales de vista correctas.

**Nota:**  Este procedimiento debe completarse en todos los equipos que no pertenezcan al dominio. En función del número de equipos que no estén conectados a un dominio en su entorno, podría ser una operación muy tediosa. Puede usar scripts y la interfaz de línea de comandos de Credential Manager para ayudar a los administradores a automatizar este proceso.

 

**Para asignar las credenciales correctas para los clientes de App-V que ejecutan Windows Vista**

1.  Con privilegios de administrador en el cliente de escritorio de App-V que ejecuta Windows Vista, abra el panel de control de **cuentas de usuario** (panel de control clásico).

2.  Seleccione **administrar las contraseñas de red** desde **cuentas de usuario** en el panel tareas de la izquierda.

3.  Seleccione **Agregar** en la pantalla **nombres de usuarios y contraseñas almacenados** .

4.  En la pantalla **propiedades de credenciales almacenadas** , proporcione la información de la infraestructura de App-V:

    1.  **Inicie sesión en:** Nombre externo del servidor de publicación.

    2.  **Nombre de usuario:** Nombre de usuario del usuario externo en el formulario Domain\\Username.

    3.  **Contraseña:** Contraseña de la cuenta de usuario especificada en el campo **nombre de usuario** .

    4.  Deje seleccionado **tipo de credencial** y haga clic en **Aceptar**.

5.  Haz clic en **Cerrar**. Las credenciales se almacenan en el almacén de credenciales para la autenticación correcta en la infraestructura de App-V.

## Temas relacionados


[Clientes unidos a un dominio y no unidos a un dominio](domain-joined-and-non-domain-joined-clients.md)

[Cómo asignar las credenciales correctas para Windows XP](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





