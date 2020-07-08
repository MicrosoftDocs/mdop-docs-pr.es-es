---
title: Cómo conectarse a un sistema de virtualización de aplicaciones
description: Cómo conectarse a un sistema de virtualización de aplicaciones
author: dansimp
ms.assetid: ac38216c-5464-4c0b-a4d3-3949ba6358ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 30d60e187e1b7595fd0dce6641fa027a1df68f3d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817711"
---
# Cómo conectarse a un sistema de virtualización de aplicaciones


Debe conectar la consola de administración de Application Virtualization Server a un sistema de virtualización de aplicaciones antes de poder usar la consola de administración para administrar aplicaciones, asociaciones de tipos de archivo, paquetes, licencias de aplicaciones, grupos de servidores, directivas y administradores de proveedores. El procedimiento siguiente describe los pasos que debe seguir para conectar la consola a un sistema de virtualización de aplicaciones.

**Para conectarse a un sistema de virtualización de aplicaciones**

1. Haga clic con el botón derecho en el nodo del sistema de virtualización de aplicaciones en el panel de **ámbito** y seleccione **conectar con el sistema de virtualización de aplicaciones** en el menú emergente.

   **Nota**  
   Hay tres componentes para la administración de servidores de virtualización de aplicaciones: la consola de administración de virtualización de aplicaciones, el servicio Web de administración y el almacén de SQL. Si estos componentes se distribuyen en diferentes equipos físicos, debe configurar la seguridad correctamente para que los componentes se comuniquen a través del sistema. Para obtener más información, consulte los siguientes manuales y artículos:

   [Cómo configurar el servidor para que sea de confianza para la delegación](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)

   [Guía de planeación e implementación del sistema de virtualización de aplicaciones](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)

   [Guía de operaciones del sistema de virtualización de aplicaciones](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)

   [Artículo 930472](https://go.microsoft.com/fwlink/?LinkId=114647) de Microsoft Knowledge base (https://go.microsoft.com/fwlink/?LinkId=114647)

   [Artículo 930565](https://go.microsoft.com/fwlink/?LinkId=114648) de Microsoft Knowledge base (https://go.microsoft.com/fwlink/?LinkId=114648)

     

2. Complete los campos en el cuadro de diálogo **conectar con el sistema de virtualización de aplicaciones** :

   1. **Nombre de host del servicio Web**: escriba el nombre del sistema de virtualización de aplicaciones al que desea conectarse o escriba **localhost** para conectarse al servidor local.

   2. **Usar conexión segura**: Seleccione esta casilla si desea conectarse al servidor con una conexión segura.

   3. **Puerto**: Introduzca el número de puerto que desea usar para la conexión. **80** es el número de Puerto normal predeterminado y **443** es el número de puerto seguro.

   4. **Usar cuenta de Windows actual**: Seleccione este botón de radio para usar las credenciales de cuenta de Windows actuales.

   5. **Especificar cuenta de Windows**: Seleccione este botón de radio cuando desee conectar con el servidor como otro usuario.

   6. **Nombre**: escriba el nombre del nuevo usuario con el formato *DOMAIN\\username* o el <em> username@domain </em> .

   7. **Contraseña**: escriba la contraseña que corresponde al nuevo usuario.

3. Haz clic en **Aceptar**.

## Temas relacionados


[Cómo realizar tareas administrativas en la consola de administración de servidor de virtualización de aplicaciones](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





