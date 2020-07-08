---
title: Configurar la seguridad del correo electrónico para AGPM
description: Configurar la seguridad del correo electrónico para AGPM
author: dansimp
ms.assetid: 4850ed8e-a1c6-43f0-95c5-853aa66a94ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3694662fd0ed81edacd16cf55ac9760b1be2ba97
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818990"
---
# Configurar la seguridad del correo electrónico para AGPM


De forma predeterminada, las notificaciones por correo electrónico enviadas a causa de las acciones de administración avanzada de directivas de grupo (AGPM) no se cifran y se envían a través del puerto SMTP 25. Sin embargo, puede configurar la seguridad del correo electrónico para AGPM mediante la configuración del registro para especificar si se usa el cifrado de capa de sockets seguros (SSL) y el puerto SMTP que se va a usar.

Al cifrar las notificaciones de correo electrónico de AGPM, puede proteger mejor las personas que podrían revelar información confidencial sobre la seguridad de la organización. El cifrado de notificaciones por correo electrónico es recomendable cuando se retransmiten a través de servidores de correo remoto y es posible que se lo exija alguna normativa de cumplimiento.

**PRECAUCIÓN**  La edición incorrecta del registro puede dañar gravemente el sistema. Antes de realizar cambios en el registro, debe hacer una copia de seguridad de los datos valiosos del equipo.

 

Una cuenta de usuario que tenga el rol de administrador (control total) AGPM, la cuenta de usuario del aprobador que creó el objeto de directiva de grupo (GPO) que se usó en estos procedimientos, o una cuenta de usuario que tenga los permisos necesarios en AGPM, se necesita para completar estos procedimientos. Revise los detalles en "consideraciones adicionales" en este tema.

**Para configurar la seguridad del correo electrónico para AGPM con preferencias de directiva de grupo**

1.  En el árbol de **consola de administración de directivas de grupo** , edite un GPO que se aplica a todos los servidores de AGPM para los que desea configurar la seguridad del correo electrónico. (Para obtener más información, consulte [edición de un GPO](editing-a-gpo-agpm30ops.md)).

2.  En la **ventana Editor de administración de directivas de grupo** , expanda la configuración del **equipo**, las **preferencias**, la **configuración de Windows**y las carpetas **del registro** .

3.  En el árbol de consola, haga clic con el botón derecho en **registro**, seleccione **nuevo**, haga clic en **elemento de recopilación**y escriba **seguridad de correo electrónico de AGPM**.

4.  Crear un elemento de preferencias del registro para activar el cifrado:

    1.  En el árbol de consola, haga clic con el botón secundario en **seguridad de correo electrónico de AGPM**, seleccione **nuevo**y, después, haga clic en **elemento de registro**.

    2.  En el cuadro de diálogo **nuevas propiedades del registro** , seleccione la acción de **actualización** .

    3.  Para **subárbol**, seleccione **HKEY \ _LOCAL \ _MACHINE**.

    4.  En **ruta**de la clave, escriba **SOFTWARE\\Microsoft\\AGPM**.

    5.  En **nombre del valor**, escriba **EncryptSmtp**.

    6.  En **tipo de valor**, seleccione **reg \ _DWORD**.

    7.  En **base**, seleccione **decimal**y, para **datos de valor**, escriba **1** para usar el cifrado SSL o **0** para permitir que el correo electrónico se envíe sin cifrar. De forma predeterminada, el correo electrónico se envía sin cifrado.

    8.  Haga clic en **Aceptar**.

5.  Cree un elemento de preferencias del registro para especificar el puerto SMTP:

    1.  En el árbol de consola, haga clic con el botón secundario en **seguridad de correo electrónico de AGPM**, seleccione **nuevo**y, después, haga clic en **elemento de registro**.

    2.  En el cuadro de diálogo **nuevas propiedades del registro** , seleccione la acción de **actualización** .

    3.  Para **subárbol**, seleccione **HKEY \ _LOCAL \ _MACHINE**.

    4.  En el cuadro de diálogo ruta de la **clave** , escriba **SOFTWARE\\Microsoft\\AGPM**.

    5.  En **nombre del valor**, escriba **SmtpPort**.

    6.  En **tipo de valor**, seleccione **reg \ _DWORD**.

    7.  En **base**, seleccione **decimal**y, para **información del valor**, escriba un número de puerto para el puerto SMTP. De forma predeterminada, el puerto SMTP es el puerto 25 si el cifrado no está habilitado o el puerto 587 si el cifrado SSL está habilitado.

    8.  Haga clic en **Aceptar**.

6.  Cierre la ventana del **Editor de administración de directivas de grupo** y, a continuación, proteja e implemente el GPO. Para obtener más información, consulte [implementar un GPO](deploy-a-gpo-agpm30ops.md).

### Consideraciones adicionales

-   Debe poder editar e implementar un GPO para establecer la configuración del registro mediante preferencias de directiva de grupo. Consulte [editar un GPO](editing-a-gpo-agpm30ops.md) e [implementar un GPO](deploy-a-gpo-agpm30ops.md) para obtener más detalles.

### Referencias adicionales

-   [Configuración de Administración avanzada de directivas de grupo](configuring-advanced-group-policy-management.md)

 

 





