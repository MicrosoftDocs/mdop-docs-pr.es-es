---
title: Implementación de cliente de MBAM 1.0
description: Implementación de cliente de MBAM 1.0
author: dansimp
ms.assetid: f7ca233f-5035-4ff9-ab3a-f2453b4929d1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dee8c2f4a9b398c9f0797ada35e4c36610c755b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822901"
---
# Implementación de cliente de MBAM 1.0


El cliente de administración y supervisión de Microsoft BitLocker permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa. El cliente de BitLocker puede integrarse en una organización implementando el cliente a través de herramientas como Active Directory Domain Services o cifrando directamente los equipos cliente como parte del proceso de creación de imágenes inicial.

Según el momento en que implemente el cliente MBAM, puede habilitar el cifrado de BitLocker en un equipo de su organización, ya sea antes o después de que el usuario final reciba el equipo. Para controlar estos intervalos, debe configurar la Directiva de grupo e implementar el software de cliente de MBAM mediante un sistema de implementación de software empresarial.

Puede usar uno de estos métodos o ambos en su organización. Si usa ambos métodos, puede mejorar la compatibilidad, la elaboración de informes y la compatibilidad de recuperación de claves.

## Implementar el cliente de MBAM en equipos portátiles o de escritorio


Una vez configurada la Directiva de grupo, puede implementar los archivos de Windows Installer de instalación del cliente MBAM en los equipos de destino. Para ello, puede usar un producto de sistema de implementación de software empresarial como Microsoft System Center 2012 Configuration Manager o servicios de dominio de Active Directory. Los dos archivos de Windows Installer de la instalación de cliente de MBAM están MBAMClient-64bit.msi y MBAMClient-32bit.msi. Estos archivos se proporcionan con el software MBAM. Para obtener más información sobre cómo implementar MBAM objetos de directiva de grupo, consulte [implementar objetos de directiva de grupo de MBAM 1,0](deploying-mbam-10-group-policy-objects.md).

[Cómo implementar al cliente MBAM en equipos portátiles o de escritorio](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-1.md)

## Implementar el cliente de MBAM como parte de una implementación de Windows


En algunas organizaciones, los nuevos equipos se reciben y configuran de forma centralizada. Esta situación permite a los administradores instalar el cliente de MBAM para administrar el cifrado de BitLocker en cada equipo antes de que los datos de usuario se escriban en el equipo. Este enfoque ayuda a garantizar que los equipos estén correctamente cifrados, ya que el administrador realiza la acción sin depender de la acción del usuario final. Una de las suposiciones clave para este escenario es que la Directiva de la organización instala una imagen de Windows corporativa antes de que el equipo se entregue al usuario.

[Cómo implementar al cliente MBAM como parte de una implementación de Windows](how-to-deploy-the-mbam-client-as-part-of-a-windows-deployment-mbam-1.md)

## Otros recursos para implementar el cliente de MBAM


[Implementación de MBAM 1.0](deploying-mbam-10.md)

[Planificación para la implementación de clientes de MBAM 1.0](planning-for-mbam-10-client-deployment.md)

 

 





