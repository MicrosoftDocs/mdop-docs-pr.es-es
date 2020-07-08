---
title: Mantenimiento de MBAM 1.0
description: Mantenimiento de MBAM 1.0
author: dansimp
ms.assetid: 02ffb093-c364-4837-bbe8-23d4c09fbd3d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7eecef4e82680b08fde1b1bef88487a6fc156fe4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825771"
---
# Mantenimiento de MBAM 1.0


Después de completar todos los planes necesarios y, a continuación, implementar Microsoft BitLocker Administration and Monitoring (MBAM), puede configurar MBAM para que se ejecute de forma muy disponible mientras lo usa para administrar las operaciones de cifrado de BitLocker de la empresa. En la información de esta sección se describen las opciones de alta disponibilidad para MBAM, así como la manera de mover MBAM características de servidor si es necesario.

## Paquete de administración de MBAM


El MicrosoftSystemCenterOperationsManager Management Pack para MBAM está disponible para su descarga desde el centro de descarga de Microsoft.

Este módulo de administración supervisa las interacciones críticas de la infraestructura del servidor, como las conexiones entre las bases de datos y los servicios web y las llamadas operativas entre sitios web y su servicio Web de soporte. También carga las solicitudes entre los clientes de escritorio y sus puntos de conexión de servicio Web de recepción respectivos.

[Módulo de administración de supervisión y administración de Microsoft BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=258390)

## Garantizar la alta disponibilidad de MBAM 1,0


MBAM está diseñado para ser tolerante a errores. Si un servidor no está disponible, los usuarios no se verán afectados de forma negativa. La información de esta sección se puede usar para configurar una instalación MBAM de alta disponibilidad.

[Alta disponibilidad de MBAM 1.0](high-availability-for-mbam-10.md)

## Mover características de MBAM 1,0 a otro servidor


Cuando tenga que mover una característica de MBAM Server de un equipo servidor a otro, existe un orden específico y obligatorios pasos que debe seguir para evitar la pérdida de productividad o datos. En esta sección se describen los pasos que debe seguir para mover una o más características del servidor de MBAM a un equipo diferente.

[Cómo mover funciones de MBAM 1.0 a otro equipo](how-to-move-mbam-10-features-to-another-computer.md)

## Otros recursos para mantener MBAM


[Operaciones para MBAM 1.0](operations-for-mbam-10.md)

 

 





