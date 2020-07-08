---
title: Cómo modificar la configuración de cliente mediante el uso de PowerShell
description: Cómo modificar la configuración de cliente mediante el uso de PowerShell
author: dansimp
ms.assetid: 53ccb2cf-ef81-4310-a853-efcb395f006e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5d3173944abfe2c2b3d30aa9654dae81f204a32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813830"
---
# Cómo modificar la configuración de cliente mediante el uso de PowerShell


Use el siguiente procedimiento para configurar la configuración del cliente de App-V 5,0.

**Para modificar la configuración de cliente de App-V 5,0 con PowerShell**

1.  Para configurar las opciones de cliente con PowerShell, use el cmdlet **set-AppvClientConfiguration** .

2.  Para modificar la configuración del cliente, abra un símbolo del sistema de PowerShell y ejecute el cmdlet **set-AppvClientConfiguration** con los parámetros obligatorios. Por ejemplo:

    `$config = Get-AppvClientConfiguration`

    `Set-AppvClientConfiguration $config`

    `Set-AppvClientConfiguration –AutoLoad 2`

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.0](operations-for-app-v-50.md)

 

 





