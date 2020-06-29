---
title: Sincronizar Office 2013 con UE-V 2,0
description: Sincronizar Office 2013 con UE-V 2,0
author: dansimp
ms.assetid: c46feb6d-28a8-4799-888d-053531dc5842
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c9b079d3f21e6ced689fa2101f5321fa9b1406c8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826890"
---
# Sincronizar Office 2013 con UE-V 2,0


Virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0 admite la sincronización de la configuración de la aplicación Microsoft Office 2013 mediante una plantilla disponible en la galería de plantillas de UE-V. La combinación de UE-V 2 y App-V 5,0 SP2 de Office 2013 Professional Plus permite la misma experiencia en una instancia virtualizada de Office 2013 desde cualquier dispositivo habilitado para UE-V o escritorio virtualizado.

Para activar la compatibilidad de configuración de aplicaciones de UE-V de Office 2013, puede descargar plantillas oficiales de Office 2013 de UE-V de la galería de plantillas de [Microsoft User Experience Virtualization (UE-v) 2](https://go.microsoft.com/fwlink/p/?LinkId=246589). Este recurso proporciona plantillas de ubicación para la configuración de UE-V creadas por Microsoft, así como plantillas de ubicación de configuración desarrolladas por la comunidad.

## Soporte técnico de Microsoft Office en UE-V


UE-V 1,0 y UE-V 2 incluyen plantillas de ubicación de configuración para Microsoft Office 2010. Estas plantillas se distribuyen y registran como parte del proceso de instalación de UE-V Agent. Estas plantillas ayudan a sincronizar la experiencia de usuario de Office entre dispositivos. Las plantillas de UE-V para Office 2013 proporcionan una experiencia de configuración muy similar a las plantillas de Office 2010. La configuración de Microsoft Office 2013 desplazada por la experiencia de Office 365 no se incluye en esta configuración. Para obtener una lista de las configuraciones específicas de Office 365, vea [información general sobre la configuración de usuarios y roaming en office 2013](https://go.microsoft.com/fwlink/p/?LinkId=391220).

## Configuración sincronizada de Office 2013


En las tablas siguientes se incluyen los detalles de la compatibilidad de Office 2013 en UE-V:

### Plantillas de UE-V compatibles para Microsoft Office

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Plantillas de Office 2013 (UE-V 2,0, disponibles en la galería de UE-V):</th>
<th align="left">Plantillas de Office 2010 (UE-V 1,0 &amp; 1,0 SP1):</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>MicrosoftOffice2013Win32.xml</p>
<p>MicrosoftOffice2013Win64.xml</p>
<p>MicrosoftLync2013Win32.xml</p>
<p>MicrosoftLync2013Win64.xml</p></td>
<td align="left"><p>MicrosoftOffice2010Win32.xml</p>
<p>MicrosoftOffice2010Win64.xml</p>
<p>MicrosoftLync2010.xml</p>
<p></p></td>
</tr>
</tbody>
</table>

 

### Aplicaciones de Microsoft Office compatibles con las plantillas de UE-V

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Microsoft Access 2013</p>
<p>Microsoft Lync 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft Word 2013</p>
<p>Administrador de carga de Microsoft Office</p></td>
<td align="left"><p>Microsoft Access 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft SharePoint Designer 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft Word 2010</p>
<p></p></td>
</tr>
</tbody>
</table>

 

## Implementar las plantillas de Office 2013


Puede implementar la plantilla de ubicación configuración de UE-V con los métodos siguientes:

-   **Registrando la plantilla mediante PowerShell**. Si usa Windows PowerShell para administrar equipos, ejecute el siguiente comando de Windows PowerShell como administrador para registrar esta plantilla de ubicación de configuración:

    ``` syntax
    Register-UevTemplate -Path <Path_to_Template>
    ```

    Para obtener más información sobre cómo usar UE-V y Windows PowerShell, consulte [administrar plantillas de ubicación de configuración de UE-v 2. x con Windows PowerShell y WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).

-   **Registrando la plantilla a través de la ruta del catálogo de plantillas**. Si usa la ruta de acceso del catálogo de plantillas de configuración para administrar las plantillas de los equipos de los usuarios, copie la plantilla de Office 2013 en la carpeta definida en UE-V Agent. La próxima vez que se ejecute la tarea programada de actualización automática (ApplySettingsCatalog.exe) de plantillas, la plantilla de ubicación de configuración se registrará en el dispositivo. Para obtener más información, vea [implementar el catálogo de plantillas de configuración para UE-V 2](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue).

-   **Registrando la plantilla mediante Configuration Manager**. Si usa Configuration Manager para administrar las plantillas de almacenamiento de configuración de UE-V, vuelva a crear el archivo. CAB de línea base de plantilla, impórtelo en Configuration Manager y, a continuación, implemente la línea base en los clientes. Para obtener más información, consulte las instrucciones proporcionadas en la documentación del [paquete de configuración System Center 2012 para la virtualización de la experiencia del usuario de Microsoft 2](https://go.microsoft.com/fwlink/?LinkId=317263).






 

 





