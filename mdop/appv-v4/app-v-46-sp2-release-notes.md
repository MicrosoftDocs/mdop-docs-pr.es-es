---
title: Notas de la versión de App-V 4.6 SP2
description: Notas de la versión de App-V 4.6 SP2
author: dansimp
ms.assetid: abb536f0-e187-4c5b-952a-f837abd10ad2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cf36a6361e6f49c2b868c6752e1b2eb379cc9a31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822341"
---
# Notas de la versión de App-V 4.6 SP2


**Para buscar estas notas de la versión, presione CTRL + F.**

Lea estas notas de la versión minuciosamente antes de instalar Microsoft Application Virtualization (App-V) 4.6 SP2.

Estas notas de la versión contienen la información necesaria para instalar correctamente Application Virtualization 4,6 SP2. Las notas de la versión también contienen información que no está disponible en la documentación del producto. Si hay una diferencia entre estas notas de la versión y otra documentación de App-V 4.6 SP2, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## Acerca de la documentación del producto


Para obtener más información sobre la documentación de App-V, consulte la página de [virtualización de aplicaciones](https://go.microsoft.com/fwlink/?LinkID=232982) en Microsoft TechNet.

## Comentarios


Nos interesan tus comentarios en App-V 4.6 SP2. Puedes enviar tus comentarios a <mdopdocs@microsoft.com> .

**Nota:**  Esta dirección de correo electrónico no es un canal de soporte técnico, pero tus comentarios nos ayudarán a planificar futuros cambios para la documentación y las versiones de producto.

 

Para obtener la información más reciente acerca de MDOP y recursos de aprendizaje adicionales, consulte la página [experiencia de información de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Para obtener más información sobre las nuevas actualizaciones o para proporcionar comentarios, síganos en [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## <a href="" id="known-issues-with-app-v-4-6-sp2-"></a>Problemas conocidos con App-V 4.6 SP2


### La compatibilidad con los nombres de archivo cortos está deshabilitada para las unidades físicas que no son del sistema cuando se secuencia

Cuando se hace una secuencia en Windows 8 o Windows Server 2012, la compatibilidad con los nombres de archivo cortos (8,3) está deshabilitada de forma predeterminada para las unidades físicas que no son del sistema.

La unidad física subyacente asociada al directorio de la aplicación virtual principal (por ejemplo, "Q:\\appname") en la estación de secuenciación debe proporcionar compatibilidad de nombre corto (8,3) para que el secuenciador de App-V 4.6 SP2 genere nombres de archivo cortos al crear paquetes de aplicaciones virtuales. La compatibilidad de nombre corto de archivo (8,3) está deshabilitada de forma predeterminada para las unidades físicas que no son del sistema en Windows 8 o Windows Server 2012.

**Solución alternativa:** Habilitar la compatibilidad con nombres de archivo cortos (8,3) en unidades físicas que no son del sistema. Puede usar el siguiente comando para habilitar la compatibilidad de nombre de archivo breve en Windows 8 o Windows Server 2012.

``` syntax
fsutil 8dot3name set <virtual drive letter>:
```

Por ejemplo, use el comando siguiente si la letra de unidad es "Q:":

``` syntax
fsutil 8dot3name set Q: 0
```

**Nota:**  No es necesario cambiar esta configuración en el cliente de App-V porque el sistema de archivos de App-V controla correctamente las rutas breves en Windows 8 o Windows Server 2012.

 

### <a href="" id="-------------app-v-does-not-override-the-default-handler-for-file-type-or-protocol-associations-on-windows-8"></a> App-V no invalida el controlador predeterminado para las asociaciones de protocolo o tipo de archivo en Windows 8

Si selecciona una aplicación predeterminada usando **programas predeterminados** en el **Panel de control** en Windows 8, App-V no invalidará las asociaciones de tipos de archivo asociados de esa aplicación.

**Solución alternativa:** Nada.

### Outlook 2010 virtualizado no se ofrece como una opción para los vínculos que se puede hacer clic en correo en Windows 8

La extensión de Shell mailto no ofrece la 2010 virtualizada de Outlook en Windows 8. Por ejemplo, si hace clic en un vínculo mailto: desde la 2010 de Outlook virtualizada que se ejecuta en Windows 8, no se creará una ventana de correo electrónico nueva. Esta opción funciona correctamente en Windows 7 y versiones anteriores del sistema operativo Windows.

**Solución alternativa:** Nada.

### <a href="" id="-------------application-virtualization-4-6-sp2-update-is-not-offered-on-all-locales-that-use-microsoft-update"></a> La actualización de Application Virtualization 4,6 SP2 no se ofrece en todas las configuraciones regionales que usan Microsoft Update

Cuando usa Microsoft Update, la actualización de App-V 4.6 SP2 no está disponible para las siguientes configuraciones regionales de idioma:

-   Kazajo

-   Hindi

-   Serbio-cirílico

**Solución alternativa:** Si usa Microsoft Windows Server Update Services (WSUS), use la versión en Inglés de la actualización o descargue la actualización desde el catálogo de Microsoft Update.

## Información de copyright de notas de versión


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune y WindowsPowerShell son marcas comerciales del grupo de empresas de Microsoft. El resto de marcas comerciales pertenecen a sus respectivos dueños.



## Temas relacionados


[Acerca de Microsoft Application Virtualization4.6SP2](about-microsoft-application-virtualization-46-sp2.md)

 

 





