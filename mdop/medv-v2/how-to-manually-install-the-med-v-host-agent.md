---
title: Cómo instalar manualmente el agente de host de MED-V
description: Cómo instalar manualmente el agente de host de MED-V
author: dansimp
ms.assetid: 4becc90b-6481-4e1f-a4d3-aec74c8821ec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a7fb44b23a390cf394af2331152955afc2d8eba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812895"
---
# Cómo instalar manualmente el agente de host de MED-V


Existen dos componentes diferentes, pero relacionados, para la solución de virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0: el agente de host MED-V y el agente invitado. El agente de hospedaje reside en el equipo host (el equipo de un usuario que ejecuta Windows 7) y proporciona un canal para comunicarse con el invitado MED-V (la máquina virtual MED-V que se ejecuta en el equipo host). También proporciona ciertas funcionalidades relacionadas con MED-V, como la publicación de aplicaciones.

Normalmente, implementa e instala el agente de host MED-V usando el método preferido de aprovisionamiento de su empresa. Sin embargo, antes de implementar MED-V en toda su empresa, es posible que prefiera instalar el agente de host de forma local para realizar las pruebas. En esta sección se proporcionan instrucciones paso a paso para instalar manualmente el agente de host MED-V.

**Nota:**  El agente invitado MED-V se instala automáticamente durante la configuración de primera vez.

 

**Importante**  Cierre Internet Explorer antes de instalar el agente de host MED-V; de lo contrario, los conflictos pueden producirse posteriormente con el redireccionamiento de URL. También puede hacerlo especificando un reinicio del equipo durante una distribución.

 

**Para instalar el agente de host MED-V**

1.  Ubique los archivos de instalación de MED-V que recibió como parte de la descarga de software.

2.  Haga doble clic en el archivo de instalación MED-V \ _HostAgent \ _Setup.

    Se abre el Asistente de **configuración del agente de host de Microsoft Enterprise Desktop Virtualization (MED-V)** . Haz clic en **Siguiente** para continuar.

3.  Acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente**.

4.  Seleccione la carpeta de destino para instalar el agente de host MED-V. Haz clic en **Siguiente**.

5.  Para comenzar la instalación del agente de host, haga clic en **instalar**.

6.  Una vez completada la instalación correctamente, haga clic en **Finalizar** para cerrar el asistente.

    Para comprobar que la instalación del agente de host se realizó correctamente, haga clic en **Inicio**, haga clic en **todos los programas**, haga clic en **Microsoft Enterprise Desktop Virtualization**y, a continuación, haga clic en **agente de host MED-V**.

**Nota:**  Hasta que se instale un área de trabajo de MED-V, el agente de host MED-V puede iniciarse y ejecutarse, pero no proporciona ninguna funcionalidad.

 

## Temas relacionados


[Cómo implementar los componentes de MED-V a través de un sistema de distribución electrónica de Software](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md)

[Cómo instalar el empaquetador de área de trabajo de MED-V](how-to-install-the-med-v-workspace-packager.md)

[Cómo desinstalar los componentes de MED-V](how-to-uninstall-the-med-v-components.md)

 

 





