---
title: Configurar notificaciones por correo electrónico
description: Configurar notificaciones por correo electrónico
author: dansimp
ms.assetid: b32ce395-d1b9-4c5b-b765-97cdbf455f9e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0204f2bd3430fa47b785d13a73b107e311990b82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819001"
---
# Configurar notificaciones por correo electrónico


Cuando un editor o un revisor intenta crear, implementar o eliminar un objeto de directiva de grupo (GPO), se envía una solicitud de esta acción a una o más direcciones de correo electrónico para que un aprobador pueda evaluar la solicitud e implementarla o denegarla. Determine la dirección o direcciones de correo electrónico a las que se envían las notificaciones, así como el alias desde el que se envían las notificaciones.

Para completar este procedimiento, debe tener una cuenta de usuario con el rol de administrador de AGPM (control total) o los permisos necesarios en administración avanzada de directivas de grupo (AGPM). Revise los detalles en "consideraciones adicionales" en este tema.

**Para configurar la notificación de correo electrónico para AGPM**

1.  En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.

2.  En el panel de detalles, haga clic en la pestaña **delegación de dominios** .

3.  En el campo **desde dirección de correo electrónico** , escriba el alias de correo electrónico de AGPM desde el que se deben enviar las notificaciones.

4.  En el campo **dirección de correo electrónico** , escriba una lista delimitada por comas de las direcciones de correo electrónico de los aprobadores que deberían recibir solicitudes de aprobación.

5.  En el campo **servidor SMTP** , escriba un servidor de correo SMTP válido.

6.  En los campos **nombre de usuario** y **contraseña** , escriba las credenciales de un usuario con acceso al servicio SMTP.

7.  Haz clic en **Apply**.

### Consideraciones adicionales

-   Para realizar este procedimiento, debe ser administrador de AGPM (control total) de forma predeterminada. En concreto, debe tener los permisos **Mostrar contenido** y **modificar opciones** para el dominio.

-   La notificación por correo electrónico para AGPM es una configuración de nivel de dominio. Puede proporcionar diferentes direcciones de correo electrónico de aprobadores o alias de correo electrónico AGPM en la pestaña de **delegación de dominios** de cada dominio o usar las mismas direcciones de correo electrónico en todo el entorno.

-   De forma predeterminada, los mensajes de correo electrónico enviados como resultado de acciones en administración avanzada de directivas de grupo (AGPM) no están cifradas. Sin embargo, puede configurar la seguridad del correo electrónico para AGPM usando la configuración del registro para especificar si desea usar el cifrado de capa de sockets seguros (SSL) y qué puerto SMTP debe usar. Para obtener más información, consulte [configurar la seguridad del correo electrónico para AGPM](configure-e-mail-security-for-agpm-agpm30ops.md)

### Referencias adicionales

-   [Configuración de Administración avanzada de directivas de grupo](configuring-advanced-group-policy-management.md)

 

 





