---
title: Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control
description: Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control
author: dansimp
ms.assetid: e2ff153e-5770-4a12-b79d-cda998b8a8ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a42901ac9d8a1a3527712f4cf342b5c0ca9ffdfd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825110"
---
# Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control


Una aplicación del panel de control administración y supervisión de Microsoft BitLocker (MBAM), que se denomina opciones de cifrado de BitLocker, estará disponible en **sistema y seguridad** cuando esté instalado el cliente de supervisión y administración de Microsoft BitLocker. Este panel de control personalizado de MBAM es un panel de control adicional. No reemplaza el panel de control predeterminado de BitLocker de Windows. El panel de control de MBAM se puede usar para desbloquear unidades cifradas y extraíbles, y también para administrar su PIN o contraseña. Para obtener más información sobre cómo habilitar el panel de control de MBAM, consulta [cómo ocultar el cifrado de BitLocker predeterminado en el panel de control de Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).

**Para usar el panel de control del cliente de MBAM**

1.  Para abrir las opciones de cifrado de BitLocker, haga clic en **Inicio** y seleccione **Panel de control**. Cuando se abra el **Panel de control** , seleccione **sistema y seguridad**.

2.  Haga doble clic en **Opciones de cifrado de BitLocker** para abrir el panel de control MBAM personalizado. Verá una lista de todas las unidades de disco duro del equipo y su estado de cifrado, además de una opción para administrar su PIN o contraseñas.

    La lista de unidades de disco duro se puede usar para comprobar el estado del cifrado, desbloquear una unidad o solicitar una exención para la protección de BitLocker si se han implementado las directivas de exención de usuario y equipo.

    El panel de control de las opciones de cifrado de BitLocker también permite que los usuarios que no sean administradores administren sus PIN o contraseñas. Al seleccionar **administrar PIN**, a los usuarios se les pide que introduzcan un PIN actual y un nuevo PIN (además de confirmar el nuevo PIN). Al seleccionar **Actualizar PIN** se restablecerá el PIN al nuevo que han seleccionado los usuarios.

    Para administrar la contraseña, seleccione **desbloquear unidad** e introduzca la contraseña actual. Tan pronto como se desbloquee la unidad, seleccione **Restablecer contraseña** para cambiar la contraseña actual.

## Temas relacionados


[Administración de funciones de MBAM 2.0](administering-mbam-20-features-mbam-2.md)

 

 





