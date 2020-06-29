---
title: Implementación de Microsoft Office 2010 mediante el uso de App-V
description: Implementación de Microsoft Office 2010 mediante el uso de App-V
author: dansimp
ms.assetid: ae0b0459-c0d6-4946-b62d-ff153f52d1fb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90454373e9a1c894eba8cbf1b8642656b986bc94
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814623"
---
# Implementación de Microsoft Office 2010 mediante el uso de App-V


Puede crear paquetes de Office 2010 para Microsoft Application Virtualization (App-V) 5,1 mediante uno de los siguientes métodos:

-   Application Virtualization (App-V) Sequencer

-   Acelerador de paquetes de Application Virtualization (App-V)

## Soporte técnico de App-V para Office 2010


En la siguiente tabla se muestran las versiones de App-V, los métodos de creación de paquetes de Office, las licencias admitidas y las implementaciones admitidas para Office 2010.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento admitido</th>
<th align="left">Nivel de compatibilidad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Versiones de App-V compatibles</p></td>
<td align="left"><ul>
<li><p>4,6</p></li>
<li><p>5.0</p></li>
<li><p>5,1</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Creación de paquetes</p></td>
<td align="left"><ul>
<li><p>128</p></li>
<li><p>Acelerador de paquetes</p></li>
<li><p>Office Deployment Kit</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Licencias admitidas</p></td>
<td align="left"><p>Licencias por volumen</p></td>
</tr>
<tr class="even">
<td align="left"><p>Implementaciones admitidas</p></td>
<td align="left"><ul>
<li><p>Escritorio</p></li>
<li><p>VDI personal</p></li>
<li><p>RDS</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Crear Office 2010 App-V 5,1 con el secuenciador


La secuencia de Office 2010 es uno de los métodos principales para crear un paquete de Office 2010 en App-V 5,1. Microsoft proporciona una receta detallada a través de un artículo de Knowledge base. Para crear un paquete de Office 2010 en App-V 5,1, consulte el vínculo siguiente para obtener instrucciones detalladas:

[Cómo secuenciar Microsoft Office 2010 en Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

## Crear paquetes de aplicación de Office 2010: V 5,1 con aceleradores de paquetes


Los paquetes de Office 2010 App-V 5,1 se pueden crear a través de aceleradores de paquetes. Microsoft ha proporcionado aceleradores de paquetes para crear Office 2010 en Windows 10, Windows 8 y Windows 7. Para crear paquetes de Office 2010 en App-V con aceleradores de paquetes, consulte las páginas siguientes para obtener acceso al Acelerador de paquetes correspondiente:

-   [Acelerador de paquetes de App-V 5,0 para Office Professional Plus 2010 (Windows 8)](https://go.microsoft.com/fwlink/p/?LinkId=330677)

-   [Acelerador de paquetes de App-V 5,0 para Office Professional Plus 2010: Windows 7](https://go.microsoft.com/fwlink/p/?LinkId=330678)

Para obtener instrucciones detalladas sobre cómo crear paquetes de aplicaciones virtuales con aceleradores de paquetes de App-V, vea [Cómo crear un paquete de aplicaciones virtual con un acelerador de paquetes de App-v](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator51.md).

## Implementación del paquete de Microsoft Office para App-V 5,1


Puede implementar paquetes de Office 2010 con cualquiera de los siguientes métodos de implementación de App-V:

-   System Center Configuration Manager

-   Servidor de App-V

-   Independiente a través de los comandos de PowerShell

## Personalización y administración de paquetes de Office App-V


Los paquetes de Office 2010 se pueden administrar como cualquier otro paquete de App-V 5,1 mediante mecanismos de administración de paquetes conocidos. No se necesitan instrucciones especiales, por ejemplo, para agregar, publicar, anular la publicación o quitar paquetes de Office.

## Integración de Microsoft Office con Windows


En la tabla siguiente se proporciona una lista completa de los puntos de integración admitidos para Office 2010.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Punto de extensión</th>
<th align="left">Descripción</th>
<th align="left">Office 2010</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Complemento para unirse a una reunión de Lync para Firefox y Chrome</p></td>
<td align="left"><p>El usuario puede unirse a reuniones de Lync desde Firefox y Chrome</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de impresión enviado a OneNote</p></td>
<td align="left"><p>El usuario puede imprimir en OneNote</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Notas vinculadas de OneNote</p></td>
<td align="left"><p>Notas vinculadas de OneNote</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Enviar a OneNote Internet Explorer (complemento)</p></td>
<td align="left"><p>El usuario puede enviar a OneNote desde IE</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Excepción de Firewall para Lync y Outlook</p></td>
<td align="left"><p>Excepción de Firewall para Lync y Outlook</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente MAPI</p></td>
<td align="left"><p>Los complementos y las aplicaciones nativas pueden interactuar con la aplicación virtual de Outlook a través de MAPI</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Complemento de SharePoint para Firefox</p></td>
<td align="left"><p>El usuario puede usar las características de SharePoint en Firefox</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Applet del panel de control de correo</p></td>
<td align="left"><p>El usuario obtiene el applet de panel de control de correo en Outlook</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ensamblados de interoperabilidad primarios</p></td>
<td align="left"><p>Compatibilidad con complementos administrados</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de caché de documentos de Office</p></td>
<td align="left"><p>Permite la caché de documentos de las aplicaciones de Office</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Controlador de búsqueda de protocolo de Outlook</p></td>
<td align="left"><p>El usuario puede buscar en Outlook</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controles Active X:</p></td>
<td align="left"><p>Para obtener más información sobre los controles ActiveX, consulte referencia de la <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API de controles ActiveX </a> .</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Groove. SiteClient</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect.PersonalSite</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. openDocuments</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Sharpoint.OpenXMLDocuments</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ClipboardCtl</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   WinProj. Activator</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   Nombre. NameCtrl</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   STSUPld.CopyCtl</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx.JoinManager</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Control ActiveX</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>   Aplicación auxiliar de explorador OneDrive Pro</p></td>
<td align="left"><p>Control Active X)</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Iconos superpuestos de OneDrive Pro</p></td>
<td align="left"><p>Superposiciones del icono del shell del explorador de Windows cuando los usuarios examinan carpetas carpetas de OneDrive Pro</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## Recursos adicionales


**Recursos adicionales de los paquetes de Office 2013 App-V**

[Escenarios admitidos para implementar Microsoft Office como un paquete de App-V con secuencia](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**Paquetes de Office 2010 App-V**

[Kit de secuenciación 2010 de Microsoft Office para Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[Problemas conocidos al crear o usar un paquete de Office 2010 de App-V 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[Cómo secuenciar Microsoft Office 2010 en Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**Grupos de conexión**

[Implementación de grupos de conexión en Microsoft App-V V5](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[Administración de grupos de conexión](managing-connection-groups51.md)

**Configuración dinámica**

[Acerca de la configuración dinámica de App-V 5.1](about-app-v-51-dynamic-configuration.md)






 

 





