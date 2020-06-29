---
title: Cómo administrar la redirección de la dirección URL mediante el Empaquetador de área de trabajo de MED-V
description: Cómo administrar la redirección de la dirección URL mediante el Empaquetador de área de trabajo de MED-V
author: dansimp
ms.assetid: 1a8d25af-479f-42d3-bf5f-c7fd974bbf8c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 88167923e3bd47f2a3b0b3ada5e818715740dbe3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824820"
---
# Cómo administrar la redirección de la dirección URL mediante el Empaquetador de área de trabajo de MED-V


Puede usar el Empaquetador de área de trabajo de MED-V para administrar el redireccionamiento de direcciones URL en el área de trabajo de MED-V.

**Para administrar el redireccionamiento de direcciones web en un área de trabajo de MED-V**

1.  Para abrir el **Empaquetador de área de trabajo de MED-V**, haga clic en **Inicio**, haga clic en **todos los programas**, en **Microsoft Enterprise Desktop Virtualization**y, a continuación, haga clic en **Empaquetador de área de trabajo de MED-V**.

2.  En el panel principal de **empaquetador del área de trabajo de MED-V** , haga clic en **administrar redireccionamiento web**.

3.  En la ventana **administrar redireccionamiento web** , puede escribir, pegar o importar una lista de las direcciones URL que se redirigen a Internet Explorer en el área de trabajo de MED-V.

    **Nota**  
    El redireccionamiento de direcciones URL en MED-V solo admite los protocolos HTTP y HTTPS. MED-V no proporciona soporte técnico para FTP ni para otros protocolos.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. Haga clic en **Guardar como...** para guardar los archivos de redireccionamiento de URL actualizados en la carpeta especificada. MED-V crea un archivo de registro que contiene la información de redireccionamiento de la dirección URL actualizada. Implemente la clave del registro actualizada con la Directiva de grupo. Para obtener más información acerca de cómo usar la Directiva de grupo, consulte [instalación de software de directiva de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

   MED-V también crea un script de Windows PowerShell en la carpeta especificada que puede usar para volver a crear el paquete de área de trabajo de MED-V actualizado.

## Temas relacionados


[Cómo agregar o quitar la información de redireccionamiento de dirección URL en un área de trabajo de MED-V implementada](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[Administrar la redirección de la dirección URL de MED-V](manage-med-v-url-redirection.md)









