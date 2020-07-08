---
title: Cómo publicar una aplicación virtual en el cliente
description: Cómo publicar una aplicación virtual en el cliente
author: dansimp
ms.assetid: 90af843e-b5b3-4a71-a3a1-fa5f4c087f28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5585f82150db69929ccedbee3aecab969c5e7dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816871"
---
# Cómo publicar una aplicación virtual en el cliente


Al implementar la virtualización de aplicaciones mediante un sistema electrónico de distribución de software, puede usar uno de los procedimientos siguientes para publicar un paquete de aplicación para sus usuarios.

**Para publicar un paquete con un archivo de Windows Installer independiente**

1.  El cliente debe instalarse con el parámetro *REQUIREAUTHORIZATIONIFCACHED* establecido en 0 (cero). Para obtener más información sobre la configuración de este parámetro, consulte [parámetros de la línea de comandos del instalador del cliente de virtualización de aplicaciones](application-virtualization-client-installer-command-line-parameters.md)

2.  Copie el archivo de Windows Installer y el archivo SFT a la misma carpeta del equipo de destino.

3.  Ejecute el siguiente comando en el equipo:

    `Msiexec.exe /I "packagename.msi" /q`

**Para publicar un paquete con Windows Installer y el manifiesto del paquete**

1.  Copie el archivo de Windows Installer en el equipo de destino y el archivo SFT en el recurso compartido de contenido del servidor de transmisión.

2.  Ejecute el siguiente comando en el equipo de cada usuario:

    `Msiexec.exe /I "\\pathtomsi\packagename.msi" MODE=STREAMING  OVERRIDEURL="\\\\server\\share\\package.sft" LOAD=TRUE /q`

    **Importante**  Para OVERRIDEURL todos los caracteres de barra invertida se deben escapar con una barra diagonal inversa anterior, o la ruta de acceso de OVERRIDEURL no se analizará correctamente. Además, las propiedades y los valores deben escribirse en mayúsculas, excepto en el caso de que el valor sea una ruta de acceso a un archivo.

     

**Para publicar un paquete con SFTMIME**

-   Para obtener un ejemplo de cómo publicar una aplicación para todos los usuarios de un equipo, ejecute el siguiente comando en el equipo del usuario:

    `SFTMIME ADD PACKAGE:package-name /MANIFEST manifest-path                                 [/GLOBAL] [/LOG log-pathname | /CONSOLE | /GUI]`

    Para obtener más información sobre estos y otros comandos de SFTMIME, consulte [SFTMIME referencia de comandos](sftmime--command-reference.md).

## Temas relacionados


[Determinar el método de publicación](determine-your-publishing-method.md)

[Escenario basado en distribución electrónica de software](electronic-software-distribution-based-scenario.md)

[Referencia de comandos de SFTMIME](sftmime--command-reference.md)

[Escenario de distribución independiente para clientes de virtualización de aplicaciones](stand-alone-delivery-scenario-for-application-virtualization-clients.md)

 

 





