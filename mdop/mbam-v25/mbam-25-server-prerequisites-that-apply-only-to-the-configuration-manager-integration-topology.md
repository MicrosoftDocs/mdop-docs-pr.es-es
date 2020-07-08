---
title: Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración
description: Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración
author: dansimp
ms.assetid: 74180d8d-7b0f-460f-b301-53595cde8381
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd9b89e1a1383997d6ebc92f8e034fbf2945823f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812566"
---
# Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración


Si va a instalar la administración y supervisión de Microsoft BitLocker (MBAM) 2,5 mediante la característica de integración de System Center Configuration Manager, debe completar los requisitos previos que se describen en este tema, además de los de [MBAM 2,5 Server Prerequisites para las topologías de integración independiente y de configuración](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md). También debe crear o modificar archivos. mof necesarios para la topología de integración del administrador de configuración.

## Requisitos previos de la función de integración de Administrador de configuración


Si está configurando MBAM con la topología de integración de System Center Configuration Manager, debe completar los requisitos previos adicionales que se requieren para Configuration Manager.

[Requisitos previos de la función de integración de Administrador de configuración](prerequisites-for-the-configuration-manager-integration-feature.md)

## Editar el archivo Configuration. mof


Para permitir que los equipos cliente informen detalles de compatibilidad con BitLocker a través de los informes de MBAM Configuration Manager, tiene que editar el archivo Configuration. mof para SystemCenter2012 ConfigurationManager y Microsoft System Center Configuration Manager 2007.

[Editar el archivo Configuration.mof](edit-the-configurationmof-file-mbam-25.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Crear o editar el archivo SMS \ _def. mof


Para permitir que los equipos cliente informen de los detalles de cumplimiento de BitLocker en los informes de MBAM Configuration Manager, tiene que crear o editar el archivo SMS \ _def. mof. Si está usando SystemCenter2012 ConfigurationManager, debe crear el archivo. En el administrador de configuración 2007, el archivo ya existe, por lo que tendrá que editar, pero no sobrescribir, el archivo existente.

[Crear o editar el archivo SMS \ _def. mof](create-or-edit-the-sms-defmof-file-mbam-25.md)


## Temas relacionados


[Preparación del entorno para MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Configuraciones admitidas de MBAM 2.5](mbam-25-supported-configurations.md)

[Planificación de implementación de MBAM 2.5](planning-to-deploy-mbam-25.md)

 

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




