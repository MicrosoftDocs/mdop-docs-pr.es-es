---
title: Introducción técnica de AGPM
description: Introducción técnica de AGPM
author: dansimp
ms.assetid: 36bc0ab5-f752-474c-8559-721ea95169c2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cc635f46c2aabb0c9fa1f472a258a3e65a07b55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818300"
---
# Introducción técnica de AGPM


Administración avanzada de directivas de grupo (AGPM) de Microsoft es una aplicación cliente/servidor. El servidor AGPM almacena objetos de directiva de grupo (GPO) sin conexión en el archivo que AGPM crea en el sistema de archivos del servidor. Los administradores de directivas de grupo usan el complemento de AGPM para la consola de administración de directivas de grupo (GPMC) para trabajar con los GPO en el servidor que hospeda el archivo. Comprender las partes de AGPM y los elementos relacionados, cómo almacenan los GPO en el sistema de archivos y cómo los permisos que controlan las acciones disponibles para cada rol de usuario pueden mejorar la efectividad de los administradores de directivas de grupo con AGPM.

## Terminología


A continuación se explican las condiciones básicas de AGPM.

-   **Cliente de AGPM:** Un equipo que ejecuta el complemento de AGPM para la consola de administración de directivas de grupo (GPMC) y desde el que los administradores de directivas de grupo administran los GPO.

-   **Complemento de AGPM:** El componente de software de AGPM instalado en clientes de AGPM para que puedan administrar GPO.

-   **Servidor de AGPM:** Un servidor que ejecuta el servicio AGPM y administra un archivo. Cada servidor de AGPM puede administrar un solo archivo, pero un servidor de AGPM puede administrar los datos de archivo de varios dominios en un archivo. Un archivo se puede hospedar en un equipo que no sea un servidor de AGPM.

-   **Servicio AGPM:** El componente de software de AGPM que se ejecuta en un servidor de AGPM como servicio. El servicio administra los GPO en el archivo y en el entorno de producción de ese bosque.

-   **Archivo:** En AGPM, almacén central que contiene los GPO controlados que administra el servidor de AGPM asociado, además del historial de cada uno de esos GPO. Esto incluye todas las versiones controladas anteriores de cada GPO. Un archivo se compone de un archivo de índice de archivo y datos de archivo asociados que pueden incluir datos de los GPO de varios dominios. Un archivo se puede hospedar en un equipo que no sea un servidor de AGPM.

-   **GPO controlado:** Un GPO administrado por AGPM. AGPM administra el historial y los permisos de los GPO controlados, que se almacenan en el archivo.

-   **Objeto de directiva de grupo** no superpuesto: Un GPO en el entorno de producción para un dominio y no administrado por AGPM.

## Lo que AGPM instala, crea y afecta


En un servidor de AGPM, el programa de configuración de AGPM instala el servicio AGPM. AGPM no modifica el servicio de directorio® de Active Directory ni el esquema. De forma predeterminada, los archivos de programa del servidor AGPM se instalan en%ProgramFiles%\\Microsoft\\AGPM\\Server. Puede instalar el servicio AGPM en un controlador de dominio si es necesario; sin embargo, le recomendamos que instale el servicio AGPM en un servidor miembro.

En un cliente de AGPM, el programa de configuración de AGPM instala el complemento de AGPM y agrega una carpeta de **control de cambios** a cada dominio que aparece en la GPMC. De forma predeterminada, los archivos de programa cliente AGPM se instalan en%ProgramFiles%\\Microsoft\\AGPM\\Client.

En la tabla 1 se describen los elementos que AGPM instala o crea y las partes del sistema operativo que afectan a la operación AGPM.

