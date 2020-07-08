---
title: Administrar impresoras en un área de trabajo de MED-V
description: Administrar impresoras en un área de trabajo de MED-V
author: dansimp
ms.assetid: ba0a65ad-444f-4d18-95eb-8b9fa1a3ffba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bc7a62075c95e8816a425eff89ffb992f1185d04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826120"
---
# Administrar impresoras en un área de trabajo de MED-V


En Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, la redirección de impresora proporciona a los usuarios finales una experiencia de impresión coherente entre la máquina virtual MED-V y el equipo host.

Este tema proporciona información sobre cómo administrar la impresión en un área de trabajo de MED-V.

## Administración de impresoras en áreas de trabajo de MED-V


En la mayoría de los casos, MED-V controla automáticamente el redireccionamiento de la impresora. Después de que finalice la configuración por primera vez, MED-V identifica todas las impresoras de red instaladas en el host, recupera los drivers correspondientes del servidor de impresión de red y, si lo encuentra, instala los drivers relevantes en el área de trabajo de MED-V. Una vez que se han encontrado e instalado todos los drivers, MED-V reinicia el área de trabajo de MED-V. Solo después de que se reinicie el área de trabajo de MED-V, las impresoras de host estarán presentes y disponibles en el invitado, generalmente en unos minutos.

**Nota:**  Si las aplicaciones se ejecutan en el área de trabajo de MED-V, se solicita al usuario final que continúe o pospongala hasta más tarde. Si no se está ejecutando ninguna aplicación, el reinicio es automático y no se muestra al usuario final.

 

Cada vez que se reinicie MED-V, se comprueba si hay instaladas nuevas impresoras en el host y, si las encuentra, se recuperan los drivers correspondientes del servidor de impresión de red y se instalan en el invitado. A continuación, MED-V reinicia el área de trabajo MED-V como la primera vez que se completó la configuración.

**Importante**  Una vez que los drivers correspondientes estén instalados en el invitado, las impresoras solo estarán visibles en el invitado después de que se reinicie.

 

Si en cualquier momento no se puede ubicar ni instalar un controlador, debe instalarlo manualmente en el invitado para que la impresora de red esté disponible para el usuario final.

La siguiente lista ofrece instrucciones adicionales:

**MED-V solo administra impresoras de red**. Los drivers de las impresoras instaladas de forma local en el host no se instalan automáticamente en el invitado.

**MED-V solo instala drivers de impresora si se encuentran en el servidor de impresión**. Si no se encuentra, los drivers de impresora deben instalarse manualmente.

**Las impresoras instaladas manualmente en el invitado no son accesibles para el host**. De forma predeterminada, MED-V solo admite el redireccionamiento de impresoras desde el invitado al host.

**ADVERTENCIA**  Si una impresora se instala manualmente en el invitado y la misma impresora se instala posteriormente en el host, el resultado es que la impresora se instala dos veces en el invitado. Para evitar esta situación, una práctica recomendada de MED-V es administrar el redireccionamiento de la impresora de una manera: deshabilite la redirección e instale las impresoras manualmente en el invitado, o bien habilite el redireccionamiento y no instale las impresoras de forma manual en el invitado.

 

## Temas relacionados


[Administrar la configuración del área de trabajo de MED-V](manage-med-v-workspace-settings.md)

 

 





