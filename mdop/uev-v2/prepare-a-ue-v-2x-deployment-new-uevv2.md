---
title: Preparar una implementación de UE-V 2. x
description: Preparar una implementación de UE-V 2. x
author: dansimp
ms.assetid: c429fd06-13ff-48c5-b9c9-fa1ec01ab800
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: e6b2de407990536e1a08532632dcea19ea0d0ee9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826421"
---
# Preparar una implementación de UE-V 2. x


Hay que realizar tareas de planeación y preparación antes de implementar la virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0 o 2,1 como solución para sincronizar la configuración entre dispositivos a los que los usuarios tienen acceso en su empresa. Este tema le ayuda a determinar qué tipo de implementación realizará y qué preparación puede hacer previamente para que su implementación se realice correctamente.

En primer lugar, echemos un vistazo a las tareas que debe realizar para implementar UE-V:

-   Planear la implementación de UE-V

    Antes de implementar cualquier cosa, un buen primer paso es realizar un poco de planificación para que pueda determinar qué características de UE-V va a implementar. Por lo tanto, si sale de esta página, asegúrese de volver y leer la información de planeación que se muestra a continuación.

-   [Implementar funciones necesarias para UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

    Todas las implementaciones de UE-V requieren estas actividades:

    -   [Definir una ubicación de almacenamiento de configuración](https://technet.microsoft.com/library/dn458891.aspx#ssl)

    -   [Decidir cómo implementar el agente de UE-V y cómo administrar las configuraciones de UE-V](https://technet.microsoft.com/library/dn458891.aspx#config)

    -   [Instalar el agente UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) en todos los equipos de los usuarios que necesiten una configuración sincronizada

-   De manera opcional, puede [implementar UE-V 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

    La planeación le ayudará a averiguar si quiere que UE-V admita la sincronización de la configuración de aplicaciones personalizadas (de terceros o de línea de negocio), que requiere estas características de UE-V:

    -   [Instalar el generador de UEV](https://technet.microsoft.com/library/dn458942.aspx#uevgen) para que pueda crear, editar y validar las plantillas de ubicación de configuración personalizada necesarias para sincronizar la configuración de la aplicación personalizada

    -   [Crear plantillas de ubicación de configuración personalizadas](https://technet.microsoft.com/library/dn458942.aspx#createcustomtemplates) con el generador de UE-V

    -   [Implementar un catálogo de plantillas de configuración de UE-V](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue) que use para almacenar las plantillas de ubicación de configuración personalizadas

Este diagrama de flujo de trabajo proporciona un conocimiento de alto nivel de una implementación de UE-V y las decisiones que determinan cómo implementar UE-V en su empresa.

![deploymentworkflow](images/deploymentworkflow.png)

**Planeamiento de una implementación de UE-V:** En primer lugar, desea hacer un poco de planeación para poder determinar qué componentes de UE-V va a implementar. Planear una implementación de UE-V conlleva las siguientes características:

-   [Decidir si sincronizar la configuración de aplicaciones personalizadas](#deciding)

    Esto determina si instalará el generador de UE-V durante la implementación, lo que le permite crear plantillas de ubicación de configuración personalizadas. Incluye lo siguiente:

    Revise la [configuración que se sincroniza automáticamente en una implementación de UE-V](#autosyncsettings).

    [Determine si necesita la configuración sincronizada para otras aplicaciones](#determinesettingssync).

-   Revise [otras consideraciones para implementar UE-V](#considerations), como la alta disponibilidad y la planificación de capacidad.

-   [Confirmar los requisitos previos y las configuraciones admitidas para UE-V](#prereqs)

## <a href="" id="deciding"></a>Decidir si sincronizar la configuración de aplicaciones personalizadas


En una implementación de UE-V, muchas opciones de configuración se sincronizan automáticamente. Pero también puede personalizar UE-V para sincronizar la configuración de otras aplicaciones, como la línea de negocio y las aplicaciones de terceros.

Decidir si desea que UE-V sincronice la configuración de aplicaciones personalizadas es probablemente la parte más importante de la planificación de la implementación de UE-V. Los temas de esta sección le ayudarán a tomar esta decisión.

### <a href="" id="autosyncsettings"></a>Configuración que se sincroniza automáticamente en una implementación de UE-V

Esta sección proporciona información sobre la configuración que se sincronizan de forma predeterminada en la versión de UE-V, incluyendo lo siguiente:

Aplicaciones de escritorio cuya configuración está sincronizada de forma predeterminada

Configuración del escritorio de Windows que se sincronizan de forma predeterminada

Una declaración de compatibilidad con la sincronización de la configuración de aplicaciones de Windows

Vea [plantillas de configuración de virtualización de experiencia de usuario (UE-V) para que Microsoft Office](https://www.microsoft.com/download/details.aspx?id=46367) Descargue una lista completa de las configuraciones específicas de microsoft office 2013, microsoft Office 2010 y microsoft office 2007 que se sincronizan con UE-V.

### Aplicaciones de escritorio sincronizadas de forma predeterminada en UE-V 2,1 y UE-V 2,1 SP1

Al instalar el agente UE-V 2,1 o 2,1 SP1, se registra un grupo predeterminado de plantillas de ubicación de configuración que capturan valores de configuración para estas aplicaciones comunes de Microsoft.

**Sugerencia**  
**Sincronización de configuración de Microsoft Office 2007** : en UE-V 2,1 y 2,1 SP1, ya no se incluye una plantilla de ubicación de configuración de forma predeterminada para las aplicaciones de Office 2007. Sin embargo, todavía puede usar las plantillas de Office 2007 desde UE-V 2,0 o versiones anteriores y puede obtener las plantillas de la [Galería de plantillas de UE-v](https://go.microsoft.com/fwlink/p/?LinkID=246589).



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Categoría de aplicación</strong></th>
<th align="left"><strong>Descripción</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aplicaciones de Microsoft Office 2010</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Descargar una lista de todas las opciones de configuración sincronizadas </a> )</p></td>
<td align="left"><p>Microsoft Word 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft Access 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aplicaciones de Microsoft Office 2013</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Descargar una lista de todas las opciones de configuración sincronizadas </a> )</p></td>
<td align="left"><p>Microsoft Word 2013</p>
<p>Microsoft Excel 2013</p>
<p>Microsoft Outlook 2013</p>
<p>Microsoft Access 2013</p>
<p>Microsoft Project 2013</p>
<p>Microsoft PowerPoint 2013</p>
<p>Microsoft Publisher 2013</p>
<p>Microsoft Visio 2013</p>
<p>Microsoft InfoPath 2013</p>
<p>Microsoft Lync 2013</p>
<p>Microsoft OneNote 2013</p>
<p>Microsoft SharePoint Designer 2013</p>
<p>Centro de carga de Microsoft Office 2013</p>
<p>Microsoft OneDrive para la empresa 2013</p>
<p>Las plantillas de ubicación de configuración de UE-V 2,1 y 2,1 SP1 de Microsoft Office 2013 incluyen compatibilidad mejorada con la firma de Outlook. Hemos agregado la sincronización de la configuración de firma predeterminada para mensajes de correo electrónico nuevos, de respuesta y reenviados.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Debe crearse un perfil de Outlook para cualquier dispositivo en el que un usuario desee sincronizar su firma de Outlook. Si el perfil aún no se ha creado, el usuario puede crear uno y, a continuación, reiniciar Outlook en ese dispositivo para habilitar la sincronización de firmas.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Opciones del explorador: Internet Explorer 8, Internet Explorer 9, Internet Explorer 10 e Internet Explorer 11</p></td>
<td align="left"><p>Favoritos, Página principal, pestañas y barras de herramientas.</p>
<div class="alert">
<strong>Nota</strong><br/><p>UE-V no tiene una configuración de itinerancia para las cookies de Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Accesorios de Windows</p></td>
<td align="left"><p>Calculadora de Microsoft, Bloc de notas, WordPad.</p></td>
</tr>
</tbody>
</table>



**Nota**  
UE-V 2,1 SP1 no sincroniza la configuración entre la calculadora de Microsoft en Windows 10 y la calculadora de Microsoft en sistemas operativos anteriores.



### Aplicaciones de escritorio sincronizadas de forma predeterminada en UE-V 2,0

Al instalar el agente de UE-V 2,0, se registra un grupo predeterminado de plantillas de ubicación de configuración que capturan valores de configuración para estas aplicaciones comunes de Microsoft.

**Sugerencia**  
**Sincronización de configuración de Microsoft Office 2013** : en UE-V 2,0, una plantilla de ubicación de configuración no se incluye de forma predeterminada para las aplicaciones de Office 2013, pero se puede descargar desde la [Galería de plantillas de UE-V](https://go.microsoft.com/fwlink/p/?LinkID=246589). [Sincronizar Office 2013 con UE-V 2,0](synchronizing-office-2013-with-ue-v-20-both-uevv2.md) proporciona detalles sobre las plantillas compatibles que sincronizan la configuración de Office 2013.



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Categoría de aplicación</strong></th>
<th align="left"><strong>Descripción</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aplicaciones de Microsoft Office 2007</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Descargar una lista de todas las opciones de configuración sincronizadas </a> )</p></td>
<td align="left"><p>Microsoft Access 2007</p>
<p>Microsoft Communicator 2007</p>
<p>Microsoft Excel 2007</p>
<p>Microsoft InfoPath 2007</p>
<p>Microsoft OneNote 2007</p>
<p>Microsoft Outlook 2007</p>
<p>Microsoft PowerPoint 2007</p>
<p>Microsoft Project 2007</p>
<p>Microsoft Publisher 2007</p>
<p>Microsoft SharePoint Designer 2007</p>
<p>Microsoft Visio 2007</p>
<p>Microsoft Word 2007</p></td>
</tr>
<tr class="even">
<td align="left"><p>Aplicaciones de Microsoft Office 2010</p>
<p>( <a href="https://www.microsoft.com/download/details.aspx?id=46367" data-raw-source="[Download a list of all settings synced](https://www.microsoft.com/download/details.aspx?id=46367)"> Descargar una lista de todas las opciones de configuración sincronizadas </a> )</p></td>
<td align="left"><p>Microsoft Word 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft Access 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010</p>
<p>Microsoft SharePoint Designer 2010</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Opciones del explorador: Internet Explorer 8, Internet Explorer 9 e Internet Explorer 10</p></td>
<td align="left"><p>Favoritos, Página principal, pestañas y barras de herramientas.</p>
<div class="alert">
<strong>Nota</strong><br/><p>UE-V no tiene una configuración de itinerancia para las cookies de Internet Explorer.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Accesorios de Windows</p></td>
<td align="left"><p>Calculadora de Microsoft, Bloc de notas, WordPad.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="autosyncsettings2"></a>Configuración de Windows sincronizada de forma predeterminada

UE-V incluye plantillas de ubicación de configuración que capturan valores de configuración para esta configuración de Windows.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuración de Windows</th>
<th align="left">Descripción</th>
<th align="left">Aplicar en</th>
<th align="left">Exportar el</th>
<th align="left">Estado predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Fondo de escritorio</p></td>
<td align="left"><p>El fondo o el papel tapiz de escritorio actualmente están activos.</p></td>
<td align="left"><p>Inicio de sesión, desbloquear, conexión remota, eventos de tarea programada.</p></td>
<td align="left"><p>Cierre de sesión, bloqueo, desconexión remota, usuario haciendo clic <strong> en sincronizar ahora </strong> en el centro de configuración de la empresa o intervalo de tarea programada</p></td>
<td align="left"><p>Habilitado</p></td>
</tr>
<tr class="even">
<td align="left"><p>Accesibilidad</p></td>
<td align="left"><p>Accesibilidad y configuración de entrada, ampliador de Microsoft, narrador y teclado en pantalla.</p></td>
<td align="left"><p>Solo inicio de sesión.</p></td>
<td align="left"><p>Cerrar sesión, usuario haciendo clic <strong> en sincronizar ahora </strong> en el centro de configuración de la empresa o intervalo de tarea programada</p></td>
<td align="left"><p>Habilitado</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuración del escritorio</p></td>
<td align="left"><p>Configuración del menú Inicio y de la barra de tareas, opciones de carpeta, iconos predeterminados del escritorio, relojes adicionales y configuración de región e idioma.</p></td>
<td align="left"><p>Solo inicio de sesión.</p></td>
<td align="left"><p>Cerrar sesión, usuario haciendo clic <strong> en sincronizar ahora </strong> en el centro de configuración de la compañía o tarea programada</p></td>
<td align="left"><p>Habilitado</p></td>
</tr>
</tbody>
</table>



**Nota**  
A partir de Windows 8, UE-V no realiza una configuración de itinerancia relacionada con la pantalla de inicio, como los elementos y las ubicaciones. Además, UE-V no admite la sincronización de elementos de la barra de tareas anclados o de los accesos directos de archivos de Windows.



**Importante**  
UE-V 2,1 SP1 rela configuración de la barra de tareas entre dispositivos con Windows 10. Sin embargo, UE-V no sincroniza la configuración de la barra de tareas entre dispositivos con Windows 10 y dispositivos que ejecutan sistemas operativos anteriores.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Grupo de configuración</th>
<th align="left">Categoría</th>
<th align="left">Obtener</th>
<th align="left">Aplicar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Configuración de la aplicación</strong></p></td>
<td align="left"><p>Aplicaciones de Windows  </p></td>
<td align="left"><p>Cerrar aplicación</p>
<p>Evento de cambio de configuración de aplicación de Windows</p></td>
<td align="left"><p>Iniciar el monitor de aplicaciones de UE-V en el inicio</p>
<p>Abrir aplicación</p>
<p>Evento de cambio de configuración de aplicación de Windows</p>
<p>Llegada de un paquete de configuración</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Aplicaciones de escritorio</p></td>
<td align="left"><p>La aplicación se cierra</p></td>
<td align="left"><p>La aplicación se abre y se cierra</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Configuración del escritorio</strong></p></td>
<td align="left"><p>Fondo de escritorio</p></td>
<td align="left"><p>Bloqueo o cierre de sesión</p></td>
<td align="left"><p>Inicio de sesión, desbloqueo, conexión remota, notificación de llegada de paquetes nuevos, el usuario hace clic en <strong> sincronizar ahora </strong> en el centro de configuración de la compañía o ejecuta una tarea programada.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Facilidad de acceso (común: accesibilidad, narrador, lupa, teclado en pantalla)</p></td>
<td align="left"><p>Bloqueo o cierre de sesión</p></td>
<td align="left"><p>Sesiones</p></td>
</tr>
<tr class="odd">
<td align="left"><p></p></td>
<td align="left"><p>Facilidad de acceso (Shell: audio, accesibilidad, teclado, mouse)</p></td>
<td align="left"><p>Bloqueo o cierre de sesión</p></td>
<td align="left"><p>Inicio de sesión, desbloqueo, conexión remota, notificación de llegada de paquetes nuevos, el usuario hace clic en <strong> sincronizar ahora </strong> en el centro de configuración de la compañía o ejecuta una tarea programada</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>Configuración del escritorio</p></td>
<td align="left"><p>Bloqueo o cierre de sesión</p></td>
<td align="left"><p>Sesiones</p></td>
</tr>
</tbody>
</table>



### UE-V-compatibilidad con aplicaciones para Windows

En el caso de las aplicaciones de Windows, el desarrollador de la aplicación especifica la configuración que se sincroniza. Puede especificar qué aplicaciones de Windows están habilitadas para la sincronización de configuración.

Para mostrar una lista de las aplicaciones de Windows que pueden sincronizar la configuración de un equipo con el nombre de familia del paquete, el estado habilitado y el origen habilitado, en el símbolo del sistema de Windows PowerShell, escriba: `Get-UevAppxPackage`

**Nota**  
A partir de Windows 8, UE-V no sincroniza la configuración de la aplicación de Windows si el usuario del dominio vincula sus credenciales de inicio de sesión con su cuenta de Microsoft. Esta vinculación sincroniza la configuración con Microsoft OneDrive, por lo que es UE-V, que deshabilita la sincronización de la configuración de la aplicación de Windows.



### UE-V-compatibilidad con impresoras de itinerancia

UE-V 2,1 SP1 permite que las impresoras de red sean móviles entre dispositivos para que el usuario tenga acceso a sus impresoras de red al iniciar sesión en cualquier dispositivo de la red. Esto incluye la itinerancia de la impresora que establecieron como predeterminada.

La itinerancia de la impresora en UE-V requiere uno de estos escenarios:

-   El servidor de impresión puede descargar el controlador requerido cuando se desplaza a un nuevo dispositivo.

-   El controlador para la impresora de red de itinerancia está preinstalado en cualquier dispositivo que necesite acceder a esa impresora de red.

-   El controlador de impresora se puede obtener en Windows Update.

**Nota**  
La característica de itinerancia de la impresora UE-V **no tiene preferencias** , como la impresión a doble cara.



### <a href="" id="determinesettingssync"></a>Determinar si necesita la configuración sincronizada para otras aplicaciones

Una vez que haya revisado la configuración que se sincroniza automáticamente en una implementación de UE-V, tendrá que decidir si sincronizará la configuración de otras aplicaciones, ya que esto determina cómo implementar UE-V en toda la empresa.

Como administrador, cuando considere qué aplicaciones de escritorio incluir en su solución de UE-V, considere qué opciones puede personalizar un usuario y cómo y dónde se almacenará la aplicación. No todas las aplicaciones de escritorio tienen opciones de configuración que se pueden personalizar o que los usuarios personalizan rutinariamente. Además, no todas las configuraciones de aplicaciones de escritorio se pueden sincronizar de forma segura en varios equipos o entornos.

En general, puede sincronizar la configuración que cumpla los siguientes criterios:

-   Configuración que se almacena en ubicaciones accesibles para el usuario. Por ejemplo, no sincronice la configuración almacenada en system32 o fuera de la sección HKEY \ _CURRENT \ _USER (HKCU) del registro.

-   Configuración que no es específica del equipo en particular. Por ejemplo, excluya la configuración de red o de hardware.

-   Configuración que se puede sincronizar entre equipos sin riesgo de datos dañados. Por ejemplo, no use la configuración almacenada en un archivo de base de datos.

### <a href="" id="checklistsettingssync"></a>Lista de comprobación para evaluar aplicaciones personalizadas

Si ha decidido que necesita la configuración sincronizada para otras aplicaciones, puede usar esta lista de comprobación para averiguar qué aplicaciones incluirá.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿Esta aplicación contiene opciones de configuración que el usuario puede personalizar?</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿Es importante para el usuario que esta configuración esté sincronizada?</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿Esta configuración de usuario ya está administrada por una solución de directiva de configuración o administración de aplicaciones? UE-V aplica la configuración de la aplicación en el inicio de la aplicación y en la configuración de Windows en los eventos de inicio de sesión, desbloquear o conexión remota. Si usa UE-V con otras soluciones de uso compartido de configuración, es posible que los usuarios experimenten una incoherencia en la configuración sincronizada.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿Son las configuraciones específicas de la aplicación para el equipo? Las preferencias y personalizaciones de la aplicación que están relacionadas con el hardware o con la configuración específica de un equipo no se sincronizan de forma coherente en todas las sesiones y pueden provocar una mala experiencia de la aplicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿La configuración del almacén de aplicaciones en el directorio archivos de programa o en el directorio de archivos que se encuentra en el <strong> </strong> &lt; Directorio de &gt; </strong> &lt; LocalLow seguro &gt; </strong> de los usuarios [nombre de usuario] Los datos de la aplicación que se almacenan en cualquiera de estas ubicaciones generalmente no se sincronizan con el usuario, porque estos datos son específicos del equipo o porque los datos son demasiado grandes para sincronizarlos.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿La aplicación almacena la configuración en un archivo que contiene otros datos de la aplicación que no deberían sincronizarse? UE-V sincroniza los archivos como una sola unidad. Si los valores se almacenan en archivos que incluyen datos de aplicaciones distintos de la configuración, la sincronización de estos datos adicionales puede provocar una mala experiencia de la aplicación.</p></td>
</tr>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>¿Cuál es el tamaño de los archivos que contienen la configuración? El rendimiento de la sincronización de configuración puede verse afectado por archivos grandes. La inclusión de archivos grandes puede afectar al rendimiento de la sincronización de configuración.</p></td>
</tr>
</tbody>
</table>



## <a href="" id="considerations"></a>Otras consideraciones al preparar una implementación de UE-V


También debe tener en cuenta lo siguiente cuando se está preparando para implementar UE-V:

-   [Administración de la sincronización de credenciales](#creds)

-   [Sincronización de configuración de aplicaciones de Windows](#appxsettings)

-   [Plantillas de ubicación de configuración personalizada de UE-V](#custom)

-   [Configuraciones de configuración de usuario no intencionadas](#prevent)

-   [Rendimiento y capacidad](#capacity)

-   [Alta disponibilidad](#high)

-   [Sincronización del reloj del equipo](#clocksync)

### <a href="" id="creds"></a>Administración de la sincronización de credenciales en UE-V 2,1 y UE-V 2,1 SP1

Muchas aplicaciones empresariales, entre las que se incluyen Microsoft Outlook y Lync, solicitan a los usuarios sus credenciales de dominio en el inicio de sesión. Los usuarios tienen la opción de guardar sus credenciales en disco para evitar tener que escribirlas cada vez que abran estas aplicaciones. Habilitar la sincronización de credenciales de itinerancia permite a los usuarios guardar sus credenciales en un equipo y evitar volver a escribirlas en todos los equipos que usan en su entorno. Los usuarios pueden sincronizar algunas credenciales de dominio con UE-V 2,1 y 2,1 SP1.

**Importante**  
La sincronización de credenciales está deshabilitada de forma predeterminada. Debe habilitar de forma explícita la sincronización de credenciales durante la implementación para implementar esta característica.



UE-V 2,1 y 2,1 SP1 pueden sincronizar las credenciales de la empresa, pero no las credenciales destinadas para su uso en el equipo local.

Las credenciales son configuraciones sincrónicas, lo que significa que se aplican a su perfil la primera vez que inicia sesión en el equipo después de sincronizar UE-V.

La sincronización de credenciales se administra mediante su propia plantilla de ubicación de configuración, que está deshabilitada de forma predeterminada. Puede habilitar o deshabilitar esta plantilla mediante los mismos métodos que se usan para otras plantillas. El identificador de la plantilla para esta característica es RoamingCredentialSettings.

**Importante**  
Si está usando las credenciales móviles de Active Directory en su entorno, le recomendamos que no habilite la plantilla de itinerancia de credenciales UE-V.



Use uno de estos métodos para habilitar la sincronización de credenciales:

-   Centro de configuración de empresa

-   PowerShell

-   Directiva de grupo

**Nota**  
Las credenciales se cifran durante la sincronización.



[Centro de configuración de la compañía](https://technet.microsoft.com/library/dn458903.aspx)**:** Active la casilla configuración de credenciales de itinerancia en configuración de Windows para habilitar la sincronización de credenciales. Desactive la casilla para deshabilitarlo. Esta casilla solo aparece en el centro de configuración de la empresa si su cuenta no está configurada para sincronizar la configuración con una cuenta de Microsoft.

[PowerShell](https://technet.microsoft.com/library/dn458937.aspx)**:** este cmdlet de PowerShell habilita la sincronización de credenciales:

``` syntax
Enable-UevTemplate RoamingCredentialSettings
```

Este cmdlet de PowerShell deshabilita la sincronización de credenciales:

``` syntax
Disable-UevTemplate RoamingCredentialSettings
```

[Directiva de grupo](https://technet.microsoft.com/library/dn458893.aspx)**:** debe [implementar la última plantilla de MDOP de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393944) para habilitar la sincronización de credenciales mediante la Directiva de grupo. La sincronización de credenciales se administra con la configuración de Windows. Para administrar esta característica con la Directiva de grupo, habilite la Directiva sincronizar la configuración de Windows.

1.  Abra el editor de directivas de grupo y vaya a **configuración de usuario: Plantillas administrativas – componentes de Windows – virtualización**de la experiencia del usuario de Microsoft.

2.  Haga doble clic en **sincronizar configuración de Windows**.

3.  Si esta directiva está habilitada, puede habilitar la sincronización de credenciales activando la casilla **credenciales de itinerancia** o desactivando la sincronización de credenciales.

4.  Haga clic en **Aceptar**.

### Ubicaciones de credenciales sincronizadas por UE-V

Los archivos de credenciales guardados por las aplicaciones en las siguientes ubicaciones están sincronizadas:

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Credentials\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Crypto\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\Protect\\

-   %UserProfile%\\AppData\\Roaming\\Microsoft\\SystemCertificates\\

Las credenciales guardadas en otras ubicaciones no están sincronizadas por UE-V.

### <a href="" id="appxsettings"></a>Sincronización de configuración de aplicaciones de Windows

UE-V administra la sincronización de la configuración de aplicaciones de Windows de tres maneras:

-   **Sincronizar aplicaciones de Windows:** Permitir o denegar cualquier sincronización de aplicaciones de Windows

-   **Lista de aplicaciones de Windows:** Sincronizar una lista de aplicaciones de Windows

-   **Comportamiento de sincronización predeterminado no listado:** Determine el comportamiento de sincronización de las aplicaciones de Windows que no se encuentran en la lista de aplicaciones de Windows.

Para obtener más información, consulta la [lista de aplicaciones de Windows](https://technet.microsoft.com/library/dn458925.aspx#win8applist).

### <a href="" id="custom"></a>Plantillas de ubicación de configuración personalizada de UE-V

Si implementa UE-V para sincronizar la configuración de aplicaciones personalizadas, usará el generador de UE-V para crear plantillas de ubicación de configuración personalizadas para esas aplicaciones de escritorio. Después de crear y probar una plantilla de ubicación de configuración personalizada en un entorno de prueba, puede implementar las plantillas de ubicación de configuración en los equipos de la empresa.

Las plantillas de ubicación de configuración personalizada deben implementarse con una infraestructura de implementación existente, como un método de distribución de software de empresa (ESD), como System Center Configuration Manager, con preferencias, o al configurar un catálogo de plantillas de configuración de UE-V. Las plantillas implementadas con el administrador de configuración o la Directiva de grupo se deben registrar con UE-V WMI o Windows PowerShell.

Para obtener más información sobre las plantillas de ubicación de configuración personalizada, consulte [implementar UE-V 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md). Para obtener más información sobre cómo usar UE-V con Configuration Manager, consulte [Configuring UE-v 2. x with System Center Configuration manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).

### <a href="" id="prevent"></a>Evitar la configuración de un usuario no intencionado

UE-V descarga información nueva de configuración de usuario desde una ubicación de almacenamiento de configuración y aplica la configuración al equipo local en estas instancias:

-   Cada vez que se inicia una aplicación que tiene una plantilla registrada de UE-V.

-   Cuando un usuario inicia sesión en un equipo.

-   Cuando un usuario desbloquea un equipo.

-   Cuando se establece una conexión con un equipo de escritorio remoto que tiene UE-V instalado.

-   Cuando se ejecuta la tarea programada de controlador de sincronización.

Si UE-V está instalado en el equipo A y en el equipo B, y la configuración que desea para la aplicación se encuentra en el equipo A, entonces el equipo A debe abrirse y cerrar la aplicación en primer lugar. Si la aplicación se abre y cierra en el equipo B, la configuración de la aplicación en el equipo a se establece en la configuración de la aplicación en el equipo B. la configuración se sincroniza entre equipos en función de la aplicación. Con el tiempo, la configuración se vuelve coherente entre los equipos a medida que se abren y cierran con la configuración preferida.

Este escenario también se aplica a la configuración de Windows. Si la configuración de Windows en el equipo B debe ser la misma que la configuración de Windows del equipo A, el usuario debe iniciar sesión y cerrar la sesión en el equipo A.

Si la configuración de usuario que quiere el usuario se aplica en el orden equivocado, se puede recuperar ejecutando una operación de restauración para la aplicación específica o la configuración de Windows en el equipo en el que se sobrescribió la configuración. Para obtener más información, vea [administrar la copia de seguridad administrativa y restaurar en UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md).

### <a href="" id="capacity"></a>Planificación de rendimiento y capacidad

Especifique los requisitos de UE-V con capacidad de disco estándar y supervisión de estado de la red.

UE-V usa un recurso compartido de bloque de mensajes de servidor (SMB) para el almacenamiento de paquetes de configuración. El tamaño de los paquetes de configuración varía según la información de configuración de cada aplicación. Aunque la mayoría de los paquetes de configuración son pequeños, la sincronización de archivos potencialmente grandes, como las imágenes de escritorio, puede dar lugar a un bajo nivel de rendimiento, especialmente en redes más lentas.

Para reducir los problemas con la latencia de red, cree ubicaciones de almacenamiento de configuración en las mismas redes locales donde residen los equipos de los usuarios. Recomendamos 20 MB de espacio en disco por usuario para la ubicación de almacenamiento de configuración.

De forma predeterminada, la sincronización de UE-V agota los 2 segundos para evitar un retraso excesivo debido a un paquete de configuración grande. Puede configurar la opción SyncMethod = SyncProvider mediante objetos de [Directiva de grupo](https://technet.microsoft.com/library/dn458893.aspx).

### <a href="" id="high"></a>Alta disponibilidad para UE-V

La configuración de UE-V ubicación de almacenamiento y configuración catálogo de plantillas permite almacenar datos de usuario en cualquier recurso compartido grabable. Para garantizar la alta disponibilidad, siga estos criterios:

-   Formatee el volumen de almacenamiento con un sistema de archivos NTFS.

-   El uso compartido puede usar el sistema de archivos distribuido (DFS) pero existen restricciones.
En concreto, se admite la configuración de un único destino de replicación del sistema de archivos distribuido (DFS-R) con o sin un espacio de nombres del sistema de archivos distribuido (DFS-N).
Del mismo modo, solo se admite una única configuración de destino con DFS-N.
Para obtener información detallada, consulte [la declaración de soporte de Microsoft sobre los datos de Perfil de usuario replicados](https://go.microsoft.com/fwlink/p/?LinkId=313991) y también [información sobre la Directiva de soporte técnico de Microsoft para un escenario de implementación DFS-R y DFS-N](https://support.microsoft.com/kb/2533009).

    Además, como SYSVOL usa DFS-R para la replicación, SYSVOL no se puede usar para la replicación de archivos de datos de UE-V.

-   Configure los permisos de uso compartido y las listas de control de acceso (ACL) de NTFS como se especifica en [implementar la ubicación de almacenamiento de configuración de UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#ssl).

-   Use el clúster de servidor de archivos junto con el agente de UE-V para proporcionar acceso a las copias de los datos de estado de usuario en el caso de que se produzcan errores de comunicación.

-   Puede almacenar la configuración de datos de ruta de almacenamiento (datos de usuario) y plantillas de catálogo de plantillas de configuración en recursos compartidos agrupados, en recursos compartidos DFS-N o en ambos.

### <a href="" id="clocksync"></a>Sincronizar relojes de equipo para la sincronización de configuración de UE-V

Los equipos que ejecutan el agente de UE-V deben usar un servidor de tiempo para mantener una experiencia de configuración coherente. UE-V usa marcas de tiempo para determinar si es necesario sincronizar la configuración desde la ubicación de almacenamiento de configuración. Si el reloj del equipo no es exacto, es posible que la configuración anterior sobrescriba la configuración más reciente o que la nueva configuración no se guarde en la ubicación de almacenamiento de configuración.

## <a href="" id="prereqs"></a>Confirmar los requisitos previos y las configuraciones admitidas para UE-V


Antes de continuar, asegúrese de que su entorno incluye los siguientes requisitos para la ejecución de UE-V.

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
<th align="left"><strong>Sistema operativo</strong></th>
<th align="left"><strong>Edición</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>Arquitectura del sistema</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 7</p></td>
<td align="left"><p>Ultimate, Enterprise o Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 o superior</p></td>
<td align="left"><p>.NET Framework 4,5 o posterior para UE-V 2,1.</p>
<p>.NET Framework 4 o posterior para UE-V 2,0.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2008 R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter o Web Server</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 o superior</p></td>
<td align="left"><p>.NET Framework 4,5 o posterior para UE-V 2,1.</p>
<p>.NET Framework 4 o posterior para UE-V 2,0.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8 y Windows 8,1</p></td>
<td align="left"><p>Enterprise o Pro</p></td>
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>32 o 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 o superior</p></td>
<td align="left"><p>.NET Framework 4,5 o versiones posteriores</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows 10, versión anterior a 1607</p>
<div class="alert">
<strong>Nota</strong><br/><p>Solo UE-V 2,1 SP1 es compatible con Windows 10, versión anterior a la 1607</p>
</div>
<div>

</div></td>
<td align="left"><p>Enterprise o Pro</p></td>
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>32 o 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 o superior</p></td>
<td align="left"><p>.NET Framework 4.6</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows Server 2012 y Windows Server 2012 R2</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 o superior</p></td>
<td align="left"><p>.NET Framework 4,5 o versiones posteriores</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsServer2016</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 o superior</p></td>
<td align="left"><p>.NET Framework 4,6 o versiones posteriores</p></td>
</tr>
</tbody>
</table>



También...

-   **Licencia de MDOP:** Esta tecnología es parte del paquete de optimización de escritorio de Microsoft (MDOP). Los clientes empresariales pueden obtener MDOP con Microsoft Software Assurance. Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte ¿Cómo puedo obtener MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Credenciales administrativas** de cualquier equipo en el que vaya a instalarlo

**Nota**  

-   A partir de WIndows 10, versión 1607, UE-V se incluye con [Windows 10 para empresas](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) y ya no forma parte del paquete de optimización de escritorio de Microsoft.

-   La característica de Windows PowerShell de UE-V del agente de UE-V requiere .NET Framework 4 o superior, y Windows PowerShell 3,0 o versiones posteriores se habilitan. Descargue Windows PowerShell 3,0 [aquí](https://go.microsoft.com/fwlink/?LinkId=309609).

-   Instale .NET Framework 4 o .NET Framework 4,5 en equipos que ejecutan el sistema operativo Windows Server 2008 o Windows 7. Los sistemas operativos Windows 8, Windows 8,1 y Windows Server 2012 vienen con .NET Framework 4,5 instalado. El sistema operativo Windows 10 viene con .NET Framework 4,6 instalado.
-   La Directiva "eliminar la caché de itinerancia" de los perfiles obligatorios no es compatible con UE-V y no debe usarse.



No hay ningún requisito especial de memoria de acceso aleatorio (RAM) específico para UE-V.

### Sincronización de la configuración a través del proveedor de sincronización

El proveedor de sincronización es el valor predeterminado para los usuarios, que sincroniza una caché local con la ubicación de almacenamiento de configuración en estas instancias:

-   Inicio de sesión/cierre de sesión

-   Bloquear/desbloquear

-   Conexión o desconexión de escritorio remoto

-   Apertura de la aplicación/cerrar

Una tarea programada administra esta sincronización de la configuración cada 30 minutos o a través de ciertos eventos desencadenadores para ciertas aplicaciones. Para obtener más información, consulte [cambiar la frecuencia de UE-V 2. x tareas programadas](changing-the-frequency-of-ue-v-2x-scheduled-tasks-both-uevv2.md).

El agente UE-V sincroniza la configuración de usuario para equipos que no están siempre conectados a la red empresarial (equipos remotos y portátiles) y a equipos que siempre están conectados a la red (equipos que ejecutan Windows Server y sesiones de interfaz de escritorio virtual de host (VDI)).

**Sincronización para equipos con conexiones siempre disponibles:** Cuando usa UE-V en equipos que siempre están conectados a la red, debe configurar el agente de UE-V para sincronizar la configuración con el parámetro *SyncMethod = None* , que trata el servidor de almacenamiento de configuración como un recurso compartido de red estándar. En esta configuración, UE-V Agent se puede configurar para notificar si se retrasa la importación de la configuración de la aplicación.

Habilite esta configuración a través de uno de estos métodos:

-   Durante la instalación de UE-V, en el símbolo del sistema o en un archivo por lotes, establezca el parámetro AgentSetup.exe *SyncMethod = None*. [Implementar el agente de UE-V 2. x](https://technet.microsoft.com/library/dn458891.aspx#agent) proporciona más información.

-   Después de la instalación de UE-V, use la característica de administración de configuración en System Center 2012 Configuration Manager o en las plantillas de MDOP ADMX para insertar la configuración *SyncMethod = None* .

-   Use Windows PowerShell o el instrumental de administración de Windows (WMI) para establecer la configuración *SyncMethod = None* .

    **Nota**  
    Estos dos últimos métodos no funcionan para entornos de infraestructura de escritorio virtual (VDI) agrupados.



Debe reiniciar el equipo antes de que se inicie la sincronización de configuración.

**Nota**  
Si establece *SyncMethod = None*, los cambios de configuración se guardan directamente en el servidor. Si no se encuentra la conexión de red a la ruta de almacenamiento de configuración, los cambios de configuración se almacenan en caché en el dispositivo y se sincronizan la próxima vez que se ejecuta el proveedor de sincronización. Si no se encuentra la ruta de almacenamiento de configuración y el perfil de usuario se quita de un entorno de VDI agrupado, al cerrar sesión, se perderán los cambios de configuración y el usuario deberá volver a aplicar el cambio cuando el equipo se vuelva a conectar a la ruta de almacenamiento de configuración.



**Sincronización para motores de sincronización externos:** El parámetro *SyncMethod = external* especifica que si se escribe la configuración de UE-V en una carpeta local en el equipo del usuario, cualquier motor de sincronización externo (como OneDrive para la empresa, carpetas de trabajo, SharePoint o Dropbox) se puede usar para aplicar esta configuración a los diferentes equipos a los que los usuarios tienen acceso.

**Compatibilidad con sesiones de VDI compartidas:** UE-V 2,1 y 2,1 SP1 proporcionan soporte técnico para las sesiones de VDI que se comparten entre los usuarios finales. Puede registrar y configurar una plantilla especial de VDI, que garantiza que UE-V mantiene toda su funcionalidad intacta para sesiones de VDI no persistentes.

**Nota**  
Si no habilita el modo VDI para las sesiones de VDI no persistentes, algunas características no funcionarán, como [la copia de seguridad o la restauración y la última buena conocida (LKG)](https://technet.microsoft.com/library/dn878331.aspx).



La plantilla VDI se proporciona con UE-V 2,1 y 2,1 SP1 y suele estar disponible aquí después de la instalación: C:\\Archivos de Programa\\microsoft Virtualization\\Templates\\VdiState.xml

### Requisitos previos para la compatibilidad con el generador de UE-V

Instale el generador de UE-V en el equipo que se usa para crear plantillas de ubicación de configuración personalizadas. Este equipo debería poder ejecutar las aplicaciones cuya configuración está sincronizada. Debe ser miembro del grupo administradores en el equipo que ejecuta el software de generación de UE-V.

El generador de UE-V debe instalarse en un equipo que use un sistema de archivos NTFS. El software de generación de UE-V requiere .NET Framework 4. Para obtener más información, consulte [implementar UE-V 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).

## Otros recursos para este producto


-   [Virtualización de la experiencia del usuario de Microsoft (UE-V) 2. x](index.md)

-   [Introducción a UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Administración de UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Solución de problemas de UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Referencia técnica de UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)














