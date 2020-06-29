---
title: Cómo localizar la instrucción "HelpdeskText" que dirige a los usuarios a obtener más información del portal de autoservicio
description: Cómo localizar la instrucción "HelpdeskText" que dirige a los usuarios a obtener más información del portal de autoservicio
author: dansimp
ms.assetid: 09ba2a07-3186-45d9-adef-4034c70ae7cf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2367424185da813a46fa52f3614c03083864f75f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823421"
---
# Cómo localizar la instrucción "HelpdeskText" que dirige a los usuarios a obtener más información del portal de autoservicio


Puede configurar una versión localizada de la instrucción "HelpdeskText" del portal de autoservicio, que informa a los usuarios finales sobre cómo obtener ayuda adicional cuando usan el portal de autoservicio. Si configura el texto localizado de la instrucción, tal y como se describe en las siguientes instrucciones, MBAM muestra la versión localizada. Si MBAM no encuentra la versión localizada, muestra el valor que está en el parámetro **HelpdeskText** .

**Nota:**  En las siguientes instrucciones, *SelfService* es el nombre del directorio virtual predeterminado para el portal de autoservicio. Es posible que haya usado un nombre diferente al configurar el portal de autoservicio.

 

**Para mostrar una versión localizada de la instrucción HelpdeskText**

1.  En el servidor en el que ha configurado el portal de autoservicio, vaya a **sitios** &gt; configuración de **Administración y supervisión de Microsoft BitLocker** &gt; **SelfService** &gt; **configuración**de la aplicación.

2.  En el panel **acciones** , haga clic en **Agregar** para abrir el cuadro de diálogo **Agregar configuración de aplicación** .

3.  En el campo **nombre** , escriba **HelpdeskText**\ _ &lt; *Language* &gt; , donde &lt; *idioma* &gt; es el código de idioma adecuado para el texto.

    Por ejemplo, para crear una instrucción HelpdeskText localizada en español, asigne el nombre **HelpdeskText \ _es-es**.

    El nombre de la carpeta de idioma también puede ser **el nombre del** idioma neutral en lugar de **es-es**. Si el explorador del usuario final se establece en es **-es** y esa carpeta no existe, la configuración regional principal (tal como se define en .net) se recupera y se comprueba de forma recursiva, lo que permite resolver &lt; el directorio de instalación de autoservicio &gt;\\SelfServiceWebsite\\es\\Notice.txt antes de convertirse en el archivo predeterminado Notice.txt. Esta reserva recursiva imita las reglas de carga de recursos de .NET.

    Para obtener una lista de los códigos de idioma válidos que puede usar, consulte referencia de la [API de compatibilidad con el idioma nacional (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  En el campo **valor** , escriba el texto localizado que desea mostrar a los usuarios finales.



## Temas relacionados


[Personalización del portal de autoservicio para la organización](customizing-the-self-service-portal-for-your-organization.md)

 

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



