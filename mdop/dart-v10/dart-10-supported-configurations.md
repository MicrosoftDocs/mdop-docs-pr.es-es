---
title: Configuraciones admitidas de DaRT 10
description: Configuraciones admitidas de DaRT 10
author: dansimp
ms.assetid: a07d6562-1fa9-499f-829c-9cc487ede0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 414b9d5cb7bf78dcfeda3fafc1c476e367709446
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813135"
---
# Configuraciones admitidas de DaRT 10


En este tema, se especifica el software necesario y los requisitos de configuración admitidos para instalar y ejecutar Microsoft Diagnostics and Recovery Toolset (DaRT) 10 en su entorno. Se especifican los requisitos del sistema operativo y los requisitos del sistema necesarios para ejecutar DaRT 10. Para obtener información sobre los requisitos previos que debe considerar para crear la imagen de recuperación de DaRT, consulte [planificación para crear la imagen de recuperación de DART 10](planning-to-create-the-dart-10-recovery-image.md).

Para obtener información sobre las configuraciones compatibles que se aplican a versiones posteriores, consulte la documentación de la versión correspondiente.

Puede instalar DaRT de una de estas dos maneras. Puede instalar toda la funcionalidad en un equipo de administrador de ti, donde llevará a cabo todas las tareas asociadas con la ejecución de DaRT. Como alternativa, puede instalar, en el PC administrador, solo la funcionalidad de DaRT que crea la imagen de recuperación y luego instalar la funcionalidad usada para ejecutar DaRT (es decir, el visor de conexión remota de DaRT) en un equipo de asistencia.

## Software de prerrequisito de DaRT 10


Asegúrese de que se cumplan los siguientes requisitos previos antes de instalar DaRT.

### Requisitos previos del equipo de administrador

En la siguiente tabla se enumeran los requisitos previos de instalación para el equipo administrador cuando está instalando DaRT 10 y todas las herramientas de DaRT.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Como requisito previo</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Kit de desarrollo y evaluación de Windows (ADK)</strong></p></td>
<td align="left"><p>Requerido para el Asistente de imagen de recuperación de DaRT. Contiene las herramientas de implementación, que se usan para personalizar, implementar y atender imágenes de Windows, y contiene el entorno de preinstalación de Windows (Windows PE). El ADK no es necesario si instalas solo el visor de conexión remota o el analizador de bloqueo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Kit de desarrollo de Windows o kit de desarrollo de software (opcional)</strong></p></td>
<td align="left"><p>Crash Analyzer requiere que las herramientas de depuración de Windows 10 del kit de controladores de Windows analicen los archivos de volcado de memoria.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Imagen ISO de 10 64 o 32 bits de Windows</strong></p></td>
<td align="left"><p>DaRT requiere la imagen del entorno de recuperación de Windows (Windows RE) de Windows 10 media. Descargue la versión de 32 bits o de 64 bits de Windows 10, según el tipo de imagen de recuperación de DaRT que desee crear. Si admite ambos tipos de sistema en su entorno, descargue ambas versiones de Windows 10.</p></td>
</tr>
</tbody>
</table>

 

### Requisitos previos del equipo del servicio de asistencia

En la siguiente tabla se enumeran los requisitos previos de instalación para el equipo de asistencia al usuario cuando se ejecuta el visor de conexión remota de DaRT 10.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Como requisito previo</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Visor de conexión remota de DaRT 10</strong></p></td>
<td align="left"><p>Debe instalarse en un sistema operativo Windows 10.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Herramientas de depuración para Windows</strong></p></td>
<td align="left"><p>Solo es necesario si instalas la herramienta analizador de bloqueo</p></td>
</tr>
</tbody>
</table>

 

### Requisitos previos de equipos del usuario final

No hay ningún software previo que deba instalarse en los equipos de los usuarios finales, excepto en el sistema operativo Windows 10.

## <a href="" id="---------dart-10-operating-system-requirements"></a> Requisitos del sistema operativo DaRT 10


