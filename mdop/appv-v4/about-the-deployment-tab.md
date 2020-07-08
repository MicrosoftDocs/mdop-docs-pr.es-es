---
title: Acerca de la pestaña Implementación
description: Acerca de la pestaña Implementación
author: dansimp
ms.assetid: 12891798-baa4-45a5-b845-b9505ab95633
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 147e8b1057c789d97087461a585fa3f365089784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819961"
---
# Acerca de la pestaña Implementación


Use la pestaña **implementación** en la consola de Application Virtualization Sequencer para cambiar la información de una aplicación que va a secuenciar. Esta pestaña contiene los siguientes elementos.

## Dirección URL del servidor


Use los controles de **dirección URL del servidor** para especificar los valores de configuración del servidor de aplicaciones virtual.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Control</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Protocolo</strong></p></td>
<td align="left"><p>Le permite seleccionar el protocolo que transmitirá el paquete de aplicación secuenciado de un servidor de aplicaciones virtual a un cliente de escritorio de virtualización de aplicaciones. Están disponibles los siguientes protocolos:</p>
<ul>
<li><p><strong>RTSP </strong> : el valor predeterminado especifica que el protocolo de transmisión por secuencias en tiempo real controla el intercambio de aplicaciones habilitadas para la virtualización.</p></li>
<li><p><strong>RTSPs </strong> : especifica que el protocolo de transmisión por secuencias en tiempo real con seguridad de la capa de transporte controla el intercambio de un paquete de aplicación de secuencia.</p></li>
<li><p><strong>Archivo </strong> : especifica que la aplicación secuenciada se transmitirá desde un recurso compartido de archivos.</p></li>
<li><p><strong>HTTPS </strong> : especifica que el protocolo de transporte de hipertexto seguro controla el intercambio de un paquete.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Nombre</strong></p></td>
<td align="left"><p>Le permite seleccionar el servidor de aplicaciones virtual o el equilibrador de carga delante de un grupo de servidores de aplicaciones virtuales que transmitirán el paquete de software a un cliente de escritorio de virtualización de aplicaciones. Debe completar este elemento para crear un paquete de aplicación de secuencia, pero puede cambiar la variable de entorno% SFT_SOFTGRIDSERVER% predeterminada al nombre de host o la dirección IP reales de un servidor de aplicaciones virtual.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si decide no especificar una dirección IP o un nombre de host estático, en cada cliente de escritorio de virtualización de aplicaciones debe configurar una variable de entorno denominada SFT_SOFTGRIDSERVER. Su valor debe ser el nombre de host o la dirección IP del servidor de aplicaciones virtual o del equilibrador de carga que es este cliente&#39;es el origen de las aplicaciones. Debe convertir esta variable de entorno en una variable del sistema en lugar de una variable de usuario. Cualquier sesión del cliente de escritorio de virtualización de aplicaciones que se esté ejecutando en este equipo durante la asignación de esta variable debe cerrarse y, a continuación, abrirse para que la sesión reanudada tenga conocimiento de su nuevo origen de la aplicación.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Port</strong></p></td>
<td align="left"><p>Le permite especificar el puerto en el que escuchará el servidor de aplicaciones virtual o el equilibrador de carga para un cliente de escritorio de virtualización de aplicaciones&#39;s para el paquete. Esta información es necesaria para crear un paquete, pero puedes cambiarlo. El puerto predeterminado es 554.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Ruta de acceso</strong></p></td>
<td align="left"><p>Le permite especificar la ruta de acceso relativa en el servidor de aplicaciones virtual donde se almacena el paquete de software y desde el que se transmitirá. Esta información es necesaria para crear un paquete si el archivo SFT se almacena en un subdirectorio de contenido. de lo contrario, esta información no es necesaria.</p></td>
</tr>
</tbody>
</table>



## Sistemas operativos


Use los controles de **sistemas operativos** para especificar los requisitos del sistema operativo de la aplicación. Si un cliente de escritorio de virtualización de aplicaciones no puede admitir ninguno de los sistemas operativos seleccionados, la aplicación no se iniciará.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Controles</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Sistemas operativos disponibles</strong></p></td>
<td align="left"><p>Muestra una lista de los sistemas operativos que pueden admitir las aplicaciones del paquete.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Sistemas operativos seleccionados</strong></p></td>
<td align="left"><p>Muestra una lista de los sistemas operativos seleccionados que admiten las aplicaciones del paquete.</p></td>
</tr>
</tbody>
</table>



## Opciones de salida


Use los controles de **Opciones de resultados** para especificar las opciones de salida de la aplicación que se va a instalar.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Control</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Algoritmo de compresión</strong></p></td>
<td align="left"><p>Usar para seleccionar el método para comprimir el archivo SFT para la transmisión por secuencias a través de una red. Seleccione uno de los siguientes métodos de compresión:</p>
<ul>
<li><p><strong>Comprimido </strong> : especifica que el archivo SFT se comprimirá en <a href="https://go.microsoft.com/fwlink/?LinkId=111475" data-raw-source="[ZLIB](https://go.microsoft.com/fwlink/?LinkId=111475)"> formato zlib </a> .</p></li>
<li><p><strong>No comprimido </strong> : es el valor predeterminado; especifica que el archivo SFT no se comprimirá.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Exigir descriptores de seguridad</strong></p></td>
<td align="left"><p>Seleccione esta opción para aplicar los descriptores de seguridad de las aplicaciones en el paquete después de que se implemente en el cliente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Generar el paquete de Microsoft Windows Installer (MSI)</strong></p></td>
<td align="left"><p>Seleccione para instalar o implementar un paquete de aplicación de secuencia con Windows Installer. Si ha realizado algún cambio con el secuenciador, los cambios no se incluirán en el archivo de Windows Installer. El archivo de Windows Installer siempre se creará con el archivo. SFT guardado en el disco duro.</p></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Cómo cambiar las propiedades de implementación](how-to-change-deployment-properties.md)

[Consola de secuenciador](sequencer-console.md)









