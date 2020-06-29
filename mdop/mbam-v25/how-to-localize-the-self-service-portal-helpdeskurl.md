---
title: Cómo localizar el portal de autoservicio "HelpdeskURL"
description: Cómo localizar el portal de autoservicio "HelpdeskURL"
author: dansimp
ms.assetid: 86798460-077b-459b-8d54-4b605e07d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0d7ec4ce87bbe5aab56e9fa877ced5f51625a5dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826710"
---
# Cómo localizar el portal de autoservicio "HelpdeskURL"


Puede configurar una versión localizada de la dirección URL del portal de autoservicio para que se muestre a los usuarios finales de forma predeterminada. La dirección URL del portal de autoservicio se representa mediante el parámetro **HelpdeskURL**.

Si crea una versión localizada, tal y como se describe en las siguientes instrucciones, Microsoft BitLocker Administration and Monitoring (MBAM) busca y muestra la versión localizada. Si MBAM no encuentra una versión localizada, muestra la dirección URL que está configurada para el parámetro **HelpDeskURL**.

**Nota:**  En las siguientes instrucciones, *SelfService* es el nombre del directorio virtual predeterminado para el portal de autoservicio. Es posible que haya usado un nombre diferente al configurar el portal de autoservicio.

 

**Para localizar la dirección URL del portal de autoservicio**

1.  En el servidor en el que ha configurado el portal de autoservicio, vaya a **sitios** &gt; configuración de **Administración y supervisión de Microsoft BitLocker** &gt; **SelfService** &gt; **configuración**de la aplicación.

2.  En el panel **acciones** , haga clic en **Agregar** para abrir el cuadro de diálogo **Agregar configuración de aplicación** .

3.  En el campo **nombre** , escriba **HelpdeskURL**\ _ &lt; *Language* &gt; , donde &lt; *idioma* &gt; es el código de idioma adecuado para la dirección URL.

    Por ejemplo, para crear una versión localizada del `HelpdeskURL` valor en español, asigne el nombre **HelpdeskURL \ _es-es**.

    El nombre de la carpeta de idioma también puede ser **el nombre del** idioma neutral en lugar de **es-es**. Si el explorador del usuario final se establece en es **-es** y esa carpeta no existe, la configuración regional principal (tal como se define en .net) se recupera y se comprueba de forma recursiva, lo que permite resolver &lt; el directorio de instalación de autoservicio &gt;\\SelfServiceWebsite\\es\\Notice.txt antes de convertirse en el archivo predeterminado Notice.txt. Esta reserva recursiva imita las reglas de carga de recursos de .NET.

    Para obtener una lista de los códigos de idioma válidos que puede usar, consulte referencia de la [API de compatibilidad con el idioma nacional (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  En el campo **valor** , escriba la versión localizada del `HelpdeskURL` valor que desea mostrar a los usuarios finales.



## Temas relacionados


[Personalización del portal de autoservicio para la organización](customizing-the-self-service-portal-for-your-organization.md)

 

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