### Requisitos del sistema para el equipo del administrador

En la siguiente tabla se enumeran los sistemas operativos que se admiten para la instalación de equipos con DaRT 10 Administrator.

**Nota:**  Asegúrese de asignar espacio suficiente para las herramientas adicionales que quiera instalar en el PC administrador.

 

**Nota:**  Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack inmediatamente anterior. Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)

 

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edición</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
<th align="left">Requisitos del sistema operativo</th>
<th align="left">Requisito de RAM para ejecutar DaRT</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Todas las ediciones</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Todas las ediciones</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="-------------dart-help-desk-computer-system-requirements"></a> Requisitos del sistema para el equipo de asistencia de DaRT

Si permite que un servicio de asistencia pueda solucionar problemas de forma remota, debe tener instalado el visor de conexión remota en el equipo de soporte técnico. De forma opcional, puede instalar la herramienta analizador de bloqueo en el equipo de soporte técnico.

DaRT 10 permite que un trabajador del Departamento de soporte se conecte a un equipo DaRT 10 mediante el visor de conexión remota DaRT 7,0, DaRT 8,0, DaRt 8,1 o DaRT 10. Los visores de conexión remota de DaRT 7,0, DaRT 8,0 y DaRt 8,1 requieren sistemas operativos Windows 7, Windows 8 o Windows 8,1, mientras que el visor de conexión remota de DaRT 10 requiere Windows 10. El visor de conexión remota de DaRT 10 y todas las demás herramientas de DaRT 10 solo se pueden instalar en un equipo con Windows 10.

En la siguiente tabla se enumeran los sistemas operativos que se admiten en la instalación de equipos del Departamento de soporte de DaRT.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edición</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
<th align="left">Requisitos del sistema operativo</th>
<th align="left">Requisitos de RAM para ejecutar DaRT</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Todas las ediciones</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows10 (solo con el visor de conexión remota 10,0)</p></td>
<td align="left"><p>Todas las ediciones</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Todas las ediciones</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows8 (solo con el visor de conexión remota 8,0)</p></td>
<td align="left"><p>Todas las ediciones</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 7 (solo con visor de conexión remota 7,0)</p></td>
<td align="left"><p>Todas las ediciones</p></td>
<td align="left"><p>SP1, SP2</p></td>
<td align="left"><p>64 bits o 32 bits</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>N/D</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Centro de datos Standard, Enterprise</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>1,0 GB</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server2012R2</p></td>
<td align="left"><p>Centro de datos Standard, Enterprise</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>1,0 GB</p></td>
</tr>
</tbody>
</table>

 

DaRT también tiene los siguientes requisitos mínimos de hardware para el equipo del usuario final:

Una unidad de CD o DVD o un puerto USB: solo es necesario si implementas DaRT en tu empresa con un CD, DVD o USB.

Compatibilidad del BIOS para iniciar el equipo desde un CD o DVD, una unidad flash USB o desde una partición remota o de recuperación.

### <a href="" id="-------------dart-10-end-user-computer-system-requirements"></a> Requisitos del sistema para equipos de usuario final DaRT 10

La ventana del conjunto de herramientas de diagnóstico y recuperación en DaRT 10 requiere que el equipo del usuario final use uno de los siguientes sistemas operativos, junto con la cantidad especificada de memoria del sistema disponible para DaRT:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edición</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
<th align="left">Requisitos del sistema operativo</th>
<th align="left">Requisitos de RAM</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Todas las ediciones</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>2 GB</p></td>
<td align="left"><p>2,5 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10</p></td>
<td align="left"><p>Todas las ediciones</p></td>
<td align="left"><p>N/D</p></td>
<td align="left"><p>32 bits</p></td>
<td align="left"><p>1 GB</p></td>
<td align="left"><p>1,5 GB</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Planificación de la implementación de DaRT 10](planning-to-deploy-dart-10.md)

 

 





