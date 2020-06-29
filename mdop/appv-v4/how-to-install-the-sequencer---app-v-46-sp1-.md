---
title: Cómo instalar el secuenciador (App-V 4,6 SP1)
description: Cómo instalar el secuenciador (App-V 4,6 SP1)
author: dansimp
ms.assetid: fe8eb876-28fb-46ae-b592-da055107e639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 611564e861d65dcd357c58732fb60dab21c05abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817271"
---
# Cómo instalar el secuenciador (App-V 4,6 SP1)


El secuenciador de Microsoft Application Virtualization (App-V) supervisa y registra el proceso de instalación y configuración de las aplicaciones para que la aplicación se pueda ejecutar como una aplicación virtual. Debe instalar el secuenciador de App-V en un equipo que solo tenga instalado el sistema operativo. Como alternativa, puede instalar el secuenciador en un equipo que se ejecute en un entorno virtual, por ejemplo, un equipo virtual. Este método es útil porque es más fácil mantener un entorno de secuenciación limpio que puede reutilizar con una configuración adicional mínima.

Debe tener credenciales administrativas en el equipo que está usando para secuenciar la aplicación, y el equipo no debe estar ejecutando ninguna versión de cliente de App-V. La creación de una aplicación virtual mediante el secuenciador de App-V requiere varias operaciones, por lo que es importante que instale el secuenciador en un equipo que cumpla o supere los [requisitos de software y hardware](application-virtualization-sequencer-hardware-and-software-requirements.md)del transformador de Application Virtualization.

**Nota**  
No se admite la ejecución del secuenciador de App-V en el modo seguro.



**Para instalar Microsoft Application Virtualization Sequencer**

1.  Copie los archivos de instalación de Microsoft Application Virtualization Sequencer en el equipo en el que desea instalarlo.

2.  Para iniciar el Asistente para la instalación de Microsoft Application Virtualization Sequencer, haga doble clic en **Setup.exe**. Si el **paquete redistribuible de Microsoft Visual C++ SP1 (x86)** no se detecta antes de la instalación, haga clic en **instalar** para instalar el requisito previo requerido.

3.  Para continuar con la instalación, en la página **principal** , haga clic en **siguiente**.

4.  En la página **contrato de licencia** , para aceptar las condiciones del contrato de licencia, haga clic en Acepto **las condiciones del contrato de licencia**y, a continuación, haga clic en **siguiente**.

5.  En la página **carpeta de destino** , para aceptar la carpeta de instalación predeterminada, haga clic en **siguiente**. Para especificar otra carpeta de destino, haga clic en **cambiar** y especifique la carpeta de instalación que se usará para la instalación. Haz clic en **Siguiente**.

6.  En la página **unidad virtual** , para configurar la unidad predeterminada de Application Virtualization **Q:\\** (predeterminada) como la unidad desde la que se ejecutarán todas las aplicaciones secuenciadas, haga clic en **siguiente**. Si desea especificar una letra de unidad diferente, use la lista y seleccione la letra de unidad que desea usar seleccionando la letra de unidad correspondiente y, a continuación, haga clic en **siguiente**.

    **Importante**  
    La letra de unidad de virtualización de aplicaciones especificada en este paso es la letra de unidad desde la que se ejecutarán las aplicaciones virtuales en los equipos de destino. La letra de unidad especificada debe estar disponible y no está en uso en los equipos que ejecutan el cliente de App-V. Si la unidad especificada ya está en uso, la aplicación virtual falla en el equipo de destino.



7.  En la página **listo para instalar el programa** , para iniciar la instalación, haga clic en **instalar**.

8.  En la página **completado del asistente InstallShield** , para cerrar el Asistente de instalación y abrir el secuenciador de App-V, haga clic en **Finalizar**. Para cerrar el Asistente de instalación sin abrir el secuenciador, desactive **iniciar el programa**y, a continuación, haga clic en **Finalizar**.

    **Nota**  
    Si instaló el secuenciador de App-V en un equipo que ejecuta un entorno virtual, por ejemplo, una máquina virtual, debe tomar una instantánea. Después de secuenciar una aplicación, puede volver a esta imagen, de modo que pueda secuenciar la siguiente aplicación.



~~~
When you uninstall the Sequencer, the following registry keys are not removed from the computer that the Sequencer was installed on. Additionally, you must restart the computer after you have uninstalled the Sequencer so that all associated drivers can be stopped and the operation can be completed.

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard**

-   **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey**
~~~

## Temas relacionados


[Configuración del secuenciador de virtualización de aplicaciones (App-V 4.6 SP1)](configuring-the-application-virtualization-sequencer--app-v-46-sp1-.md)









