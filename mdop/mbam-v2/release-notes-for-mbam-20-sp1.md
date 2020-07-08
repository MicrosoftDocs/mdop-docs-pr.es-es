---
title: Notas de la versión de MBAM 2.0 SP1
description: Notas de la versión de MBAM 2.0 SP1
author: dansimp
ms.assetid: b39002ba-33c6-45ec-9d1b-464327b60f5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 54a77fc7a493b36217ae2cdc875226b25fdc6e7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825581"
---
# Notas de la versión de MBAM 2.0 SP1


Para buscar estas notas de la versión, presione Ctrl + F.

Lea estas notas de la versión minuciosamente antes de instalar Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 Service Pack 1 (SP1). Estas notas de la versión contienen la información necesaria para instalar correctamente la administración de BitLocker y la supervisión de 2,0 SP1, y contienen información que no está disponible en la documentación del producto. Si hay una diferencia entre estas notas de la versión y otra documentación de MBAM 2,0 SP1, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> Problemas conocidos de MBAM 2,0 SP1


Esta sección contiene problemas conocidos de MBAM 2,0 SP1.

### La actualización de MBAM con topología integrada de Configuration Manager a MBAM 2,0 SP1 requiere la eliminación manual de los objetos de Configuration Manager

Si está usando MBAM con Configuration Manager y desea actualizar a MBAM 2,0 SP1, debe quitar manualmente todos los objetos de Configuration Manager que se instalaron en Configuration Manager como parte de la instalación de MBAM. Los objetos que debe quitar manualmente son los informes MBAM, la colección de MBAM equipos compatibles y la línea base de configuración de protección de BitLocker y los elementos de configuración asociados.

**Solución alternativa**: actualice los objetos de Configuration Manager completando los siguientes pasos:

1.  Haga una copia de seguridad de los datos de cumplimiento existentes en un archivo externo, como se describe en los siguientes pasos.

    **Nota:**  Todos los datos de cumplimiento de BitLocker existentes se eliminarán al eliminar la línea base existente en Configuration Manager. Los datos se volverán a generar a lo largo del tiempo, pero se recomienda que guarde una copia de los datos en caso de que necesite los datos de cumplimiento de un equipo determinado antes de que se hayan regenerado los datos de cumplimiento.

     

    1.  Para guardar los datos de cumplimiento de BitLocker históricos, abra el informe **detalles de cumplimiento de BitLocker Enterprise** .

    2.  Haga clic en el icono **Guardar** en el informe y seleccione **Excel**.

        El informe guardado contendrá datos como, por ejemplo, el nombre del equipo, el nombre de dominio, el estado de cumplimiento, la exención, los usuarios del dispositivo, los detalles del estado de cumplimiento y la fecha y hora del último contacto. Algunos datos, como la información detallada del volumen y la intensidad de cifrado, no se guardan.

2.  Desinstale **MBAM** del servidor con el instalador de **MBAM** .

3.  Elimine manualmente los siguientes objetos de Configuration Manager:

    -   Colección de equipos compatibles con MBAM

    -   Línea base de protección de BitLocker

    -   Elemento de configuración de protección de unidad del sistema operativo BitLocker

    -   Elemento de configuración de protección de unidades de datos fijos de BitLocker

4.  Elimine manualmente la carpeta de informes de MBAM en el sitio de SQL Server Reporting Services de Configuration Manager. Para ello:

    1.  Use Internet Explorer para desplazarse hasta el punto de servicios de informes, por ejemplo, http:// &lt; yourcmserver &gt; /Reports.

    2.  Haga clic en el vínculo de código de sitio de Configuration Manager adecuado.

    3.  Elimine la carpeta MBAM.

5.  Use el instalador de MBAM Server para volver a instalar los objetos de integración de Configuration Manager. Los equipos cliente comenzarán a cargar los datos de cumplimiento de BitLocker a lo largo del tiempo.

### El botón Enviar del portal de autoservicio no funciona en Internet Explorer10

Al usar Internet Explorer10 para acceder al sitio web de administración y supervisión, el botón **Enviar** del sitio web no funciona.

