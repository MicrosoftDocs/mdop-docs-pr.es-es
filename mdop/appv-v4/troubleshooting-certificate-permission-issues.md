---
title: Solución de problemas de permisos de certificado
description: Solución de problemas de permisos de certificado
author: dansimp
ms.assetid: 06b8cbbc-93fd-44aa-af39-2d780792d3c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 728c35b9f51c8f2e18db8acd63708c70bb5d3100
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815210"
---
# Solución de problemas de permisos de certificado


Después de la instalación de App-V 4.5, si la clave privada no se ha configurado con la ACL adecuada para el servicio de red, se registra un evento en el registro de eventos de NT y se coloca una entrada en el `Sft-server.log` archivo.

## Mensajes de error


### Windows Server2003

IDENTIFICADOR de evento 36870: se ha producido un error grave al intentar obtener acceso a la clave privada de la credencial del servidor SSL. El código de error devuelto del módulo criptográfico es 0x80090016.

### Windows Server2008

IDENTIFICADOR de evento 36870: se ha producido un error grave al intentar obtener acceso a la clave privada de la credencial del servidor SSL. El código de error devuelto del módulo criptográfico es 0x8009030d.

## SFT-Server. log


El error siguiente se coloca en el `sft-server.log` archivo que se encuentra en el `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` Directorio:

No se pudo cargar el certificado. Código de error \ [-2146893043 \]. Asegúrese de que la cuenta de servicio de red tiene acceso adecuado al certificado y al archivo de clave privada correspondiente.

 

 





