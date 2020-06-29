---
title: Actualización de MED-V 2.0
description: Actualización de MED-V 2.0
author: dansimp
ms.assetid: beea2f54-42d7-4a17-98e0-d243a8562265
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 62e8987ec511783422b8dd336dd4f3be2008c9b2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823731"
---
# Actualización de MED-V 2.0


Ayude a proteger el sistema aplicando las actualizaciones de seguridad adecuadas para Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Actualización de MED-V


Puede actualizar MED-V de forma interactiva, por el usuario final o silenciosamente usando un sistema electrónico de distribución de software. La instalación del agente de host MED-V actualiza el agente de host MED-V y, a continuación, actualiza el área de trabajo MED-V si es necesario. El agente de host MED-V y el agente invitado se mantienen sincronizados. Si las aplicaciones se ejecutan desde el área de trabajo de MED-V mientras se actualiza el agente de host MED-V, se debe reiniciar el equipo host para completar la actualización. Si no se está ejecutando ninguna aplicación, MED-V se reinicia automáticamente y la actualización se completa sin reiniciar el equipo host.

Si está actualizando MED-V mediante un sistema de distribución de software electrónico, puede controlar el comportamiento de reinicio. Para ello, suprima el reinicio si escribe **Reboot = "ReallySuppress"** en el símbolo del sistema al instalar MED-V\_HostAgent\_Setup.exe. Después, configure el sistema electrónico de distribución de software para capturar el código de retorno de 3010 (que indica que es necesario reiniciar) y realizar el comportamiento de reinicio.

## Temas relacionados


[Referencia técnica de MED-V](technical-reference-for-med-v.md)

 

 





