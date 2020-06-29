---
title: Alta disponibilidad de MBAM 1.0
description: Alta disponibilidad de MBAM 1.0
author: dansimp
ms.assetid: 5869ecf8-1056-4c32-aecb-838a37e05d39
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1227967d647cbfbc16967b5936066fd73d2412e2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825361"
---
# Alta disponibilidad de MBAM 1.0


En este tema se describe cómo configurar una instalación de alta disponibilidad de administración y supervisión de Microsoft BitLocker (MBAM).

## Escenarios de alta disponibilidad para MBAM


Administración y supervisión de Microsoft BitLocker (MBAM) está diseñada para ser tolerante a errores. Si un servidor no está disponible, los usuarios no se verán afectados de forma negativa. Por ejemplo, si el agente de MBAM no se puede conectar al servidor Web de MBAM, no se le pedirá que lo solicite.

Cuando planee su instalación de MBAM, tenga en cuenta las siguientes preocupaciones que pueden afectar a la disponibilidad del servicio MBAM:

-   Cifrado de unidad y contraseña de recuperación: Si no se puede enviar una contraseña de recuperación, el cifrado no se iniciará en el equipo cliente.

-   Carga de datos del estado de cumplimiento: Si el servidor que hospeda el servicio informe de estado de cumplimiento no está disponible, los datos de cumplimiento no permanecerán actualizados.

-   Acceso a la clave de recuperación del servicio de asistencia: Si el servicio de asistencia no puede tener acceso a la información de la base de datos MBAM, no podrá proporcionar claves de recuperación a los usuarios.

-   Disponibilidad de informes: los informes no estarán disponibles si el servidor que hospeda los informes de cumplimiento y cumplimiento no está disponible.

La principal preocupación de MBAM alta disponibilidad es la disponibilidad de la recuperación de claves de BitLocker. Si el servicio de asistencia no puede proporcionar claves de recuperación, los usuarios que están bloqueados no pueden desbloquear sus equipos. Para evitar este problema, considere la posibilidad de implementar servidores web y bases de datos redundantes para garantizar una alta disponibilidad.

Para obtener más información acerca de la escalabilidad y la alta disponibilidad de MBAM, consulte las notas del producto de la [escalabilidad MBAM](https://go.microsoft.com/fwlink/p/?LinkId=229025) ( https://go.microsoft.com/fwlink/p/?LinkId=229025) .

Para obtener instrucciones generales sobre la alta disponibilidad de Microsoft SQL Server, consulte [High Availability](https://go.microsoft.com/fwlink/p/?LinkId=221504) ( https://go.microsoft.com/fwlink/p/?LinkId=221504) .

Para obtener instrucciones generales sobre la disponibilidad y escalabilidad para servidores Web, consulte [disponibilidad y escalabilidad](https://go.microsoft.com/fwlink/p/?LinkId=221503) ( https://go.microsoft.com/fwlink/p/?LinkId=221503) .

## Temas relacionados


[Mantenimiento de MBAM 1.0](maintaining-mbam-10.md)

 

 





