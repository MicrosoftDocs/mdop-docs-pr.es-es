---
title: Consideraciones de seguridad para DaRT 10
description: Consideraciones de seguridad para DaRT 10
author: dansimp
ms.assetid: c653daf1-f12a-4667-98cc-f0c89fa38e3f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f10ecf81021d41fbc08b288573c05a8d64c47d7c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823051"
---
# Consideraciones de seguridad para DaRT 10


Este tema contiene una breve descripción general sobre las cuentas y grupos, los archivos de registro y otras consideraciones relacionadas con la seguridad para Microsoft Diagnostics and Recovery Toolset (DaRT) 10. Para obtener más información, siga los vínculos de este artículo.

## Consideraciones generales de seguridad


**Comprender los riesgos de seguridad**. DaRT 10 incluye una funcionalidad que permite a un administrador o a un trabajador del Departamento de soporte ejecutar las herramientas de DaRT de manera remota para resolver problemas en un equipo de usuario final. Además, puede guardar la imagen de la organización internacional de normalización (ISO) en una unidad flash USB o colocar la imagen ISO en una red para incluir su contenido como una partición de recuperación en el disco duro de un equipo. Estas capacidades proporcionan flexibilidad, pero también crean posibles riesgos de seguridad que se deben tener en cuenta al configurar DaRT.

**Proteja físicamente sus equipos**. Cuando los administradores y los trabajadores del Departamento de soporte no estén físicamente en sus equipos, deberían bloquear sus equipos y usar un protector de pantalla seguro.

**Aplique las actualizaciones de seguridad más recientes a todos los equipos**. Manténgase informado acerca de las nuevas actualizaciones de los sistemas operativos mediante la suscripción al servicio de notificación de seguridad ( <https://go.microsoft.com/fwlink/?LinkId=28819> ).

## Limitar el acceso de usuarios finales a las herramientas de DaRT


Al crear la imagen de recuperación de DaRT, puede seleccionar las herramientas que desea incluir. Por razones de seguridad, es posible que desee restringir el acceso de los usuarios finales a las herramientas de DaRT más eficaces, como el barrido de disco y el locksmith. En DaRT 10, puede deshabilitar determinadas herramientas durante la configuración y seguirlas disponibles para los trabajadores del servicio de asistencia cuando el usuario final inicia la característica de conexión remota.

Incluso puede configurar la imagen de DaRT de modo que la opción para iniciar una sesión de conexión remota sea la única herramienta disponible para el usuario final.

**Importante**  Una vez establecida la conexión remota, todas las herramientas que incluyó en la imagen de recuperación, incluidas las que no están disponibles para el usuario final, estarán disponibles para cualquier trabajador del servicio de asistencia al cliente que esté trabajando en el equipo del usuario final.

 

Para obtener más información sobre cómo incluir herramientas en la imagen de recuperación de DaRT, consulte [información general sobre las herramientas de DART 10](overview-of-the-tools-in-dart-10.md).

## Proteger la imagen de recuperación de DaRT


Si implementa la imagen de recuperación de DaRT guardándola en una unidad flash USB o creando una partición remota o una partición de recuperación, es posible que desee incluir el método preferido de cifrado de unidad de su empresa en la ISO. El cifrado de la ISO ayuda a garantizar que los usuarios finales no puedan usar la funcionalidad de DaRT si van a obtener acceso a la imagen de recuperación y garantiza que los usuarios no autorizados no pueden iniciar en DaRT en equipos que pertenecen a otra persona. Si usa un método de cifrado, asegúrese de implementarlo y habilitarlo en todos los equipos.

**Nota:**  DaRT 10 admite BitLocker de forma nativa.

 

Para incluir el cifrado de unidad, agregue los archivos de la solución de cifrado cuando cree la imagen de recuperación. La solución de cifrado debe poder ejecutarse en WinPE. Los usuarios finales que arrancan a partir de la ISO pueden acceder a esa solución de cifrado y desbloquear la unidad.

## Mantener la seguridad entre dos equipos al usar una conexión remota


De forma predeterminada, la comunicación entre dos equipos que han establecido una sesión de **conexión remota** no se puede cifrar. Por lo tanto, para ayudar a mantener la seguridad entre los dos equipos, recomendamos que ambos equipos formen parte de la misma red.

## Temas relacionados


[Seguridad y privacidad para DaRT 10](security-and-privacy-for-dart-10.md)

 

 





