---
title: Acerca de la virtualización de la experiencia del usuario 1.0
description: Acerca de la virtualización de la experiencia del usuario 1.0
author: dansimp
ms.assetid: 3758b100-35a8-4e10-ac08-f583fb8ddbd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6010f9c4ebc260eec0324fb880dc2c92fd675130
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822711"
---
# Acerca de la virtualización de la experiencia del usuario 1.0


Virtualización de la experiencia del usuario de Microsoft (UE-V) supervisa los cambios realizados por los usuarios en la configuración de la aplicación y en la configuración del sistema operativo Windows. La configuración de usuario se captura y centraliza en una ubicación de almacenamiento de configuración. Esta configuración se puede aplicar a los diferentes equipos a los que el usuario tiene acceso, como equipos de escritorio, equipos portátiles y sesiones de infraestructura de escritorio virtual (VDI).

La virtualización de la experiencia del usuario usa plantillas de ubicación de configuración para especificar las aplicaciones y la configuración de Windows de los equipos de los usuarios que se supervisan y se centralizan. La plantilla de ubicación de configuración es un archivo XML que especifica qué ubicaciones de archivos y registros se asocian con cada configuración de aplicación o sistema operativo. La plantilla no contiene valores para la configuración; contiene solo las ubicaciones de la configuración que se va a supervisar.

UE-V supervisa la configuración de la aplicación y la configuración de Windows cuando los usuarios trabajan en sus equipos. Los valores de la configuración de la aplicación se almacenan en el servidor de almacenamiento de configuración cuando el usuario cierra la aplicación. Los valores de configuración de Windows se almacenan cuando el usuario cierra la sesión, cuando el equipo está bloqueado o cuando se desconecta de forma remota desde un equipo.

Un administrador puede crear una plantilla de ubicación de configuración de UE-V para especificar la configuración de la aplicación empresarial. UE-V incluye un conjunto de plantillas de ubicación de configuración para algunas aplicaciones de Microsoft y la configuración de Windows. Para obtener una lista de las aplicaciones y configuraciones predeterminadas en UE-V, consulte [planear las aplicaciones que se van a sincronizar con UE-v 1,0](planning-which-applications-to-synchronize-with-ue-v-10.md).

## Notas de la versión de UEV 1,0


Para obtener más información y para obtener noticias de última hora que no se han incorporado en la documentación, consulte notas de la [versión 1,0 de Microsoft User Experience Virtualization (UE-V)](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).

## Temas relacionados


[Introducción a la virtualización de la experiencia del usuario 1.0](getting-started-with-user-experience-virtualization-10.md)

[Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0](index.md)

[Arquitectura de alto nivel para UE-V 1.0](high-level-architecture-for-ue-v-10.md)

 

 





