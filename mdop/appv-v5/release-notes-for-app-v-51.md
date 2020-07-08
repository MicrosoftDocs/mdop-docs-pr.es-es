---
title: Notas de la versión de App-V 5.1
description: Notas de la versión de App-V 5.1
author: dansimp
ms.assetid: 62c5be3b-0a46-4512-93ed-97c23184f343
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2016
ms.openlocfilehash: 7437a16bc10b21bb15b0f8307c2711177e78cb72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813310"
---
# Notas de la versión de App-V 5.1


A continuación se muestran algunos problemas conocidos de Microsoft Application Virtualization (App-V) 5,1.

## Se produce un error durante la actualización de publicación entre el servidor de administración de App-V 5,0 SP3 y el cliente de App-V 5,1 en Windows 10


Se genera un error durante la actualización de publicación al sincronizar paquetes desde el servidor de administración de App-V 5,0 SP3 a un cliente de App-V 5,1 en Windows 10. Este error se produce porque el servidor de App-V 5,0 SP3 no comprende el sistema operativo Windows 10 que se especifica en la dirección URL de publicación. El problema se ha corregido en el servidor de publicación de App-V 5,1, pero no se ha importado a las versiones de App-V 5,0 SP3 o anterior.

**Solución**: actualice el servidor de administración de App-v 5,0 al servidor de administración de App-v 5,1 para clientes de Windows 10.

## Las configuraciones personalizadas no se aplican a los paquetes que se publicarán globalmente si se configuran con el servidor de App-V 5,1


Si asigna un paquete a un grupo de AD que contiene cuentas de equipo y aplica una configuración personalizada a ese grupo con el servidor de App-V, la configuración personalizada no se aplicará a esos equipos. El cliente de App-V 5,1 publicará paquetes asignados a una cuenta de equipo en todo el mundo. Sin embargo, almacena los archivos de configuración personalizados por usuario en el perfil de cada usuario. Los paquetes publicados globalmente no tendrán acceso a esta configuración personalizada.

**Solución alternativa**: realice una de las siguientes acciones:

-   Asigne el paquete a grupos que contengan solo cuentas de usuario. Esto asegurará que la configuración personalizada del paquete se almacenará en el perfil de cada usuario y se aplicará correctamente.

-   Cree un archivo de configuración de implementación personalizado y aplíquelo al paquete en el cliente con el cmdlet Add-AppvClientPackage con el parámetro – DynamicDeploymentConfiguration. Para obtener más información [, consulta acerca de la configuración dinámica de App-V 5,1](about-app-v-51-dynamic-configuration.md) .

-   Cree un paquete nuevo con la configuración personalizada mediante el secuenciador de aplicaciones-V 5,1.

## Archivos de servidor no eliminados después de la instalación de la nueva aplicación: V 5,1 Server


Si desinstala el servidor de App-V 5,0 SP1 y luego instala el servidor de App-V 5,1, se producirá un error en la instalación, se instalará la versión incorrecta del servidor de administración y se devolverá un mensaje de error. El problema se produce porque los archivos del servidor no se eliminan al desinstalar App-V 5,0 SP1, por lo que el proceso de instalación realiza una actualización en lugar de una instalación nueva.

**Solución alternativa**: Elimine esta clave del registro antes de empezar a instalar App-V 5,1:

En HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall, busque y elimine la clave GUID de instalación que contiene el valor DWORD "DisplayName" con datos de valor "Microsoft Application Virtualization (App-V) Server". Esta es la única tecla que debe eliminarse.

## Las asociaciones de tipos de archivo agregadas manualmente no se guardan correctamente


Las asociaciones de tipos de archivo agregadas manualmente a un paquete de aplicación mediante los accesos directos y la ficha FTAs al final del Asistente para actualización de aplicaciones no se guardan correctamente. No estarán disponibles para el cliente de App-V ni para el secuenciador cuando actualice el paquete guardado de nuevo.

