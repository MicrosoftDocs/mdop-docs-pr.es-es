---
title: Configurar MED-V para redes remotas
description: Configurar MED-V para redes remotas
author: dansimp
ms.assetid: 4d2f0081-622f-4a6f-8d73-f8c2108036e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 328376046ee5213f3d5bb09be7adf8c81f8508b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826721"
---
# Configurar MED-V para redes remotas


Puede configurar MED-V para que funcione desde dentro de una red, de forma remota o desde dentro de la red y de forma remota.

## <a href="" id="bkmk-howtoconfiguremedvtoworkfrominsideanetworkorremotely"></a>


**Para configurar MED-V para que funcione desde dentro de una red**

-   Configurar un servidor de MED-V y una distribución de imágenes dentro de la red.

**Para configurar MED-V para que funcionen de forma remota**

1.  Configurar un servidor de MED-V y un servidor de distribución de imágenes accesibles desde Internet.

2.  Si es necesario, configure un proxy inverso de red perimetral (también llamado DMZ).

3.  Establezca el método de autenticación, en el archivo *ClientSettings.xml* , que puede encontrarse en la carpeta **Servers\\Configuration Server\\**

**Para configurar MED-V para que funcione desde dentro de una red y de forma remota**

1.  Configurar un servidor de MED-V y un servidor de distribución de imágenes en la red.

2.  Asegúrese de que los servidores son accesibles desde Internet.

3.  Configure la resolución DNS para que cuando el cliente intente conectarse a un servidor, se conecte automáticamente al servidor correcto (dentro de la red o a través de Internet) en función de la ubicación del cliente.

4.  Si es necesario, configure un proxy inverso de red perimetral.

5.  Establezca el método de autenticación, en el archivo *ClientSettings.xml* , que puede encontrarse en la carpeta **Servers\\Configuration Server\\**

**Nota:**  Al aplicar la nueva configuración, se debe reiniciar el servicio.

 

-   Puede cambiar el esquema de autenticación de IIS a uno de los siguientes: básico, implícito, NTLM o NEGOTIATE. El valor predeterminado es NEGOTIATE y usa la siguiente entrada:

    ```xml
    <ImageDistribution>
    <!-- The authentication used for image download. Basic and digest authentication should be used only under SSL.-->
       <!-- The line below can be one of the following: -->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_BASIC</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_DIGEST</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NTLM</BG_AUTH_SCHEME-->
       <!--BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME-->
       <Authentication type="Kidaro.Foundation.Bits.BG_AUTH_SCHEME">
          <BG_AUTH_SCHEME>BG_AUTH_SCHEME_NEGOTIATE</BG_AUTH_SCHEME>
       </Authentication>
    </ImageDistribution>
    ```

## Temas relacionados


[Diseño y planificación de la infraestructura de MED-V](med-v-infrastructure-planning-and-design.md)

 

 





