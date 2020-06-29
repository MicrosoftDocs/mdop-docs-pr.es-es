---
title: Información de solución de problemas del servidor de virtualización de aplicaciones
description: Información de solución de problemas del servidor de virtualización de aplicaciones
author: dansimp
ms.assetid: e9d43d9b-84f2-4d1b-bb90-a13740151e0c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7c98ad42a00e20900263d0598822a6381e2df1ef
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815190"
---
# Información de solución de problemas del servidor de virtualización de aplicaciones


En este tema se incluye información que puede usar para solucionar varios problemas en los servidores de virtualización de aplicaciones (App-V).

## Mensaje de advertencia 25017 en el registro de instalación después de instalar el servidor


Es posible que encuentre el siguiente mensaje en el registro de configuración del servidor después de la instalación.

*ADVERTENCIA 25017. El programa de instalación no pudo crear el objeto de marcador de Active Directory para el servidor. La cuenta que se usó para instalar no tenía los derechos suficientes para escribir en Active Directory o Active Directory no estaba disponible.*

El instalador de la administración de App-V o de Streaming Server crea una entrada de punto de conexión de servicio bajo el objeto de equipo en servicios de dominio de Active Directory (ADDS) que corresponde al equipo en el que está instalado el servidor si la cuenta usada para ejecutar el instalador tiene los derechos apropiados. Si no crea esta entrada, no se producirá un error en la instalación y esto no debería afectar al funcionamiento del producto. La causa probable de cualquier error es que la cuenta de usuario usada para ejecutar la instalación no tenía suficientes derechos para escribir en ADDS. Aunque el registro del servidor de App-V en ADDS es opcional, una de las ventajas de hacerlo permite a las herramientas de administración centralizadas ubicar el servidor de App-V con fines de inventario y administración.

## Temas relacionados


[Servidor de virtualización de aplicaciones](application-virtualization-server.md)

 

 





