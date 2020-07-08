---
title: Cómo implantar DaRT 7.0
description: Cómo implantar DaRT 7.0
author: dansimp
ms.assetid: 30522441-40cb-4eca-99b4-dff758f5c647
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2059b64e5f3ae7af8926bc00e5965598ede4288
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813047"
---
# Cómo implantar DaRT 7.0


Este tema proporciona instrucciones para implementar Microsoft Diagnostics and Recovery Toolset (DaRT) 7 en su entorno. En el primer procedimiento de este tema se supone que está instalando toda la funcionalidad en un equipo de administrador. Cuando necesite implementar o desinstalar DaRT en varios equipos, mediante un sistema electrónico de distribución de software, por ejemplo, puede que sea más fácil usar las opciones de instalación de la línea de comandos. Estas opciones se definen en el segundo procedimiento de este tema, que proporciona el uso de ejemplo para las opciones de línea de comandos disponibles.

**Importante**  Antes de instalar DaRT, asegúrese de que el equipo cumpla con los requisitos mínimos de sistema enumerados en [DaRT 7,0 configuraciones admitidas](dart-70-supported-configurations-dart-7.md).

 

**Para instalar DaRT en un PC administrador**

1.  Ubique los archivos de instalación de DaRT que recibió como parte de la descarga de software.

2.  Haga doble clic en el archivo de instalación de DaRT que corresponde a los requisitos del sistema: 32 o 64 bits. El archivo de instalación de DaRT se denomina **MSDaRT70.msi**.

3.  Acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente**.

4.  Seleccione la carpeta de destino para instalar DaRT, seleccione si DaRT debe instalarse para todos los usuarios o solo para el usuario actual y, a continuación, haga clic en **siguiente**.

5.  Seleccione si la instalación debe ser **típica**, **personalizada**o **completa**y, a continuación, haga clic en **siguiente**.

    -   **Típica** instala las herramientas que se usan con más frecuencia. Se recomienda usar este método para la mayoría de los usuarios.

    -   **Personalizado** le permite seleccionar las herramientas que se instalan y dónde se instalarán. Esto es recomendable para usuarios avanzados, especialmente si está instalando diferentes herramientas de DaRT en diferentes equipos del servicio de asistencia al usuario.

    -   **Completa** : instala todas las herramientas de DART y requiere la mayor parte del espacio en disco.

    Una vez que haya seleccionado el método de instalación, haga clic en **siguiente**.

6.  Para iniciar la instalación, haga clic en **instalar**.

7.  Una vez completada la instalación correctamente, haga clic en **Finalizar** para salir del asistente.

**Para instalar DaRT en el símbolo del sistema**

1.  En el ejemplo siguiente se muestra cómo instalar todas las funcionalidades de DaRT.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
    ```

2.  En el siguiente ejemplo se muestra cómo instalar solo el **Asistente de imagen de recuperación de DART**.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,DaRTRecoveryImage
    ```

3.  En el ejemplo siguiente se muestra cómo instalar solo el analizador de bloqueo y el visor de conexión remota de DaRT.

    ``` syntax
    msiexec /i MSDaRT70.msi ADDLOCAL=CommonFiles,MSDaRTHelp,CrashAnalyzer,RemoteViewer 
    ```

4.  En el ejemplo siguiente se crea un registro de instalación para Windows Installer. Esto es útil para la depuración.

    ``` syntax
    msiexec.exe /i MSDaRT70.msi /l*v log.txt 
    ```

**Nota:**  Puede Agregar/QN o/QB a cualquiera de las opciones del símbolo del sistema de la instalación de DaRT para realizar una instalación silenciosa.

 

## Temas relacionados


[Implementación de DaRT 7.0 en equipos de administrador](deploying-dart-70-to-administrator-computers-dart-7.md)

 

 





