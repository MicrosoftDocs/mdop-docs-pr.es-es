---
title: Solución de problemas del secuenciador de virtualización de aplicaciones
description: Solución de problemas del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 12ea8367-0b84-44e1-a885-e0539486556b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60c47b853c74d90afc21e9ca172c0eec2a2c7a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815181"
---
# Solución de problemas del secuenciador de virtualización de aplicaciones


En este tema se incluye información que puede usar para solucionar problemas generales en el secuenciador de Application Virtualization (App-V).

## Crear un archivo SFTD mediante el secuenciador de App-V aumenta el número de versión de forma inesperada


El número de versión asociado a un archivo de SFTD se incrementa de forma inesperada.

**Solución**

Use la línea de comandos para generar un nuevo archivo. SFT. Para crear el archivo. SFT con la línea de comandos, escriba lo siguiente en un símbolo del sistema:

**Nombre de archivo de mkdiffpkg.exe &lt; base SFT &gt; &lt; diff SFT nombre de archivo&gt;**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a>El nombre de archivo del archivo OSD no es correcto después de actualizar el paquete


Después de actualizar un paquete existente, el nombre de archivo no es correcto.

**Solución**

Cuando abre un paquete para la actualización, debe especificar la unidad raíz de Q:\\ como la ubicación de salida del paquete. No especifique un nombre de archivo asociado con la ubicación de salida.

## La instalación predeterminada de Microsoft Word2003 provoca un error cuando se transmite a un cliente


Al transmitir Microsoft Word2003 a un cliente, se devuelve un error pero Microsoft Word continúa ejecutándose.

**Solución**

Reordene el paquete de aplicación virtual y seleccione **instalación completa**.

## La actualización del paquete no funciona al crear un paquete dependiente


Cuando se crea un paquete dependiente mediante la actualización de un paquete y se agregan nuevas entradas del registro, parece que funciona correctamente, pero las entradas del registro actualizadas no están disponibles.

**Solución**

La configuración del registro siempre se almacena con la versión original del paquete, por lo que las actualizaciones del paquete no estarán disponibles a menos que repares el paquete original.

## Error al intentar realizar la secuencia. NET 2.0


Al secuenciar un paquete que lo requiera. NET 2.0, se producirá un error.

**Solución**

Secuencias de paquetes que requieren. NET 2.0 no es compatible.

## Temas relacionados


[Secuenciador de virtualización de aplicaciones](application-virtualization-sequencer.md)

 

 





