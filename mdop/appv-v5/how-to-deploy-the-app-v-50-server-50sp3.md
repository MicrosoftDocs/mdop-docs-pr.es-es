---
title: Cómo implementar el servidor de App-V 5.0
description: Cómo implementar el servidor de App-V 5.0
author: dansimp
ms.assetid: 4f8f16af-7d74-42b4-84b8-b04ce668225d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b94bab16349751aacf0aca0f8c2e5ac5a6ae6da7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814175"
---
# Cómo implementar el servidor de App-V 5.0


Use el siguiente procedimiento para instalar el servidor de App-V 5,0. Para obtener información sobre cómo implementar el servidor de App-V 5,0 SP3, consulte [acerca de App-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).

**Antes de empezar:**

-   Asegúrese de que ha instalado el software necesario. Consulte [requisitos previos de App-V 5,0](app-v-50-prerequisites.md).

-   Revise la sección de servidor de [consideraciones de seguridad de App-V 5,0](app-v-50-security-considerations.md).

-   Especifique un puerto en el que se hospedará cada componente.

-   Agregar reglas de Firewall para permitir que las solicitudes entrantes tengan acceso a los puertos especificados.

-   Si usa secuencias de comandos SQL, en lugar de Windows Installer, para configurar la base de datos de administración o la base de datos de informes, debe ejecutar las secuencias de comandos SQL antes de instalar el servidor de administración o el servidor de informes. Vea [cómo implementar las bases de datos de App-V con scripts SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).

**Para instalar el servidor de App-V 5,0**

1. Copie los archivos de instalación de App-V 5,0 Server en el equipo en el que desea instalarlo.

2. Para iniciar la instalación del servidor de App-V 5,0, haga clic con el botón secundario en **appv\_server\_setup.exe** como administrador y, a continuación, haga clic en **instalar**.

3. Revise y acepte los términos de licencia y elija si desea habilitar las actualizaciones de Microsoft.

4. En la página **selección de características** , seleccione todos los componentes siguientes.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Componente</th>
   <th align="left">Descripción</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Servidor de administración</p></td>
   <td align="left"><p>Proporciona funcionalidad de administración general para la infraestructura de App-V.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Base de datos de administración</p></td>
   <td align="left"><p>Facilita las preimplementaciones de base de datos para administración de App-V.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Servidor de publicación</p></td>
   <td align="left"><p>Proporciona funcionalidades de hospedaje y transmisión por secuencias para aplicaciones virtuales.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Servidor de informes</p></td>
   <td align="left"><p>Proporciona App-V 5,0 Reporting Services.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Base de datos de informes</p></td>
   <td align="left"><p>Facilita las preimplementaciones de base de datos para informes de App-V.</p></td>
   </tr>
   </tbody>
   </table>

     

5. En la página **Ubicación de instalación** , acepte la ubicación predeterminada en la que se instalarán los componentes seleccionados, o bien cambie la ubicación escribiendo una nueva ruta en la línea de ubicación de **instalación** .

6. En la página inicial **crear nueva base de datos de administración** , configure la instancia de **Microsoft SQL Server** y la **base de datos del servidor de administración** seleccionando la opción correspondiente a continuación.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Método</th>
   <th align="left">Lo que debe hacer</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Está usando una instancia personalizada de Microsoft SQL Server.</p></td>
   <td align="left"><p>Seleccione <strong> usar la instancia personalizada </strong> y escriba el nombre de la instancia.</p>
   <p>Use el formato <strong> InstanceName </strong> . La ubicación de instalación asumida es el equipo local.</p>
   <p>No compatible: un nombre de servidor con el formato <strong> ServerName </strong> &lt; &gt; Instance </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Está usando un nombre de base de datos personalizado.</p></td>
   <td align="left"><p>Seleccione <strong> Configuración personalizada </strong> y escriba el nombre de la base de datos.</p>
   <p>El nombre de la base de datos debe ser único o se producirá un error en la instalación.</p></td>
   </tr>
   </tbody>
   </table>

     

7. En la página **configurar** , acepte el valor predeterminado **use este equipo local**.

   **Nota**  
   Si va a instalar el servidor de administración y la base de datos de administración en paralelo, algunas opciones de esta página no estarán disponibles. En este caso, las opciones adecuadas se seleccionan de forma predeterminada y no se pueden cambiar.

     

