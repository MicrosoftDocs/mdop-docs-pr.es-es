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
# <span data-ttu-id="2b8e0-103">Cómo establecer la marca de portal de autoservicio y el tiempo de espera de sesión</span><span class="sxs-lookup"><span data-stu-id="2b8e0-103">How to Set the Self-Service Portal Branding and Session Time-out</span></span>


<span data-ttu-id="2b8e0-104">Después de configurar el portal de autoservicio, puede marcarlo con el nombre de la compañía, la dirección URL del servicio de asistencia y el texto "aviso".</span><span class="sxs-lookup"><span data-stu-id="2b8e0-104">After you configure the Self-Service Portal, you can brand it with your company name, Help Desk URL, and "notice" text.</span></span> <span data-ttu-id="2b8e0-105">También puede cambiar la configuración de tiempo de espera de la sesión para que la sesión del usuario final venza después de un período especificado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="2b8e0-105">You can also change the Session Time-out setting to make the end user’s session expire after a specified period of inactivity.</span></span>

**<span data-ttu-id="2b8e0-106">Nota</span><span class="sxs-lookup"><span data-stu-id="2b8e0-106">Note</span></span>**  
<span data-ttu-id="2b8e0-107">También puede personalizar el portal de autoservicio mediante el cmdlet **enable-MbamWebApplication de** Windows PowerShell o el Asistente para la configuración del servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="2b8e0-107">You can also brand the Self-Service Portal by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet or the MBAM Server Configuration wizard.</span></span> <span data-ttu-id="2b8e0-108">Para obtener instrucciones sobre cómo usar el asistente, consulte [Cómo configurar las aplicaciones Web de MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).</span><span class="sxs-lookup"><span data-stu-id="2b8e0-108">For instructions on using the wizard, see [How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md).</span></span>



**<span data-ttu-id="2b8e0-109">Nota</span><span class="sxs-lookup"><span data-stu-id="2b8e0-109">Note</span></span>**  
<span data-ttu-id="2b8e0-110">En las siguientes instrucciones, *SelfService* es el nombre del directorio virtual predeterminado para el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="2b8e0-110">In the following instructions, *SelfService* is the default virtual directory name for the Self-Service Portal.</span></span> <span data-ttu-id="2b8e0-111">Es posible que haya usado un nombre diferente al configurar el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="2b8e0-111">You might have used a different name when you configured the Self-Service Portal.</span></span>



**<span data-ttu-id="2b8e0-112">Para establecer el tiempo de espera y la personalización de la sesión en el portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="2b8e0-112">To set the session time-out and branding for the Self-Service Portal</span></span>**

1.  <span data-ttu-id="2b8e0-113">Para establecer el tiempo de espera de la sesión del usuario final, inicie el **Administrador de servicios de Internet Information Server**o ejecute **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="2b8e0-113">To set the time-out period for the end user’s session, start the **Internet Information Services Manager**, or run **inetmgr.exe**.</span></span>

2.  <span data-ttu-id="2b8e0-114">Vaya a **sitios** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.net** &gt; **Estado de sesión**y cambie el valor de **tiempo de espera** en **configuración de cookies** al número de minutos después de los cuales vence la sesión del portal de autoservicio del usuario final.</span><span class="sxs-lookup"><span data-stu-id="2b8e0-114">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **ASP.NET** &gt; **Session State**, and change the **Time-out** value under **Cookie Settings** to the number of minutes after which the end user’s Self-Service Portal session expires.</span></span> <span data-ttu-id="2b8e0-115">El valor predeterminado es **5**.</span><span class="sxs-lookup"><span data-stu-id="2b8e0-115">The default value is **5**.</span></span> <span data-ttu-id="2b8e0-116">Para deshabilitar la configuración de modo que no haya tiempo de espera, establezca el valor en **0**.</span><span class="sxs-lookup"><span data-stu-id="2b8e0-116">To disable the setting so that there is no time-out, set the value to **0**.</span></span>

3.  <span data-ttu-id="2b8e0-117">Para establecer los elementos de personalización de marca para el portal de autoservicio, inicie el **Administrador de servicios de Internet Information Server** o ejecute **inetmgr.exe**.</span><span class="sxs-lookup"><span data-stu-id="2b8e0-117">To set the branding items for the Self-Service Portal, start the **Internet Information Services Manager** or run **inetmgr.exe**.</span></span>

4.  <span data-ttu-id="2b8e0-118">Vaya a **sitios** &gt; **Microsoft BitLocker administración y supervisión** &gt; **SelfService** &gt; **configuración**de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b8e0-118">Browse to **Sites** &gt; **Microsoft BitLocker Administration and Monitoring** &gt; **SelfService** &gt; **Application Settings**.</span></span>

5.  <span data-ttu-id="2b8e0-119">En la columna **nombre** , seleccione el elemento que desee cambiar y cambie el valor predeterminado para que refleje el nombre que desea usar.</span><span class="sxs-lookup"><span data-stu-id="2b8e0-119">In the **Name** column, select the item that you want to change, and change the default value to reflect the name that you want to use.</span></span> <span data-ttu-id="2b8e0-120">En la tabla siguiente se enumeran los valores que puede establecer.</span><span class="sxs-lookup"><span data-stu-id="2b8e0-120">The following table lists the values that you can set.</span></span>

    **<span data-ttu-id="2b8e0-121">Actúe</span><span class="sxs-lookup"><span data-stu-id="2b8e0-121">Caution</span></span>**  
    <span data-ttu-id="2b8e0-122">No cambie el valor de la columna Name (CompanyName \ \*), ya que el portal de autoservicio dejará de funcionar.</span><span class="sxs-lookup"><span data-stu-id="2b8e0-122">Do not change the value in the Name column (CompanyName\*), as it will cause Self-Service Portal to stop working.</span></span>



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





## <span data-ttu-id="2b8e0-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2b8e0-123">Related topics</span></span>


[<span data-ttu-id="2b8e0-124">Personalización del portal de autoservicio para la organización</span><span class="sxs-lookup"><span data-stu-id="2b8e0-124">Customizing the Self-Service Portal for Your Organization</span></span>](customizing-the-self-service-portal-for-your-organization.md)



## <span data-ttu-id="2b8e0-125">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="2b8e0-125">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="2b8e0-126">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="2b8e0-126">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="2b8e0-127">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="2b8e0-127">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





