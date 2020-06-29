---
title: Cómo poner la marca en el portal de autoservicio
description: Cómo poner la marca en el portal de autoservicio
author: dansimp
ms.assetid: 3ef9e951-7c42-4f7f-b131-3765d39b3207
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe4f4efc5852042671711ba5780cc78055957ba8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825150"
---
# Cómo poner la marca en el portal de autoservicio


Después de instalar el portal de autoservicio de administración y supervisión de Microsoft BitLocker (MBAM), puede personalizar el portal de autoservicio con el nombre de su compañía, la dirección URL del servicio de asistencia y el texto "aviso". También puede cambiar el valor de tiempo de espera de la sesión para que la sesión del usuario final venza después de un período especificado de inactividad.

**Para establecer el tiempo de espera y la personalización de la sesión en el portal de autoservicio**

1.  Para establecer el tiempo de espera de la sesión del usuario final, inicie el **Administrador de servicios de Internet Information Server**o ejecute **inetmgr.exe**.

2.  Vaya a **sitios** &gt; **Microsoft BitLocker administración y supervisión** &gt; **SelfService** &gt; **ASP.net** &gt; **Estado de sesión**y cambie el valor de **tiempo de espera** en **configuración de cookies** al número de minutos después de los cuales la sesión de portal de autoservicio del usuario final va a expirar. El valor predeterminado es 5. Para deshabilitar la configuración de modo que no haya tiempo de espera, establezca el valor en **0**.

3.  Para establecer los elementos de personalización de marca para el portal de autoservicio, inicie el **Administrador de servicios de información de Internet**o ejecute **inetmgr.exe**.

4.  Vaya a **sitios** &gt; **Microsoft BitLocker administración y supervisión** &gt; **SelfService** &gt; **configuración**de la aplicación.

5.  En la columna **nombre** , seleccione el elemento que desee cambiar y cambie el valor predeterminado para que refleje el nombre que desea usar. En la tabla siguiente se enumeran los valores que puede establecer.

    **Actúe**  
    No cambie el valor de la columna Nombre (NombreCompañía \ *), ya que el portal de autoservicio dejará de funcionar.



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Default Value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CompanyName*</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText*</p></td>
<td align="left"><p>Contact Help Desk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl*</p></td>
<td align="left"><p>Http://www.microsoft.com</p></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/jQuery/jquery-1.7.2.min.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MicrosoftAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/3.5/MicrosoftAjax.js</p></td>
</tr>
<tr class="even">
<td align="left"><p>MicrosoftMvcAjaxPath</p></td>
<td align="left"><p>//ajax.aspnetcdn.com/ajax/mvc/2.0/MicrosoftMvcValidation.js</p></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the Notice text either by using the IIS Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>
~~~



## Temas relacionados


[Implementación de la infraestructura de servidor de MBAM 2.0](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









