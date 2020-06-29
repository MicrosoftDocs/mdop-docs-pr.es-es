---
title: Cómo cargar paquetes y archivos
description: Cómo cargar paquetes y archivos
author: dansimp
ms.assetid: f86f5bf1-99a4-44d7-ae2f-e6049c482f68
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9427fd8089ec9c22d7d379b15ae94bf421ca2d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817240"
---
# Cómo cargar paquetes y archivos


Puede usar el siguiente procedimiento para cargar archivos y paquetes en servidores de virtualización de aplicaciones.

**Nota:**  Durante el proceso de instalación, especificó la ubicación del directorio \\Content en la página **ruta de contenido** . Este directorio debe crearse y configurarse como un recurso compartido de archivos estándar antes de apuntar a su ubicación.

 

**Para cargar archivos y paquetes**

1.  En el equipo desde el que se transfieren las aplicaciones, vaya a la ubicación que especificó para el directorio \\Content. Si es necesario, cree el directorio y configúrelo como un recurso compartido de archivos estándar.

2.  Mueva los archivos SFT de las aplicaciones virtuales y los paquetes al directorio \\Content. Para mantener organizados los archivos de SFT y evitar confusiones, ponga aplicaciones y paquetes en subcarpetas dedicadas.

3.  Cargue las aplicaciones y los paquetes de acuerdo con los requisitos de su escenario y configuración, teniendo en cuenta las condiciones siguientes:

    -   Si sus aplicaciones y paquetes se almacenan en un servidor de administración de Application Virtualization (App-V), cárguelos a través de la consola de administración. Para obtener más información, vea [Cómo cargar o descargar una aplicación](how-to-load-or-unload-an-application.md) o [Cómo cargar aplicaciones virtuales desde el área de notificación del escritorio](how-to-load-virtual-applications-from-the-desktop-notification-area.md).

    -   Si las aplicaciones se almacenan en un servidor de streaming de App-V, un servidor web o un equipo configurado como servidor de archivos, las aplicaciones se pueden cargar automáticamente.

        **Nota:**  El servidor de streaming de App-V sondea automáticamente el directorio \\Content de aplicaciones y paquetes y coloca esta información en la RAM para atender las solicitudes de la aplicación.

        Los clientes de App-V deben estar configurados correctamente para recuperar aplicaciones y paquetes de servidores web y servidores de archivos. Para obtener más información, vea [Cómo configurar el cliente para la recuperación de paquetes de aplicaciones](how-to-configure-the-client-for-application-package-retrieval.md).

         

## Temas relacionados


[Servidor de virtualización de aplicaciones](application-virtualization-server.md)

 

 





