---
title: Lista de exclusión de aplicación de Windows Virtual PC
description: Lista de exclusión de aplicación de Windows Virtual PC
author: dansimp
ms.assetid: 7715f198-f5ed-421e-8740-0cec2ca4ece3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/28/2017
ms.openlocfilehash: 190049ce99865ef237d8d26e14a8279def7da521
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823691"
---
# Lista de exclusión de aplicación de Windows Virtual PC


En algunos casos, es posible que no desee que las aplicaciones instaladas en el área de trabajo de MED-V se publiquen en el menú **Inicio** del equipo host. Puede anular la publicación de estas aplicaciones siguiendo las instrucciones [que encontrará en cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md). Sin embargo, si el programa se actualiza de forma automática, también puede volver a publicarse automáticamente. Esto hace que tenga que volver a publicar la aplicación.

Windows Virtual PC incluye una característica que se denomina "lista de exclusión" que le permite especificar determinadas aplicaciones instaladas que no desea que se publiquen en el menú **Inicio** del host. La "lista de exclusión" se encuentra en el registro de invitados de la clave HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList y enumera las aplicaciones que no se han publicado en el menú **Inicio** de host. Puede pensar en la "lista de exclusión" como en el que se cancela la publicación de las aplicaciones especificadas de forma permanente porque todas las actualizaciones automáticas de las aplicaciones que aparecen en la lista no provocarán que se vuelvan a publicar automáticamente.

## Administración de aplicaciones con la lista de exclusión en Windows Virtual PC


****

1.  Abra el área de trabajo de MED-V en pantalla completa.

    Para obtener información sobre cómo abrir el área de trabajo de MED-V en el modo de pantalla completa con el kit de herramientas de administración de MED-V, vea [Ver configuraciones de áreas de trabajo de Med-v](viewing-med-v-workspace-configurations.md#bkmk-fullscreen). O bien, puede abrirlo manualmente en pantalla completa haciendo clic en **Inicio**, haga clic en **todos los programas**, en **Windows Virtual PC**, en **Windows Virtual PC**y, a continuación, haga doble clic en el área de trabajo de MED-V.

2.  En la ventana del área de trabajo virtual de Windows, abra el editor del registro.

    Haga clic en **Inicio**, haga clic en **Ejecutar**y, a continuación, escriba regedit. A continuación, haga clic en **Aceptar**.

3.  En el editor del registro, busque la clave del registro HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\Virtual Machine\\VPCVAppExcludeList.

4.  Cree un nuevo valor de registro para la aplicación instalada que no desea que se publique en el menú **Inicio** del equipo host. Por ejemplo, si desea anular la publicación del programa publicado automáticamente, Microsoft Silverlight, siga estos pasos:

    1.  Con la clave de registro VPCVAppExcludeList resaltada, haga clic en **Editar**, en **nuevo**y, a continuación, en **valor de cadena**.

    2.  Escriba el nombre del nuevo valor del registro. Por ejemplo, para Microsoft Silverlight, puede escribir sllauncher.exe.

    3.  Haga doble clic en el nuevo valor del registro y escriba los datos del valor.

        Los datos del valor son la ruta de acceso completa del comando cuya publicación desea anular. Puede encontrar la ruta completa haciendo clic con el botón secundario del mouse en el acceso directo en el menú **Inicio** de la aplicación que no desea publicar y, después, haciendo clic en **propiedades**. La ruta completa se muestra en la pestaña **acceso directo** en **destino**.

        Por ejemplo, para el programa Microsoft Silverlight, la ruta de acceso completa puede ser "C:\\Archivos de Programa\\microsoft Silverlight\\4.0.50917.0\\Silverlight.Configuration.exe".

        **Importante**  Si procede, quite las comillas de la ruta de acceso completa al introducirla en el campo valor de datos.

         

5.  Cierre el editor del registro y reinicie la máquina virtual del área de trabajo MED-V.

    La aplicación aún se instala en el área de trabajo de MED-V, pero ahora se ha quitado del menú **Inicio** del equipo host.

También puede volver a publicar una aplicación excluida en el menú de **Inicio** de host eliminando el valor correspondiente de la clave VPCVAppExcludeList. Por ejemplo, para volver a publicar Microsoft Silverlight, haga clic con el botón derecho en el valor del registro sllauncher.exe y seleccione **eliminar**.

## Temas relacionados


[Referencia técnica de MED-V](technical-reference-for-med-v.md)

[Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V](how-to-publish-and-unpublish-an-application-on-the-med-v-workspace.md)

 

 





