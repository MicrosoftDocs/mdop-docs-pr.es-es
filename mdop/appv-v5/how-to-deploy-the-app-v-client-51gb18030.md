---
title: Cómo implementar el cliente de App-V
description: Cómo implementar el cliente de App-V
author: dansimp
ms.assetid: 981f57c9-56c3-45da-8261-0972bfad3e5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: ea216f6b86820f752e0c0ac693470eac72cb847a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814126"
---
# Cómo implementar el cliente de App-V


Use el siguiente procedimiento para instalar el cliente de Microsoft Application Virtualization (App-V) 5,1 y el cliente de servicios de escritorio remoto. Debe instalar la versión del cliente que se corresponda con el sistema operativo del equipo de destino.

<a href="" id="bkmk-clt-install-prereqs"></a>**Qué hacer antes de empezar**

1. Revise e instale los requisitos previos de software:

   Instale el software necesario que corresponde a la versión de la aplicación de App-V que está instalando:

   -   [Acerca de App-V 5.1](about-app-v-51.md)

   -   [Requisitos previos de App-V 5.1](app-v-51-prerequisites.md)

2. Revise la coexistencia del cliente y los escenarios no admitidos, como se aplica a la instalación:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Implementación de clientes de App-V coexistentes</p></td>
   <td align="left"><p><a href="planning-for-the-app-v-51-sequencer-and-client-deployment.md" data-raw-source="[Planning for the App-V 5.1 Sequencer and Client Deployment](planning-for-the-app-v-51-sequencer-and-client-deployment.md)">Planificación de la implementación del cliente y del secuenciador de App-V 5.1</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Escenarios de instalación no compatibles o limitadas</p></td>
   <td align="left"><p>Consulte la sección cliente en las <a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)"> configuraciones admitidas de App-V 5,1</a></p></td>
   </tr>
   </tbody>
   </table>



3. Revise las ubicaciones de información del registro del cliente, registro y solución de problemas:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Información del registro del cliente</p></td>
<td align="left"><ul>
<li><p>De forma predeterminada, después de instalar el cliente de App-V 5,1, la información del cliente se almacena en el registro, en la siguiente clave del registro:</p>
<p><strong>HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ APPV \ CLIENTE</strong></p></li>
<li><p>Al implementar un paquete virtualizado en un equipo que ejecuta el cliente de App-V, los datos del paquete asociado se almacenan en la siguiente ubicación:</p>
<p><strong>C: \ ProgramData \ App-V</strong></p>
<p>Sin embargo, puede volver a configurar esta ubicación con la siguiente clave del registro:</p>
<p><strong>HKEY_LOCAL_MACHINE \ SOFTWARE \ MICROSOFT \ SOFTWARE \ MICROSOFT \ APPV \ CLIENT \ STREAMING \ PACKAGEINSTALLATIONROOT</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Archivos de registro de cliente</p></td>
<td align="left"><ul>
<li><p>Para obtener información sobre el archivo de registro asociada con el cliente de App-V 5,1, busque en el siguiente registro:</p>
<p><strong>Registros de eventos/aplicaciones y servicios/Microsoft/AppV</strong></p></li>
<li><p>En App-V 5,0 SP3, algunos registros se consolidaron y se movieron a la siguiente ubicación:</p>
<p><strong>Registros de eventos, registros de aplicaciones y servicios/Microsoft/AppV/ServiceLog</strong></p>
<p>Para obtener una lista de los registros que se han movido, consulte <a href="about-app-v-50-sp3.md#bkmk-event-logs-moved" data-raw-source="[About App-V 5.0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved)"> acerca de App-V 5,0 SP3 </a> .</p></li>
<li><p>Los paquetes que se encuentran almacenados en los equipos que ejecutan el cliente de App-V 5,1 se guardan en la siguiente ubicación:</p>
<p><strong>C:\ProgramData\App-V &amp; lt; identificador de paquete &gt; &amp; lt; identificador de versión&gt;</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Información para la solución de problemas de instalación del cliente</p></td>
<td align="left"><p>Consulte el registro de errores en la <strong> carpeta% Temp% </strong> . Para revisar los archivos de registro, haga clic en <strong> Inicio </strong> , escriba <strong> % temp% </strong> y, a continuación, busque el <strong> registro de appv_ </strong> .</p></td>
</tr>
</tbody>
</table>



