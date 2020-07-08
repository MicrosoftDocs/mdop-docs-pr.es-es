---
title: Implementación de cliente de MBAM 2.5
description: Implementación de cliente de MBAM 2.5
author: dansimp
ms.assetid: 0a96a0ee-f280-49d9-a244-88f4147fe9fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 375af8966c8e66a58baec5065d065891187899fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826280"
---
# Implementación de cliente de MBAM 2.5


El software cliente de supervisión y administración de Microsoft BitLocker (MBAM) permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa. El cliente de BitLocker se puede integrar en una organización implementando el cliente a través de un sistema de distribución de software electrónico, como servicios de dominio de Active Directory, o bien cifrando directamente los equipos cliente como parte del proceso de creación de imágenes inicial.

Según el momento en que implemente el software cliente de supervisión y administración de BitLocker de Microsoft, puede habilitar el cifrado de unidad BitLocker en un equipo de su organización antes de que el usuario reciba el equipo o posteriormente mediante la configuración de la Directiva de grupo e implementar el software de cliente de MBAM mediante un sistema de implementación de software empresarial.

## Implementar el cliente de MBAM en equipos portátiles o de escritorio


Una vez configurada la configuración de directiva de grupo, puede usar un producto del sistema de implementación de software empresarial como MicrosoftSystemCenter2012 ConfigurationManager o Active Directory Domain Services para implementar los archivos de Windows Installer de instalación del cliente MBAM en equipos de destino. Puede usar los archivos de 32 o 64 bits de MbamClientSetup.exe o los archivos de MBAMClient.msi de 32 bits o 64, que se proporcionan con el software de cliente de MBAM. Para obtener más información acerca de la implementación de la configuración de directiva de grupo de MBAM, consulte [implementar objetos de directiva de grupo de MBAM 2,5](deploying-mbam-25-group-policy-objects.md).

**Nota:**  A partir de MBAM 2,5 SP1, ya no se incluye un MSI aparte con el producto MBAM. Sin embargo, puede extraer el MSI del archivo ejecutable (. exe) que se incluye con el producto.

 

[Cómo implementar al cliente MBAM en equipos portátiles o de escritorio](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25.md)

## Implementar el cliente de MBAM como parte de una implementación de Windows


En las organizaciones donde los equipos se reciben y configuran de forma centralizada, puede instalar el cliente MBAM para administrar el cifrado de unidad BitLocker en cada equipo antes de que se escriban datos de usuario. La ventaja de este proceso es que cada equipo es compatible con el cifrado de unidad BitLocker. Este método no depende de la acción del usuario porque el administrador ya cifró el equipo. Una de las suposiciones clave para este escenario es que la Directiva de la organización instala una imagen de Windows corporativa antes de que el equipo se entregue al usuario. Si la configuración de directiva de grupo se ha configurado para requerir un PIN, se les pedirá a los usuarios que establezcan un PIN después de que reciban la Directiva.

[Cómo habilitar BitLocker utilizando MBAM como parte de una implementación de Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

## Cómo implementar el cliente de MBAM mediante una línea de comandos


En esta sección se explica cómo instalar el cliente de MBAM mediante una línea de comandos.

[Cómo implementar el cliente de MBAM mediante el uso de una línea de comandos](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

## Otros recursos para implementar el cliente de MBAM


[Implementación de MBAM 2.5](deploying-mbam-25.md)



## Temas relacionados


[Implementación de MBAM 2.5](deploying-mbam-25.md)

[Planificación para MBAM 2.5](planning-for-mbam-25.md)

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





