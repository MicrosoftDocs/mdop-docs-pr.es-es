---
title: Alta disponibilidad de MBAM 2.0
description: Alta disponibilidad de MBAM 2.0
author: dansimp
ms.assetid: 244ee013-9e2a-48d2-b842-4e10594fd74f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6482a099d96aee731f81368b8b787325e592c453
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824730"
---
# Alta disponibilidad de MBAM 2.0


En este tema se proporciona información básica sobre una instalación de alta disponibilidad de administración y supervisión de Microsoft BitLocker (MBAM). Los escenarios de alta disponibilidad no son totalmente compatibles con esta versión de MBAM, por lo que no se describen aquí. Se recomienda buscar en blogs y foros relacionados, en los que los usuarios describen cómo han configurado correctamente una alta disponibilidad para MBAM en sus entornos.

## Escenarios de alta disponibilidad para MBAM


La administración y supervisión de Microsoft BitLocker está diseñada para ser tolerante a errores. Si un servidor no está disponible, los usuarios no se verán afectados de forma negativa. Por ejemplo, si el agente de MBAM no se puede conectar al servidor Web de MBAM, no se le pedirá que lo solicite.

Cuando planee su instalación de MBAM, tenga en cuenta los siguientes elementos, que pueden afectar a la disponibilidad del servicio MBAM:

-   Cifrado de unidad y contraseña de recuperación: Si no se puede enviar una contraseña de recuperación, el cifrado no se inicia en el equipo cliente.

-   Carga de datos del estado de cumplimiento: Si el servidor que hospeda el servicio informe de estado de cumplimiento no está disponible, los datos de cumplimiento no permanecen actualizados.

-   Acceso a clave de recuperación del servicio de asistencia: Si el servicio de asistencia no puede acceder a la información de la base de datos MBAM, el servicio de asistencia no puede proporcionar claves de recuperación a los usuarios.

-   Disponibilidad de los informes: Si el servidor que hospeda los informes de cumplimiento y cumplimiento no está disponible, los informes no estarán disponibles.

## <a href="" id="how-the-mbam-backup-uses-the-volume-shadow-copy-service--vss--"></a>Cómo usa la copia de seguridad de MBAM el servicio de instantáneas de volumen (VSS)


MBAM 2.0 proporciona un escritor de servicio de instantáneas de volumen (VSS), denominado escritor de administración y administración de Microsoft BitLocker, que facilita la copia de seguridad de la base de datos de cumplimiento y la auditoría y la base de datos de recuperación.

El servidor de MBAM Windows Installer registra el escritor de VSS de MBAM. Cualquier error durante el registro de VSS Writer hace que la instalación de MBAM Server se revierta. En una topología en la que las bases de datos de cumplimiento y comprobación y la base de datos de recuperación están instaladas en diferentes servidores, se registra una instancia independiente de MBAM VSS Writer en cada servidor. El escritor de VSS de MBAM depende de SQL Server VSS Writer. El escritor de VSS de SQL Server se registra como parte de la instalación de Microsoft SQL Server. Cualquier tecnología de copia de seguridad que use escritores de VSS para realizar copias de seguridad puede descubrir el MBAM VSS Writer.

## Temas relacionados


[Mantenimiento de MBAM 2.0](maintaining-mbam-20-mbam-2.md)

 

 





