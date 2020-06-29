---
title: Cómo implementar manualmente un área de trabajo de MED-V
description: Cómo implementar manualmente un área de trabajo de MED-V
author: dansimp
ms.assetid: 94bfb209-2230-49b6-bb40-9c6ab088dbf4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f13d06e2232681f87df7a71b9a3ef3269b4f9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827280"
---
# Cómo implementar manualmente un área de trabajo de MED-V


En algunos casos, es posible que desee implementar el área de trabajo de MED-V manualmente, por ejemplo, si su empresa no utiliza un sistema electrónico de distribución de software para implementar aplicaciones.

Esta sección proporciona instrucciones sobre cómo implementar manualmente un área de trabajo de MED-V.

**Para implementar un área de trabajo de MED-V manualmente**

1.  Copie todas las aplicaciones necesarias y los archivos de paquete del área de trabajo de MED-V en una unidad compartida o en un DVD. A continuación se muestra una lista de las aplicaciones y archivos necesarios.

    -   **Windows Virtual PC**. Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).

    -   **Adiciones y actualizaciones de Windows Virtual PC**. Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).

    -   **Archivo de instalación del agente de host Med-v** : instala el agente de host (MED-v \ _HostAgent \ _setup archivo de instalación).

        **Advertencia**  
        Cierre Internet Explorer antes de instalar el agente de host MED-V; de lo contrario, los conflictos pueden producirse posteriormente con el redireccionamiento de URL. También puede hacerlo especificando un reinicio del equipo durante una distribución.



~~~
-   **MED-V Workspace Installer, VHD, and Setup Executable** – created with the **MED-V Workspace Packager**. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    **Important**  
    The compressed VHD file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.
~~~



2. Instale lo siguiente en el orden que aparece en la lista. El usuario final puede realizar esta tarea manualmente o puede crear un script para instalar lo siguiente:

   -   Windows Virtual PC y las adiciones y actualizaciones de Virtual PC de Windows. Es necesario reiniciar el equipo.

   -   Agente de host MED-V.

       **Nota**  
       Si se está ejecutando, se debe reiniciar Internet Explorer antes de que finalice la instalación del agente de host MED-V.



~~~
-   The MED-V workspace package.

    Install the MED-V workspace by running the setup.exe program that is included in the MED-V workspace package files.
~~~

3. Completa la configuración de la primera vez.

   Una vez instalado el área de trabajo de MED-V, tiene la opción de iniciar MED-V. Esto inicia el agente de host MED-V. Puede iniciar MED-V en ese momento o iniciar el agente de host MED-V más tarde para completar la configuración de la primera vez.

   Para iniciar el agente de hospedaje de MED-V, haga clic en **Inicio**, haga clic en **todos los programas**, en **Microsoft Enterprise Desktop Virtualization**y, por último, en **agente de host MED-V**.

## Temas relacionados


[Cómo implementar un área de trabajo de MED-V a través de un sistema de distribución electrónica de Software](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

[Cómo implementar un área de trabajo de MED-V en una imagen de Windows 7](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)

[Implementación del paquete del área de trabajo de MED-V](deploying-the-med-v-workspace-package.md)









