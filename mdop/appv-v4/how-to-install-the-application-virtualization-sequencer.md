---
title: Cómo instalar el secuenciador de virtualización de aplicaciones
description: Cómo instalar el secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 89cdf60d-18b0-4204-aa9f-b402610f8f0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a6fe03f2149504b6c34c70b2b82ce2ba0b55ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817310"
---
# Cómo instalar el secuenciador de virtualización de aplicaciones


Microsoft Application Virtualization SPRJ supervisa y registra el proceso de instalación y configuración de las aplicaciones para que la aplicación se pueda ejecutar como una aplicación virtual. Debe instalar el secuenciador en un equipo que solo tenga instalado el sistema operativo. Como alternativa, puede instalar el secuenciador en un equipo que ejecute un entorno virtual, por ejemplo, Microsoft Virtual PC. Este método es útil porque es más fácil mantener un entorno de secuenciación limpio que se puede volver a usar con una configuración adicional mínima.

Debe tener derechos administrativos en el equipo que está usando para secuenciar la aplicación y el equipo no debe estar ejecutando ninguna versión del cliente de Application Virtualization (App-V). Crear una aplicación virtual mediante el secuenciador es muy intensivo de recursos, por lo que es importante que instale el secuenciador en un equipo que cumpla o supere los requisitos recomendados. No se admite la ejecución del secuenciador de App-V en el modo seguro. Para obtener más información sobre los requisitos del sistema, consulte [requisitos del sistema de Application Virtualization](application-virtualization-system-requirements.md).

**Importante**  Una vez que haya realizado la secuencia de una aplicación, antes de que pueda secuenciar correctamente una nueva aplicación, debe reinstalar el sistema operativo y el secuenciador en el equipo que está usando para secuenciar las aplicaciones.

 

**Para instalar Microsoft Application Virtualization Sequencer**

1.  Copie los archivos de instalación de Microsoft Application Virtualization Sequencer en el equipo en el que desea instalarlo.

2.  Para iniciar el Asistente para la instalación de Microsoft Application Virtualization Sequencer, seleccione **setup.exe**. Si el **paquete redistribuible de Microsoft Visual C++ SP1 (x86)** no se detecta antes de la instalación, **setup.exe** lo instalará.

3.  En la página **principal** , haga clic en **siguiente**.

4.  En la página **contrato de licencia** , para aceptar las condiciones del contrato de licencia, seleccione Acepto **las condiciones del contrato de licencia**. Haz clic en **Siguiente**.

5.  En la página **carpeta de destino** , para aceptar la carpeta de instalación predeterminada, haga clic en **siguiente**. Para especificar otra carpeta de destino, haga clic en **cambiar** y especifique la carpeta de instalación que se usará para la instalación. Haz clic en **Siguiente**.

6.  En la página **listo para instalar el programa** , para iniciar la instalación, haga clic en **instalar**.

7.  En la página **completado del asistente InstallShield** , para cerrar el Asistente de instalación y abrir el secuenciador, haga clic en **Finalizar**. Para cerrar el Asistente de instalación sin abrir el secuenciador, anule la selección de **iniciar el programa** y haga clic en **Finalizar**.

## Temas relacionados


[Cómo actualizar el cliente secuenciador de virtualización de aplicaciones](how-to-upgrade-the-application-virtualization-sequencer.md)

[Requisitos de implementación de virtualización de aplicaciones](application-virtualization-deployment-requirements.md)

 

 