**Para instalar el cliente de App-V 5,1**

1.  Copie el archivo de instalación del cliente App-V 5,1 en el equipo en el que se instalará. Elija entre los siguientes tipos de cliente:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Tipo de cliente</th>
    <th align="left">Archivo para usar</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Versión estándar del cliente</p></td>
    <td align="left"><p><strong>appv_client_setup.exe</strong></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Versión de servicios de escritorio remoto del cliente</p></td>
    <td align="left"><p><strong>appv_client_setup_rds.exe</strong></p></td>
    </tr>
    </tbody>
    </table>



2.  Haga doble clic en el archivo de instalación y haga clic en **instalar**. Antes de comenzar la instalación, el instalador comprueba si el equipo tiene [requisitos previos de App-V 5,1](app-v-51-prerequisites.md).

3.  Revise y acepte los términos de licencia del software, elija si desea usar Microsoft Update y si desea participar en el programa para la mejora de la experiencia del usuario de Microsoft, y haga clic en **instalar**.

4.  En la página la **configuración se completó correctamente** , haga clic en **cerrar**.

    La instalación crea las siguientes entradas para el cliente App-V en los **programas**:

    -   **.exe**

    -   **.msi**

    -   **paquete de idioma**

        **Nota**  
        Después de la instalación, solo se puede desinstalar el archivo. exe.



**Para instalar el cliente de App-V 5,1 con un script**

