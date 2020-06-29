---
title: Clase WMI de paquetes de App-V
description: Clase WMI de paquetes de App-V
author: dansimp
ms.assetid: 0fc26c3b-9706-4804-be2d-645771dc33ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa452afaaeb2f490c179a928b24de47207d6dc63
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819800"
---
# Clase WMI de paquetes de App-V


En el cliente de Application Virtualization (App-V), la clase del **paquete** es una clase de instrumental de administración de Windows (WMI) que representa todos los paquetes virtuales del cliente. Los paquetes virtuales pueden contener muchas aplicaciones virtuales.

## Sintaxis


``` syntax
class Package
{
      string Name;
      string Version;
      string PackageGUID;
      string SftPath;
      uint64 TotalSize;
      uint64 CachedSize;
      uint64 LaunchSize;
      uint64 CachedLaunchSize;
      boolean InUse;
      boolean Locked;
      uint16 CachedPercentage;
      string VersionGUID;
 };
```

## Propiedades


<a href="" id="name"></a>**Nombre**  
Tipo de datos: **cadena**

Tipo de acceso: solo lectura

Cualificadores: ninguno

El nombre descriptivo del paquete virtual.

<a href="" id="version"></a>**Versión**  
Tipo de datos: **cadena**

Tipo de acceso: solo lectura

Cualificadores: ninguno

La versión del paquete virtual.

<a href="" id="packageguid"></a>**PackageGUID**  
Tipo de datos: **cadena**

Tipo de acceso: solo lectura

Cualificadores: clave

Identificador GUID de la configuración del paquete y los archivos de origen.

<a href="" id="sftpath"></a>**SftPath**  
Tipo de datos: **cadena**

Tipo de acceso: solo lectura

Cualificadores: ninguno

La ruta de acceso del archivo SFT.

<a href="" id="totalsize"></a>**TotalSize**  
Tipo de datos: **UInt64**

Tipo de acceso: solo lectura

Cualificadores: ninguno

El tamaño total del paquete virtual, en kilobytes.

<a href="" id="cachedsize"></a>**CachedSize**  
Tipo de datos: **UInt64**

Tipo de acceso: solo lectura

Cualificadores: ninguno

El tamaño total de la caché para el paquete virtual, en kilobytes.

<a href="" id="launchsize"></a>**LaunchSize**  
Tipo de datos: **UInt64**

Tipo de acceso: solo lectura

Cualificadores: ninguno

El tamaño total del bloque de características principal del paquete virtual, en kilobytes.

<a href="" id="cachedlaunchsize"></a>**CachedLaunchSize**  
Tipo de datos: **UInt64**

Tipo de acceso: solo lectura

Cualificadores: ninguno

Tamaño total del bloque de características principal del paquete virtual que se ha almacenado en caché, en kilobytes.

<a href="" id="inuse"></a>**InUse**  
Tipo de datos: **Boolean**

Tipo de acceso: solo lectura

Cualificadores: ninguno

**true** si se está ejecutando cualquier aplicación virtual del paquete virtual; en caso contrario, **false**.

<a href="" id="locked"></a>**Bloqueadas**  
Tipo de datos: **Boolean**

Tipo de acceso: solo lectura

Cualificadores: ninguno

**true** si el paquete virtual está bloqueado; en caso contrario, **false**.

<a href="" id="cachedpercentage"></a>**CachedPercentage**  
Tipo de datos: **UInt16**

Tipo de acceso: solo lectura

Cualificadores: ninguno

El porcentaje de los archivos en caché. Basado en la fórmula siguiente: CachedSize/TotalSize × 100.

<a href="" id="versionguid"></a>**VersionGUID**  
Tipo de datos: **cadena**

Tipo de acceso: solo lectura

Cualificadores: ninguno

Identificador de GUID de la versión del paquete.

 

 