**Solución alternativa**: en el servidor donde instaló el sitio web de supervisión y administración, instale el [hotfix para ASP.net archivos de definición de explorador](https://go.microsoft.com/fwlink/?LinkId=317798).

### No se admiten nombres de dominio internacionales

MBAM 2,0 SP1 no admite nombres de dominio internacionales.

**Solución alternativa**: ninguno.

### Los informes del sitio web de administración y supervisión muestran una advertencia si SSL no está configurado en SSRS

Si SQLServer Reporting Services (SSRS) no se configuró para usar la capa de sockets seguros (SSL), la dirección URL de los informes se establecerá en HTTP en lugar de HTTPS cuando instale el servidor MBAM. Si, a continuación, visita el sitio web de administración y supervisión y selecciona un informe, aparece el siguiente mensaje: "solo se muestra el contenido seguro".

**Solución**: para corregir este problema, configure SSL en el **Administrador de configuración de Reporting Services** en el servidor de MBAM donde esté instalado SQLServer Reporting Services. Desinstale y vuelva a instalar el sitio web del servidor de supervisión y administración.

### Al hacer clic en atrás en el informe Resumen de cumplimiento puede crear un error

Si profundiza en un informe Resumen de cumplimiento y, a continuación, hace clic en el vínculo **atrás** en el informe de SSRS, es posible que se produzca un error.

**Solución alternativa**: ninguno.

### El cifrado de espacio usado no funciona correctamente

Si cifra un equipo por primera vez después de instalar el cliente MBAM y ha establecido un objeto de directiva de grupo para implementar el cifrado solo de espacio usado, MBAM cifra de forma errónea todo el disco en lugar de cifrar solo el espacio usado por el disco. Si un equipo ya está cifrado con el cifrado solo de espacio usado antes de instalar el cliente MBAM y ha establecido el mismo objeto de directiva de grupo de cifrado de espacio solo usado, MBAM reconoce la configuración e informa correctamente el cifrado en los informes de cumplimiento.

**Solución alternativa**: ninguno.

### La intensidad de cifrado no se muestra correctamente en el informe de cumplimiento de equipos

Si no establece una intensidad de cifrado específica en el objeto de directiva de grupo **elegir método de cifrado de unidad y intensidad** de cifrado, el informe de cumplimiento de equipos de la topología integrada de Configuration Manager siempre muestra **desconocido** para la intensidad de cifrado, incluso si la intensidad de cifrado usa el valor predeterminado de cifrado de 128 bits. El informe muestra la intensidad de cifrado correcta si establece una intensidad de cifrado específica en el objeto de directiva de grupo.

**Solución alternativa**: establezca siempre una intensidad de cifrado específica en el **método elegir cifrado de unidad y** el objeto de directiva de grupo intensidad de cifrado.

### La distribución del estado de cumplimiento por tipo de unidad muestra datos antiguos después de actualizar los elementos de configuración

Después de actualizar los elementos de configuración de MBAM en SystemCenter2012 ConfigurationManager, el gráfico de barras distribución del estado de cumplimiento por tipo de unidad del panel de cumplimiento de la empresa de BitLocker muestra datos que se basan en información de versiones anteriores de los elementos de configuración.

**Solución alternativa**: ninguno. No se admite la modificación de los elementos de configuración MBAM y es posible que el informe no se muestre de la forma esperada.

### La configuración de seguridad mejorada puede provocar que los informes no se muestren correctamente

Si la configuración de seguridad mejorada de Internet Explorer (ESC) está activada, es posible que aparezca un mensaje de **acceso denegado** cuando intente ver informes en el servidor de MBAM. De forma predeterminada, la configuración de seguridad mejorada está activada para proteger el servidor al disminuir la exposición del servidor a potenciales ataques que pueden producirse a través de contenido web y secuencias de comandos de aplicaciones.

**Solución**: Si el mensaje **acceso denegado** aparece cuando intenta ver informes en el servidor de MBAM, puede establecer un objeto de directiva de grupo o cambiar el valor predeterminado manualmente en la imagen para deshabilitar la configuración de seguridad mejorada. También puede ver los informes desde otro equipo en el que la configuración de seguridad mejorada no esté habilitada.

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> Se produce un error en la instalación de MBAM Server al actualizar de SQLServer2008 a SQLServer2012

Si actualiza de SQLServer2008 a SQLServer2012 y, a continuación, intenta instalar la base de datos de cumplimiento y auditoría o la base de datos de recuperación, se produce un error en la instalación y se deshace. El error se produce porque el archivo de SQLCMD.exe necesario se quitó durante la actualización de SQLServer y el instalador de MBAM no lo puede encontrar. Las líneas del archivo de registro MSI pueden tener un aspecto similar al siguiente:

RunDbInstallScript de BD de recuperación de RunDbInstallScript: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exede BD dB de recuperación: dbInstance-xxxxxx\\I01RunDbInstallScript de BD Recovery: sqlScript-C:\\Archivos de Files\\Microsoft\\Microsoft administración de BitLocker y Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript de BD de recuperación: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript defaultFileName-MBAM _Recovery \ I01\\MSSQL\\DATA\\RunDbInstallScript de BD de recuperación de certificados: defaultLogPath-K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\RunDbInstallScript recuperación de la BD CA: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Program Files\\Microsoft\\Microsoft administración de BitLocker y Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript de BD Recovery dB: comenzando a ejecutar el complemento de base de datos de recuperación scriptRunDbInstallScript recuperación de BD de BD: el archivo de registro SQLCMD se encuentra en C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript de BD de recuperación excepción: instalar la acción personalizada de la base de datos de recuperación excepción: el sistema no puede encontrar el archivo especificado

El Windows Installer de MBAM Server está codificado para encontrar la ruta de acceso SQLCMD.exe mirando en el valor de la cadena de la ruta de acceso en el registro en HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup. La clave sigue presente durante la migración de SQLServer2008 a SQLServer2012, pero la ruta de acceso a la que hace referencia el valor de los datos no contiene el archivo SQLCMD.exe, porque el proceso de SQLupgrade quitó el archivo.

**Solución alternativa**: Cambie temporalmente el valor de la cadena de ruta de acceso de HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup a **path \ _old**y, a continuación, vuelva a ejecutar Windows Installer en el servidor de MBAM. Cuando la instalación se complete correctamente y cree las bases de datos en SQLServer2012, cambie el nombre de **path \ _old** a **path**.

## Revisiones y artículos de Knowledge base para MBAM 2,0 SP1


Esta sección contiene revisiones y artículos de KB para MBAM 2,0 SP1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Artículo de KB</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2831166</p></td>
<td align="left"><p>Instalar Microsoft BitLocker Administration and Monitoring (MBAM) 2,0 falla con los &quot; objetos de System Center cm ya instalados&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)">support.microsoft.com/kb/2831166/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870849</p></td>
<td align="left"><p>Los usuarios no pueden recuperar la clave de recuperación de BitLocker con el portal de autoservicio de MBAM 2.0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)">support.microsoft.com/kb/2870849/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2756402</p></td>
<td align="left"><p>El cliente de MBAM no funcionaba con el identificador de evento 4 y el código de error 0x8004100E en la descripción del evento</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620287</p></td>
<td align="left"><p>Mensaje de error "error de servidor en '/Reports ' aplicación" al hacer clic en la pestaña informes en MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)">support.microsoft.com/kb/2620287/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Error al abrir informes de cumplimiento de los equipos o de la empresa en MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>Los informes de empresa de MBAM no se actualizan</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2712461</p></td>
<td align="left"><p>No se admite la instalación de MBAM en un controlador de dominio</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)">support.microsoft.com/kb/2712461/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2876732</p></td>
<td align="left"><p>Recibe el código de error 0x80071a90 durante la instalación independiente o de integración del administrador de configuración de MBAM 2.0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)">support.microsoft.com/kb/2876732/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2754259</p></td>
<td align="left"><p>MBAM y comunicaciones seguras de red</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)">support.microsoft.com/kb/2754259/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>El programa de instalación de MBAM 2.0 falla durante el escenario de integración de Configuration Manager con SQL Server 2008</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2668533</p></td>
<td align="left"><p>Se produce un error en la instalación de MBAM si SQL SSRS no se ha configurado correctamente</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)">support.microsoft.com/kb/2668533/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870847</p></td>
<td align="left"><p>La instalación de MBAM 2,0 produce un &quot; error al recuperar la configuración del rol de servidor de Configuration Manager para &#39;rol de&#39; de punto de servicios de informes&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)">support.microsoft.com/kb/2870847/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2870839</p></td>
<td align="left"><p>Los informes de MBAM 2.0 Enterprise no se actualizan en la topología de MBAM 2.0 Standalone debido a errores de CreateCache de trabajo de SQL</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)">support.microsoft.com/kb/2870839/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>Los informes de empresa de MBAM no se actualizan</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2935997</p></td>
<td align="left"><p>MBAM equipos compatibles los informes de cumplimiento incluyen incorrectamente los productos no compatibles</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)">support.microsoft.com/kb/2935997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2612822</p></td>
<td align="left"><p>El registro del equipo se ha rechazado en MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)">support.microsoft.com/kb/2612822/EN-US</a></p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Acerca de MBAM 2.0 SP1](about-mbam-20-sp1.md)

 

 





