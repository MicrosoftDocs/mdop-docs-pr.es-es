---
title: Identificación del número y los tipos de áreas de trabajo de MED-V
description: Identificación del número y los tipos de áreas de trabajo de MED-V
author: dansimp
ms.assetid: 11642253-6b1f-4c4a-a11e-48d8a360e1ea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e0c9ed4b0ce92d0ca752525b847405bbce90a270
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827261"
---
# Identificación del número y los tipos de áreas de trabajo de MED-V


MED-V crea un entorno virtual para ejecutar aplicaciones que requieren Windows XP o que requieren una versión de Internet Explorer diferente de la de la versión del equipo host. Este entorno virtual se conoce como área de trabajo de MED-V.

En función de los requisitos de compatibilidad de la aplicación a los que se enfrenta la organización al migrar a Windows 7, solo algunos usuarios o departamentos pueden requerir áreas de trabajo de MED-V. Mientras planea la implementación, debe determinar el número de áreas de trabajo de MED-V que necesita su empresa. También debe definir los requisitos de cada área de trabajo de MED-V.

## Identificar el número y los tipos de áreas de trabajo de MED-V


Identifique los equipos y grupos de su empresa para los que va a crear áreas de trabajo de MED-V. Normalmente, estos son los usuarios que requieren acceso a las aplicaciones que no se pueden migrar a Windows 7. Identifique las aplicaciones que no se pueden migrar y los usuarios que necesitan un área de trabajo de MED-V para ejecutar estas aplicaciones.

Es posible que también tenga direcciones de intranet que aún no se hayan optimizado para Windows 7. El área de trabajo de MED-V proporciona un explorador Internet Explorer a través del cual los usuarios finales pueden obtener mejores acceso a las direcciones web que aún no están listas para la migración a Windows 7. Mientras está preparando y planificando su implementación de MED-V, tendrá que identificar y compilar una lista de direcciones URL para redirigir desde Internet Explorer en el equipo host a Internet Explorer en el área de trabajo de MED-V.

Por último, debe evaluar los requisitos de espacio en disco. La mayoría de las áreas de trabajo de MED-V son de 2 gigabytes (GB) o más. El espacio en disco disponible en un sistema se puede consumir rápidamente, según el número de usuarios y la configuración de MED-V. Además, la forma preferida de distribución de su empresa puede requerir espacio adicional. Generalmente, debe liberar un mínimo de 10 GB de espacio en disco para un área de trabajo MED-V, pero esto varía en gran medida según el tamaño de la imagen.

### Calcular los requisitos de espacio en disco para áreas de trabajo de MED-V

Un área de trabajo de MED-V requiere memoria y espacio en disco del equipo host en el que está instalada. Como mínimo, se necesitan 2 GB de espacio en disco en el host. El espacio en disco es variable y depende del número de aplicaciones y de los datos en el área de trabajo de MED-V del usuario.

Le recomendamos un mínimo de 10 GB de espacio en disco para MED-V. Este monto permite un área de trabajo básica de Windows XP y algunas aplicaciones y redireccionamiento web básicos instalados. También proporciona espacio disponible para la unidad de intercambio del host. En una configuración básica, MED-V y un área de trabajo de MED-V implementada ocupan hasta 6 GB. Si incluye una gran cantidad de aplicaciones en el área de trabajo de MED-V o tiene más de un usuario por equipo, puede usar el siguiente cálculo para determinar con mayor precisión el espacio en disco que necesita su área de trabajo de MED-V:

*Base VHD + (usuario por equipo x (diferencia de disco + estado guardado))*

Para calcular el espacio en disco necesario, determine lo siguiente:

-   **Tamaño del VHD base** : el disco duro virtual que se usó para crear el área de trabajo de MED-V.

    **Importante**  No use el tamaño de archivo. medv para el cálculo porque el archivo. medv está comprimido.

     

-   **Usuarios por equipo** : Med-v crea un área de trabajo de Med-v para cada usuario de un equipo; el área de trabajo de MED-V consume espacio en disco cuando cada usuario inicia sesión y se crea el área de trabajo de MED-V.

-   **Tamaño del disco de diferenciación** : se usa para realizar un seguimiento de la diferencia entre el VHD de base. Este tamaño varía a medida que se agregan aplicaciones y actualizaciones de software en el disco duro virtual. Se crea un disco de diferenciación para cada usuario de MED-V cuando inicia MED-V por primera vez.

-   **Tamaño del archivo de estado guardado** : se usa para mantener el estado en la máquina virtual. Por lo general, este es un poco más grande que la memoria RAM asignada para la máquina virtual. Por ejemplo, 1 GB de RAM asignada crea un archivo sobre 1.081.000 KB.

En el ejemplo siguiente se muestra un cálculo basado en tres usuarios de un área de trabajo de MED-V que tiene un disco duro virtual de 2,6 GB:

*2,6 GB + (3 x (1,5 GB + 1 GB)) = 10.1 GB*

**Nota:**  Una práctica recomendada de MED-V es calcular el espacio necesario mediante una implementación de laboratorio para validar los requisitos.

 

### Buscar los archivos para determinar el tamaño de archivo

Las siguientes ubicaciones contienen los archivos de la configuración del usuario y del equipo:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo</th>
<th align="left">Ubicación</th>
<th align="left">Archivos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>VHD base</p></td>
<td align="left"><p>%ProgramData%\Microsoft\Medv\Workspace</p></td>
<td align="left"><p><em>InternalName </em> . vhd: donde <em> InternalName </em> es el nombre del disco duro virtual que seleccionó en el empaquetador del área de trabajo de MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Disco de diferenciación</p></td>
<td align="left"><p>Máquinas%LocalAppData%\Microsoft\MEDV\v2\Virtual</p></td>
<td align="left"><p><em>WorkspaceName </em> . vhd</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Archivo de estado guardado</p></td>
<td align="left"><p>Máquinas%LocalAppData%\Microsoft\MEDV\v2\Virtual</p></td>
<td align="left"><p><em>WorkspaceName </em> . VSV</p></td>
</tr>
</tbody>
</table>

 

### Calcular los requisitos de espacio en disco para áreas de trabajo compartidas de MED-V

Si está calculando una implementación de un área de trabajo de MED-V compartida en un único equipo, el número de usuarios por equipo en el cálculo es siempre "1", ya que MED-V solo configura un único disco de diferenciación para todos los usuarios.

Puede encontrar el disco de diferenciación y el archivo de estado guardado para áreas de trabajo compartidas de MED-V en%ProgramData%\\Microsoft\\Medv\\AllUsers.

## Temas relacionados


[Definir y planificar la implementación de MED-V](define-and-plan-your-med-v-deployment.md)

[Planificación de MED-V](planning-for-med-v.md)

 

 





