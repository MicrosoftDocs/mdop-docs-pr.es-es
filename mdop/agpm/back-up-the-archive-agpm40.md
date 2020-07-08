---
title: Copia de seguridad del archivo
description: Copia de seguridad del archivo
author: dansimp
ms.assetid: 538d85eb-3596-4c1d-bbd7-26bc28857c28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c6888d61e126d603aefa4e818f1070c5a493ea6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819211"
---
# Copia de seguridad del archivo


Para ayudar en la recuperación del archivo para administración de directivas de grupo (AGPM) avanzada si se produce un desastre, un administrador de AGPM (control total) debe realizar una copia de seguridad del archivo con frecuencia. De forma predeterminada, el archivo se crea en%ProgramData%\\Microsoft\\AGPM. Sin embargo, puede especificar una ruta diferente durante la configuración de administración de directivas de grupo (servidor) avanzada de Microsoft.

Para completar este procedimiento, se necesita una cuenta de usuario que tenga acceso al servidor de AGPM (el equipo en el que está instalado el servicio AGPM) y a la carpeta que contiene el archivo.

**Para hacer una copia de seguridad del archivo**

1.  Detenga el servicio AGPM. Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm40.md).

2.  Haga una copia de seguridad de la carpeta de archivo con el explorador de Windows, xcopy, Windows Server® copia de seguridad u otra herramienta de copia de seguridad. Asegúrese de hacer una copia de seguridad de los archivos ocultos, de sistema y de solo lectura.

3.  Almacene la copia de seguridad del archivo en un lugar seguro.

4.  Reinicie el servicio AGPM. Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm40.md).

**Nota:**  Si un administrador de AGPM realiza copias de seguridad del archivo con frecuencia, los objetos de directiva de grupo (GPO) de la copia de seguridad del archivo no estarán actualizados. Para asegurarse de que la copia de seguridad del archivo esté actualizada, haga una copia de seguridad del archivo como parte de la estrategia de copia de seguridad diaria de su organización.

 

### Referencias adicionales

-   [Restaurar el archivo desde una copia de seguridad](restore-the-archive-from-a-backup-agpm40.md)

-   [Mover el servidor AGPM y el archivo](move-the-agpm-server-and-the-archive-agpm40.md)

-   [Administración del archivo](managing-the-archive-agpm40.md)

 

 





