---
title: Cómo cargar los Cmdlets de PowerShell y obtener ayuda de Cmdlet
description: Cómo cargar los Cmdlets de PowerShell y obtener ayuda de Cmdlet
author: dansimp
ms.assetid: b6ae5460-2c3a-4030-b132-394d9d5a541e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 32b5bb26331f204acffbf96ea119ac4209c3cd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813950"
---
# Cómo cargar los Cmdlets de PowerShell y obtener ayuda de Cmdlet


Qué trata este tema:

-   [Requisitos para usar los cmdlets de PowerShell](#bkmk-reqs-using-posh)

-   [Cargar los cmdlets de PowerShell](#bkmk-load-cmdlets)

-   [Obtener ayuda para los cmdlets de PowerShell](#bkmk-get-cmdlet-help)

-   [Mostrar la ayuda para un cmdlet de PowerShell](#bkmk-display-help-cmdlet)

## <a href="" id="bkmk-reqs-using-posh"></a>Requisitos para usar los cmdlets de PowerShell


Revise los siguientes requisitos para usar los cmdlets de PowerShell de App-V:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisitos</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Los usuarios solo pueden ejecutar cmdlets de servidor de App-V si le conceden acceso mediante uno de los siguientes métodos:</p></td>
<td align="left"><ul>
<li><p><strong>Al implementar y configurar el servidor de App-V </strong> :</p>
<p>Especifique un grupo de Active Directory o un usuario individual que tenga permisos para administrar el entorno de App-V. Vea <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> cómo implementar el servidor de App-V 5,1 </a> .</p></li>
<li><p><strong>Después de implementar el servidor de App-V </strong> :</p>
<p>Use la consola de administración de App-V para agregar un usuario o grupo de Active Directory adicional. Consulte <a href="how-to-add-or-remove-an-administrator-by-using-the-management-console51.md" data-raw-source="[How to Add or Remove an Administrator by Using the Management Console](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)"> Cómo agregar o quitar un administrador mediante la consola de administración </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Cmdlets que requieren un símbolo del sistema con privilegios elevados</p></td>
<td align="left"><ul>
<li><p>Add-AppvClientPackage</p></li>
<li><p>Remove-AppvClientPackage</p></li>
<li><p>Set-AppvClientConfiguration</p></li>
<li><p>Add-AppvClientConnectionGroup</p></li>
<li><p>Remove-AppvClientConnectionGroup</p></li>
<li><p>Add-AppvPublishingServer</p></li>
<li><p>Remove-AppvPublishingServer</p></li>
<li><p>Send-AppvClientReport</p></li>
<li><p>Set-AppvClientMode</p></li>
<li><p>Set-AppvClientPackage</p></li>
<li><p>Set-AppvPublishingServer</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Cmdlets que los usuarios finales pueden ejecutar, a menos que los configure para requerir un símbolo del sistema con privilegios elevados</p></td>
<td align="left"><ul>
<li><p>Publicar-AppvClientPackage</p></li>
<li><p>Anulación de la publicación-AppvClientPackage</p></li>
</ul>
<p>Para configurar estos cmdlets para que requieran un símbolo del sistema con privilegios elevados, use uno de los siguientes métodos:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Más recursos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ejecute el <strong> cmdlet Set-AppvClientConfiguration </strong> con el <strong> parámetro-RequirePublishAsAdmin </strong> .</p></td>
<td align="left"><ul>
<li><p><a href="how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg" data-raw-source="[How to Manage Connection Groups on a Stand-alone Computer by Using PowerShell](how-to-manage-connection-groups-on-a-stand-alone-computer-by-using-powershell51.md#bkmk-admin-only-posh-topic-cg)">Cómo administrar grupos de conexión en un equipo independiente mediante el uso de PowerShell</a></p></li>
<li><p><a href="how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.1 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-51-packages-running-on-a-stand-alone-computer-by-using-powershell.md)">Cómo administrar paquetes App-V 5.1 que se ejecutan en un equipo independiente mediante PowerShell</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Habilite la configuración de directiva de grupo "requerir publicación como administrador" para los clientes de App-V.</p></td>
<td align="left"><p><a href="how-to-publish-a-package-by-using-the-management-console-51.md" data-raw-source="[How to Publish a Package by Using the Management Console](how-to-publish-a-package-by-using-the-management-console-51.md)">Cómo publicar un paquete mediante el uso de la consola de administración</a></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-load-cmdlets"></a>Cargar los cmdlets de PowerShell

Para cargar los módulos del cmdlet de PowerShell:

1.  Abra Windows PowerShell o el entorno de scripting integrado de Windows PowerShell (ISE).

2.  Escriba uno de los siguientes comandos para cargar los cmdlets para el módulo que desee:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente de App-V</th>
<th align="left">Comando para escribir</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de App-V</p></td>
<td align="left"><p>Importación-módulo AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Secuenciador de App-V</p></td>
<td align="left"><p>Importación-módulo AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cliente de App-V</p></td>
<td align="left"><p>Importación-módulo AppvClient</p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-get-cmdlet-help"></a>Obtener ayuda para los cmdlets de PowerShell
A partir de App-V 5,0 SP3, la ayuda del cmdlet está disponible en dos formatos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Como módulo descargable</p></td>
<td align="left"><p>Para descargar la ayuda más reciente después de descargar el módulo cmdlet:</p>
<ol>
<li><p>Abra Windows PowerShell o el entorno de scripting integrado de Windows PowerShell (ISE).</p></li>
<li><p>Escriba uno de los siguientes comandos para cargar los cmdlets para el módulo que desee:</p></li>
</ol>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente de App-V</th>
<th align="left">Comando para escribir</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de App-V</p></td>
<td align="left"><p>Update-Help-Module AppvServer</p></td>
</tr>
<tr class="even">
<td align="left"><p>Secuenciador de App-V</p></td>
<td align="left"><p>Update-Help-Module AppvSequencer</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cliente de App-V</p></td>
<td align="left"><p>Update-Help-Module AppvClient</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p>En TechNet como páginas web</p></td>
<td align="left"><p>Consulte el nodo App-V en la <a href="https://technet.microsoft.com/library/dn520245.aspx" data-raw-source="[Microsoft Desktop Optimization Pack Automation with Windows PowerShell](https://technet.microsoft.com/library/dn520245.aspx)"> automatización de Microsoft Desktop Optimization Pack con Windows PowerShell </a> .</p></td>
</tr>
</tbody>
</table>

## <a href="" id="bkmk-display-help-cmdlet"></a>Mostrar la ayuda para un cmdlet de PowerShell
Para mostrar la ayuda de un cmdlet de PowerShell específico:

1.  Abra Windows PowerShell o el entorno de scripting integrado de Windows PowerShell (ISE).

2.  Escriba **cmdlet Get-Help** &lt; *cmdlet* &gt; ; por ejemplo, **Get-Help Publish-AppvClientPackage**.

**¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

 

 





