---
title: Consideraciones de seguridad de UE-V 1.0
description: Consideraciones de seguridad de UE-V 1.0
author: dansimp
ms.assetid: c5cdf9ff-dc96-4491-98e9-0eada898ffe0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b503028ae327f92759fe0f64f33fe0cffc62b05c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824000"
---
# Consideraciones de seguridad de UE-V 1.0


Este tema contiene una breve introducción a las cuentas y grupos, los archivos de registro y otras consideraciones relacionadas con la seguridad de la virtualización de la experiencia del usuario de Microsoft (UE-V). Para obtener más información, siga los vínculos que se proporcionan aquí.

## Consideraciones de seguridad para la configuración de UE-V


**Cuando cree el recurso compartido de almacenamiento de configuración, limite el acceso compartido a los usuarios que necesitan acceso.**

Como los paquetes de configuración pueden contener información personal, debe tener cuidado para protegerlos de la mejor manera posible. En general, haga lo siguiente:

-   Restringir el uso compartido solo a los usuarios que lo necesiten. Cree un grupo de seguridad para los usuarios que tengan carpetas redirigidas en un determinado recurso compartido y limite el acceso a solo esos usuarios.

-   Cuando crees el uso compartido, oculta el uso compartido colocando un $ después del nombre compartido. Esto ocultará el uso compartido de los exploradores ocasionales y el uso compartido no se verá en mis sitios de red.

-   Otorgue a los usuarios la cantidad mínima de permisos necesarios. Los permisos necesarios se muestran en las tablas siguientes.

    1.  Establezca los siguientes permisos de nivel de uso compartido (SMB) para la carpeta de ubicación de almacenamiento de configuración:

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left">Cuenta de usuario</th>
        <th align="left">Permisos recomendados</th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Todos</p></td>
        <td align="left"><p>No hay permisos</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Grupo de seguridad de UE-V</p></td>
        <td align="left"><p>Control total</p></td>
        </tr>
        </tbody>
        </table>



~~~
2.  Set the following NTFS permissions for the settings storage location folder:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Folder</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Admins</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Security group of UE-V users</p></td>
    <td align="left"><p>List Folder/Read Data, Create Folders/Append Data</p></td>
    <td align="left"><p>This Folder Only</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>Remove all Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    </tbody>
    </table>



3.  Set the following share-level (SMB) permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommend permissions</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>Read Permission Levels</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Read/Write Permission Levels</p></td>
    </tr>
    </tbody>
    </table>



4.  Set the following NTFS permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Apply to</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>List Folder Contents and Read</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    </tbody>
    </table>
~~~



### Usar servidores de Windows Server 2003 o versiones posteriores para hospedar recursos compartidos de archivos redirigidos

Los archivos del paquete de configuración de usuario contienen información personal que se transfiere entre el equipo cliente y el servidor que almacena los paquetes de configuración. Por ello, debe asegurarse de que los datos estén protegidos mientras viajan por la red.

Los datos de configuración de usuario son vulnerables a estas amenazas potenciales: interceptar los datos a medida que pasan por la red; manipulación de los datos a medida que pasan por la red; y imitación del servidor que hospeda los datos.

Varias características de Windows Server 2003 y versiones posteriores pueden ayudar a proteger los datos de usuario:

-   **Kerberos** : Kerberos es estándar en todas las versiones de Windows 2000 y windows Server 2003 y posteriores. Kerberos garantiza el nivel más alto de seguridad para los recursos de red. NTLM autentica solo al cliente; Kerberos autentica al servidor y al cliente. Cuando se usa NTLM, el cliente no sabe si el servidor es válido. Esto es especialmente importante si el cliente intercambia archivos personales con el servidor, como es el caso de los perfiles móviles. Kerberos proporciona mayor seguridad que NTLM. Kerberos no está disponible en Windows NT versión 4,0 o en sistemas operativos anteriores.

-   **IPSec** : el protocolo de seguridad IP (IPSec) proporciona autenticación de nivel de red, integridad de datos y cifrado. IPsec garantiza lo siguiente:

    -   Los datos móviles son seguros para la modificación de datos mientras se encuentra en tránsito.

    -   Los datos móviles son seguros para interceptar, ver o copiar.

    -   Es seguro que las personas sin autenticación acceden a los datos móviles.

-   **Firma SMB** : el protocolo de autenticación de bloque de mensajes de servidor (SMB) admite la autenticación de mensajes que evita los ataques de mensajes activos y "hombre en el medio". La firma SMB proporciona esta autenticación al colocar una firma digital en cada SMB. Después, el cliente y el servidor comprueban la firma digital. Para poder usar la firma SMB, primero debe habilitarla o requerirla en el cliente SMB y en el servidor SMB. Tenga en cuenta que la firma SMB impone una disminución del rendimiento. No consume más ancho de banda de la red, pero usa más ciclos de CPU en el cliente y el servidor.