1. Instale todo el software necesario necesario en los equipos de destino. Consulte [Qué hacer antes de empezar](#bkmk-clt-install-prereqs). Si instala el cliente con un archivo. msi, se producirá un error en la instalación si falta alguno de los requisitos previos.

2. Para usar un script para instalar el cliente de App-V 5,1, use los siguientes parámetros con **appv\_client\_setup.exe**.

   **Nota**  
   El instalador de Windows (. msi) cliente admite el mismo conjunto de conmutadores, excepto el parámetro **/log** .

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p>/INSTALLDIR</p></td>
   <td align="left"><p>Especifica el directorio de instalación. Ejemplo de uso: <strong> /INSTALLDIR = c:\Archivos de Files\AppV Client</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/CEIPOPTIN</p></td>
   <td align="left"><p>Permite la participación en el programa para la mejora de la experiencia del usuario. Ejemplo de uso: <strong> /CEIPOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/MUOPTIN</p></td>
   <td align="left"><p>Habilita Microsoft Update. Ejemplo de uso: <strong> /MUOPTIN = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/PACKAGEINSTALLATIONROOT</p></td>
   <td align="left"><p>Especifica el directorio en el que se instalarán todas las nuevas aplicaciones y actualizaciones. Ejemplo de uso: <strong> /PACKAGEINSTALLATIONROOT =&#39;C:\App-V packages&#39;</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/PACKAGESOURCEROOT</p></td>
   <td align="left"><p>Invalida la ubicación de origen para descargar el contenido del paquete. Ejemplo de uso: <strong> /PACKAGESOURCEROOT =&#39;<a href="http://packageStore" data-raw-source="http://packageStore"> http://packageStore </a>&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/AUTOLOAD</p></td>
   <td align="left"><p>Especifica cómo se cargarán los nuevos paquetes por App-V 5,1 en un equipo específico. Las siguientes opciones están habilitadas: [1]; cargar automáticamente todos los paquetes [2]; o no carga automáticamente paquetes [0]. <strong> Ejemplo de uso:/AUTOLOAD = [0 | 1 | 2]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/SHAREDCONTENTSTOREMODE</p></td>
   <td align="left"><p>Especifica que el contenido del paquete transmitido no se guardará en el disco duro local. Ejemplo de uso: <strong> /SHAREDCONTENTSTOREMODE = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/MIGRATIONMODE</p></td>
   <td align="left"><p>Permite que el cliente de App-V 5,1 modifique los accesos directos y los FTAs asociados a los paquetes creados con una versión anterior. Ejemplo de uso: <strong> /MIGRATIONMODE = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ENABLEPACKAGESCRIPTS</p></td>
   <td align="left"><p>Habilita los scripts que se definen en el archivo de manifiesto del paquete o los archivos de configuración que se deben ejecutar. Ejemplo de uso: <strong> /ENABLEPACKAGESCRIPTS = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/ROAMINGREGISTRYEXCLUSIONS</p></td>
   <td align="left"><p>Especifica las rutas de registro que no se transferirán a un perfil de usuario. Ejemplo de uso: <strong> /ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ROAMINGFILEEXCLUSIONS</p></td>
   <td align="left"><p>Especifica las rutas de archivo relativas a% userprofile% que no se mueven con un perfil de usuario&#39;s. Ejemplo de uso: <strong> /ROAMINGFILEEXCLUSIONS &#39;escritorio; mis imágenes&#39;</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERNAME</p></td>
   <td align="left"><p>Muestra el nombre del servidor de publicación. Ejemplo de uso: <strong> /S2PUBLISHINGSERVERNAME = MyPublishingServer</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] PUBLISHINGSERVERURL</p></td>
   <td align="left"><p>Muestra la dirección URL del servidor de publicación. Ejemplo de uso: <strong> /S2PUBLISHINGSERVERURL = \pubserver</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHENABLED-</p></td>
   <td align="left"><p>Habilita una actualización de publicación global. Ejemplo de uso: <strong> /S2GLOBALREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHONLOGON</p></td>
   <td align="left"><p>Inicia una actualización de publicación global cuando un usuario inicia sesión. Ejemplo de uso: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVAL-</p></td>
   <td align="left"><p>Especifica el intervalo de actualización de la publicación, donde <strong> 0 </strong> indica que no se actualiza periódicamente. Ejemplo de uso: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] GLOBALREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>Especifica la unidad de intervalo (horas [0], días [1]). Ejemplo de uso: <strong> /S2GLOBALREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHENABLED</p></td>
   <td align="left"><p>Habilita la actualización de publicaciones de usuario. Ejemplo de uso: <strong> /S2USERREFRESHENABLED = [0 | 1]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHONLOGON</p></td>
   <td align="left"><p>Inicia una actualización de publicación de usuario cuando un usuario inicia sesión. Ejemplo de uso: <strong> /S2LOGONREFRESH = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVAL-</p></td>
   <td align="left"><p>Especifica el intervalo de actualización de la publicación, donde <strong> 0 </strong> indica que no se actualiza periódicamente. Ejemplo de uso: <strong> /S2PERIODICREFRESHINTERVAL = [0-744]</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/S [1-5] USERREFRESHINTERVALUNIT</p></td>
   <td align="left"><p>Especifica la unidad de intervalo (horas [0], días [1]). Ejemplo de uso: <strong> /S2USERREFRESHINTERVALUNIT = [0 | 1]</strong></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Log</p></td>
   <td align="left"><p>Especifica una ubicación donde se guarda la información del registro. La ubicación predeterminada es% Temp%. Ejemplo de uso: <strong> /log C:\logs\log.log</strong></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>q</p></td>
   <td align="left"><p>Especifica una instalación desatendida.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Pair</p></td>
   <td align="left"><p>Repara una instalación de cliente anterior.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/NORESTART</p></td>
   <td align="left"><p>Impide que el equipo se reinicie después de la instalación del cliente.</p>
   <p>El parámetro impide que el equipo del usuario final se reinicie después de que se instalen las actualizaciones y le permite programar el reinicio cuando lo desee. Por ejemplo, puede instalar App-V 5,1 y, a continuación, instalar el paquete de revisiones Y sin reiniciar después de la instalación del Service Pack. Después de la instalación, debe reiniciar antes de empezar a usar App-V.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/UNINSTALL</p></td>
   <td align="left"><p>Desinstala el cliente.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/ACCEPTEULA</p></td>
   <td align="left"><p>Acepta el contrato de licencia. Esto es necesario para una instalación desatendida. Ejemplo de uso: <strong> /ACCEPTEULA </strong> o <strong> /ACCEPTEULA = 1 </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/LAYOUT</p></td>
   <td align="left"><p>Especifica la acción de diseño asociada. También extrae los archivos de Windows Installer (. msi) y de script a una carpeta sin instalar App-V 5,1. No se espera ningún valor.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>/LAYOUTDIR</p></td>
   <td align="left"><p>Especifica el directorio de diseño. Requiere un valor de cadena. Ejemplo de uso: <strong> /LAYOUTDIR = "cliente de virtualización de C:\Application" </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>/?,/h,/Help</p></td>
   <td align="left"><p>Solicita ayuda acerca de los parámetros de instalación anteriores.</p></td>
   </tr>
   </tbody>
   </table>



