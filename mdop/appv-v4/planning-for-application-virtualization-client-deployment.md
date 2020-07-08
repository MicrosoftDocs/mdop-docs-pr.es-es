---
title: Planificación de implementación de cliente de virtualización de aplicaciones
description: Planificación de implementación de cliente de virtualización de aplicaciones
author: dansimp
ms.assetid: a352f80f-f0f9-4fbf-ac10-24c510b2d6be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c9fc4f29020af83a8606827015947e78761f4d7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815951"
---
# Planificación de implementación de cliente de virtualización de aplicaciones


Una vez que haya decidido cómo va a publicar e implementar paquetes de aplicaciones virtuales en los equipos de los usuarios finales, debe planear la implementación del software de cliente de virtualización de aplicaciones.

El cliente de virtualización de aplicaciones es el componente que realmente ejecuta las aplicaciones virtuales. El cliente de virtualización de aplicaciones permite a los usuarios interactuar con iconos y hacer doble clic en los tipos de archivo para iniciar una aplicación virtual. También controla el streaming del contenido de la aplicación desde un servidor de streaming y lo almacena en caché antes de iniciar la aplicación. El contenido de la aplicación está estructurado de forma que todo el contenido necesario para iniciar la aplicación y controlar la interacción inicial del usuario se transmite primero al equipo del usuario final. Existen dos tipos diferentes de software de cliente de virtualización de aplicaciones: el cliente de virtualización de aplicaciones para servicios de escritorio remoto (anteriormente servicios de Terminal Server), que se usa en sistemas de servidor de host de sesión de escritorio remoto (host RDSession), y el cliente de escritorio de virtualización de aplicaciones, que se usa para todos los demás equipos.

El cliente de Application Virtualization debe configurarse en el momento de la instalación, ya sea en la consola de administración de Application Virtualization o a través de la línea de comandos del instalador, con una serie de opciones importantes, entre las que se incluyen las siguientes:

-   Ubicaciones de los iconos de todas las aplicaciones.

-   La ubicación del archivo OSD que contiene la información de definición del paquete.

-   Origen de contenido de la aplicación.

-   El protocolo de comunicaciones que se va a usar al recuperar los elementos anteriores.

-   El método de administración de tamaño de caché y tamaño de caché que se va a usar.

Para agilizar la implementación del software de cliente de virtualización de aplicaciones al usar una solución de distribución de software electrónico (ESD), la configuración anterior debe definirse con cuidado. Esto es especialmente importante cuando tiene equipos en diferentes oficinas, donde sus clientes tendrían que estar configurados para usar ubicaciones de origen diferentes.

**Nota**  
-   La ubicación del icono y los valores del archivo OSD son un factor importante que se debe tener en cuenta al elegir el método de publicación, ya sea mediante Windows Installer o SFTMIME. La configuración del origen de contenido de la aplicación se define por la elección del método de transmisión por secuencias.

-   Para asegurarse de que la memoria caché tiene suficiente espacio asignado para todos los paquetes que se pueden implementar, use la configuración de **umbral usar espacio libre en disco** al configurar el cliente para que la caché pueda crecer según sea necesario. Como alternativa, determine de antemano cuánto espacio en disco será necesario para la caché de App-V y, en el momento de la instalación, establezca el tamaño de la caché según corresponda. Para obtener más información sobre la característica de administración de espacios en caché, consulte **Cómo usar la característica de administración de espacio en caché** en la guía de operaciones de Microsoft Application Virtualization (App-V).

-   Durante tanto la publicación como las operaciones de transmisión HTTP (S), los clientes de App-V 4,5 SP1 usan la configuración del servidor proxy que está configurada en Internet Explorer en el equipo del usuario.

Para obtener más información sobre cómo configurar los parámetros de instalación del cliente, consulte [parámetros de la línea de comandos del instalador del cliente de virtualización de aplicaciones](application-virtualization-client-installer-command-line-parameters.md).

 

Por último, debe determinar cómo implementar el software de cliente de escritorio de virtualización de aplicaciones para los clientes de escritorio. Aunque es posible implementar el cliente de escritorio de Application Virtualization manualmente en cada equipo, la mayoría de las organizaciones necesitarán hacerlo a través de un proceso automatizado. Una organización mediana o grande puede tener un sistema de ESD en funcionamiento y es una manera ideal de implementar el cliente. Si no existe ningún sistema ESD, puede usar el método estándar de instalación del software de su organización. Las opciones incluyen Directiva de grupo o varias técnicas de scripting. Según el número y el tamaño de las oficinas que tenga, este proceso de implementación puede ser complejo y es esencial que adopte un enfoque estructurado para asegurarse de que todos los equipos tengan un cliente instalado con la configuración correcta.

## Temas relacionados


[Planificación de la implementación del sistema de virtualización de aplicaciones](planning-for-application-virtualization-system-deployment.md)

[Cómo instalar el cliente mediante el uso de la línea de comandos](how-to-install-the-client-by-using-the-command-line-new.md)

[Cómo publicar una aplicación virtual en el cliente](how-to-publish-a-virtual-application-on-the-client.md)

[Cómo actualizar el cliente de virtualización de aplicaciones](how-to-upgrade-the-application-virtualization-client.md)

[Cómo desinstalar el cliente de App-V](how-to-uninstall-the-app-v-client.md)

 

 





