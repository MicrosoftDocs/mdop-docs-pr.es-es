---
title: Registros de eventos de servidor
description: Registros de eventos de servidor
author: dansimp
ms.assetid: 04e724d2-28cc-4fa8-86a1-0d4ab0234b11
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 269e9b4bc2644fae4dc5796652c7587bb0ef6076
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823381"
---
# Registros de eventos de servidor


Las tablas de esta sección proporcionan información acerca de los identificadores de eventos de registro de MBAM Server.

## Configuración


La siguiente tabla contiene mensajes e información de solución de problemas para los identificadores de eventos que pueden producirse en el servidor de MBAM durante la configuración.

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
<th align="left">Id. de evento</th>
<th align="left">Source</th>
<th align="left">Símbolo de evento</th>
<th align="left">Mensaje</th>
<th align="left">Solución de problemas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>103</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Operational</p></td>
<td align="left"><p>VssRegistrationException</p></td>
<td align="left"><p>Se produjo una excepción durante el registro de VSS.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>104</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Operational</p></td>
<td align="left"><p>VssDeregistrationException</p></td>
<td align="left"><p>Se produjo una excepción durante la anulación del registro de VSS.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>300</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>CmdletError</p></td>
<td align="left"><p>Error al quitar la carpeta.</p></td>
<td align="left"><p>Indica que se ha producido un error de terminación al realizar una tarea. Examine otros mensajes de eventos en el registro para diagnosticar más el programa de instalación de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>301</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>cmdletUnexpectedError</p></td>
<td align="left"><p>Error de cmdlet inesperado.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>302</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>CmdletWarning</p></td>
<td align="left"><p>ADVERTENCIA de cmdlet.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>303</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Operational</p></td>
<td align="left"><p>CmdletInformation</p></td>
<td align="left"><p>Información del cmdlet.</p></td>
<td align="left"><p>Solo informativo; no se necesita solución de problemas. El evento indica que los cmdlets están realizando una tarea, como enabling\disabling una característica o cancelando una operación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>400</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ConfiguratorError</p></td>
<td align="left"><p>Error de configurador.</p></td>
<td align="left"><p>Indica que se ha producido un error al iniciar el configurador de MBAM. Asegúrese de que el usuario tiene los privilegios adecuados para iniciar el configurador de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>401</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ConfiguratorUnexpectedError</p></td>
<td align="left"><p>Error inesperado del configurador.</p></td>
<td align="left"><p>Indica que se ha producido un error de terminación al realizar una tarea de configurador de MBAM. El mensaje de error contendrá más detalles sobre el error. Examine otros mensajes de error en el registro de eventos para diagnosticar más el programa de instalación de MBAM. Entre los errores conocidos se incluyen:</p>
<ul>
<li><p>Error al recuperar o validar un certificado seleccionado por el usuario</p></li>
<li><p>Error al analizar la dirección URL de los informes</p></li>
<li><p>Error al abrir registros de eventos para el usuario</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>402</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ConfiguratorWarning</p></td>
<td align="left"><p>ADVERTENCIA del configurador.</p></td>
<td align="left"><p>Indica que una tarea del configurador de MBAM no se ha completado de la forma esperada, pero no ha fallado por completo. Entre las tareas conocidas se incluyen los certificados que faltan en el almacén de LocalMachine\My que se configuró en la característica de aplicación web o un tiempo de espera para una tarea pendiente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>410</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Operational</p></td>
<td align="left"><p>ConfiguratorInformation</p></td>
<td align="left"><p>Información del configurador.</p></td>
<td align="left"><p>Solo informativo; no se necesita solución de problemas. El evento indica que el configurador de MBAM está invocando una tarea. Entre las tareas conocidas se incluyen:</p>
<ul>
<li><p>Iniciar el configurador</p></li>
<li><p>Comprobar los requisitos previos de software para una característica de MBAM</p></li>
<li><p>Validación de parámetros para una característica de MBAM</p></li>
<li><p>Enabling\disabling\committing una característica de MBAM</p></li>
<li><p>Generar un script de PowerShell desde el configurador</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>500</p></td>
<td align="left"><p>Microsoft_Windows_MBAM_Server_Admin</p></td>
<td align="left"><p>WebProviderUnexpectedError</p></td>
<td align="left"><p>Error inesperado en el proveedor de la aplicación Web.</p></td>
<td align="left"><p>Indica que se ha producido un error al habilitar y configurar un sitio web o un servicio Web de MBAM en IIS. Entre los errores conocidos se incluyen:</p>
<ul>
<li><p>Error al buscar la carpeta raíz del WWW de IIS</p></li>
<li><p>Error al acceder a la configuración de IIS en web.config debido a archivos mal formados o a la configuración perdida</p></li>
<li><p>Error al crear o quitar una aplicación Web</p></li>
<li><p>Violación de acceso a IIS</p></li>
</ul>
<p>Este error también se registra si MBAM no puede tener acceso a Active Directory (AD) para validar cuentas de usuario. Compruebe que IIS está instalado, configurado correctamente y que el servicio IIS se está ejecutando. Compruebe que se hayan superado todas las comprobaciones de requisitos previos del software MBAM. Compruebe que el usuario tiene los permisos correctos para crear aplicaciones web en la instancia de IIS. Compruebe que el usuario tiene acceso para leer los objetos de la cuenta de usuario en AD.</p></td>
</tr>
<tr class="even">
<td align="left"><p>501</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>WebProviderError</p></td>
<td align="left"><p>Error inesperado en el proveedor de la aplicación Web.</p></td>
<td align="left"><p>Indica que se ha producido un error al habilitar, deshabilitar o configurar un sitio web MBAM o un servicio Web en IIS. Entre los errores conocidos se incluyen:</p>
<ul>
<li><p>Error al leer la información de enlace básica o WSHttp desde IIS</p></li>
<li><p>Falta la sección identidad o la entrada DNS en la sección de identidad de los archivos de configuración de IIS</p></li>
<li><p>Error al abrir la clave del registro HKLM\SOFTWARE\Microsoft\InetStp</p></li>
<li><p>Error al leer el valor PathWWWRoot de la clave de registro HKLM\SOFTWARE\Microsoft\InetStp</p></li>
<li><p>El usuario está intentando especificar un nombre de directorio virtual con un nombre reservado para MBAM</p></li>
</ul>
<p>Compruebe que IIS está instalado y configurado correctamente. Compruebe que la clave del registro HKLM\SOFTWARE\Microsoft\InetStp: PathWWWRoot existe y es accesible. Compruebe que la información de enlace en IIS no está dañada.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>502</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>WebProviderWarning</p></td>
<td align="left"><p>ADVERTENCIA del proveedor de la aplicación Web.</p></td>
<td align="left"><p>Indica que se ha producido un error de no terminación al habilitar un sitio web o servicio Web de MBAM. Entre los errores conocidos se incluyen:</p>
<ul>
<li><p>Error al acceder a AD para validar el nombre principal de servicio (SPN) en la cuenta del grupo de aplicaciones</p></li>
<li><p>Error al validar el SPN porque está asignado a varias cuentas en AD</p></li>
<li><p>Error al registrar un SPN en la cuenta del grupo de aplicaciones en AD</p></li>
<li><p>El SPN está registrado en una cuenta que no es el grupo de aplicaciones de AD</p></li>
<li><p>Error al quitar SPN de la cuenta del grupo de aplicaciones en AD durante una operación de reversión</p></li>
<li><p>Error al comprobar si se ha concedido al grupo IIS_IUSRS el privilegio de inicio de sesión como lote en el servidor IIS</p></li>
</ul>
<p>El mensaje de evento contendrá más información sobre el error específico. Compruebe que se puede contactar con AD desde el servidor en el que se está ejecutando la instalación de MBAM. Compruebe que el usuario que ejecuta el programa de instalación de MBAM tiene permisos de lectura en la cuenta del grupo de aplicaciones de AD. Si un SPN ya está registrado en la cuenta del grupo de aplicaciones de AD, asegúrese de que no está registrado en otras cuentas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>503</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Operational</p></td>
<td align="left"><p>WebProviderInformation</p></td>
<td align="left"><p>Información del proveedor de la aplicación Web. Texto</p></td>
<td align="left"><p>Solo informativo; no se necesita solución de problemas. El evento indica que el programa de instalación de MBAM está invocando una tarea. Las tareas conocidas incluyen la obtención de configuración de IIS, como la información de enlace y el sitio raíz, y la configuración del nombre principal de servicio (SPN).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>600</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupUnexpectedError</p></td>
<td align="left"><p>Error de instalación inesperado.</p></td>
<td align="left"><p>Indica que se ha producido un error de terminación al enabling\disabling o configurar una característica de MBAM. Entre los errores conocidos se incluyen:</p>
<ul>
<li><p>Error al revertir una tarea después de un error</p></li>
<li><p>Error al leer del registro</p></li>
<li><p>Error al crear o eliminar una carpeta en el sistema de archivos</p></li>
<li><p>Error al leer la información de versión de SQL</p></li>
<li><p>Error al registrar VSS Writer en SQL</p></li>
</ul>
<p>El mensaje de evento contendrá más información sobre el error específico. Compruebe que se superan todas las comprobaciones de requisitos previos del software MBAM. Asegúrese de que la ruta de acceso del registro MBAM, si existe, HKEY_LOCAL_MACHINE servidor de \SOFTWARE\Microsoft\MBAM y que todas las subclaves sean legibles. Compruebe que se puede contactar con AD desde el servidor en el que se está ejecutando la instalación de MBAM. Compruebe que el usuario que ejecuta el programa de instalación de MBAM tiene permisos de lectura en AD.</p>
<p>Para un registro de VSS Writer satisfactorio, compruebe que está instalada una versión compatible de SQL y que el usuario que ejecuta el programa de instalación de MBAM puede acceder a una instancia. Si deshabilita una característica de MBAM o desinstala MBAM Compruebe que todos los archivos, como los archivos de registro y los archivos de web.config están cerrados, de modo MBAM puede quitar sus sitios web y servicios Web.</p></td>
</tr>
<tr class="even">
<td align="left"><p>601</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupError</p></td>
<td align="left"><p>Error de instalación.</p></td>
<td align="left"><p>Indica que se ha producido un error de terminación al enabling\disabling o configurar una característica de MBAM. Entre los errores conocidos se incluyen:</p>
<ul>
<li><p>Error al leer la configuración de MBAM en IIS</p></li>
<li><p>Sección appSettings dañada en configuración de IIS o configuración mal configurada</p></li>
<li><p>Error al validar el nombre de host</p></li>
<li><p>Error al leer la información de versión de SQL</p></li>
<li><p>Error al registrar VSS Writer en SQL</p></li>
</ul>
<p>El mensaje de evento contendrá más información sobre el error específico. Compruebe que IIS está instalado y configurado correctamente. Compruebe que se superan todas las comprobaciones de requisitos previos del software MBAM. Para un registro de VSS Writer satisfactorio, compruebe que está instalada una versión compatible de SQL y que el usuario que ejecuta el programa de instalación de MBAM puede acceder a una instancia.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>602</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupWarning</p></td>
<td align="left"><p>ADVERTENCIA de configuración.</p></td>
<td align="left"><p>Indica que se ha producido un error de no terminación al enabling\disabling o configurar una característica de MBAM, como la integración de Configuration Manager (CM) o la aplicación Web de MBAM. Entre los errores conocidos se incluyen: error al eliminar los informes de MBAM desde el punto de función de SRS en el CM y no se puede resolver un nombre de host desde el controlador de dominio. El mensaje de evento contendrá más información sobre el error específico.</p>
<p>Compruebe que se puede contactar con AD desde el servidor en el que se está ejecutando la instalación de MBAM. Compruebe que el usuario que ejecuta el programa de instalación de MBAM tiene permisos para quitar la instancia de SSRS que está configurada como punto de función SRS en CM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>603</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Operational</p></td>
<td align="left"><p>SetupInformation</p></td>
<td align="left"><p>Información de configuración.</p></td>
<td align="left"><p>Solo informativo; no se necesita solución de problemas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>605</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>WebProviderSoftwareCheckFailure</p></td>
<td align="left"><p>No se puede habilitar la aplicación web porque no se cumplen una o más dependencias de software.</p></td>
<td align="left"><p>Durante la instalación de MBAM sitio web/servicio Web, MBAM comprueba si los requisitos previos necesarios están en vigor. Este mensaje indica que MBAM no pudo instalar el sitio web o el servicio Web solicitado porque falta el requisito previo necesario. Consulte mensajes de error anteriores a este mensaje para obtener más información sobre los requisitos previos que faltan.</p></td>
</tr>
<tr class="even">
<td align="left"><p>606</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupParameterValidationFailure</p></td>
<td align="left"><p>El parámetro necesario para habilitar la característica de servidor no se especificó o no pasó la validación.</p></td>
<td align="left"><p>Indica que el parámetro necesario para configurar una característica de MBAM no se especificó o no pasó la validación.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>607</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>SetupParameterValidationFailureWithError</p></td>
<td align="left"><p>Error al intentar validar el parámetro especificado necesario para habilitar la característica de servidor.</p></td>
<td align="left"><p>Indica que se detectó un error al intentar validar el parámetro especificado que se necesita para habilitar la característica de servidor.</p></td>
</tr>
<tr class="even">
<td align="left"><p>700</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderUnexpectedError</p></td>
<td align="left"><p>Error inesperado de proveedor de base de BD.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>701</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderError</p></td>
<td align="left"><p>Error de proveedor de BD.</p></td>
<td align="left"><p>El mensaje contenido en la sección EventDetails debe proporcionar más información sobre el error real. Estas son algunas de las áreas que hay que comprobar:</p>
<ul>
<li><p>El programa de instalación de MBAM no se pudo conectar a la base de datos con la información de conexión proporcionada. Compruebe los detalles de la cadena de conexión proporcionados a la instalación de MBAM.</p></li>
<li><p>El programa de instalación de MBAM no se pudo conectar a la base de datos proporcionada mediante las credenciales de cuenta de dominio proporcionadas. Compruebe que el nombre de usuario y la contraseña de la cuenta de dominio sean válidos.</p></li>
<li><p>El programa de instalación de MBAM no se pudo conectar a la base de datos proporcionada mediante las credenciales de cuenta de dominio proporcionadas. Compruebe que la cuenta de dominio proporcionada tiene los permisos necesarios para conectarse a la base de datos de MBAM.</p></li>
<li><p>MBAM DAC PAC fallará si ya hay instalada una versión más reciente de MBAM base de datos. Compruebe que no existe una nueva versión de MBAM DBs en el servidor SQL Server dado.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>702</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderWarning</p></td>
<td align="left"><p>ADVERTENCIA de proveedor de base de BD.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>703</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Operational</p></td>
<td align="left"><p>DbProviderInformation</p></td>
<td align="left"><p>Información de proveedor de BD.</p></td>
<td align="left"><p>Solo informativo; no se necesita solución de problemas.</p></td>
</tr>
<tr class="even">
<td align="left"><p>704</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderDacError</p></td>
<td align="left"><p>Se produjo un error al implementar la aplicación de capa de datos.</p></td>
<td align="left"><p>MBAM empaqueta sus bases de datos como aplicaciones de capa de datos e intenta registrarlas con Microsoft. SqlServer. DAC. DacServices. El mensaje de error en contexto es notificado por el servicio DAC. El evento debe contener información detallada sobre lo que causó. Lea la información del mensaje de error para solucionar y corregir el problema.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>705</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>DbProviderDacWarning</p></td>
<td align="left"><p>Se produjo una advertencia al implementar la aplicación de capa de datos.</p></td>
<td align="left"><p>MBAM empaqueta sus bases de datos como aplicación de capa de datos e intenta registrarlas con Microsoft. SqlServer. DAC. DacServices. El servicio DAC notifica el mensaje de advertencia en contexto. El evento debe contener información detallada sobre lo que causó. Lea la información del mensaje de advertencia para solucionar y corregir el problema.</p></td>
</tr>
<tr class="even">
<td align="left"><p>706</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Operational</p></td>
<td align="left"><p>DbProviderDacInformation</p></td>
<td align="left"><p>Se generó un mensaje al implementar la aplicación de capa de datos.</p></td>
<td align="left"><p>Solo informativo; no se necesita solución de problemas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>800</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ReportProviderUnexpectedError</p></td>
<td align="left"><p>Error inesperado del proveedor de informes.</p></td>
<td align="left"><p>Error inesperado del proveedor de informes. Texto {exceptionDetails} Estos son algunos de los posibles detalles de la excepción:</p>
<p><strong>Se produjo un error al obtener el nombre del directorio &#39; {directoryName} &#39;</strong></p>
<p><strong>Se produjo una excepción al obtener archivos para el directorio &#39; {directoryName} &#39;</strong></p>
<p><strong>Se produjo una excepción al enumerar los directorios en el directorio &#39; {directoryName} &#39;</strong></p>
<p><strong>Se produjo una excepción al leer todos los bytes del archivo &#39; {fileName} &#39;</strong></p>
<p>Durante la instalación de MBAM, el programa de instalación de MBAM descomprime todos los archivos de informe en la ruta de instalación especificada. Como parte de la instalación de informes, el módulo de instalación intenta acceder a los archivos de informe descomprimidos en la ruta de instalación y se comunica con SQL Reporting Services para publicar los archivos de informe. Los errores anteriores se producen cuando MBAM no puede acceder a los archivos o carpetas en la ruta de instalación descomprimida. Estas son algunas sugerencias para solucionar este problema:</p>
<ul>
<li><p>Verifique que MBAM esté instalado.</p></li>
<li><p>Compruebe que el usuario que ejecuta la aplicación RegKey HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\InstallationPath está presente y es accesible para él.</p></li>
<li><p>Compruebe que la ruta de acceso a los archivos de informe en MBAM InstallationPath no supere 248 caracteres.</p></li>
<li><p>Compruebe que la carpeta de instalación de MBAM o los archivos contenidos en MBAM no se han modificado desde la instalación.</p></li>
<li><p>Compruebe que el usuario que ejecuta la configuración está autorizado para leer o escribir en la carpeta de instalación MBAM.</p></li>
</ul>
<p><strong>Error en la conectividad de Reporting Services. {exceptionDetails}</strong></p>
<p>Durante la instalación de MBAM informes, los módulos intentan comunicarse con los servicios Web de SSRS para crear carpetas y publicar informes. El mensaje anterior indica que MBAM no pudo encontrar ni comunicarse con los servicios Web de SSRS. Estas son algunas sugerencias para solucionar este problema:</p>
<ul>
<li><p>Comprobar que SSRS está instalado en el equipo especificado.</p></li>
<li><p>Con la consola de SSRS, compruebe que SSRS está habilitado y se está ejecutando.</p></li>
<li><p>Comprobar que el usuario que ejecuta la configuración está autorizado para acceder a SSRS.</p></li>
</ul>
<p><strong>Error al quitar los informes de MBAM con la dirección URL de la instancia de Reporting Services &#39; {SSRSInstanceUrl} &#39;. Asegúrese de que la instancia de SSRS necesaria para los informes de MBAM se esté ejecutando y esté configurada correctamente.</strong></p>
<p>Cuando se produce un error en la instalación de MBAM o el usuario deshabilita las características de informes de MBAM, el módulo de instalación quita los informes de SSRS. El mensaje anterior indica que MBAM no pudo quitar los informes de SSRS. Estas son algunas sugerencias para solucionar este problema:</p>
<ul>
<li><p>Comprobar que SSRS está instalado en el equipo especificado.</p></li>
<li><p>Con la consola de SSRS, compruebe que SSRS está habilitado y se está ejecutando.</p></li>
<li><p>Compruebe que el usuario que ejecuta la configuración tiene autorización para acceder a SSRS.</p></li>
</ul>
<p><strong>Se produjo un error durante la publicación de informes. {exceptionDetails}.</strong></p>
<p>Durante la instalación de MBAM informes, los módulos intentan comunicarse con los servicios Web de SSRS para crear carpetas y publicar informes. El mensaje anterior indica que el servicio Web de SSRS informó de un informe y una excepción durante la publicación de informes. Estas son algunas sugerencias para solucionar este problema:</p>
<ul>
<li><p>Con la consola de SSRS, compruebe que SSRS está habilitado y se está ejecutando.</p></li>
<li><p>Compruebe que el usuario que ejecuta la configuración está autorizado para acceder a los informes y publicarlos en SSRS.</p></li>
</ul>
<p><strong>Ya existe una directiva para el nombre de usuario de grupo &#39; {nombreusuario} &#39;. En caso de que no sea correcta, revise manualmente el servicio de informes para las directivas duplicadas o no válidas.</strong></p>
<p>Después de publicar los informes de MBAM, el programa de instalación de MBAM intenta crear un MBAM notificar a los usuarios los roles (si todavía no existe) y establece la Directiva de usuario correspondiente. El error anterior indica que el servicio Web de SSRS produjo una excepción al configurar la Directiva de rol de usuario de informes. Siga las instrucciones del mensaje de evento y consulte &quot; <a href="https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp;ProdVer=8.00&amp;EvtID=rsInvalidPolicyDefinition&amp;EvtSrc=Microsoft.ReportingServices.Diagnostics.ErrorStrings.resources.Strings&amp;LCID=1033&amp;quot" data-raw-source="https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp;amp;ProdVer=8.00&amp;amp;EvtID=rsInvalidPolicyDefinition&amp;amp;EvtSrc=Microsoft.ReportingServices.Diagnostics.ErrorStrings.resources.Strings&amp;amp;LCID=1033&amp;quot"> https://www.microsoft.com/technet/support/ee/transform.aspx?ProdName=SQL+Server+Reporting+Services&amp ; ProdVer = 8.00 &amp; EvtID = rsInvalidPolicyDefinition &amp; EvtSrc = Microsoft. ReportingServices. Diagnostics. errorStrings. Resources. Strings: &amp; 1033&quot </a> ; para obtener más ayuda.</p>
<p><strong>Se produjo un error al validar el acceso a SSRS {exceptionDetails}.</strong></p>
<p>Como parte de la comprobación de requisitos previos, MBAM el programa de instalación verifica si el usuario tiene los permisos necesarios para obtener acceso a la carpeta o crear una carpeta en SSRS. El mensaje de error indica que se ha producido una excepción al comprobar el acceso a SSRS. Consulte los detalles de la excepción para obtener sugerencias de depuración.</p>
<p><strong>Se produjo un error de SOAP al comprobar la dirección URL de SSRS. {exceptionDetails}</strong></p>
<p><strong>Se produjo un error Web al comprobar la dirección URL de SSRS. {exceptionDetails}</strong></p>
<p><strong>Se produjo un error de http/https al comprobar la dirección URL de SSRS. {exceptionDetails}</strong></p>
<p><strong>Se produjo un error al comprobar la dirección URL de SSRS. {exceptionDetails}</strong></p>
<p>Como parte de la comprobación de requisitos previos, MBAM el programa de instalación recupera las direcciones URL asociadas a la instancia de SSRS proporcionada e intenta comunicarse con el servicio Web de SSRS. El mensaje de error anterior indica que el servicio Web de SSRS en la dirección URL dada ha producido una excepción, consulte los detalles de la excepción para obtener más información. Estas son algunas sugerencias para resolver problemas de comunicación de SSRS.</p>
<ul>
<li><p>Comprobar que SSRS está instalado en el equipo especificado.</p></li>
<li><p>Con la consola de SSRS, compruebe que SSRS está habilitado y se está ejecutando.</p></li>
<li><p>Compruebe que el usuario que ejecuta la configuración tiene autorización para acceder a SSRS.</p></li>
</ul>
<p><strong>Se produjo un error al recuperar la versión de SSRS. {exceptionDetails}</strong></p>
<p>Como parte de la comprobación de requisitos previos, la configuración de MBAM consulta a WMI para recuperar el número de versión asociado a la instancia de SSRS proporcionada. El mensaje de error anterior indica que se produjo una excepción al consultar WMI. Para obtener más información, consulta exceptionDetails. Estas son algunas de las comprobaciones que puede realizar:</p>
<ul>
<li><p>Compruebe que SSRS con el nombre de instancia dado está instalado en el equipo especificado.</p></li>
<li><p>Con la consola de SSRS, compruebe que SSRS está habilitado y se está ejecutando.</p></li>
<li><p>Compruebe que el usuario que ejecuta la configuración está autorizado para consultar la clase SSRS en el espacio de nombres WMI.</p></li>
</ul>
<p><strong>El usuario actual no tiene autorización para acceder al espacio de nombres WMI &#39; {ssrsWMINamespace} &#39;.</strong></p>
<p><strong>Se produjo un error al enumerar el espacio de nombres &#39; {ssrsWMINamespace} &#39;. No se encuentra el servidor RPC para SSRS proveedor WMI en el host local.</strong></p>
<p><strong>Se produjo un error al enumerar el espacio de nombres &#39; {ssrsNamespace} &#39;. No se puede encontrar una instancia de SSRS en el host local.</strong></p>
<p><strong>Se produjo un error al acceder a WMI. No se encontró el servidor RPC para la instancia &#39; {ssrsInstance} &#39;.</strong></p>
<p><strong>Se produjo un error al acceder a WMI. El nombre de instancia &#39; {ssrsInstanceName} &#39; no es correcto.</strong></p>
<p><strong>Se produjo un error al acceder a WMI. No se puede encontrar la instancia &#39; {ssrsInstanceName} &#39; en el host local.</strong></p>
<p>Como parte de la comprobación de requisitos previos, la configuración de MBAM consulta a WMI para recuperar el espacio de nombres WMI asociado a la instancia dada. El mensaje de error anterior indica que se ha producido una excepción al consultar WMI. Para obtener más información, consulta exceptionDetails. Estas son algunas de las comprobaciones que puede realizar:</p>
<ul>
<li><p>Compruebe que SSRS con el nombre de instancia dado está instalado en el equipo especificado.</p></li>
<li><p>Con la consola de SSRS, compruebe que SSRS está habilitado y se está ejecutando.</p></li>
<li><p>Compruebe que el usuario que ejecuta la configuración está autorizado para acceder/consultar la clase SSRS en el espacio de nombres WMI.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>801</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ReportProviderError</p></td>
<td align="left"><p>Error inesperado del proveedor de informes.</p></td>
<td align="left"><p>Dado el nombre de instancia de SQL Server Reporting Services, MBAM intenta encontrar el espacio de nombres WMI correspondiente a la instancia de informes y conectarse a él. Este error se produce si MBAM encuentra una excepción cuando MBAM busca o intenta conectar con el espacio de nombres WMI de SSRS. Lea la información de los mensajes de error que se han registrado en el canal de instalación de MBAM antes de este mensaje para obtener más información. Estas son algunas de las cosas que puede comprobar:</p>
<ul>
<li><p>Comprobar que SSRS con el nombre de instancia proporcionado está activo y ejecutándose</p></li>
<li><p>Compruebe que la cuenta de usuario con la instalación de MBAM tiene los permisos necesarios para consultar/conectar al espacio de nombres WMI de SSRS</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>802</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>ReportProviderWarning</p></td>
<td align="left"><p>ADVERTENCIA del proveedor de informes.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>803</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Operational</p></td>
<td align="left"><p>ReportProviderInformation</p></td>
<td align="left"><p>Información del proveedor de informes.</p></td>
<td align="left"><p>Solo informativo; no se necesita solución de problemas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>900</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>CMProviderUnexpectedError</p></td>
<td align="left"><p>Error inesperado del proveedor de CM.</p></td>
<td align="left"><p>Indica que se ha producido un error de terminación al enabling\disabling o configurar la característica de integración de Configuration Manager (CM) en MBAM. Entre los errores conocidos se incluyen:</p>
<ul>
<li><p>Error al conectar con el servidor de sitio de CM a través del proveedor de SMS</p></li>
<li><p>Error al leer del registro</p></li>
<li><p>Error al crear o eliminar una carpeta en el sistema de archivos</p></li>
<li><p>Error al ubicar la instalación de la consola de Configuration Manager en la máquina local</p></li>
<li><p>Error al recuperar información para la instancia de SSRS que está configurada como punto de función SRS en CM</p></li>
</ul>
<p>El mensaje de evento contendrá más información sobre el error específico. Compruebe que se superan todas las comprobaciones de requisitos previos del software MBAM. Compruebe que la ruta de acceso del registro MBAM, si existe, HKEY_LOCAL_MACHINE servidor de \SOFTWARE\Microsoft\MBAM y que todas las subclaves sean legibles. Compruebe que MBAM se ha integrado con una versión compatible de Configuration Manager. Compruebe que la consola de Configuration Manager está instalada en el equipo en el que se invoca la configuración de MBAM y que la consola se puede usar para conectarse al servidor de sitio de CM de destino. Compruebe que haya una instancia de SSRS válida configurada como punto de función SRS en CM y que el usuario que ejecuta el programa de instalación de MBAM tiene permisos de read\write en la instancia de SSRS.</p></td>
</tr>
<tr class="even">
<td align="left"><p>901</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Admin</p></td>
<td align="left"><p>CMProviderError</p></td>
<td align="left"><p>Error inesperado del proveedor de CM.</p></td>
<td align="left"><p>Indica que se ha producido un error de terminación al enabling\disabling o configurar la característica de integración de Configuration Manager (CM) en MBAM. Entre los errores conocidos se incluyen:</p>
<ul>
<li><p>Error al conectar con el servidor de sitio de CM a través del proveedor de SMS</p></li>
<li><p>Error al leer del registro</p></li>
<li><p>Error al crear o eliminar una carpeta en el sistema de archivos</p></li>
<li><p>Error al ubicar la instalación de la consola de Configuration Manager en la máquina local</p></li>
<li><p>falta la carpeta de ConfigMgr en SSRS como la carpeta raíz para los informes de punto de función SRS</p></li>
<li><p>origen de datos compartido de ConfigMgr ausente en SSRS</p></li>
<li><p>Error al implementar informes de SSRS en la instancia de SSRS que está configurada como un punto de función SRS en CM</p></li>
<li><p>Error al crear elementos de configuración y líneas de base en CM</p></li>
</ul>
<p>El mensaje de evento contendrá más información sobre el error específico. Compruebe que se superan todas las comprobaciones de requisitos previos del software MBAM. Compruebe que la ruta de acceso del registro MBAM, si existe, HKEY_LOCAL_MACHINE servidor de \SOFTWARE\Microsoft\MBAM y que todas las subclaves sean legibles. Compruebe que MBAM se ha integrado con una versión compatible de Configuration Manager. Compruebe que la consola de Configuration Manager está instalada en el equipo en el que se invoca la configuración de MBAM y que la consola se puede usar para conectarse al servidor de sitio de CM de destino. Compruebe que el usuario tiene los permisos de read\write necesarios para crear elementos de configuración, líneas de base y colecciones en CM. Compruebe que haya una instancia de SSRS válida configurada como punto de función SRS en CM y que el usuario que ejecuta el programa de instalación de MBAM tiene permisos de read\write en la instancia de SSRS.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>902</p></td>
<td align="left"><p>Microsoft_Windows_MBAM_Server_Admin</p></td>
<td align="left"><p>CMProviderWarning</p></td>
<td align="left"><p>ADVERTENCIA de proveedor de CM.</p></td>
<td align="left"><p>Indica que se ha producido un error de no terminación al habilitar la característica de integración de Configuration Manager (CM). Entre los errores conocidos se incluyen: no se pueden confirmar las reglas de recopilación en la colección de equipos compatibles MBAM en CM y otros SSRS y errores relacionados con la red.</p>
<p>El mensaje de evento contendrá más información sobre el error específico. Algunas de las operaciones que provocaron esta advertencia se retirarán después de la advertencia. Si después de varios intentos persiste el error, MBAM podría finalizar con un error real. Examine otros mensajes de eventos en el registro para diagnosticar más el programa de instalación de MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>903</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-Server/Operational</p></td>
<td align="left"><p>CMProviderInformation</p></td>
<td align="left"><p>Información del proveedor de CM.</p></td>
<td align="left"><p>Solo informativo; no se necesita solución de problemas.</p></td>
</tr>
</tbody>
</table>

 

