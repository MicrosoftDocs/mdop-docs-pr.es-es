---
title: Componentes adicionales de paquete de aplicaciones virtuales
description: Componentes adicionales de paquete de aplicaciones virtuales
author: dansimp
ms.assetid: 476b0f40-ebd6-4296-92fa-61fa9495c03c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d30c2c6561b0d2c08fd75e0c977bf4590d7e6688
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815080"
---
# Componentes adicionales de paquete de aplicaciones virtuales


El secuenciador de App-V ha detectado un directorio que contiene los ejecutables de 64 bits y 32 bits, o los archivos de biblioteca de vínculos dinámicos (. dll) que dependen del mismo ensamblado en paralelo. Normalmente, el secuenciador crea ensamblados simultáneos privados para todos los ensamblados públicos que usa el paquete; sin embargo, no es posible crear versiones de 32 y 64 bits de los ensamblados privados en el mismo directorio.

Si el secuenciador detecta un único conflicto, realizará las siguientes acciones:

-   Quite todos los ensamblados privados de 64 bits existentes en todo el paquete, si el directorio tiene un conflicto o no.

-   Cree solo las versiones de 32 bits de los ensamblados en paralelo privados.

Debe instalar de forma nativa las versiones públicas de todos los ensamblados de 64 bits necesarios en el equipo que ejecuta el secuenciador y en todos los equipos cliente de App-V.

Para encontrar los ensamblados públicos existentes necesarios, abra el directorio en el que está guardado el paquete y búsquelo en la carpeta **VFS** . Por ejemplo, si la raíz del paquete es **Q:\\MyApp**, cuando ordene la aplicación, busque en **Q:\\MyApp\\VFS\\CSIDL\ _Windows \\winsxs\\manifests** y busque todos los ensamblados públicos existentes. Las versiones de 64 bits de estos archivos siempre comenzarán con el texto siguiente al principio del nombre del manifiesto: **AMD64...**. El nombre exacto y la versión del ensamblado pueden encontrarse en el archivo de manifiesto asociado.

Use cualquiera de los siguientes vínculos para descargar e instalar la versión correcta de los requisitos previos necesarios:

-   [Paquete redistribuible de Microsoft Visual C++ 2005 (x64)](https://go.microsoft.com/fwlink/?LinkId=152697)

-   [Paquete redistribuible de Microsoft Visual C++ 2005 SP1 (x64)](https://go.microsoft.com/fwlink/?LinkId=152698)

-   [Paquete redistribuible de Microsoft Visual C++ 2008 (x64)](https://go.microsoft.com/fwlink/?LinkId=152699)

-   [Paquete redistribuible de Microsoft Visual C++ 2008 SP1 (x64)](https://go.microsoft.com/fwlink/?LinkId=152700)

 

 





