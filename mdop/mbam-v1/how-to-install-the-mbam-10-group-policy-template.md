---
title: Instalación de la plantilla de directiva de grupo de MBAM 1.0
description: Instalación de la plantilla de directiva de grupo de MBAM 1.0
author: dansimp
ms.assetid: 451a50b0-939c-47ad-9248-a138deade550
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a055c84fb6b1645592b53d957daf157a6055880
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825340"
---
# Instalación de la plantilla de directiva de grupo de MBAM 1.0


Además de las características relacionadas con el servidor de administración y supervisión de Microsoft BitLocker (MBAM), la aplicación de configuración del servidor incluye una plantilla de directiva de grupo MBAM. Puede instalar esta plantilla en cualquier equipo que sea capaz de ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).

Los pasos siguientes describen cómo instalar la plantilla de directiva de grupo MBAM.

**Nota:**  Asegúrese de usar la configuración de 32 bits en servidores de 32 bits y la configuración de 64 bits en servidores de 64 bits.

 

**Para instalar la plantilla de directiva de grupo MBAM**

1.  Iniciar el Asistente para la instalación de MBAM. después, haga clic en **instalar** en la Página principal.

2.  Lea y acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.

3.  De forma predeterminada, se seleccionan todas las características de MBAM para la instalación. Desactive todas las opciones de característica excepto **plantilla de directiva**y, a continuación, haga clic en **siguiente** para continuar con la instalación.

    **Nota:**  El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan. Si se cumplen todos los requisitos previos, la instalación continúa. Si se detecta un requisito previo que falta, debe resolver el requisito previo que falta y, a continuación, volver a hacer clic en **comprobar requisitos previos**. Una vez cumplidos todos los requisitos previos, la instalación se reanudará.

     

4.  Cuando el Asistente para la instalación de MBAM muestre las páginas de instalación de las características seleccionadas, haga clic en **Finalizar** para cerrar MBAM configuración.

## Temas relacionados


[Implementación de objetos de directiva de grupo de MBAM 1.0](deploying-mbam-10-group-policy-objects.md)

 

 





