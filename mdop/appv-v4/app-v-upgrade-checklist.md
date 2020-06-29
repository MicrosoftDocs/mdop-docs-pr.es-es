---
title: Lista de comprobación de actualización de App-V
description: Lista de comprobación de actualización de App-V
author: dansimp
ms.assetid: 64e317d2-d260-4b67-8a49-ba9ac513087a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad856ce3067c327f3e604f9269ee384a66a1675a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819740"
---
# Lista de comprobación de actualización de App-V


Antes de intentar actualizar a Microsoft Application Virtualization (App-V) 4,5 o versiones posteriores, cualquier versión anterior a App-V 4,1 debe actualizarse a App-V 4,1. Debe planear la actualización de los clientes en primer lugar y, a continuación, actualizar los componentes del servidor. Los clientes de App-V que se han actualizado a App-V 4,5 siguen trabajando con servidores de App-V que aún no se han actualizado. Las versiones anteriores del cliente no son compatibles con los servidores que se han actualizado a App-V 4,5.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paso</th>
<th align="left">Referencia</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Actualice los clientes de App-V.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-client.md" data-raw-source="[How to Upgrade the Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)">Cómo actualizar el cliente de virtualización de aplicaciones</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Actualice los servidores y la base de datos de App-V.</p>
<div class="alert">
<strong>Importante</strong><br/><p>Si tiene más de un servidor que comparte el acceso a la base de datos de App-V, todos los servidores deben estar desconectados mientras la base de datos se está actualizando. Debe seguir sus prácticas habituales de negocios para la actualización de la base de datos, pero le recomendamos que pruebe la actualización de la base de datos con una copia de seguridad de la base de datos en primer lugar en un servidor de prueba. Después, seleccione uno de los servidores para la primera actualización, que actualizará el esquema de la base de datos. Una vez que la base de datos de producción se ha actualizado correctamente, puede actualizar el software de App-V en los otros servidores.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Cómo actualizar los servidores y componentes del sistema</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Actualice el servicio Web de administración de App-V.</p>
<p>Este paso solo se aplica si el servicio Web de administración está en un servidor independiente, lo que requiere que ejecute el programa de instalación del servidor en ese servidor independiente para actualizar el servicio Web de administración. De lo contrario, el paso de actualización del servidor anterior actualizará automáticamente el servicio Web de administración.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Cómo actualizar los servidores y componentes del sistema</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Actualice la consola de administración de App-V.</p>
<p>Este paso solo se aplica si la consola de administración está en un equipo independiente, lo que requiere que ejecute el programa de instalación de servidor en ese equipo diferente para actualizar la consola. De lo contrario, el paso de actualización del servidor anterior actualizará la consola de administración.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-servers-and-system-components.md" data-raw-source="[How to Upgrade the Servers and System Components](how-to-upgrade-the-servers-and-system-components.md)">Cómo actualizar los servidores y componentes del sistema</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Actualice el secuenciador de App-V.</p></td>
<td align="left"><p><a href="how-to-upgrade-the-application-virtualization-sequencer.md" data-raw-source="[How to Upgrade the Application Virtualization Sequencer](how-to-upgrade-the-application-virtualization-sequencer.md)">Cómo actualizar el cliente secuenciador de virtualización de aplicaciones</a></p></td>
</tr>
</tbody>
</table>



## Consideraciones de actualización adicionales


