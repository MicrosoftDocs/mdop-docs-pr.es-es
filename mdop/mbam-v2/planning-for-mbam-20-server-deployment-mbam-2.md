---
title: Planeación para la implementación de servidores de MBAM 2.0
description: Planeación para la implementación de servidores de MBAM 2.0
author: dansimp
ms.assetid: b57f1a42-134f-4997-8697-7fbed08e2fc4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 57e6510556522dce029c958172bd89a361e06b83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812614"
---
# Planeación para la implementación de servidores de MBAM 2.0


La infraestructura de servidor de administración y supervisión de Microsoft BitLocker depende de un conjunto de características de servidor que se pueden instalar en uno o más equipos servidor, según los requisitos de la empresa. Si va a instalar administración y supervisión de Microsoft BitLocker con la topología del administrador de configuración, consulte [planificación para implementar MBAM con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

**Nota:**  Las instalaciones de administración y supervisión de Microsoft BitLocker en un solo servidor se recomiendan solo para entornos de prueba.

 

## Planificación de la implementación de MBAM Server


La infraestructura de una implementación de servidor de MBAM incluye las características siguientes:

-   Base de datos de recuperación

-   Base de datos de cumplimiento y auditoría

-   Informes de cumplimiento y cumplimiento

-   Portal de autoservicio

-   Servidor de administración y supervisión

-   MBAM plantilla de directiva de grupo

Las bases de datos y características de MBAM Server se pueden instalar en diferentes configuraciones, en función de los requisitos de escalabilidad. Todas las características de MBAM Server se pueden instalar en un único servidor o se pueden distribuir en varios servidores. Le recomendamos que use una configuración de dos servidores para entornos de producción, aunque también se pueden usar configuraciones de dos a cuatro servidores, en función de sus requisitos informáticos.

Cada característica de MBAM tiene requisitos previos específicos. Para obtener una lista completa de los requisitos previos de las características de servidor y los requisitos de hardware y software, consulte [MBAM 2,0 Deployment Prerequisites](mbam-20-deployment-prerequisites-mbam-2.md) y [MBAM 2,0 Supported](mbam-20-supported-configurations-mbam-2.md).

Además de las características de MBAM relacionadas con el servidor, la aplicación de configuración del servidor incluye una plantilla de directiva de grupo MBAM. La plantilla contiene la configuración del objeto de directiva de grupo (GPO) que se configura para administrar el cifrado de unidad BitLocker en la empresa. Puede instalar esta plantilla en cualquier equipo que pueda ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).

Mientras planea la implementación del servidor de MBAM, tenga en cuenta que las claves de recuperación de BitLocker de MBAM están pensadas solo para uso único, después de las que vencen las claves de recuperación. Para que las claves expiren después de su uso, deben recuperarse a través del portal del servicio de asistencia o del portal de autoservicio.

## Orden de implementación de las características de MBAM Server


Para implementar características de MBAM en varios servidores, tiene que instalar las características en el siguiente orden:

1.  Base de datos de recuperación

2.  Base de datos de cumplimiento y auditoría

3.  Auditoría y informes de cumplimiento

4.  Portal de autoservicio

5.  Servidor de administración y supervisión

6.  MBAM plantilla de directiva de grupo

**Nota:**  Realice un seguimiento de los nombres de los equipos en los que instala cada característica. Debe usar esta información durante el proceso de instalación. Puede imprimir y usar una lista de comprobación de la implementación para ayudarle en este esfuerzo. Para obtener más información sobre la MBAM de la implementación de la implementación, consulte [MBAM 2,0 lista de comprobación de implementación](mbam-20-deployment-checklist-mbam-2.md).

 

## Temas relacionados


[Planificación de la implementación de MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Implementación de la infraestructura de servidor de MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)

 

 





