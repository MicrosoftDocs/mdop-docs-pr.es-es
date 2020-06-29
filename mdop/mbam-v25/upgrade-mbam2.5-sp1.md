---
title: Actualización de MBAM 2,5 a MBAM 2,5 SP1 Service Release Update
author: dansimp
ms.author: ksharma
manager: miaposto
audience: ITPro
ms.topic: article
ms.prod: w10
ms.localizationpriority: Normal
ms.openlocfilehash: 372822e1ec049871c62af9f429290b88bbfac949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812767"
---
# Actualizar de MBAM 2,5 a MBAM 2,5 SP1 Service Release Update

Este artículo proporciona instrucciones paso a paso para actualizar la administración y supervisión de Microsoft BitLocker (MBAM) 2,5 a MBAM 2,5 Service Pack 1 (SP1) junto con [Microsoft Desktop Optimization Pack (MDOP) puede 2019 el mantenimiento](https://support.microsoft.com/help/4505175/may-2019-servicing-release-for-microsoft-desktop-optimization-pack) de la actualización en una configuración independiente.

En esta guía, usaremos una configuración de dos servidores. Un servidor será un servidor de base de datos que ejecuta Microsoft SQL Server 2016. Este servidor hospedará las bases de datos y los informes de MBAM. El otro servidor será un servidor Web de Windows Server 2012 R2. Este servidor hospedará "administración y supervisión" y "portal de autoservicio".

## Prepararse para actualizar MBAM 2,5 SP1

### Conocer los servidores de MBAM en su entorno

1. Motor de base de datos de SQL Server: servidor que hospeda las bases de datos de MBAM.
2. SQL Server Reporting Services: servidor que hospeda los informes de MBAM.
3. Servidores Web de Internet Information Services (IIS): servidor que hospeda las aplicaciones Web de MBAM y los servicios de MBAM.
4. Faculta Servidor de sitio principal de Microsoft System Center Configuration Manager: la aplicación de configuración MBAM se ejecuta en este servidor para integrar los informes de MBAM con Configuration Manager. Estos informes se combinan con los informes de Configuration Manager existentes en la instancia de SQL Server Reporting Services (SSRS) de Configuration Manager.

### Identificar las cuentas de servicio, los grupos, el nombre del servidor y la dirección URL de los informes

1. Identifique la cuenta de servicio del grupo de aplicaciones MBAM que usan los servidores Web de IIS para leer y escribir datos en las bases de datos de MBAM.
2. Identifique los grupos que se usan durante la configuración de características Web de MBAM y la dirección URL del servicio Web de informes.
3. Identifique el nombre y el nombre de la instancia de SQL Server. Vea este vídeo para obtener más información.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ANP1]

4. Identifique la cuenta de SQL Server Reporting Services que se usa para leer los datos de cumplimiento de la base de datos de cumplimiento y auditoría. Vea este vídeo para obtener más información.

    > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALdZ]

## Actualizar la infraestructura de MBAM a la última versión disponible

La instalación o actualización de la infraestructura de servidor de MBAM siempre se realiza en el orden que se indica a continuación:

- Motor de base de datos de SQL Server: bases de datos
- SQL Server Reporting Services: informes
- Servidor Web: aplicaciones Web
- Servidor SCCM: informes integrados de SCCM si corresponde
- Clientes: agente de MBAM o actualización de cliente
- Plantillas de directiva de Grupo: actualizar la Directiva de grupo existente con nuevas plantillas y habilitar la nueva configuración en la Directiva de grupo de MBAM existente

> [!NOTE]
> Le recomendamos que cree una copia de seguridad completa de las bases de datos de MBAM antes de ejecutar las actualizaciones.

### Actualizar MBAM SQL Server

Vea este vídeo para obtener información sobre cómo actualizar MBAM SQL Server:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALew]

### Actualizar el servidor Web de MBAM

Vea este vídeo para obtener información sobre cómo actualizar el servidor Web de MBAM:

   > [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3ALex]

## Más información

Para obtener más información sobre los problemas conocidos de MBAM 2,5 SP1, consulte [notas de la versión de MBAM 2,5 SP1](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/release-notes-for-mbam-25-sp1).
