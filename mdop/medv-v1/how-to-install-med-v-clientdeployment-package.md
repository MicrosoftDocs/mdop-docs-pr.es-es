---
title: Cómo instalar el cliente de MED-V
description: Cómo instalar el cliente de MED-V
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827191"
---
# Cómo instalar el cliente de MED-V


En un escenario basado en un paquete de implementación, la instalación del cliente MED-V se incluye en el paquete de implementación y se instala directamente desde el paquete.

**Importante**  
Cuando use un paquete de implementación que no incluya una imagen, asegúrese de que la imagen se carga en la web o se inserta en la carpeta prestage antes de instalar el paquete de implementación.



**Para instalar un paquete de implementación**

1.  Realiza una de las siguientes acciones:

    -   Descargar el paquete MED-V de la Web.

    -   Inserte el USB o el DVD de implementación en la unidad host.

2.  Si MED-V no se inicia automáticamente, haga doble clic en MED-VAutoInstaller.exe.

    Aparece un cuadro de diálogo en el que se enumeran los componentes que ya están instalados y los que se están instalando.

    **Nota**  
    Si en el equipo host hay una versión de Microsoft Virtual PC que no es compatible, aparecerá un mensaje en el que se le indicará que desinstale la versión existente y vuelva a ejecutar el instalador.



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. Si es necesario, reinicie el equipo.

   Cuando se complete la instalación, MED-V se iniciará y aparecerá un mensaje que le notificará que se ha completado la instalación.

4. Inicie sesión en MED-V con el nombre de usuario y la contraseña siguientes:

   -   Escriba el nombre de dominio y el nombre de usuario seguido de la contraseña del usuario de dominio que tiene permiso para trabajar con MED-V.

       Ejemplo: "domain \ _name \\user\ _name", "contraseña"

## Temas relacionados


[Cómo configurar un paquete de implementación](how-to-configure-a-deployment-package.md)

[Cómo cargar una imagen de MED-V en el servidor](how-to-upload-a-med-v-image-to-the-server.md)

[Referencia de línea de comandos de instalación de cliente](client-installation-command-line-reference.md)