**Tabla 1: elementos instalados, creados o afectados por AGPM**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servicio AGPM</p></td>
<td align="left"><p>El servicio AGPM se ejecuta en el servidor de AGPM. El servicio administra el archivo, que contiene los GPO desconectados y los GPO controlados en el entorno de producción. La configuración predeterminada del servicio AGPM es la siguiente:</p>
<ul>
<li><p><strong>Nombre del servicio: </strong> servicio AGPM</p></li>
<li><p><strong>Nombre para mostrar: </strong> servicio AGPM</p></li>
<li><p><strong>Ruta de acceso al ejecutable: </strong> % ProgramFiles% \Microsoft\AGPM\Server\Agpm.exe</p></li>
<li><p><strong>Inicio: </strong> automático</p></li>
<li><p><strong>Iniciar sesión como: </strong> cuenta de servicio AGPM especificada durante la instalación del servidor de AGPM, que se puede cambiar usando <strong> programas y características </strong> en el <strong> Panel de control </strong> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Archivo de AGPM</p></td>
<td align="left"><p>De forma predeterminada, AGPM crea el archivo en%ProgramData%\Microsoft\AGPM en el servidor de AGPM. El archivo proporciona almacenamiento para objetos de directiva de grupo desconectados y puede almacenar varias versiones de cada uno de ellos. Los cambios que AGPM realiza a los GPO en el archivo no afectan al entorno de producción hasta que un administrador o aprobador de AGPM implemente el GPO en el entorno de producción y vincule el GPO a una unidad organizativa (OU).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Firewall de Windows</p></td>
<td align="left"><p>Durante la instalación, AGPM habilita una regla de Firewall de Windows entrante que permite que el cliente de AGPM se comunique con el servidor de AGPM. La regla predeterminada de Firewall de Windows es la siguiente:</p>
<ul>
<li><p><strong>Nombre: </strong> servicio AGPM</p></li>
<li><p><strong>Acción: </strong> permitir la conexión</p></li>
<li><p><strong>Programas: </strong> todos los programas que cumplen las condiciones especificadas</p></li>
<li><p><strong>Tipo de protocolo: </strong> TCP</p></li>
<li><p><strong>Puerto local: </strong> 4600</p></li>
<li><p><strong>Puerto remoto: </strong> todos los puertos</p></li>
<li><p><strong>Dirección IP local: </strong> cualquiera</p></li>
<li><p><strong>Dirección IP remota: </strong> cualquiera</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de correo electrónico</p></td>
<td align="left"><p>AGPM usa el Protocolo simple de transferencia de correo (SMTP) para enviar solicitudes de correo electrónico a las direcciones configuradas en la <strong> pestaña delegación de dominios </strong> . Por ejemplo, cuando un editor solicita que se cree un nuevo GPO, AGPM notifica a cada dirección de correo electrónico especificada en la <strong> pestaña delegación de dominios </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Complemento AGPM</p></td>
<td align="left"><p>El complemento de AGPM para la GPMC se ejecuta en los clientes de AGPM y lo usan los administradores de la Directiva de grupo para administrar GPO. El complemento aparece en la GPMC como una <strong> </strong> carpeta de control de cambios en cada dominio.</p></td>
</tr>
</tbody>
</table>

 

### Referencias adicionales

Para obtener más información acerca de los archivos instalados por AGPM, consulte la [Guía de planeación de AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).

## Archive


De forma predeterminada, el proceso de instalación del servidor de AGPM crea el archivo en el disco duro local del servidor de AGPM en%ProgramData%\\Microsoft\\AGPM. Sin embargo, puede cambiar la ruta durante la instalación e incluso crear el archivo en un servidor que no sea el servidor de AGPM.

El archivo contiene una subcarpeta por cada versión de cada objeto de directiva de grupo que contiene el archivo. El nombre de cada subcarpeta es un GUID que identifica una versión del GPO.

El archivo gpostate.xml registra el estado de cada GPO en el archivo. El archivo es un manifiesto que describe el contenido del archivo. Por ejemplo, un GPO puede tener varias versiones, y cada versión está en su propia subcarpeta en el archivo. El archivo gpostate.xml indica qué subcarpetas contienen diferentes versiones de un único GPO. Además, las plantillas de GPO tienen subcarpetas en el archivo, pero gpostate.xml indica que se trata de plantillas y de objetos no controlados. De forma similar, cuando los administradores de directivas de grupo eliminan los GPO, AGPM cambia sus Estados en gpostate.xml para indicar que se encuentran en la **papelera de reciclaje** , pero que no quita realmente las subcarpetas de los GPO del archivo.

**PRECAUCIÓN**  No edite manualmente gpostate.xml o los GPO que contiene el archivo. Esta información solo se proporciona para mejorar la comprensión del archivo de AGPM. En su lugar, use el complemento de AGPM para cambiar los GPO.

 

Cuando AGPM crea el archivo, ofrece control total para el sistema, los administradores y la cuenta de servicio AGPM (especificada en la configuración del servidor de AGPM). El cambio de permisos mediante la interfaz de usuario de AGPM en el complemento de AGPM no modifica los permisos del archivo, ya que la cuenta de servicio AGPM realiza todas las operaciones en nombre del usuario que ha iniciado sesión.

### Referencias adicionales

