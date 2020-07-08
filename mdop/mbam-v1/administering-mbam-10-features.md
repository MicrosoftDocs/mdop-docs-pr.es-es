---
title: Administración de funciones de MBAM 1.0
description: Administración de funciones de MBAM 1.0
author: dansimp
ms.assetid: dd9a9eff-f1ad-4af3-85d9-c19131a4ad22
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a99ac556227c0f113fb20f3aca32d21c204877b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821221"
---
# Administración de funciones de MBAM 1.0


Después de completar toda la planeación y la implementación de Microsoft BitLocker (MBAM), puede configurar y usar MBAM para administrar el cifrado de BitLocker empresarial. En la información de esta sección se describen las tareas posteriores a la instalación de las funciones de la MBAM.

## Administrar los roles de administrador de MBAM


Una vez completada la configuración de MBAM para todas las características del servidor, se debe conceder acceso a los usuarios administrativos a estas características de servidor. Como práctica recomendada, los administradores que administrarán o usarán características de servidor de MBAM se deben asignar a grupos de seguridad de Active Directory y, a continuación, esos grupos deben agregarse al grupo local administrativo de MBAM adecuado.

[Cómo administrar los roles de administrador de MBAM](how-to-manage-mbam-administrator-roles-mbam-1.md)

## Administrar la compatibilidad de hardware


La característica de compatibilidad de hardware de MBAM puede ayudarle a garantizar que solo se cifrará el hardware del equipo que especifique como compatible con BitLocker. Cuando esta característica está activada, bit \ _admmontla cifrará solo los equipos que estén marcados como compatibles.

**Importante**  Cuando esta característica está desactivada, todos los equipos en los que se implemente la Directiva MBAM estarán cifrados.

 

MBAM puede recopilar información sobre la marca y el modelo de equipos cliente si implementa la Directiva de grupo "permitir comprobación de compatibilidad de hardware". Si configura esta Directiva, el agente de MBAM notifica la marca del equipo y la información del modelo al servidor de MBAM cuando se implementa el cliente MBAM en un equipo cliente.

[Cómo administrar la compatibilidad de hardware](how-to-manage-hardware-compatibility-mbam-1.md)

[Cómo administrar exenciones de cifrado de BitLocker de usuario](how-to-manage-user-bitlocker-encryption-exemptions-mbam-1.md)

## Administrar exenciones de cifrado de BitLocker


MBAM puede conceder dos formas de exención del cifrado de BitLocker: exención de equipos y exención de usuarios. La exención de equipo se usa normalmente cuando una empresa tiene equipos que no tienen que cifrarse, como equipos que se usan en el desarrollo o la prueba, o equipos anteriores que no son compatibles con BitLocker. En algunos casos, la legislación local también puede requerir que determinados equipos no estén cifrados. También puede optar por eximir a los usuarios que no necesiten o deseen que sus unidades estén cifradas.

[Cómo administrar exenciones de cifrado de BitLocker de equipo](how-to-manage-computer-bitlocker-encryption-exemptions.md)

## Administrar las opciones de cifrado de BitLocker de MBAM con el panel de control


Si se habilita mediante objetos de directiva de grupo (GPO), un panel de control de MBAM personalizado que se denomine opciones de cifrado de BitLocker estará disponible en **sistema y seguridad**. Este panel de control personalizado reemplaza al panel de control predeterminado de BitLocker de Windows. El panel de control de MBAM te permite desbloquear unidades cifradas (fijas y extraíbles) y también te ayuda a administrar tu PIN o tu contraseña.

[Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-1.md)

## Otros recursos para administrar características de MBAM


[Operaciones para MBAM 1.0](operations-for-mbam-10.md)

 

 





