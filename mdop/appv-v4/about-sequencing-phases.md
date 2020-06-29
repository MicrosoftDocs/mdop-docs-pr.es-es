---
title: Acerca de las fases de secuenciación
description: Acerca de las fases de secuenciación
author: dansimp
ms.assetid: c1cb7b6c-204c-48f2-848c-4bd5a3d5ecb6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4e3d1504f0af82f3d21806b38bb4640b6f7ebc45
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820001"
---
# Acerca de las fases de secuenciación


La secuencia es el proceso mediante el cual se crea un paquete de aplicación secuencial mediante el secuenciador Microsoft Application Virtualization (App-V). Durante la secuenciación, el secuenciador supervisa y registra todos los procesos de instalación y configuración de una aplicación y crea los siguientes archivos: ICO, OSD, SFT y SPRJ. Estos archivos contienen toda la información necesaria sobre una aplicación y permiten que esa aplicación se ejecute en un entorno virtual.

Las cuatro fases para secuenciar una aplicación y crear un paquete de aplicación virtual son: instalación, Inicio, personalización y almacenamiento. En la siguiente lista se proporciona información acerca de cada una de las fases:

1.  **Fase de instalación**: durante la fase de instalación, especifique el nombre del paquete y un comentario asociado opcional que se asociará con el paquete. También puede configurar opciones de supervisión avanzadas durante esta fase. Las opciones de supervisión avanzadas incluyen especificar el tamaño del bloque y si se instalarán actualizaciones automáticas durante la supervisión. El secuenciador registra toda la información y todas las configuraciones necesarias para crear un paquete de aplicación virtual, así como el archivo asociado y la configuración del registro.

    **Importante**  Para ver las opciones avanzadas, seleccione **Mostrar opciones de supervisión avanzadas** en la página **información del paquete** .

     

2.  **Fase de inicio**: durante la fase de inicio, puede especificar cualquier asociación de archivos necesaria y los descriptores de seguridad que se deben configurar con el paquete. Debe abrir la aplicación tantas veces como sea necesario para garantizar la funcionalidad y la estabilidad de la aplicación.

3.  **Fase de personalización**: durante la fase de personalización, puede configurar el paquete mediante los archivos. OSD asociados. Puede especificar si desea que los scripts asociados se ejecuten dentro o fuera del entorno virtual, especificar acciones adicionales que se deben realizar, especificar cómo se ejecutan las secuencias de comandos asociadas (sincrónicamente o asincrónicamente), y especificar cualquier script adicional que deba ejecutarse en el contexto del usuario.

4.  **Guardar fase**: durante la fase de guardado, se crean todos los archivos necesarios para el paquete de aplicaciones virtuales. Los archivos creados son. SPRJ,. SFT,. OSD,. ico,. XML y el archivo de Windows Installer (. msi).

## Temas relacionados


[Secuenciador de virtualización de aplicaciones](application-virtualization-sequencer.md)

 

 