**Solución alternativa**: para agregar una asociación de tipo de archivo, abra el paquete para modificar y ejecute el Asistente para actualización. Durante el paso de instalación, agregue la nueva asociación de tipo de archivo a través del sistema operativo. El secuenciador detectará la nueva asociación en el registro del sistema y la agregará al registro virtual del paquete, donde estará disponible para el cliente.

## Al transmitir paquetes en el modo de almacén de contenido compartido (SCS) a un cliente que también se administra con AppLocker, se escriben datos adicionales en el disco local.


Para reducir la cantidad de datos que se escriben en el disco local de un cliente, puede habilitar el modo SCS en el cliente de App-V 5,1 para transmitir el contenido de un paquete a petición. Sin embargo, si AppLocker administra una aplicación dentro del paquete, algunos datos podrían escribirse en el disco local del cliente que no se escribiría de otra manera.

**Solución alternativa**: ninguna

## En el cuadro de diálogo Agregar paquete de consola de administración, el botón examinar no está disponible al usar Chrome o Firefox


En la página paquetes de la consola de administración, si hace clic en **Agregar o actualizar** en la esquina inferior derecha, aparece el cuadro de diálogo **Agregar paquete** . Si accede a la consola de administración con Chrome o Firefox como explorador, no podrá desplazarse hasta la ubicación del paquete.

**Solución alternativa**: escriba o copie y pegue la ruta de acceso al paquete en el campo **Agregar paquete** de entrada. Si la consola de administración tiene acceso a esta ruta de acceso, podrá agregar el paquete. Si el paquete está en un recurso compartido de red, puede ir a la ubicación con el explorador de archivos siguiendo estos pasos:

1.  Mantenga pulsada la **tecla Mayús**y haga clic con el botón derecho en el archivo del paquete.

2.  Seleccione **Copiar como ruta de acceso**

3.  Pegue la ruta de acceso en el campo de entrada del cuadro de diálogo **Agregar paquete**

## <a href="" id="upgrading-app-v-management-server-to-5-1-sometimes-fails-with-the-message--a-database-error-occurred-"></a>Al actualizar App-V Management Server a 5,1, a veces se produce un error con el mensaje "se ha producido un error de base de datos"


Si instala el servidor de administración de App-V 5,0 SP1 y, a continuación, intenta actualizar a App-V 5,1 Server cuando se han configurado y habilitado varios grupos de conexión, se muestra el siguiente error: "error de base de datos. Motivo: ' nombre de columna no válido ' PackageOptional '. Nombre de columna no válido ' VersionOptional '.

**Solución**: ejecute este comando en la base de datos SQL:

`ALTER TABLE AppVManagement.dbo.PackageGroupMembers ADD PackageOptional bit NOT NULL DEFAULT 0, VersionOptional bit NOT NULL DEFAULT 0`

donde "AppVManagement" es el nombre de la base de datos.

## Los usuarios no pueden abrir un paquete en un grupo de conexión publicado por el usuario si agrega o quita un paquete opcional


En los entornos en los que se ejecuta el cliente RDS o que tienen varios usuarios simultáneos por equipo, los usuarios con sesión iniciada no pueden abrir aplicaciones en paquetes que se encuentren en un grupo de conexiones publicadas por el usuario si se agrega o se quita un paquete opcional del grupo de conexiones.

**Solución alternativa**: haga que los usuarios cierren sesión y vuelva a iniciarla.

## El mensaje de error se muestra de forma incorrecta cuando el grupo de conexión se publica solo para el usuario


Cuando ejecute repair-AppvClientConnectionGroup, se mostrará el error siguiente, incluso cuando el grupo de conexión se publique solo para el usuario: "error de integración de la aplicación interna: el paquete no está integrado para el usuario. Asegúrese de que el paquete se agregue a la máquina y se publique para el usuario.

**Solución alternativa**: realice una de las siguientes acciones:

