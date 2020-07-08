---
title: Acerca de App-V 5.1
description: Acerca de App-V 5.1
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4f2404dcd431b32f5d9a4ae7c49f1e376979e04e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814950"
---
# Acerca de App-V 5.1


Use las siguientes secciones para revisar la información sobre los cambios significativos que se aplican a Application Virtualization (App-V) 5,1:

[Requisitos previos de software de App-V 5,1 y configuraciones admitidas](#bkmk-51-prereq-configs)

[Migrar a App-V 5,1](#bkmk-migrate-to-51)

[Novedades de App-V 5,1](#bkmk-whatsnew)

[Compatibilidad de App-V para Windows 10](#bkmk-win10support)

[Cambios en la consola de administración de App-V](#bkmk-mgmtconsole)

[Mejoras en el secuenciador](#bkmk-seqimprove)

[Mejoras en el conversor de paquetes](#bkmk-pkgconvimprove)

[Compatibilidad con varios scripts en un solo desencadenador de eventos](#bkmk-supmultscripts)

[La ruta de acceso codificada de la carpeta de instalación se redirige a la raíz del sistema de archivos virtual](#bkmk-hardcodepath)

## <a href="" id="bkmk-51-prereq-configs"></a>Requisitos previos de software de App-V 5,1 y configuraciones admitidas


Consulte los siguientes vínculos para los requisitos previos del software de App-V 5,1 y las configuraciones admitidas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Vínculos a requisitos previos y configuraciones admitidas</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-51-prerequisites.md" data-raw-source="[App-V 5.1 Prerequisites](app-v-51-prerequisites.md)">Requisitos previos de App-V 5.1</a></p></td>
<td align="left"><p>Requisitos previos de software que debe instalar antes de iniciar la instalación de App-V 5,1</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">Configuraciones compatibles con App-V 5.1</a></p></td>
<td align="left"><p>Requisitos de hardware y sistemas operativos compatibles con el servidor de App-V, el secuenciador y los componentes de cliente</p></td>
</tr>
</tbody>
</table>



**Compatibilidad con el uso del administrador de configuración con App-V:** App-V 5,1 es compatible con System Center 2012 R2 Configuration Manager SP1. Consulte [planificación de la integración de App-v con Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) para obtener información sobre cómo integrar el entorno de App-v con Configuration Manager y Configuration Manager.

## <a href="" id="bkmk-migrate-to-51"></a>Migrar a App-V 5,1


Use la siguiente información para actualizar a App-V 5,1 desde versiones anteriores. Para obtener más información [, consulte migrar a App-V 5,1 desde una versión anterior](migrating-to-app-v-51-from-a-previous-version.md) .

### Antes de iniciar la actualización

Revise la siguiente información antes de iniciar la actualización:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elementos para revisar antes de actualizar</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Componentes para actualizar, en cualquier orden</p></td>
<td align="left"><ol>
<li><p>Servidor de App-V</p></li>
<li><p>Secuenciador</p></li>
<li><p>Cliente de App-V o de servicios de escritorio remoto (RDS) de App-V</p></li>
</ol>
<div class="alert">
<strong>Nota</strong><br/><p>Antes de la aplicación-V 5,0 SP2, la interfaz de usuario de administración de clientes se proporcionó con la instalación del cliente de App-V. Para las instalaciones de App-V 5,0 SP2 (o versiones posteriores), puede usar la interfaz de usuario de administración de cliente si descarga de la <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> aplicación de interfaz de usuario del cliente de Application virtualization 5,0 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Actualizando desde App-V 4. x</p></td>
<td align="left"><p>Primero debe actualizar a App-V 5,0. No puede actualizar directamente de App-V 4. x a App-V 5,1. Para más información, consulta lo siguiente:</p>
<ul>
<li><p>"Diferencias entre App-V 4,6 y App-V 5,0" en <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"> acerca de App-v 5,0</a></p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)">Planificación para migrar desde una versión anterior de App-V</a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Actualización de App-V 5,0 o posterior</p></td>
<td align="left"><p>Puede actualizar a App-V 5,1 directamente desde cualquiera de las siguientes versiones:</p>
<ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
<li><p>App-V 5,0 SP3</p></li>
</ul>
<p>Para actualizar a App-V 5,1, siga los pasos que se indican en el resto de las secciones de este tema.</p>
<p>Los paquetes y grupos de conexión seguirán funcionando con App-V 5,1 ya que actualmente lo hacen.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a>Pasos para actualizar la infraestructura de App-V

Complete los siguientes pasos para actualizar cada componente de la infraestructura de App-V a App-V 5,1. El siguiente orden es solo una sugerencia; puede actualizar los componentes en cualquier orden.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paso</th>
<th align="left">Para más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Paso 1: actualizar el servidor de App-V.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si no usa el servidor de App-V, omita este paso y vaya al siguiente paso.</p>
</div>
<div>

</div></td>
<td align="left"><p>Sigue estos pasos:</p>
<ol>
<li><p>Siga uno de estos procedimientos, según el método que use para actualizar la base de datos de administración o la base de datos de informes:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método de actualización de base de datos</th>
<th align="left">Paso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Installer</p></td>
<td align="left"><p>Omita este paso y vaya al paso 2, "si está actualizando el servidor de App-V..."</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scripts SQL</p></td>
<td align="left"><p>Siga los pasos <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> que se indican en cómo implementar las bases de datos de App-V con scripts SQL </a> .</p></td>
</tr>
</tbody>
</table>
<li><p>Si está actualizando el servidor de App-V desde el paquete de revisiones 3 o posterior de App-V 5,0 SP1, complete los pasos de la sección <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)"> comprobar las claves del registro después de instalar el servidor de App-V 5,0 SP3 </a> .</p></li>
<li><p>Siga los pasos <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> que se indican en cómo implementar el servidor de App-V 5,1</a></p></li>
<p> </p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Paso 2: actualice el secuenciador de App-V.</p></td>
<td align="left"><p>Vea <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> Cómo instalar el secuenciador </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Paso 3: actualizar el cliente de App-V o de App-V RDS.</p></td>
<td align="left"><p>Consulta <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> cómo implementar el cliente de App-V </a> .</p></td>
</tr>
</tbody>
</table>



### Conversión de paquetes creados con una versión anterior de App-V

Use la utilidad de conversión de paquetes para actualizar paquetes de aplicaciones virtuales creados con versiones de App-V anteriores a App-V 5,0. El convertidor de paquetes usa PowerShell para convertir paquetes y puede ayudar a automatizar el proceso si tiene muchos paquetes que requieren conversión.

**Nota**  
Los paquetes de App-V 5,1 son exactamente iguales a los de App-V 5,0. No se ha realizado ningún cambio en el formato de paquete entre las versiones, por lo que no es necesario convertir los paquetes de App-V 5,0 en paquetes de App-V 5,1.



## <a href="" id="bkmk-whatsnew"></a>Novedades de App-V 5,1


Estas secciones son para usuarios que ya están familiarizados con App-V y desean saber qué ha cambiado en App-V 5,1. Si aún no está familiarizado con App-V, debe empezar por leer [la planificación de App-v 5,1](planning-for-app-v-51.md).

### <a href="" id="bkmk-win10support"></a>Compatibilidad de App-V para Windows 10

En la siguiente tabla se muestra el soporte técnico de Windows 10 para App-V. Windows 10 no es compatible con las versiones de App-V anteriores a App-V 5,1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente</th>
<th align="left">5.1 de App-V</th>
<th align="left">App-V 5,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Cliente de App-V</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente RDS de App-V</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Secuenciador de App-V</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>No</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-mgmtconsole"></a>Cambios en la consola de administración de App-V

En esta sección se compara la funcionalidad actual y actual de la consola de administración de App-V.

### Silverlight ya no es necesario

La interfaz de usuario de la consola de administración ya no requiere Silverlight. La consola de administración de 5,1 está integrada en HTML5 y JavaScript.

### Las notificaciones y los mensajes se muestran individualmente en un cuadro de diálogo

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nuevo en App-V 5,1</th>
<th align="left">Antes de la aplicación-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Indicador de número de mensajes:</strong></p>
<p>En la barra de título de la consola de administración de App-V, se muestra un número junto a un icono de indicador para indicar el número de mensajes que están esperando para ser leídos.</p></td>
<td align="left"><p>Solo puedes ver un mensaje o un error a la vez, y no pudimos determinar cuántos mensajes había.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Apariencia del mensaje:</strong></p>
<ul>
<li><p>Los mensajes que requieren la intervención del usuario se muestran en un cuadro de diálogo independiente que se muestra en la parte superior de la página actual que estaba viendo y requieren una respuesta antes de poder descartarlos.</p></li>
<li><p>Los mensajes y errores aparecen en una lista, con uno debajo del otro.</p></li>
</ul></td>
<td align="left"><p>Solo puede ver un mensaje o error a la vez.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Desechar mensajes:</strong></p>
<p>Use el <strong> vínculo descartar todos </strong> para descartar todos los mensajes y errores a la vez, o bien descartarlos de uno en uno.</p></td>
<td align="left"><p>Puede descartar mensajes y errores solo de uno en uno.</p></td>
</tr>
</tbody>
</table>



### Las páginas de la consola ahora son direcciones URL independientes

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nuevo en App-V 5,1</th>
<th align="left">Antes de la aplicación-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Cada página de la consola tiene una dirección URL diferente, lo que le permite marcar páginas específicas para acceder rápidamente en el futuro.</p>
<p>El número que aparece en algunas direcciones URL indica el paquete específico. Estos números son únicos.</p></td>
<td align="left"><p>Se obtiene acceso a todas las páginas de la consola a través de la misma dirección URL.</p></td>
</tr>
</tbody>
</table>



### Nueva página de grupos de conexiones y opción de menú independientes

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nuevo en App-V 5,1</th>
<th align="left">Antes de la aplicación-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ahora, la página grupos de conexión forma parte del menú principal, en el mismo nivel que la página paquetes.</p></td>
<td align="left"><p>Para abrir la página de grupos de conexión, navegue por la página paquetes.</p></td>
</tr>
</tbody>
</table>



### Las opciones de menú de los paquetes han cambiado

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nuevo en App-V 5,1</th>
<th align="left">Antes de la aplicación-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Las siguientes opciones son ahora botones que aparecen en la parte inferior de la página paquetes:</p>
<ul>
<li><p>Agregar o actualizar</p></li>
<li><p>Publicar</p></li>
<li><p>Quitar</p></li>
<li><p>Eliminar</p></li>
</ul>
<p>Las siguientes opciones seguirán apareciendo al hacer clic con el botón secundario del ratón en un paquete para abrir el menú contextual:</p>
<ul>
<li><p>Publicar</p></li>
<li><p>Quitar</p></li>
<li><p>Editar el acceso a AD</p></li>
<li><p>Editar configuración de implementación</p></li>
<li><p>Transferir configuración de implementación desde...</p></li>
<li><p>Transferir acceso y configuración de...</p></li>
<li><p>Eliminar</p></li>
</ul>
<p>Al hacer clic en <strong> eliminar </strong> para quitar un paquete, se abre un cuadro de diálogo en el que se le pide que confirme que desea eliminar el paquete.</p></td>
<td align="left"><p>La <strong> opción Agregar o actualizar </strong> era un botón en la parte superior derecha de la página paquetes.</p>
<p>Las <strong> Opciones publicar, anular la </strong> <strong> publicación </strong> y <strong> eliminar </strong> solo estaban disponibles si hizo clic con el botón derecho en el nombre de un paquete en la lista paquetes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Las siguientes operaciones de paquete son ahora botones en la página Detalles del paquete de cada paquete:</p>
<ul>
<li><p>Transferir (menú desplegable con las siguientes opciones):</p>
<ul>
<li><p>Transferir configuración de implementación desde...</p></li>
<li><p>Transferir acceso y configuración de...</p></li>
</ul></li>
<li><p>Editar (grupos de conexión y acceso a AD)</p></li>
<li><p>Quitar</p></li>
<li><p>Eliminar</p></li>
<li><p>Editar configuración predeterminada</p></li>
</ul></td>
<td align="left"><p>Estas opciones de paquete solo estaban disponibles si hace clic con el botón derecho en el nombre de un paquete en la lista paquetes.</p></td>
</tr>
</tbody>
</table>



### Los iconos del panel izquierdo tienen colores y texto nuevos

Se han cambiado los colores de los iconos en el panel izquierdo y se ha agregado texto para que los iconos sean coherentes con otros productos de Microsoft.

### Se ha eliminado la página de información general

En el panel izquierdo de la consola de administración, se ha eliminado la opción del menú información general y la página de descripción asociada.

### <a href="" id="bkmk-seqimprove"></a>Mejoras en el secuenciador

Se han realizado las siguientes mejoras en el editor de paquetes en el secuenciador de aplicaciones-V 5,1.

### Importar y exportar el archivo de manifiesto

Puede importar y exportar el archivo de AppxManifest.xml. Para exportar el archivo de manifiesto, seleccione la pestaña **avanzadas** y en el cuadro archivo de manifiesto, haga clic en **exportar...**. Puede realizar cambios en el archivo de manifiesto, como quitar extensiones de shell o editar asociaciones de tipos de archivo.

Después de realizar los cambios, haga clic en **Importar...** y seleccione el archivo que editó. Una vez que lo haya importado correctamente, el archivo de manifiesto se actualizará inmediatamente en el editor de paquetes.

**Actúe**  
Al importar el archivo, los cambios se validan en el esquema XML. Si el archivo no es válido, recibirá un error. Tenga en cuenta que es posible importar un archivo que se valida con el esquema XML, pero que todavía no se puede ejecutar por otros motivos.



### Agregar Windows 10 a la lista de sistemas operativos

En la pestaña implementación, se agregaron Windows 10 32 bits y Windows 10-64 bit a la lista de sistemas operativos para los que puede secuenciar un paquete. Si selecciona **cualquier sistema operativo**, Windows 10 se incluye automáticamente entre los sistemas operativos que admitirá el paquete secuenciado.

### La ruta de acceso actual se muestra en la parte inferior del editor de registro virtual

En la pestaña registro virtual, la ruta de acceso se muestra ahora en la parte inferior del editor de registro virtual, lo que le permite determinar la clave seleccionada actualmente. Anteriormente, tenía que desplazarte por el árbol del registro para encontrar la clave seleccionada actualmente.

### <a href="" id="combined--find-and-replace--dialog-box-and-shortcut-keys-added-in-virtual-registry-editor"></a>Cuadro de diálogo combinado "buscar y reemplazar" y las teclas de método abreviado agregadas en el editor del registro virtual

En el editor del registro virtual, se han agregado teclas de método abreviado para la opción Buscar (Ctrl + b), y un cuadro de diálogo que combina las tareas "Buscar" y "reemplazar" que le permiten buscar y reemplazar valores y datos. Para obtener acceso a este cuadro de diálogo combinado, seleccione una clave y realice una de las siguientes acciones:

-   Presione **Ctrl + H**

-   Haga clic con el botón secundario en una tecla y seleccione **reemplazar**.

-   Seleccione **Ver** el &gt; **reemplazo del registro virtual** &gt; **Replace**.

Anteriormente, el cuadro de diálogo "reemplazar" no existía y el usuario tenía que realizar cambios de forma manual.

### Cambiar el nombre de las claves del registro y los archivos del paquete correctamente

Puede cambiar el nombre de archivos y claves de registro virtuales sin experimentar problemas con el secuenciador. Anteriormente, el secuenciador dejó de funcionar si intentabas cambiar el nombre de una clave.

### Importar y exportar claves de registro virtuales

Puede importar y exportar claves de registro virtuales. Para importar una clave, haga clic con el botón secundario en el nodo en el que desea importar la clave, navegue hasta la clave que desea importar y, a continuación, haga clic en **importar**. Para exportar una clave, haga clic con el botón derecho en ella y seleccione **exportar**.

### Importar un directorio al sistema de archivos virtual

Puede importar un directorio en el VFS. Para importar un directorio, haga clic en la pestaña **archivos de paquete** y, a continuación, haga clic en **Ver** &gt; Directorio de importación **del sistema de archivos virtual** &gt; **Import Directory**. Si intenta importar un directorio que contiene archivos que ya están en el VFS, se produce un error en la importación y se muestra un mensaje explicativo. Antes de la 5,1 de App-V, no pudiste importar directorios.

### Importar o exportar un archivo VFS sin tener que eliminarlo y, después, volver a agregarlo al paquete

Puede importar o exportar archivos del VFS sin tener que eliminar el archivo y, después, volver a agregarlo al paquete. Por ejemplo, puede usar esta característica para exportar un registro de cambios a una unidad local, editar el archivo con un editor externo y, a continuación, volver a importar el archivo en el VFS.

Para exportar un archivo, seleccione la pestaña **archivos del paquete** , haga clic con el botón derecho en el archivo en el VFS, haga clic en **exportar**y elija una ubicación de exportación desde la que pueda hacer las modificaciones.

Para importar un archivo, seleccione la pestaña **archivos de paquete** y haga clic con el botón derecho en el archivo que ha exportado. Busque el archivo que editó y, a continuación, haga clic en **importar**. El archivo importado sobrescribirá el archivo existente.

Después de importar un archivo, debe guardarlo haciendo clic en guardar **archivo** &gt; **Save**.

### El menú para agregar un archivo de paquete ha sido movido

Se movió la opción de menú para agregar un archivo de paquete. Para buscar la opción Agregar, seleccione la pestaña **archivos del paquete** y, a continuación, haga clic en **Ver** &gt; **archivo del sistema de archivos virtual** &gt; **Add File**. Anteriormente, se hizo clic con el botón secundario del mouse en una carpeta bajo el nodo VFS y se eligió **Agregar archivo**.

### El nodo de registro virtual expande secciones de equipos y usuarios de forma predeterminada

Al abrir el registro virtual, las secciones equipo y usuario se muestran debajo del nodo de nivel superior del registro. Anteriormente, tenía que expandir el nodo del registro para mostrar los subárboles debajo.

### Habilitar o deshabilitar objetos auxiliares del explorador

Puede habilitar o deshabilitar objetos auxiliares del explorador activando una nueva casilla, habilitando los objetos auxiliares del explorador, en la pestaña avanzadas de la interfaz de usuario del secuenciador. Si los objetos auxiliares del explorador:

-   Existe en el paquete y están habilitados, la casilla de verificación está activada de forma predeterminada.

-   Está en el paquete y están deshabilitadas, la casilla de verificación aparece desactivada de forma predeterminada.

-   Existe en el paquete, con uno o más habilitado y uno o más deshabilitado, la casilla se establece en indeterminada de forma predeterminada.

-   No existen en el paquete, la casilla está deshabilitada.

### <a href="" id="bkmk-pkgconvimprove"></a>Mejoras en el conversor de paquetes

Ahora puede usar el convertidor de paquetes para convertir paquetes de App-V 4,6 que contienen scripts y la información del registro y scripts de los archivos. OSD de origen se incluyen ahora en la salida del convertidor de paquetes.

Para obtener más información, como ejemplos, consulte [migrar a App-V 5,1 desde una versión anterior](migrating-to-app-v-51-from-a-previous-version.md).

### <a href="" id="bkmk-supmultscripts"></a>Compatibilidad con varios scripts en un solo desencadenador de eventos

App-V 5,1 admite el uso de varios scripts en un solo desencadenador de eventos para paquetes de App-V, incluidos los paquetes que está convirtiendo de App-V 4,6 a App-V 5,0 o posterior. Para habilitar el uso de varios scripts, App-V 5,1 usa una aplicación de iniciador de scripts, denominada ScriptRunner.exe, que se instala como parte de la instalación del cliente de App-V.

Para obtener más información, incluida una lista de desencadenadores de eventos y el contexto en el que se pueden ejecutar scripts, consulte la sección scripts en acerca de la [configuración dinámica de App-V 5,1](about-app-v-51-dynamic-configuration.md).

### <a href="" id="bkmk-hardcodepath"></a>La ruta de acceso codificada de la carpeta de instalación se redirige a la raíz del sistema de archivos virtual

Al convertir paquetes de App-V 4,6 a 5,1, el paquete App-V 5,1 puede acceder a la unidad codificada que tenía que usar al crear paquetes 4,6. La letra de unidad será la que seleccionó como unidad de instalación en la máquina de secuenciación de 4,6. (La letra de unidad predeterminada es Q:\\.)

Anteriormente, la carpeta raíz de 4,6 no fue reconocida y los paquetes de App-V 5,0 no podían acceder a ella. Los paquetes de App-V 5,1 pueden acceder a archivos codificados por su ruta de acceso completa o pueden enumerar archivos mediante programación en la raíz de instalación de App-V 4,6.

**Detalles técnicos:** El conversor de paquetes de App-V 5,1 guardará la carpeta raíz de instalación de App-V 4,6 y los nombres cortos de carpeta en el FilesystemMetadata.xml archivo del elemento filesystem. Cuando el cliente de App-V 5,1 crea el proceso virtual, se asignarán solicitudes de la raíz de instalación de App-V 4,6 a la raíz del sistema de archivos virtual.

## Cómo obtener tecnologías de MDOP


App-V es parte del paquete de optimización de escritorio de Microsoft (MDOP). MDOP es parte de Microsoft Software Assurance. Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049)






## Temas relacionados


[Notas de la versión de App-V 5.1](release-notes-for-app-v-51.md)









