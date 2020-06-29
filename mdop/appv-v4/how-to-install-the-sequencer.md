---
title: Cómo instalar el secuenciador
description: Cómo instalar el secuenciador
author: dansimp
ms.assetid: 2cd16427-a0ba-4870-82d1-3e3c79e1959b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 75a0f987fcc76d1ed92631085a4364ae6e06c9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817270"
---
# Cómo instalar el secuenciador


El secuenciador de Microsoft Application Virtualization (App-V) supervisa y registra el proceso de instalación y configuración de las aplicaciones para que la aplicación se pueda ejecutar como una aplicación virtual. Debe instalar el secuenciador en un equipo que solo tenga instalado el sistema operativo. Como alternativa, puede instalar el secuenciador en un equipo que ejecute un entorno virtual, por ejemplo, Microsoft Virtual PC. Este método es útil porque es más fácil mantener un entorno de secuenciación limpio que se puede volver a usar con una configuración adicional mínima.

Debe tener derechos administrativos en el equipo que está usando para secuenciar la aplicación y el equipo debe estar conectado a la red. El equipo no debe estar ejecutando ninguna versión del cliente de Application Virtualization (App-V). Crear una aplicación virtual con el secuenciador es muy intensivo de recursos, por lo que es importante que instale el secuenciador en un equipo que cumpla o supere los requisitos recomendados. Para obtener más información sobre los requisitos del sistema, consulte [los requisitos de software y hardware del secuenciador](sequencer-hardware-and-software-requirements.md)..

**Para instalar Microsoft Application Virtualization Sequencer**

1.  Copie los archivos de instalación de Microsoft Application Virtualization Sequencer en el equipo en el que desea instalarlo.

2.  Para iniciar el Asistente para la instalación de Microsoft Application Virtualization Sequencer, seleccione **setup.exe**. Si el **paquete redistribuible de Microsoft Visual C++ SP1 (x86)** no se detecta antes de la instalación, **setup.exe** lo instalará.

3.  En la página **principal** , haga clic en **siguiente**.

4.  En la página **contrato de licencia** , para aceptar las condiciones del contrato de licencia, seleccione Acepto **las condiciones del contrato de licencia**. Haz clic en **Siguiente**.

5.  En la página **carpeta de destino** , para aceptar la carpeta de instalación predeterminada, haga clic en **siguiente**. Para especificar otra carpeta de destino, haga clic en **cambiar** y especifique la carpeta de instalación que se usará para la instalación. Haz clic en **Siguiente**.

6.  En la página **listo para instalar el programa** , para iniciar la instalación, haga clic en **instalar**.

7.  En la página **completado del asistente InstallShield** , para cerrar el Asistente de instalación y abrir el secuenciador, haga clic en **Finalizar**. Para cerrar el Asistente de instalación sin abrir el secuenciador, anule la selección de **iniciar el programa** y haga clic en **Finalizar**.

## Temas relacionados


[Configuración del secuenciador de virtualización de aplicaciones](configuring-the-application-virtualization-sequencer.md)

 

 





