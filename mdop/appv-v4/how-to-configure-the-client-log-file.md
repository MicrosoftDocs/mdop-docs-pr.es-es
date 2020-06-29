---
title: Cómo configurar el archivo de registro del cliente
description: Cómo configurar el archivo de registro del cliente
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817800"
---
# Cómo configurar el archivo de registro del cliente


Puede usar los procedimientos siguientes para configurar el archivo de registro de cliente de Application Virtualization (App-V).

**Para cambiar la ubicación del archivo de registro**

-   Edite el siguiente valor de la clave del registro para especificar la nueva ruta de acceso del archivo de registro. Debe reiniciar el servicio **sftlist** después de cambiar este valor. Esta ubicación también se puede cambiar de forma interactiva después de la instalación.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName

**Para cambiar el nivel de informes de registro**

-   De forma predeterminada, el tipo de mensajes que se escriben en el registro incluye todos los eventos de nivel de gravedad 4 (informativo) o superior. El nivel de gravedad se almacena en el siguiente valor de clave. Establezca este valor de clave en 5 para habilitar el registro detallado. Use el registro detallado solo durante breves períodos de solución de problemas, ya que generará un gran volumen de mensajes y hará que el registro se llene rápidamente.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity

**Para cambiar el tamaño del registro**

-   En Application Virtualization (App-V) 4,5, el tamaño del registro está controlado por el siguiente valor de la clave del registro. Este valor se establece de forma predeterminada en 256 MB y define el tamaño máximo, en MB, que puede alcanzar el registro antes de restablecerlo.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize

    **PRECAUCIÓN**  Este valor de clave del registro debe establecerse en un valor mayor que cero para garantizar que el archivo de registro se restablezca.

     

**Para cambiar el número de copias de seguridad**

-   Cuando el archivo de registro alcanza el tamaño máximo, se fuerza un reinicio cuando se produce la siguiente escritura en el registro. Un restablecimiento hace que se cree un nuevo archivo de registro y el nombre del archivo antiguo es de copia de seguridad. La siguiente configuración del registro controla el número de copias de seguridad del archivo de registro que se conservan cuando se restablece el archivo. El valor predeterminado es 4.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount

    El formato de los nombres de archivo de registro de la copia de seguridad es: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** y se basa en el tiempo de restablecimiento, en hora universal coordinada (UTC). En la tabla siguiente se enumeran los símbolos que se usan para crear los nombres de archivo y sus descripciones.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Símbolo</th>
    <th align="left">Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>DD</p></td>
    <td align="left"><p>año de 4 dígitos</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>MM</p></td>
    <td align="left"><p>mes de 2 dígitos (01 a 12)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>YYYY</p></td>
    <td align="left"><p>día del mes de 2 dígitos (01 a 31)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>HH</p></td>
    <td align="left"><p>hora (00 a 23)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>mm</p></td>
    <td align="left"><p>minutos (00 a 59)</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>ss</p></td>
    <td align="left"><p>segundos (00 a 59)</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>uuu</p></td>
    <td align="left"><p>milisegundos (000 a 999)</p></td>
    </tr>
    </tbody>
    </table>

     

## Temas relacionados


[Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





