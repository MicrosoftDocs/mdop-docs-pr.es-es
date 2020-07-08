---
title: Implementación de la actualización de versión de idioma de MBAM 1.0
description: Implementación de la actualización de versión de idioma de MBAM 1.0
author: dansimp
ms.assetid: 9dbd85c3-e470-4752-a90f-25754dd46dab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a819be81594efd9349e3f6c0f6559c2b810bdc9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812823"
---
# Implementación de la actualización de versión de idioma de MBAM 1.0


Administración y supervisión de Microsoft BitLocker (MBAM) 1.0 versión de idioma es una actualización de MBAM e incluye compatibilidad con nuevos idiomas. Los nuevos idiomas son:

-   Inglés (es-es)

-   Francés (fr)

-   Italiano (it)

-   Alemán (de)

-   Español (es)

-   Coreano (KO)

-   Japonés (JA)

-   Portugués brasileño (pt-br)

-   Ruso (RU)

-   Chino tradicional (zh-TW)

-   Chino simplificado (zh-CN)

La actualización del idioma de MBAM 1.0 cambiará el número de versión de MBAM 1.0.1237.1 a MBAM 1.0.2001.

No es necesario volver a instalar todas las características de MBAM para agregar estos idiomas adicionales. Este tema define los pasos necesarios para agregar los nuevos idiomas admitidos.

## Implementar la versión internacional de MBAM en las características de MBAM Server


Para comenzar, debe actualizar las siguientes características del servidor de MBAM:

-   Informe de cumplimiento y cumplimiento

-   Servidor de administración y supervisión

-   Plantillas de Directiva

A continuación, debe ejecutar **MbamSetup.exe** para actualizar las características de MBAM que se ejecutan en el mismo servidor al mismo tiempo.

[Cómo instalar la actualización de lenguaje MBAM en un único servidor](how-to-install-the-mbam-language-update-on-a-single-server-mbam-1.md)

[Cómo instalar la actualización de lenguaje MBAM en servidores distribuidos](how-to-install-the-mbam-language-update-on-distributed-servers-mbam-1.md)

## Instalar la actualización de idioma MBAM para las directivas de grupo


Las plantillas de directiva de grupo MBAM se pueden instalar en cada estación de trabajo de administración o se pueden copiar en el almacén central de directivas de grupo para que las plantillas estén disponibles para todos los administradores de la Directiva de grupo. Las plantillas de Directiva no se pueden instalar directamente en un controlador de dominio. Si no usa una tienda central de directivas de grupo, debe copiar las directivas manualmente en cada controlador de dominio que administre la Directiva de grupo de MBAM.

Para agregar las plantillas de directivas de idioma de MBAM, copie los archivos de idioma de directiva de grupo de%SystemRoot%\\PolicyDefinitions en el equipo donde se instaló la función "plantillas de directiva" en la misma ubicación del equipo de la estación de trabajo. A continuación se muestran algunos ejemplos de archivos de directiva de Grupo:

-   BitLockerManagement. ADMX

-   BitLockerUserManagement. ADMX

-   en-us\\BitLockerManagement.adml

-   en-us\\BitLockerUserManagement.adml

-   fr-fr\\ BitLockerManagement. ADML

-   fr-fr\\ BitLockerUserManagement. ADML

-   (y de forma similar para cada idioma admitido)

## Problemas conocidos de la versión internacional de MBAM


Este tema contiene problemas conocidos de la versión internacional de administración y supervisión de Microsoft BitLocker.

[Problemas conocidos de la versión internacional de MBAM.](known-issues-in-the-mbam-international-release-mbam-1.md)

## Otros recursos para implementar la actualización de idioma MBAM 1,0


[Implementación de MBAM 1.0](deploying-mbam-10.md)

 

 





