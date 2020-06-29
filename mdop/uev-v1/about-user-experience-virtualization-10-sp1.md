---
title: Acerca de la virtualización de experiencia del usuario 1.0 SP1
description: Acerca de la virtualización de experiencia del usuario 1.0 SP1
author: dansimp
ms.assetid: 0212d3fb-e882-476c-9496-9eb52301703d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a480ac5d4f4083fc15a724b7cc79390b0caef14
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826891"
---
# Acerca de la virtualización de experiencia del usuario 1.0 SP1


Microsoft User Experience Virtualization (UE-V) 1,0 Service Pack 1 cambia la versión de 1.0.414 a 1.0.520. Cuando se inicia el agente de UE-V Agent setup.exe o el generador de setup.exe de UE-V, se detectará la necesidad de una actualización y se actualizará el agente o generador de UE-V.

## Idiomas adicionales ahora compatibles


UE-V 1,0 Service Pack 1 proporciona actualizaciones para el agente de UE-V y para el generador de UE-V que admita idiomas adicionales. Todos los idiomas admitidos se instalan cuando se ejecuta el programa de instalación. Los siguientes idiomas están incluidos en UE-V 1 SP1:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">UE-V Agent</th>
<th align="left">UE-V generator</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>Chino simplificado (PRC) zh-CN</p></li>
</ul>
<ul>
<li><p>Chino tradicional-Taiwán zh-TW</p></li>
</ul>
<ul>
<li><p>Checo (República Checa) CS-CZ</p></li>
</ul>
<ul>
<li><p>Danés (Dinamarca) da-DK</p></li>
</ul>
<ul>
<li><p>Neerlandés (Países Bajos) nl-NL</p></li>
</ul>
<ul>
<li><p>Finés (Finlandia) fi-FI</p></li>
</ul>
<ul>
<li><p>Francés (Francia) fr-FR</p></li>
</ul>
<ul>
<li><p>Alemán (Alemania) de-DE</p></li>
</ul>
<ul>
<li><p>Griego (Grecia) el-GR</p></li>
</ul>
<ul>
<li><p>Húngaro (Hungría) Hu-HU</p></li>
</ul>
<ul>
<li><p>Italiano (Italia) ti</p></li>
</ul>
<ul>
<li><p>Japonés (Japón) ja-JP</p></li>
</ul>
<ul>
<li><p>Coreano ko-KR</p></li>
</ul>
<ul>
<li><p>Noruego-Noruega Bokmal NB-NO</p></li>
</ul>
<ul>
<li><p>Polaco (Polonia) PL: PL</p></li>
</ul>
<ul>
<li><p>Portugués (Brasil) pt-BR</p></li>
</ul>
<ul>
<li><p>Portugués (Portugal) pt-PT</p></li>
</ul>
<ul>
<li><p>Ruso (Rusia) ru-RU</p></li>
</ul>
<ul>
<li><p>República Eslovaca (Eslovaquia) SK-SK</p></li>
</ul>
<ul>
<li><p>Esloveno (Eslovenia) SL-SL</p></li>
</ul>
<ul>
<li><p>Español, alfabetización Internacional (España) es-ES</p></li>
</ul>
<ul>
<li><p>Sueco (Suecia) VP-SE</p></li>
</ul>
<ul>
<li><p>Turco (Turquía) tr-TR</p></li>
</ul>
<p></p></td>
<td align="left"><ul>
<li><p>Chino simplificado (PRC) zh-CN</p></li>
</ul>
<ul>
<li><p>Chino tradicional-Taiwán zh-TW</p></li>
</ul>
<ul>
<li><p>Francés (Francia) fr-FR</p></li>
</ul>
<ul>
<li><p>Alemán (Alemania) de-DE</p></li>
</ul>
<ul>
<li><p>Italiano (Italia) ti</p></li>
</ul>
<ul>
<li><p>Japonés (Japón) ja-JP</p></li>
</ul>
<ul>
<li><p>Coreano ko-KR</p></li>
</ul>
<ul>
<li><p>Portugués (Brasil) pt-BR</p></li>
</ul>
<ul>
<li><p>Ruso (Rusia) ru-RU</p></li>
</ul>
<ul>
<li><p>Español, alfabetización Internacional (España) es-ES</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Importante**  Mientras el programa de instalación de UE-V Agent (AgentSetup.exe) y el programa de instalación de UE-V Generator (ToolSetup.exe) se traducen a los idiomas anteriores, los archivos de Windows Installer (. msi) solo están disponibles en inglés.

 

## Plantillas de ubicación de configuración de Office 2007


