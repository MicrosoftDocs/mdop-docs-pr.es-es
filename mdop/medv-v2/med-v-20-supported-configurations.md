---
title: Configuraciones admitidas de MED-V 2.0
description: Configuraciones admitidas de MED-V 2.0
author: dansimp
ms.assetid: 88f1d232-aa01-45ab-8da7-d086269250b5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0fed090ec04cf67a32b13533f4003c01ae167493
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825220"
---
# Configuraciones admitidas de MED-V 2.0


Su entorno puede cumplir los requisitos de configuración que se proporcionan aquí para que pueda instalar y ejecutar Microsoft Enterprise Desktop Virtualization (MED-V) 2,0. Hemos incluido requisitos como el sistema operativo de host, el espacio en el disco y los requisitos del área de trabajo de MED-V.

## Requisitos del equipo host MED-V 2.0


### Requisitos del sistema operativo del host MED-V 2,0

En la siguiente tabla se enumeran los sistemas operativos que se admiten para la instalación de MED-V 2,0 en el equipo host.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edición</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>Professional, Enterprise o Ultimate</p></td>
<td align="left"><p>Ninguno o SP1</p></td>
<td align="left"><p>x86 o x64</p></td>
</tr>
</tbody>
</table>

 

En la siguiente tabla se enumera la cantidad mínima de RAM requerida para cada sistema operativo compatible con MED-V 2,0.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">RAM mínima requerida</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows7 x86</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows7 x64</p></td>
<td align="left"><p>2 GB</p></td>
</tr>
</tbody>
</table>

 

### Espacio mínimo de disco recomendado

Recomendamos un mínimo de 10 GB de almacenamiento disponible. Sin embargo, el espacio en disco necesario varía enormemente y depende del número de aplicaciones publicadas en el área de trabajo de MED-V.

### <a href="" id="med-v-2-0-host-configuration-"></a>Configuración de host MED-V 2.0

**Versión de .NET Framework**

La versión de .NET Framework 3.5 SP1 de Microsoft .NET Framework es necesaria para MED-V 2,0. Sin embargo, puede instalar .NET Framework 4 o una versión posterior si ya está instalada la versión 3,5 de .NET Framework.

**Motor de virtualización**

PCwith virtual de Windows la revisión que se describe en el artículo 977206 de Microsoft Knowledge base es compatible con MED-V 2,0.

**Explorador de Internet**

Windows Internet Explorer8 y Windows Internet Explorer 9 son compatibles con MED-V 2,0.

**Entornos de servidor de Microsoft**

El agente de hospedaje MED-V y el Empaquetador de área de trabajo MED-V no son compatibles con ningún entorno de servidor.

## Requisitos del área de trabajo de MED-V 2.0


### Requisitos del sistema operativo del área de trabajo MED-V 2,0

En la siguiente tabla se enumeran los sistemas operativos compatibles con las áreas de trabajo de MED-V 2,0.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Sistema operativo</th>
<th align="left">Edición</th>
<th align="left">Service Pack</th>
<th align="left">Arquitectura del sistema</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>WindowsXP</p></td>
<td align="left"><p>Edición profesional</p></td>
<td align="left"><p>SP3</p></td>
<td align="left"><p>x86</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="med-v-2-0-workspace-configuration-"></a>Configuración del área de trabajo MED-V 2.0

**Versión de .NET Framework**

Solo se admite la versión de .NET Framework 3.5 SP1 de Microsoft .NET Framework para la instalación del área de trabajo MED-V 2,0.

**Explorador de Internet**

Windows Internet Explorer6, Windows Internet Explorer7, Windows Internet Explorer8 y Windows Internet Explorer9 son compatibles con la instalación del área de trabajo MED-V 2,0.

### Creación del área de trabajo MED-V 2,0

El disco duro virtual usado para crear un paquete de área de trabajo de MED-V 2,0 debe crearse con Windows Virtual PC.

## Información de globalización de MED-V 2,0


### Información de globalización del agente de hospedaje MED-V 2,0

Las siguientes versiones de idioma del sistema operativo Windows son compatibles con el agente de host MED-V 2,0:

-   Francés

-   Italiano

-   Alemán

-   Español

-   Coreano

-   Japonés

-   Portugués de Brasil

-   Ruso

-   Chino tradicional

-   Chino simplificado

-   Neerlandés

-   Sueco

-   Danés

-   Finés

-   Portugués

-   Noruego

-   Polaco

-   Turco

-   Húngaro

-   Checo

-   Griego

-   Eslovaco

-   Esloveno

### Información de globalización del Empaquetador del área de trabajo MED-V 2,0

Las siguientes versiones de idioma del sistema operativo Windows son compatibles con el Empaquetador de área de trabajo MED-V 2,0:

-   Francés

-   Italiano

-   Alemán

-   Español

-   Coreano

-   Japonés

-   Portugués de Brasil

-   Ruso

-   Chino tradicional

-   Chino simplificado

## Temas relacionados


[Implementación de MED-V](deployment-of-med-v.md)

 

 





