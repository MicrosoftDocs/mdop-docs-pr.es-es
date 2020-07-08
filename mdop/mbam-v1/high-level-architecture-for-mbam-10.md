---
title: Arquitectura de alto nivel de MBAM 1.0
description: Arquitectura de alto nivel de MBAM 1.0
author: dansimp
ms.assetid: b1349196-88ed-4d6c-8a1d-998f18127b6b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de3529fdb565859fcc212d1a9a614ac4ef4b183e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825240"
---
# Arquitectura de alto nivel de MBAM 1.0


Administración y supervisión de Microsoft BitLocker (MBAM) es una solución de cifrado de datos de cliente/servidor que puede ayudarle a simplificar el aprovisionamiento y la implementación de BitLocker, mejorar el cumplimiento y los informes de BitLocker y reducir los costos de soporte técnico. MBAM incluye las características que se describen en este tema.

Además, hay un vídeo que proporciona una descripción general de la arquitectura de MBAM y la configuración de MBAM. Para obtener más información, consulte [información general sobre la implementación y la arquitectura de MBAM](https://go.microsoft.com/fwlink/p/?LinkId=258392).

## Descripción general de la arquitectura


En el siguiente diagrama se muestra la arquitectura de MBAM. La topología de implementación de MBAM de un único servidor se muestra para presentar las características de MBAM. Sin embargo, esta topología de implementación de MBAM se recomienda solo para entornos de laboratorio.

**Nota:**  Se recomienda al menos una topología de implementación de MBAM de tres equipos para una implementación de producción. Para obtener más información sobre las topologías de implementación de MBAM, consulte [implementación de la infraestructura de servidor de MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).

 

![topología de implementación de servidor único de Mbam](images/mbam-1-server.jpg)

1.  **Servidor de administración y supervisión**. El servidor de supervisión y administración de MBAM está instalado en un servidor de Windows y hospeda el sitio web de administración y administración de MBAM y los servicios Web de supervisión. El sitio web de administración y administración de MBAM se usa para determinar el estado de cumplimiento de la empresa, para auditar la actividad, para administrar la capacidad de hardware y para obtener acceso a datos de recuperación, como las claves de recuperación de BitLocker. El servidor de administración y supervisión se conecta a las siguientes bases de datos y servicios:

    -   Base de datos de recuperación y hardware. La base de datos de recuperación y de hardware se instala en un servidor basado en Windows y en la instancia de SQLServer compatible. Esta base de datos almacena datos de recuperación e información de hardware que se recopilan de MBAM equipos cliente.

    -   Base de datos de cumplimiento y auditoría. La base de datos de cumplimiento y auditoría está instalada en un servidor de Windows y en una instancia de SQLServer compatible. Esta base de datos almacena datos de cumplimiento para equipos cliente de MBAM. Estos datos se usan principalmente para los informes que se hospedan en SQL Server Reporting Services (SSRS).

    -   Informes de auditoría y cumplimiento. Los informes de cumplimiento y cumplimiento se instalan en un servidor basado en Windows y en la instancia de SQLServer compatible que tiene la característica SSRS instalada. Estos informes proporcionan administración de Microsoft BitLocker y los informes de supervisión. Se puede acceder a estos informes desde el sitio web de administración de MBAM y administración o directamente desde el servidor de SSRS.

2.  **Cliente de MBAM**. El cliente de administración y supervisión de Microsoft BitLocker realiza las siguientes tareas:

    -   Usa la Directiva de grupo para exigir el cifrado de BitLocker de los equipos cliente de la empresa.

    -   Recopila la clave de recuperación de los tres tipos de unidades de datos de BitLocker: unidades de sistema operativo, unidades de datos fijas y unidades de datos extraíbles (USB).

    -   Recopila información de recuperación e información de hardware acerca de los equipos cliente.

    -   Recopila los datos de cumplimiento del equipo y los pasa al sistema de informes.

3.  **Plantilla de directiva**. La plantilla de directiva de grupo MBAM se instala en un servidor o equipo cliente de Windows compatible. Esta plantilla se usa para especificar la configuración de implementación de MBAM para el cifrado de unidad BitLocker.

## Temas relacionados


[Introducción a MBAM 1.0](getting-started-with-mbam-10.md)

 

 





