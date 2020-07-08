---
title: Parámetros de línea de comandos del secuenciador
description: Parámetros de línea de comandos del secuenciador
author: dansimp
ms.assetid: 28fb875a-c302-4d95-b2e0-8dc0c5dbb0f8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ecfa269de04cf3dcba30cbb4a40f9176f03f6571
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815551"
---
# Parámetros de línea de comandos del secuenciador


Puede usar los siguientes parámetros de secuenciador de Application Virtualization (App-V) para secuenciar una aplicación y para actualizar una aplicación virtual existente mediante una línea de comandos. Para obtener más información sobre cómo secuenciar una aplicación mediante una línea de comandos, consulte [Cómo secuenciar una nueva aplicación mediante la línea de comandos](how-to-sequence-a-new-application-by-using-the-command-line.md).

## Parámetros de línea de comandos del secuenciador


<a href="" id="-help-or---"></a>**/HELP o/?**  
Muestra información sobre los parámetros que están disponibles para usar una línea de comandos para secuenciar aplicaciones.

<a href="" id="-installpackage-or--i"></a>**/INSTALLPACKAGE o/I**  
Especifica el Windows Installer o un archivo por lotes que se utilizará para instalar una aplicación de modo que se pueda secuenciar.

<a href="" id="-installpath-or--p"></a>**/INSTALLPATH o/P**  
Especifica el directorio raíz del paquete de una aplicación.

<a href="" id="-outputfile-or--o"></a>**/OUTPUTFILE o/O**  
Especifica la ruta y el nombre de archivo del archivo SPRJ que se generará.

<a href="" id="-fullload-or--f"></a>**/FULLLOAD o/F**  
Especifica si todos los archivos estarán contenidos en el bloque de características principal. Si se especifica el parámetro **/FULLLOAD** en la línea de comandos, todos los datos de la aplicación asociada se agregan al bloque de características principal. Si el parámetro **/FULLLOAD** no se especifica en la línea de comandos, entonces ninguno de los datos de la aplicación asociada se agrega al bloque de características principal.

<a href="" id="-packagename-or--k"></a>**/PACKAGENAME o/K**  
Especifica el nombre del paquete que se asignará a la aplicación de secuencia.

<a href="" id="-blocksize"></a>**/BLOCKSIZE**  
Especifica el tamaño de bloque de archivos SFT que se usará para transmitir el paquete a los equipos cliente. Puede seleccionar uno de los siguientes valores:

-   4 KB

-   16 KB

-   32 KB

-   64 KB

Debe tener en cuenta el tamaño del archivo SFT Cuando especifique el tamaño de bloque. Un archivo con un tamaño de bloque más pequeño tarda más tiempo en transmitirse a través de la red, pero requiere menos ancho de banda. Los archivos con tamaños de bloque mayores usan más ancho de banda de red.

<a href="" id="-compression"></a>**/COMPRESSION**  
Especifica el método para comprimir el archivo SFT que se transmitirá al cliente.

<a href="" id="-msi-or--m"></a>**/MSI o/M**  
Especifica si se debe crear un instalador de Windows para la aplicación de secuencia.

<a href="" id="-default"></a>**/DEFAULT**  
Especifica el archivo SPRJ predeterminado que se usará al crear un paquete de aplicación virtual. Este archivo se usa como plantilla. SPRJ cuando la aplicación se secuencia por primera vez.

<a href="" id="-upgrade"></a>**/UPGRADE**  
Especifica la ruta y el nombre de archivo del archivo SPRJ que se actualizará.

<a href="" id="-decodepath"></a>**/DECODEPATH**  
Especifica el directorio en el equipo en el que se encuentran los archivos asociados con el paquete de aplicación de secuencia instalado. Use uno de los siguientes formatos al especificar el directorio:

-   /decodepath: Q:

-   /decodepath:Q:.

-   /decodepath:"Q:."

-   /decodepath: "Q:"

## Temas relacionados


[Secuenciador de virtualización de aplicaciones](application-virtualization-sequencer.md)

[Códigos de error de línea de comandos de secuenciador](sequencer-command-line-error-codes.md)

 

 





