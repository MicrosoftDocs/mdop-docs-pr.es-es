---
title: Cómo configurar el servidor para IIS
description: Cómo configurar el servidor para IIS
author: dansimp
ms.assetid: 1fcfc583-322f-4a38-90d0-e64bfa9ee3d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9fe3367698b6f387d4467afdad1b3e17211134d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817741"
---
# Cómo configurar el servidor para IIS


Antes de que las aplicaciones virtuales se puedan transmitir por secuencias al cliente de escritorio de virtualización de aplicaciones y al cliente para servicios de escritorio remoto (anteriormente servicios de Terminal Server), los servidores IIS deben estar configurados. Al configurar los servidores, está configurando el directorio de contenido en el que se cargan y almacenan los archivos de SFT. Los archivos SFT contienen la aplicación virtual (o aplicaciones).

**Para configurar el directorio de contenido en el servidor IIS**

1.  En el servidor que ejecuta IIS, busque el directorio que desea usar como directorio de contenido o cree el directorio si no existe. Configure este directorio como un recurso compartido de archivos estándar.

2.  En el servidor en el que se ejecuta IIS, abra el **Administrador de IIS**y, en el sitio web predeterminado, cree un directorio virtual que se corresponda con el directorio de contenido que ha creado en el servidor. Asegúrese de que **lectura** está activada.

3.  Conceda al directorio virtual recién creado el **contenido**de alias.

4.  Acepte la configuración predeterminada para este directorio virtual.

5.  Configure los permisos del sistema de archivos NTFS en el directorio de contenido y en las carpetas de paquetes en el directorio de contenido con los grupos de seguridad de los servicios de dominio de Active Directory que definió anteriormente.

**Nota:**  Si está usando IIS para publicar los archivos ICO y OSD, debe configurar un tipo MIME para OSD = TXT; de lo contrario, IIS no enviará los archivos ICO y OSD a los clientes. Si está usando IIS para publicar paquetes (archivos SFT), debe configurar un tipo MIME para SFT = Binary; de lo contrario, IIS no enviará los archivos SFT a los clientes.

 

## Temas relacionados


[Escenario basado en servidor de virtualización de aplicaciones](application-virtualization-server-based-scenario.md)

[Escenario basado en distribución electrónica de software](electronic-software-distribution-based-scenario.md)

[Cómo configurar los servidores de administración de virtualización de aplicaciones](how-to-configure-the-application-virtualization-management-servers.md)

[Cómo configurar los servidores de streaming de virtualización de aplicaciones](how-to-configure-the-application-virtualization-streaming-servers.md)

[Cómo configurar el servidor de archivos](how-to-configure-the-file-server.md)

 

 





