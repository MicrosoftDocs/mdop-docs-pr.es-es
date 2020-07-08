---
title: Administración de funciones de MBAM 2.0
description: Administración de funciones de MBAM 2.0
author: dansimp
ms.assetid: 065e0704-069e-4372-9b86-0b57dd7638dd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 35bb855e185ad8e3fa6880853938074cf6185a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823510"
---
# Administración de funciones de MBAM 2.0


Después de completar todo el planeamiento necesario y, a continuación, implementar la administración y supervisión de Microsoft BitLocker (MBAM), puede configurarlo y usarlo para administrar el cifrado de BitLocker en toda la empresa. la información de esta sección describe las tareas de operaciones de supervisión y administración de BitLocker posteriores a la instalación.

## Administrar los roles de administrador de MBAM


Una vez completada la configuración de MBAM para todas las características del servidor, se debe conceder acceso a los usuarios administrativos. Como práctica recomendada, los administradores que administrarán o usarán las características de servidor de MBAM deben asignarse a grupos de seguridad de los servicios de dominio de Active Directory y, a continuación, esos grupos deben agregarse al grupo local administrativo de MBAM adecuado.

[Cómo administrar los roles de administrador de MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md)

## Administrar exenciones de cifrado de BitLocker


MBAM le permite conceder exenciones de cifrado a usuarios específicos que no necesitan o quieren que sus unidades estén cifradas. La exención de equipo se usa normalmente cuando una empresa tiene equipos que no tienen que cifrarse, como equipos que se usan en el desarrollo o la prueba, o equipos anteriores que no son compatibles con BitLocker. En algunos casos, la legislación local también puede requerir que determinados equipos no estén cifrados.

[Cómo administrar exenciones de cifrado de BitLocker de usuario](how-to-manage-user-bitlocker-encryption-exemptions-mbam-2.md)

## Administrar las opciones de cifrado de BitLocker de MBAM con el panel de control


MBAM proporciona un panel de control personalizado, denominado opciones de cifrado de BitLocker, que aparecerá en **sistema y seguridad**. El panel de control de MBAM se puede usar para desbloquear unidades cifradas y extraíbles, y también para administrar su PIN o contraseña.

**Nota:**  Este panel de control personalizado no reemplaza al panel de control predeterminado de BitLocker de Windows.

 

[Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control](how-to-manage-mbam-client-bitlocker-encryption-options-by-using-the-control-panel-mbam-2.md)

## Otros recursos para administrar características de MBAM


[Operaciones para MBAM 2.0](operations-for-mbam-20-mbam-2.md)

 

 





