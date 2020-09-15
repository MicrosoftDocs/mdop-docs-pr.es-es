---
title: Aplicación de revisiones en MBAM 2.5 SP1
description: Aplicación de revisiones en MBAM 2.5 SP1
ms.author: dansimp
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: ea564d93a3eec6a46ec7d4c1be0f794abba9c93e
ms.sourcegitcommit: 8ecbf818a6ff2ddafd80b93614c01256484737ad
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/14/2020
ms.locfileid: "11014994"
---
# Aplicación de revisiones en MBAM 2.5 SP1
En este tema se describe el proceso de aplicación de las revisiones para Microsoft BitLocker Administration and Monitoring (MBAM) Server 2,5 SP1

### Antes de empezar, descargue la última versión de Microsoft BitLocker Administration and Monitoring (MBAM) Server 2,5 SP1
[Paquete de optimización de escritorio](https://www.microsoft.com/download/details.aspx?id=57157)

> [!NOTE]
> Para obtener más información sobre las versiones de hotfix, vea el [gráfico de versión de MBAM](https://docs.microsoft.com/archive/blogs/dubaisec/mbam-version-chart).

#### Pasos para actualizar el servidor de MBAM para el entorno de MBAM existente 
1. Para quitar MBAM característica de servidor (para ello, abre la herramienta de configuración del servidor de MBAM y selecciona quitar características).
2. Quitar MDOP MBAM desde el panel de control | Programas y características.
3. Instale los componentes del servidor RTM de MBAM 2,5 SP1.
4. Instale el paquete acumulativo de revisiones MBAM 2,5 SP1 más reciente.
5. Configure las características de MBAM con MBAM Server Configurator.

#### Pasos para instalar el nuevo Hotfix del servidor MBAM 2,5 SP1
Haga referencia al documento para obtener una [instalación de servidor nueva](deploying-the-mbam-25-server-infrastructure.md).
