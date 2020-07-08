---
title: Cómo instalar el cliente MED-V y la consola de administración de MED-V
description: Cómo instalar el cliente MED-V y la consola de administración de MED-V
author: dansimp
ms.assetid: 8a5f3010-3a50-487e-99d8-e352e5cb51c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a486cc7cf5534171f80b08dc93742e03cd4a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826981"
---
# Cómo instalar el cliente MED-V y la consola de administración de MED-V


Los siguientes componentes de MED-V se incluyen en el paquete Client. msi:

-   Cliente MED-V: el software MED-V que debe instalarse en los equipos cliente para ejecutar áreas de trabajo de MED-V.

-   Consola de administración MED-V: la herramienta administrativa que los administradores pueden usar para crear y mantener imágenes, áreas de trabajo de MED-V y directivas.

La consola de administración de MED-V y el cliente de MED-V se instalan desde el paquete de cliente MED-V. msi. Sin embargo, el cliente de MED-V puede instalarse independientemente sin la consola de administración de MED-V desactivando la casilla **instalar la aplicación de administración Med-v** durante la instalación.

**Nota**  
El cliente MED-V y la consola de administración de MED-V solo se pueden instalar en equipos basados en Windows 7, Windows Vista y Windows XP. No se pueden instalar en productos de servidor.



**Nota**  
No instale el cliente de MED-V con el comando **runas** de Windows.



**Para instalar el cliente MED-V**

1.  Inicie sesión como usuario con derechos de administrador local en el equipo local.

2.  Ejecute el paquete MED-V. msi.

    El paquete MED-V. msi se llama *MED-V\_x.msi*, donde *x* es el número de versión.

    Por ejemplo, *MED-V\_1.0.65.msi*.

3.  Cuando aparezca la pantalla de **bienvenida del asistente de InstallShield** , haga clic en **siguiente**.

4.  En la pantalla **contrato de licencia** , lea el contrato de licencia, haga clic en Acepto **las condiciones del contrato de licencia**y haga clic en **siguiente**.

    Aparece la pantalla **carpeta de destino** , donde se muestra la carpeta de instalación predeterminada.

    La carpeta de instalación predeterminada es el directorio donde está instalado el sistema operativo.

    -   Para cambiar la carpeta donde debe instalarse MED-V, haga clic en **cambiar**y busque una carpeta existente.

5.  Haz clic en **Siguiente**.

6.  En la pantalla **configuración de Med-v** , configure la instalación de Med-v de la siguiente manera:

    -   Seleccione la casilla **instalar la aplicación de administración de MED-V** para incluir el componente de administración en la instalación.

        **Nota**  
        Los administradores de virtualización de escritorio de empresa deben instalar la aplicación de administración de MED-V. Esta aplicación es necesaria para configurar imágenes de escritorio y áreas de trabajo de MED-V.



~~~
-   Select the **Load MED-V when Windows starts** check box to start MED-V automatically on startup.

-   Select the **Add a MED-V shortcut to my desktop** check box to create a MED-V shortcut on your desktop.

-   In the **Server address** field, type the server address.

-   In the **Server port** field, type the server's port.

-   Select the **Server requires encrypted connections (https)** check box to work with https.

-   The default virtual machine images folder is displayed. The default installation folder is *%systemdrive%\\MED-V Images\\*. To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.
~~~

7. Haz clic en **Siguiente**.

8. En la pantalla **preparado para instalar el programa** , haga clic en **instalar**.

   Se inicia la instalación del cliente de MED-V. Esto puede demorar varios minutos y es posible que no se muestre el texto en la pantalla. Durante la instalación, aparecen varias pantallas de progreso. Si aparece un mensaje, siga las instrucciones proporcionadas.

   Una vez que la instalación se haya realizado correctamente, aparecerá la pantalla **Asistente InstallShield finalizado** .

9. Haga clic en **Finalizar** para cerrar el asistente.

## Temas relacionados


[Configuraciones admitidas](supported-configurationsmedv-orientation.md)

[Listas de comprobación de instalación y actualización](installation-and-upgrade-checklists.md)









