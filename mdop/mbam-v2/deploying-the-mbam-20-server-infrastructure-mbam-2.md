---
title: Implementación de la infraestructura de servidor de MBAM 2.0
description: Implementación de la infraestructura de servidor de MBAM 2.0
author: dansimp
ms.assetid: 52e68d94-e2b4-4b06-ae55-f900ea6cc59f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22a69fe8f6853c02a818bb026b36771cd09632f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824760"
---
# Implementación de la infraestructura de servidor de MBAM 2.0


Las características de servidor de administración y supervisión de Microsoft BitLocker (MBAM) para la topología independiente se pueden instalar en diferentes configuraciones en dos o más servidores en un entorno de producción. La configuración recomendada es de dos servidores para un entorno de producción, en función de los requisitos de escalabilidad. Use un solo servidor para una instalación de MBAM solo en entornos de prueba. Para obtener más información sobre la planeación de la implementación de características de MBAM Server, consulte [Planning for MBAM 2,0 Server Deployment](planning-for-mbam-20-server-deployment-mbam-2.md).

En el siguiente diagrama se muestra un ejemplo de cómo puede configurar la implementación recomendada de dos servidores de MBAM. Esta configuración admite hasta 200.000 clientes MBAM en un entorno de producción. Las características de servidor y las bases de datos de la imagen de arquitectura se describen en la siguiente sección y se enumeran en el equipo o servidor en el que se recomienda instalarlas.

![Mbam 2 2-topología de implementación de servidor](images/mbam2-3-servers.gif)

## Servidor de administración y supervisión


Las siguientes características están instaladas en este servidor:

-   **Servidor de administración y supervisión**. La característica servidor de administración y supervisión se instala en un servidor Windows y consta del sitio web de asistencia y los servicios Web de supervisión.

-   **Portal de autoservicio**. El portal de autoservicio se instala en un servidor de Windows. El portal de autoservicio permite a los usuarios finales de equipos cliente iniciar sesión de forma independiente en un sitio web, donde pueden obtener una clave de recuperación para recuperar un volumen de BitLocker bloqueado.

## Servidor de bases de datos


Las siguientes características están instaladas en este servidor:

-   **Base de datos de recuperación**. La base de datos de recuperación se instala en un servidor Windows y en una instancia compatible de Microsoft SQLServer. Esta base de datos almacena datos de recuperación que se recopilan de MBAM equipos cliente.

-   **Base de datos de cumplimiento y auditoría**. La base de datos de cumplimiento y auditoría está instalada en un servidor de Windows y una instancia compatible de SQLServer. Esta base de datos almacena datos de cumplimiento para equipos cliente de MBAM. Estos datos se usan principalmente para los informes que hospedan los hosts de SQL Server Reporting Services (SSRS).

-   **Informes de auditoría y cumplimiento**. Los informes de cumplimiento y cumplimiento se instalan en un servidor de Windows y en una instancia admitida de SQLServer que tiene instalada la característica SQL Server Reporting Services (SSRS). Estos informes proporcionan informes de MBAM a los que puede obtener acceso desde el sitio web del Departamento de soporte técnico o directamente desde el servidor de SSRS.

## Estación de trabajo de administración


La siguiente característica está instalada en la estación de trabajo de administración, que puede ser un servidor de Windows o un equipo cliente.

-   **Plantilla de directiva**. La plantilla de directiva consta de directivas de grupo que definen la configuración de implementación de MBAM para el cifrado de unidad BitLocker. Puede instalar la plantilla de directiva en cualquier servidor o estación de trabajo, pero normalmente se instala en una estación de trabajo de administración, que es un servidor de Windows o un equipo cliente de Windows compatible. La estación de trabajo no tiene que ser un equipo dedicado.

## <a href="" id="---------mbam-client"></a> Cliente de MBAM


El cliente MBAM está instalado en un equipo con Windows y tiene las siguientes características:

-   Usa la Directiva de grupo para exigir el cifrado de unidad BitLocker de equipos cliente de la empresa.

-   Recopila la clave de recuperación de los tres tipos de unidades de datos de BitLocker: unidades de sistema operativo, unidades de datos fijas y unidades de datos extraíbles (USB).

-   Recopila los datos de cumplimiento del equipo y los pasa al sistema de informes.

## Otros recursos para implementar características de servidor de MBAM 2,0


[Implementación de MBAM 2.0](deploying-mbam-20-mbam-2.md)

 

 





