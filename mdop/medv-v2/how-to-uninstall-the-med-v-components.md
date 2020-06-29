---
title: Cómo desinstalar los componentes de MED-V
description: Cómo desinstalar los componentes de MED-V
author: dansimp
ms.assetid: c121dd27-6b2f-4d41-a21a-c6e8608c5c41
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 514ec8227b858b34289ca2330f7cfb038bc4f00e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813030"
---
# Cómo desinstalar los componentes de MED-V


En determinadas circunstancias, es posible que desee desinstalar todos o parte de los componentes de virtualización de Microsoft Enterprise Desktop (MED-V) 2,0 de su empresa. Por ejemplo, se han resuelto todos los problemas de compatibilidad con el sistema operativo de la aplicación o se desea implementar un área de trabajo de MED-V diferente en la empresa.

Normalmente, puede configurar su sistema de distribución electrónica de software (ESD) para desinstalar los componentes de MED-V con un instalador basado en Windows. Como alternativa, puede desinstalar manualmente todos o algunos componentes de MED-V.

**Importante**  Antes de desinstalar el agente de host MED-V, primero debe desinstalar cualquier área de trabajo de MED-V instalada.

 

Use los procedimientos siguientes para desinstalar los componentes de MED-V de su empresa.

**Para desinstalar MED-V mediante un sistema electrónico de distribución de software**

1.  Use su sistema ESD para distribuir un script que invoque el programa ejecutable de uninstall.exe para cada área de trabajo de MED-V que desee desinstalar. El archivo se encuentra en C:\\ProgramData\\Microsoft\\Medv\\Workspace. Puede establecer una marca para ejecutar el programa ejecutable para la desinstalación en modo silencioso, de modo que los usuarios finales no sean conscientes de la desinstalación.

2.  Cree un paquete para distribuir el archivo de instalación del agente de host MED-V a cada equipo en el que se haya desinstalado un área de trabajo de MED-V. Configure el paquete para que ejecute la desinstalación en modo silencioso.

El cliente ESD reconoce cuando los nuevos paquetes están disponibles y comienza a desinstalar los paquetes según la definición y los requisitos.

**Para desinstalar manualmente un área de trabajo de MED-V**

1.  En el equipo host, haga clic en **Inicio**, haga clic en **Panel de control**y, a continuación, haga clic en **programas y características**.

2.  En la ventana **programas y características** , seleccione el área de trabajo de MED-V que desee quitar y, a continuación, haga clic en **desinstalar**. (El área de trabajo de MED-V se denomina "área de trabajo MED-V"- &lt; *área de trabajo \ _name* &gt; "). &lt;Se abrirá el *área de trabajo \ _name* &gt; **Asistente de configuración** .

3.  En el **Asistente de configuración**, haga clic en **siguiente**y, a continuación, en **quitar**.

4.  Si lo prefiere, active la casilla para eliminar el disco principal de VHD y los discos de diferenciación creados por MED-V. Esto no es necesario, pero libera espacio en el disco después de que finalice la desinstalación.

5.  Haga clic en **quitar**.

    **Nota:**  Si se está ejecutando MED-V, aparecerá un cuadro de diálogo en el que se le preguntará si desea apagarlo. Haga clic en **sí** para continuar con la desinstalación. Haga clic en **no** para cancelar la desinstalación.

     

Como alternativa, puede quitar un área de trabajo de MED-V ejecutando el `uninstall.exe` archivo, que normalmente se encuentra en C:\\ProgramData\\Microsoft\\Medv\\Workspace.

**Para desinstalar manualmente el agente de host MED-V**

1.  En el equipo host de Windows 7, haga clic en **Inicio**, haga clic en **Panel de control**y, a continuación, haga clic en **programas y características**.

2.  En la ventana **programas y características** , seleccione **agente de host MED-V**y, a continuación, haga clic en **desinstalar**.

    Windows Installer quita el agente de host MED-V.

    **Nota:**  Si intenta desinstalar el agente de host MED-V antes de desinstalar el área de trabajo MED-V, aparece un cuadro de diálogo que indica que primero debe desinstalar el área de trabajo de MED-V. Haz clic en **Aceptar** para continuar.

     

**Para desinstalar manualmente el empaquetador del área de trabajo de MED-V**

1.  En el equipo host, haga clic en **Inicio**, haga clic en **Panel de control**y, a continuación, haga clic en **programas y características**.

2.  En la ventana **programas y características** , seleccione **Empaquetador de área de trabajo de MED-V**y, a continuación, haga clic en **desinstalar**.

    Windows Installer quita el empaquetador del área de trabajo de MED-V.

    **Nota:**  Puede desinstalar el paquete del área de trabajo de MED-V en cualquier momento sin afectar a las áreas de trabajo de MED-V implementadas.

     

## Temas relacionados


[Implementar los componentes MED-V](deploy-the-med-v-components.md)

 

 





