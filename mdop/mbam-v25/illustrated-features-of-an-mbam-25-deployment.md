---
title: Funciones mostradas de una implementación MBAM 2.5
description: Funciones mostradas de una implementación MBAM 2.5
author: dansimp
ms.assetid: 7b5eff42-af8c-4bd0-a20a-18cc2e779f01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/15/2018
ms.openlocfilehash: c3b205d4f0b4b18cf8bdbf51982b5a59e5e1b9d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812398"
---
# Funciones mostradas de una implementación MBAM 2.5


En este tema se describen las características individuales que conforman una implementación de administración y supervisión de Microsoft BitLocker (MBAM) 2,5 para las siguientes topologías:

-   MBAM independiente

-   Integración de System Center Configuration Manager

**Importante**  
Estas características no representan la arquitectura recomendada para implementar MBAM. Use esta información solo como guía para comprender las características individuales que componen una implementación de MBAM. Consulte [arquitectura de alto nivel para MBAM 2,5](high-level-architecture-for-mbam-25.md) de la arquitectura recomendada para MBAM.



Para obtener una lista de las versiones compatibles del software mencionadas en este tema, consulte [MBAM 2,5 configuraciones admitidas](mbam-25-supported-configurations.md).

## <a href="" id="bkmk-standalone"></a> MBAM topología independiente


En la siguiente imagen y tabla se explican las características de una topología independiente de MBAM.

![mbab2\-5](images/mbam2-5-standalonecomponents.png)

|Tipo de característica|Descripción|Base de datos|
|-|-|-|
|Base de datos de recuperación|Esta base de datos almacena datos de recuperación que se recopilan de MBAM equipos cliente.|Esta característica está configurada en un servidor que ejecuta Windows Server y una instancia de SQL Server compatible.|
|Base de datos de cumplimiento y auditoría|Esta base de datos almacena los datos de cumplimiento, que se usan principalmente para los informes que hospeda SQL Server Reporting Services.|Esta característica está configurada en un servidor que ejecuta Windows Server y una instancia de SQL Server compatible.|
|Informes de cumplimiento y cumplimiento|||
|Servicio Web de informes|Este servicio web permite la comunicación entre el sitio web de administración y supervisión y la instancia de SQL Server donde se almacenan los datos de informes.|Esta característica está instalada en un servidor que ejecuta Windows Server.|
|Sitio web de informes (sitio web de supervisión y administración)|Los informes se visualizan desde el sitio web de administración y supervisión. Los informes proporcionan auditoría de recuperación y datos del estado de cumplimiento sobre los equipos cliente de su empresa.|Esta característica está configurada en un servidor que ejecuta Windows Server.|
|SQL Server Reporting Services (SSRS)|Los informes se configuran en una instancia de la base de datos SSRS. Los informes se pueden ver directamente desde SSRS o desde el sitio web de supervisión y supervisión.|Esta característica está configurada en un servidor que ejecuta Windows Server y una instancia de SQL Server compatible que ejecuta SSRS.|
|Servidor de autoservicio|||
|Servicio Web de autoservicio|Este servicio web es utilizado por el cliente MBAM y el sitio web de administración y supervisión y el portal de autoservicio para comunicarse con la base de datos de recuperación.|Esta característica se instala en un equipo con Windows Server.|
|Sitio web de autoservicio (portal de autoservicio)|Este sitio web permite a los usuarios finales de equipos cliente iniciar sesión de forma independiente en un sitio web para obtener una clave de recuperación si pierden o olvidan su contraseña de BitLocker.|Esta característica está configurada en un equipo con Windows Server.|
|Servidor de administración y supervisión|||
|Servicio Web de administración y supervisión|El cliente de MBAM y los sitios web usan el servicio Web de supervisión para comunicarse con las bases de datos.|Esta característica se instala en un equipo con Windows Server.|

**Importante**  
El servicio Web de autoservicio ya no está disponible en el SP1 de administración y supervisión de Microsoft BitLocker (MBAM) 2,5, en el que el cliente de MBAM, el sitio web de administración y supervisión, y el portal de autoservicio se comunican directamente con la base de datos de recuperación.

**Importante**  
El servicio Web de supervisión ya no está disponible en Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 ya que el cliente de MBAM y los sitios web se comunican directamente con la base de datos de recuperación.


## <a href="" id="bkmk-cmintegrated"></a>Topología de integración de System Center Configuration Manager

En la siguiente imagen y tabla se explican las características de la topología de integración de System Center Configuration Manager.

![mbam2\-5](images/mbam2-5-cmcomponents.png)

**Importante**  
El servicio Web de autoservicio ya no está disponible en el SP1 de administración y supervisión de Microsoft BitLocker (MBAM) 2,5, en el que el cliente de MBAM, el sitio web de administración y supervisión, y el portal de autoservicio se comunican directamente con la base de datos de recuperación.

**Advertencia**  
El servicio Web de supervisión ya no está disponible en Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1 ya que el cliente de MBAM y los sitios web se comunican directamente con la base de datos de recuperación.


|                        Tipo de característica                        |                                                                                                    Descripción                                                                                                    |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                    Servidor de autoservicio                     |                                                                                                                                                                                                                   |
|                  Servicio Web de autoservicio                  |                                                 Este servicio web es utilizado por el cliente MBAM y el portal de autoservicio para comunicarse con la base de datos de recuperación.                                                  |
|                    Sitio web de autoservicio                    |                          Este sitio web permite a los usuarios finales de equipos cliente iniciar sesión de forma independiente en un sitio web para obtener una clave de recuperación si pierden o olvidan su contraseña de BitLocker.                          |
| Servidor de administración y supervisión informe de auditoría de recuperación |                                                                                                                                                                                                                   |
|         Servicio Web de administración y supervisión          |                               Este servicio web permite la comunicación entre el sitio web de administración y supervisión y las bases de datos de SQL Server donde se almacenan los datos de informes.                               |
|           Sitio web de administración y supervisión            | El informe de auditoría de recuperación se visualiza desde el sitio web de administración y supervisión. Use la consola del administrador de configuración para ver todos los demás informes o ver informes directamente desde SQL Server Reporting Services. |
|                         Bases de datos                          |                                                                                                                                                                                                                   |
|                     Base de datos de recuperación                      |                                                                 Esta base de datos almacena datos de recuperación que se recopilan de MBAM equipos cliente.                                                                  |
|                       Base de datos de auditoría                       |                                                                   Esta base de datos almacena información de auditoría sobre los intentos de recuperación y la actividad.                                                                    |
|               Características de Configuration Manager               |                                                                                                                                                                                                                   |
|          Consola de administración de Configuration Manager          |                                                                   Esta consola está integrada en Configuration Manager y se usa para ver informes.                                                                   |
|               Informes de Configuration Manager                |                                                             Los informes muestran los datos de comprobación de cumplimiento y de recuperación de los equipos cliente de su empresa.                                                              |
|               SQL Server Reporting Services                |                                                SSRS habilita los informes de MBAM. Los informes se pueden ver directamente desde SSRS o desde la consola de Configuration Manager.                                                 |

## Temas relacionados

[Arquitectura de alto nivel de MBAM 2.5](high-level-architecture-for-mbam-25.md)

[Introducción a MBAM 2.5](getting-started-with-mbam-25.md)

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




