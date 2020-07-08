---
title: Implementación de objetos de directiva de grupo de MBAM 1.0
description: Implementación de objetos de directiva de grupo de MBAM 1.0
author: dansimp
ms.assetid: 2129291e-d2b2-41ed-b643-1e311c49fee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8d14123f1d5b197146e425cba063e8ce4c180641
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821220"
---
# Implementación de objetos de directiva de grupo de MBAM 1.0


Para implementar correctamente administración y supervisión de Microsoft BitLocker (MBAM), primero debe determinar las directivas de grupo que va a usar en la implementación de MBAM. Para obtener más información sobre las diversas directivas disponibles, consulte [requisitos de la Directiva de grupo planificación de MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md). Cuando haya determinado las directivas que va a usar, debe usar la plantilla de directiva de grupo MBAM 1,0 para crear e implementar uno o varios objetos de directiva de grupo (GPO) que incluyan la configuración de directiva de MBAM.

## Instalar la plantilla de directiva de grupo MBAM 1,0


Además de ofrecer características relacionadas con el servidor de MBAM, la aplicación de configuración del servidor incluye una plantilla de directiva de grupo MBAM. Puede instalar esta plantilla en cualquier equipo que pueda ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).

[Instalación de la plantilla de directiva de grupo de MBAM 1.0](how-to-install-the-mbam-10-group-policy-template.md)

## Implementar la configuración de directiva de grupo de MBAM 1,0


Después de crear los GPO necesarios, debe implementar la configuración de la Directiva de grupo MBAM en los equipos cliente de su organización.

[Cambiar la configuración del GPO de MBAM 1.0](how-to-edit-mbam-10-gpo-settings.md)

## Mostrar el panel de control de MBAM en Windows


Como MBAM ofrece un panel de control de MBAM personalizado que puede reemplazar el panel de control predeterminado de BitLocker de Windows, también puede elegir ocultar el panel de control predeterminado de BitLocker de los usuarios finales mediante una directiva de grupo.

[Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md)

## Otros recursos para implementar objetos de directiva de grupo de MBAM 1,0


[Implementación de MBAM 1.0](deploying-mbam-10.md)

 

 





