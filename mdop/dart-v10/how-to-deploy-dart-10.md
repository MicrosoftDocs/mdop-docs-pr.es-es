---
title: Cómo implantar DaRT 10
description: Cómo implantar DaRT 10
author: dansimp
ms.assetid: 13e8ba20-21c3-4870-94ed-6d3106d69f21
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9e78f55e238cce16798525915487e4b753d92e6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813071"
---
# Cómo implantar DaRT 10


En las siguientes instrucciones se explica cómo implementar Microsoft Diagnostics and Recovery Toolset (DaRT) 10 en su entorno. Para obtener el software de DaRT, consulte [Cómo obtener MDOP](https://go.microsoft.com/fwlink/?LinkId=322049). Se supone que está instalando toda la funcionalidad en un equipo de administrador. Si necesita implementar o desinstalar DaRT 10 en varios equipos, mediante un sistema electrónico de distribución de software, por ejemplo, puede que sea más fácil usar las opciones de instalación de la línea de comandos. En esta sección se proporcionan descripciones y ejemplos de las opciones de línea de comandos disponibles.

**Importante**  Antes de instalar DaRT, consulte [configuraciones admitidas de DART 10](dart-10-supported-configurations.md) para asegurarse de que ha instalado todo el software necesario y de que el equipo cumple con los requisitos mínimos del sistema. El equipo en el que instale DaRT debe estar ejecutando Windows 10.

 

Puede instalar DaRT usando una de dos configuraciones distintas:

-   Instale DaRT y todas las herramientas de DaRT en el PC del administrador.

-   Instale en el equipo del administrador solo las herramientas que necesita para crear la imagen de recuperación de DaRT y, a continuación, instale el **visor de conexión remota** y, opcionalmente, **Crash Analyzer** en un equipo de asistencia.

El archivo de instalación de DaRT está disponible en las versiones de 32 y 64 bits. Instale la versión que coincida con la arquitectura del equipo en el que está ejecutando el Asistente para imágenes de recuperación de DaRT, no la arquitectura del equipo de la imagen de recuperación que está creando.

Puede usar cualquiera de las versiones del archivo de instalación de DaRT para crear una imagen de recuperación para equipos de 32 o 64 bits, pero no puede crear una imagen de recuperación para equipos de 32 bits y 64 bits.

**Para instalar DaRT y todas las herramientas de DaRT en un PC administrador**

1.  Descargue la versión de 32 bits o 64 bits del archivo de instalación de DaRT 10. Elija la arquitectura que se corresponda con el equipo en el que está instalando DaRT y ejecute el Asistente para imágenes de recuperación de DaRT.

2.  En la carpeta en la que descargó DaRT 10, ejecute el archivo de instalación **MSDaRT.msi** correspondiente a los requisitos del sistema.

3.  En la página **Asistente para la instalación de DART 10 de Microsoft** , haga clic en **siguiente**.

4.  Acepte los términos de licencia del software de Microsoft y, a continuación, haga clic en **siguiente**.

5.  En la página **Microsoft Update** , seleccione **usar Microsoft Update al buscar actualizaciones**y, a continuación, haga clic en **siguiente**.

6.  En la página **Seleccionar carpeta de instalación** , seleccione una carpeta o haga clic en **siguiente** para instalar DART en la ubicación de instalación predeterminada.

7.  En la página **Opciones de configuración** , seleccione las características de DART que desee instalar o haga clic en **siguiente** para instalar DART con todas las características.

8.  Para iniciar la instalación, haga clic en **instalar**.

9.  Una vez completada la instalación correctamente, haga clic en **Finalizar** para salir del asistente.

## Para instalar DaRT y todas las herramientas de DaRT en un equipo administrador mediante el símbolo del sistema


Al instalar o desinstalar DaRT, tiene la opción de ejecutar los archivos de instalación en el símbolo del sistema. En esta sección se describen algunos ejemplos de las diferentes opciones que puede especificar al instalar o desinstalar DaRT en el símbolo del sistema.

En el ejemplo siguiente se muestra cómo instalar todas las funcionalidades de DaRT.

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, DaRTRecoveryImage,CrashAnalyzer,RemoteViewer 
```

En el siguiente ejemplo se muestra cómo instalar solo el Asistente de imagen de recuperación de DaRT.

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles, ,DaRTRecoveryImage
```

En el ejemplo siguiente se muestra cómo instalar solo el analizador de bloqueo y el visor de conexión remota de DaRT.

``` syntax
msiexec /i MSDaRT.msi ADDLOCAL=CommonFiles,CrashAnalyzer,RemoteViewer 
```

En el ejemplo siguiente se crea un registro de instalación para Windows Installer. Esto es útil para la depuración.

``` syntax
msiexec.exe /i MSDaRT.msi /l*v log.txt 
```

**Nota:**  Puede Agregar/QN o/QB para realizar una instalación silenciosa.

 

**Para validar la instalación de DaRT**

1.  Haga clic en **Inicio**y seleccione **diagnóstico y conjunto de herramientas de recuperación**.

    Se abrirá la ventana **conjunto de herramientas de diagnóstico y recuperación** .

2.  Verifique que todas las herramientas de DaRT que seleccionó para la instalación se instalaron correctamente.

## Temas relacionados


[Implementación de DaRT 10 en equipos de administrador](deploying-dart-10-to-administrator-computers.md)

 

 





