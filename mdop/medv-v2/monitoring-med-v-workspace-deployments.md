---
title: Supervisión de las implementaciones de área de trabajo de MED-V
description: Supervisión de las implementaciones de área de trabajo de MED-V
author: dansimp
ms.assetid: 5de0cb06-b8a9-48a5-b8b3-836954295765
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ec4c7c85326e7945aa3d61b7f96872afe24fe37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827211"
---
# Supervisión de las implementaciones de área de trabajo de MED-V


La característica de supervisión de la virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0 permite ejecutar consultas en áreas de trabajo individuales de MED-V para determinar si la primera configuración se realizó correctamente en toda la empresa después de implementar las áreas de trabajo de MED-V. Supervisar el éxito de la configuración es importante porque MED-V no se encuentra en un estado utilizable hasta que la configuración se complete correctamente por primera vez.

Esta sección proporciona información e instrucciones para ayudarle a supervisar el éxito o el fracaso de la configuración de la primera vez.

## Para supervisar implementaciones del área de trabajo de MED-V


La característica de supervisión consiste en un proveedor integrado de instrumental de administración de Windows (WMI) en proceso que puede consultar con el lenguaje de consultas WMI para descubrir el estado de la configuración de primera vez para todos los usuarios finales en un área de trabajo de MED-V.

El proveedor WMI se implementa mediante el marco de extensiones del proveedor WMI de Microsoft .NET Framework 3,5. El proveedor WMI se ejecuta en el contexto de LocalService y almacena el estado de la configuración por primera vez en \\ProgramData.

El proveedor WMI se implementa en el espacio de nombres **root\\microsoft\\medv** e implementa la clase **FTS \ _Status**, que expone el método **SetFtsState**. MED-V usa **SetFtsState** para establecer el estado de configuración de la primera vez.

La clase contiene las siguientes propiedades.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propiedad</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Máquina</strong></p></td>
<td align="left"><p><strong></strong>Propiedad de solo lectura que contiene el nombre de la máquina virtual invitada aprovisionada por la configuración primera vez. Esta clave contiene el nombre que el invitado habría tenido en el primer error de configuración.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>StatusCode</strong></p></td>
<td align="left"><p><strong></strong>Propiedad de solo lectura que contiene cero si la configuración de la primera vez se realizó correctamente. Cualquier otro valor devuelto es igual al identificador de evento del error que se ha registrado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Tiempo</strong></p></td>
<td align="left"><p>La hora UTC en que se completó por primera vez la configuración.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Usuario</strong></p></td>
<td align="left"><p>El usuario para el que se ejecutó por primera vez la configuración.</p></td>
</tr>
</tbody>
</table>

 

En el código siguiente se muestra el archivo de formato de objetos administrados (MOF) que define la clase **FTS \ _Status** .

``` syntax
[dynamic: ToInstance, provider("MedvWmi, Version=2.0.258.0, Culture=neutral, PublicKeyToken=14986c3f172d1c2c")]
class FTS_Status
{
[read, key] string User;
[read] string Machine;
[read] sint32 StatusCode;
[read] datetime Time;
[static, implemented] void SetFtsState([in] sint32 statusCode, [in] string machine);
};
```

Como lo más probable es que la preocupación principal sea que las áreas de trabajo de MED-V no se completen correctamente por primera vez, puede escribir la consulta para que solo devuelva los errores que no se hayan podido configurar por primera vez, por ejemplo:

``` syntax
Select * from FTS_Status where StatusCode != 0
```

En este caso, la característica de supervisión devuelve una lista de las áreas de trabajo de MED-V en las que se produjo un error en la configuración de la primera vez, que puede usar para tomar las medidas adecuadas para resolver el error.

## Temas relacionados


[Áreas de trabajo de monitor MED-V](monitor-med-v-workspaces.md)

[Cómo comprobar la configuración de instalación de primera vez](how-to-verify-first-time-setup-settings.md)

 

 





