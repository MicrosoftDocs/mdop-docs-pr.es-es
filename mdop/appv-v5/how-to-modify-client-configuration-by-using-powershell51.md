---
title: Cómo modificar la configuración de cliente mediante el uso de PowerShell
description: Cómo modificar la configuración de cliente mediante el uso de PowerShell
author: dansimp
ms.assetid: c3a59592-bb0d-43b6-8f4e-44f3a2d5b7ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 368a0d12c12e10a623afad3f9040ae01cee6cb38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813814"
---
# Cómo modificar la configuración de cliente mediante el uso de PowerShell


Use el siguiente procedimiento para configurar la configuración del cliente de App-V 5,1.

**Para modificar la configuración de cliente de App-V 5,1 con PowerShell**

1.  Para configurar las opciones de cliente con PowerShell, use el cmdlet **set-AppvClientConfiguration** . Para obtener más información sobre la instalación de PowerShell y una lista de los cmdlets, consulte [Cómo cargar los cmdlets de PowerShell y obtener ayuda sobre el cmdlet](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md).

2.  Para modificar la configuración del cliente, abra un símbolo del sistema de PowerShell y ejecute el cmdlet **set-AppvClientConfiguration** con los parámetros obligatorios. Por ejemplo:

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)

 

 





