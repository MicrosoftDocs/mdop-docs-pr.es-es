---
title: Planificación de la migración desde versiones anteriores
description: Planificación de la migración desde versiones anteriores
author: dansimp
ms.assetid: 62967bf1-542f-41b0-838f-c62f3430ac73
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9b239e09da06270b30b401151cf12e817e2cf8d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815930"
---
# Planificación de la migración desde versiones anteriores


Antes de intentar actualizar a Microsoft Application Virtualization 4.5 o versiones posteriores, cualquier versión anterior a 4.1 debe actualizarse a la versión 4.1. Debe planear la actualización de los clientes en primer lugar y, a continuación, actualizar los componentes del servidor. Los clientes que se hayan actualizado a 4.5 seguirán funcionando con servidores de virtualización de aplicaciones que aún no se hayan actualizado. Los servidores que se han actualizado a 4.5 no admiten versiones anteriores del cliente. Para obtener más información sobre cómo actualizar los componentes del sistema, vea [implementación de Application Virtualization y consideraciones](application-virtualization-deployment-and-upgrade-considerations.md)sobre la actualización.

Para ayudar a garantizar una migración correcta, los componentes del sistema de virtualización de aplicaciones deben actualizarse en el siguiente orden:

1.  **Clientes de Microsoft Application Virtualization.** Para obtener instrucciones paso a paso para la actualización, vea [Cómo actualizar el cliente de virtualización de aplicaciones](how-to-upgrade-the-application-virtualization-client.md).

2.  **Base de datos y servidores de virtualización de aplicaciones de Microsoft.** Para obtener instrucciones paso a paso para la actualización, consulte [Cómo actualizar los servidores y los componentes del sistema](how-to-upgrade-the-servers-and-system-components.md).

    **Nota:**  Si tiene más de un servidor que comparte el acceso a la base de datos de virtualización de la aplicación, todos esos servidores deben estar desconectados mientras se actualiza la base de datos. Debe seguir las prácticas normales de negocios para la actualización de la base de datos, pero es muy aconsejable que pruebe la actualización de la base de datos con una copia de seguridad de la base de datos en primer lugar en un servidor de prueba. Después, seleccione uno de los servidores para la primera actualización, que actualizará el esquema de la base de datos. Una vez que la base de datos de producción se ha actualizado correctamente, puede actualizar los otros servidores.

     

3.  **Servicio Web de administración de Microsoft Application Virtualization.** Este paso solo se aplica si el servicio Web de administración está en un servidor independiente, lo que requiere que ejecute el programa de instalación del servidor en ese servidor independiente para actualizar el servicio Web. De lo contrario, el paso de actualización del servidor anterior actualizará automáticamente el servicio Web de administración.

4.  **Consola de administración de Microsoft Application Virtualization.** Este paso solo se aplica si la consola de administración está en un equipo independiente, lo que requiere que ejecute el programa de instalación de servidor en ese equipo diferente para actualizar la consola. De lo contrario, el paso de actualización del servidor anterior actualizará la consola de administración.

5.  **Microsoft Application Virtualization Sequencer.** Para obtener instrucciones paso a paso, vea [Cómo instalar Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md). No será necesario reordenar los paquetes de aplicaciones virtuales de la versión 4.2 para usarlos con la versión 4.5. Sin embargo, considere la posibilidad de actualizar los paquetes virtuales al formato Microsoft Application Virtualization 4.5 Si desea aplicar listas de control de acceso (ACL) predeterminadas o generar un archivo de Windows Installer. Este es un proceso simple y solo requiere que el paquete de la aplicación virtual existente se abra y se guarde con el secuenciador de la versi 4.5. Esto se puede automatizar usando la interfaz de línea de comandos de Application Virtualization Sequencer.

## <a href="" id="app-v-4-6-client-package-support-"></a>Compatibilidad con paquetes del cliente de App-V 4.6


Puede implementar paquetes creados en versiones anteriores de App-V para aplicaciones-V 4.6 clientes. Sin embargo, debe modificar el archivo **. OSD** asociado para que incluya la información adecuada sobre la arquitectura del chip y el sistema operativo. Use los valores siguientes.

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

 

Para ejecutar un paquete de 32 bits recién creado, debe secuenciar la aplicación en un equipo que ejecute un sistema operativo de 32 bits con App-V 4.6 Sequencer instalado. Una vez que haya realizado la secuencia de la aplicación, en la consola del secuenciador, seleccione la pestaña **implementación** y, a continuación, especifique la arquitectura de sistema operativo y de chips adecuada según sea necesario.

**Importante**  Las aplicaciones que se ordenan en un equipo con un sistema operativo de 64 bits se deben implementar en equipos que ejecuten un sistema operativo de 64 bits. Los nuevos paquetes de 32 de bits creados mediante el secuenciador de App-V 4.6 no se ejecutarán en equipos que ejecuten el cliente de App-V 4,5.

 

