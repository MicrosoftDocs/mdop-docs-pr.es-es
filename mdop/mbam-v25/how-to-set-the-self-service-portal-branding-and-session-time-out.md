---
title: Cómo establecer la marca de portal de autoservicio y el tiempo de espera de sesión
description: Cómo establecer la marca de portal de autoservicio y el tiempo de espera de sesión
author: dansimp
ms.assetid: 031eedfc-fade-4d2f-8771-b329e1d38c0d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e222880b2d5557ef15cd7a4efd6421b9972541f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812534"
---
# Cómo establecer la marca de portal de autoservicio y el tiempo de espera de sesión


Después de configurar el portal de autoservicio, puede marcarlo con el nombre de la compañía, la dirección URL del servicio de asistencia y el texto "aviso". También puede cambiar la configuración de tiempo de espera de la sesión para que la sesión del usuario final venza después de un período especificado de inactividad.

**Nota**  
También puede personalizar el portal de autoservicio mediante el cmdlet **enable-MbamWebApplication de** Windows PowerShell o el Asistente para la configuración del servidor de MBAM. Para obtener instrucciones sobre cómo usar el asistente, consulte [Cómo configurar las aplicaciones Web de MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).



**Nota**  
En las siguientes instrucciones, *SelfService* es el nombre del directorio virtual predeterminado para el portal de autoservicio. Es posible que haya usado un nombre diferente al configurar el portal de autoservicio.



**Para establecer el tiempo de espera y la personalización de la sesión en el portal de autoservicio**

1.  Para establecer el tiempo de espera de la sesión del usuario final, inicie el **Administrador de servicios de Internet Information Server**o ejecute **inetmgr.exe**.

2.  Vaya a **sitios** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.net** &gt; **Estado de sesión**y cambie el valor de **tiempo de espera** en **configuración de cookies** al número de minutos después de los cuales vence la sesión del portal de autoservicio del usuario final. El valor predeterminado es **5**. Para deshabilitar la configuración de modo que no haya tiempo de espera, establezca el valor en **0**.

3.  Para establecer los elementos de personalización de marca para el portal de autoservicio, inicie el **Administrador de servicios de Internet Information Server** o ejecute **inetmgr.exe**.

4.  Vaya a **sitios** &gt; **Microsoft BitLocker administración y supervisión** &gt; **SelfService** &gt; **configuración**de la aplicación.

5.  En la columna **nombre** , seleccione el elemento que desee cambiar y cambie el valor predeterminado para que refleje el nombre que desea usar. En la tabla siguiente se enumeran los valores que puede establecer.

    **Actúe**  
    No cambie el valor de la columna Name (CompanyName \ *), ya que el portal de autoservicio dejará de funcionar.



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Name</th>
<th align="left">Default value</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>ClientValidationEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>CompanyName</p></td>
<td align="left"><p>Contoso IT</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DisplayNotice</p></td>
<td align="left"><p>true</p></td>
</tr>
<tr class="even">
<td align="left"><p>HelpdeskText</p></td>
<td align="left"><p>Contact Helpdesk or IT Department</p></td>
</tr>
<tr class="odd">
<td align="left"><p>HelpdeskUrl</p></td>
<td align="left"><p>#</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, the HelpdeskUrl default value is empty.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryPath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390515](//go.microsoft.com/fwlink/?LinkID=390515)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery-1.10.2.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>jQueryValidatePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390516](//go.microsoft.com/fwlink/?LinkID=390516)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>jQueryValidateUnobtrusivePath</p></td>
<td align="left"><p>[//go.microsoft.com/fwlink/?LinkID=390517](//go.microsoft.com/fwlink/?LinkID=390517)</p>
<div class="alert">
<strong>Note</strong>  
<p>In MBAM 2.5 SP1, this has been changed to a local JavaScript file shipped with the product, located at ~/Scripts/jquery.validate.unobtrusive.min.js</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>NoticeTextPath</p></td>
<td align="left"><p>Notice.txt</p>
<div class="alert">
<strong>Note</strong>  
<p>You can edit the notice text either by using the Internet Information Services (IIS) Manager or by opening and changing the Notice.txt file in the installation directory.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>UnobtrusiveJavaScriptEnabled</p></td>
<td align="left"><p>true</p></td>
</tr>
</tbody>
</table>
~~~





## Temas relacionados


[Personalización del portal de autoservicio para la organización](customizing-the-self-service-portal-for-your-organization.md)



## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





