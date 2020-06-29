---
title: Cómo modificar los sistemas operativos asociados con un archivo de instalador de Windows existente
description: Cómo modificar los sistemas operativos asociados con un archivo de instalador de Windows existente
author: dansimp
ms.assetid: 0633f7e2-aebf-4e00-be02-35bc59dec420
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63184852f996cbe09b476f456f7c2b509549f4fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816951"
---
# Cómo modificar los sistemas operativos asociados con un archivo de instalador de Windows existente


Use el siguiente procedimiento para modificar las versiones del sistema operativo asociadas a un archivo existente de Windows Installer (**MSI**) que se creó con el secuenciador de App-V.

**Para modificar los sistemas operativos de un archivo de Windows Installer existente**

1.  Instale el secuenciador de App-V en un equipo de su entorno que solo tenga instalado el sistema operativo. Como alternativa, puede instalar el secuenciador en un equipo que ejecute un entorno virtual, por ejemplo, Microsoft Virtual PC. Este método es útil porque es más fácil mantener un entorno de secuenciación limpio que puede reutilizar con una configuración adicional mínima. Para obtener más información sobre cómo instalar el secuenciador de App-V, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer.md).

2.  Copie el paquete de la aplicación virtual completo que contiene el archivo de Windows Installer que desea modificar al equipo que ejecuta el secuenciador.

3.  Para modificar el archivo de Windows Installer, abra la consola del secuenciador, seleccione **paquete**  /  **abierto**y, a continuación, vaya a la ubicación donde se guardó el paquete de aplicación virtual asociado con el archivo de Windows Installer.

4.  Para agregar o quitar sistemas operativos, seleccione la ficha **implementación** en la consola del secuenciador. Para especificar sistemas operativos adicionales que se asociarán con el archivo de Windows Installer, seleccione el sistema operativo que desee y, a continuación, haga clic en la flecha que apunta al control de lista del sistema operativo **seleccionado** .

    Para quitar una asociación de sistema operativo, seleccione el sistema operativo que desee quitar y, a continuación, haga clic en la flecha que apunta al control de lista de sistema operativo **disponible** .

5.  Para crear un nuevo Windows Installer que se asociará con el paquete de la aplicación virtual, seleccione **generar paquete de Microsoft Windows Installer (MSI)**. También puede seleccionar **herramientas**para  /  **crear MSI**.

    **Nota:**  Si selecciona **herramientas** / **crear MSI** para crear un nuevo archivo de Windows Installer, puede omitir el **paso 6** de este procedimiento.

     

6.  Para guardar el paquete de aplicación virtual, **Package**seleccione  /  **Guardar**paquete.

## Temas relacionados


[Tareas del secuenciador de virtualización de aplicaciones](tasks-for-the-application-virtualization-sequencer.md)

 

 





