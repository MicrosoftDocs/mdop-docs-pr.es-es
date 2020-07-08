---
title: Parámetros de línea de comandos
description: Parámetros de línea de comandos
author: dansimp
ms.assetid: d90a0591-f1ce-4cb8-b244-85cc70461922
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31d6ca1215648e2519e9818817ab5cc779a746d0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819401"
---
# Parámetros de línea de comandos


Use los siguientes parámetros de Application Virtualization Sequencer para secuenciar una aplicación y actualizar un paquete de aplicación de secuencia en el símbolo del sistema. En el directorio Microsoft Application Virtualization Sequencer, escribiría **SFTSequencer**, seguido por el parámetro adecuado.

<a href="" id="-help-or---"></a>*/Help* o */?*  
Se usa para mostrar la lista de parámetros disponibles para la secuencia de la línea de comandos.

<a href="" id="-installpackage-or--i"></a>*/INSTALLPACKAGE* o */i*  
Se usa para especificar el instalador o un archivo por lotes para la aplicación que se va a secuenciar.

<a href="" id="-installpath-or--p"></a>*/InstallPath* o */p*  
Usar para especificar el directorio raíz del paquete.

<a href="" id="-outputfile-or--o"></a>*/OutputFile* o */o*  
Se usa para especificar la ruta y el nombre de archivo del archivo SPRJ que se generará.

**Importante**  El parámetro */OutputFile* no está disponible al abrir un paquete que no desee actualizar.

 

<a href="" id="-fullload-or--f"></a>*/FULLLOAD* o */f*  
Se usa para especificar si se coloca todo en el bloque de características principal.

<a href="" id="-packagename-or--k"></a>*/Packagename* o */k*  
Se usa para especificar el nombre de paquete de la aplicación de secuencia.

<a href="" id="-blocksize"></a>*/BLOCKSIZE*  
Especifica el tamaño de bloque de archivos SFT que se usará para transmitir el paquete a los equipos cliente. Puede seleccionar uno de los siguientes valores:

-   4 KB

-   16 KB

-   32 KB

-   64 KB

Debe tener en cuenta el tamaño del archivo SFT Cuando especifique el tamaño de bloque. Un archivo con un tamaño de bloque más pequeño tarda más tiempo en transmitirse a través de la red, pero requiere menos ancho de banda. Los archivos con tamaños de bloque mayores usan más ancho de banda de red.

<a href="" id="-compression"></a>*/COMPRESSION*  
Se usa para especificar el método para comprimir el archivo SFT a medida que se transmite al cliente.

<a href="" id="-msi-or--m"></a>*/MSI* o */m*  
Se usa para especificar la generación de un paquete de Microsoft Windows Installer para la aplicación de secuencia.

<a href="" id="-default"></a>*/DEFAULT*  
Especifica el archivo SPRJ predeterminado que se usará al crear un paquete de aplicación virtual. Este archivo se usa como plantilla. SPRJ cuando la aplicación se secuencia por primera vez.

<a href="" id="-upgrade"></a>*/UPGRADE*  
Especifica la ruta y el nombre de archivo del archivo SPRJ que se actualizará.

<a href="" id="-decodepath"></a>*/DECODEPATH*  
Especifica el directorio en el equipo en el que se encuentran los archivos asociados con el paquete de aplicación de secuencia instalado. Use uno de los siguientes formatos al especificar el directorio:

-   /decodepath: Q:

-   /decodepath:Q:.

-   /decodepath:"Q:."

-   /decodepath: "Q:"

## Temas relacionados


[Acerca de cómo usar la línea de comandos del secuenciador](about-using-the-sequencer-command-line.md)

[Cómo abrir una aplicación secuenciada mediante la línea de comandos](how-to-open-a-sequenced-application-using-the-command-line.md)

[Cómo actualizar un paquete mediante el comando Abrir paquete](how-to-upgrade-a-package-using-the-open-package-command.md)

 

 





