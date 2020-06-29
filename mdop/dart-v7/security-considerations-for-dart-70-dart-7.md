---
title: Consideraciones de seguridad para DaRT 7.0
description: Consideraciones de seguridad para DaRT 7.0
author: dansimp
ms.assetid: 52ad7e6c-c169-4ba4-aa76-56335a585eb8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739c0319195aeb26e38d55ffe01d14b623de7f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822731"
---
# Consideraciones de seguridad para DaRT 7.0


Microsoft Diagnostics and Recovery Toolset (DaRT) 7 incluye una funcionalidad que permite a un administrador ejecutar las herramientas de DaRT de manera remota para resolver problemas en un equipo de usuario final. En versiones anteriores de DaRT, un técnico o administrador de soporte técnico tenía que estar físicamente en un equipo de usuario final y arrancar en DaRT usando el CD o el DVD que incluía la imagen de recuperación de DaRT. Ahora, el técnico o administrador del servicio de asistencia pueden realizar los mismos procedimientos de forma remota.

Además, en DaRT7, además de grabar un CD o DVD, ya puede guardar la imagen de la organización internacional para la estandarización (ISO) en una unidad flash USB. También puede colocar la imagen ISO en una red o incluir su contenido como una partición de recuperación en el disco duro de un equipo.

La característica de **conexión remota** de DaRT7 permite a los usuarios finales acceder a DART mediante uno de estos nuevos métodos de implementación. Por lo tanto, pueden comenzar más fácilmente con DaRT y acceder a las herramientas de DaRT.

Las nuevas funcionalidades de DaRT7 ofrecen mucha más flexibilidad en el uso de DaRT en su empresa. Sin embargo, también crean su propio conjunto de problemas de seguridad que debe solucionarse. Le recomendamos que considere las siguientes sugerencias de seguridad al configurar DaRT.

## Para ayudar a mantener la seguridad al crear la imagen de recuperación de DaRT


Al crear la imagen de recuperación de DaRT, puede seleccionar las herramientas que desea incluir. Por razones de seguridad, es posible que desee restringir el acceso de los usuarios finales a las herramientas de DaRT más eficaces, como el barrido de disco y el locksmith. En DaRT7, puede deshabilitar determinadas herramientas durante la configuración y seguirlas disponibles para los agentes del Departamento de soporte técnico cuando el usuario final inicia la característica de conexión remota.

Incluso puede configurar la imagen de DaRT de modo que la opción para iniciar una sesión de conexión remota sea la única herramienta disponible para el usuario final.

**Importante**  Una vez establecida la conexión remota, todas las herramientas que incluyó en la imagen de recuperación, incluidas las que no están disponibles para el usuario final, estarán disponibles para el agente de asistencia que trabaja en el equipo del usuario final.

 

Para obtener más información sobre cómo incluir herramientas en la imagen de recuperación de DaRT, consulte [Cómo usar el Asistente de imagen de recuperación de DART para crear la imagen de recuperación](how-to-use-the-dart-recovery-image-wizard-to-create-the-recovery-image-dart-7.md).

## Para ayudar a mantener la seguridad mediante el cifrado de la imagen de recuperación de DaRT


Si usa una de las opciones de implementación nuevas en DaRT7, por ejemplo, guardar en una unidad flash USB o crear una partición remota o una partición de recuperación, puede incluir el método preferido de cifrado de unidad de su empresa en la ISO. Esto le ayudará a asegurarse de que un usuario final no pueda usar la funcionalidad de DaRT en caso de que obtenga acceso a la imagen de recuperación. Además, se asegurará de que los usuarios no autorizados no puedan iniciar en DaRT en equipos que pertenezcan a otra persona.

El método de cifrado debe implementarse y habilitarse en todos los equipos.

**Nota:**  DaRT7 es compatible de forma nativa con BitLocker.

 

## Para ayudar a mantener la seguridad entre dos equipos durante una conexión remota


De forma predeterminada, la comunicación entre dos equipos que han establecido una sesión de **conexión remota** no se puede cifrar. Por lo tanto, para ayudar a mantener la seguridad entre los dos equipos, recomendamos que ambos equipos formen parte de la misma red.

## Temas relacionados


[Operaciones para DaRT 7.0](operations-for-dart-70-new-ia.md)

 

 





