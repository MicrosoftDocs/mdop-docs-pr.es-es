---
title: Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos
description: Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos
author: dansimp
ms.assetid: 3e3d873f-13d2-402f-97b4-f62d0c399171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c424f39c8209ca641f6073838ebcb8726acc9e25
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817900"
---
# Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos


Una vez que el cliente de Application Virtualization (App-V) se ha implementado y configurado durante la instalación mediante la línea de comandos, podría ser necesario cambiar una o más opciones de configuración del cliente. Esto se consigue modificando las claves del registro apropiadas, con uno de los siguientes métodos:

-   Usar el editor del registro directamente

-   Uso de un archivo. reg

-   Usar un lenguaje de scripts como VBScript o Windows PowerShell

También hay una plantilla ADM que puede usar. Para obtener más información sobre la plantilla ADM, consulte <https://go.microsoft.com/fwlink/?LinkId=121835> .

**PRECAUCIÓN**  Tenga cuidado cuando edite el registro porque los errores pueden dejar el equipo en un estado inutilizable. Asegúrese de seguir las prácticas empresariales estándar que se relacionan con las modificaciones del registro. Pruebe minuciosamente todos los cambios propuestos en un entorno de prueba antes de implementarlos en los equipos de producción.

 

## En esta sección


**Importante**  En un equipo de 64 bits, las claves y los valores que se describen en las siguientes secciones estarán bajo HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.

 

<a href="" id="how-to-reset-the-filesystem-cache"></a>[Cómo restablecer la caché de sistema de archivos](how-to-reset-the-filesystem-cache.md)  
Proporciona la información necesaria para restablecer la caché del sistema de archivos.

<a href="" id="how-to-change-the-size-of-the-filesystem-cache"></a>[Cómo cambiar el tamaño de la caché de sistema de archivos](how-to-change-the-size-of-the-filesystem-cache.md)  
Explica cómo se puede cambiar el tamaño de la memoria caché.

<a href="" id="how-to-use-the-cache-space-management-feature"></a>[Cómo usar la función de administración de espacio de caché](how-to-use-the-cache-space-management-feature.md)  
Describe cómo configurar la característica de administración de espacio en caché.

<a href="" id="how-to-configure-the-client-log-file"></a>[Cómo configurar el archivo de registro del cliente](how-to-configure-the-client-log-file.md)  
Describe los diversos valores de las claves del registro que controlan el archivo de registro del cliente y cómo se pueden cambiar.

<a href="" id="how-to-configure-user-permissions"></a>[Cómo configurar los permisos de usuario](how-to-configure-user-permissions.md)  
Identifica la clave del registro que controla los permisos de usuario y proporciona ejemplos de cómo puede cambiar algunos permisos.

<a href="" id="how-to-configure-the-client-for-application-package-retrieval"></a>[Cómo configurar al cliente para la recuperación del paquete de aplicación](how-to-configure-the-client-for-application-package-retrieval.md)  
Explica cómo configurar el cliente para recuperar asociaciones de tipo de archivo, iconos y contenido del paquete de diferentes orígenes, y ofrece varios ejemplos de formato de ruta de acceso correcto.

<a href="" id="how-to-configure-the-client-for-disconnected-operation-mode"></a>[Cómo configurar al cliente para el modo de operación desconectado](how-to-configure-the-client-for-disconnected-operation-mode.md)  
Proporciona información sobre cómo configurar las diversas opciones asociadas al modo de operaciones sin conexión.

<a href="" id="how-to-configure-shortcut-and-file-type-association-behavior"></a>[Cómo configurar el acceso directo y el comportamiento de las asociaciones de tipos de archivo](how-to-configure-shortcut-and-file-type-association-behavior-46-only.md)  
Describe los valores de la clave del registro que controlan los accesos directos y las asociaciones de tipos de archivo en el cliente de App-V y proporciona detalles sobre cómo configurarlos.

## Temas relacionados


[Cliente de virtualización de aplicaciones](application-virtualization-client.md)

 

 





