---
title: Solución de problemas del secuenciador de virtualización de aplicaciones
description: Solución de problemas del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 2712094b-a0bc-4643-aced-5415535f3fec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8b84f37217f29ff2c08a2254d7f54ce74348d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815241"
---
# Solución de problemas del secuenciador de virtualización de aplicaciones


En este tema se incluye información que puede usar para solucionar problemas generales en el secuenciador de Application Virtualization (App-V).

## Crear un archivo SFTD mediante el secuenciador de App-V aumenta el número de versión de forma inesperada


Use la línea de comandos para generar un nuevo archivo. SFT. Para crear el archivo. SFT con la línea de comandos, escriba lo siguiente en un símbolo del sistema:

**Nombre de archivo de mkdiffpkg.exe &lt; base SFT &gt; &lt; diff SFT nombre de archivo&gt;**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a>El nombre de archivo del archivo OSD no es correcto después de actualizar el paquete


Cuando abre un paquete para la actualización, debe especificar la unidad raíz de Q:\\ como la ubicación de salida del paquete. No especifique un nombre de archivo asociado con la ubicación de salida.

## La instalación predeterminada de Microsoft Word2003 provoca un error cuando se transmite a un cliente


Al transmitir Microsoft Word2003 a un cliente, se devuelve un error, pero Microsoft Word continúa ejecutándose.

**Solución**

Reordene el paquete de aplicación virtual y seleccione **instalación completa**.

## La actualización activa no funciona al crear un paquete dependiente


Cuando se crea un paquete dependiente mediante una actualización activa y se agregan nuevas entradas del registro, parece que funciona correctamente, pero las entradas del registro actualizadas no están disponibles.

**Solución**

La configuración del registro siempre se almacena con la versión original del paquete, por lo que las actualizaciones del paquete no estarán disponibles a menos que repares el paquete original.

## No se puede ver la información detallada de los documentos de Microsoft Office2007 mediante la página de propiedades


Cuando intenta ver información detallada asociada a un documento de Microsoft Office2007 mediante la página Propiedades, la información detallada no está visible.

**Solución**

App-V no es compatible con las extensiones de Shell necesarias para estas páginas de propiedades.

## Algunas claves de registro no se capturan al secuenciar aplicaciones de 16 bits


En App-V 4,5, el enlace de registro se ha movido del modo de núcleo al modo de usuario. Si desea secuenciar una aplicación de 16 bits o una aplicación que use un instalador de 16 bits, primero debe configurar el equipo secuenciador de modo que el proceso se ejecute en su propia copia de la máquina DOS virtual de Windows NT (NTVDM).

**Solución**

Antes de secuenciar la aplicación, establezca el siguiente valor de la clave del registro global REGSZ en "sí" en el equipo de secuenciación:

HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM

Debe reiniciar el equipo antes de que esto surta efecto.

## Temas relacionados


[Secuenciador de virtualización de aplicaciones](application-virtualization-sequencer.md)

 

 





