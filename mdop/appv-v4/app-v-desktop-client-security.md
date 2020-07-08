---
title: Seguridad de cliente de escritorio de App-V
description: Seguridad de cliente de escritorio de App-V
author: dansimp
ms.assetid: 216b9c16-7bb4-4f94-b9d8-810501285008
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 26add6f855780113613cf1591c41722643954477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822320"
---
# Seguridad de cliente de escritorio de App-V


El cliente de escritorio de App-V ofrece muchas mejoras de seguridad que no estaban disponibles en versiones anteriores del producto. Estos cambios proporcionan mayores niveles de seguridad de forma predeterminada, así como la configuración de la configuración de los clientes.

**Nota:**  Al instalar el cliente de escritorio de App-V en un equipo, el software tiene como valor predeterminado la configuración más segura. Sin embargo, al actualizar, la configuración anterior del cliente continúa.

 

De forma predeterminada, el cliente de escritorio de App-V solo está configurado con los permisos necesarios para permitir que un usuario no administrativo realice una actualización de publicación y aplicaciones de transmisión por secuencias. Entre las mejoras de seguridad adicionales proporcionadas en el cliente de escritorio de App-V se incluyen las siguientes:

-   De forma predeterminada, solo el proceso de actualización de la publicación permite una actualización de la caché OSD.

-   El archivo de registro ( `sftlog.txt` ) solo es accesible para las cuentas con acceso administrativo local al cliente.

-   El archivo de registro ahora tiene un tamaño máximo.

-   Los archivos de registro se administran mediante la configuración de archivo.

-   El registro de eventos del sistema se realiza ahora.

## Permisos


Después de instalar el cliente de escritorio, puede configurar otras opciones de seguridad a través de MMC o en un cliente individual mediante el registro o la plantilla ADM proporcionada por Microsoft. El cliente de escritorio de App-V tiene permisos que puede configurar para restringir el acceso de usuarios no administrativos a todas las características del cliente de escritorio. Para obtener una lista completa de los permisos, consulte el archivo de ayuda del cliente de App-V o la guía de operaciones de App-V.

**Importante**  Considere detenidamente las consecuencias de cambiar los derechos de acceso, especialmente en los sistemas compartidos por varios usuarios, como los servidores de terminal.

 

**Nota:**  Si los usuarios del entorno tienen privilegios de administrador local para sus equipos, los permisos se pasan por alto.

 

### Plantilla ADM

Microsoft Application Virtualization (App-V) presenta una plantilla ADM que puede usar para establecer la configuración de cliente más común mediante directivas de grupo. Esta plantilla permite a los administradores implementar y cambiar muchas de las opciones de configuración del cliente a través de un modelo de administración centralizado. Algunos de los valores disponibles en la plantilla ADM son configuración de seguridad.

**Importante**  Cuando use la plantilla ADM, recuerde que la configuración es la configuración de preferencias de directiva de grupo y no directivas de grupo completamente administradas.

 

Para obtener una descripción completa de la plantilla ADM, la configuración específica y la orientación para implementar correctamente clientes en su entorno, consulte las notas del producto de la plantilla ADM de App-V en [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063) .

## Quitar asociaciones de tipo de archivo OSD


Si su organización no requiere que los usuarios abran las aplicaciones directamente desde un archivo OSD, puede mejorar la seguridad si quita las asociaciones de tipos de archivo en el cliente. Quite las `HKEY_CURRENT_USERS` teclas para OSD y `Softgird.osd.file` con el editor del registro. Puede poner este proceso en un script de inicio de sesión o en un script posterior a la instalación para automatizar estos cambios.

 

 