-   Publicar todos los paquetes de un grupo de conexiones.

    El problema surge cuando el grupo de conexión que se repara tiene paquetes que faltan o que no están disponibles para el usuario (es decir, no se publican globalmente ni al usuario). Sin embargo, la reparación funcionará si todos los paquetes del grupo de conexión están disponibles, así que asegúrese de que todos los paquetes estén publicados.

-   Para reparar paquetes de forma individual, use el comando repair-AppvClientPackage en lugar del comando repair-AppvClientConnectionGroup.

    Determine qué paquetes estarán disponibles para los usuarios y, a continuación, ejecute el comando repair-AppvClientPackage una vez para cada paquete. Use los cmdlets de PowerShell para hacer lo siguiente:

    1.  Obtener todos los paquetes de un grupo de conexiones.

    2.  Compruebe si cada paquete está publicado actualmente.

    3.  Si el paquete está publicado actualmente, ejecute repair-AppvClientPackage en ese paquete.

## Los iconos no se muestran correctamente en el secuenciador


Los iconos de las pestañas accesos directos y asociaciones de tipos de archivo no se muestran correctamente al modificar un paquete en el secuenciador de App-V. Este problema se produce cuando el tamaño de los iconos no es 16x16 ni de 32x32.

**Solución alternativa**: Use iconos que sean 16x16 o 32x32.

## La secuencia de comandos InsertVersionInfo. SQL ya no es necesaria para la base de datos de administración


La secuencia de comandos InsertVersionInfo. SQL no es necesaria para las versiones de la base de datos de administración de App-V 5,0 SP3 más tarde que App-V SP3.

La secuencia de comandos Permissions. SQL debe actualizarse de acuerdo con el **paso 2** del [artículo 3031340 de KB](https://support.microsoft.com/kb/3031340).

**Importante** 
 El **paso 1** no es necesario para las versiones de App-v posteriores a App-V 5,0 SP3.

 

## Microsoft Visual Studio 2012 no es compatible


App-V 5,1 no admite Visual Studio 2012.

**Solución alternativa**: ninguna

## Restricciones del nombre de archivo de la aplicación para el secuenciador de App-V 5. x


El secuenciador de App-V 5. x no puede secuenciar aplicaciones con nombres de archivo que coincidan con "CO_ &lt; x &gt; " donde x es un número. Se generará el error 0x8007139F.

**Solución alternativa**: use otro nombre de archivo

## Error intermitente "archivo no encontrado" al montar un paquete


En ocasiones, al montar un paquete, se genera un error "archivo no encontrado" (0x80070002). Esto suele ocurrir cuando una carpeta en un paquete de App-V contiene muchos archivos (es decir, 20.000 o más). Esto puede provocar que la transmisión tarde más de lo esperado y que se agote el tiempo de espera, lo que genera el error "no se encuentra el archivo".

**Solución alternativa**: a partir de HF06, se ha introducido una nueva clave del registro para habilitar la extensión de este período de tiempo de espera.

<table>
<colgroup>
<col width="20%" />
<col width="80%" />
</colgroup>
<tbody>
<tr>
<td align="left">Ruta de acceso</td>
<td align="left">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\Streaming</td>
</tr>
<tr>
<td align="left">Configuración</td>
<td align="left">StreamResponseWaitTimeout</td>
</tr>
<tr>
<td align="left">Tipo de de</td>
<td align="left">DWORD</td>
</tr>
<tr>
<td align="left">Unit</td>
<td align="left">Segundos</td>
</tr>
<tr>
<td align="left">Predeterminado</td>
<td align="left">4<br />
<strong>Nota </strong> : este valor es el predeterminado si la clave del registro no está definida o se &lt; especifica un valor = 5.
</td>
</tr>
</tbody>
</table>






## Temas relacionados


[Acerca de App-V 5.1](about-app-v-51.md)

 

 





