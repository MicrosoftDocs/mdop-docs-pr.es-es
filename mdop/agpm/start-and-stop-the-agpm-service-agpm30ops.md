---
title: Iniciar y detener el servicio AGPM
description: Iniciar y detener el servicio AGPM
author: dansimp
ms.assetid: b9d26920-c439-4992-9a78-73e4fba8309d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2be1c2386bedd5888c0ed032479bf1237ce8289c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820220"
---
# Iniciar y detener el servicio AGPM


El servicio AGPM es un servicio de Windows que actúa como un proxy de seguridad y administra el acceso de clientes a objetos de directiva de grupo (GPO) en el entorno de almacenamiento y producción.

**Importante**  Si se detiene o deshabilita el servicio AGPM, los clientes de AGPM no podrán realizar operaciones (como enumerar o editar GPO) a través del servidor.

 

Para completar este procedimiento, se necesita una cuenta de usuario con acceso al servidor de AGPM (el equipo en el que está instalado el servicio AGPM).

**Para iniciar o detener el servicio AGPM**

1.  En el equipo en el que está instalado Microsoft Advanced Group Management Server-servidor (y, por tanto, el servicio AGPM), haga clic en **Inicio**, haga clic en **Panel de control**, haga clic en **herramientas administrativas**y, a continuación, haga clic en **servicios**.

2.  En la lista de servicios, haga clic con el botón secundario en **servicio AGPM** y seleccione **iniciar**, **reiniciar**o **detener**.

    **PRECAUCIÓN**  No modifique la configuración del servicio de AGPM a través de **herramientas administrativas** y **servicios** en el sistema operativo. Esto puede impedir que el servicio AGPM se inicie.

     

### Referencias adicionales

-   [Administrar el servicio AGPM](managing-the-agpm-service-agpm30ops.md)

 

 





