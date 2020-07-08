---
title: Administrar 5.1 de App-V mediante el uso de PowerShell
description: Administrar 5.1 de App-V mediante el uso de PowerShell
author: dansimp
ms.assetid: 9e10ff07-2cd9-4dc1-9e99-582f90c36081
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f0c64d7e0330ff5d737dfa02d87f156cc3236b04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814871"
---
# Administrar 5.1 de App-V mediante el uso de PowerShell


Microsoft Application Virtualization (App-V) 5,1 proporciona cmdlets de Windows PowerShell, que pueden ayudar a los administradores a realizar varias tareas de App-V 5,1. En las siguientes secciones se proporciona más información sobre cómo usar PowerShell con App-V 5,1.

## Cómo administrar App-V 5,1 mediante PowerShell


Use los siguientes procedimientos de PowerShell para realizar varias tareas de App-V 5,1.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nombre</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md" data-raw-source="[How to Load the PowerShell Cmdlets and Get Cmdlet Help](how-to-load-the-powershell-cmdlets-and-get-cmdlet-help-51.md)">Cómo cargar los Cmdlets de PowerShell y obtener ayuda de Cmdlet</a></p></td>
<td align="left"><p>Describe cómo instalar los cmdlets de PowerShell y cómo encontrar ayuda y ejemplos de cmdlet.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">Cómo administrar paquetes App-V 5.1 que se ejecutan en un equipo independiente mediante PowerShell</a></p></td>
<td align="left"><p>Describe cómo administrar el ciclo de vida de paquetes del cliente en un equipo independiente con PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md)">Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell</a></p></td>
<td align="left"><p>Describe cómo administrar grupos de conexión con PowerShell.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-modify-client-configuration-by-using-powershell51.md" data-raw-source="[How to Modify Client Configuration by Using PowerShell](how-to-modify-client-configuration-by-using-powershell51.md)">Cómo modificar la configuración de cliente mediante el uso de PowerShell</a></p></td>
<td align="left"><p>Describe cómo modificar el cliente con PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-apply-the-user-configuration-file-by-using-powershell51.md" data-raw-source="[How to Apply the User Configuration File by Using PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell51.md)">Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell</a></p></td>
<td align="left"><p>Describe cómo aplicar un archivo de configuración de usuario con PowerShell.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-apply-the-deployment-configuration-file-by-using-powershell51.md" data-raw-source="[How to Apply the Deployment Configuration File by Using PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)">Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell</a></p></td>
<td align="left"><p>Describe cómo aplicar un archivo de configuración de implementación con PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-sequence-a-package--by-using-powershell-51.md" data-raw-source="[How to Sequence a Package by Using PowerShell](how-to-sequence-a-package--by-using-powershell-51.md)">Cómo hacer una secuencia de un paquete con PowerShell</a></p></td>
<td align="left"><p>Describe cómo crear un paquete nuevo con PowerShell.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-package-accelerator-by-using-powershell51.md" data-raw-source="[How to Create a Package Accelerator by Using PowerShell](how-to-create-a-package-accelerator-by-using-powershell51.md)">Cómo crear un acelerador de paquetes mediante el uso de PowerShell</a></p></td>
<td align="left"><p>Describe cómo crear un acelerador de paquetes con PowerShell. Puede usar aceleradores de paquetes para hacer secuencias de aplicaciones grandes y complejas de forma automática.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md" data-raw-source="[How to Enable Reporting on the App-V 5.1 Client by Using PowerShell](how-to-enable-reporting-on-the-app-v-51-client-by-using-powershell.md)">Cómo habilitar los informes en el cliente de App-V 5.1 mediante PowerShell</a></p></td>
<td align="left"><p>Describe cómo habilitar el equipo que ejecuta el 5,1 de App-V para enviar información de informes.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md" data-raw-source="[How to Install the App-V Databases and Convert the Associated Security Identifiers by Using PowerShell](how-to-install-the-app-v-databases-and-convert-the-associated-security-identifiers--by-using-powershell51.md)">Cómo instalar las bases de datos de App-V y convertir los identificadores de seguridad asociados mediante PowerShell</a></p></td>
<td align="left"><p>Describe cómo tomar una matriz de nombres de cuenta y convertir cada una de ellas en el SID correspondiente en formatos hexadecimales y estándar.</p></td>
</tr>
</tbody>
</table>

 

**Importante**  Asegúrese de que todas las secuencias de comandos que ejecute con los paquetes de App-V coincidan con la Directiva de ejecución que haya configurado para PowerShell.

 

## Control de errores de PowerShell


Use la tabla siguiente para obtener información sobre el control de errores de App-V 5,1 PowerShell.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Evento</th>
<th align="left">Acción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Usar el atributo RollbackOnError con scripts incrustados</p></td>
<td align="left"><p>Al usar el <strong> atributo RollbackOnError </strong> con scripts incrustados, el atributo se omite para los eventos siguientes:</p>
<ul>
<li><p>Quitar un paquete</p></li>
<li><p>Anulando la publicación de un paquete</p></li>
<li><p>Finalizar un entorno virtual</p></li>
<li><p>Finalizar un proceso</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>El nombre del paquete contiene<strong>$</strong></p></td>
<td align="left"><p>Si un nombre de paquete contiene el carácter ( <strong> $ </strong> ), debe usar una comilla simple ( <strong> ' </strong> ); por ejemplo,</p>
<p><strong>Add-AppvClientPackage ' contoso $ app. appv '</strong></p></td>
</tr>
</tbody>
</table>

 






## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)

 

 





