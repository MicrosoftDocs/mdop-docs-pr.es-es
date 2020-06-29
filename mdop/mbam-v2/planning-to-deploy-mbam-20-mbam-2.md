---
title: Planificación de la implementación de MBAM 2.0
description: Planificación de la implementación de MBAM 2.0
author: dansimp
ms.assetid: 2dc05fcd-aed9-4315-aeaf-92aaa9e0e955
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c7f065e52655212261dfe8b6b3f081f697142473
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825631"
---
# Planificación de la implementación de MBAM 2.0


Debe tener en cuenta varias configuraciones de implementación y requisitos previos antes de crear su plan de implementación para administración y supervisión de Microsoft BitLocker (MBAM). Esta sección incluye información que puede ayudarle a recopilar la información necesaria para formular un plan de implementación que se adapte mejor a sus requisitos empresariales. Si va a instalar MBAM con la topología del administrador de configuración, vea [planear la implementación de MBAM con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md) para obtener información de planeación adicional.

## Revisar las configuraciones admitidas de MBAM 2,0


Después de preparar el entorno de equipos para la instalación de características de servidor y cliente de MBAM, asegúrese de revisar las configuraciones admitidas para confirmar que los equipos en los que está instalando MBAM cumplan con los requisitos mínimos de hardware y sistema operativo. Para obtener más información sobre los requisitos previos de implementación de MBAM, consulte [requisitos previos de implementación de MBAM 2,0](mbam-20-deployment-prerequisites-mbam-2.md).

[Configuraciones admitidas de MBAM 2.0](mbam-20-supported-configurations-mbam-2.md)

## Planear la implementación de servidor y cliente de MBAM 2,0


La infraestructura de servidor de MBAM depende de un conjunto de características de servidor que se pueden instalar en uno o más equipos servidor, en función de los requisitos de la empresa. Estas características se pueden instalar en una configuración distribuida en varios servidores.

**Nota:**  Solo se recomienda una instalación de MBAM en un único servidor para entornos de laboratorio.

 

El cliente de MBAM permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa. El cliente de BitLocker se puede integrar en una organización implementando el cliente a través de un sistema de entrega de software empresarial o instalando el agente cliente en equipos cliente como parte del proceso de creación de imágenes inicial.

Con MBAM, puede cifrar un equipo de su organización antes de que el usuario reciba el equipo, o posteriormente mediante una directiva de grupo.

[Planeación para la implementación de servidores de MBAM 2.0](planning-for-mbam-20-server-deployment-mbam-2.md)

[Planeación para la implementación de clientes de MBAM 2.0](planning-for-mbam-20-client-deployment-mbam-2.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>Otros recursos para la planeación de MBAM


[Planificación para MBAM 2.0](planning-for-mbam-20-mbam-2.md)

 

 





