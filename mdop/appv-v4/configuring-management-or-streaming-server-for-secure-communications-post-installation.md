---
title: Configuración del servidor de administración o streaming para la postinstalación de comunicaciones seguras
description: Configuración del servidor de administración o streaming para la postinstalación de comunicaciones seguras
author: dansimp
ms.assetid: 1062a213-470b-4ae2-b12f-b3e28a6ab745
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a2713f130809c431b7444f3e928a523838597a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821880"
---
# Configuración del servidor de administración o streaming para la postinstalación de comunicaciones seguras


Si no se aprovisionó el certificado adecuado antes de instalar el servidor de administración de App-V o el servidor de streaming de App-V, App-V puede configurarse para mejorar la seguridad después de la instalación inicial. Puede configurar el servidor de administración de App-V a través de la consola de administración de App-V. Sin embargo, el servidor de streaming de App-V se administra a través del registro. En cualquier caso, el certificado debe incluir el *uso de clave extendida* (EKU) adecuado para la autenticación del servidor y el servicio de red debe tener acceso de lectura a la clave privada.

## En esta sección


<a href="" id="how-to-configure-management-server-security-post-installation"></a>[Cómo configurar la postinstalación de seguridad del servidor de administración](how-to-configure-management-server-security-post-installation.md)  
Proporciona un procedimiento que se puede ejecutar después de la instalación, usando la consola de administración de App-V, para agregar el certificado y configurar el servidor de administración de App-V para mejorar la seguridad.

<a href="" id="how-to-configure-streaming-server-security-post-installation"></a>[Cómo configurar la postinstalación de seguridad del servidor de streaming](how-to-configure-streaming-server-security-post-installation.md)  
Proporciona un procedimiento que se puede ejecutar después de la instalación, para agregar el certificado y configurar el servidor de streaming de App-V para mejorar la seguridad.

<a href="" id="troubleshooting-certificate-permission-issues"></a>[Solución de problemas de permisos de certificado](troubleshooting-certificate-permission-issues.md)  
Proporciona instrucciones para la solución de problemas cuando la clave privada no se ha configurado con la ACL adecuada para el servicio de red.

 

 





