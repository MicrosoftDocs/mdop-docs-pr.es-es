---
title: Implementación del secuenciador y del cliente de App-V 5.1
description: Implementación del secuenciador y del cliente de App-V 5.1
author: dansimp
ms.assetid: 74f32794-4c76-436f-a542-f9e95d89063d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 3b78059e5005f563bb99d7e6f4b5fe0af2eae8d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814567"
---
# Implementación del secuenciador y del cliente de App-V 5.1


El secuenciador y el cliente de Microsoft Application Virtualization (App-V) 5,1 permiten a los administradores virtualizar y ejecutar aplicaciones virtualizadas.

## Implementar el cliente


El cliente de App-V 5,1 es el componente que ejecuta una aplicación virtualizada en un equipo de destino. El cliente permite que los usuarios interactúen con iconos y hagan doble clic en los tipos de archivo para que puedan iniciar una aplicación virtualizada. El cliente también puede obtener el contenido virtual de la aplicación desde el servidor de administración.

[Cómo implementar el cliente de App-V](how-to-deploy-the-app-v-client-51gb18030.md)

[Cómo desinstalar el cliente de App-V 5.1](how-to-uninstall-the-app-v-51-client.md)

[Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,1 en el mismo equipo](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)

## Configuración de cliente


El cliente de App-V 5,1 almacena su configuración en el registro. Puede recopilar información útil sobre el cliente si comprende el formato de los datos del registro. También puede configurar muchas acciones de cliente cambiando las entradas del registro.

[Información acerca de la configuración de cliente](about-client-configuration-settings51.md)

## Configurar el cliente mediante la plantilla ADMX y la Directiva de grupo


Puede usar la plantilla Microsoft ADMX para establecer la configuración de cliente para el cliente de App-V 5,1 y el cliente de servicios de escritorio remoto. La plantilla ADMX administra configuraciones de cliente comunes mediante una infraestructura de directivas de grupo existente e incluye la configuración de la configuración de cliente de App-V 5,1.

**Importante**  Puede obtener la plantilla App-V 5,1 ADMX en el centro de descarga de Microsoft.

 

Después de descargar e instalar la plantilla ADMX, realice los siguientes pasos en el equipo que va a usar para administrar la Directiva de grupo. Normalmente es el controlador de dominio.

1.  Guarde el archivo **. ADMX** en el siguiente directorio: **Windows \ \ PolicyDefinitions**

2.  Guarde el archivo **. ADML** en el siguiente directorio: **Windows \ \ PolicyDefinitions \ \ &lt; directorio &gt; de idioma**

Una vez completados los pasos anteriores, puede administrar la configuración del cliente de App-V 5,1 con la consola de **Administración de directivas de grupo** .

El cliente de App-V 5,1 también almacena su configuración en el registro. Puede recopilar información útil sobre el cliente si comprende el formato de los datos del registro. También puede configurar muchas acciones de cliente cambiando las entradas del registro.

[Cómo modificar la configuración del cliente de App-V 5.1 mediante la plantilla ADMX y la directiva de grupo](how-to-modify-app-v-51-client-configuration-using-the-admx-template-and-group-policy.md)

## Implementar el cliente mediante el modo de almacén de contenido compartido


El modo App-V 5,1 de almacenamiento compartido de contenido (SCS) permite que los clientes de SCS App-V 5,1 ejecuten aplicaciones virtualizadas sin guardar ninguno de los datos de paquetes asociados de forma local. Todos los datos de paquetes virtualizados requeridos se transmiten a través de la red; por lo tanto, solamente debe usar el modo SCS en entornos con una conexión rápida. Los servicios de escritorio remoto (RDS) y la versión estándar del cliente de App-V 5,1 son compatibles con el modo SCS.

**Importante**  Si el cliente de App-V 5,1 está configurado para ejecutarse en el modo SCS, la ubicación donde se transfieren los paquetes de App-V 5,1 debe estar disponible; de lo contrario, se producirá un error en el paquete virtualizado. Además, no recomendamos la implementación de aplicaciones virtualizadas en equipos que ejecutan el cliente App-V 5,1 en el modo SCS a través de Internet.

 

Además, SCS no es una ubicación física que contiene paquetes virtualizados. Es un modo que permite que el cliente de App-V 5,1 transmita los datos de los paquetes virtualizados necesarios a través de la red.

El modo SCS es útil en los siguientes escenarios:

-   Implementaciones de infraestructura de escritorio virtual (VDI)

-   Implementaciones de servicios de escritorio remoto (RDS)

Para usar SCS en su entorno, debe habilitar el cliente de App-V 5,1 para que se ejecute en modo SCS. Esta configuración debe especificarse durante la instalación. De forma predeterminada, el cliente no está configurado para usar el modo SCS. Si tiene previsto usar SCS, debe instalar el cliente mediante el procedimiento sugerido. Sin embargo, puede configurar un cliente de App-V 5,1 para que se ejecute en el modo SCS escribiendo el siguiente comando de PowerShell en el equipo que ejecuta el cliente de App-V 5,1:

**Set-AppvClientConfiguration-SharedContentStoreMode 1**

Puede haber casos en los que el administrador cargue previamente algunas aplicaciones virtuales en el equipo que ejecuta el cliente de App-V 5,1 en el modo SCS. Esto se puede llevar a cabo con los comandos de PowerShell para agregar, publicar y montar el paquete. Por ejemplo, si un paquete se carga previamente en todos los equipos, el Administrador podría agregar, publicar y montar el paquete con los comandos de PowerShell. El paquete no se transmitió por la red porque se almacenaría de forma local.

[Cómo instalar el cliente de App-V 5.1 para el modo de almacén de contenido compartido](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)

## Implementar el secuenciador


El secuenciador es una herramienta que se usa para convertir aplicaciones estándar en paquetes virtuales para su implementación en equipos que ejecutan el cliente de App-V 5,1. El secuenciador ofrece un proceso de conversión simple y predecible con cambios mínimos en los flujos de trabajo de secuenciación anteriores. Además, el secuenciador permite a los usuarios configurar las aplicaciones de forma más fácil para habilitar conexiones de aplicaciones virtualizadas.

Para obtener una lista de cambios en el secuenciador de App-V 5,1, consulte [acerca de App-v 5,1](about-app-v-51.md).

[Cómo instalar el secuenciador](how-to-install-the-sequencer-51beta-gb18030.md)

## <a href="" id="---------app-v-5-1-client-and-sequencer-logs"></a> Registros del cliente y el secuenciador de App-V 5,1


Puede usar la información de registro del secuenciador de App-V 5,1 para ayudar a solucionar problemas de instalación del secuenciador y de los eventos operativos al utilizar App-V 5,1. La información de registro relacionada con el secuenciador se puede revisar con el **visor de eventos**. En la siguiente línea se muestra la ruta de acceso específica para los eventos relacionados con el secuenciador:

**Visor de eventos \ \ aplicaciones y servicios registros \ \ Microsoft \ \ App V**. Los eventos relacionados con el secuenciado llevan el prefijo de **AppV \ _Sequencer**. Los eventos relacionados con el cliente llevan el prefijo de **AppV \ _Client**.

## Otros recursos para implementar el secuenciador y el cliente


[Implementación de App-V 5.1](deploying-app-v-51.md)

[Planificación de App-V 5.1](planning-for-app-v-51.md)






 

 





