---
title: Solución de problemas de operaciones
description: Solución de problemas de operaciones
author: dansimp
ms.assetid: 948d7869-accd-44da-974f-93409234dee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 126b5fae517c59914dcb7fb155ef4ad47278b5bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812742"
---
# Solución de problemas de operaciones


En este tema se incluye información que puede usar para ayudar a solucionar problemas generales operativos en Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Solución de problemas en las operaciones de MED-V


A continuación se muestran algunos problemas que pueden encontrar los usuarios finales al ejecutar MED-V y soluciones para ayudarle a solucionar estos problemas:

**Error en el redireccionamiento de documentación**. Este problema suele ocurrir cuando la carpeta Mis documentos de un usuario final apunta a una ubicación de red. Windows no admite la creación de un recurso compartido desde otra carpeta compartida. Cuando una unidad o una carpeta se redirigen al invitado, RDP\\Windows Virtual PC crea un recurso compartido para esa carpeta. Por lo tanto, si la carpeta Mis documentos en el host ya está apuntando a un recurso compartido, RDP\\Windows Virtual PC no puede crear un recurso compartido de un recurso compartido.

Otra causa posible de este problema es que las credenciales necesarias para conectarse al recurso de red sean diferentes de las credenciales del dominio del usuario. MED-V puede estar detectando que los documentos se redirigen al host, envía esa información al invitado y, a continuación, intenta volver a conectar el recurso de red. Si las credenciales del usuario no se autentican, es posible que MED-V deje de intentar autenticar.

**Solución**

Pruebe una de las siguientes acciones para resolver este problema:

-   Establezca el directorio raíz del usuario dentro de Active Directory. Después, el invitado y el anfitrión deben conectarse al mismo recurso de red.

-   En lugar de redirigir la carpeta Mis documentos a una ruta UNC, asígnela a una letra de unidad (en el host, asigne una unidad que apunte al recurso de red). Después, la carpeta Mis documentos se puede configurar para que use la letra de unidad en lugar de la ruta de acceso UNC. El invitado se redirigirá a la misma unidad asignada de la forma esperada.

-   Cree un script de inicio en el invitado que redirija la carpeta Mis documentos al recurso de red y proporcione las credenciales adicionales según sea necesario.

**Error en el redireccionamiento de URL**. Una dirección URL que ha especificado para el redireccionamiento desde el host al invitado no se redirige como se pretende o devuelve un mensaje de error que indica que el sitio web no existe.

**Solución**

Este error puede producirse cuando hay un uso incorrecto o incorrecto de caracteres, como un asterisco (\ *), en la información sobre el redireccionamiento de la dirección URL. Compruebe el valor del registro para el redireccionamiento de direcciones URL y corrija los errores.

La clave del registro se llama `RedirectUrls` y suele encontrarse en:

Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

**Icono de la barra de tareas que se ha provocado erróneamente**. De forma predeterminada, el icono que aparece en la barra de tareas del usuario final para las aplicaciones publicadas y las direcciones URL redirigidas es el icono de Windows Virtual PC. Si un usuario final no reconoce este comportamiento predeterminado, se puede confundir al mirar la barra de tareas para localizar su aplicación.

**Solución**

La única manera de evitar este comportamiento predeterminado es cambiar la configuración de usuario de las propiedades de la barra de tareas de la siguiente manera:

1.  Haga clic con el botón secundario en la barra de tareas y seleccione **propiedades**.

2.  En el cuadro de diálogo Propiedades de la **barra de tareas y el menú Inicio** , haga clic en la pestaña **barra de tareas** .

3.  En la barra desplegable del cuadro botones de la **barra de tareas** , seleccione no **combinar nunca**.

4.  Haga clic en **Aceptar**.

Se muestran los iconos esperados para las aplicaciones publicadas y las direcciones URL redirigidas.

**ADVERTENCIA emitida si el segundo usuario intenta iniciar sesión o si la máquina virtual está en uso**. Se emite un mensaje de advertencia cuando un segundo usuario inicia sesión en un área de trabajo de MED-V mientras un primer usuario sigue ejecutando MED-V. La advertencia también se emite si se inicia MED-V mientras se usa la máquina virtual, por ejemplo, si la máquina virtual se inició a través de Virtual PC de Windows en el menú **Inicio** . Cuando el usuario final acepta el mensaje de advertencia, MED-V se cierra.

**Solución**

Un usuario final debe comprobar que todos los demás usuarios han cerrado la sesión MED-V antes de intentar iniciar sesión. Esto garantiza que ninguna otra instancia de MED-V se esté ejecutando y que Windows Virtual PC no esté bajo el control de la máquina virtual.