8. En la página inicial **crear nueva base de datos de informes** , configure la instancia de **Microsoft SQL Server** y la **base de datos del servidor de informes** seleccionando la opción correspondiente a continuación.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Método</th>
   <th align="left">Lo que debe hacer</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Está usando una instancia personalizada de Microsoft SQL Server.</p></td>
   <td align="left"><p>Seleccione <strong> usar la instancia personalizada </strong> y escriba el nombre de la instancia.</p>
   <p>Use el formato <strong> InstanceName </strong> . La ubicación de instalación asumida es el equipo local.</p>
   <p>No compatible: un nombre de servidor con el formato <strong> ServerName </strong> &lt; &gt; Instance </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Está usando un nombre de base de datos personalizado.</p></td>
   <td align="left"><p>Seleccione <strong> Configuración personalizada </strong> y escriba el nombre de la base de datos.</p>
   <p>El nombre de la base de datos debe ser único o se producirá un error en la instalación.</p></td>
   </tr>
   </tbody>
   </table>

     

9. En la página **configurar** , acepte el valor predeterminado: **usar este equipo local**.

   **Nota**  
   Si va a instalar el servidor de administración y la base de datos de administración en paralelo, algunas opciones de esta página no estarán disponibles. En este caso, las opciones adecuadas se seleccionan de forma predeterminada y no se pueden cambiar.

     

10. En la página **configurar** (configuración del servidor de administración), especifique lo siguiente:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Elemento para configurar</th>
    <th align="left">Descripción y ejemplos</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Escriba el grupo de AD con permisos suficientes para administrar el entorno de App-V.</p></td>
    <td align="left"><p>Ejemplo: MyDomain\MyUser</p>
    <p>Después de la instalación, puede Agregar usuarios o grupos adicionales mediante la consola de administración. Sin embargo, los grupos de seguridad global y los grupos de distribución de servicios de dominio de Active Directory (AD DS) no son compatibles. <strong> </strong> <strong> Para realizar esta acción, es necesario usar grupos universales o locales </strong> de dominio.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Nombre del sitio Web </strong> : especifique el nombre personalizado que se usará para ejecutar el servicio de publicación.</p></td>
    <td align="left"><p>Si no tiene un nombre personalizado, no realice ningún cambio.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Enlace de puerto </strong> : especifique un número de puerto único que será usado por App-V.</p></td>
    <td align="left"><p>Ejemplo: <strong> 12345</strong></p>
    <p>Asegúrate de que el puerto especificado no esté siendo usado por otro sitio Web.</p></td>
    </tr>
    </tbody>
    </table>

     

11. En la página **configurar** **Publishing Server** , especifique lo siguiente:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Elemento para configurar</th>
    <th align="left">Descripción y ejemplos</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Especifique la dirección URL para el servicio de administración.</p></td>
    <td align="left"><p>Ejemplo<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Nombre del sitio Web </strong> : especifique el nombre personalizado que se usará para ejecutar el servicio de publicación.</p></td>
    <td align="left"><p>Si no tiene un nombre personalizado, no realice ningún cambio.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Enlace de puerto </strong> : especifique un número de puerto único que será usado por App-V.</p></td>
    <td align="left"><p>Ejemplo: 54321</p>
    <p>Asegúrate de que el puerto especificado no esté siendo usado por otro sitio Web.</p></td>
    </tr>
    </tbody>
    </table>

     

12. En la página **servidor de informes** , especifique lo siguiente:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Elemento para configurar</th>
    <th align="left">Descripción y ejemplos</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Nombre del sitio Web </strong> : especifique el nombre personalizado que se usará para ejecutar el servicio de informes.</p></td>
    <td align="left"><p>Si no tiene un nombre personalizado, no realice ningún cambio.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Enlace de puerto </strong> : especifique un número de puerto único que será usado por App-V.</p></td>
    <td align="left"><p>Ejemplo: 55555</p>
    <p>Asegúrate de que el puerto especificado no esté siendo usado por otro sitio Web.</p></td>
    </tr>
    </tbody>
    </table>

     

13. Para iniciar la instalación, haga clic en **instalar** en la página **listo** y, a continuación, haga clic en **cerrar** en la página **finalizada** .

14. Para comprobar que la configuración se completó correctamente, abra un explorador Web y escriba la siguiente dirección URL:

    **http:// &lt; Nombre del equipo servidor de administración &gt; : &lt; número de puerto del servicio de administración &gt; /Console.html**.

    Ejemplo: **http://localhost:12345/console.html** . Si la instalación se realizó correctamente, se muestra la consola de administración de App-V sin errores.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Implementación de App-V 5.0](deploying-app-v-50.md)

[Cómo instalar bases de datos de informes y administración en distintos equipos desde los servicios de informes y administración](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[Cómo instalar el servidor de publicación en un equipo remoto](how-to-install-the-publishing-server-on-a-remote-computer.md)

[Cómo implementar el servidor de App-V 5.0 mediante un script](how-to-deploy-the-app-v-50-server-using-a-script.md)

[Cómo habilitar los informes en el cliente de App-V 5.0 mediante PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

 

 





