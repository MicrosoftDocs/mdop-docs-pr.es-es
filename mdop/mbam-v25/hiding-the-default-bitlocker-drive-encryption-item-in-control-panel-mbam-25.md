---
title: Ocultación del elemento de Cifrado de unidad BitLocker predeterminado en el Panel de Control
description: Ocultación del elemento de Cifrado de unidad BitLocker predeterminado en el Panel de Control
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823100"
---
# Ocultación del elemento de Cifrado de unidad BitLocker predeterminado en el Panel de Control


En este tema se describe cómo ocultar el elemento del panel de control del **cifrado de unidad BitLocker** , que aparece de forma predeterminada en el panel de control como parte del sistema operativo Windows.

**Nota:**  Administración y supervisión de Microsoft BitLocker (MBAM) crea un elemento de panel de control adicional personalizado, denominado **Opciones de cifrado de BitLocker**, que permite a los usuarios finales administrar su PIN y contraseña, Activar BitLocker para una unidad y comprobar el cifrado.

 

Consulte [comprender las opciones de cifrado de BitLocker y los elementos de cifrado de unidad BitLocker en el panel de control](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) para obtener información sobre:

-   Diferencias entre el MBAM y los elementos predeterminados del panel de control

-   Menú contextual de **Administración de BitLocker** que aparece al hacer clic con el botón secundario en una unidad en el explorador de Windows

**Importante**  No cambie la configuración de directiva de grupo en el nodo **cifrado de unidad BitLocker** . Si lo hace, MBAM no funcionará correctamente. Al establecer la configuración de directiva de grupo en el nodo de **MBAM de MDOP (administración de BitLocker)** , MBAM configura automáticamente la configuración de **cifrado de unidad BitLocker** para usted.

 

**Para ocultar el elemento de cifrado de unidad BitLocker predeterminado en el panel de control**

1.  En la consola de administración de directivas de grupo (GPMC) o en administración avanzada de directivas de grupo, vaya a directivas de **configuración de usuario** en el &gt; **Policies** &gt; Panel de control **plantillas administrativas** &gt; **Control Panel**.

2.  En el panel de **detalles** , haga doble clic en **Ocultar elementos especificados del panel de control**y, a continuación, haga clic en **habilitado**.

3.  Haga clic en **Mostrar**, en **Agregar**y, a continuación, escriba **Microsoft. BitLockerDriveEncryption**.



## Temas relacionados


[Comprender las opciones de cifrado de BitLocker y elementos de Cifrado de unidad BitLocker en el Panel de Control](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[Implementación de objetos de directiva de grupo de MBAM 2.5](deploying-mbam-25-group-policy-objects.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





