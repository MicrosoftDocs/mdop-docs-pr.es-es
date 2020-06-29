---
title: Implementación de la infraestructura de servidor de MBAM 1.0
description: Implementación de la infraestructura de servidor de MBAM 1.0
author: dansimp
ms.assetid: 90529379-b70e-4c92-b188-3d7aaf1844af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: de136db557233a097d95f47ef0a1bba5996798c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825180"
---
# Implementación de la infraestructura de servidor de MBAM 1.0


Puede instalar las características de servidor de administración y supervisión de Microsoft BitLocker en diferentes configuraciones usando de uno a cinco servidores. Por lo general, debe usar una configuración de tres a cinco servidores para entornos de producción, en función de sus necesidades de escalabilidad. Para obtener más información sobre la escalabilidad de rendimiento de MBAM y las topologías de implementación recomendadas, consulte las notas del [producto MBAM la escalabilidad y la guía de alta disponibilidad](https://go.microsoft.com/fwlink/p/?LinkId=258314).

## Implementar todas las MBAM 1,0 en un solo servidor


En esta configuración, todas las características de MBAM se instalan en un solo servidor. Esta topología de implementación de la infraestructura de servidor de MBAM admitirá hasta 21.000 equipos cliente de MBAM.

**Importante**  Esta configuración es compatible, pero se recomienda solo para pruebas.

 

Los procedimientos de esta sección describen la instalación completa de las características de MBAM en un solo servidor.

[Cómo instalar y configurar MBAM en un único servidor](how-to-install-and-configure-mbam-on-a-single-server-mbam-1.md)

## Implementar MBAM 1,0 en servidores distribuidos


Las características de MBAM se pueden instalar en diferentes configuraciones, en función de sus necesidades de escalabilidad. Para obtener más información sobre cómo planear la implementación de las características de MBAM Server, consulte [Planning for MBAM 1,0 Server Deployment](planning-for-mbam-10-server-deployment.md).

Los procedimientos de esta sección describen la instalación completa de las características de MBAM en los servidores distribuidos.

### Configuración de tres equipos

En el siguiente diagrama se muestra la topología de implementación de tres equipos para MBAM. Recomendamos esta topología para entornos de producción que admiten hasta 55.000 clientes MBAM.

![Mbam topología de implementación de tres equipos](images/mbam-3-server.jpg)

En esta configuración, las características de MBAM se instalan en la siguiente configuración:

1.  La base de datos de hardware y de recuperación, la base de datos de auditoría y cumplimiento, y los informes de auditoría y cumplimiento se instalan en un servidor.

2.  La característica servidor de administración y supervisión se instala en un servidor.

3.  MBAM plantilla de directiva de grupo se instala en un equipo que es capaz de modificar objetos de directiva de grupo (GPO).

### Configuración de cuatro equipos

En el siguiente diagrama se muestra la topología de implementación de cuatro equipos para MBAM. Recomendamos esta topología para entornos de producción que admiten hasta 110.000 clientes MBAM.

![Mbam topología de implementación de cuatro equipos.](images/mbam-4-computer.jpg)

En esta configuración, las características de MBAM se instalan en la siguiente configuración:

1.  La base de datos de hardware y de recuperación, la base de datos de auditoría y cumplimiento, y los informes de auditoría y cumplimiento se instalan en un servidor.

2.  La característica servidor de administración y supervisión se instala en un servidor configurado en un clúster de servidor de equilibrio de carga de red (NLB).

3.  MBAM plantilla de directiva de grupo se instala en un equipo que es capaz de modificar los objetos de directiva de grupo.

### Configuración de cinco equipos

En el siguiente diagrama se muestra la topología de implementación de cinco equipos para MBAM. Recomendamos esta topología para entornos de producción que admiten hasta 135.000 clientes MBAM.

![Mbam topología de implementación de cinco equipos.](images/mbam-5-computer.jpg)

En esta configuración, las características de MBAM se instalan en la siguiente configuración:

1.  La base de datos de recuperación y hardware se instala en un servidor.

2.  La base de datos de cumplimiento y auditoría y los informes de cumplimiento y cumplimiento se instalan en un servidor.

3.  La característica servidor de administración y supervisión se instala en un servidor configurado en un clúster de servidor de equilibrio de carga de red (NLB).

4.  MBAM plantilla de directiva de grupo se instala en un equipo que es capaz de modificar objetos de directiva de grupo.

[Cómo instalar y configurar MBAM en servidores distribuidos](how-to-install-and-configure-mbam-on-distributed-servers-mbam-1.md)

[Cómo configurar el equilibrio de carga de red para MBAM](how-to-configure-network-load-balancing-for-mbam.md)

## Otros recursos para la implementación de características de servidor de MBAM 1,0


[Implementación de MBAM 1.0](deploying-mbam-10.md)

 

 





