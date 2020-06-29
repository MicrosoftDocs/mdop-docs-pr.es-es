---
title: Cómo instalar el secuenciador
description: Cómo instalar el secuenciador
author: dansimp
ms.assetid: 5e8f1696-9bc0-4f44-8cb7-b809b2daae10
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b72330718a14cb8ffb0e582c946ff1e70539036c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813966"
---
# Cómo instalar el secuenciador


Use el siguiente procedimiento para instalar el secuenciador de Microsoft Application Virtualization (App-V) 5,1. El equipo que ejecutará el secuenciador no debe estar ejecutando ninguna versión del cliente de App-V 5,1.

No se admite la actualización de una instalación anterior de App-V Sequencer.

**Importante**  Para obtener una lista completa de los requisitos del secuenciador consulte las secciones SPRJ de los [requisitos previos de App-v 5,1](app-v-51-prerequisites.md) y las [configuraciones compatibles de app-v 5,1](app-v-51-supported-configurations.md).

 

También puede usar la línea de comandos para instalar el secuenciador de App-V 5,1. En la siguiente lista se muestra información sobre las opciones para instalar el secuenciador con la línea de comandos y **appv\_sequencer\_setup.exe**:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Comando</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/INSTALLDIR</p></td>
<td align="left"><p>Especifica el directorio de instalación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/CEIPOPTIN</p></td>
<td align="left"><p>Permite participar en el programa para la mejora de la experiencia del usuario de Microsoft.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Log</p></td>
<td align="left"><p>Especifica dónde se guardará el registro de instalación, la ubicación predeterminada es <strong> % temp% </strong> . Por ejemplo, <strong> C:\ Registra \ log. log </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>q</p></td>
<td align="left"><p>Especifica una instalación silenciosa o silenciosa.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/Uninstall</p></td>
<td align="left"><p>Especifica la eliminación del secuenciador.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/ACCEPTEULA</p></td>
<td align="left"><p>Acepta el contrato de licencia. Esto es necesario para una instalación desatendida. Ejemplo de uso: <strong> /ACCEPTEULA </strong> o <strong> /ACCEPTEULA = 1 </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/LAYOUT</p></td>
<td align="left"><p>Especifica la acción de diseño asociada. También extrae los archivos de Windows Installer (. msi) y de script a una carpeta sin instalar App-V 5,1. No se espera ningún valor.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/LAYOUTDIR</p></td>
<td align="left"><p>Especifica el directorio de diseño. Requiere un valor de cadena. Ejemplo de uso: <strong> /LAYOUTDIR = "cliente de virtualización de C:\Application" </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/? O/h o/Help</p></td>
<td align="left"><p>Muestra la ayuda asociada.</p></td>
</tr>
</tbody>
</table>

 

**Para instalar el secuenciador de 5,1 de App-V**

1.  Copie los archivos de instalación de App-V 5,1 SPRJ en el equipo en el que se instalará. Haga doble clic en **appv\_sequencer\_setup.exe** y, después, haga clic en **instalar**.

2.  En la página de **términos de licencia del software** , debe revisar los términos de licencia. Para aceptar los términos de licencia, seleccione **acepto los términos de licencia.** Haz clic en **Siguiente**.

3.  En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).** Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**. Haz clic en **Siguiente**.

4.  En la página programa para la mejora de la **experiencia del usuario** , para participar en el programa, seleccione **unirse al programa para la mejora de la experiencia del usuario**. Esto le permitirá recopilar información sobre cómo está usando App-V 5,1. Si no desea participar en el programa, seleccione **no deseo incorporarme al programa en este momento**. Haz clic en **Instalar**.

5.  Para abrir el secuenciador, haga clic en **Inicio** y, a continuación, en **Microsoft Application Virtualization Sequencer**.

**Para solucionar problemas de la instalación de App-V 5,1 Sequencer**

-   Para obtener más información acerca de la instalación del secuenciador, puede ver el registro de errores en la carpeta **% temp%** . Para revisar los archivos de registro, haga clic en **Inicio**, escriba **% temp%** y, a continuación, busque el **registro appv\_**.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Planificación de la implementación de App-V](planning-to-deploy-app-v51.md)

 

 





