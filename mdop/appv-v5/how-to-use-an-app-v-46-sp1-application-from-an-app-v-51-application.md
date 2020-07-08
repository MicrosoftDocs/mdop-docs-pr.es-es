---
title: Cómo usar una aplicación de App-V 4,6 desde una aplicación de App-V 5,1
description: Cómo usar una aplicación de App-V 4,6 desde una aplicación de App-V 5,1
author: dansimp
ms.assetid: 909b4391-762b-4988-b0cf-32b67f1fcf0e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: c0d308dcae33b02c089c101ffcd5041b2e665f59
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813638"
---
# Cómo usar una aplicación de App-V 4,6 desde una aplicación de App-V 5,1

*Nota:** App-V 4,6 ha salido del soporte técnico estándar. Lo siguiente se aplica a un paquete de App-V 4,6 SP3.

Use el siguiente procedimiento para ejecutar una aplicación de App-V 4.6 con aplicaciones de App-V 5,1 en un cliente independiente.

**Nota:**  En este procedimiento se supone que está ejecutando la última versión de App-V 4,6.

**Para ejecutar aplicaciones en un cliente independiente**

1.  Seleccione dos aplicaciones de su entorno que se pueden abrir entre sí. Por ejemplo, Microsoft Outlook y Adobe Acrobat Reader. Puede acceder a un archivo adjunto de correo electrónico creado con Adobe Acrobat.

2.  Convierta los paquetes o cree un nuevo paquete para cualquiera de las aplicaciones con el formato de App-V 5,1. Para obtener más información sobre la conversión de paquetes, consulte [Cómo migrar puntos de extensión desde un paquete de App-v 4,6 a un paquete de App-v 5,1 convertido para todos los usuarios de un equipo específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md) o [Cómo migrar puntos de extensión desde un paquete de app-v 4,6 a App-v 5,1 para un usuario específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md).

3.  Agregue y aprovisione el paquete con la consola de administración de App-V 5,1. Para obtener más información sobre agregar y aprovisionar paquetes, consulte [Cómo agregar o actualizar paquetes mediante la consola de administración](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md) y [Cómo configurar el acceso a los paquetes mediante la consola de administración](how-to-configure-access-to-packages-by-using-the-management-console-51.md).

4.  La aplicación convertida ahora se ejecuta con App-V 5,1 y puede abrir una aplicación de la otra. Por ejemplo, si ha convertido un paquete de Microsoft Office en un paquete de App-V 5,1 y Adobe Acrobat aún se está ejecutando como un paquete de App-V 4.6, puede abrir un archivo adjunto de Adobe Acrobat Reader con Microsoft Outlook.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)

 

 





