---
title: Cómo instalar el cliente de App-V mediante el uso de Setup.exe
description: Cómo instalar el cliente de App-V mediante el uso de Setup.exe
author: dansimp
ms.assetid: 106a5d97-b5f6-4a16-bf52-a84f4d558c74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60f79a2d2f74848ab121ba13cdf8c215088d54db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817340"
---
# Cómo instalar el cliente de App-V mediante el uso de Setup.exe


En este tema se describe cómo instalar el cliente de App-V con el programa setup.exe. Al instalar el cliente de App-V con el programa setup.exe, el instalador determina qué software necesario necesita y lo instala automáticamente antes de instalar el cliente.

**Para instalar el cliente de virtualización de aplicaciones con Setup.exe**

1.  Asegúrese de que ha iniciado sesión con una cuenta que tiene derechos de administrador en el equipo.

2.  Abra una ventana del símbolo del sistema y, a continuación, cambie el directorio a la carpeta que contiene los archivos de instalación. Al instalar la versión 4.6 o una versión posterior del cliente de App-V, debe usar el instalador correcto para el sistema operativo del equipo, 32 bits o 64 bits. La instalación no se realizará y aparecerá un mensaje de error si usa el instalador equivocado.

3.  Escriba la cadena de comando de instalación en el símbolo del sistema. Como alternativa, puede crear un archivo de comandos y ejecutarlo desde el símbolo del sistema. También puede usar un lenguaje de scripts, como VBScript o Windows PowerShell, para ejecutar el comando.

4.  En el siguiente ejemplo de línea de comandos se muestra cómo se puede usar setup.exe con un número de parámetros opcionales. Para obtener más información sobre estos parámetros, consulte [parámetros de la línea de comandos del instalador del cliente de virtualización de aplicaciones](application-virtualization-client-installer-command-line-parameters.md).

    **"setup.exe"/s/v "/QN SWICACHESIZE = \ \" 10240 \ \ "SWIPUBSVRDISPLAY = \ \" Production System\\ "SWIPUBSVRTYPE = \ \" HTTP/secure\\ "SWIPUBSVRHOST = \ \" PRODSYS\\ "SWIPUBSVRPORT = \ \" 443 \ \ "SWIPUBSVRPATH = \ \"/AppVirt/appsntype.xml \ \ "SWIPUBSVRREFRESH = \ \" on\\ "SWIGLOBALDATA = \ \" D:\\AppVirt\\Global\\ "SWIUSERDATA = \ \" ^% LOCALAPPDATA ^%\\Windows\\Application virtualización Client\\ "SWIFSDRIVE = \ \" Q\\ ""**

    **Importante**  
    -   Las comillas que aparecen en la sección "**/v**" se deben tratar como caracteres especiales e introducirse con un " **\\** " anterior. Las comillas solo son necesarias cuando el valor contiene un espacio. sin embargo, por coherencia, todas las instancias del ejemplo anterior se muestran con comillas.

    -   Los caracteres "" **%** en "**% HomeDrive%**" deben ir precedidos del **^** carácter de escape "". En caso contrario, el shell de comandos de Windows establece el valor en el del usuario que realiza la instalación.

    -   Los modificadores de **InstallShield** **/s** y **/QN** son necesarios para que esto sea una instalación silenciosa. El modificador **/QN** debe ir a continuación del modificador **/v** , separado por un carácter de comillas sin espacios intermedios.

    -   La carpeta especificada en el valor **SWIGLOBALDATA** debe existir previamente.

     

5.  Una vez completada la instalación, le recomendamos que ejecute una búsqueda de Microsoft Update para asegurarse de que están instaladas las actualizaciones más recientes.

## Temas relacionados


[Cómo instalar el cliente mediante el uso de la línea de comandos](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





