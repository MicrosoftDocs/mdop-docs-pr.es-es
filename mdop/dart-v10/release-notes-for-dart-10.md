---
title: Notas de la versión de DaRT 10
description: Notas de la versión de DaRT 10
author: dansimp
ms.assetid: eb996980-f9c4-42cb-bde9-6b3d4b82b58c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 12ae5865538155f3c9ecf8b5f23b0d9e23232833
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822951"
---
# Notas de la versión de DaRT 10


**Para buscar estas notas de la versión, presione CTRL + F.**

Lea estas notas de la versión minuciosamente antes de instalar Microsoft Diagnostics and Recovery Toolset (DaRT) 10.

Estas notas de la versión contienen la información necesaria para instalar correctamente los diagnósticos y el conjunto de herramientas de recuperación 10. Las notas de la versión también contienen información que no está disponible en la documentación del producto. Si hay una diferencia entre estas notas de la versión y otra documentación de DaRT, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## Problemas conocidos con DaRT 10


### Disk Commander no puede reparar un registro de inicio maestro dañado en una partición física en Windows 10

En Windows 10, la opción "restaurar el registro de inicio maestro (MBR) o el encabezado de la tabla de particiones GUID (GPT)" en Disk Commander no puede reparar un registro de inicio maestro dañado en una partición física y, por lo tanto, no puede arrancar el equipo cliente.

**Solución alternativa:** Inicie **reparación de inicio**, haga clic en **solución de problemas**, **Opciones avanzadas**y, a continuación, haga clic en **iniciar reparación**.

### Varias instancias de borrado de disco dirigidas a la misma unidad hacen que todas las instancias, excepto la última, notifiquen un error

Si inicia varias instancias de borrado de disco y, a continuación, intenta borrar la misma unidad con dos instancias de borrado de disco separadas, todas las instancias excepto la última informarán de que se ha producido un error al borrar la unidad.

**Solución alternativa:** Nada.

### El borrado del disco puede no borrar todos los datos de las unidades de estado sólido que tienen memoria Flash

Si usa el borrado de disco para borrar los datos en una unidad de estado sólido (SSD) que tiene memoria Flash, es posible que no se eliminen todos los datos. Este problema se produce porque el firmware SSD controla la ubicación física de las escrituras mientras se ejecuta el borrador de disco.

**Solución alternativa:** Nada.

### Restaurar sistema falla al ejecutar el Asistente para locksmith o el editor del registro

Si ejecuta el Asistente de locksmith, el editor del registro y posiblemente otras herramientas, se producirá un error en Restaurar sistema.

**Solución alternativa:** Cierre y reinicie DaRT y, a continuación, inicie Restaurar sistema.

### El comprobador de archivos de sistema (SFC) no se puede ejecutar después de iniciar y cerrar el Asistente de locksmith o la administración de equipos

Si inicia y cierra Asistente para locksmith o herramientas en administración de equipos, el comprobador de archivos de sistema no podrá ejecutarse.

**Solución alternativa:** Cierre y reinicie DaRT y, a continuación, inicie el comprobador de archivos de sistema.

### <a href="" id="-------------dart-installer-does-not-fail-when-the-windows-assessment-and-deployment-kit-is-not-installed"></a> El instalador de DaRT no falla cuando no está instalado el Windows Assessment and Deployment Kit

Si instala DaRT 10 mediante la línea de comandos para ejecutar Windows Installer (. msi) y no se ha instalado el Windows Assessment and Deployment Kit (WindowsADK), la instalación de DaRT debería fallar. En la actualidad, el instalador de DaRT 10 instala todos los componentes excepto la imagen de recuperación de DaRT.

**Solución alternativa:** Nada.

## Temas relacionados


[Acerca de DaRT 10](about-dart-10.md)

 

 