Para obtener información sobre cómo realizar una copia de seguridad del archivo, restaurarlo a partir de una copia de seguridad o mover tanto el servidor de AGPM como el archivo, consulte la sección "realizar tareas de administrador de AGPM" en la [Guía de operaciones de AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).

## Roles y permisos


Roles simplificar la delegación. En lugar de asignar permisos detallados a los administradores de directivas de grupo, los administradores de AGPM pueden asignar uno de los cuatro roles a los administradores de directiva de grupo para permitirles realizar el trabajo relacionado con ese rol:

-   **Administrador AGPM:** Los administradores de la Directiva de grupo que tengan asignado el rol de administrador de AGPM (control total) pueden realizar cualquier tarea en AGPM. Los administradores de AGPM pueden configurar opciones para todo el dominio y delegar permisos a otros administradores de la Directiva de grupo.

-   **Aprobador:** Los administradores de la Directiva de grupo que tengan asignada la función de aprobador pueden implementar GPO en el entorno de producción de un dominio. Los aprobadores también pueden crear y eliminar objetos de directiva de grupo y aprobar o rechazar solicitudes de editores. Los aprobadores pueden ver la lista de GPO en un dominio, ver la configuración de la Directiva en los GPO y crear y ver informes de la configuración de la Directiva en un GPO. No pueden editar la configuración de la Directiva en los GPO a menos que también tengan asignada la función editor.

-   **Editor:** Los administradores de la Directiva de grupo que tengan asignada la función editor pueden ver la lista de GPO de un dominio, ver la configuración de la Directiva en los GPO, editar la configuración de la Directiva en los GPO y crear y ver informes de la configuración de la Directiva en un GPO. A menos que también se les asigne el rol de aprobador, los editores no podrán crear, implementar ni eliminar objetos de directiva de grupo. Sin embargo, pueden solicitar que los GPO se creen, se implementen o se eliminen.

-   **Revisor:** Los administradores de la Directiva de grupo que tienen asignada la función de revisor pueden ver la lista de los GPO de un dominio y crear y ver informes de la configuración de la Directiva en un GPO. A menos que se les asigne la función editor, no pueden editar la configuración de directiva en un GPO.

AGPM proporciona a los administradores de AGPM la flexibilidad de configurar permisos en un nivel más detallado que los roles mediante el complemento de AGPM. En la tabla 2 se describen estos permisos y se indican los permisos otorgados a cada rol de forma predeterminada.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Permiso</th>
<th align="left">Descripción</th>
<th align="left">Administrador AGPM</th>
<th align="left">Approver</th>
<th align="left">Procesador</th>
<th align="left">Revisor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Control total</strong></p></td>
<td align="left"><p>Tener todos los permisos.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Crear GPO</strong></p></td>
<td align="left"><p>Crear GPO en un dominio.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Contenido de la lista</strong></p></td>
<td align="left"><p>Enumere los GPO de un dominio.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Leer configuración</strong></p></td>
<td align="left"><p>Leer la configuración de la Directiva dentro de un objeto de directiva de grupo.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Editar configuración</strong></p></td>
<td align="left"><p>Cambiar la configuración de la Directiva en un GPO.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Eliminar GPO</strong></p></td>
<td align="left"><p>Eliminar un GPO.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Modificar la seguridad</strong></p></td>
<td align="left"><p>Delegar el acceso a nivel de dominio, delegar el acceso a un único GPO y delegar el acceso al entorno de producción.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Implementar GPO</strong></p></td>
<td align="left"><p>Implemente un GPO desde el archivo en el entorno de producción.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Crear plantilla</strong></p></td>
<td align="left"><p>Cree una plantilla de GPO en AGPM.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Modificar opciones</strong></p></td>
<td align="left"><p>Configurar la notificación de correo electrónico AGPM y limitar las versiones de GPO almacenadas en el archivo.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Exportar GPO</strong></p></td>
<td align="left"><p>Exportar un GPO a un archivo.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Importar GPO</strong></p></td>
<td align="left"><p>Importar un GPO desde un archivo.</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

**Nota:** 
 **Exportar** permisos de GPO y de **GPO de importación** no están disponibles en AGPM 3,0 o 2,5.

La capacidad de delegar el acceso a los GPO en el entorno de producción de un dominio y la capacidad de limitar el número de versiones de GPO almacenadas no están disponibles en AGPM 2,5.

 

### Referencias adicionales

Para obtener información acerca de qué tareas pueden realizar los administradores de directivas de grupo asignadas a una determinada función o sobre qué permisos son necesarios para realizar una tarea específica, consulte la [Guía de operaciones de AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).

 

 





