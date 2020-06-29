---
title: Códigos de error de línea de comandos de secuenciador
description: Códigos de error de línea de comandos de secuenciador
author: dansimp
ms.assetid: 3d491314-4923-45fd-9839-c541c5e620bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 74f5bd0c1b66656ac6891dcc1c019254fa36fdac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815560"
---
# Códigos de error de línea de comandos de secuenciador


Use la siguiente lista para identificar errores relacionados con las aplicaciones de secuencia mediante la línea de comandos. También puede ver esta información en el archivo de registro del secuenciador de App-V asociado.

**Nota:**  Pueden surgir varios errores durante la secuenciación y, si esto sucede, el código de error que se muestra puede ser la suma de dos códigos de error. Por ejemplo, si faltan los parámetros */InstallPath* y */OutputFile* , el secuenciador de App-V devolverá **96**, la suma de los dos códigos de error.

 

<a href="" id="01"></a>Agosto  
Hay un error no especificado.

<a href="" id="02"></a>neto  
El directorio de instalación especificado (/INSTALLPACKAGE) no es válido.

<a href="" id="04"></a>2004  
El directorio raíz del paquete (/INSTALLPATH) especificado no es válido.

<a href="" id="08"></a>08  
El parámetro de */OutputFile* especificado no es válido.

<a href="" id="16"></a>apartado  
No se especificó el directorio de instalación (/INSTALLPACKAGE).

<a href="" id="32"></a>32  
No se especificó el directorio de raíz del paquete (/INSTALLPATH).

<a href="" id="64"></a>64  
No se especificó el parámetro */OutputFile* .

<a href="" id="128"></a>128  
La unidad de virtualización de aplicaciones especificada no es válida.

<a href="" id="256"></a>256  
Error en el instalador.

<a href="" id="512"></a>512  
Error al secuenciar la aplicación.

<a href="" id="1024"></a>1024  
Error al evaluar los accesos directos instalados.

<a href="" id="2048"></a>2048  
No se puede guardar el paquete de aplicación de secuencia.

<a href="" id="4096"></a>4096  
El nombre de paquete especificado (/PACKAGENAME) no es válido.

<a href="" id="8192"></a>8192  
El tamaño de bloque especificado (/BLOCKSIZE) no es válido.

<a href="" id="16384"></a>16384  
El tipo de compresión especificado (/COMPRESSION) no es válido.

<a href="" id="32768"></a>32768  
La ruta de acceso del proyecto especificada no es válida.

<a href="" id="65536"></a>65536  
El parámetro de actualización especificado no es válido.

<a href="" id="131072"></a>131072  
El parámetro de proyecto de actualización especificado no es válido.

<a href="" id="262144"></a>262144  
El parámetro de la ruta de descodificación especificada no es válido.

<a href="" id="525288"></a>525288  
No se especificó el nombre del paquete.

## Temas relacionados


[Referencia del secuenciador de virtualización de aplicaciones](application-virtualization-sequencer-reference.md)

[Parámetros de línea de comandos del secuenciador](sequencer-command-line-parameters.md)

 

 





