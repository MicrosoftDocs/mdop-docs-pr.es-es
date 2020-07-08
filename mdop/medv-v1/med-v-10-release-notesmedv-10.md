---
title: Notas de la versión de MED-V 1.0
description: Notas de la versión de MED-V 1.0
author: dansimp
ms.assetid: 006a3537-5c5b-43b5-8df8-4bf6ddd3cd2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 683056f768a3d547828996a9b191d58337c21ad6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826591"
---
# Notas de la versión de MED-V 1.0


## Problemas conocidos con MED-V


Esta sección proporciona la información más actualizada sobre problemas generales con la plataforma de virtualización de escritorio de Microsoft Enterprise (MED-V). Estos problemas no aparecen en la documentación del producto y, en algunos casos, podrían contradecir la documentación del producto existente. Siempre que sea posible, estos problemas se resolverán en versiones posteriores.

### Las descargas de archivos no siguen las reglas de redireccionamiento web

Descargas de archivos no siga las reglas de redirección web establecidas en una directiva de área de trabajo de MED-V.

### Al expandir una ventana de aplicación publicada en la consola a pantalla completa, desaparece

Si expande la ventana de una aplicación publicada en consola (como cmd.exe) a pantalla completa dentro de un área de trabajo de MED-V configurada en modo de integración transparente, la ventana de la aplicación podría desaparecer o no responder.

### Al trabajar en el modo de escritorio completo, las ubicaciones de los iconos en el escritorio no se guardan

Al trabajar en modo de escritorio completo, los cambios de ubicación manual de los iconos en el escritorio no se guardan entre las sesiones del área de trabajo de MED-V.

### No puede existir en el mismo dominio una imagen local y una imagen de prueba con el mismo nombre

Si una imagen local se une al dominio y el administrador crea una nueva versión de la misma imagen con el mismo nombre de equipo que una imagen de prueba, cuando la imagen de prueba se une al dominio, se produce un error en la acción unirse al dominio o la imagen local se quita del dominio.

### MED-V no es compatible con las características de Windows Aero

MED-V no es compatible con las características de Windows Aero (como aero Flip 3D).

### La consola de administración solo la puede usar un usuario de Windows por equipo

La consola de administración de MED-V solo la pueden usar los administradores y el usuario de Windows que instaló la aplicación de administración.

### La utilidad de configuración del servidor MED-V prueba la conectividad de Microsoft SQL Server en contexto de usuario en lugar de en el contexto de servicio servidor MED-V

MED-V usa el contexto de servicio de servidor MED-V para recopilar informes de la base de datos de informes de Microsoft SQL Server. La utilidad de configuración del servidor MED-V comprueba la base de datos y prueba la cadena de conexión de la base de datos. No valida el acceso del servicio servidor MED-V a la base de datos.

 

 





