---
title: Acerca de la pestaña Archivos
description: Acerca de la pestaña Archivos
author: dansimp
ms.assetid: 3c20e720-4b0f-465b-b7c4-3013dae1c815
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e71cd0b60f9722da9736fc6987100f5c7bf53ab
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819930"
---
# Acerca de la pestaña Archivos


La pestaña **archivos** muestra la lista completa de archivos que se incluyen en un paquete de aplicación de secuencia. En el panel izquierdo se muestra, con un formato de exploración de archivos estándar, la lista completa de archivos del paquete que se creó durante la secuenciación de la aplicación. Estos archivos incluyen el directorio raíz del paquete (el directorio especificado durante la fase de instalación de la aplicación), la carpeta del sistema de archivos virtual (VFS) y los archivos de entorno virtual. El panel derecho muestra el nombre de archivo, los atributos de archivo y los atributos del secuenciador.

## Nombre de archivo y nombre corto


<a href="" id="file-name"></a>**Nombre de archivo**  
El nombre del archivo se encuentra en el panel de la izquierda. Los archivos que se muestran en el panel izquierdo se crean durante la secuenciación.

<a href="" id="short-name"></a>**Nombre corto**  
Este es el nombre de un archivo seleccionado en el panel de la izquierda, escrito en la Convención de nomenclatura de formato de 8,3.

## Atributos de archivo


<a href="" id="file-size"></a>**Tamaño de archivo**  
Tamaño del archivo en bytes.

<a href="" id="file-version"></a>**Versión de archivo**  
La versión del archivo seleccionado.

<a href="" id="date-created"></a>**Fecha de creación**  
La fecha y la hora en que se creó el archivo seleccionado.

<a href="" id="date-modified"></a>**Fecha de modificación**  
La fecha y la hora en que se modificó el archivo seleccionado por última vez.

<a href="" id="file-id"></a>**File ID**  
El GUID del archivo.

## Atributos del secuenciador


<a href="" id="user-data"></a>**Datos de usuario**  
Seleccione este atributo para especificar que una aplicación debe conservar la información de un usuario individual.

<a href="" id="application-data"></a>**Datos de la aplicación**  
Seleccione este atributo para especificar que una aplicación debe conservar la información general de un grupo de usuarios.

<a href="" id="override"></a>**Invalidar**  
Cuando se selecciona, el cliente de escritorio de Application Virtualization sobrescribe el archivo correspondiente cuando el paquete de aplicación secuenciado se actualiza y se transmite al cliente. Si esta casilla no está activada, el cliente determina si se sobrescribe o no el archivo seleccionado.

## Temas relacionados


[Cómo modificar los archivos incluidos en un paquete](how-to-modify-the-files-included-in-a-package.md)

[Consola de secuenciador](sequencer-console.md)

 

 





