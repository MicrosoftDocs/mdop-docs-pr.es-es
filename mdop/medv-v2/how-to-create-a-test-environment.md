---
title: Cómo crear un entorno de prueba
description: Cómo crear un entorno de prueba
author: dansimp
ms.assetid: a0db2299-16f3-4516-8769-7d55ca4a1e98
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ee2ab131f6003b56cce7a60ffea1cd00b067fae3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827290"
---
# Cómo crear un entorno de prueba


A continuación se muestran algunos pasos e instrucciones para ayudarle a crear un entorno de prueba que pueda usar para probar el paquete de área de trabajo MED-V localmente antes de implementarlo en toda la empresa. Esta sección proporciona instrucciones sobre cómo crear un entorno de prueba, ya sea de forma manual o mediante un sistema electrónico de distribución de software.

**Para crear un entorno de prueba con un ESD**

1.  Use el método de su empresa para implementar software en toda la empresa para implementar los siguientes componentes necesarios en un equipo de prueba. Instálelos en el siguiente orden:

    -   **Windows Virtual PC** : Si aún no está instalado. Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).

    -   **Adiciones y actualizaciones de Windows Virtual PC**: Si aún no están instaladas. Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).

    -   **Archivo de instalación del agente de host Med-v** : instala el agente de host (MED-v \ _HostAgent \ _setup archivo de instalación). Para obtener más información, vea [Cómo instalar manualmente el agente de host MED-V](how-to-manually-install-the-med-v-host-agent.md).

    -   **Instalador de área de trabajo de Med-v, VHD y ejecutable de configuración** : creados en el **Empaquetador de área de trabajo de Med-v**. Para obtener más información, vea [crear un paquete de área de trabajo de MED-V](create-a-med-v-workspace-package.md).

        **Importante**  El VHD y el programa ejecutable de configuración deben estar en la misma carpeta que el instalador del área de trabajo de MED-V. Después, instale el instalador de área de trabajo MED-V ejecutando setup.exe.

         

2.  Una vez que todos los componentes estén instalados en el equipo de prueba, ejecute el agente de host MED-V para iniciar la configuración por primera vez.

    Haga clic en **Inicio**, seleccione **todos los programas**, haga clic en **virtualización de escritorio de Microsoft Enterprise**y, a continuación, haga clic en **agente de host MED-V**.

    **Nota:**  Si no puede ejecutar físicamente el agente de host MED-V en el equipo de prueba, la configuración se iniciará automáticamente la próxima vez que se reinicie el equipo.

     

La configuración comienza por primera vez y puede tardar diez minutos o más en finalizar.

Para obtener información sobre cómo probar las opciones de configuración cuando se ejecuta la primera configuración, consulte [Cómo comprobar la configuración de primera hora](how-to-verify-first-time-setup-settings.md).

**Para crear un entorno de prueba manualmente**

1.  Instale el agente de host MED-V en un entorno de prueba local que incluya requisitos previos de MED-V, como Windows Virtual PC, con adiciones y actualizaciones. Para obtener información, consulte [Cómo instalar manualmente el agente de host MED-V](how-to-manually-install-the-med-v-host-agent.md).

2.  Copie los archivos de área de trabajo de MED-V en el entorno de prueba. Los archivos de área de trabajo de MED-V se encuentran en la carpeta de destino que especificó en el **empaquetador del área de trabajo de Med-v**.

    **Importante**  El VHD y el programa ejecutable de configuración deben estar en la misma carpeta del entorno de prueba que el instalador del área de trabajo de MED-V.

     

3.  Instale el área de trabajo de MED-V ejecutando setup.exe.

4.  Para iniciar la configuración primera, ejecute el agente de host MED-V.

    Haga clic en **Inicio**, seleccione **todos los programas**, haga clic en **virtualización de escritorio de Microsoft Enterprise**y, a continuación, haga clic en **agente de host MED-V**.

La configuración comienza por primera vez y puede tardar varios minutos en completarse, según el tamaño del VHD especificado.

Ya está listo para probar las diferentes configuraciones de configuración, publicación de aplicaciones y redireccionamiento de URL que especificó para el área de trabajo de MED-V.

**Nota:**  De forma predeterminada, MED-V reemplaza la Directiva de bloqueo de pantalla del invitado. Sin embargo, esto no representa un problema de seguridad porque el equipo host sigue respetando la Directiva de bloqueo de pantalla.

 

## Temas relacionados


[Cómo comprobar la configuración de instalación de primera vez](how-to-verify-first-time-setup-settings.md)

[Cómo probar la publicación de aplicaciones](how-to-test-application-publishing.md)

[Cómo comprobar el redireccionamiento de la dirección URL](how-to-test-url-redirection.md)

 

 





