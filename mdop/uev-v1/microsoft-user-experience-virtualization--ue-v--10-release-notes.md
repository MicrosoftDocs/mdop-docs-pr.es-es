---
title: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0
description: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0
author: dansimp
ms.assetid: 920f3fae-e9b5-4b94-beda-32c19d31e94b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9f9942eef7ea84cf7010a0c0173427827a512216
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812487"
---
# Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0


Para buscar las notas de la versión de virtualización de Microsoft User Experience (UE-V), presione Ctrl + F.

Debe leer estas notas de la versión minuciosamente antes de instalar UE-V. Las notas de la versión contienen información necesaria para instalar correctamente la virtualización de la experiencia del usuario y contienen información adicional que no está disponible en la documentación del producto. Si hay diferencias entre estas notas de la versión y otra documentación de UE-V, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## Comentarios


Díganos lo que piensa sobre nuestra documentación de MDOP enviándonos sus comentarios y comentarios. Envíe sus comentarios sobre la documentación a [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).

## Problemas conocidos de UE-V


Esta sección contiene notas de la versión para la virtualización de la experiencia del usuario.

### La configuración del registro no se sincroniza entre App-V y aplicaciones nativas en el mismo equipo

Cuando un equipo tiene una aplicación que está disponible a través de la aplicación Application Virtualization (App-V) y de una aplicación de instalación nativa (instalada con un archivo. msi), la configuración basada en el registro no se sincroniza entre las tecnologías.

SOLUCIÓN alternativa: para resolver este problema, ejecute la aplicación seleccionando una de las dos tecnologías, pero no ambas.

### Error en la sincronización de configuración de Windows 8: "Boost:: filesystem:: EXISTS:: nombre de usuario o contraseña incorrectos"

La sincronización de la configuración del sistema operativo Windows® 8 falla con el siguiente mensaje de error: **Boost:: filesystem:: EXISTS:: nombre de usuario o contraseña incorrectos**. Para buscar eventos de registro operativos, abra el **visor de eventos** y vaya a **registros de aplicaciones y servicios**  /  **Microsoft**  /  **User Experience virtualización**  /  **Logging**  /  **operativo**. Los recursos compartidos de red que se usan para la configuración de UE-V las ubicaciones de almacenamiento deben residir en el mismo dominio de Active Directory que el usuario. De lo contrario, puede producirse el siguiente error: "nombre de usuario o contraseña incorrectos".

SOLUCIÓN: Use recursos compartidos de red del mismo dominio de Active Directory que el usuario. .

### Itinerancia de la firma de correo electrónico para Outlook 2010

UE-V moverá los archivos de firma de Outlook 2010 entre dispositivos. Sin embargo, las opciones de firma predeterminadas para los mensajes nuevos y las respuestas y reenvíos no son.Estas dos configuraciones se almacenan en el perfil de Outlook, que UE no Vdoes.

SOLUCIÓN alternativa: ninguno.

### La configuración de sincronización no se sincroniza en el intervalo esperado cuando se ejecuta en modo de vínculo de baja velocidad

En condiciones normales, configuración las ubicaciones de almacenamiento deberían estar disponibles a través de una conexión de red de vínculo rápido. En el modo de vínculo de baja velocidad, la sincronización solo se realizará de forma periódica. De forma predeterminada, la programación de sincronización del modo de vínculos lentos se establece en cada 360 minutos.

SOLUCIÓN: para cambiar la frecuencia de la sincronización en segundo plano para equipos en modo de vínculo de baja velocidad, puede configurar la Directiva de grupo para la Directiva de sincronización en segundo plano para **archivos sin conexión**.

### Los caracteres especiales no se sincronizan

Ciertos caracteres, como los símbolos de moneda, no se sincronizan entre equipos con Windows 7 y Windows 8 que ejecutan el agente de UE-V.

SOLUCIÓN alternativa: ninguno.

### UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Microsoft Office

Le recomendamos que instale la versión de 32 bits de Microsoft Office para sistemas operativos de 32 y 64 bits. Para elegir la versión de Microsoft Office que necesita, haga clic aquí. ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)). UE-V admite la configuración de itinerancia entre versiones de arquitectura idénticas de Office. Por ejemplo, la configuración de Office de 32 bits se transferirá entre todas las instancias de Office de 32 bits. UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Office.

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

### No se admiten rutas de más de 260 caracteres

Las rutas de almacenamiento de configuración con más de 260 caracteres no se admiten. Se producirá un error al copiar los paquetes de configuración de UE-V en las rutas de almacenamiento de configuración de más de 260 caracteres y se generará el siguiente mensaje de excepción en el registro de eventos operativos de UE-V: **\ [Boost:: filesystem:: Copy \ _file: el sistema no puede encontrar la ruta de acceso especificada \]**. Para buscar eventos de registro operativos, abra el **visor de eventos** y vaya a **registros de aplicaciones y servicios**  /  **Microsoft**  /  **User Experience virtualización**  /  **Logging**  /  **operativo**.

Actualmente no se admiten las rutas de configuración de archivo de más de 260 caracteres. La configuración de archivo a la que se hace referencia en la configuración de UE-V plantillas de ubicación no se puede encontrar en una ruta de directorio que tenga más de 260 caracteres.

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

### Los marcadores de Internet Explorer no aparecen en la SmartBar de Internet Explorer

Cuando los marcadores de Internet Explorer se transfieren de un equipo a otro, el índice del segundo equipo no se puede actualizar, por lo que, cuando se escribe en la barra de direcciones, el favorito no aparecerá como un posible resultado de búsqueda en el equipo 2.

SOLUCIÓN alternativa: ninguna

 

 





