---
title: Restaurar el archivo desde una copia de seguridad
description: Restaurar el archivo desde una copia de seguridad
author: dansimp
ms.assetid: 49666337-d72c-4e44-99e4-9eb59b2355a9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b00d2e5e612e2ac43f965e4adf6175e2fd159007
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818361"
---
# Restaurar el archivo desde una copia de seguridad


Si se produce un desastre y el archivo de administración de directivas de grupo (AGPM) avanzada está dañado o se ha destruido, un administrador de AGPM (control total) puede restaurar el archivo desde una copia de seguridad preparada por adelantado y, a continuación, importar desde el entorno de producción los objetos de directiva de grupo (GPO) que no se encuentren en el archivo o para los que la versión Para obtener información sobre cómo restaurar una copia de seguridad de archivo en un servidor diferente, vea [mover el servidor de AGPM y el archivo](move-the-agpm-server-and-the-archive.md).

Para completar este procedimiento, se necesita una cuenta de usuario que tenga acceso al servidor de AGPM (el equipo en el que está instalado el servicio AGPM) y a la carpeta que contiene el archivo.

**Para restaurar el archivo a partir de una copia de seguridad**

1.  Detenga el servicio AGPM. Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm30ops.md).

2.  Quitar el archivo existente. De forma predeterminada, la carpeta de archivo es%ProgramData%\\Microsoft\\AGPM, pero es posible que el administrador AGPM que instaló Microsoft Advanced Group Policy Management-Server haya introducido una ubicación diferente durante la instalación.

3.  Vuelva a crear la carpeta de archivo mediante la configuración de la ruta de archivo, la cuenta del servicio AGPM, el propietario del archivo y el puerto de escucha. No es necesario usar los mismos valores que se usan en la instalación original. Para obtener más información, vea [modificar el servicio AGPM](modify-the-agpm-service-agpm30ops.md).

4.  Copie el contenido de la copia de seguridad archivada en la carpeta archivo, copie las subcarpetas y archivos para asegurarse de que cada subcarpeta y archivo heredan los permisos de la carpeta archivo. Tenga cuidado de no sobrescribir la carpeta de archivo.

5.  Si no está seguro de si un GPO en la copia de seguridad de archivo es más reciente que la copia de ese GPO en producción, genere un informe de diferencias y compare su configuración. Para obtener más información, consulte [identificar diferencias entre objetos de directiva de grupo, versiones de GPO o plantillas](identify-differences-between-gpos-gpo-versions-or-templates-agpm30ops.md).

6.  Reinicie el servicio AGPM. Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm30ops.md).

### Referencias adicionales

-   [Copia de seguridad del archivo](back-up-the-archive.md)

-   [Mover el servidor AGPM y el archivo](move-the-agpm-server-and-the-archive.md)

-   [Administración del archivo](managing-the-archive.md)

 

 





