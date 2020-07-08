---
title: Tecnología de transferencia de recorte de MED-V
description: Tecnología de transferencia de recorte de MED-V
author: dansimp
ms.assetid: 2744e855-a486-4028-9606-f0084794ec65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa11c8036954070bbff465a6ad78992fdd52f3a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826190"
---
# Tecnología de transferencia de recorte de MED-V


## <a href="" id="bkmk-medvtrimtransfertechnology"></a>


La tecnología de desduplicación avanzada de transferencia de guarnecidos de MED-V acelera la descarga de las imágenes de máquina virtual iniciales y actualizadas a través de LAN o WAN, lo que reduce el ancho de banda de red necesario para transportar una máquina virtual de área de trabajo de MED-V a varios usuarios finales.

Esta tecnología innovadora usa datos locales existentes para crear la imagen de la máquina virtual, aprovechando el hecho de que, en muchos casos, una gran parte de la máquina virtual (por ejemplo, archivos del sistema y de la aplicación) ya existe en el disco del usuario final. Por ejemplo, si se envía una máquina virtual que contiene WindowsXP a un cliente que ejecuta una copia local de WindowsXP, MED-V eliminará automáticamente los elementos de WindowsXP redundantes de la transferencia. Para garantizar un área de trabajo válida y funcional, el cliente MED-V comprueba de forma criptográfica la integridad de los datos locales antes de su uso, garantizando que los bloques locales de datos son absolutamente bits a los de la imagen de la máquina virtual deseada. Los bloques que no coinciden no se usan.

El proceso es transparente y de ancho de banda, y las transferencias se ejecutan en segundo plano, usando recursos de red y de CPU no usados.

Al actualizar a una nueva versión de la imagen (por ejemplo, cuando los administradores desean distribuir una nueva aplicación o parche), solo se descargan los elementos que han cambiado ("deltas") y no toda la máquina virtual, lo que reduce significativamente el ancho de banda de red requerido y el tiempo de entrega.

Puede configurar qué carpetas se indizan en el host como parte del Protocolo de transferencia de recorte, en función del sistema operativo del host. Estas opciones se configuran en el archivo *ClientSettings.xml* , que se encuentra en la carpeta de **Server\\ de Servers\\Configuration** .

Al aplicar la nueva configuración, se debe reiniciar el servicio.

```xml
<HostIndexingXP type="System.String[]"> 
- <ArrayOfString>
<string>%WINDIR%</string> 
<string>%ProgramFiles%\Common Files</string> 
<string>%ProgramFiles%\Internet Explorer</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
<string>%ProgramFiles%\Windows NT</string> 
<string>%ProgramFiles%\Messenger</string> 
<string>%ProgramFiles%\Adobe</string> 
<string>%ProgramFiles%\Outlook Express</string> 
</ArrayOfString> 
</HostIndexingXP> 
- <HostIndexingVista type="System.String[]"> 
- <ArrayOfString> 
<string>%WINDIR%\MSAgent</string> 
<string>%WINDIR%\winsxs</string> 
<string>%WINDIR%\system</string> 
<string>%WINDIR%\system32</string> 
<string>%WINDIR%\Microsoft.NET</string> 
<string>%WINDIR%\SoftwareDistribution</string> 
<string>%WINDIR%\L2Schemas</string> 
<string>%WINDIR%\Cursors</string> 
<string>%WINDIR%\Boot</string> 
<string>%WINDIR%\Help</string> 
<string>%WINDIR%\assembly</string> 
<string>%WINDIR%\inf</string> 
<string>%WINDIR%\fonts</string> 
<string>%WINDIR%\Installer</string> 
<string>%WINDIR%\IME</string> 
<string>%WINDIR%\Resources</string> 
<string>%WINDIR%\servicing</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
</ArrayOfString> 
</HostIndexingVista>
```

 

 





