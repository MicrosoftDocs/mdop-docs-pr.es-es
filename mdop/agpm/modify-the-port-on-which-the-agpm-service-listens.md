---
title: Modificar el puerto en el que el servicio AGPM escucha
description: Modificar el puerto en el que el servicio AGPM escucha
author: dansimp
ms.assetid: a82c6873-e916-4a04-b263-aa612cd6956b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2af79ecb9bd05acbc55083163903ae14ab44d06
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820490"
---
# Modificar el puerto en el que el servicio AGPM escucha


El servicio AGPM es un servicio de Windows que actúa como un proxy de seguridad y administra el acceso de clientes a objetos de directiva de grupo (GPO) en el entorno de almacenamiento y producción. De forma predeterminada, el servicio AGPM escucha en el puerto 4600. Puede cambiar este puerto modificando el archivo de índice de archivo de administración avanzada de directivas de grupo (AGPM) para cada archivo.

**Nota:**  Antes de modificar el puerto en el que el servicio AGPM escucha, se recomienda que haga una copia de seguridad del archivo de índice de archivo de AGPM (gpostate.xml). Este archivo se encuentra en la carpeta especificada como la ruta de acceso al archivo durante la instalación de administración avanzada de directivas de grupo-servidor. De forma predeterminada, esta ubicación de este archivo es% CommonAppData% \\Microsoft\\AGPM\\gpostate.xml en el servidor de AGPM. Si no sabe qué equipo hospeda el archivo, puede seguir el procedimiento para modificar la ruta de archivo para mostrar la ruta de archivo actual. Para obtener más información, vea [modificar la ruta de acceso del archivo](modify-the-archive-path.md).

 

Para completar este procedimiento, se necesita una cuenta de usuario con acceso al servidor de AGPM (el equipo en el que está instalado el servicio AGPM) y el archivo de índice de archivo.

**Para modificar el puerto en el que escucha el servicio AGPM**

1.  En el equipo que hospeda el archivo, abra el archivo de índice de archivo (gpostate.xml) en un editor de texto.

2.  En el archivo, busque **AGPM: Port = "4600"**.

3.  Reemplazar **4600** por el puerto en el que debería escuchar el servicio AGPM; después, guarde y cierre el archivo.

4.  En el servidor de AGPM, reinicie el servicio AGPM. (Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service.md)).

5.  Modifique el puerto en la conexión del servidor de AGPM para cada administrador de directiva de grupo. Para obtener más información, vea [configurar la conexión del servidor de AGPM](configure-the-agpm-server-connection.md).

6.  Repita este paso para cada archivo y servidor AGPM.

### Referencias adicionales

-   [Administrar el servicio AGPM](managing-the-agpm-service.md)

 

 





