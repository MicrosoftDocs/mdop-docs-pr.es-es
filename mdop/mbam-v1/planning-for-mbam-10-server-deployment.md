---
title: Planificación para la implementación de servidores de MBAM 1.0
description: Planificación para la implementación de servidores de MBAM 1.0
author: dansimp
ms.assetid: 3cbef284-3092-4c42-9234-2826b18ddef1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 76ff9c444ce3f9c39161341610fb0cd9a763dc6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812430"
---
# Planificación para la implementación de servidores de MBAM 1.0


La infraestructura de servidor de administración y supervisión de Microsoft BitLocker depende de un conjunto de características de servidor que se pueden instalar en uno o más equipos servidor, según los requisitos de la empresa.

## Planificación de la implementación de MBAM Server


Las siguientes características de MBAM representan la infraestructura de servidor para una implementación de servidor de MBAM:

-   Base de datos de recuperación y hardware

-   Base de datos de cumplimiento y auditoría

-   Informes de cumplimiento y cumplimiento

-   Servidor de administración y supervisión

Las bases de datos y las características de MBAM Server se pueden instalar en diferentes configuraciones, en función de sus necesidades de escalabilidad. Todas las características de MBAM Server se pueden instalar en un único servidor o se pueden distribuir en varios servidores. Por lo general, le recomendamos que use una configuración de tres o cinco servidores para entornos de producción, aunque también se pueden usar configuraciones de dos o cuatro servidores, dependiendo de sus necesidades informáticas.

**Nota:**  Para obtener más información sobre la escalabilidad de rendimiento de MBAM y las topologías de implementación recomendadas, consulte las notas del producto de la escalabilidad y de la escalabilidad de la MBAM en <https://go.microsoft.com/fwlink/p/?LinkId=258314> .

 

Cada característica de MBAM tiene requisitos previos específicos. Para obtener una lista completa de los requisitos previos de las características de servidor y los requisitos de hardware y software, consulte [MBAM 1,0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) y [MBAM 1,0 Supported](mbam-10-supported-configurations.md).

Además de las características de MBAM relacionadas con el servidor, la aplicación de configuración del servidor incluye una plantilla de directiva de grupo MBAM. Esta plantilla se puede instalar en cualquier equipo que pueda ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).

## Orden de implementación de las características de MBAM Server


Al implementar las características del servidor de MBAM, instale las características en el siguiente orden:

1.  Base de datos de recuperación y hardware

2.  Base de datos de cumplimiento y auditoría

3.  Auditoría y informes de cumplimiento

4.  Servidor de administración y supervisión

5.  Plantilla de Directiva

**Nota:**  Realice un seguimiento de los nombres de los equipos en los que instala cada característica. Usará esta información durante el proceso de instalación. Puede imprimir y usar una lista de comprobación de la implementación para ayudarle en el proceso de instalación. Para obtener más información sobre la MBAM de la implementación de la implementación, consulte [MBAM 1,0 lista de comprobación de implementación](mbam-10-deployment-checklist.md).

 

## Temas relacionados


[Planificar la implementación de MBAM 1.0](planning-to-deploy-mbam-10.md)

[Implementación de la infraestructura de servidor de MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





