---
title: Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden acceder a la red de entrega de contenido de Microsoft
description: Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden acceder a la red de entrega de contenido de Microsoft
author: dansimp
ms.assetid: 90ee76db-9876-41b5-994a-118556d5ed3b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ffce3dd023cb6ff9bd5cdb13ea789b348661de24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824491"
---
# Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden acceder a la red de entrega de contenido de Microsoft


Siga estas instrucciones si los equipos cliente de su organización no tienen acceso a la red de entrega de contenido (CDN) de Microsoft Ajax.

**Por qué necesita configurar esto:**

Los equipos cliente necesitan tener acceso a la red CDN, lo que proporciona al portal de autoservicio el acceso necesario a determinados archivos de JavaScript. Si no configura el portal de autoservicio cuando los equipos cliente no pueden obtener acceso a la red CDN, solo se mostrará el nombre de la empresa y la cuenta en la que se inicia sesión en el usuario final. No se mostrará ningún mensaje de error.

**Nota:**  En MBAM 2,5 SP1, los archivos JavaScript se incluyen en el producto y no es necesario que siga las instrucciones de esta sección para configurar el SSP para que admita clientes que no tienen acceso a Internet.

 

**Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden obtener acceso a la red CDN**

1. Descargue los siguientes archivos JavaScript desde la red CDN:

   -   [jQuery-1.10.2.min.js](https://go.microsoft.com/fwlink/?LinkID=390515)

   -   [jQuery.validate.min.js](https://go.microsoft.com/fwlink/?LinkID=390516)

   -   [jQuery.validate.unobtrusive.min.js](https://go.microsoft.com/fwlink/?LinkID=390517)

2. Copie los archivos de JavaScript en el directorio **scripts** del portal de autoservicio. Este directorio se encuentra en <em> &lt; MBAM de autoservicio de directorio de instalación de autoservicio &gt; \\ </em> Website\\Scripts.

3. Abra el administrador de Internet Information Services (IIS).

4. Expanda **sitios** &gt; **Microsoft BitLocker administración y supervisión**, y resalte **SelfService**.

   **Nota**  
   *SelfService* es el nombre del directorio virtual predeterminado. Si ha elegido un nombre diferente para este directorio durante la configuración, recuerde reemplazar *SelfService* en estas instrucciones con el nombre que ha elegido.

     

5. En el panel central, haga doble clic en configuración de la **aplicación**.

6. Para cada elemento de la siguiente lista, edite la configuración de la aplicación para que haga referencia a la nueva ubicación mediante reemplazo/ &lt; *directorio virtual* &gt; /con/SelfService/(o el nombre que haya elegido durante la configuración). Por ejemplo, la ruta de acceso del directorio virtual será similar a/selfservice/Scripts/jQuery-1.10.2.min.js.

   -   jQueryPath:/ &lt; *directorio virtual* &gt; /scripts/jQuery-1.10.2.min.js

   -   jQueryValidatePath:/ &lt; *directorio virtual* &gt; /scripts/jQuery.validate.min.js

   -   jQueryValidateUnobtrusivePath:/ &lt; *directorio virtual* &gt; /scripts/jQuery.validate.unobtrusive.min.js



## Temas relacionados


[Cómo configurar las aplicaciones web de MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





