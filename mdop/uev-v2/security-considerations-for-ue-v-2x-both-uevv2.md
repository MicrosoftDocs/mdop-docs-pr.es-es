---
title: Consideraciones de seguridad para UE-V 2.x
description: Consideraciones de seguridad para UE-V 2.x
author: dansimp
ms.assetid: 9d5c3cae-9fcb-4dea-bd67-741b3dea63be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8e24e9e37de11053663bb90974fabf2ff369aeca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824661"
---
# Consideraciones de seguridad para UE-V 2.x


Este tema contiene una breve introducción a las cuentas y grupos, los archivos de registro y otras consideraciones relacionadas con la seguridad de virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1. Para obtener más información, siga los vínculos que se proporcionan aquí.

## Consideraciones de seguridad para la configuración de UE-V


**Importante**  Cuando cree el recurso compartido de almacenamiento de configuración, limite el acceso compartido a los usuarios que necesiten tener acceso.

 

Como los paquetes de configuración pueden contener información personal, debe tener cuidado para protegerlos al máximo. En general, haga lo siguiente:

-   Restrinja el uso compartido solo a los usuarios que requieran acceso. Cree un grupo de seguridad para los usuarios que hayan Redirigido carpetas en un recurso compartido determinado y limiten el acceso a solo esos usuarios.

-   Cuando crees el uso compartido, oculta el uso compartido colocando un $ después del nombre compartido. Esta adición oculta el uso compartido de los exploradores ocasionales y el uso compartido no está visible en mis sitios de red.

-   Otorgue a los usuarios la cantidad mínima de permisos que deben tener. En las tablas siguientes se muestran los permisos necesarios.

    1.  Establezca los siguientes permisos SMB de nivel de recurso compartido para la carpeta configuración de la ubicación de almacenamiento.

        | Cuenta de usuario | Permisos recomendados |
        | - | - |
        | Todos | No hay permisos |
        |Grupo de seguridad de UE-V | Control total |

    2.  Establezca los siguientes permisos del sistema de archivos NTFS en la carpeta de ubicación de almacenamiento de configuración.

        | Cuenta de usuario | Permisos recomendados | Carpeta |
        | - | - | - |
        | Creador/propietario | Control total | Solo subcarpetas y archivos|
        | Administradores de dominio | Control total | Esta carpeta, subcarpetas y archivos |
        | Grupo de seguridad de los usuarios de UE-V | Listar carpeta/leer datos, crear carpetas/anexar datos | Solo esta carpeta |
        | Todos | Quitar todos los permisos | No hay permisos |

    3.  Configure los siguientes permisos SMB de nivel de recurso compartido para la carpeta de catálogos de plantillas de configuración.

        | Cuenta de usuario | Recomendar permisos |
        | - | - |
        | Todos | No hay permisos |
        | Equipos del dominio | Niveles de permisos de lectura |
        | Administradores | Niveles de permisos de lectura y escritura |
         
    4.  Configure los siguientes permisos NTFS para la carpeta del catálogo de plantillas de configuración.

        | Cuenta de usuario | Permisos recomendados | Aplicar a |
        | - | - | - |
        | Creador/propietario | Control total | Esta carpeta, subcarpetas y archivos |
        | Equipos del dominio | Mostrar el contenido de la carpeta y los permisos de lectura | Esta carpeta, subcarpetas y archivos|
        | Todos| No hay permisos| No hay permisos|
        | Administradores| Control total| Esta carpeta, subcarpetas y archivos|

### Usar WindowsServer a partir de WindowsServer2003 para hospedar recursos compartidos de archivos

Los archivos del paquete de configuración de usuario contienen información personal que se transfiere entre el equipo cliente y el servidor que almacena los paquetes de configuración. Debido a este proceso, debe asegurarse de que los datos estén protegidos mientras se transmiten a través de la red.

Los datos de configuración de usuario son vulnerables a estas amenazas potenciales: interceptar los datos a medida que pasan por la red, alterando los datos a medida que pasan por la red y suplantación del servidor que los hospeda.

A partir de Windows Server2003, varias características del sistema operativo Windows Server pueden ayudar a proteger los datos de usuario:

-   **Kerberos** : Kerberos es estándar en todas las versiones de Microsoft Windows2000Server y windowsserver a partir de windowsserver2003. Kerberos garantiza el nivel más alto de seguridad para los recursos de red. NTLM autentica solo al cliente; Kerberos autentica al servidor y al cliente. Cuando se usa NTLM, el cliente no sabe si el servidor es válido. Esta diferencia es particularmente importante si el cliente intercambia archivos personales con el servidor, como es el caso de los perfiles de usuario itinerante. Kerberos proporciona mayor seguridad que NTLM. Kerberos no está disponible en los sistemas operativos Microsoft WindowsNTServer 4,0 o versiones anteriores.

