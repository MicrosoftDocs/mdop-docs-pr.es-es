---
title: Instalación de la plantilla de directiva de grupo de MBAM 2.0
description: Instalación de la plantilla de directiva de grupo de MBAM 2.0
author: dansimp
ms.assetid: bc193232-d060-4285-842e-d194a74dd3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6420fc4d499de05ed740b038b40aff6a9cd8a05f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826251"
---
# Instalación de la plantilla de directiva de grupo de MBAM 2.0


Además de las características de administración y supervisión de Microsoft BitLocker relacionadas con el servidor (MBAM), la aplicación de configuración del servidor incluye una plantilla de directiva de grupo supervisión y administración de Microsoft BitLocker. Esta plantilla se puede instalar en cualquier equipo capaz de ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).

Los pasos siguientes describen cómo instalar la plantilla de directiva de grupo MBAM.

**Nota:**  Asegúrese de usar la configuración de 32 bits en servidores de 32 bits y la configuración de 64 bits en servidores de 64 bits.

 

**Para instalar la plantilla de directiva de grupo MBAM**

1.  En el servidor en el que desea instalar MBAM, ejecute **MBAMSetup.exe** para iniciar el Asistente para la instalación de MBAM.

2.  En la página **principal** , seleccione el programa para la mejora de la **experiencia del usuario**y haga clic en **iniciar**.

3.  Lea y acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.

4.  De forma predeterminada, se seleccionan todas las características de supervisión y administración de Microsoft BitLocker para la instalación. Desactive todas las opciones de característica excepto **plantilla de directiva**y, a continuación, haga clic en **siguiente** para continuar con la instalación.

    **Nota:**  El Asistente de instalación comprueba los requisitos previos de la instalación y muestra los requisitos previos que faltan. Si se cumplen todos los requisitos previos, la instalación continúa. Si se detecta un requisito previo que falta, debe resolver los requisitos previos que faltan y, a continuación, vuelva a hacer clic en **comprobar requisitos previos**. Una vez cumplidos todos los requisitos previos, la instalación se reanudará.

     

5.  Para conocer los pasos específicos sobre cómo y dónde instalar las plantillas, consulte [Cómo descargar e implementar plantillas de directiva de grupo de MDOP (. admx)](https://technet.microsoft.com/library/dn659707.aspx).

6.  Después de que el Asistente para la configuración de administración y supervisión de Microsoft BitLocker muestre páginas de instalación para las características seleccionadas, haga clic en **Finalizar** para cerrar la configuración de MBAM.

## Temas relacionados


[Implementación de objetos de directiva de grupo de MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





