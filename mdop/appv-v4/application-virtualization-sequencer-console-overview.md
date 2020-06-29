---
title: Introducción a la consola del secuenciador de virtualización de aplicaciones
description: Introducción a la consola del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 681bb40d-2937-4645-82aa-4a44775232d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2f977fccaaded0309181a1d74c16b749498abb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822191"
---
# Introducción a la consola del secuenciador de virtualización de aplicaciones


El secuenciador de Application Virtualization (App-V) crea aplicaciones de modo que se puedan ejecutar en un entorno virtual, como aplicaciones virtuales. Una vez que se ha realizado la secuencia de una aplicación, puede ejecutarse desde un servidor de App-V hasta equipos de destino que ejecuten el cliente de escritorio de App-V o el cliente de App-v para servicios de escritorio remoto (anteriormente servicios de Terminal Server) mediante un proceso denominado transmisión por secuencias. El secuenciador de App-V supervisa el proceso de instalación y configuración de las aplicaciones, y registra toda la información necesaria para que la aplicación se ejecute en el entorno virtual. Este proceso también determina qué archivos y configuraciones se aplican a todos los usuarios y qué configuraciones pueden personalizar los usuarios. Las aplicaciones virtuales se ejecutan en equipos de destino y no tienen ningún efecto en el sistema operativo que se ejecuta en el equipo de destino o en cualquier aplicación instalada en el equipo de destino.

## Consideraciones de seguridad del transordeno de Application Virtualization


El secuenciador de App-V ejecuta todos los servicios detectados en el momento de la secuenciación con la cuenta del sistema local y no aplica los descriptores de seguridad en las solicitudes de control de servicio. Si el servicio se instaló con una cuenta de usuario diferente o si los descriptores de seguridad están diseñados para conceder a diferentes grupos de usuarios permisos de servicio específicos, considere detenidamente si el servicio debe virtualizarse. En algunos casos, debe instalar el servicio localmente para asegurarse de que se mantiene la seguridad de los servicios previstas.

## Opciones del menú de la consola de Application Virtualization Sequencer


Los siguientes elementos de menú están disponibles en la consola del secuenciador de App-V:

-   **Archivo**: contiene varios comandos para ayudarle a crear, abrir, modificar y guardar aplicaciones secuenciadas.

-   **Editar**: contiene varios comandos para editar las aplicaciones virtuales existentes.

-   **Vista**: contiene varios comandos para ver las propiedades de una aplicación virtual.

-   **Herramientas**: contiene diversas herramientas y diagnósticos para configurar aplicaciones virtuales.

## Opciones de la barra de herramientas de Application Virtualization Sequencer


Los siguientes botones de la barra de herramientas están disponibles en la consola del secuenciador de App-V:

-   **Nuevo paquete**: haga clic para crear una nueva aplicación de secuencia.

-   **Abrir**: haga clic para abrir un paquete de aplicaciones de secuencia en la consola del secuenciador de App-V.

-   **Abrir para actualización**: haga clic para abrir una aplicación de secuencia para actualizar o aplicar una actualización.

-   **Guardar**: haga clic para guardar una aplicación virtual secuencial.

-   **Asistente para secuenciación**: haga clic para abrir el Asistente para secuenciación. Debe usar este botón para iniciar el Asistente para secuenciación si realiza algún cambio en la pestaña **General** , en opciones de **herramientas**  /  **Options**.

## Pestañas de aplicaciones virtuales


Las siguientes pestañas se muestran al ver una aplicación virtual en la consola del secuenciador de App-V:

-   **Propiedades**: muestra información sobre la aplicación virtual seleccionada. Puede actualizar el **nombre del paquete** y los **comentarios** asociados a la aplicación virtual.

-   **Implementación**: muestra información sobre cómo los equipos de destino accederán a la aplicación virtual. Puede configurar el método de entrega virtual de aplicaciones y puede configurar los sistemas operativos que deben ejecutarse en el equipo de destino. También puede configurar las opciones de salida asociadas. Si desea que los clientes tengan acceso a una aplicación virtual desde un archivo, use el siguiente formato al especificar la ruta de acceso: **File://Server/share/path/.SFT**. Seleccione **exigir descriptores de seguridad** para preservar la seguridad asociada con el paquete durante una actualización, o los permisos se restablecerán durante la actualización.

-   **Historial de cambios**: muestra información sobre las actualizaciones que se han realizado en la aplicación virtual.

-   **Archivos**: muestra los archivos asociados a la aplicación virtual seleccionada. Puede hacer pequeñas revisiones de las propiedades del archivo asociado mediante los campos correspondientes.

-   **Registro virtual**: muestra el registro virtual asociado a la aplicación virtual seleccionada. Puede Agregar o eliminar claves de registro haciendo clic con el botón secundario en la entrada correspondiente.

-   **Sistema de archivos virtual**: muestra los sistemas de archivos virtuales asociados a la aplicación virtual seleccionada. Puede Agregar, eliminar o editar entradas del sistema de archivos en esta pestaña haciendo clic con el botón secundario en la entrada correspondiente y seleccionando la opción.

-   **Servicios virtuales**: muestra los servicios asociados a la aplicación virtual seleccionada.

-   **OSD**: muestra información sobre el descriptor de software abierto (OSD) asociado con la aplicación virtual. Puede actualizar los archivos asociados con el archivo OSD haciendo clic con el botón secundario en la entrada correspondiente y seleccionando la acción que desee.

## Temas relacionados


[Secuenciador de virtualización de aplicaciones](application-virtualization-sequencer.md)

 

 





