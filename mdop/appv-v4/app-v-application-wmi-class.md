---
title: Clase WMI de aplicación de App-V
description: Clase WMI de aplicación de App-V
author: dansimp
ms.assetid: b79b0d5a-ba57-442f-8bb4-d7154fc056f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a4e1e49e35b231ddb2a480a06c46e364121ac2d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822321"
---
# Clase WMI de aplicación de App-V


En el cliente de Application Virtualization (App-V), la clase de la **aplicación** es una clase de instrumental de administración de Windows (WMI) que representa todas las aplicaciones virtuales en el cliente.

La siguiente sintaxis se ha simplificado del código de formato de objeto administrado (MOF). El código incluye todas las propiedades heredadas.

## Sintaxis


``` syntax
class Application
{
      string Name;
      string Version;
      string PackageGUID;
      datetime LastLaunchOnSystem;
      uint32 GlobalRunningCount;
      boolean Loading;
      string OriginalOsdPath;
      string CachedOsdPath;
};
```

## Requisitos


## Propiedades


<a href="" id="name"></a>**Nombre**  
Tipo de datos: **cadena**

Tipo de acceso: solo lectura

Cualificadores: clave

El nombre para mostrar de la aplicación virtual.

<a href="" id="version"></a>**Versión**  
Tipo de datos: **cadena**

Tipo de acceso: solo lectura

Cualificadores: clave

La versión de la aplicación virtual.

<a href="" id="packageguid"></a>**PackageGUID**  
Tipo de datos: **cadena**

Tipo de acceso: solo lectura

Cualificadores: ninguno

El GUID del paquete con el que está asociada la aplicación virtual.

<a href="" id="lastlaunchonsystem"></a>**LastLaunchOnSystem**  
Tipo de datos: **DateTime**

Tipo de acceso: solo lectura

Cualificadores: ninguno

La última fecha y hora en la que se inició la aplicación virtual.

<a href="" id="globalrunningcount"></a>**GlobalRunningCount**  
Tipo de datos: **UInt32**

Tipo de acceso: solo lectura

Cualificadores: ninguno

Recuento de las instancias en ejecución de la aplicación virtual que se iniciaron directamente.

<a href="" id="loading"></a>**Cargando**  
Tipo de datos: **Boolean**

Tipo de acceso: solo lectura

Cualificadores: ninguno

**true** si la aplicación virtual se está iniciando; en caso contrario, **false**.

<a href="" id="originalosdpath"></a>**OriginalOsdPath**  
Tipo de datos: **cadena**

Tipo de acceso: solo lectura

Cualificadores: ninguno

La ruta de acceso original del archivo OSD que se registró con el cliente de App-V.

<a href="" id="cachedosdpath"></a>**CachedOsdPath**  
Tipo de datos: **cadena**

Tipo de acceso: solo lectura

Cualificadores: ninguno

La ruta de acceso al archivo OSD si el cliente de App-V ha almacenado en caché el archivo OSD de forma local.

 

 





