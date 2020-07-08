---
title: Planificación de implementación de MBAM 2.5
description: Planificación de implementación de MBAM 2.5
author: dansimp
ms.assetid: 1343b80c-d87a-42e7-b912-e84ba997d7e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2e955b426b00539aa2a4ef0b7c3a6650b05633a5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826691"
---
# Planificación de implementación de MBAM 2.5


Debe tener en cuenta varias configuraciones de implementación y requisitos previos antes de crear su plan de implementación para administración y supervisión de Microsoft BitLocker (MBAM). Esta sección incluye información que puede ayudarle a recopilar la información necesaria para formular un plan de implementación que se adapte mejor a sus requisitos empresariales.

## Revisar las configuraciones admitidas de MBAM 2,5


Después de preparar el entorno de equipos para la implementación de características de cliente y servidor de MBAM, asegúrese de revisar las configuraciones admitidas para confirmar que los equipos en los que está instalando MBAM cumplan con los requisitos mínimos de hardware y sistema operativo. Para obtener más información sobre los requisitos previos de implementación de MBAM, consulte [requisitos previos de implementación de MBAM 2,5](mbam-25-deployment-prerequisites.md).

[Configuraciones admitidas de MBAM 2.5](mbam-25-supported-configurations.md)

## Planear la implementación de servidor y cliente de MBAM 2,5


La infraestructura de servidor de MBAM depende de un conjunto de características de servidor que se pueden configurar en uno o más equipos servidor, en función de los requisitos de la empresa. Estas características se pueden configurar en una configuración distribuida en varios servidores.

**Nota:**  Solo se recomienda una instalación de MBAM en un único servidor para entornos de laboratorio.

 

El cliente de MBAM permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa. El cliente de BitLocker se puede integrar en una organización implementando el cliente a través de un sistema de entrega de software empresarial o instalando el cliente en equipos cliente como parte del proceso de creación de imágenes inicial.

Con MBAM, puede cifrar un equipo de su organización antes de que el usuario reciba el equipo, o posteriormente mediante una directiva de grupo.

[Planificación para la implementación de servidores de MBAM 2.5](planning-for-mbam-25-server-deployment.md)

[Planificación para la implementación de clientes de MBAM 2.5](planning-for-mbam-25-client-deployment.md)

## <a href="" id="other-resources-for-mbam-planning-"></a>Otros recursos para la planeación de MBAM


[Planificación para MBAM 2.5](planning-for-mbam-25.md)

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

 

 