## Operación


La tabla siguiente contiene mensajes e información de solución de problemas para los identificadores de eventos que se pueden producir mientras se ejecuta MBAM.

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
<th align="left">Id. de evento</th>
<th align="left">Source</th>
<th align="left">Símbolo de evento</th>
<th align="left">Mensaje</th>
<th align="left">Solución de problemas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>uno</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>WebAppSpnError</p></td>
<td align="left"><p>Aplicación: {SiteName} {VirtualDirectory} no tiene los siguientes nombres principales de servicio (SPN): {ListOfSpns} registrar los SPN necesarios en la cuenta: {ExecutionAccount}.</p></td>
<td align="left"><p>Para que la autenticación integrada de Windows funcione correctamente, es necesario disponer de SPN. Este mensaje indica que el SPN necesario para la aplicación MBAM no se ha configurado correctamente. Los detalles contenidos en este evento deben proporcionar más información.</p>
<p>Para obtener más información, vea "nombre principal de servicio (SPN)" en los <a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md#bkmk-prereqsams" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md#bkmk-prereqsams)"> requisitos previos del servidor de MBAM 2,5 para topologías de integración de administrador independiente y de configuración </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>cuatro</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/Operational</p></td>
<td align="left"><p>PerformanceCounterError</p></td>
<td align="left"><p>Se produjo un error al recuperar un contador de rendimiento.</p>
<p>Mensaje: {EventMessage} Categoría: {CategoryOfPerformanceCounter} contador de rendimiento: {NameOfPerformanceCounter} instancia: {nombre de instancia de categoría de contador de rendimiento} excepción: {ExceptionThrown}</p>
<p>El mensaje de seguimiento contendrá el mensaje de excepción real, algunos de los cuales se explican aquí:</p>
<p><strong>ArgumentNullException </strong> : esta excepción se produce si la categoría, el contador o la instancia del contador de rendimiento solicitado no es válido.</p>
<p><strong>System. InvalidOperationException </strong> : categoryName es una cadena vacía ( &quot; &quot; ) o es una cadena vacía ( &quot; &quot; ).</p>
<p>-o bien-la configuración de los permisos de lectura y escritura solicitada no es válida para este contador.</p>
<p>-o bien-la categoría especificada no existe (si readOnly es true).</p>
<p>-o bien-la categoría especificada no es una categoría personalizada de .NET Framework (si readOnly es false).</p>
<p>-o bien-la categoría especificada se marca como de varias instancias y requiere que se cree el contador de rendimiento con un nombre de instancia.</p>
<p>-o-instanceName es superior a 127 caracteres.</p>
<p>-o-categoryName y ennombre se han localizado en diferentes idiomas.</p>
<p><strong>System. ComponentModel. Win32Exception </strong> : se ha producido un error al acceder a una API del sistema.</p>
<p><strong>System. PlatformNotSupportedException </strong> : la plataforma es windows 98 o Windows Millennium Edition (me), que no admite los contadores de rendimiento.</p>
<p><strong>System. UnauthorizedAccessException </strong> : el código que se ejecuta sin privilegios de administrador intentó leer un contador de rendimiento.</p></td>
<td align="left"><p>El mensaje contenido en el evento proporcionará más información sobre la excepción que se ha iniciado. Si se inició una excepción System. UnauthorizedAccessException, compruebe que la cuenta de ejecución de MBAM (grupo de aplicaciones) tenga acceso a las API de los contadores de rendimiento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>100</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>AdminServiceRecoveryDbError</p></td>
<td align="left"><p><strong>GetMachineUsers </strong> : se produjo un error al obtener la información de usuario de la base de datos. Mensaje: {Message}-o bien-</p>
<p><strong>GetRecoveryKey </strong> : se produjo un error al obtener la clave de recuperación de la base de datos. Mensaje: {Message}-o bien-</p>
<p><strong>GetRecoveryKey </strong> : se produjo un error al obtener la información de usuario de la base de datos. Mensaje: {Message}-o bien-</p>
<p><strong>GetRecoveryKeyIds </strong> : se produjo un error al obtener los identificadores de clave de recuperación de la base de datos. Mensaje: {Message}-o bien-</p>
<p><strong>GetTpmHashForUser </strong> : se produjo un error al obtener datos hash de TPM de la base de datos de recuperación. Mensaje: {Message}-o bien-</p>
<p><strong>GetTpmHashForUser </strong> : se produjo un error al obtener datos hash de TPM de la base de datos de recuperación. Mensaje: {Message}-o bien-</p>
<p><strong>QueryDriveRecoveryData </strong> : se produjo un error al obtener datos de recuperación de unidades de la base de datos. Mensaje: {Message}-o bien-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : se produjo un error al obtener los identificadores de clave de recuperación de la base de datos. Mensaje: {Message}-o bien-</p>
<p><strong>QueryVolumeUsers </strong> : se produjo un error al obtener la información de usuario de la base de datos.</p></td>
<td align="left"><p>Este mensaje se registra siempre que se produce una excepción al comunicarte con la base de datos de recuperación de MBAM. Lea la información contenida en el seguimiento para obtener detalles específicos sobre la excepción.</p>
<p>Para obtener instrucciones detalladas para la solución de problemas, consulte el artículo de TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> sobre cómo solucionar problemas de conexión con el motor de base de datos de SQL Server </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>101</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>AdminServiceComplianceDbError</p></td>
<td align="left"><p><strong>GetRecoveryKey </strong> : se produjo un error al registrar un evento de auditoría en la base de datos de cumplimiento. Mensaje: {Message}-o bien-</p>
<p><strong>GetRecoveryKeyIds </strong> : se produjo un error al registrar un evento de auditoría en la base de datos de cumplimiento. Mensaje: {Message}-o bien-</p>
<p><strong>GetTpmHashForUser </strong> : se produjo un error al registrar un evento de auditoría en la base de datos de cumplimiento. Mensaje: {Message}-o bien-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : se produjo un error al registrar un evento de auditoría en la base de datos de cumplimiento. Mensaje: {Message}-o bien-</p>
<p><strong>QueryDriveRecoveryData </strong> : se produjo un error al registrar un evento de auditoría en la base de datos de cumplimiento. Mensaje: {mensaje}</p></td>
<td align="left"><p>Este mensaje se registra siempre que se produce una excepción al comunicar la base de datos de cumplimiento de MBAM. Lea la información contenida en el seguimiento para obtener detalles específicos sobre la excepción.</p>
<p>Para obtener instrucciones detalladas para la solución de problemas, consulte el artículo de TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> sobre cómo solucionar problemas de conexión con el motor de base de datos de SQL Server </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>102</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>AgentServiceRecoveryDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Este mensaje indica una excepción cuando el servicio agente de MBAM intenta comunicarse con la base de datos de recuperación. Lea el mensaje contenido en el evento para obtener información específica sobre la excepción.</p>
<p>Consulte el artículo de TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> sobre cómo solucionar problemas de conexión al motor de base de datos de SQL Server </a> para comprobar si la cuenta del grupo de aplicaciones MBAM tiene los permisos necesarios para conectarse o ejecutar en MBAM base de datos de recuperación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>103</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>AgentServiceError</p></td>
<td align="left"><p>No se puede detectar la cuenta del equipo cliente ni la cuenta de usuario de migración de datos. O bien</p>
<p>Error en la verificación de cuenta para la identidad del autor de la llamada.</p></td>
<td align="left"><p>Cada vez que se realiza una llamada a los &quot; &quot; &quot; métodos Web PostKeyRecoveryInfo, IsRecoveryKeyResetRequired &quot; , &quot; COMMITRECOVERYKEYREST &quot; o &quot; GetTpmHash &quot; Web en MBAM servicios de agente, se recupera el contexto de llamada para obtener las credenciales de la llamada. Si el contexto de la llamada es null o está vacío, el servicio del agente MBAM &quot; no puede detectar la cuenta del equipo cliente ni la cuenta de usuario de migración de datos.&quot;</p>
<p>El mensaje &quot; no se pudo comprobar la identidad de la persona que llama &quot; si el método Web espera que la persona que llama se registre en una cuenta de equipo y la persona que llama no es una cuenta de equipo, o si el método Web está excepto que la persona que llama es una cuenta de usuario y la persona que llama no es una cuenta de usuario ni miembro de la cuenta de grupo de migración</p></td>
</tr>
<tr class="odd">
<td align="left"><p>104</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>StatusServiceComplianceDbConfigError</p></td>
<td align="left"><p>&quot;La cadena de conexión de la base de datos de cumplimiento del registro está vacía.&quot;</p></td>
<td align="left"><p>Este mensaje se registra cuando la cadena de conexión de BD de cumplimiento no es válida.</p>
<p>Compruebe el valor de la clave de registro HKLM\Software\Microsoft\MBAM Server\Web\ComplianceDBConnectionString</p></td>
</tr>
<tr class="even">
<td align="left"><p>105</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>StatusServiceComplianceDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Este error indica que los sitios web de MBAM/Web Services no pudieron conectarse a la base de datos de MBAMCompliance.</p>
<p>Consulte el artículo de TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> sobre cómo solucionar problemas de conexión al motor de base de datos de SQL Server </a> para comprobar que la cuenta del grupo de aplicaciones de IIS podría conectarse a la base de datos de cumplimiento de MBAM.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>106</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>HelpdeskError</p></td>
<td align="left"><p>La solicitud a la dirección URL {URL} causó un error interno. O bien</p>
<p>Se produjo un error al obtener información de contexto de ejecución. No se puede comprobar el registro del nombre principal de servicio (SPN). O bien</p>
<p>Se produjo un error al comprobar el registro de nombre principal de servicio (SPN).</p></td>
<td align="left"><p>Indica que se ha producido una excepción no controlada en la aplicación del Departamento de soporte técnico. Revise las entradas del registro en el canal operativo del administrador de MBAM para buscar la excepción específica. ni</p>
<p>Durante la operación de carga del sitio web del servicio de asistencia inicial, se realiza una comprobación SPN. Para comprobar el SPN, el Departamento de soporte técnico requiere información de la cuenta de ejecución, el Nombresitio de IIS y ApplicationVirtualPath correspondiente al sitio web del Departamento de soporte. Este mensaje de error se registra cuando una o más de estas opciones no son válidas o no están disponibles. ni</p>
<p>Este mensaje indica que se produce una excepción de seguridad al realizar la verificación SPN. Consulte la excepción incluida en la sección Detalles del evento.</p></td>
</tr>
<tr class="even">
<td align="left"><p>107</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>SelfServicePortalError</p></td>
<td align="left"><p>Se produjo un error al obtener la clave de recuperación de un usuario. EventDetails: {ExceptionMessage}-o bien-</p>
<p>Se produjo un error al obtener información de contexto de ejecución. No se puede comprobar el registro del nombre principal de servicio (SPN). EventDetails: usuario: {username Identity} aplicación: {SiteName\ApplicationVirtualPath}-o bien-</p>
<p>Se produjo un error al comprobar el registro de nombre principal de servicio (SPN). EventDetails:{ExceptionMessage}</p></td>
<td align="left"><p>Indica que se ha producido una excepción inesperada cuando se realizó una solicitud para recuperar la clave de recuperación. Consulte el mensaje de excepción incluido en la sección Detalles del evento. Si la traza está habilitada en MBAM Helpdesk, consulte datos de seguimiento para obtener mensajes de excepción detallados. ni</p>
<p>Durante una operación de carga inicial, el portal de autoservicio (SSP) recupera la información de la cuenta de ejecución, los archivos de configuración de IIS siteName y ApplicationVirtualPath correspondiente al sitio web de autoservicio para comprobar el SPN. Este mensaje de error se registra cuando uno o más de los siguientes no son válidos. ni</p>
<p>Este mensaje indica que se ha producido una excepción de seguridad al realizar la verificación SPN. Consulte la excepción incluida en la sección Detalles del evento.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>108</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>DomainControllerError</p></td>
<td align="left"><p>Se produjo un error al resolver el nombre de dominio {DomainName}, se produjo un error de asignación de memoria. O bien</p>
<p>No se pudo invocar el método DsGetDcName. EventDetails:{ExceptionMessage}</p></td>
<td align="left"><p>Para resolver el nombre de dominio, MBAM aprovecha la &quot; API de Windows de DsGetDcName &quot; . Este mensaje se registra cuando &quot; DsGetDcName &quot; devuelve &quot; ERROR_NOT_ENOUGH_MEMORY &quot; que indica un error de asignación de memoria. ni</p>
<p>Este mensaje indica que &quot; &quot; el método API de DsGetDcName no está disponible en el sistema de hospedaje.</p></td>
</tr>
<tr class="even">
<td align="left"><p>109</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>WebAppRecoveryDbError</p></td>
<td align="left"><p>Error al leer la configuración de la base de datos de recuperación. La cadena de conexión a la base de datos de recuperación no está configurada. Mensaje: {Message}-o bien-</p>
<p><strong>DoesUserHaveMatchingRecoveryKey </strong> : se produjo un error al obtener los identificadores de clave de recuperación de un usuario. Mensaje: {Message}-o bien-</p>
<p><strong>QueryDriveRecoveryData </strong> : se produjo un error al obtener los datos de recuperación de la unidad. Mensaje: {Message}-o bien-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : se produjo un error al obtener los identificadores de clave de recuperación de un usuario. Mensaje: {Message}-o bien-</p>
<p>Se produjo un error al obtener el hash de contraseña de TPM de la base de datos de recuperación. EventDetails:{ExceptionMessage}</p></td>
<td align="left"><p>Este mensaje indica que la información de la cadena de conexión de la base de datos de recuperación en &quot; HKLM\Software\Microsoft\MBAM Server\Web\RecoveryDBConnectionString &quot; no es válida. Comprobar el valor de la clave de registro especificada. ni</p>
<p>Si se registra alguno de los mensajes restantes, consulte los pasos de solución de problemas que aparecen en el artículo de TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> sobre cómo solucionar problemas de conexión al motor de base de datos de SQL Server </a> para comprobar si se puede establecer una conexión con la base de datos de recuperación de MBAM desde el servidor de IIS mediante credenciales del grupo de aplicaciones.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>110</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>WebAppComplianceDbError</p></td>
<td align="left"><p>Error al leer la configuración de la base de datos de cumplimiento. La cadena de conexión a la base de datos de cumplimiento no está configurada. O bien</p>
<p><strong>GetRecoveryKeyForCurrentUser </strong> : se produjo un error al registrar un evento de auditoría en la base de datos de cumplimiento. Mensaje: {Message}-o bien-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : se produjo un error al registrar un evento de auditoría en la base de datos de cumplimiento. Mensaje: {Message}-o bien-</p>
<p><strong>QueryRecoveryKeyIdsForUser </strong> : se produjo un error al registrar un evento de auditoría en la base de datos de cumplimiento. Mensaje: {mensaje}</p></td>
<td align="left"><p>Este mensaje indica que la información de la cadena de conexión de base de datos de cumplimiento en &quot; HKLM\Software\Microsoft\MBAM Server\Web\ComplianceDBConnectionString &quot; no es válida. Comprobar el valor que corresponde a la clave del registro anterior. ni</p>
<p>Si se registra alguno de los mensajes restantes, consulte los pasos de solución de problemas que aparecen en el artículo de TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> sobre cómo solucionar problemas de conexión al motor de base de datos de SQL Server </a> para comprobar si se puede establecer una conexión con la base de datos de cumplimiento de MBAM desde el servidor IIS con las credenciales del grupo de aplicaciones.</p></td>
</tr>
<tr class="even">
<td align="left"><p>111</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>WebAppDbError</p></td>
<td align="left"><p></p></td>
<td align="left"><p>Estos errores indican una de las dos condiciones siguientes:</p>
<ul>
<li><p>MBAM sitios web o WebService no pudieron conectarse a la base de datos de MBAMCompliance o MBAMRecovery</p></li>
<li><p>Sitios web de MBAM/cuenta de ejecución (cuenta del grupo de aplicaciones) no se pudo ejecutar el procedimiento almacenado GetVersion en la base de datos de MBAMCompliance o MBAMRecovery</p></li>
</ul>
<p>El mensaje contenido en el evento proporcionará más información sobre la excepción.</p>
<p>Consulte los pasos de solución de problemas que aparecen en el artículo de TechNet <a href="https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx" data-raw-source="[How to Troubleshoot Connecting to the SQL Server Database Engine](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx)"> sobre cómo solucionar problemas de conexión al motor de base de datos de SQL Server </a> para comprobar que la cuenta de ejecución de MBAM (cuenta del grupo de aplicaciones) se pudo conectar a la base de datos de cumplimiento/recuperación de MBAM y tiene permisos para ejecutar el procedimiento almacenado GetVersion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>112</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/administrador</p></td>
<td align="left"><p>WebAppError</p></td>
<td align="left"><p>Se produjo un error al comprobar el registro de nombre principal de servicio (SPN). EventDetails:{ExceptionMessage}</p></td>
<td align="left"><p>Para realizar la verificación del SPN, MBAM consulta Active Directory para recuperar una lista de la cuenta de ejecución asignada a los SPN. MBAM también consulta el &quot;ApplicationHost.config&quot; para obtener MBAM enlaces de sitios Web. Este mensaje de error indica que MBAM no pudo comunicarse con Active Directory o no pudo cargar el archivo de applicationHost.config.</p>
<p>Compruebe que la cuenta de ejecución (cuenta del grupo de aplicaciones) tiene permisos para consultar AD o el archivo de ApplicationHost.config. Compruebe también las entradas de enlace del sitio en ApplicationHost.config archivo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>200</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/Operational</p></td>
<td align="left"><p>HelpDeskInformation</p></td>
<td align="left"><p>La aplicación de sitio web de administración detectó y se conectó correctamente a una versión compatible de la base de datos de recuperación. O bien</p>
<p>La aplicación de sitio web de administración encontró y se conectó correctamente a una versión compatible de la base de datos de cumplimiento.</p></td>
<td align="left"><p>Indica una conexión correcta a la base de datos de recuperación y cumplimiento desde el sitio web de MBAM Helpdesk.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>201</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/Operational</p></td>
<td align="left"><p>SelfServicePortalInformation</p></td>
<td align="left"><p>La aplicación de portal de autoservicio se ha encontrado correctamente y se ha conectado a una versión compatible de la base de datos de recuperación. O bien</p>
<p>La aplicación de portal de autoservicio se ha encontrado correctamente y se ha conectado a una versión compatible de la base de datos de cumplimiento.</p></td>
<td align="left"><p>Indica una conexión correcta a la base de datos de recuperación y cumplimiento desde el portal de autoservicio MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>202</p></td>
<td align="left"><p>Microsoft-Windows-MBAM-web/Operational</p></td>
<td align="left"><p>WebAppInformation</p></td>
<td align="left"><p>La aplicación tiene sus SPN registrados correctamente.</p></td>
<td align="left"><p>Indica que los SPN necesarios para el sitio web del Departamento de soporte técnico de MBAM están registrados correctamente en la cuenta que se está ejecutando.</p></td>
</tr>
</tbody>
</table>

 


## Temas relacionados


[Referencia técnica de MBAM 2.5](technical-reference-for-mbam-25.md)

[Registros de eventos de cliente](client-event-logs.md)

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





