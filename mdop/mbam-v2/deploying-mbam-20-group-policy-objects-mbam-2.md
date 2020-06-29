---
title: Implementación de objetos de directiva de grupo de MBAM 2.0
description: Implementación de objetos de directiva de grupo de MBAM 2.0
author: dansimp
ms.assetid: f17f3897-73ab-431b-a6ec-5a6cff9f279a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1ce2c2a37631d9d678d6de7c1d66b7fdafb2ade9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823491"
---
# Implementación de objetos de directiva de grupo de MBAM 2.0


Para implementar correctamente administración y supervisión de Microsoft BitLocker (MBAM), primero tiene que determinar las directivas de grupo que usará en la implementación de administración y supervisión de Microsoft BitLocker. Consulte [planificación de requisitos de la Directiva de grupo de MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) para obtener más información sobre las diferentes directivas disponibles. Cuando haya determinado las directivas que va a usar, deberá crear e implementar uno o varios objetos de directiva de grupo (GPO) que incluyan la configuración de la Directiva para MBAM mediante la plantilla de directiva de grupo MBAM 2,0.

## Instalar la plantilla de directiva de grupo MBAM 2,0


Además de las características de supervisión y administración de Microsoft BitLocker relacionadas con el servidor, la aplicación de configuración del servidor incluye una plantilla de directiva de grupo MBAM. Esta plantilla se puede instalar en cualquier equipo capaz de ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).

[Instalación de la plantilla de directiva de grupo de MBAM 2.0](how-to-install-the-mbam-20-group-policy-template-mbam-2.md)

## Implementar la configuración de directiva de grupo de MBAM 2,0


Después de crear los GPO necesarios, debe implementar la configuración de la Directiva de grupo MBAM en los equipos cliente de su organización.

[Cómo editar la configuración del GPO de MBAM 2.0](how-to-edit-mbam-20-gpo-settings-mbam-2.md)

## Mostrar el panel de control de MBAM en Windows


Como MBAM ofrece un panel de control de MBAM personalizado que puede reemplazar el panel de control predeterminado de BitLocker de Windows, también puede elegir ocultar el panel de control predeterminado de BitLocker de los usuarios finales mediante una directiva de grupo.

[Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md)

## Otros recursos para implementar objetos de directiva de grupo de MBAM 2,0


[Implementación de MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





