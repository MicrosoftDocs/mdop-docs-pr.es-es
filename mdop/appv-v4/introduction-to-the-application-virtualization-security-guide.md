---
title: Introducción a la guía de seguridad de Application Virtualization
description: Introducción a la guía de seguridad de Application Virtualization
author: dansimp
ms.assetid: 50e1d220-7a95-45b8-933b-3dadddebe26f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4b41c65c5ad753aa606d47d2eafe4a28e035cc4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816270"
---
# Introducción a la guía de seguridad de Application Virtualization


Esta guía de seguridad de Microsoft Application Virtualization (App-V) proporciona instrucciones para los administradores responsables de configurar las características de seguridad que se han seleccionado para la implementación de App-V.

**Nota:**  En esta documentación no se proporcionan instrucciones para elegir las opciones de seguridad específicas. Esa información se proporciona en las notas del producto de las mejores prácticas de seguridad de App-V disponibles en <https://go.microsoft.com/fwlink/?LinkId=127120> .

 

Como administrador de App-V que usa esta guía, debe estar familiarizado con las siguientes tecnologías relacionadas con la seguridad:

-   Active Directory Domain Services

-   Infraestructura de clave pública (PKI)

-   Seguridad del Protocolo de Internet (IPsec)

-   Directivas de grupo

-   Servicios de Internet Information Server (IIS)

## Componentes de infraestructura de APP-V


Al planificar un entorno de App-V de seguridad mejorado, puede considerar varios modelos de infraestructura diferentes.

**Nota:**  Para obtener más información sobre los modelos de infraestructura de App-V, consulte la siguiente documentación:

-   [Guía de planeación e implementación de App-V](https://go.microsoft.com/fwlink/?LinkId=122063)

-   [Planificación de infraestructura y serie de guías de diseño](https://go.microsoft.com/fwlink/?LinkId=151986)

 

Estos modelos usan algunos de los componentes de App-V, pero posiblemente no todos, representados en la siguiente ilustración.

![diagrama de sucursales de App-v](images/appvbranchoffices.gif)

<a href="" id="application-virtualization--app-v--management-server"></a>Servidor de administración de Application Virtualization (App-V)  
El servidor de administración de App-V transmite el contenido del paquete y publica los accesos directos y las asociaciones de tipo de archivo en el cliente de App-V. El servidor de administración de App-V también es compatible con la actualización activa, la administración de licencias y una base de datos que se puede usar para informes.

<a href="" id="application-virtualization--app-v--streaming-server"></a>Servidor de streaming de Application Virtualization (App-V)  
El servidor de streaming de App-V hospeda los paquetes para la transmisión por secuencias a clientes de App-V en entornos como sucursales, donde el ancho de banda de la conexión con el servidor de administración de App-V es insuficiente para transmitir el contenido del paquete a los clientes. El servidor de transmisión solo contiene funcionalidad de transmisión por secuencias y no le proporciona la consola de administración de App-V ni el servicio Web de administración de App-V.

<a href="" id="application-virtualization--app-v--data-store"></a>Application Virtualization (App-V) almacén de datos  
El almacén de datos de App-V, en la base de datos SQL, conserva la información relacionada con la infraestructura de App-V. La información del almacén de datos de App-V incluye todos los registros de aplicaciones, asignaciones de aplicaciones y qué grupos administran el entorno de virtualización de aplicaciones.

<a href="" id="application-virtualization--app-v--management-service"></a>Servicio de administración de Application Virtualization (App-V)  
El servicio de administración de App-V comunica las solicitudes de lectura y escritura al almacén de datos de la virtualización de aplicaciones. Este componente se puede instalar en el mismo equipo que el servidor de administración de App-V o en un equipo independiente con IIS instalado.

<a href="" id="application-virtualization--app-v--management-console"></a>Consola de administración de Application Virtualization (App-V)  
La consola de administración de App-V es una utilidad de administración de complementos para la administración de servidores de App-V. Este componente se puede instalar en el mismo equipo que el servidor de App-V o en una estación de trabajo independiente que tenga MMC 3.0 y. NET 2.0 instalado.

<a href="" id="application-virtualization--app-v--sequencer"></a>Application Virtualization (App-V) Sequencer  
El secuenciador de App-V supervisa y captura la instalación de las aplicaciones y crea paquetes de aplicaciones virtuales. El resultado del secuenciador consiste en el icono de la aplicación, el archivo OSD que contiene información sobre la definición de la aplicación, un archivo de manifiesto del paquete y un archivo SFT que contiene los archivos de contenido de la aplicación. De manera opcional, se puede crear un archivo de Windows Installer para instalar el paquete sin usar la infraestructura de App-V.

<a href="" id="application-virtualization--app-v--client"></a>Cliente de Application Virtualization (App-V)  
El cliente de App-V está instalado en el equipo cliente de escritorio de App-V o en el equipo cliente de servicios de Terminal Server de App-V. Proporciona el entorno virtual para los paquetes de aplicaciones virtuales. El cliente de App-V administra la transmisión de paquetes a la caché, la actualización de la publicación de aplicaciones virtuales y la interacción con los servidores de virtualización de aplicaciones.

 

 





