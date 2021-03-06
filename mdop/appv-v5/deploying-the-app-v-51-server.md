---
title: Implementación del servidor de App-V 5.1
description: Implementación del servidor de App-V 5.1
author: dansimp
ms.assetid: 987b61dc-00d6-49ba-8f1b-92d7b948e702
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bcff2a3211ea3e2f666aff1d6f2ad919509aa3a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814566"
---
# Implementación del servidor de App-V 5.1

Puede instalar las características de servidor de Microsoft Application Virtualization (App-V) 5,1 con diferentes configuraciones de implementación, que se describen en este tema. Antes de instalar las características de servidor, revise la sección servidor de [consideraciones de seguridad de App-V 5,1](app-v-51-security-considerations.md).

Para obtener información sobre cómo implementar el servidor de App-V, consulte [acerca de App-v 5,1](about-app-v-51.md#bkmk-migrate-to-51).

> [!IMPORTANT]
> Antes de instalar y configurar los servidores de App-V 5,1, debe especificar un puerto en el que se hospedará cada componente. También debe agregar las reglas de Firewall asociadas para permitir que las solicitudes entrantes tengan acceso a los puertos especificados. El instalador no modifica la configuración del firewall.

## <a href="" id="---------app-v-5-1-server-overview"></a> Información general de App-V 5,1 Server

El servidor de App-V 5,1 está formado por cinco componentes. Cada componente tiene un propósito diferente dentro del entorno de App-V 5,1. Cada uno de los cinco componentes se describe brevemente aquí:

- Servidor de administración: proporciona funcionalidad de administración general para la infraestructura de App-V 5,1.
- Base de datos de administración: facilita las preimplementaciones de base de datos para la administración de App-V 5,1.
- Publishing Server: proporciona funcionalidad de hospedaje y transmisión por secuencias para aplicaciones virtuales.
- Servidor de informes: proporciona App-V 5,1 Reporting Services.
- Base de datos de informes: facilita las preimplementaciones de base de datos para informes de App-V 5,1.

## <a href="" id="---------app-v-5-1-stand-alone-deployment"></a> Implementación independiente de App-V 5,1

La implementación de App-V 5,1 independiente proporciona una topología adecuada para una implementación pequeña o un entorno de prueba. Al usar este tipo de implementación, todos los componentes de servidor se implementan en un solo equipo. Los servicios y las bases de datos asociadas competirán por los recursos en el equipo que ejecuta los componentes de App-V 5,1. Por lo tanto, no debe usar esta topología para implementaciones más grandes.

[Cómo implementar el servidor de App-V 5.1](how-to-deploy-the-app-v-51-server.md)

[Cómo implementar el servidor de App-V 5.1 mediante un script](how-to-deploy-the-app-v-51-server-using-a-script.md)

## <a href="" id="---------app-v-5-1-server-distributed-deployment"></a> Implementación distribuida de App-V 5,1 Server

La topología de implementación distribuida puede admitir una gran base de aplicaciones de la aplicación-V 5,1 cliente y le permite administrar y escalar el entorno más fácilmente. Al usar este tipo de implementación, los componentes de servidor de App-V 5,1 se implementan en varios equipos, en función de la estructura y los requisitos de la organización.

[Cómo instalar bases de datos de informes y administración en distintos equipos desde los servicios de informes y administración](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)

[Cómo instalar el servidor de administración en un equipo independiente y conectarlo a la base de datos](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)

[Cómo implementar el servidor de App-V 5.1 mediante un script](how-to-deploy-the-app-v-51-server-using-a-script.md)

[Cómo instalar el servidor de publicación en un equipo remoto](how-to-install-the-publishing-server-on-a-remote-computer51.md)

[Cómo instalar el servidor de administración en un equipo independiente y conectarlo a la base de datos](how-to-install-the-management-server-on-a-standalone-computer-and-connect-it-to-the-database51.md)

## Usar una solución de distribución de software para empresas (ESD) y App-V 5,1

También puede implementar los clientes y paquetes de App-V 5,1 con un ESD sin tener que implementar App-V 5,1. Las capacidades completas de integración varían según el ESD que uses.

> [!NOTE]
> El servidor de informes de App-V 5,1 y la base de datos de informes aún pueden implementarse junto con ESD para recopilar los datos de informes de los clientes de App-V 5,1. Sin embargo, los otros tres componentes del servidor no deben implementarse porque entrarán en conflicto con la funcionalidad de ESD.

[Implementación de paquetes de App-V 5.1 mediante la distribución de software electrónica (ESD)](deploying-app-v-51-packages-by-using-electronic-software-distribution--esd-.md)

## <a href="" id="---------app-v-5-1-server-logs"></a> Registros de servidor de App-V 5,1

Puede usar la información de registro de App-V 5,1 Server para ayudarle a solucionar problemas de instalación del servidor y los eventos operativos al usar App-V 5,1. La información de registro relacionada con el servidor puede revisarse con el **visor de eventos**. La siguiente línea muestra la ruta de acceso específica de los eventos relacionados con el servidor:

**Visor de eventos \ \ aplicaciones y servicios registros \ \ Microsoft \ \ aplicación V**

Los registros de configuración asociados se guardan en el siguiente directorio:

**dicha**

En App-V 5,0 SP3, se consolidaron y movieron algunos registros. Consulte [acerca de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).

## <a href="" id="---------app-v-5-1-reporting"></a> Informes de App-V 5,1

Los informes de App-V 5,1 permiten a los clientes de App-V 5,1 recopilar datos y, a continuación, enviarlos de nuevo para que se almacenen en un repositorio central. Puede usar esta información para obtener una mejor vista del uso de aplicaciones virtuales dentro de su organización. En la siguiente lista se muestran algunos de los tipos de información que recopila el cliente de App-V 5,1:

- Información sobre el equipo que ejecuta el cliente de App-V 5,1.
- Información sobre paquetes virtualizados en un equipo específico que ejecuta el cliente de App-V 5,1.
- Información sobre la apertura y el cierre de paquetes para un usuario específico.

La información de los informes se mantendrá hasta que se envíe correctamente a la base de datos del servidor de informes. Una vez que los datos están en la base de datos, puede usar Microsoft SQL Server Reporting Services para generar los informes necesarios.

Si desea recuperar información de un informe, debe usar Microsoft SQL Server Reporting Services (SSRS), que está disponible con Microsoft SQL. SSRS no se instala al instalar el servidor de informes de App-V 5,1 y debe implementarse por separado para generar los informes asociados.

Use el siguiente vínculo para obtener más información [sobre los informes de App-V 5,1](about-app-v-51-reporting.md).

[Cómo habilitar los informes en el cliente de App-V 5.1 mediante PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)

## Otros recursos para el servidor de App-V

[Implementación de App-V 5.1](deploying-app-v-51.md)
