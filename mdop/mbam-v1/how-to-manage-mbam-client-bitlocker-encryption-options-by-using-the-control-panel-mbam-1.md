---
title: Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control
description: Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control
author: dansimp
ms.assetid: c08077e1-5529-468f-9370-c3b33fc258f3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 271147d0e5581f6ce49fe0b46aa83dae6ae4556b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812958"
---
# Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control


Una aplicación de panel de control de administración y supervisión de Microsoft BitLocker (MBAM), que se denomina opciones de cifrado de BitLocker, estará disponible en **sistema y seguridad** cuando se instale el cliente de MBAM. Este panel de control personalizado de MBAM reemplaza al panel de control predeterminado de BitLocker de Windows. El panel de control de MBAM te permite desbloquear unidades cifradas (fijas y extraíbles) y también te ayuda a administrar tu PIN o tu contraseña. Para obtener más información sobre cómo habilitar el panel de control de MBAM, consulta [cómo ocultar el cifrado de BitLocker predeterminado en el panel de control de Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).

**Nota:**  Para el cliente de BitLocker, los archivos de registro operativos y de administración se encuentran en el visor de eventos, en **registros de aplicaciones y servicios**de  /  **Microsoft**  /  **Windows**  /  **BitLockerManagement**.

 

**Para usar el panel de control del cliente de MBAM**

1.  Para abrir las opciones de cifrado de BitLocker, haga clic en **Inicio**y seleccione **Panel de control**. Cuando se abra el **Panel de control** , seleccione **sistema y seguridad**.

2.  Haga doble clic en **Opciones de cifrado de BitLocker** para abrir el panel de control MBAM personalizado. Verá una lista de todas las unidades de disco duro del equipo y su estado de cifrado. También verá una opción para administrar su PIN o sus contraseñas.

3.  Use la lista de unidades de disco duro del equipo para comprobar el estado de cifrado, desbloquear una unidad o solicitar una exención para la protección de BitLocker si se han implementado las directivas de exención de usuario y equipo.

4.  Los usuarios que no sean administradores pueden usar el panel de control de las opciones de cifrado de BitLocker para administrar PIN o contraseñas. Un usuario puede seleccionar **administrar PIN** y, a continuación, escribir un PIN actual y un nuevo PIN. Los usuarios también pueden confirmar su nuevo PIN. La función **Actualizar PIN** restablecerá el PIN al nuevo que selecciona el usuario.

5.  Para administrar la contraseña, seleccione **desbloquear unidad** e introduzca la contraseña actual. Tan pronto como se desbloquee la unidad, seleccione **Restablecer contraseña** para cambiar la contraseña actual.

## Temas relacionados


[Administración de funciones de MBAM 1.0](administering-mbam-10-features.md)

 

 





