---
title: Información de solución de problemas del cliente de virtualización de aplicaciones
description: Información de solución de problemas del cliente de virtualización de aplicaciones
author: dansimp
ms.assetid: 260a8dad-847f-4ec0-b7dd-6e6bc52017ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2ab332f5f3b7f8cdc40f6d35e8712d55028a60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815191"
---
# Información de solución de problemas del cliente de virtualización de aplicaciones


En este tema se incluye información que puede usar para solucionar varios problemas en el cliente de Application Virtualization (App-V).

## La actualización de publicaciones es muy lenta


Si la actualización de publicación en un equipo específico tarda mucho más tiempo de lo esperado y si el cliente está configurado para usar la configuración de **IconSourceRoot** , determine si **IconSourceRoot** contiene una dirección URL no válida. Una dirección URL no válida producirá retrasos muy largos durante la actualización de la publicación.

## Los usuarios no pueden conectarse al servidor e ir al modo de operaciones desconectadas


Si está usando un servidor de administración de App-V configurado con el protocolo RTSPs, si los usuarios no pueden conectarse y entran en el modo de operaciones desconectadas, determine si el certificado que se usa en el servidor es válido. Un certificado no válido evitará que los usuarios se conecten y harán que pasen al modo de operaciones desconectadas.

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a>Los usuarios experimentan un bajo nivel de rendimiento cuando las aplicaciones no se almacenan en caché.


Cuando las aplicaciones no se almacenan en la memoria caché, es posible que ocasionalmente se produzcan problemas de rendimiento lentos o intermitentes al iniciar o usar la aplicación. Hay varios motivos posibles por los que esto puede ocurrir, por ejemplo, cuando el cliente de App-V se encuentra en el proceso de carga automática de una aplicación o cuando se está procesando una solicitud fuera de secuencia. Cuando las aplicaciones se almacenan en la caché por completo, estos problemas ya no se producen.

## <a href="" id="error-displayed-after-an-update-is-removed-"></a>Error que se muestra después de quitar una actualización


Debe usar el formato de comando correcto de Windows Installer 3,1 para quitar una actualización del cliente de App-V, de la siguiente manera:

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

El uso del anterior formato de comando `msiexec /package <GUID> /uninstall <GUID>` producirá el error 6003 "no se pudo iniciar el cliente de Application Virtualization".

## Código de error 0A-0000E01E se produce cuando intenta iniciar una aplicación


Código de error 0A-0000E01E indica que el paquete de la aplicación secuenciada podría estar dañado. La solución es reordenar el paquete.

## Los usuarios no pueden acceder a los archivos que han creado en la unidad Q:


Si los usuarios guardan archivos en la unidad **Q:** , no pueden recuperarlos porque no tienen derechos de lectura en la unidad. Los usuarios no deben guardar los archivos en la unidad **Q:** .

## Se muestra un mensaje de error 1D1


Cuando la dirección URL de transmisión de archivos se establece incorrectamente en el archivo descriptor de software abierto (OSD), el cliente de App-V devuelve un error 1D1 en lugar de un error "no se encuentra el archivo". Este error indica que se produjo un error en el inicio de la aplicación y el usuario se ha forzado al modo de operaciones desconectado. Corrija la dirección URL de transmisión de archivos.

## Iconos incorrectos asociados con algunas aplicaciones


Cuando se va a usar un icono en una operación de publicación, el cliente de App-V determina en primer lugar si ya tiene una copia en caché del icono, consultando la caché de iconos de un elemento cuya ruta de acceso de origen original coincide con la ruta de acceso del icono dado a la operación de publicación. Si el cliente de App-V encuentra una coincidencia, usará el icono ya almacenado en caché; en caso contrario, se descargará el nuevo icono en la caché. Si la ruta de acceso al icono es un directorio de borrador o si se vuelve a utilizar para nuevos iconos o paquetes, la búsqueda en la memoria caché podría mostrar un icono incorrecto de una operación anterior.

## Se solicitan las credenciales a los usuarios al iniciar una aplicación


Si un usuario intenta iniciar una aplicación virtual a la que el administrador del sistema ha restringido el acceso, es posible que se le pida al usuario que escriba las credenciales. El usuario debe escribir el nombre de usuario y la contraseña de una cuenta que tenga permiso para iniciar la aplicación y, a continuación, presionar entrar.

## Se produce un error en la actualización de publicación después de actualizar el cliente de App-V a la versión 4,5


Si el directorio de datos de usuario se colocó anteriormente en una ubicación no estándar (%*ALLUSERSPROFILE*%\\Documents\\SoftGrid Client\\Users\\%*nombreusuario*%), los usuarios que no tengan privilegios de administrador en el equipo encontrarán la actualización de publicación después de que se actualice el cliente de App-V. Durante la actualización, el directorio de datos globales del cliente App-V y todos sus subdirectorios están configurados con derechos de acceso restringido solo para administradores. Para evitar este problema, cambie el directorio de datos de usuario antes de la actualización para que no sea un subdirectorio del directorio de datos global.

## Reinicio necesario después de un error de instalación


Si se produce un error en la instalación del cliente por cualquier motivo y, si los intentos posteriores de instalar el cliente también fallan, compruebe el registro de Windows Installer para ver si se muestra un error "sftplay error, error = 1072". Si es así, reinicie el equipo antes de intentar instalar el cliente de nuevo.

## Reparar una aplicación virtual dañada


Si, por cualquier motivo, un paquete de aplicaciones virtual instalado con un archivo de paquete de Windows Installer (MSI) se daña, vuelva a instalar el paquete. La función de reparación disponible en Windows Installer no actualizará los volúmenes de usuario.

## Temas relacionados


[Referencia del cliente de virtualización de aplicaciones](application-virtualization-client-reference.md)

 

 