### Usar siempre el sistema de archivos NTFS para los volúmenes que contienen datos de los usuarios

Para obtener la configuración más segura, configure los servidores que hospedan los archivos de configuración de UE-V para que usen el sistema de archivos NTFS. A diferencia de FAT, NTFS admite las listas de control de acceso discrecional (DACL) y las listas de control de acceso del sistema (SACL). Las DACL y las SACL controlan quién puede realizar operaciones en un archivo y qué eventos desencadenarán el registro de las acciones realizadas en un archivo.

### <a href="" id="do-not-rely-on-efs-to-encrypt-users--files-when-transmitted-over-the-network"></a>No confíe en EFS para cifrar los archivos de los usuarios cuando se transmitan a través de la red.

Al usar el sistema de archivos cifrados (EFS) para cifrar archivos en un servidor remoto, los datos cifrados no se cifran durante el tránsito a través de la red; Solo se cifrará cuando se almacene en disco.

Las excepciones para ello son cuando el sistema incluye seguridad de protocolo Internet (IPsec) o sistema distribuido de creación y control de versiones web (WebDAV). IPsec cifra los datos mientras se transfieren a través de una red TCP/IP. Si el archivo está cifrado antes de copiarlo o moverlo a una carpeta WebDAV de un servidor, permanecerá cifrado durante la transmisión y mientras esté almacenado en el servidor.

### Cifrar la caché de archivos sin conexión

De forma predeterminada, la caché de archivos sin conexión está protegida en particiones NTFS por ACL, pero el cifrado de la caché mejora aún más la seguridad en un equipo local. De forma predeterminada, la caché del equipo local no está cifrada, por lo que los archivos cifrados almacenados en caché de la red no se cifrarán en el equipo local. Esto puede suponer un riesgo de seguridad en algunos entornos.

Cuando el cifrado está habilitado, todos los archivos de la caché de archivos sin conexión están cifrados. Esto incluye el cifrado de archivos existentes, así como los archivos que se agregan más tarde. La copia en caché en el equipo local se ve afectada, pero no la copia de red asociada.

La caché se puede cifrar de una de estas dos maneras:

1.  A través de una directiva de grupo. -Habilite la opción **cifrar la memoria caché de archivos sin conexión** , ubicada en archivos de Configuration\\Administrative Templates\\Network\\Offline de equipo, en el editor de directivas de grupo.

2.  Automáticamente. -Seleccione Herramientas y, a continuación, opciones de carpeta en el menú de comandos del explorador de Windows. Seleccione la pestaña archivos sin conexión y, a continuación, seleccione la casilla **cifrar archivos sin conexión para proteger los datos** .

### Dejar que el agente de UE-V cree carpetas para cada usuario

Para asegurarse de que UE-V funcione de manera óptima, cree solo el recurso compartido raíz en el servidor y deje que el agente de UE-V cree las carpetas para cada usuario. UE-V creará estas carpetas de usuario con la seguridad adecuada.

Esta configuración de permisos permite a los usuarios crear carpetas para el almacenamiento de configuración. El agente UE-V crea y protege una carpeta settingspackage mientras se ejecuta en el contexto del usuario. El usuario recibe control total en su carpeta settingspackage. Otros usuarios no heredan el acceso a esta carpeta. No es necesario crear ni proteger directorios de usuarios individuales. El agente que se ejecuta en el contexto del usuario lo hará automáticamente.

**Nota**  
Se puede configurar la seguridad adicional cuando se usa un servidor de Windows para el recurso de almacenamiento de configuración. UE-V se puede configurar para comprobar que el grupo de administradores local o el usuario actual es el propietario de la carpeta donde se almacenan los paquetes de configuración. Para habilitar la seguridad adicional, use el siguiente comando:

1.  Agregue una clave del registro de REG \ _DWORD denominada "RepositoryOwnerCheckEnabled" `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .

2.  Establezca el valor de la clave del registro en 1.

Cuando esta configuración está en vigor, UE-V Agent comprueba que el grupo del administrador local o el usuario actual es el propietario de la carpeta settingspackage. De lo contrario, UE-V Agent no permitirá el acceso a la carpeta.



Si tiene que crear carpetas para los usuarios y asegurarse de que tiene los permisos correctos establecidos.

Le recomendamos encarecidamente que no precree carpetas y que, en su lugar, permita que UE-V Agent cree la carpeta para el usuario.

### <a href="" id="ensure-that-correct-permissions-are-set-when-storing-ue-v-settings-in-a-user-s-home-directory"></a>Asegurarse de que se configuran los permisos correctos al almacenar la configuración de UE-V en el directorio principal de un usuario

Si redirige la configuración de UE-V al directorio particular de un usuario, asegúrese de que los permisos en el directorio principal del usuario están establecidos correctamente para su organización.

## Temas relacionados


[Seguridad y privacidad para UE-V 1.0](security-and-privacy-for-ue-v-10.md)









