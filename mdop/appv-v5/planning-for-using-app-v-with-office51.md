---
title: Planificación para el uso de App-V con Office
description: Planificación para el uso de App-V con Office
author: dansimp
ms.assetid: e7a19b43-1746-469f-bad6-8e75cf4b3f67
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/16/2017
ms.openlocfilehash: ae225db3c47faca5fba790fb9963bfd4dc2c66b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813414"
---
# Planificación para el uso de App-V con Office


Use la siguiente información para planear cómo implementar Office mediante Microsoft Application Virtualization (App-V) 5,1. Este artículo incluye:

-   [Compatibilidad de App-V para paquetes de idioma](#bkmk-lang-pack)

-   [Versiones compatibles de Microsoft Office](#bkmk-office-vers-supp-appv)

-   [Planificación para usar App-V con versiones coexistentes de Office](#bkmk-plan-coexisting)

-   [Cómo se integra Office con Windows al implementar use App-V para implementar Office](#bkmk-office-integration-win)

## <a href="" id="bkmk-lang-pack"></a>Compatibilidad de App-V para paquetes de idioma


Puede usar el secuenciador de aplicaciones-V 5,1 para crear paquetes de complementos para paquetes de idioma, paquetes de interfaz de idiomas, herramientas de corrección e idiomas de información en pantalla. Después, puede incluir los paquetes de complementos en un grupo de conexión, junto con el paquete de Office 2013 que cree con el kit de herramientas de implementación de Office. Las aplicaciones de Office y los paquetes de idioma del complemento interactúan sin problemas en el mismo grupo de conexión, como cualquier otro paquete que se agrupa en un grupo de conexión.

>**Nota:**  Microsoft Visio y Microsoft Project no proporcionan compatibilidad con el paquete de idioma tailandés.

 

## <a href="" id="bkmk-office-vers-supp-appv"></a>Versiones compatibles de Microsoft Office

Vea los [identificadores de producto de Microsoft Office compatibles con App-V](https://support.microsoft.com/help/2842297/product-ids-that-are-supported-by-the-office-deployment-tool-for-click) para obtener una lista de los productos de Office admitidos.
>**Nota:** &nbsp; &nbsp; Debe usar la herramienta de implementación de Office para crear paquetes de App-V para las aplicaciones de Microsoft 365 para empresas. No se admite la creación de paquetes para las versiones con licencia por volumen de Office Professional Plus o Office Standard. No puede usar el secuenciador de App-V.

 

## <a href="" id="bkmk-plan-coexisting"></a>Planificación para usar App-V con versiones coexistentes de Office


Puede instalar más de una versión de Microsoft Office en paralelo en el mismo equipo con "Microsoft Office coexistente". Puede implementar coexistencia de Office con combinaciones de todas las versiones principales de Office y con métodos de instalación, según sea el caso, con la versión de Office basada en Windows Installer (MSi), hacer clic y ejecutar y App-V 5,1. Sin embargo, Microsoft no recomienda el uso de coexistencia de Office.

El procedimiento recomendado de Microsoft es evitar la coexistencia de Office por completo para evitar problemas de compatibilidad. Sin embargo, al migrar a una versión más reciente de Office, surgen problemas que no se pueden resolver inmediatamente, por lo que puede implementar temporalmente la coexistencia para facilitar una migración más rápida a la última versión del producto. No se recomienda usar la coexistencia de Office a largo plazo, y su organización debe tener un plan para realizar una transición completa en el futuro inmediato.

### Antes de implementar la coexistencia de Office

Antes de implementar la coexistencia de Office, revise la siguiente documentación de Office. Elija el artículo correspondiente a la versión más reciente de Office para la que planea implementar la coexistencia.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión de Office</th>
<th align="left">Vínculo a orientación</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2784668" data-raw-source="[Information about how to use Office 2013 suites and programs (MSI deployment) on a computer that is running another version of Office](https://support.microsoft.com/kb/2784668)">Información sobre cómo usar los conjuntos y programas de Office 2013 (implementación de MSI) en un equipo que ejecuta otra versión de Office</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2121447" data-raw-source="[Information about how to use Office 2010 suites and programs on a computer that is running another version of Office](https://support.microsoft.com/kb/2121447)">Información sobre cómo usar los conjuntos y programas de Office 2010 en un equipo que ejecuta otra versión de Office</a></p></td>
</tr>
</tbody>
</table>

 

La documentación de Office proporciona instrucciones detalladas sobre la coexistencia de instalaciones basadas en Windows Installer (MSi) y de hacer clic y ejecutar de Office. Este tema de App-V de coexistencia complementa las instrucciones de Office con información más específica para las implementaciones de App-V.

### Escenarios de coexistencia de Office compatibles

En las tablas siguientes se resumen los escenarios de coexistencia admitidos. Se organizan de acuerdo con la versión y el método de implementación que está empezando y la versión y el método de implementación al que va a migrar. Asegúrese de probar completamente todas las soluciones de coexistencia antes de implementarlas en una audiencia de producción.

>**Nota:**  Microsoft no admite el uso de varias versiones de Office en entornos de Windows Server que tengan habilitado el servicio de rol host de sesión de escritorio remoto. Para ejecutar escenarios de coexistencia de Office, debe deshabilitar este servicio de rol.

 

### La coexistencia de Windows Integrations & Office

Los métodos de instalación de Office basados en Windows Installer y hacer clic y ejecutar se integran con determinados puntos del sistema operativo Windows subyacente. Cuando se usa la coexistencia, las integraciones comunes de sistemas operativos entre dos versiones de Office pueden entrar en conflicto, causando problemas de compatibilidad y experiencia del usuario. Con App-V, puede secuenciar determinadas versiones de Office para excluir integraciones y, por lo tanto, "aislarlas" del sistema operativo.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Modo en el que App-V puede hacer una secuencia de esta versión de Office</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Office 2007</p></td>
<td align="left"><p>Siempre no integrado. App-V no ofrece ninguna integración de sistema operativo con una versión virtualizada de Office 2007.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Office 2010</p></td>
<td align="left"><p>Modo integrado y no integrado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Office 2013</p></td>
<td align="left"><p>Siempre integrado. No se pueden deshabilitar las integraciones del sistema operativo Windows.</p></td>
</tr>
</tbody>
</table>

 

Microsoft recomienda implementar la coexistencia de Office con una única instancia de Office integrada. Por ejemplo, si usa App-V para implementar Office 2010 y Office 2013, debe secuenciar Office 2010 en modo no integrado. Para obtener más información sobre cómo secuenciar Office en modo no integrado (aislado), consulte [Cómo secuenciar Microsoft Office 2010 en Microsoft Application virtualization 5,0](https://support.microsoft.com/kb/2830069).

### Limitaciones conocidas de los escenarios de coexistencia de Office

En las siguientes secciones se describen algunos problemas que pueden surgir al usar App-V para implementar la coexistencia con Office.

### Limitaciones de escenarios de coexistencia de Office de App-V basados en Windows Installer o hacer clic y ejecutar.

Las siguientes limitaciones pueden producirse al instalar las siguientes versiones de Office en el mismo equipo:

-   Office 2010 con la versión basada en Windows Installer

-   Office 2013 mediante App-V

Después de publicar Office 2013 mediante App-V en paralelo con una versión anterior de 2010 Office basado en Windows Installer, también podría iniciarse el inicio de Windows Installer. Esto se debe a que la versión de Office 2010 basada en Windows Installer o de hacer clic y ejecutar se registra automáticamente en el equipo.

Para omitir la operación de registro automático para Word original 2010, siga estos pasos:

1.  Salga de Word 2010.

2.  Para iniciar el editor del registro, haga lo siguiente:

    -   En Windows 7: haga clic en **Inicio**, escriba **regedit** en el cuadro iniciar búsqueda y, a continuación, presione Entrar.

    -   En Windows 8,1 o Windows 10, escriba **regedit** y presione Entrar en la página de inicio y, a continuación, presione Entrar.

    Si se le pide una contraseña de administrador o una confirmación, escriba la contraseña o haga clic en **continuar**.

3.  Busque y seleccione la siguiente subclave del registro:

    ``` syntax
    HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\Word\Options
    ```

4.  En el menú **Editar** , haga clic en **nuevo**y, a continuación, haga clic en **valor DWORD**.

5.  Escriba **NoReReg**y, a continuación, presione Entrar.

6.  Haga clic con el botón derecho en **NoReReg** y luego en **modificar**.

7.  En el cuadro **valuedata** , escriba **1**y, a continuación, haga clic en **Aceptar**.

8.  En el menú Archivo, haga clic en **salir** para cerrar el editor del registro.

## <a href="" id="bkmk-office-integration-win"></a>Cómo se integra Office con Windows cuando usa App-V para implementar Office


Al implementar Office 2013 mediante App-V, Office está totalmente integrado con el sistema operativo, que proporciona a los usuarios finales las mismas características y funciones que Office tiene cuando se implementa sin App-V.

El paquete de Office 2013 App-V admite los siguientes puntos de integración con el sistema operativo Windows:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Punto de extensión</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Complemento para unirse a una reunión de Lync para Firefox y Chrome</p></td>
<td align="left"><p>El usuario puede unirse a reuniones de Lync desde Firefox y Chrome</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de impresión enviado a OneNote</p></td>
<td align="left"><p>El usuario puede imprimir en OneNote</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Notas vinculadas de OneNote</p></td>
<td align="left"><p>Notas vinculadas de OneNote</p></td>
</tr>
<tr class="even">
<td align="left"><p>Enviar a OneNote Internet Explorer (complemento)</p></td>
<td align="left"><p>El usuario puede enviar a OneNote desde IE</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Excepción de Firewall para Lync y Outlook</p></td>
<td align="left"><p>Excepción de Firewall para Lync y Outlook</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente MAPI</p></td>
<td align="left"><p>Los complementos y las aplicaciones nativas pueden interactuar con la aplicación virtual de Outlook a través de MAPI</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Complemento de SharePoint para Firefox</p></td>
<td align="left"><p>El usuario puede usar las características de SharePoint en Firefox</p></td>
</tr>
<tr class="even">
<td align="left"><p>Applet del panel de control de correo</p></td>
<td align="left"><p>El usuario obtiene el applet de panel de control de correo en Outlook</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ensamblados de interoperabilidad primarios</p></td>
<td align="left"><p>Compatibilidad con complementos administrados</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controlador de caché de documentos de Office</p></td>
<td align="left"><p>Permite la caché de documentos de las aplicaciones de Office</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Controlador de búsqueda de protocolo de Outlook</p></td>
<td align="left"><p>El usuario puede buscar en Outlook</p></td>
</tr>
<tr class="even">
<td align="left"><p>Controles Active X:</p></td>
<td align="left"><p>Para obtener más información sobre los controles ActiveX, consulte referencia de la <a href="https://go.microsoft.com/fwlink/p/?LinkId=331361" data-raw-source="[ActiveX Control API Reference](https://go.microsoft.com/fwlink/p/?LinkId=331361)"> API de controles ActiveX </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   Groove. SiteClient</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   PortalConnect.PersonalSite</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. openDocuments</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ExportDatabase</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. SpreadSheetLauncher</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. StssyncHander</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. DragUploadCtl</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. DragDownloadCtl</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   SharePoint. OpenXMLDocuments</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   SharePoint. ClipboardCtl</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   WinProj. Activator</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   Nombre. NameCtrl</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   STSUPld.CopyCtl</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   CommunicatorMeetingJoinAx.JoinManager</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="odd">
<td align="left"><p>   LISTNET. Listnet</p></td>
<td align="left"><p>Control ActiveX</p></td>
</tr>
<tr class="even">
<td align="left"><p>   Aplicación auxiliar de explorador OneDrive Pro</p></td>
<td align="left"><p>Control Active X)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Iconos superpuestos de OneDrive Pro</p></td>
<td align="left"><p>Superposiciones del icono del shell del explorador de Windows cuando los usuarios examinan carpetas carpetas de OneDrive Pro</p></td>
</tr>
<tr class="even">
<td align="left"><p>Extensiones de Shell de :</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Abreviados</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Search</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 






 

 





