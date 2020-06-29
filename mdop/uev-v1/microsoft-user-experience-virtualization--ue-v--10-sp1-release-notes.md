---
title: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0 SP1
description: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0 SP1
author: dansimp
ms.assetid: 447fae0c-fe87-4d1c-b616-6f92fbdaf6d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8584999d9fdbdfccc3e9b2b1486cb97635475747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812486"
---
# Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0 SP1


Para buscar las notas de versión de Microsoft User Experience Virtualization (UE-V) 1,0 Service Pack 1, presione Ctrl + F.

Debe leer estas notas de la versión minuciosamente antes de instalar UE-V. Las notas de la versión contienen información necesaria para instalar correctamente la virtualización de la experiencia del usuario y contienen información adicional que no está disponible en la documentación del producto. Si hay diferencias entre estas notas de la versión y otra documentación de UE-V, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## Problemas conocidos de UE-V


Esta sección contiene notas de la versión para la experiencia del usuario de virtualización de 1,0 SP1.

### La configuración del registro no se sincroniza entre App-V y aplicaciones nativas en el mismo equipo

Cuando un equipo tiene una aplicación que está disponible a través de la aplicación Application Virtualization (App-V) y de una aplicación de instalación nativa instalada con un Windows Installer (archivo. msi), la configuración basada en el registro no se sincroniza entre las tecnologías.

SOLUCIÓN alternativa: para resolver este problema, ejecute la aplicación seleccionando una de las dos tecnologías, pero no ambas.

### <a href="" id="windows-8-setting-synchronization-fails-when-network-share-is-outside-user-s-domain"></a>Se produce un error en la sincronización de configuración de Windows 8 cuando el recurso compartido de red está fuera del dominio del usuario

Cuando Windows® 8 intenta la sincronización de configuración del sistema operativo, se produce un error en synchrnization con el siguiente mensaje de error: **Boost:: filesystem:: EXISTS:: nombre de usuario o contraseña incorrectos**. Este error puede indicar que el recurso compartido de red está fuera del dominio del usuario. Para buscar eventos de registro operativos, abra el **visor de eventos** y vaya a **registros de aplicaciones y servicios**  /  **Microsoft**  /  **User Experience virtualización**  /  **Logging**  /  **operativo**. Los recursos compartidos de red que se usan para la configuración de UE-V las ubicaciones de almacenamiento deben residir en el mismo dominio de Active Directory que el usuario.

SOLUCIÓN: Use recursos compartidos de red del mismo dominio de Active Directory que el usuario. .

### Itinerancia de la firma de correo electrónico para Outlook 2010

UE-V moverá los archivos de firma de Outlook 2010 entre dispositivos. Sin embargo, las opciones de firma predeterminadas para los mensajes nuevos y las respuestas y reenvíos no se mueven. Estas dos opciones de configuración se almacenan en el perfil de Outlook, que UE-V no se mueve.

SOLUCIÓN alternativa: ninguno.

### La configuración de sincronización no se sincroniza en el intervalo esperado cuando se ejecuta en modo de vínculo de baja velocidad

En condiciones normales, configuración las ubicaciones de almacenamiento deberían estar disponibles a través de una conexión de red de vínculo rápido. En el modo de vínculo de baja velocidad, la sincronización solo se realizará de forma periódica. De forma predeterminada, la programación de sincronización del modo de vínculos lentos se establece en cada 360 minutos.

SOLUCIÓN: para cambiar la frecuencia de la sincronización en segundo plano para equipos en modo de vínculo de baja velocidad, puede configurar la Directiva de grupo para la Directiva de sincronización en segundo plano para **archivos sin conexión**.

### Los caracteres especiales no se sincronizan

Ciertos caracteres, como los símbolos de moneda, no se sincronizan entre equipos con Windows 7 y Windows 8 que ejecutan el agente de UE-V.

SOLUCIÓN alternativa: ninguno.

### UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Microsoft Office

Le recomendamos que instale la versión de 32 bits de Microsoft Office para sistemas operativos de 32 y 64 bits. Para elegir la versión de Microsoft Office que necesita, haga clic aquí ( [http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623) ). UE-V admite la configuración de itinerancia entre versiones de arquitectura idénticas de Office. Por ejemplo, la configuración de Office de 32 bits se transferirá entre todas las instancias de Office de 32 bits. UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Office.

SOLUCIÓN alternativa: ninguna

### <a href="" id="msi-s-are-not-localized"></a>Los MSI no están localizados

