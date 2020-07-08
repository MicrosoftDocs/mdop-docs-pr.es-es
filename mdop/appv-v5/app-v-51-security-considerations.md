---
title: Consideraciones de seguridad de App-V 5.1
description: Consideraciones de seguridad de App-V 5.1
author: dansimp
ms.assetid: 6bc6c1fc-f813-47d4-b763-06fd4faf6a72
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a5606b3e0ba5e6fb8c62f14e2ed8d93ea2cf134
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814766"
---
# Consideraciones de seguridad de App-V 5.1


Este tema contiene una breve introducción a las cuentas y grupos, los archivos de registro y otras consideraciones relacionadas con la seguridad de Microsoft Application Virtualization (App-V) 5,1.

**Importante**  
App-V 5,1 no es un producto de seguridad y no proporciona ninguna garantía para un entorno seguro.



## La característica PackageStoreAccessControl (PSAC) ha quedado obsoleta


Desde el 2014 de junio de, la característica PackageStoreAccessControl (PSAC) que se introdujo en Microsoft Application Virtualization (App-V) 5,0 Service Pack 2 (SP2) ha quedado obsoleta en entornos con un único usuario y varios usuarios.

## Consideraciones generales de seguridad


**Comprender los riesgos de seguridad.** El riesgo más serio para App-V 5,1 es que un usuario no autorizado pudiera secuestrar su funcionalidad, que podría volver a configurar los datos clave en los clientes de App-V 5,1. La pérdida de la funcionalidad de App-V 5,1 durante un breve período de tiempo debido a un ataque de denegación de servicio generalmente no tendría un impacto catastrófico.

**Proteja físicamente sus equipos**. La seguridad está incompleta sin seguridad física. Cualquier persona que tenga acceso físico a un servidor de App-V 5,1 podría atacar toda la base de clientes. Cualquier posible ataque físico debe considerarse de alto riesgo y mitigarse de forma adecuada. Los servidores de App-V 5,1 deben almacenarse en una sala de servidores físicamente segura con acceso controlado. Proteja estos equipos cuando los administradores no estén presentes físicamente haciendo que el sistema operativo bloquee el equipo o usando un protector de pantalla seguro.

**Aplique las actualizaciones de seguridad más recientes a todos los equipos**. Para mantenerse informado acerca de las actualizaciones más recientes para sistemas operativos, Microsoft SQL Server y App-V 5,1, suscríbase al servicio de notificación de seguridad ( <https://go.microsoft.com/fwlink/p/?LinkId=28819> ).

**Use contraseñas seguras o frases**. Use siempre contraseñas seguras con 15 o más caracteres para todas las cuentas de administrador de App-V 5,1 y de App-V 5,1. Nunca use contraseñas en blanco. Para obtener más información sobre los conceptos de contraseñas, consulte las notas del producto "directivas y contraseñas de la cuenta" en TechNet ( <https://go.microsoft.com/fwlink/p/?LinkId=30009> ).

## Cuentas y grupos en App-V 5,1


Un procedimiento recomendado para la administración de cuentas de usuario es crear grupos globales de dominio y agregarles cuentas de usuario. Después, agregue las cuentas globales de dominio a los grupos locales App-V 5,1 en los servidores App-V 5,1.

**Nota**  
Las cuentas de equipos cliente de App-V que necesitan conectarse al servidor de publicación deben formar parte del grupo local de **usuarios** del servidor de publicación. De forma predeterminada, todos los equipos del dominio forman parte del grupo **usuarios autorizados** , que forma parte del grupo local **usuarios** .



### <a href="" id="-------------app-v-5-1-server-security"></a> Seguridad del servidor de App-V 5,1

Durante la instalación de App-V 5,1 no se crean grupos automáticamente. Debe crear los siguientes grupos globales de servicios de dominio de Active Directory para administrar las operaciones del servidor de App-V 5,1.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre de grupo</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Grupo de administradores de administración de App-V</p></td>
<td align="left"><p>Se usa para administrar el servidor de administración de App-V 5,1. Este grupo se crea durante la instalación de servidor de administración de App-V 5,1.</p>
<div class="alert">
<strong>Importante</strong><br/><p>No hay ningún método para crear el grupo con la consola de administración una vez completada la instalación.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Base de datos de lectura/escritura para la cuenta del servicio de administración</p></td>
<td align="left"><p>Proporciona acceso de lectura y escritura a la base de datos de administración. Esta cuenta debe crearse durante la instalación de la base de datos de administración de App-V 5,1.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Instalación de la cuenta de administrador del servicio de administración de App-V</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esto solo es necesario si la base de datos de administración se instala por separado del servicio.</p>
</div>
<div>

</div></td>
<td align="left"><p>Proporciona acceso público a la tabla de versión de esquema de la base de datos de administración. Esta cuenta debe crearse durante la instalación de la base de datos de administración de App-V 5,1.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Instalación de la cuenta de administrador de App-V Reporting Service</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esto solo es necesario si la base de datos de informes se instala por separado del servicio.</p>
</div>
<div>

</div></td>
<td align="left"><p>Acceso público a la tabla de versión de esquema de la base de datos de informes. Esta cuenta debe crearse durante la instalación de la base de datos de informes de App-V 5,1.</p></td>
</tr>
</tbody>
</table>



Considere la siguiente información adicional:

-   Acceso a los recursos compartidos del paquete: Si un recurso compartido se encuentra en el mismo equipo que el servidor de administración, el servicio de **red** requiere acceso de lectura al recurso compartido. Además, cada equipo cliente de App-V debe tener acceso de lectura al recurso compartido de paquete.

    **Nota**  
    En versiones anteriores de App-V, el recurso compartido de paquetes se denominaba recurso compartido de contenido.



-   Registrar servidores de publicación con el servidor de administración: un servidor de publicación debe estar registrado en el servidor de administración. Por ejemplo, debe agregarse a la base de datos para que las cuentas del equipo del servidor de publicación puedan llamar a la API del servicio de administración.

### <a href="" id="-------------app-v-5-1-package-security"></a> Seguridad del paquete de App-V 5,1

Lo siguiente le ayudará a planear cómo asegurarse de que los paquetes virtualizados sean seguros.

-   Si un instalador de aplicaciones aplica una lista de control de acceso (ACL) a un archivo o directorio, esa ACL no se conserva en el paquete. Cuando se implementa el paquete, si un usuario modifica el archivo o el directorio, este heredará la ACL en **% userprofile%** o heredará la ACL del directorio del equipo de destino. El primer caso se da si el archivo o directorio no existe en una ubicación de un sistema de archivos virtual; el último caso se produce si el archivo o el directorio existe en una ubicación del sistema de archivos virtual, por ejemplo, **% WINDIR%**.

## <a href="" id="---------app-v-5-1-log-files"></a> Archivos de registro de App-V 5,1


Durante la instalación de App-V 5,1, los archivos de registro de configuración se crean en la carpeta **% temp%** del usuario de instalación.






## Temas relacionados


[Preparación del entorno para App-V 5.1](preparing-your-environment-for-app-v-51.md)









