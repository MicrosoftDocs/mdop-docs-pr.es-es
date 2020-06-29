---
title: Cómo implementar al cliente MBAM en equipos portátiles o de escritorio
description: Cómo implementar al cliente MBAM en equipos portátiles o de escritorio
author: dansimp
ms.assetid: 3a7639e0-468e-4496-8be2-ed29b8e07c53
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b67533a555da4dabec6654ed3f95f91ad8d37bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824480"
---
# Cómo implementar al cliente MBAM en equipos portátiles o de escritorio


En este tema se explica cómo implementar el cliente MBAM en los equipos de los usuarios finales. Puede implementar el cliente de MBAM a través de un sistema electrónico de distribución de software, como servicios de dominio de Active Directory o administrador de MicrosoftSystemCenterConfiguration.

Para implementar el cliente de MBAM como parte de una implementación de Windows, consulte [Cómo habilitar BitLocker con MBAM como parte de una implementación de Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md).

Antes de iniciar la implementación del cliente de MBAM, revise las [configuraciones admitidas de MBAM 2,5](mbam-25-supported-configurations.md).

**Para implementar el cliente de MBAM en equipos portátiles o de escritorio**

1.  Ubique los archivos de instalación del cliente MBAM que se proporcionan con el software MBAM.

2.  Use servicios de dominio de Active Directory o una herramienta de implementación de software empresarial como el administrador de MicrosoftSystemCenterConfiguration para implementar el paquete de Windows Installer en equipos de destino.

3.  Establezca la configuración de distribución o la configuración de directiva de grupo para ejecutar el archivo de instalación del cliente MBAM.

    Después de una instalación correcta, el cliente de MBAM aplica la configuración de directiva de grupo que se recibe de un controlador de dominio para iniciar el cifrado de unidad BitLocker y las funciones de administración.

    **Importante**  El cliente MBAM no inicia las acciones de cifrado de unidad BitLocker si una conexión de protocolo de escritorio remoto está activa. Todas las conexiones de consola remota deben cerrarse y un usuario debe haber iniciado sesión en una sesión de consola física antes de que se inicie el cifrado de unidad BitLocker.

     


## Temas relacionados
[Implementación de cliente de MBAM 2.5](deploying-the-mbam-25-client.md)

[Planificación para la implementación de clientes de MBAM 2.5](planning-for-mbam-25-client-deployment.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