El software de instalación de UE-V Agent instala el agente y registra un grupo predeterminado de plantillas de ubicación de configuración para las aplicaciones comunes de Microsoft. Microsoft Office 2007 ahora forma parte de estas aplicaciones. Hay dos plantillas de Office 2007: MicrosoftOffice2007.xml y MicrosoftCommunicator2007.xml. Estas plantillas de ubicación de configuración capturan la configuración de captura en Microsoft Office 2007 para las siguientes aplicaciones:

-   Microsoft Access 2007

-   Microsoft Communicator 2007

-   Microsoft Excel 2007

-   Microsoft InfoPath 2007

-   Microsoft OneNote 2007

-   Microsoft Outlook 2007

-   Microsoft PowerPoint 2007

-   Microsoft Project 2007

-   Microsoft Publisher 2007

-   Microsoft SharePoint Designer 2007

-   Microsoft Visio 2007

-   Microsoft Word 2007

### Actualizaciones de plantillas de ubicación de configuración de Office 2010

También se ha realizado una actualización de las plantillas de ubicación de configuración. Estos cambios incluyen:

-   Se ha agregado compatibilidad con Microsoft SharePoint Designer 2010 agregando una nueva plantilla a las plantillas de Office 2010 (MicrosoftOffice2010Win32.xml y MicrosoftOffice2010Win64.xml)

-   Correcciones de errores menores, como personalizar la barra de estado (Word, Excel y PowerPoint)

## La tarea programada para las actualizaciones de catálogos ahora está aleatoria


La tarea de actualización automática de la plantilla comprueba el catálogo de plantillas de configuración para las plantillas nuevas, actualizadas o eliminadas. Esta tarea solo se ejecuta si el SettingsTemplateCatalog está configurado. La tarea actualización automática de plantilla ejecuta el ApplySettingsCatalog.exe archivo, que se encuentra en el directorio de instalación de UE-V Agent y con UE-V SP1 se ha cambiado para aleatorizar la actualización durante un período de una hora.

## Compatibilidad con Citrix EdgeSight


Se detectó un conflicto con UE-V ejecutándose en un servidor con Citrix EdgeSight. UE-V 1,0 SP1 resuelve este problema.

## Indización de favoritos de Internet Explorer


Cuando UE-V mueve los favoritos de Internet Explorer de un equipo a otro, la indexación de las direcciones favoritas de la barra de direcciones en el equipo sincronizado se actualiza. Cuando un usuario escribe en la barra de direcciones, los favoritos móviles ahora aparecen como resultado de búsqueda disponible en los equipos sincronizados.

## Nuevos parámetros de línea de comandos de setup.exe para el agente de UE-V Agent y UE-V generator


Con el lanzamiento de UE-V 1,0 SP1, los setup.exe para el agente de UE-V y para el generador de UE-V se han actualizado para permitir los siguientes parámetros de línea de comandos adicionales:

1.  `CEIPENABLED` : Permite que el programa de instalación acepte la opción que se va a incluir en el programa para la mejora de la experiencia del usuario de Microsoft.

2.  `INSTALLFOLDER` : Permite establecer una carpeta de instalación diferente para el agente o generador.

3.  `MUENABLED` : Permite que el programa de instalación acepte la opción que se va a incluir en el programa Microsoft Update.

## Nuevos códigos de error para la configuración


Al ejecutar la configuración de UE-V para UE-V Agent (AgentSetup.exe), se pueden ver los siguientes códigos devueltos en el registro de instalación "/log &lt;log.txt" &gt; .

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>,0</p></td>
<td align="left"><p>La configuración se completó correctamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>1</p></td>
<td align="left"><p>Se usó una versión anterior de UE-V para intentar desinstalarla. Para desinstalar UE-V, use la misma versión de UE-V que usó para instalar.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>2</p></td>
<td align="left"><p>Se usó una versión más reciente de UE-V para desinstalar. Para desinstalar UE-V, use la misma versión de UE-V que usó para instalar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>cuatro</p></td>
<td align="left"><p>Error inesperado del programa de instalación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>4</p></td>
<td align="left"><p>La versión completa de UE-V no se puede instalar en la parte superior de la versión de prueba (evaluación). Desinstale la versión de prueba e inténtelo de nuevo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>6</p></td>
<td align="left"><p>Error inesperado durante la instalación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>siete</p></td>
<td align="left"><p>No se encontró .NET 3,5 Framework en un equipo con Windows 7 o Windows Server2008 R2.</p></td>
</tr>
<tr class="even">
<td align="left"><p>4,8</p></td>
<td align="left"><p>La característica archivos sin conexión no está habilitada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>99,999</p></td>
<td align="left"><p>El programa de instalación de UE-V no puede determinar si UE-V ya está instalado o se produjo un error en el archivo de configuración.</p></td>
</tr>
</tbody>
</table>

 

 

 





