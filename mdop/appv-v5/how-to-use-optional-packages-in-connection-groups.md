---
title: Cómo usar los paquetes opcionales en grupos de conexión
description: Cómo usar los paquetes opcionales en grupos de conexión
author: dansimp
ms.assetid: 4d08a81b-55e5-471a-91dc-9a684fb3c9a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 64a2c0758294bfa617d3d85f888cfce3a2c0d21e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813631"
---
# Cómo usar los paquetes opcionales en grupos de conexión


A partir de Microsoft Application Virtualization (App-V) 5,0 SP3, puede agregar paquetes opcionales a los grupos de conexión para simplificar la administración de grupos de conexión. En la tabla siguiente se resumen las tareas que se pueden completar más fácilmente mediante paquetes opcionales y se proporcionan vínculos a las instrucciones de cada tarea.

**Nota:** 
 Los **paquetes opcionales solo se admiten en App-V 5,0 SP3.**

 

Antes de usar paquetes opcionales, consulte [los requisitos para usar paquetes opcionales en grupos de conexión](#bkmk-reqs-using-cg).

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Vínculo a las instrucciones</th>
<th align="left">Tarea</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="#bkmk-apps-plugs-optional" data-raw-source="[Use one connection group, with optional packages, for multiple users who have different packages entitled to them](#bkmk-apps-plugs-optional)">Usar un grupo de conexión, con paquetes opcionales, para varios usuarios que tienen paquetes diferentes a los que tienen derecho</a></p></td>
<td align="left"><p>Use un único grupo de conexiones para que diferentes grupos de aplicaciones y complementos estén disponibles para los distintos usuarios finales.</p>
<p>Por ejemplo, desea distribuir Microsoft Office a todos los usuarios finales, pero distribuir diferentes complementos a diferentes subconjuntos de usuarios.</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="#bkmk-unpub-del-optl-pkg" data-raw-source="[Unpublish or delete an optional package, or unpublish an optional package and republish it later, without changing the connection group](#bkmk-unpub-del-optl-pkg)">Cancelar la publicación o la eliminación de un paquete opcional, o bien, anular la publicación de un paquete opcional y volver a publicarlo más adelante, sin cambiar el grupo de conexión</a></p></td>
<td align="left"><p>Para anular la publicación, eliminar o volver a publicar un paquete opcional sin tener que deshabilitar, quitar, editar, agregar y volver a habilitar el grupo de conexión en el cliente de App-V.</p>
<p>También puede anular la publicación del paquete opcional y volver a publicarlo más adelante sin tener que deshabilitar o volver a publicar el grupo de conexión.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-apps-plugs-optional"></a>Usar un grupo de conexión, con paquetes opcionales, para varios usuarios con paquetes diferentes a los que tienen derecho


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Descripción de la tarea</th>
<th align="left">Cómo realizar la tarea</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Con App-V 5,0 SP3</strong></p>
<p>Puede agregar paquetes opcionales a grupos de conexión, lo que le permite proporcionar diferentes combinaciones de aplicaciones y complementos a diferentes usuarios finales.</p>
<p><strong>Ejemplo </strong> : desea distribuir Microsoft Office a los usuarios finales, pero habilitar un determinado complemento solo para un subconjunto de usuarios.</p>
<p>Para ello, cree un grupo de conexiones que contenga un paquete con Office y otro paquete con complementos de Office y, a continuación, haga que el paquete de complementos sea opcional.</p>
<p>Los usuarios finales que no tengan derecho al paquete de complementos seguirán pudiendo ejecutar Office.</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Pasos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de App-V: consola de administración</p></td>
<td align="left"><ol>
<li><p>En la consola de administración, seleccione <strong> packages (paquetes) </strong> para abrir la página packages (paquetes).</p></li>
<li><p>Seleccione <strong> grupos </strong> de conexión para mostrar la biblioteca de grupos de conexión.</p></li>
<li><p>Seleccione el grupo de conexiones correcto en la biblioteca de grupos de conexión.</p></li>
<li><p>Haga clic en <strong> Editar </strong> en el panel de paquetes conectados.</p></li>
<li><p>Seleccione <strong> opcional </strong> junto al nombre del paquete.</p></li>
<li><p>Active la <strong> casilla Agregar acceso de paquete al grupo </strong> . Este paso obligatorio agrega al grupo de conexiones los derechos de paquete que configuró anteriormente al asignar paquetes a grupos de Active Directory.</p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de App-V: cmdlet de PowerShell</p></td>
<td align="left"><p>Use el cmdlet siguiente y especifique el <strong> parámetro-Optional </strong> :</p>
<p><strong>Add-AppvServerConnectionGroupPackage</strong></p>
<p><strong>Sintáctica</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage [-AppvServerConnectionGroup] &lt;SerializableConnectionGroup&gt; [[-AppvServerPackage] &lt;PackageVersion&gt;] [-Optional] [-Order &lt;int&gt;] [-UseAnyPackageVersion]</code></p>
<p><strong>Por ejemplo:</strong></p>
<p><code>Add-AppvServerConnectionGroupPackage -Name &quot;Connection Group 1&quot; -PackageName &quot;Package 1&quot; -Optional</code></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cliente de App-V en un equipo independiente</p></td>
<td align="left"><ol>
<li><p>Cree el documento XML del grupo de conexiones y establezca el <strong> atributo de etiqueta de paquete </strong> <strong> IsOptional </strong> en <strong> "true".</strong></p></li>
<li><p>Use los siguientes cmdlets para agregar y habilitar el grupo de conexión:</p>
<ul>
<li><p>Add-AppvClientConnectionGroup</p></li>
<li><p>Enable-AppvClientConnectionGroup</p></li>
</ul></li>
</ol>
<p><strong>Ejemplo de documento XML de grupo de conexión con paquetes opcionales:</strong></p>
<pre class="syntax" space="preserve"><code>&lt;?xml version=&quot;1.0&quot; ?&gt;
&lt;AppConnectionGroup
   xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;
   AppConnectionGroupId=&quot;8105CCD5-244B-4BA1-8888-E321E688D2CB&quot;
   VersionId=&quot;84CE3797-F1CB-4475-A223-757918929EB4&quot;
   DisplayName=&quot;Contoso Software Connection Group&quot; &gt;
&lt;Packages&gt;
&lt;Package
   PackageId=&quot;7735d1a8-5ef9-4df9-a1cf-3aa92ef54fe7&quot;
   VersionId=&quot;ec560d6f-e62e-48eb-a9e5-7c52a8c2e149&quot;
   DisplayName=&quot;Contoso Business Manager&quot;
/&gt;

&lt;Package
   PackageId=&quot;fc6fe0f7-be3d-4643-b37d-fc3f62d4dd5c&quot;
   VersionId=&quot;c67a71cd-3542-4a48-93e8-20c643c50970&quot;
   DisplayName=&quot;Contoso Forms&quot;
   IsOptional=&quot;false&quot;
/&gt;

&lt;Package
   PackageId=&quot;8f6301a5-4348-4039-9560-b27a5bb72711&quot;
   VersionId=&quot;6c694b45-3e19-46c6-a327-d159aa39e1d2&quot;
   DisplayName=&quot;Contoso Tax&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;Package
   PackageId=&quot;89d701bc-d507-4299-b6b6-000000003472&quot;
   VersionId=&quot;*&quot;
   DisplayName=&quot;Contoso Accounts&quot;
   IsOptional=&quot;true&quot;
/&gt;

&lt;/Packages&gt;
&lt;/AppConnectionGroup&gt;</code></pre></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Con versiones anteriores a App-V 5,0 SP3</strong></p></td>
<td align="left"><p>Tenía que crear muchos grupos de conexión para hacer que las combinaciones de aplicaciones y complementos específicas estén disponibles para usuarios específicos.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-unpub-del-optl-pkg"></a>Cancelar la publicación o la eliminación de un paquete opcional, o bien, anular la publicación de un paquete opcional y volver a publicarlo más adelante, sin cambiar el grupo de conexión


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Descripción de la tarea</th>
<th align="left">Cómo realizar la tarea</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Con App-V 5,0 SP3</strong></p>
<p>Puede anular la publicación, eliminar o volver a publicar un paquete opcional, que se encuentra en un grupo de conexiones, sin tener que deshabilitar o volver a habilitar el grupo de conexión en el cliente de App-V.</p>
<p>También puede anular la publicación de un paquete opcional y volver a publicarlo más adelante sin tener que deshabilitar o volver a publicar el grupo de conexión.</p>
<p><strong>Ejemplo </strong> : Si publica un paquete opcional que contiene un complemento de Microsoft Office y desea quitar el complemento, puede anular la publicación del paquete sin tener que deshabilitar el grupo de conexión.</p></td>
<td align="left"><table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Pasos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de App-V: consola de administración</p></td>
<td align="left"><ul>
<li><p>Para anular la publicación del paquete: en la consola de administración, seleccione elegir la <strong> </strong> Página paquetes, haga clic con el botón secundario en el paquete en el que desea anular la publicación y haga clic en <strong> Anular publicación </strong> .</p></li>
<li><p>Para quitar un paquete opcional de un grupo de conexión, en la <strong> Página grupos de conexión </strong> , seleccione el paquete que desea quitar y haga clic en la flecha derecha para quitar el paquete del panel grupo de conexiones en la parte inferior izquierda.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente de App-V en un equipo independiente</p></td>
<td align="left"><p>Use los siguientes cmdlets existentes:</p>
<ul>
<li><p>Anulación de la publicación-AppvClientPackage</p></li>
<li><p>Remove-AppvClientPackage</p></li>
</ul>
<p>Para obtener más información, vea <a href="how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md" data-raw-source="[How to Manage App-V 5.0 Packages Running on a Stand-Alone Computer by Using PowerShell](how-to-manage-app-v-50-packages-running-on-a-stand-alone-computer-by-using-powershell.md)"> Cómo administrar paquetes de App-V 5,0 que se ejecutan en un equipo independiente mediante PowerShell </a> .</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Con versiones anteriores a App-V 5,0 SP3</strong></p></td>
<td align="left"><p>Usted tenía que:</p>
<ol>
<li><p>Quite el grupo de conexiones de cada equipo cliente de App-V en el que se haya habilitado.</p></li>
<li><p>Anula la publicación del paquete.</p></li>
<li><p>Quite el paquete de la definición del grupo de conexión.</p></li>
<li><p>Vuelva a publicar el grupo de conexión.</p></li>
</ol></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-reqs-using-cg"></a>Requisitos para usar paquetes opcionales en grupos de conexión


Revise los siguientes requisitos antes de usar paquetes opcionales en grupos de conexión:

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
<td align="left"><p>Los grupos de conexión deben contener al menos un paquete no opcional.</p></td>
<td align="left"><ul>
<li><p>Compruebe detenidamente que cumple con este requisito, ya que el servidor de App-V y el cmdlet de PowerShell no validan que se cumpla el requisito.</p></li>
<li><p>Si por error crea un grupo de conexiones que no contenga al menos un paquete no opcional, y el usuario final intenta abrir una aplicación empaquetada en ese grupo de conexiones, el grupo de conexión fallará.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>Los grupos de conexión publicados por el usuario pueden contener paquetes que se publican globalmente o al usuario.</p></li>
<li><p>Los grupos de conexión publicados globalmente deben contener solo paquetes publicados globalmente.</p></li>
</ul></td>
<td align="left"><p>Los grupos de conexión publicados globalmente deben contener paquetes que se publiquen globalmente para asegurarse de que los paquetes estarán disponibles al iniciar el entorno virtual del grupo de conexión.</p>
<p>Si intenta agregar o habilitar grupos de conexión publicados globalmente que contienen paquetes publicados por el usuario, se producirá un error en el grupo de conexión.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Debe publicar todos los paquetes no opcionales antes de publicar el grupo de conexión que contiene dichos paquetes.</p></td>
<td align="left"><p>El entorno virtual de un grupo de conexión no se puede iniciar si faltan paquetes no opcionales.</p>
<p>El cliente de App-V no puede Agregar o habilitar un grupo de conexión si no se han publicado paquetes no opcionales.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Antes de anular la publicación de un paquete publicado globalmente, asegúrese de que los grupos de conexión que tienen derecho a todos los usuarios de ese equipo ya no necesiten el paquete.</p></td>
<td align="left"><p>El sistema no comprueba si el paquete es parte del grupo de conexión de otro usuario. Al anular la publicación de un paquete global dejará de estar disponible para todos los usuarios de ese equipo, así que asegúrese de que los grupos de conexión de cada usuario ya no contengan el paquete, o bien haga que el paquete sea opcional.</p></td>
</tr>
</tbody>
</table>

 






## Temas relacionados


[Administración de grupos de conexión](managing-connection-groups.md)

 

 





