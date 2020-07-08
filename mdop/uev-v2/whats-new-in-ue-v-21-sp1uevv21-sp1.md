---
title: Novedades de UE-V 2.1 SP1
description: Novedades de UE-V 2.1 SP1
author: dansimp
ms.assetid: 9a40c737-ad9a-4ec1-b42b-31bfabe0f170
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1f4b6210d95795c352a7ef1402b0353c6f52774b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827430"
---
# Novedades de UE-V 2.1 SP1


Virtualización de la experiencia del usuario 2,1 SP1 ofrece estas nuevas características y funcionalidades comparadas con UE-V 2,1. Las [notas de la versión de virtualización de la experiencia del usuario de Microsoft (UE-V) 2,1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md) proporcionan más información sobre la versión de UE-v 2,1 SP1.

## Compatibilidad con Windows 10


UE-V 2,1 SP1 agrega compatibilidad para Windows 10, además del mismo software que se admite en las versiones anteriores de UE-V.

### Compatibilidad con Microsoft Azure

Windows 10 permite a los usuarios empresariales sincronizar la configuración de la aplicación de Windows y del sistema operativo Windows en Azure en lugar de en OneDrive. Puede usar la funcionalidad de sincronización de Windows 10 Enterprise junto con UE-V para equipos locales Unidos a un dominio. Para habilitar la coexistencia entre Windows 10 y UE-V, debe deshabilitar las siguientes plantillas de UE-V con PowerShell en cada cliente o en una directiva de grupo.

En la Directiva de grupo, en el nodo virtualización de la experiencia del usuario de Microsoft, establezca esta configuración de directiva:

-   Habilitar "no sincronizar aplicaciones de Windows"

-   Deshabilitar la configuración de sincronización de Windows

### Comportamiento de sincronización de configuración cambiado para soporte técnico de Windows 10

UE-V 2,1 SP1 rela configuración de la barra de tareas entre dispositivos con Windows 10. Sin embargo, UE-V no sincroniza la configuración de la barra de tareas entre dispositivos con Windows 10 y dispositivos que ejecutan sistemas operativos anteriores.

Además, UE-V 2,1 SP1 no sincroniza la configuración entre la calculadora de Microsoft en Windows 10 y la calculadora de Microsoft en sistemas operativos anteriores.

## Soporte técnico agregado para impresoras de red de itinerancia


UE-V 2,1 SP1 permite que las impresoras de red sean móviles entre dispositivos para que el usuario tenga acceso a sus impresoras de red al iniciar sesión en cualquier dispositivo de la red. Esto incluye la itinerancia de la impresora que establecieron como predeterminada.

La itinerancia de la impresora en UE-V requiere uno de estos escenarios:

-   El servidor de impresión puede descargar el controlador requerido cuando se desplaza a un nuevo dispositivo.

-   El controlador para la impresora de red de itinerancia está preinstalado en cualquier dispositivo que necesite acceder a esa impresora de red.

-   El controlador de impresora se puede obtener en Windows Update.

**Nota:**  La característica de itinerancia de la impresora UE-V **no tiene preferencias** , como la impresión a doble cara.

 

## Plantilla de ubicación de configuración de Office 2013


UE-V 2,1 y 2,1 SP1 incluyen la plantilla de ubicación configuración de Microsoft Office 2013, con compatibilidad de firma de Outlook mejorada. Hemos agregado la sincronización de la configuración de firma predeterminada para mensajes de correo electrónico nuevos, de respuesta y reenviados. Los clientes ya no tienen que elegir la configuración de firma predeterminada.

**Nota:**  Debe crearse un perfil de Outlook para cualquier dispositivo en el que un usuario desee sincronizar su firma de Outlook. Si el perfil aún no se ha creado, el usuario puede crear uno y, a continuación, reiniciar Outlook en ese dispositivo para habilitar la sincronización de firmas.

 

Anteriormente UE-V incluía plantillas de ubicación de configuración de Microsoft Office 2010 que se distribuyeron automáticamente y se registraron en el agente de UE-V. UE-V 2,1 funciona con Office 365 para determinar si la configuración de Office 2013 se ha desplazado con Office 365. Si la configuración se mueve con Office 365, no se desplazará con UE-V. [Información general sobre la configuración de usuario y de itinerancia de Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) proporciona más información.

Para habilitar la sincronización de configuración mediante UE-V 2,1, realice una de las siguientes acciones:

-   Usar una directiva de grupo para deshabilitar la sincronización de Office 365

-   No habilite la experiencia de sincronización de Office 365 durante la instalación de Office 2013

UE-V 2,1 incluye [plantillas de office 2013 y office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings). Esta versión elimina las plantillas de Office 2007. Los usuarios pueden seguir usando las plantillas de Office 2007 de UE-V 2,0 o versiones anteriores y aún así pueden obtener las plantillas de la galería de plantillas de UE-V que se encuentran [aquí](https://go.microsoft.com/fwlink/p/?LinkID=246589).






## Temas relacionados


[Introducción a UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Preparar una implementación de UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

 

 





