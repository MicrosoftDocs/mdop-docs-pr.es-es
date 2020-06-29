---
title: Planificar la implementación de MBAM 1.0
description: Planificar la implementación de MBAM 1.0
author: dansimp
ms.assetid: 30ad4304-45c6-427d-8e33-ebe8053c7871
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2ff25e705717db5086150ed08a5640335bbacb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823190"
---
# Planificar la implementación de MBAM 1.0


Debe tener en cuenta varias configuraciones y requisitos previos de implementación diferentes antes de crear el plan de implementación de administración y supervisión de Microsoft BitLocker (MBAM) 1,0. Esta sección incluye información que puede ayudarle a recopilar la información que necesita para formular un plan de implementación que se adapte mejor a sus requisitos empresariales.

## Revisar las configuraciones admitidas de MBAM 1,0


Una vez que haya preparado el entorno de equipos para la instalación de características de cliente y servidor de MBAM, asegúrese de revisar la información de configuración admitida para MBAM para confirmar que los equipos en los que instala MBAM cumplan con los requisitos mínimos de hardware y sistema operativo. Para obtener más información sobre los requisitos previos de implementación de MBAM, consulte [requisitos previos de implementación de MBAM 1,0](mbam-10-deployment-prerequisites.md).

[Configuraciones admitidas de MBAM 1.0](mbam-10-supported-configurations.md)

## Planear la implementación de servidor y cliente de MBAM 1,0


La infraestructura de servidor de MBAM depende de un conjunto de características de servidor que se pueden instalar en uno o más equipos servidor, en función de los requisitos de la empresa. Estas características pueden instalarse en un único servidor o distribuirse entre varios servidores.

El cliente de MBAM permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en los equipos de la empresa. El cliente de BitLocker puede integrarse en una organización implementando el cliente a través de herramientas como Active Directory Domain Services o cifrando directamente los equipos cliente como parte del proceso de creación de imágenes inicial.

Con MBAM, puede cifrar un equipo de su organización antes de que el usuario reciba el equipo o después, mediante una directiva de grupo. Puede usar uno de los métodos o ambos en su organización. Si decide usar ambos métodos, puede mejorar el cumplimiento de las normas, los informes y la compatibilidad de recuperación de claves.

[Planificación para la implementación de servidores de MBAM 1.0](planning-for-mbam-10-server-deployment.md)

[Planificación para la implementación de clientes de MBAM 1.0](planning-for-mbam-10-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>Otros recursos para la planeación de MBAM


-   [Planificación para MBAM 1.0](planning-for-mbam-10.md)

 

 