-   Los paquetes de aplicaciones virtuales de la versión 4,2 no tendrán que volver a secuenciarse para usarlos con la versión 4,5. Sin embargo, considere la posibilidad de actualizar los paquetes virtuales al formato de Microsoft Application Virtualization 4,5 Si desea aplicar listas de control de acceso (ACL) predeterminadas o generar un archivo de Windows Installer. Este es un proceso sencillo y solo requiere que el paquete de la aplicación virtual existente se abra y se guarde con el secuenciador App-V 4,5. Esto se puede automatizar mediante la interfaz de línea de comandos App-VSequencer. Para obtener más información, vea [Cómo crear o actualizar aplicaciones virtuales con el secuenciador de App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

-   Una de las características de la 4,5 secuenciador es la capacidad de crear archivos de Windows Installer (. msi) como puntos de control para la interoperabilidad de paquetes de aplicaciones virtuales con sistemas ESD (Electronic Software Distribution), como Microsoft Endpoint Configuration Manager. Los archivos anteriores de Windows Installer creados con la herramienta MSI para virtualización de aplicaciones que se instalaron en un cliente de App-V 4,1 o 4,2 que se actualiza posteriormente a App-V 4,5 seguirán funcionando, aunque no se pueden instalar en el cliente de App-V 4,5. Sin embargo, no se pueden quitar ni actualizar, a menos que se actualicen en el secuenciador de aplicaciones-V 4,5. El paquete de App-V original anterior a 4,5 debe abrirse en el secuenciador de App-V 4,5 y, a continuación, se puede guardar como un archivo de Windows Installer.

    **Nota**  
    Si el cliente de App-V 4,2 ya se ha actualizado a App-V 4,5, se puede incluir una solución alternativa para conservar los paquetes de la versión 4,2 en los clientes con la versión 4,5 y permitir que se administren. Este script debe copiar dos archivos, msvcp71.dll y msvcr71.dll, a la carpeta de instalación de App-V y establecer los siguientes valores de clave del registro en la clave del registro: \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:

    "ClientVersion" = "4.2.1.20"

    "GlobalDataDirectory" = "C:\\\\Documents y Settings\\\\All Users\\\\Documents\\\\" (una ubicación de escritura global)



-   Los archivos de Windows Installer generados por el secuenciador de App-V 4,5 muestran el mensaje de error "este paquete requiere el cliente de Microsoft Application Virtualization 4,5 o posterior" al intentar ejecutarlo en un cliente de App-V 4,6. Abra el paquete antiguo con el secuenciador de App-V 4,5 SP1 o el secuenciador de App-V 4,6 y genere un nuevo archivo. msi para el paquete.

-   Los informes de la versión 4,2 que se crearon y guardaron se sobrescribirán cuando el servidor se actualice a la versión 4,5. Si tiene que mantener estos informes, debe guardar una copia de seguridad del archivo SftMMC. msc que se encuentra en la carpeta de la consola de administración de SoftGrid en el servidor y usar esa copia para reemplazar el nuevo SftMMC. msc instalado durante la actualización.

-   Para obtener más información sobre la actualización de versiones anteriores, vea [actualizar a Microsoft Application virtualization 4,5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .

## <a href="" id="app-v-4-6-client-package-support-"></a>Compatibilidad con paquetes de cliente de App-V 4,6


Puede implementar paquetes creados en versiones anteriores de App-V para los clientes de App-V 4,6. Sin embargo, debe modificar el archivo. OSD asociado para que incluya la información adecuada sobre la arquitectura del chip y el sistema operativo. Se pueden usar los siguientes valores:

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Valor del sistema operativo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>&lt;VALOR de SO = "Win2003TS"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALOR de SO = "Win2003TS64"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALOR de SO = "Win2008TS"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALOR de SO = "Win2008TS64"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALOR de SO = "Win2008R2TS64"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALOR de SO = "Win7"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALOR de SO = "Win764"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;VALOR de SO = "WinVista"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALOR de SO = "WinVista64"/&gt;</p></td>
</tr>
<tr class="even">
<td align="left"><p>&lt;OS VALUE = "WinXP"/&gt;</p></td>
</tr>
<tr class="odd">
<td align="left"><p>&lt;VALOR de SO = "WinXP64"/&gt;</p></td>
</tr>
</tbody>
</table>



Para ejecutar un paquete de 32 bits recién creado, debe secuenciar la aplicación en un equipo que ejecute un sistema operativo de 32 bits con App-V 4,6 Sequencer instalado. Una vez que haya realizado la secuencia de la aplicación, en la consola del secuenciador, haga clic en la pestaña **implementación** y especifique la arquitectura de chip y sistema operativo adecuado según sea necesario.

**Importante**  
Las aplicaciones que se ordenan en un equipo con un sistema operativo de 64 bits se deben implementar en equipos que ejecuten un sistema operativo de 64 bits. Los nuevos paquetes de 32 bits creados mediante el secuenciador de App-V 4,6 no se ejecutan en equipos que ejecutan el cliente de App-V 4,5.



Para ejecutar nuevos paquetes de 64 bits en el cliente de App-V 4,6, debe secuenciar la aplicación en un equipo que ejecute el secuenciador de App-V 4,6 y que esté ejecutando un sistema operativo de 64 bits. Una vez que haya realizado la secuencia de la aplicación, en la consola secuenciador, haga clic en la pestaña **implementación** y especifique la arquitectura de sistema operativo y de chips adecuada según sea necesario.

En la siguiente tabla se enumeran las versiones de cliente que ejecutarán los paquetes creados con las distintas versiones del secuenciador.

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
<th align="left"></th>
<th align="left">Secuenciado mediante el secuenciador de aplicaciones-V 4,2</th>
<th align="left">Secuenciado mediante el secuenciador de aplicaciones-V 4,5</th>
<th align="left">Secuenciado mediante la aplicación de 32 bits de-V 4,6 Sequencer</th>
<th align="left">Secuenciado mediante la aplicación de 64 bits de-V 4,6 Sequencer</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>cliente de 4,2</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="even">
<td align="left"><p>cliente de 4,5 ¹</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="odd">
<td align="left"><p>cliente 4,6 (32 bits)</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="even">
<td align="left"><p>cliente 4,6 (64 bits)</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
</tbody>
</table>



¹ se aplica a todas las versiones del cliente de App-V 4,5, entre las que se incluyen App-V 4,5, App-V 4,5 CU1 y App-V 4,5 SP1.