**Sonidos sonoros leídos durante la configuración de primera vez**. En ocasiones, los sonidos se escuchan mientras MED-V se está ejecutando por primera vez. Esto puede resultar confuso para un usuario final. Los pitidos se originan en la máquina virtual cuando realiza determinadas acciones, como, por ejemplo, apagar.

**Solución**

Puede detener el servicio de pitidos si especifica el comando "net stop beep" al principio de cada secuencia de inicio de la máquina virtual. También puede deshabilitar el servicio pitido especificando el comando "SC config beep Start = Disabled". Puede especificar estos comandos antes de sellar la imagen o como parte de Sysprep.

**Varias conexiones de red creadas para áreas de trabajo de MED-V en modo puente**. Si la primera configuración está creando un área de trabajo de MED-V que está configurada para el modo NAT, solo crea una única conexión de red en Windows Virtual PC. Sin embargo, si la primera configuración está creando un área de trabajo de MED-V que está configurada para el modo de puente, crea una conexión de red independiente para cada adaptador de red instalado en el equipo, porque MED-V no puede determinar qué adaptador de red está activo. Esto también garantiza que los usuarios móviles siempre dispongan de un adaptador de red disponible para las conexiones cableadas e inalámbricas.

**Solución**

Ninguna.

**La aplicación MED-V no responde demasiado tiempo al cerrar**. En algunos casos, una aplicación de MED-V deja de responder cuando está intentando cerrarse.

**Solución**

Puede especificar la cantidad de tiempo que esperará MED-V para cerrar las aplicaciones que no responden mediante la configuración de la clave de registro WaitToKillAppTimeout en la máquina virtual invitada. Para obtener más información, consulte [Cómo aumentar el tiempo de apagado para que los procesos puedan cerrarse correctamente en Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) ( https://go.microsoft.com/fwlink/?LinkId=206819) .

**Al cambiar el nombre de un acceso directo a una aplicación publicada en la máquina virtual invitada, no se cambia el nombre publicado en el host**. Al publicar una aplicación mediante la creación de un acceso directo y, a continuación, cambiar el nombre del acceso directo en la máquina virtual invitada, el nombre de la aplicación original permanece en el menú **Inicio** de host. El programa continúa ejecutándose según lo esperado, pero el programa siempre conservará el nombre original.

**Solución**

Ninguna. Este es un comportamiento conocido de Windows Virtual PC.

Al **mover un acceso directo en la máquina virtual invitada no se actualiza la ubicación en el menú Inicio del equipo host**. Los accesos directos a aplicaciones de MED-V que se publican en el menú **Inicio** del equipo host se catalogan en el registro. Si mueve un acceso directo de la aplicación a una subcarpeta, el registro no se actualizará para reflejar el cambio.

**Solución**

Siga estos pasos para cambiar la ubicación de un acceso directo a la aplicación MED-V:

1.  Cuando se esté ejecutando MED-V, abra el explorador de Windows en la máquina virtual invitada MED-V.

2.  Vaya al directorio "%ALLUSERSPROFILE%\\Start Menu\\Programs".

3.  Mueva los accesos directos de la aplicación fuera de las carpetas StartMenu o programas.

4.  Después de unos 30 segundos, valide que los métodos abreviados se quitan del menú **Inicio** del equipo host.

5.  Vuelva a mover los accesos directos de la aplicación a las carpetas del programa nuevo en el directorio Start Menu\\Programs.

6.  Después de unos 30 segundos, valide que los métodos abreviados se actualizan en el menú **Inicio** del equipo host.

**Las aplicaciones publicadas pueden agotar el tiempo de espera después de sentarse en reposo**. En algunos casos, las aplicaciones publicadas agotarán el tiempo de espera si están inactivas durante algún tiempo. Esta situación solo se produce si IPsec está habilitado y el área de trabajo MED-V está configurada para el modo NAT. Esta situación no se produce si se ejecuta en modo BRIDGEd (puente).

**Solución**

Deshabilite IPsec cuando ejecute el área de trabajo de MED-V en el modo NAT.

**Al anclar una aplicación publicada en la barra de tareas, se omite MED-V**. Si un usuario final ancla una aplicación publicada a la barra de tareas y, a continuación, cierra MED-V, se pasará por alto la próxima vez que se abra la aplicación desde el icono de la barra de tareas. En su lugar, la aplicación se abre directamente en una ventana de VMSAL.

**Solución**

No ancle las aplicaciones publicadas en MED-V a la barra de tareas.

## Temas relacionados


[Procedimientos recomendados de seguridad para las operaciones de MED-V](security-best-practices-for-med-v-operations.md)

[Solución de problemas de implementación](deployment-troubleshooting.md)

 

 





