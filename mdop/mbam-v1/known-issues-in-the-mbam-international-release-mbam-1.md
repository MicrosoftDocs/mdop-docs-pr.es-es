---
title: Problemas conocidos de la versión internacional de MBAM.
description: Problemas conocidos de la versión internacional de MBAM.
author: dansimp
ms.assetid: bbf888dc-93c1-4323-b43c-0ded098e9b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af32551135ff297d25930f94b40bf04c0fcaaafe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825790"
---
# Problemas conocidos de la versión internacional de MBAM.

Esta sección contiene problemas conocidos con la versión internacional de administración y supervisión de Microsoft BitLocker (MBAM).

## Problemas conocidos de la versión internacional de MBAM.

### El proceso de instalación no especifica Update

Después de actualizar el servidor o servidores de administración de Microsoft BitLocker, el programa de instalación no indica que se está instalando una actualización.

**Solución alternativa**: ninguno.

### Certificados que se usan para el rol de servidor administración y supervisión

Si está usando un certificado para la autenticación entre servidores MBAM, después de actualizar el servidor de administración y supervisión de MBAM debe asegurarse de que el certificado es válido y no ha sido revocado ni ha expirado.

**Solución alternativa**: ninguno.

### MBAM Svclog archivo llenado de disco

Si ha seguido el [artículo 2668170 de Knowledge Base](https://go.microsoft.com/fwlink/?LinkID=247277), es posible que tenga que repetir los pasos de KB después de instalar esta actualización.

**Solución alternativa**: ninguno.

## Temas relacionados

[Implementación de la actualización de versión de idioma de MBAM 1.0](deploying-the-mbam-10-language-release-update.md)

 

 





