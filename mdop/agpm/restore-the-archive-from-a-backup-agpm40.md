---
title: Restaurar el archivo desde una copia de seguridad
description: Restaurar el archivo desde una copia de seguridad
author: dansimp
ms.assetid: b83f6173-a236-4da2-b16e-8df20920d4cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3a1b7039ad587cf9c8d7f914fe3b963e12ba8949
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818400"
---
# Restaurar el archivo desde una copia de seguridad


Si se produce un desastre y el archivo de administración de directivas de grupo (AGPM) avanzada está dañado o destruido, un administrador AGPM (control total) puede restaurar el archivo desde una copia de seguridad preparada por adelantado y, a continuación, importar desde el entorno de producción del dominio cualquier objeto de directiva de grupo (GPO) que no esté en el archivo o cuya versión en producción sea más actual Para obtener información sobre cómo restaurar una copia de seguridad de archivo en un servidor diferente, vea [mover el servidor de AGPM y el archivo](move-the-agpm-server-and-the-archive-agpm40.md).

Para completar este procedimiento, se necesita una cuenta de usuario que tenga acceso al servidor de AGPM (el equipo en el que está instalado el servicio AGPM) y a la carpeta que contiene el archivo.

**Para restaurar el archivo a partir de una copia de seguridad**

1.  Detenga el servicio AGPM. Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm40.md).

2.  Quitar el archivo existente. De forma predeterminada, la carpeta de archivo es%ProgramData%\\Microsoft\\AGPM, pero es posible que el administrador AGPM que instaló Microsoft Advanced Group Policy Management-Server haya introducido una ubicación diferente durante la instalación.

3.  Vuelva a crear la carpeta de archivo mediante la configuración de la ruta de archivo, la cuenta del servicio AGPM, el propietario del archivo y el puerto de escucha. No es necesario usar los mismos valores que se usan en la instalación original. Para obtener más información, vea [modificar el servicio AGPM](modify-the-agpm-service-agpm40.md).

4.  Copie el contenido de la copia de seguridad archivada en la carpeta archivo, copie las subcarpetas y archivos para asegurarse de que cada subcarpeta y archivo heredan los permisos de la carpeta archivo. Tenga cuidado de no sobrescribir la carpeta de archivo.

5.  Si no está seguro de si un GPO en la copia de seguridad de archivo es más reciente que la copia de ese GPO en producción, genere un informe de diferencias y compare su configuración. Para obtener más información, consulte [identificar diferencias entre objetos de directiva de grupo, versiones de GPO o plantillas](identify-differences-between-gpos-gpo-versions-or-templates-agpm40.md).

6.  Reinicie el servicio AGPM. Para obtener más información, consulte [iniciar y detener el servicio AGPM](start-and-stop-the-agpm-service-agpm40.md).

### Referencias adicionales

-   [Copia de seguridad del archivo](back-up-the-archive-agpm40.md)

-   [Mover el servidor AGPM y el archivo](move-the-agpm-server-and-the-archive-agpm40.md)

-   [Administración del archivo](managing-the-archive-agpm40.md)

 

 





