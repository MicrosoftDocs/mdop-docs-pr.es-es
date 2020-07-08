---
title: Aplicación de revisiones en MBAM 2.5 SP1
description: Aplicación de revisiones en MBAM 2.5 SP1
ms.author: ppriya-msft
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 8/30/2018
ms.openlocfilehash: 71f840ce4d57a0698289128f92b9d760ca14ddfc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824190"
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
