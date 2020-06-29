---
title: Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell
description: Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell
author: dansimp
ms.assetid: f7d7c595-4fdd-4096-b53d-9eead111c339
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 95ae5840f5eee04a29431716a956ddec7d0487aa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814438"
---
# Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell


El archivo de configuración de usuario dinámico se aplica cuando se publica un paquete para un usuario específico y determina cómo se ejecutará el paquete.

Use el procedimiento siguiente para especificar un archivo de configuración específico del usuario. El siguiente procedimiento se basa en el ejemplo:

**c:\\Packages\\Contoso\\MyApp.appv**

**Para aplicar un archivo de configuración de usuario**

1.  Para agregar el paquete al equipo mediante la consola de PowerShell, escriba el siguiente comando:

    **Add-AppVClientPackage c:\\Packages\\Contoso\\MyApp.appv**

2.  Use el comando siguiente para publicar el paquete para el usuario y especificar el archivo de configuración de usuario dinámico actualizado:

    **Publish-AppVClientPackage $pkg – DynamicUserConfigurationPath c:\\Packages\\Contoso\\config.xml**

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.0](operations-for-app-v-50.md)

 

 





