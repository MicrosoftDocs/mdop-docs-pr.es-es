---
title: Cómo asignar las credenciales correctas para Windows XP
description: Cómo asignar las credenciales correctas para Windows XP
author: dansimp
ms.assetid: cddbd556-d8f9-4981-a947-6e8e3f552b70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81581b75a9b7d5ce35e1c50fd01e0b7bbd3f7ef5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819321"
---
# Cómo asignar las credenciales correctas para Windows XP


Use el siguiente procedimiento para configurar el cliente de escritorio de App-V para obtener las credenciales de WindowsXP apropiadas.

**Nota:**  Después de finalizar este procedimiento, el cliente que no está unido a un dominio puede realizar una actualización de publicación sin unirse a un dominio.

 

**Para asignar las credenciales correctas para los clientes de App-V que ejecutan WindowsXP**

1.  Con privilegios de administrador en el cliente de App-V que ejecuta WindowsXP, abra el panel de control de **cuentas de usuario** (panel de control clásico).

2.  Haga clic en la **pestaña Opciones avanzadas**y seleccione **Administrar contraseñas**.

3.  En la pantalla **nombres de usuarios y contraseñas almacenados** , haga clic en **Agregar**.

4.  En la pantalla **propiedades de información de inicio de sesión** , rellene los siguientes campos con información de la infraestructura de App-V:

    1.  **Server:** Nombre del nombre externo del servidor de publicación.

    2.  **Nombre de usuario:** Nombre de usuario para usuario externo en el formulario Domain\\username.

    3.  **Contraseña:** Contraseña de la cuenta de usuario especificada en el campo **nombre de usuario** .

5.  Haga clic en **Aceptar**. Las credenciales se almacenarán en el cliente.

## Temas relacionados


[Clientes unidos a un dominio y no unidos a un dominio](domain-joined-and-non-domain-joined-clients.md)

[Cómo asignar las credenciales correctas para Windows Vista](how-to-assign--the-proper-credentials-for-windows-vista.md)

 

 





