---
title: Configuración del servidor de MED-V para el modo de clúster
description: Configuración del servidor de MED-V para el modo de clúster
author: dansimp
ms.assetid: 41f0b2a3-4ce9-48e1-a6fb-4c13c4228515
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ddb7dd5af65d8a465c5c1884bb27a3027621bac1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826720"
---
# Configuración del servidor de MED-V para el modo de clúster


Puede configurar el servidor de MED-V en el modo de clúster. En el modo de clúster, se usan dos servidores y todos los archivos identificados como mutuos en ambos servidores se colocan en un sistema de archivos. El servidor accede a los archivos desde el sistema de archivos, en lugar de almacenar los archivos de forma local.

## <a href="" id="bkmk-howtoconfigurethemedvserverinclustermode"></a>


**Para configurar el servidor de MED-V en el modo de clúster**

1.  Instale y configure MED-V en uno de los servidores.

2.  Cree una red compartida en una ubicación central en la que todos los servidores puedan acceder a ella.

3.  Copie el contenido de la carpeta * &lt; INSTALLDIR &gt; /Servers/ConfigurationServer* en la red compartida.

4.  Instale MED-V Server en todos los servidores designados.

5.  En la red compartida, asigne acceso completo a todas las cuentas del sistema de servidor de MED-V.

6.  En cada servidor, haga lo siguiente:

    1.  En el archivo * &lt; InstallDir &gt; /Servers/ServerConfiguration.xml* , establezca el valor de * &lt; StorePath &gt; * en la ruta de acceso de red compartida.

    2.  Copie el archivo * &lt; InstsallDir &gt; /Servers/KeyPair.xml* desde el servidor original a todos los servidores de MED-V.

    3.  Reinicie el servicio MED-V.

**Nota:**  Si todos los servidores tienen la misma configuración local (como puertos de escucha, servidor IIS, permisos de administración, base de datos de informes, etc.), todos los servidores también pueden compartir el * &lt; &gt; ServerSettings.xmlINSTALLDIR/Servers/* .

 

## Temas relacionados


[Diseño y planificación de la infraestructura de MED-V](med-v-infrastructure-planning-and-design.md)

 

 





