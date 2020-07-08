---
title: Novedades de App-V 5.0 SP1
description: Novedades de App-V 5.0 SP1
author: dansimp
ms.assetid: e97c2dbb-7b40-46a0-8137-9ee4fc2bd071
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2542d0cc5a544d26b3279b24063cf3ef428b9f39
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813215"
---
# Novedades de App-V 5.0 SP1


Esta sección está deshabilitada para usuarios que ya están familiarizados con App-V y desean saber qué ha cambiado en App-V 5,0 SP1. Si aún no está familiarizado con App-V, debe empezar por leer [la planificación de App-v 5,0](planning-for-app-v-50-rc.md).

## Cambios en la funcionalidad estándar


Las secciones siguientes contienen información sobre los cambios en la funcionalidad estándar de App-V 5,0 SP1.

### Cambios en los idiomas admitidos

Para obtener más información, consulte [acerca de App-V 5,0 SP1](about-app-v-50-sp1.md).

La siguiente lista contiene más información sobre los nuevos paquetes de idioma:

-   Los paquetes de idioma de App-V 5.0 SP1 se incluyen en el instalador de **appv\_xxx\_setup.exe** para todos los componentes de App-v 5,0.

-   Al ejecutar el instalador, se instalará automáticamente el paquete de idioma más adecuado en función de la configuración regional del sistema operativo asociado que se ejecute en el equipo de destino.

-   Si se necesitan paquetes de idioma adicionales, debe extraer estos paquetes de idioma desde el instalador ejecutando el siguiente comando: `appv_xxx_setup.exe /Layout /LayoutDir=”<path>”` . Después de que se haya ejecutado, el contenido del instalador se extrae en la ubicación especificada.

-   Debe instalar el paquete de idioma deseado aplicando el paquete de idioma adecuado de instalación de Windows. Por ejemplo, **appv\_hib\_LP\_jmmb\_x86.msi** o **appv\_hib\_LP\_jmmb\_x64.msi**, donde **Hib** hace referencia al componente y **JMMB** hace referencia a la configuración regional.

## Compatibilidad mejorada para Microsoft Office2010


**Kit de secuencias de Microsoft Office 2010 para la virtualización de aplicaciones 5,0** : ayuda a proporcionar a los usuarios una experiencia coherente usando una versión virtualizada de Microsoft Office2010. El **Kit de secuenciación 2010 de Microsoft Office para Application virtualization 5,0** se usa junto con el **Kit de implementación de Microsoft Office 2010 para App-V** y también proporciona el servicio de licencias de Microsoft Office2010 requerido.






## Temas relacionados


[Acerca de App-V 5.0](about-app-v-50.md)

 

 





