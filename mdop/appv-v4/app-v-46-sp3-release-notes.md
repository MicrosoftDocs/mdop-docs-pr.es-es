---
title: Notas de la versión de App-V4.6SP3
description: Notas de la versión de App-V4.6SP3
author: dansimp
ms.assetid: 206fadeb-59cc-47b4-836f-191ab1c27ff8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: dd0b82c5e12cbe161066a7f4a4e0932cb92cca42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819791"
---
# Notas de la versión de App-V4.6SP3


Para buscar estas notas de la versión, presione CTRL + F.

Lea estas notas de la versión minuciosamente antes de instalar el sistema de administración de Microsoft Application Virtualization (App-V). Estas notas de la versión contienen información que le ayudará a instalar correctamente Application Virtualization (App-V) 4.6 SP3. Este documento contiene información que no está disponible en la documentación del producto. Si hay una diferencia entre estas notas de la versión y otra documentación de App-V, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## Protegerse contra virus y vulnerabilidades de seguridad


Para ayudar a protegerse contra virus y vulnerabilidades de seguridad, es importante instalar las últimas actualizaciones de seguridad disponibles para cualquier nuevo software que se instale. Para obtener más información, consulte el [sitio web de seguridad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problemas conocidos con Application Virtualization 4.6 SP3


Esta sección proporciona la información más actualizada sobre problemas con Microsoft Application Virtualization (App-V) 4.6 SP3. Estos problemas no aparecen en la documentación del producto y, en algunos casos, podrían contradecir la documentación del producto existente. Cuando sea posible, estos problemas se resolverán en versiones posteriores.

### No se pueden abrir hipervínculos con Internet Explorer11 en Microsoft Windows 8,1 dentro del entorno virtual

Si intenta abrir hipervínculos desde un entorno virtual, se producirá un error en Windows 8,1 con Internet Explorer 11. Esto se debe a que ahora Internet Explorer 11 se incluye con el modo de protección mejorado (EPM) habilitado de forma predeterminada y esto hace que las aplicaciones-V no puedan tener acceso a los objetos de claves de registro, archivos y puertos de comunicaciones obligatorios.

SOLUCIÓN alternativa: deshabilite EPM en Internet Explorer11 antes de abrir un paquete de App-V. Esto le permitirá abrir Internet Explorer desde el entorno virtual.

## Temas relacionados


[Acerca de Microsoft Application Virtualization4.6SP3](about-microsoft-application-virtualization-46-sp3.md)

 

 





