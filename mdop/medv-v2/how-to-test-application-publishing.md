---
title: Cómo probar la publicación de aplicaciones
description: Cómo probar la publicación de aplicaciones
author: dansimp
ms.assetid: 17ba2e12-50a0-4f41-8300-f61f09db9f6c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 8dffb4f79ac89c7d419b27640f4f05364bd69e5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826911"
---
# Cómo probar la publicación de aplicaciones


Después de que finalice la prueba de la primera configuración, puede comprobar que la funcionalidad de publicación de la aplicación funciona según lo esperado realizando las siguientes tareas.

<a href="" id="bkmk-apppub"></a>**Para probar la publicación de aplicaciones**

1.  Compruebe que las aplicaciones que especificó para su publicación sean visibles.

    Haga clic en **Inicio** y, después, haga clic en **todos los programas** y busque las aplicaciones especificadas.

    En algunos casos, es posible que la misma aplicación se haya instalado dos veces, una vez en el equipo host y una vez en el invitado. Si una aplicación publicada que tiene el mismo nombre se publica en la misma ubicación en el menú **Inicio** de host, se distingue del acceso directo de la aplicación host agregando el nombre de la máquina virtual al nombre del acceso directo. Por ejemplo, en el caso de una máquina virtual denominada "MEDVHost1", una aplicación host podría ser "Bloc de notas" y una aplicación publicada podría ser "Notepad (MEDVHost1)".

2.  Compruebe que las aplicaciones funcionan como se pretendía.

    En el equipo host, inicie las aplicaciones que publicó y compruebe que se abren en Windows XP SP3 en el invitado. La aplicación debe aparecer en una ventana de estilo Windows XP en el escritorio del equipo host.

3.  Si procede, compruebe que las funciones de redireccionamiento de documentos son las previstas.

    Si una aplicación publicada en el invitado tiene que abrir una carpeta en la unidad del sistema host, asegúrese de que puede abrir la carpeta especificada.

    **Importante**  Dado que Windows Virtual PC no es compatible con la creación de un recurso compartido desde una carpeta que ya está compartida, el redireccionamiento no se realiza en ningún documento que se abra desde una carpeta compartida, como una carpeta Mis documentos ubicada en la red. Para obtener más información, consulte [solución de problemas de operaciones](operations-troubleshooting-medv2.md).

Una vez que haya comprobado que las aplicaciones publicadas están instaladas y funcionan correctamente, puede comprobar si las aplicaciones se pueden agregar o quitar del área de trabajo de MED-V.

**Para comprobar que se puede Agregar o quitar una aplicación**

1.  Agregar o quitar una aplicación del área de trabajo de MED-V.

    Para obtener información sobre cómo agregar y quitar aplicaciones de un área de trabajo de MED-V, consulte [administrar las aplicaciones implementadas en áreas de trabajo de Med-v](managing-applications-deployed-to-med-v-workspaces.md).

2.  Si agregó una aplicación, repita los pasos de [para probar la publicación de aplicaciones](#bkmk-apppub) para comprobar que la nueva aplicación funciona como se pretende.

3.  Si ha quitado una aplicación, haga clic en **Inicio** y, a continuación, haga clic en **todos los programas** y compruebe que las aplicaciones que quitó ya no aparecen en la lista.

**Nota:**  Si tiene algún problema al comprobar la configuración de la publicación de la aplicación, vea [solución de problemas de operaciones](operations-troubleshooting-medv2.md).

Una vez que haya completado las pruebas de publicación de aplicaciones, puede probar otras configuraciones de área de trabajo de MED-V para comprobar que funcionan según lo previsto.

Una vez que haya completado la prueba de su paquete de área de trabajo MED-V y haya comprobado que funciona como se espera, puede implementar el área de trabajo de MED-V en su empresa.

## Temas relacionados

[Cómo comprobar el redireccionamiento de la dirección URL](how-to-test-url-redirection.md)

[Cómo comprobar la configuración de instalación de primera vez](how-to-verify-first-time-setup-settings.md)

[Implementación del paquete del área de trabajo de MED-V](deploying-the-med-v-workspace-package.md)

 

 