UE-V 1,0 SP1 incluye un programa de instalación localizado para UE-V Agent y UE-v generator. Estos archivos MSI siguen estando disponibles, pero la interfaz de usuario está minimizada y la de MSI solo se muestra en inglés. A pesar de que el archivo está en inglés, el programa de instalación instala todos los idiomas admitidos durante la instalación.

SOLUCIÓN alternativa: ninguna

### Otras carpetas del recurso compartido con la ubicación de almacenamiento de configuración no están disponibles en modo de conexión lenta

La configuración de almacenar recursos compartidos no se encuentra en un recurso compartido de red que se usa para otras carpetas que siempre deben estar disponibles. Cuando el recurso compartido de red que hospeda la ubicación de almacenamiento de configuración pasa al modo de conexión lenta, la única carpeta disponible es la de ubicación de almacenamiento de configuración. Otras carpetas del recurso compartido no están disponibles en modo de conexión lenta.

Solución alternativa: ninguna

### Los favicons asociados a los favoritos de Internet Explorer 9 no se mueven

Los favicons asociados a los favoritos de Internet Explorer 9 no se desplazan por la virtualización de la experiencia del usuario y no aparecen cuando los favoritos aparecen por primera vez en un equipo nuevo.

SOLUCIÓN: favicons aparecerá con sus favoritos asociados una vez que el marcador se use y se almacene en la memoria caché en el explorador Internet Explorer 9.

### Las rutas de configuración de archivos se almacenan en el registro

Algunas opciones de la aplicación almacenan las rutas de los archivos de configuración y configuración como valores en el registro. Los archivos a los que se hace referencia como rutas en el registro se deben sincronizar cuando se mueven los valores de configuración entre equipos.

SOLUCIÓN alternativa: Use el redireccionamiento de carpetas o cualquier otra tecnología para asegurarse de que todos los archivos a los que se hace referencia como rutas de configuración de archivos están presentes y colocados en la misma ubicación en todos los equipos en los que la configuración es móvil.

### Las rutas de almacenamiento de configuración largas pueden provocar un error

Mantenga las rutas de almacenamiento de configuración tan cortas como sea posible. Las rutas largas pueden impedir la resolución o la sincronización. UE-V usa la ruta de acceso de almacenamiento de configuración como parte de la ruta de acceso calculada para almacenar la configuración. La ruta de acceso se calcula de la siguiente manera: configuración ruta de almacenamiento + "settingspackages" + paquete DIR (ID. de plantilla) + nombre del paquete (ID. de plantilla). Si esa ruta de acceso calculada supera los 260 caracteres, almacenamiento de paquetes fallará y generará el siguiente mensaje de error en el registro de eventos operativos de UE-V:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Para comprobar los eventos de registro operativos, abra el visor de eventos y vaya a registros de aplicaciones y servicios/Microsoft/virtualización de la experiencia de usuario/inicio de sesión/operativo.

SOLUCIÓN alternativa: ninguno.

### Los retrasos del agente UE-V al cerrar sesión o iniciar sesión

Si se produce un inicio de sesión o un cierre de sesión antes de que archivos sin conexión haya determinado que hay un vínculo lento, puede que se retrase el cierre de sesión o el inicio de sesión. La característica de archivos sin conexión puede demorar hasta tres minutos en detectar el estado actual de la red. Si el inicio de sesión o el apagado se produce antes de que los archivos sin conexión hayan determinado que el equipo está conectado a un vínculo de baja velocidad, el paquete de configuración de UE-V se enviará al servidor en lugar de a la caché local.

SOLUCIÓN alternativa: ninguno.

### Conflicto de configuración al intentar trabajar con la configuración del sistema operativo en Windows 8

En Windows 8, si la sincronización de cuentas de Microsoft está habilitada junto con UE-V para la configuración del sistema operativo, la configuración que se aplica puede ser incoherente.

SOLUCIÓN alternativa: realice una de las siguientes acciones:

-   Deshabilitar la sincronización de cuentas de Microsoft si usa la configuración del sistema operativo UE-V para roaming

-   Deshabilitar UE-V para la configuración del sistema operativo

### Algunas configuraciones del sistema operativo solo se mueven entre las versiones del sistema operativo

La configuración del sistema operativo para narrador y los caracteres de moneda específicos de la configuración regional solo se transferirán a las distintas versiones del sistema operativo de Windows. Por ejemplo, los caracteres de moneda solo se transferirán de Windows 7 a Windows 7.

SOLUCIÓN alternativa: ninguna

 

 





