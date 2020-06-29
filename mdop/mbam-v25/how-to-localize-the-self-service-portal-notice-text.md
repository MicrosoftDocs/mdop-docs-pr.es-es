---
title: Cómo localizar el texto de aviso del portal de autoservicio
description: Cómo localizar el texto de aviso del portal de autoservicio
author: dansimp
ms.assetid: a4c878b7-e5c8-45af-a537-761bb2991659
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a2385f6b00713e7373bd1707b02324b80f300c0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826711"
---
# Cómo localizar el texto de aviso del portal de autoservicio


Puede configurar el texto del aviso localizado para que se muestre a los usuarios finales de forma predeterminada en el portal de autoservicio. El archivo de Notice.txt que muestra el texto del aviso se encuentra en el siguiente directorio raíz:

&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self

Para mostrar texto de aviso localizado, cree un archivo de Notice.txt localizado y, a continuación, guárdelo en una carpeta de idioma específico en el siguiente directorio de ejemplo:

&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self

**Nota:**  Puede configurar la ruta de acceso con el elemento **NoticeTextPath** en **configuración**de la aplicación.

 

MBAM muestra el texto del aviso, en función de las siguientes reglas:

-   Si crea un archivo de **Notice.txt** localizado en la carpeta de idioma correspondiente, MBAM muestra el texto del aviso localizado si el archivo de **Notice.txt** predeterminado ya existe. Si falta el archivo predeterminado **Notice.txt** , aparecerá un mensaje indicando que falta el archivo predeterminado.

-   Si MBAM no encuentra una versión localizada del archivo Notice.txt, muestra el texto en el archivo predeterminado Notice.txt.

-   Si MBAM no encuentra un archivo Notice.txt predeterminado, muestra el texto predeterminado en el portal de autoservicio.

**Nota:**  Si el explorador de un usuario final se establece en un idioma que no tiene una subcarpeta de idioma correspondiente o Notice.txt, se muestra el texto del archivo de Notice.txt en el siguiente directorio raíz:

&lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self

 

**Para crear un archivo de Notice.txt localizado**

1.  En el servidor en el que ha configurado el portal de autoservicio, cree una &lt; *Language* &gt; carpeta de idioma en el siguiente directorio de ejemplo, donde &lt; *idioma* &gt; representa el nombre del idioma localizado:

    &lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\ de servicio \\Self

    **Nota:**  Algunas carpetas de idioma ya existen, por lo que es posible que no tenga que crear una carpeta. Si tiene que crear una carpeta de idioma, vea referencia de la [API de compatibilidad con el idioma nacional (NLS)](https://go.microsoft.com/fwlink/?LinkId=317947) para obtener una lista de los nombres válidos que puede usar para la carpeta de &lt; *idioma* &gt; .

     

2.  Cree un archivo de Notice.txt que contenga el texto del aviso localizado.

3.  Guarde el archivo de Notice.txt en la carpeta de &lt; *idioma* &gt; . Por ejemplo, para crear un archivo de Notice.txt localizado en español, guarde el archivo de Notice.txt localizado en el siguiente directorio de ejemplo:

    &lt;*MBAM directorio* &gt; de instalación de autoservicio Website\\Es-es de servicio \\Self

    El nombre de la carpeta de idioma también puede ser **el nombre del** idioma neutral en lugar de **es-es**. Si el explorador del usuario final se establece en es **-es** y esa carpeta no existe, la configuración regional principal (tal como se define en .net) se recupera y se comprueba de forma recursiva, lo que permite resolver &lt; el directorio de instalación de autoservicio &gt;\\SelfServiceWebsite\\es\\Notice.txt antes de convertirse en el archivo predeterminado Notice.txt. Esta reserva recursiva imita las reglas de carga de recursos de .NET.



## Temas relacionados


[Personalización del portal de autoservicio para la organización](customizing-the-self-service-portal-for-your-organization.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





