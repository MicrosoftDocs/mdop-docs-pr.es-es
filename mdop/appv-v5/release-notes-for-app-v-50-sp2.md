---
title: Notas de la versión de App-V 5.0 SP2
description: Notas de la versión de App-V 5.0 SP2
author: dansimp
ms.assetid: fe73139d-240c-4ed5-8e59-6ae76ee8e80c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5e885e67023d0e5c1e36aeb340933c64ae92610e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813327"
---
# Notas de la versión de App-V 5.0 SP2


**Para buscar un problema específico en estas notas de la versión, presione CTRL + F.**

Lea estas notas de la versión minuciosamente antes de instalar App-V 5,0 SP2.

Estas notas de la versión contienen información necesaria para instalar correctamente App-V 5,0 SP2. Las notas de la versión también contienen información que no está disponible en la documentación del producto. Si hay diferencias entre estas notas de la versión y otra documentación de App-V 5,0, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## Acerca de la documentación del producto


Para obtener información sobre la documentación de App-V 5,0, consulte la página de inicio de App-V 5,0 en Microsoft TechNet.

## Enviar comentarios


Nos interesan tus comentarios en App-V 5,0. Puedes enviar tus comentarios a <mdopdocs@microsoft.com> .

**Nota:**  Esta dirección de correo electrónico no es un canal de soporte técnico, pero tus comentarios nos ayudarán a planificar futuros cambios en nuestra documentación y versiones de productos.

 

