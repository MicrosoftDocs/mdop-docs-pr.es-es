---
title: Novedades de UE-V 2.0
description: Novedades de UE-V 2.0
author: dansimp
ms.assetid: 5d852beb-f293-4e3a-a33b-c40df59a7515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a7566bd82432dcf7e4c46e1fa3e66e55d1515b79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824961"
---
# Novedades de UE-V 2.0


Virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0 ofrece estas nuevas características y funciones comparada con UE-V 1,0. Las [notas de la versión de virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md) proporcionan más información sobre la versión de UE-v 2,0.

## La caché del lado cliente (CSC) ya no es necesaria


Esta versión de UE-V presenta el **proveedor de sincronización**, que sustituye al requisito de la característica archivos sin conexión de Windows para admitir una caché de configuración de cliente.

Mientras que UE-V usó para sincronizar la configuración solo cuando una aplicación se abre, se cierra o cuando Windows se bloquea o se desbloquea, o al iniciar o cerrar sesión, el proveedor de sincronización también...

-   Sincroniza la aplicación local y la configuración de Windows fuera de banda con "**desencadenar eventos**"

-   Usa una **tarea programada** para sincronizar el paquete de almacenamiento de configuración en cualquier intervalo que elija para los requisitos de su empresa (cada 30 minutos de forma predeterminada)

Ciertas condiciones proporcionan una sincronización más frecuente.

-   La configuración se sincroniza cuando el usuario hace clic en el botón **sincronizar ahora** en la nueva aplicación centro de configuración de empresa.

-   El proveedor de sincronización también se puede iniciar para una sola aplicación sin esperar a la tarea de sincronización programada. Por ejemplo, cuando se cierra una aplicación, los cambios de configuración se escriben en la memoria caché local y el proceso de proveedor de sincronización se ejecuta de forma asincrónica para mover esos cambios de configuración nuevos a la ubicación de almacenamiento de configuración.

## Sincronización de aplicaciones de Windows


El desarrollador de una aplicación de Windows puede definir qué configuración, si la hay, se va a sincronizar y, ahora, esta configuración se puede capturar y sincronizar con UE-V.

De forma predeterminada, UE-V sincroniza la configuración de muchas de las aplicaciones de Windows incluidas en Windows 8 y Windows 8,1. Puede modificar la lista de aplicaciones sincronizadas con Windows PowerShell, el instrumental de administración de Windows (WMI) o la Directiva de grupo.

**Nota:**  UE-V no sincroniza la configuración de la aplicación de Windows si los usuarios del dominio vinculan sus credenciales de inicio de sesión a su cuenta de Microsoft. Esta vinculación sincroniza la configuración con Microsoft OneDrive, por lo que UE-V solo sincroniza las aplicaciones de escritorio.

 

## Vinculación de la cuenta de Microsoft


La sincronización de configuración a través de OneDrive es una novedad de Windows 8 cuando se inicia sesión con una cuenta de Microsoft o si se vincula la cuenta de Microsoft a su cuenta de dominio. Si un usuario del dominio usa UE-V y ha iniciado sesión en una cuenta de Microsoft, entonces...

-   UE-V solo sincroniza la configuración de las aplicaciones de escritorio

-   La cuenta de Microsoft controla la configuración de la aplicación de Windows y la configuración del escritorio de Windows

## Centro de configuración de empresa


Puede proporcionar a los usuarios algún control sobre las opciones de configuración que se sincronizan a través de una aplicación en UE-V 2 denominada centro de configuración de empresa. El centro de configuración de la empresa se instala junto con el agente de UE-V y los usuarios pueden acceder a él desde el panel de control, el menú **Inicio** o la pantalla de **Inicio** , y desde el icono del área de notificación de UE-V.

Centro de configuración de la empresa muestra qué opciones están sincronizadas y permite a los usuarios ver el estado de sincronización de UE-V. Si lo permite, los usuarios pueden usar el centro de configuración de la compañía para seleccionar qué configuración sincronizar. También puede hacer clic en el botón **sincronizar ahora** para sincronizar toda la configuración inmediatamente.






## Temas relacionados


[Introducción a UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Preparar una implementación de UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

 

 





