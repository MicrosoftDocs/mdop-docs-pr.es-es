---
title: Acerca de DaRT 8.0
description: Acerca de DaRT 8.0
author: dansimp
ms.assetid: ce91efd6-7d78-44cb-bb8f-1f43f768ebaa
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e70816425dc4775b11596b91d7b5c0045830c6ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821281"
---
# Acerca de DaRT 8.0


Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0 le ayuda a solucionar problemas y reparar equipos basados en Windows. Esto incluye los equipos que no se pueden iniciar. DaRT 8,0 es un conjunto de herramientas eficaz que amplía el entorno de recuperación de Windows (WinRE). Al usar DaRT, puede analizar un problema para determinar su causa, por ejemplo, inspeccionando el registro de eventos del equipo o el registro del sistema. DaRT admite la recuperación de discos duros básicos que contienen particiones, por ejemplo, particiones primarias y unidades lógicas, y admite la recuperación de volúmenes.

**Nota:**  DaRT no admite la recuperación de discos dinámicos.

 

DaRT también proporciona herramientas para ayudarle a corregir un problema tan pronto como determine la causa. Por ejemplo, puede usar las herramientas de DaRT para deshabilitar un controlador de dispositivo defectuoso, quitar revisiones, restaurar archivos eliminados y buscar malware en el equipo incluso cuando no puede o no debe iniciar el sistema operativo Windows instalado.

DaRT puede ayudarle a recuperar rápidamente los equipos que ejecutan las versiones de 32 o 64 bits de Windows 8, generalmente en menos tiempo de la que requeriría volver a crear la imagen del equipo.

La funcionalidad de DaRT le permite crear una imagen de recuperación. La imagen de recuperación inicia el entorno de recuperación de Windows (Windows RE), desde el que puede iniciar la ventana del conjunto de herramientas de **diagnóstico y recuperación** , y acceder a las herramientas de DART.

Use el **Asistente de recuperación de imágenes de DART** para crear la imagen de recuperación de DART. De forma predeterminada, el asistente crea un archivo de imagen de organización internacional de normalización (ISO) y un archivo de formato de imágenes de Windows (WIM) y permite grabar la imagen en un CD, DVD o USB. Puede implementar la imagen localmente en los equipos de los usuarios finales o puede implementarla desde una partición de red remota o una partición de recuperación en la unidad de disco duro local.

## <a href="" id="what-s-new-in-dart-8-0"></a>Novedades de DaRT 8,0


DaRT 8,0 puede ayudarle a recuperar rápidamente equipos que ejecutan versiones de 32 o 64 bits de Windows 8, generalmente en menos tiempo de los que llevaría para volver a crear una imagen del equipo. DaRT 8,0 tiene las siguientes características nuevas.

### Crear imágenes de DaRT con Windows 8 o Windows Server 2012

DaRT 8,0 le permite crear imágenes de DaRT con Windows® 8 o Windows Server® 2012. Para las versiones de Windows anteriores a Windows 8 y Windows Server 2012, los clientes deben continuar usando versiones anteriores de DaRT.

### Generar imágenes de 32 y 64 bits de un equipo PC

DaRT 8,0 le permite generar imágenes de 32 bits y 64 bits desde un solo equipo que ejecute DaRT, independientemente de si el equipo es un equipo de 32 o de 64 bits. En DaRT7, la imagen que se creó tenía que ser el mismo que el equipo que ejecutaba DaRT.

### Crear una imagen que admita equipos que tengan una interfaz de BIOS o UEFI

La compatibilidad de DaRT 8.0 con las interfaces de BIOS extensible firmware Interface (UEFI) y las interfaces de BIOS le permite crear una sola imagen que funciona con equipos que tienen cualquiera de las dos interfaces.

### Usar una tabla de particiones GUID (GPT) para la partición

Las herramientas de DaRT 8,0 ahora son compatibles con discos GPT de Windows 8, que proporcionan un mecanismo más flexible para particionar discos que el esquema de particiones del registro de inicio principal (MBR) antiguo. Las herramientas de DaRT 8,0 siguen admitiendo la partición MBR.

### Instalar Windows 8 y Windows Server 2012 en el disco duro local

Las herramientas de DaRT 8,0 solo se pueden usar cuando Windows 8 y Windows Server 2012 están instalados en el disco duro local. Por el momento, no hay soporte técnico para Windows to go.

### <a href="" id="-------------dart-8-0-release-notes"></a> Notas de la versión de DaRT 8,0

Para obtener más información y para obtener noticias de última hora que no se han incorporado en la documentación, consulte las [notas de la versión de DaRT 8,0](release-notes-for-dart-80--dart-8.md).

## Cómo obtener DaRT 8,0


Esta tecnología es parte del paquete de optimización de escritorio de Microsoft (MDOP). MDOP es parte de Microsoft Software Assurance. Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Temas relacionados


[Tareas iniciales con DaRT 8.0](getting-started-with-dart-80-dart-8.md)

[Notas de la versión de DaRT 8.0](release-notes-for-dart-80--dart-8.md)

 

 