Para ejecutar nuevos paquetes de 64 bits en el cliente de App-V 4.6, debe secuenciar la aplicación en un equipo que ejecute el secuenciador de App-V 4.6 y que esté ejecutando un sistema operativo de 64 bits. Una vez que haya realizado la secuencia de la aplicación, en la consola del secuenciador, seleccione la pestaña **implementación** y, a continuación, especifique la arquitectura de sistema operativo y de chips adecuada según sea necesario.

En la siguiente tabla se enumeran las versiones de cliente que ejecutarán los paquetes creados con las distintas versiones del secuenciador.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Secuenciado mediante el secuenciador de aplicaciones-V 4,2</th>
<th align="left">Secuenciado mediante el secuenciador de aplicaciones-V 4,5</th>
<th align="left">Secuenciado mediante la aplicación de 32 bits de-V 4,6 Sequencer</th>
<th align="left">Secuenciado mediante la aplicación de 64 bits de-V 4,6 Sequencer</th>
<th align="left">Secuenciado mediante el secuenciador de aplicación de 32 bits-V 4,6 SP1</th>
<th align="left">Secuenciado mediante el secuenciador de aplicación de 64 bits-V 4,6 SP1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>cliente de 4,2</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>No</p></td>
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
<td align="left"><p>No</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="odd">
<td align="left"><p>cliente 4,6 (32 bits)</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="even">
<td align="left"><p>cliente 4,6 (64 bits)</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cliente de 4,6 SP1</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>No</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>No</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente de 4,6 SP1 (64 bits)</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
<td align="left"><p>Sí</p></td>
</tr>
</tbody>
</table>

 

¹ se aplica a todas las versiones del cliente de App-V 4.5, entre las que se incluyen App-V 4.5, App-V 4.5 CU1 y App-V 4.5 SP1.

## Consideraciones de migración adicionales


Una de las características de App-V 4.5 Sequencer es la capacidad de crear archivos de Windows Installer (. msi) como puntos de control para la interoperabilidad de paquetes de aplicaciones virtuales con sistemas de distribución electrónica de software (ESD), como Microsoft Endpoint Configuration Manager. Los archivos anteriores de Windows Installer creados con la herramienta. msi para la virtualización de aplicaciones que se instalaron en un cliente de App-V 4.1 o 4.2 que posteriormente se actualizó a 4.5 seguirán funcionando, aunque no se pueden instalar en el cliente de la versión 4.5. Sin embargo, no se pueden quitar ni actualizar, a menos que se actualicen en el secuenciador de la versión 4.5. El paquete de la aplicación virtual original anterior a la 4,5 tendría que estar abierto en el secuenciador de la versión 4.5 y, después, guardado como un archivo de Windows Installer.

**Nota:**  Si el cliente de App-V 4.2 ya se ha actualizado a la versión 4.5, es posible usar el script como solución alternativa para preservar los paquetes 4.2 en los clientes de la versión 4.5 y permitir que sean administrados. Este script debe copiar dos archivos, msvcp71.dll y msvcr71.dll, a la carpeta de instalación de App-V y establecer los siguientes valores de clave del registro en la clave del registro \ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\]:

"ClientVersion" = "4.2.1.20"

"GlobalDataDirectory" = "C:\\\\Documents y Settings\\\\All Users\\\\Documents\\\\" (una ubicación de escritura global)

 

Los archivos de Windows Installer generados por el secuenciador de App-V 4,5 muestran el mensaje de error "este paquete requiere el cliente de Microsoft Application Virtualization 4,5 o posterior" cuando intenta ejecutarlo en un cliente de App-V 4,6. Abra el paquete antiguo con el secuenciador de App-V 4,5 SP1 o el secuenciador de App-V 4,6 y genere un nuevo. msi para el paquete.

Cualquier informe 4.2 que se haya creado y guardado se sobrescribirá cuando el servidor se actualice a la versión 4.5. Si necesita conservar estos informes, debe guardar una copia de seguridad del archivo SftMMC. msc que se encuentra en la carpeta de la consola de administración de SoftGrid en el servidor y usar esa copia para reemplazar el nuevo SftMMC. msc instalado durante la actualización.

Para obtener más información sobre la actualización de versiones anteriores, vea [actualizar a Microsoft Application virtualization 4,5 FAQ](https://go.microsoft.com/fwlink/?LinkId=120358) ( https://go.microsoft.com/fwlink/?LinkId=120358) .

## Temas relacionados


[Planificación de la implementación del sistema de virtualización de aplicaciones](planning-for-application-virtualization-system-deployment.md)

 

 





