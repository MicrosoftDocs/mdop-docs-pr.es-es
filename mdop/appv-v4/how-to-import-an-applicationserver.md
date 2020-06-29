---
title: Cómo importar una aplicación
description: Cómo importar una aplicación
author: dansimp
ms.assetid: ab40acad-1025-478d-8e13-0e1ff1bd37e4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d9cd6d065ca28b5d856acdae7d10a1280105e9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817401"
---
# Cómo importar una aplicación


Normalmente, las aplicaciones se importan para que estén disponibles para transmitirlas desde un servidor de administración de virtualización de aplicaciones. También puede Agregar una aplicación de forma manual, pero debe proporcionar información precisa y detallada sobre la aplicación para hacerlo. Para obtener más información, consulte [Cómo agregar una aplicación de forma manual](how-to-manually-add-an-application.md).

**Nota:**  Para importar una aplicación, debe tener su archivo de descriptor de software abierto (OSD) secuencial o archivo SPRJ (SPRJ) disponible en el servidor.

 

Al importar una aplicación, debe asegurarse de que el servidor está configurado con un valor en el campo **ruta de contenido predeterminada** en la pestaña **General** del cuadro de diálogo **Opciones del sistema** (accesible haciendo clic con el botón derecho en el nodo **del sistema de virtualización de aplicaciones** en la consola de servidor de App-V). El valor predeterminado de la ruta de contenido define dónde se importarán las aplicaciones y, durante el proceso de importación, este valor se usa para modificar las rutas definidas en el archivo de OSD para el archivo SFT y los accesos directos del icono. En el archivo OSD, la ruta de acceso para el archivo SFT se especifica en la entrada HREF del código base y la ruta de los iconos se especifica en la entrada ACCESOs directos.

Durante el proceso de importación, el protocolo, el servidor y, si está presente, el puerto especificado en estas dos rutas en el archivo OSD se reemplazarán por el valor de la ruta de contenido predeterminada. En la tabla siguiente se muestra un ejemplo de cómo se verá afectada la ruta de acceso a la importación.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ruta de contenido predeterminada</th>
<th align="left">CÓDIGO base de archivo OSD HREF</th>
<th align="left">Valor resultante</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>\server\content &lt; /p&gt;</td>
<td align="left"><p><a href="http://WebServer/myFolder/package.sft" data-raw-source="http://WebServer/myFolder/package.sft">http://WebServer/myFolder/package.sft</a></p></td>
<td align="left"><p>\server\content\myFolder\package.sft</p></td>
</tr>
</tbody>
</table>

 

**Para importar una aplicación**

1.  Haga clic con el botón derecho en el nodo **aplicaciones** en el panel izquierdo y seleccione **importar aplicaciones**.

2.  En el cuadro de diálogo **abrir** , vaya al archivo SPRJ o OSD de la aplicación. Resalte el archivo y haga clic en **abrir**.

3.  En el **Asistente para nueva aplicación**, asegúrese de que el cuadro **habilitado** está seleccionado para las aplicaciones que desea transmitir. También puede escribir una descripción y comprobar las rutas de archivo y el servidor. Además, si ha configurado las licencias y los grupos de servidores, puede seleccionarlos.

4.  Haz clic en **Siguiente**.

5.  En la pantalla **accesos directos publicados** , seleccione las casillas de las ubicaciones en las que desea que aparezcan los accesos directos de la aplicación en los equipos cliente.

6.  Haz clic en **Siguiente**.

7.  En la pantalla **asociaciones de archivos** , puede agregar nuevas asociaciones de archivo a esta aplicación. Para ello, haga clic en **Agregar**, escriba la extensión (sin un punto anterior), escriba una descripción y haga clic en **Aceptar**.

    **Nota:**  Las aplicaciones que se ordenan con el secuenciador 4,0 rellenan el cuadro de diálogo **asociaciones de archivos** al importarlas o crearlas a través de la consola de administración. Las aplicaciones con paquetes de versiones de Sequencer anteriores no.

     

8.  Haz clic en **Siguiente**.

9.  En la pantalla **permisos de acceso** , haga clic en **Agregar**.

10. Complete el cuadro de diálogo **seleccionar grupos** . Cuando termine, haga clic en **Aceptar**.

11. Haz clic en **Siguiente**.

12. En la pantalla **Resumen** , puede revisar la configuración de importación. Haga clic en **Finalizar**, o haga clic en **atrás** para cambiar la importación o haga clic en **Cancelar** para cancelar la importación.

## Temas relacionados


[Cómo administrar grupos de aplicaciones en la consola de administración de servidor](how-to-manage-application-groups-in-the-server-management-console.md)

[Cómo administrar aplicaciones en la consola de administración de servidor](how-to-manage-applications-in-the-server-management-console.md)

[Cómo agregar manualmente una aplicación](how-to-manually-add-an-application.md)

 

 