-   **IPSec** : el protocolo de seguridad IP (IPSec) proporciona autenticación de nivel de red, integridad de datos y cifrado. IPsec garantiza lo siguiente:

    -   Los datos móviles son seguros para la modificación de datos mientras que los datos se encuentran en tránsito.

    -   Los datos móviles son seguros para interceptar, ver o copiar.

    -   Los datos móviles son seguros para el acceso por parte de terceros no autenticados.

-   **Firma SMB** : el protocolo de autenticación de bloque de mensajes de servidor (SMB) admite la autenticación de mensajes, lo que evita los ataques de mensaje activo y de "hombre en el medio". La firma SMB proporciona esta autenticación al colocar una firma digital en cada SMB. Después, el cliente y el servidor comprueban la firma digital. Para poder usar la firma SMB, primero debe habilitarla o bien, debe solicitarla en el cliente SMB y en el servidor SMB. Tenga en cuenta que la firma SMB impone una disminución del rendimiento. No consume más ancho de banda de la red, pero usa más ciclos de CPU en el cliente y el servidor.

### Usar siempre el sistema de archivos NTFS para los volúmenes que contienen datos de usuario

Para obtener la configuración más segura, configure los servidores que hospedan los archivos de configuración de UE-V para que usen el sistema de archivos NTFS. A diferencia del sistema de archivos FAT, NTFS admite listas de control de acceso discrecional (DACL) y listas de control de acceso al sistema (SACL). Las DACL y las SACL controlan quién puede realizar operaciones en un archivo y qué eventos desencadenan el registro de las acciones que se realizan en un archivo.

### No confíe en EFS para cifrar los archivos de usuario cuando se transmiten a través de la red.

Cuando se usa el sistema de archivos de cifrado (EFS) para cifrar archivos en un servidor remoto, los datos cifrados no se cifran durante el tránsito a través de la red; solo se cifrará cuando se almacene en el disco.

Este proceso de cifrado no se aplica cuando el sistema incluye seguridad de protocolo Internet (IPsec) o sistema distribuido de creación y control de versiones web (WebDAV). IPsec cifra los datos mientras se transfieren a través de una red TCP/IP. Si el archivo está cifrado antes de copiarlo o moverlo a una carpeta WebDAV en un servidor, permanece cifrado durante la transmisión y mientras se almacena en el servidor.

### Dejar que el agente de UE-V cree carpetas para cada usuario

Para asegurarse de que UE-V funcione de manera óptima, cree solo el recurso compartido raíz en el servidor y deje que el agente de UE-V cree las carpetas para cada usuario. UE-V crea estas carpetas de usuario con la seguridad adecuada.

Esta configuración de permisos permite a los usuarios crear carpetas para el almacenamiento de configuración. El agente de UE-V crea y protege una carpeta de paquete de configuración mientras se ejecuta en el contexto del usuario. Los usuarios reciben el control total de la carpeta del paquete de configuración. Otros usuarios no heredan el acceso a esta carpeta. No es necesario crear ni proteger directorios de usuarios individuales. El agente que se ejecuta en el contexto del usuario lo hace automáticamente.

**Nota:**  Se puede configurar la seguridad adicional cuando se usa un servidor de Windows para el recurso compartido de almacenamiento de configuración. UE-V se puede configurar para comprobar que el grupo de administradores local o el usuario actual es el propietario de la carpeta donde se almacenan los paquetes de configuración. Para habilitar la seguridad adicional, use el siguiente comando:

1.  Agregue la clave del registro REG \ _DWORD RepositoryOwnerCheckEnabled a `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .

2.  Establezca el valor de la clave del registro en *1*.

Cuando esta configuración está en vigor, UE-V Agent comprueba que el grupo de administradores local o el usuario actual es el propietario de la carpeta del paquete de configuración. Si no es así, UE-V Agent no concede acceso a la carpeta.

 

Si necesita crear carpetas para los usuarios, asegúrese de tener los permisos correctos establecidos.

Le recomendamos encarecidamente que no cree previamente carpetas. En su lugar, deje que el agente de UE-V cree la carpeta para el usuario.

### Garantizar los permisos correctos para almacenar la configuración de UE-V 2 en un directorio particular o personalizado

Si redirige la configuración de UE-V al directorio particular de un usuario o a un directorio personalizado de Active Directory (AD), asegúrese de que los permisos en el directorio se establecen correctamente para su organización.






## Temas relacionados


[Referencia técnica de UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