**Para instalar el cliente de App-V 5,1 con el archivo de Windows Installer (. msi)**

1.  Instale los requisitos previos necesarios en los equipos de destino. Consulte [Qué hacer antes de empezar](#bkmk-clt-install-prereqs). Si no se cumplen los requisitos previos, se producirá un error en la instalación.

2.  Asegúrese de que los equipos de destino no tengan reinicios pendientes antes de instalar el cliente con los archivos App-V 5,1 Windows Installer (. msi). Los archivos de Windows Installer no marcan un reinicio pendiente.

3.  Implemente uno de los siguientes archivos de Windows Installer en el equipo de destino. El archivo que especifique debe coincidir con la configuración del equipo de destino.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Tipo de implementación</th>
    <th align="left">Implementar este archivo</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>El equipo está ejecutando un sistema operativo Microsoft Windows de 32 bits</p></td>
    <td align="left"><p>appv_client_MSI_x86.msi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>El equipo está ejecutando un sistema operativo Microsoft Windows de 64 bits</p></td>
    <td align="left"><p>appv_client_MSI_x64.msi</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Está implementando el cliente de servicios de escritorio remoto de App-V 5,1</p></td>
    <td align="left"><p>appv_client_rds_MSI_x64.msi</p></td>
    </tr>
    </tbody>
    </table>



4.  Con la información de la tabla siguiente, seleccione el paquete de idioma correspondiente **. msi** para instalar según el idioma que desee para el equipo de destino. La **xxxx** de la tabla se refiere a la configuración regional de destino del paquete de idioma.

    **Qué debe saber antes de empezar:**

    -   Los paquetes de idioma son comunes al cliente de App-V 5,1 estándar y a la versión de servicios de escritorio remoto del cliente de App-V 5,1.

    -   Si instala el cliente de App-V 5,1 con el **archivo. exe**, el instalador solo implementará el paquete de idioma que coincida con el sistema operativo que se ejecuta en el equipo de destino.

    -   Para implementar paquetes de idioma adicionales en un equipo de destino, use el procedimiento **para instalar el cliente de App-V 5,1 con el archivo de Windows Installer (. msi)**.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Tipo de implementación</th>
    <th align="left">Implementar este archivo</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>El equipo está ejecutando un sistema operativo Microsoft Windows de 32 bits</p></td>
    <td align="left"><p>appv_client_LP_xxxx_ x86.msi</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>El equipo está ejecutando un sistema operativo Microsoft Windows de 64 bits</p></td>
    <td align="left"><p>appv_client_LP_xxxx_ x64.msi</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Temas relacionados


[Implementación de App-V 5.1](deploying-app-v-51.md)

[Información acerca de la configuración de cliente](about-client-configuration-settings51.md)

[Cómo desinstalar el cliente de App-V 5.1](how-to-uninstall-the-app-v-51-client.md)









