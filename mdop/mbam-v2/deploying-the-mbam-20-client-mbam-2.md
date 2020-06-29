---
title: Implementación de cliente de MBAM 2.0
description: Implementación de cliente de MBAM 2.0
author: dansimp
ms.assetid: 3dd584fe-2a54-40f0-9bab-13ea74040b01
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa42c8ab3adc273f0e00ba56a59f487deba89c6f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823450"
---
# Implementación de cliente de MBAM 2.0


El cliente de administración y supervisión de Microsoft BitLocker permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa. El cliente de BitLocker se puede integrar en una organización implementando el cliente a través de un sistema de distribución de software electrónico, como servicios de dominio de Active Directory, o bien cifrando directamente los equipos cliente como parte del proceso de creación de imágenes inicial.

Según el momento en que implemente el cliente de supervisión y administración de BitLocker de Microsoft, puede habilitar el cifrado de BitLocker en un equipo de su organización antes de que el usuario reciba el equipo o, posteriormente, configurando la Directiva de grupo e implementando el software de cliente de MBAM mediante un sistema de implementación de software empresarial.

## Implementar el cliente de MBAM en equipos portátiles o de escritorio


Después de configurar la Directiva de grupo, puede usar un producto del sistema de implementación de software empresarial como Microsoft System Center Configuration Manager 2012 o los servicios de dominio de Active Directory para implementar los archivos de Windows Installer de la instalación de cliente MBAM en equipos de destino. Puede implementar el cliente con los archivos de 32 bits o 64 bits MbamClientSetup.exe o los archivos de MBAMClient.msi de 32 bits o 64, que se proporcionan con el software MBAM. Para obtener más información sobre cómo implementar MBAM objetos de directiva de grupo, consulte [implementar objetos de directiva de grupo de MBAM 2,0](deploying-mbam-20-group-policy-objects-mbam-2.md).

[Cómo implementar al cliente MBAM en equipos portátiles o de escritorio](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-2.md)

## Implementar el cliente de MBAM como parte de una implementación de Windows


En las organizaciones donde los equipos se reciben y configuran de forma centralizada, puede instalar el cliente de MBAM para administrar el cifrado de BitLocker en cada equipo antes de que se escriban datos de usuario. La ventaja de este proceso es que cada equipo es entonces compatible con el cifrado de BitLocker. Este método no depende de la acción del usuario porque el administrador ya cifró el equipo. Una de las suposiciones clave para este escenario es que la Directiva de la organización instala una imagen de Windows corporativa antes de que el equipo se entregue al usuario. Si la Directiva de grupo se ha configurado para requerir un PIN, se les pedirá a los usuarios que configuren un PIN después de que reciban la Directiva de grupo.

[Cómo implementar al cliente MBAM como parte de una implementación de Windows](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-2.md)

## Cómo usar una línea de comandos para instalar el cliente MBAM.


En esta sección se explica cómo instalar el cliente de MBAM mediante una línea de comandos.

[Cómo usar una línea de comandos para instalar el cliente MBAM.](how-to-use-a-command-line-to-install-the-mbam-client.md)

## Otros recursos para implementar el cliente de MBAM


Implementación de la planificación de [MBAM 2,0](deploying-mbam-20-mbam-2.md)[para la implementación de cliente de MBAM 2,0](planning-for-mbam-20-client-deployment-mbam-2.md)

 

 





