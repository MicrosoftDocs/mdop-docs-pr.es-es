---
title: Cómo abrir una aplicación secuenciada mediante la línea de comandos
description: Cómo abrir una aplicación secuenciada mediante la línea de comandos
author: dansimp
ms.assetid: dc23ee65-8aea-470e-bb3f-a2f2b06cb241
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c99ab6b41947fc255afa9cad5b3ed2e22e672c3e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816920"
---
# Cómo abrir una aplicación secuenciada mediante la línea de comandos


Puede abrir paquetes de aplicaciones virtuales desde la línea de comandos. Debe ejecutar el símbolo del sistema de **cmd** como administrador.

Use el procedimiento siguiente para abrir paquetes de aplicaciones secuenciales con la línea de comandos

**Para abrir una aplicación con secuencia mediante la línea de comandos**

1.  Para abrir el símbolo del sistema, haga clic en **Inicio**, seleccione **Ejecutar**, escriba **cmd**y haga clic en **Aceptar**.

2.  En un símbolo del sistema, escriba **cd\\** y especifique la ruta de acceso al directorio donde está instalado el secuenciador y, a continuación, presione **entrar.**

3.  En el símbolo del sistema, escriba el siguiente comando y reemplace el texto en cursiva con sus valores:

    SFTSequencer/OPEN:*"especifica el archivo. SPRJ que se abrirá"*

    Presione **entrar**.

4.  También puede especificar los siguientes parámetros opcionales. En el símbolo del sistema, escriba los siguientes comandos y reemplace el texto en cursiva con sus valores:

    /PACKAGENAME: "*especifica el nombre del paquete"*

    /MSI: especifica la creación de un Microsoft Windows Installer asociado.

    /COMPRESS: especifica si se comprimirá el paquete. De forma predeterminada, los paquetes no se comprimen.

    Presione **entrar**.

    **Nota:**  Si el instalador o el paquete de Windows Installer tiene una interfaz de usuario gráfica, se mostrará después de especificar los parámetros de la línea de comandos.

     

## Temas relacionados


[Cómo administrar aplicaciones virtuales con la línea de comandos](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





