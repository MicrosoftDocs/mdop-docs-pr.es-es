---
title: Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell
description: Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell
author: dansimp
ms.assetid: 78fe0f15-4a36-41e3-96d6-7d5aa77c1e06
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 49beb7ea4afe46c9b0f1640152c786d7c6ba8663
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814439"
---
# Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell


El archivo de configuración de implementación dinámica se aplica cuando se agrega un paquete o se establece en un equipo que ejecuta el cliente de App-V 5,1 antes de que se publique el paquete. El archivo configura la configuración predeterminada de paquete para todos los usuarios del equipo que ejecuta el cliente de App-V 5,1. En esta sección se describen los pasos que se usan para usar un archivo de configuración de implementación. El procedimiento se basa en el siguiente ejemplo y supone que existen los siguientes archivos de configuración y paquete en un equipo:

**c:\\Packages\\Contoso\\MyApp.appv**

**c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**

**Para aplicar el archivo de configuración de implementación con PowerShell**

-   Para especificar un nuevo conjunto predeterminado de configuraciones para todos los usuarios que ejecutarán el paquete en un equipo específico, use la consola de PowerShell y escriba lo siguiente:

    **Add-AppVClientPackage – path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**

    **Nota**  
    Este comando captura el objeto resultante en $pkg. Si el paquete ya está presente en el equipo, el cmdlet **set-AppVclientPackage** se puede usar para aplicar el documento de configuración de implementación:

    **Set-AppVClientPackage-Name MyApp – path c:\\Packages\\Contoso\\MyApp.appv-DynamicDeploymentConfiguration c:\\Packages\\Contoso\\DynamicConfigurations\\deploymentconfig.xml**



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)









