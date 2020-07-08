---
title: Arquitectura de alto nivel de MBAM 2.0
description: Arquitectura de alto nivel de MBAM 2.0
author: dansimp
ms.assetid: 7f73dd3a-0b1f-4af6-a2f0-d0c5bc5d183a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddc061a1aec5141548c2d2141be38f8501d2244d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824701"
---
# Arquitectura de alto nivel de MBAM 2.0


Administración y supervisión de Microsoft BitLocker (MBAM) es una solución cliente/servidor que puede ayudarle a simplificar la implementación y el aprovisionamiento de BitLocker, mejorar el cumplimiento y los informes de BitLocker y reducir los costos de soporte técnico. Administración y supervisión de Microsoft BitLocker incluye las características que se describen en este tema.

La administración y supervisión de Microsoft BitLocker se puede implementar en la topología independiente o en una topología integrada con Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager. En este tema se describe la arquitectura de la topología independiente. Para obtener información sobre la implementación en la topología del administrador de configuración integrado, consulte [uso de MBAM con Configuration Manager](using-mbam-with-configuration-manager.md).

El diagrama siguiente muestra la arquitectura recomendada de MBAM para un entorno de producción, que consta de dos servidores y una estación de trabajo de administración. Esta arquitectura admite hasta 200.000 clientes MBAM. Las características de servidor y las bases de datos de la imagen de arquitectura se describen en la siguiente sección y se enumeran en el equipo o servidor en el que se recomienda instalarlas.

**Nota:**  Una arquitectura de servidor único debe usarse solo en entornos de prueba.

 

![Mbam 2 2-topología de implementación de servidor](images/mbam2-3-servers.gif)

## Servidor de administración y supervisión


Las siguientes características están instaladas en este servidor:

-   **Servidor de administración y supervisión**. La característica servidor de administración y supervisión se instala en un servidor de Windows y consta del sitio web de administración y supervisión, que incluye los informes y el portal del servicio de asistencia y los servicios Web de supervisión.

-   **Portal de autoservicio**. El portal de autoservicio se instala en un servidor de Windows. El portal de autoservicio permite a los usuarios finales de equipos cliente iniciar sesión de forma independiente en un sitio web, donde pueden obtener una clave de recuperación para recuperar un volumen de BitLocker bloqueado.

## Servidor de bases de datos


Las siguientes características están instaladas en este servidor:

-   **Base de datos de recuperación**. La base de datos de recuperación se instala en un servidor Windows y en una instancia compatible de Microsoft SQLServer. Esta base de datos almacena datos de recuperación que se recopilan de MBAM equipos cliente.

-   **Base de datos de cumplimiento y auditoría**. La base de datos de cumplimiento y auditoría está instalada en un servidor de Windows y una instancia compatible de SQLServer. Esta base de datos almacena datos de cumplimiento para equipos cliente de MBAM. Estos datos se usan principalmente para los informes que hospedan los hosts de SQL Server Reporting Services (SSRS).

-   **Informes de auditoría y cumplimiento**. Los informes de cumplimiento y cumplimiento se instalan en un servidor de Windows y en una instancia admitida de SQLServer que tiene instalada la característica SQL Server Reporting Services (SSRS). Estos informes proporcionan informes de MBAM a los que puede obtener acceso desde el sitio web de administración y supervisión o directamente desde el servidor de SSRS.

## Estación de trabajo de administración


La siguiente característica está instalada en la estación de trabajo de administración, que puede ser un servidor de Windows o un equipo cliente.

-   **Plantilla de directiva**. La plantilla de directiva está formada por la configuración de directiva de grupo que define la configuración de implementación de MBAM para cifrado de unidad BitLocker. Puede instalar la plantilla de directiva en cualquier servidor o estación de trabajo, pero normalmente se instala en una estación de trabajo de administración, que es un servidor de Windows o un equipo cliente de Windows compatible. La estación de trabajo no tiene que ser un equipo dedicado.

## <a href="" id="---------mbam-client"></a> Cliente de MBAM


El cliente MBAM está instalado en un equipo con Windows y tiene las siguientes características:

-   Usa la Directiva de grupo para exigir el cifrado de unidad BitLocker de equipos cliente de la empresa.

-   Recopila la clave de recuperación de los tres tipos de unidades de datos de BitLocker: unidades de sistema operativo, unidades de datos fijas y unidades de datos extraíbles (USB).

-   Recopila los datos de cumplimiento del equipo y los pasa al sistema de informes.

## Temas relacionados


[Introducción a MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





