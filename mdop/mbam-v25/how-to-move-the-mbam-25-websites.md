---
title: Cómo mover los sitios web de MBAM 2.5
description: Cómo mover los sitios web de MBAM 2.5
author: dansimp
ms.assetid: 71af9a54-c27b-408f-9d75-37c0d02e730e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa5bd8156810b3dccc1588b4dfd4cadd96fd22fb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825750"
---
# Cómo mover los sitios web de MBAM 2.5


Use estos procedimientos para mover los siguientes sitios web de MBAM de un equipo a otro, es decir, para mover las siguientes características del servidor a al servidor B:

-   Sitio web de administración y supervisión

-   Portal de autoservicio

**Importante**  Durante la configuración de ambos sitios web, debe proporcionar la misma cadena de conexión, la dirección URL de los informes, las cuentas de grupo y la cuenta de dominio del grupo de aplicaciones de servicio web como las que está usando actualmente. Si no usa los mismos valores, no podrá obtener acceso a algunos de los servidores. Para obtener los valores actuales, use el cmdlet **Get-MbamWebApplication** de Windows PowerShell.

 

**Para mover el sitio web de administración y supervisión a otro servidor**

1.  En el servidor B, instale el software de servidor MBAM 2,5. Para obtener instrucciones, consulte [Installing the MBAM 2,5 Server Software](installing-the-mbam-25-server-software.md).

2.  En el servidor B, inicie el Asistente para la configuración del servidor de MBAM, haga clic en **Agregar nuevas características**y, a continuación, seleccione solo la característica **sitio web de administración y supervisión** .

    También puede usar el cmdlet **enable-MbamWebApplication** de Windows PowerShell para configurar el sitio web de administración y supervisión.

    Para obtener instrucciones sobre cómo configurar el sitio web de administración y supervisión, consulte [Cómo configurar las aplicaciones Web de MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).

**Para mover el portal de autoservicio a otro servidor**

1.  En el servidor B, instale el software de servidor MBAM 2,5. Para obtener instrucciones, consulte [Installing the MBAM 2,5 Server Software](installing-the-mbam-25-server-software.md).

2.  En el servidor B, inicie el Asistente para la configuración del servidor de MBAM, haga clic en **Agregar nuevas características**y, a continuación, seleccione solo la característica del **portal de autoservicio** .

    Como alternativa, puede usar el cmdlet **enable-MbamWebApplication** de Windows PowerShell para configurar el portal de autoservicio.

    Para obtener instrucciones sobre cómo configurar el sitio web de administración y supervisión, consulte [Cómo configurar las aplicaciones Web de MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).

3.  Si los equipos cliente de su organización no tienen acceso a la red de entrega de contenido de Microsoft, también tendrá que mover los archivos JavaScript. Consulte [Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden obtener acceso a la red de entrega de contenido de Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) para obtener más información.

4.  Personalizar el portal de autoservicio para su organización. Use las instrucciones de [Personalización del portal de autoservicio para que su organización](customizing-the-self-service-portal-for-your-organization.md) Revise las personalizaciones actuales y para configurar ajustes personalizados en el portal de autoservidor en el servidor B.



## Temas relacionados


[Cómo configurar las aplicaciones web de MBAM 2.5](how-to-configure-the-mbam-25-web-applications.md)

[Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[Movimiento de funciones de MBAM 2.5 a otro servidor](moving-mbam-25-features-to-another-server.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





