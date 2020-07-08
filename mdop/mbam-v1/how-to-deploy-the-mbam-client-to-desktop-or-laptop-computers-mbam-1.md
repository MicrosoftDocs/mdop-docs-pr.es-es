---
title: Cómo implementar al cliente MBAM en equipos portátiles o de escritorio
description: Cómo implementar al cliente MBAM en equipos portátiles o de escritorio
author: dansimp
ms.assetid: f32927a2-4c05-4da8-acca-1108d1dfdb7e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ce4f8597cc182c037983a89efd60c5ef935712ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825541"
---
# Cómo implementar al cliente MBAM en equipos portátiles o de escritorio


El cliente de administración y supervisión de Microsoft BitLocker permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa. El cliente de MBAM se puede integrar en una organización implementando el cliente a través de herramientas, como servicios de dominio de Active Directory o una herramienta de implementación de software empresarial, como MicrosoftSystemCenter2012 ConfigurationManager.

**Nota:**  Para consultar los requisitos del sistema del cliente de MBAM, consulte [configuraciones compatibles con MBAM 1,0](mbam-10-supported-configurations.md).

 

**Para implementar el cliente de MBAM en equipos portátiles o de escritorio**

1.  Ubique los archivos de instalación del cliente MBAM que se proporcionan con el software MBAM.

2.  Implemente el paquete de Windows Installer en equipos de destino con servicios de dominio de Active Directory o una herramienta de implementación de software empresarial, como MicrosoftSystemCenter2012 ConfigurationManager.

    **Nota:**  No debe usar una directiva de grupo para implementar el paquete de Windows Installer.

     

3.  Configure la configuración de distribución o la Directiva de grupo para ejecutar el archivo de instalación del cliente MBAM. Después de una instalación correcta, el cliente de MBAM aplica la configuración de directiva de grupo que se recibe de un controlador de dominio para iniciar las funciones de cifrado y administración de BitLocker. Para obtener más información sobre la configuración de directiva de grupo de MBAM, consulte [requisitos de la Directiva de grupo de MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).

    **Importante**  El cliente de MBAM no iniciará las acciones de cifrado de BitLocker si una conexión de protocolo de escritorio remoto está activa. Todas las conexiones de consola remota deben cerrarse antes de que se inicie el cifrado de BitLocker.

     

## Temas relacionados


[Implementación de cliente de MBAM 1.0](deploying-the-mbam-10-client.md)

 

 





