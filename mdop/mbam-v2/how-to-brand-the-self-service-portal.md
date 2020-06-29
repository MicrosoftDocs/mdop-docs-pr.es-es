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
# <span data-ttu-id="4edfb-103">Cómo poner la marca en el portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="4edfb-103">How to Brand the Self-Service Portal</span></span>


<span data-ttu-id="4edfb-104">Después de instalar el portal de autoservicio de administración y supervisión de Microsoft BitLocker (MBAM), puede personalizar el portal de autoservicio con el nombre de su compañía, la dirección URL del servicio de asistencia y el texto "aviso".</span><span class="sxs-lookup"><span data-stu-id="4edfb-104">After you install the Microsoft BitLocker Administration and Monitoring (MBAM) Self-Service Portal, you can brand the Self-Service Portal with your company name, Help Desk URL, and “notice” text.</span></span> <span data-ttu-id="4edfb-105">También puede cambiar el valor de tiempo de espera de la sesión para que la sesión del usuario final venza después de un período especificado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="4edfb-105">You can also change the Session Timeout setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="4edfb-106">Para establecer el tiempo de espera y la personalización de la sesión en el portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="4edfb-106">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="4edfb-107">Para establecer el tiempo de espera de la sesión del usuario final, inicie el **Administrador de servicios de Internet Information Server**o ejecute **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="4edfb-107">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="4edfb-108">Vaya a **sitios** &gt; **Microsoft BitLocker administración y supervisión** &gt; **SelfService** &gt; **ASP.net** &gt; **Estado de sesión**y cambie el valor de **tiempo de espera** en **configuración de cookies** al número de minutos después de los cuales la sesión de portal de autoservicio del usuario final va a expirar.</span><span class="sxs-lookup"><span data-stu-id="4edfb-108">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session will expire.</span></span> <span data-ttu-id="4edfb-109">El valor predeterminado es 5.</span><span class="sxs-lookup"><span data-stu-id="4edfb-109">The default is 5.</span></span> <span data-ttu-id="4edfb-110">Para deshabilitar la configuración de modo que no haya tiempo de espera, establezca el valor en **0**.</span><span class="sxs-lookup"><span data-stu-id="4edfb-110">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="4edfb-111">Para establecer los elementos de personalización de marca para el portal de autoservicio, inicie el **Administrador de servicios de información de Internet**o ejecute **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="4edfb-111">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="4edfb-112">Vaya a **sitios** &gt; **Microsoft BitLocker administración y supervisión** &gt; **SelfService** &gt; **configuración**de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4edfb-112">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="4edfb-113">En la columna **nombre** , seleccione el elemento que desee cambiar y cambie el valor predeterminado para que refleje el nombre que desea usar.</span><span class="sxs-lookup"><span data-stu-id="4edfb-113">From the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="4edfb-114">En la tabla siguiente se enumeran los valores que puede establecer.</span><span class="sxs-lookup"><span data-stu-id="4edfb-114">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="4edfb-115">Actúe</span><span class="sxs-lookup"><span data-stu-id="4edfb-115">Caution</span></span>**  
    <span data-ttu-id="4edfb-116">No cambie el valor de la columna Nombre (NombreCompañía \ \*), ya que el portal de autoservicio dejará de funcionar.</span><span class="sxs-lookup"><span data-stu-id="4edfb-116">Do not change the value in the Name column (CompanyName\*), as it will cause the Self-Service Portal to stop working.</span></span>



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



## <span data-ttu-id="4edfb-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4edfb-117">Related topics</span></span>


[<span data-ttu-id="4edfb-118">Implementación de la infraestructura de servidor de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="4edfb-118">Deploying the MBAM 2.0 Server Infrastructure</span></span>](deploying-the-mbam-20-server-infrastructure-mbam-2.md)