Para obtener la información más reciente acerca de MDOP y recursos de aprendizaje adicionales, consulte la página [experiencia de información de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Para obtener más información sobre las nuevas actualizaciones o para proporcionar comentarios, síganos en [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problemas conocidos con el paquete de revisiones 4 para Application Virtualization 5,0 SP2


### Los paquetes dejan de funcionar después de desinstalar el paquete de revisiones 4 para Application Virtualization 5,0 SP2

Paquetes publicados cuando se aplica el paquete de revisiones 4 para Application Virtualization 5,0 SP2 deje de funcionar cuando se quita el paquete de revisiones 4 para Application Virtualization 5,0 SP2.

SOLUCIÓN alternativa

Si la siguiente carpeta existe, debe eliminarla:

**% LocalAppData%**  \\  **Microsoft**  \\  **AppV**  \\  **Cliente**  \\  **VFS**  \\  ** &lt; identificador &gt; del paquete** para cada paquete publicado.

**Nota:**  Debe tener privilegios elevados para eliminar esta carpeta.

 

Para usar un script, para cada cuenta de usuario en el equipo y para cada identificador de paquete que se publicó después de instalar el paquete de revisiones 4 para Application Virtualization 5,0 SP2:

`Rd /s /q “%systemdrive%\users\[UserName]\AppData\Local\Microsoft\AppV\Client\VFS\[Package ID]`

-   Los accesos directos permanecerán con las sesiones de usuario incluso después de eliminar la carpeta del directorio de la sección anterior, de modo que pueda hacer clic en el acceso directo para volver a ejecutar la aplicación. No es necesario volver a publicar la aplicación.

-   Este problema se produce para paquetes publicados de forma global y empaquetadas por el usuario, por ejemplo, Microsoft Office2013. Para ambos tipos de paquetes, debe eliminarse la carpeta.

-   No es necesario eliminar la carpeta VFS en los datos de la aplicación de itinerancia (**% AppData%**). Solo se debe eliminar el **% LocalAppData%** .

### La integración de Microsoft Office apunta a una ubicación incorrecta del sistema de archivos

La integración de Microsoft Office apunta a una ubicación incorrecta del sistema de archivos (mensaje de error Groove.exe).

SOLUCIÓN alternativa

Use uno de los métodos siguientes:

1.  Elimine el acceso directo en la carpeta de inicio después de la actualización.

2.  Cambie el método abreviado en la carpeta de inicio con un script.

3.  Use el archivo de configuración de implementación para especificar el destino de acceso directo a la raíz de integración.

### <a href="" id="-------------hotfix-package-4-for-application-virtualization-5-0-sp2-installer-can-take-a-long-time"></a> El paquete de Hotfix 4 para el instalador de Application Virtualization 5,0 SP2 puede tardar mucho tiempo

El paquete de revisiones 4 para el instalador de Application Virtualization 5,0 SP2 puede tardar mucho tiempo en función de cuántos archivos se almacenan en la memoria caché del paquete existente.

La actualización de los descriptores de seguridad de paquetes asociados durante el paquete 4 de hotfix para la instalación de Application Virtualization 5,0 SP2 tiene un impacto significativo en el tiempo que tarda la instalación. Anteriormente, la instalación de la instalación era estándar de duración. Sin embargo, ahora depende de cuántos archivos haya ensayado en la caché del paquete.

SOLUCIÓN alternativa: ninguna

### No se puede desinstalar el paquete de Hotfix 4 para Application Virtualization 5,0 SP2 si el paquete JIT-V está en uso

Si instala el paquete de revisiones 4 para Application Virtualization 5,0 SP2 y, a continuación, intenta desinstalar la corrección urgente cuando se usa la virtualización Just-in-Time (JIT-V), la operación se producirá un error si se cumplen todas las condiciones siguientes:

-   Instaló con un archivo de Windows Installer (. msi) y, a continuación, aplica actualizaciones con un archivo de revisión de Microsoft Installer (. msp).

-   Intenta desinstalar una actualización con el elemento agregar o quitar programas del panel de control.

-   Un paquete habilitado para JIT se está ejecutando en el equipo.

SOLUCIÓN alternativa: Complete los pasos siguientes:

1.  Abra Windows PowerShell y ejecute los siguientes comandos:

    -   **Importación-módulo appvclient**

    -   **Get-AppvClientPackage | Stop-AppvClientPackage**

2.  Desinstale la actualización con agregar o quitar programas.

## Problemas conocidos con App-V 5,0 SP2


### <a href="" id="bkmk-folderredirection"></a>En ocasiones, el redireccionamiento de carpetas de clientes de App-V no mueve los archivos de% AppData% a% LocalAppData%

Cuando% AppData% es una carpeta de red compartida que ha configurado para el redireccionamiento de carpetas, los cambios que los usuarios finales hacen a AppData (roaming) se pueden perder al cambiar de equipos o cuando se desactiva su AppData local cuando cierran sesión y luego vuelven a iniciar sesión. Este error se produce porque la clave del registro (AppDataTime), que indica la última carga conocida, no está sincronizada con AppData locales en caché.

SOLUCIÓN: elimine manualmente la siguiente clave de registro para cada paquete relevante cuando un usuario final inicie o apague:

``` syntax
HKCU\Software\Microsoft\AppV\Client\Packages\<PACKAGE_GUID>\AppDataTime
```

La primera vez que los usuarios finales inician una aplicación en el paquete después de que inicien sesión, App-V fuerza la descarga del% AppData%, incluso si% LocalAppData% ya está actualizado.

### <a href="" id="-------------app-v-5-0-service-pack-2--app-v-5-0-sp2--does-not-include-a-new-version-of-the-app-v-server"></a> El Service Pack 2 de App-V 5,0 (App-V 5,0 SP2) no incluye una nueva versión del servidor de App-V

App-V 5.0 SP2 no incluye una nueva versión del servidor de App-V. Si implementa los clientes de App-V 5,0 SP2 que ejecutan Windows 8,1 en su entorno y planea administrar los clientes mediante la infraestructura de App-V, debe instalar el [paquete de revisiones 2 para Microsoft Application virtualization 5,0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634). (https://go.microsoft.com/fwlink/?LinkId=386634)

Si está ejecutando y administrando los clientes de App-V 5,0 SP2 con cualquiera de los siguientes métodos, no se necesita la actualización de cliente:

-   Modo Independiente.

-   Configuration Manager.

-   ESD de terceros.

El cliente de App-V 5,0 SP2 es totalmente compatible con Windows 8,1

SOLUCIÓN alternativa: ninguno.

## Información de copyright de notas de versión


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune y WindowsPowerShell son marcas comerciales del grupo de empresas de Microsoft. El resto de marcas comerciales pertenecen a sus respectivos dueños.








## Temas relacionados


[Acerca de App-V 5.0 SP2](about-app-v-50-sp2.md)

 

 





