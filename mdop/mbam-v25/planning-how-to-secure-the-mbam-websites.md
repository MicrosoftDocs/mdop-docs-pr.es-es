---
title: Planificación de cómo proteger los sitios web MBAM.
description: Planificación de cómo proteger los sitios web MBAM.
author: dansimp
ms.assetid: aea1d137-62cf-4da4-9989-541e0b5ad8d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 223c9397ad7933e11051c289c3dbcab63940fbc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825021"
---
# <span data-ttu-id="bee41-103">Planificación de cómo proteger los sitios web MBAM.</span><span class="sxs-lookup"><span data-stu-id="bee41-103">Planning How to Secure the MBAM Websites</span></span>


<span data-ttu-id="bee41-104">En este tema se describen los siguientes métodos para proteger el sitio web de administración y supervisión de Microsoft BitLocker (MBAM) 2,5 y el portal de autoservicio:</span><span class="sxs-lookup"><span data-stu-id="bee41-104">This topic describes the following methods for securing the Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 Administration and Monitoring Website and Self-Service Portal:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bee41-105">Método</span><span class="sxs-lookup"><span data-stu-id="bee41-105">Method</span></span></th>
<th align="left"><span data-ttu-id="bee41-106">¿Obligatorio u opcional?</span><span class="sxs-lookup"><span data-stu-id="bee41-106">Required or optional?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee41-107">Uso de certificados para proteger sitios web de MBAM</span><span class="sxs-lookup"><span data-stu-id="bee41-107">Using certificates to secure MBAM websites</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee41-108">Opcional, pero muy recomendable</span><span class="sxs-lookup"><span data-stu-id="bee41-108">Optional, but highly recommended</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee41-109">Registrar nombres principales de servicio (SPN) para la cuenta del grupo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="bee41-109">Registering Service Principal Names (SPN) for the application pool account</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee41-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="bee41-110">Required</span></span></p></td>
</tr>
</tbody>
</table>



<span data-ttu-id="bee41-111">Para obtener más información sobre cómo proteger la implementación de MBAM, consulte [consideraciones de seguridad de MBAM 2,5](mbam-25-security-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="bee41-111">For more information about how to secure your MBAM deployment, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md).</span></span>

## <span data-ttu-id="bee41-112">Uso de certificados para proteger sitios web de MBAM</span><span class="sxs-lookup"><span data-stu-id="bee41-112">Using certificates to secure MBAM websites</span></span>


<span data-ttu-id="bee41-113">Le recomendamos que use un certificado para asegurar la comunicación entre:</span><span class="sxs-lookup"><span data-stu-id="bee41-113">We recommend that you use a certificate to secure the communication between the:</span></span>

-   <span data-ttu-id="bee41-114">Cliente de MBAM y servicios Web</span><span class="sxs-lookup"><span data-stu-id="bee41-114">MBAM Client and the web services</span></span>

-   <span data-ttu-id="bee41-115">Explorador y el sitio web de administración y supervisión, y los sitios web del portal de autoservicio</span><span class="sxs-lookup"><span data-stu-id="bee41-115">Browser and the Administration and Monitoring Website and the Self-Service Portal websites</span></span>

<span data-ttu-id="bee41-116">Para obtener información sobre cómo solicitar e instalar un certificado, consulte [configuración de certificados de servidor de Internet](https://technet.microsoft.com/library/cc731977.aspx).</span><span class="sxs-lookup"><span data-stu-id="bee41-116">For information about requesting and installing a certificate, see [Configuring Internet Server Certificates](https://technet.microsoft.com/library/cc731977.aspx).</span></span>

**<span data-ttu-id="bee41-117">Nota</span><span class="sxs-lookup"><span data-stu-id="bee41-117">Note</span></span>**  
<span data-ttu-id="bee41-118">Puede configurar los sitios web y los servicios web en servidores diferentes solo si está usando Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bee41-118">You can configure the websites and web services on different servers only if you are using Windows PowerShell.</span></span> <span data-ttu-id="bee41-119">Si usa el Asistente para la configuración del servidor de MBAM para configurar los sitios web, debe configurar los sitios web y los servicios web en el mismo servidor.</span><span class="sxs-lookup"><span data-stu-id="bee41-119">If you use the MBAM Server Configuration wizard to configure the websites, you must configure the websites and the web services on the same server.</span></span>



<span data-ttu-id="bee41-120">Para proteger la comunicación entre los servicios web y las bases de datos, también recomendamos forzar el cifrado en SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bee41-120">To secure the communication between the web services and the databases, we also recommend that you force encryption in SQL Server.</span></span> <span data-ttu-id="bee41-121">Para obtener información sobre cómo proteger todas las conexiones a SQL Server, incluida la comunicación entre los servicios web y SQL Server, consulte [consideraciones de seguridad de MBAM 2,5](mbam-25-security-considerations.md#bkmk-secure-databases).</span><span class="sxs-lookup"><span data-stu-id="bee41-121">For information about securing all connections to SQL Server, including communication between the web services and SQL Server, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-secure-databases).</span></span>

## <span data-ttu-id="bee41-122">Registrar SPN para la cuenta del grupo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="bee41-122">Registering SPNs for the application pool account</span></span>


<span data-ttu-id="bee41-123">Para habilitar los servidores de MBAM para autenticar la comunicación desde el sitio web de administración y supervisión y el portal de autoservicio, debe registrar un nombre principal de servicio (SPN) para el nombre de host en la cuenta de dominio que está usando para el grupo de aplicaciones Web.</span><span class="sxs-lookup"><span data-stu-id="bee41-123">To enable the MBAM Servers to authenticate communication from the Administration and Monitoring Website and the Self-Service Portal, you must register a Service Principal Name (SPN) for the host name under the domain account that you are using for the web application pool.</span></span>

<span data-ttu-id="bee41-124">Este tema contiene instrucciones sobre cómo registrar SPN para los siguientes tipos de nombres de host:</span><span class="sxs-lookup"><span data-stu-id="bee41-124">This topic contains instructions on how to register SPNs for the following types of host names:</span></span>

-   <span data-ttu-id="bee41-125">Nombre de dominio completo</span><span class="sxs-lookup"><span data-stu-id="bee41-125">Fully qualified domain name</span></span>

-   <span data-ttu-id="bee41-126">Nombre NetBIOS</span><span class="sxs-lookup"><span data-stu-id="bee41-126">NetBIOS name</span></span>

-   <span data-ttu-id="bee41-127">Nombre virtual</span><span class="sxs-lookup"><span data-stu-id="bee41-127">Virtual name</span></span>

### <span data-ttu-id="bee41-128">Antes de crear SPN para una instalación de MBAM inicial</span><span class="sxs-lookup"><span data-stu-id="bee41-128">Before you create SPNs for an initial MBAM installation</span></span>

<span data-ttu-id="bee41-129">Revise la información de la siguiente tabla antes de empezar a crear SPN.</span><span class="sxs-lookup"><span data-stu-id="bee41-129">Review the information in the following table before you start creating SPNs.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bee41-130">Tarea o elemento</span><span class="sxs-lookup"><span data-stu-id="bee41-130">Task or item</span></span></th>
<th align="left"><span data-ttu-id="bee41-131">Más información</span><span class="sxs-lookup"><span data-stu-id="bee41-131">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee41-132">Crear una cuenta de servicio en servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="bee41-132">Create a service account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee41-133">La cuenta de servicio es una cuenta de usuario que se crea en AD DS para proporcionar seguridad a los sitios web de MBAM.</span><span class="sxs-lookup"><span data-stu-id="bee41-133">The service account is a user account that you create in AD DS to provide security for the MBAM websites.</span></span> <span data-ttu-id="bee41-134">Los sitios web de MBAM se ejecutan en un grupo de aplicaciones, cuya identidad es el nombre de la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="bee41-134">The MBAM websites run under an application pool, whose identity is the name of the service account.</span></span> <span data-ttu-id="bee41-135">Los SPN se registran en la cuenta del grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bee41-135">The SPNs are then registered in the application pool account.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="bee41-136">Nota</span><span class="sxs-lookup"><span data-stu-id="bee41-136">Note</span></span></strong><br/><p><span data-ttu-id="bee41-137">Debe usar la misma cuenta de grupo de aplicaciones para todos los servidores Web.</span><span class="sxs-lookup"><span data-stu-id="bee41-137">You must use the same application pool account for all web servers.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee41-138">Compruebe que la cuenta del grupo IIS-IUSRS o la cuenta del grupo de aplicaciones le han concedido los derechos necesarios.</span><span class="sxs-lookup"><span data-stu-id="bee41-138">Verify that either the IIS-IUSRS group account or the application pool account has been granted the necessary rights.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee41-139">Para comprobar esto, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="bee41-139">To check this, follow these steps:</span></span></p>
<ol>
<li><p><span data-ttu-id="bee41-140">Abra el <strong> Editor de directivas de seguridad local </strong> y expanda el <strong> nodo directivas locales </strong> .</span><span class="sxs-lookup"><span data-stu-id="bee41-140">Open the <strong>Local Security Policy editor</strong> and expand the <strong>Local Policies</strong> node.</span></span></p></li>
<li><p><span data-ttu-id="bee41-141">Seleccione el <strong> nodo asignación de derechos de usuario </strong> y, después, haga doble clic en la <strong> configuración de directiva suplantar a un cliente después de la autenticación </strong> e <strong> iniciar sesión como un trabajo por lotes </strong> en el panel derecho.</span><span class="sxs-lookup"><span data-stu-id="bee41-141">Select the <strong>User Rights Assignment</strong> node, and double-click the <strong>Impersonate a client after authentication</strong> and <strong>Log on as a batch job</strong> Group Policy settings in the right pane.</span></span></p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee41-142">Si configura los sitios web de MBAM con una cuenta de administrador de dominio, MBAM creará los SPN.</span><span class="sxs-lookup"><span data-stu-id="bee41-142">If you configure the MBAM websites by using a domain administrative account, MBAM will create the SPNs for you.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee41-143">Si configura los sitios web de MBAM con una cuenta de administrador de dominio, siga los pasos que se indican en este tema para registrar los SPN manualmente para el tipo de nombre de host que está usando.</span><span class="sxs-lookup"><span data-stu-id="bee41-143">If you configure the MBAM websites by using a domain administrative account, follow the steps in this topic to register SPNs manually for the type of host name that you are using.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="bee41-144">Registrar SPN al usar un nombre de host de dominio completo</span><span class="sxs-lookup"><span data-stu-id="bee41-144">Registering SPNs when you use a fully qualified domain host name</span></span>

<span data-ttu-id="bee41-145">Si usa un nombre de host de dominio completo al configurar MBAM, debe registrar solo un SPN, como se muestra en el siguiente ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bee41-145">If you use a fully qualified domain host name when you configure MBAM, you have to register only one SPN, as shown in the following example.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bee41-146">Lo que debe hacer</span><span class="sxs-lookup"><span data-stu-id="bee41-146">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="bee41-147">Ejemplos y más información</span><span class="sxs-lookup"><span data-stu-id="bee41-147">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee41-148">Registre un SPN para el nombre de dominio completo.</span><span class="sxs-lookup"><span data-stu-id="bee41-148">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="bee41-149">El nombre de host completo es <strong> mybitlockerrecovery.contoso.com </strong> y la cuenta de dominio que se usa para el grupo de aplicaciones web es <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="bee41-149">The fully qualified host name is <strong>mybitlockerrecovery.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee41-150">Configure la delegación restringida para el SPN que está registrando para la cuenta del grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bee41-150">Configure constrained delegation for the SPN that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="bee41-151">Configuración de la delegación restringida</span><span class="sxs-lookup"><span data-stu-id="bee41-151">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="bee41-152">Este requisito solo se aplica a MBAM 2,5; no es necesario en MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="bee41-152">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <span data-ttu-id="bee41-153">Registrar SPN al usar un nombre de host NetBIOS</span><span class="sxs-lookup"><span data-stu-id="bee41-153">Registering SPNs when you use a NetBIOS host name</span></span>

<span data-ttu-id="bee41-154">Si usa un nombre de host NetBIOS al configurar MBAM, registre un SPN para el nombre NetBIOS y otro SPN para el nombre de dominio completo, como se muestra en los siguientes ejemplos.</span><span class="sxs-lookup"><span data-stu-id="bee41-154">If you use a NetBIOS host name when you configure MBAM, register one SPN for the NetBIOS name, and another SPN for the fully qualified domain name, as shown in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bee41-155">Lo que debe hacer</span><span class="sxs-lookup"><span data-stu-id="bee41-155">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="bee41-156">Ejemplos y más información</span><span class="sxs-lookup"><span data-stu-id="bee41-156">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee41-157">Registre un SPN para el nombre de host NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="bee41-157">Register an SPN for the NetBIOS host name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="bee41-158">El nombre de host NetBIOS es <strong> nbname01 </strong> y la cuenta de dominio que se usa para el grupo de aplicaciones web es <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="bee41-158">The NetBIOS host name is <strong>nbname01</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee41-159">Registre un SPN para el nombre de dominio completo.</span><span class="sxs-lookup"><span data-stu-id="bee41-159">Register an SPN for the fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="bee41-160">El nombre de dominio completo es <strong> nbname01.contoso.com </strong> y la cuenta de dominio que se usa para el grupo de aplicaciones web es <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="bee41-160">The fully qualified domain name is <strong>nbname01.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee41-161">Configure la delegación restringida para los SPN que está registrando para la cuenta del grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bee41-161">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="bee41-162">Configuración de la delegación restringida</span><span class="sxs-lookup"><span data-stu-id="bee41-162">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="bee41-163">Este requisito solo se aplica a MBAM 2,5; no es necesario en MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="bee41-163">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a><span data-ttu-id="bee41-164">Registrar SPN al usar un nombre de host virtual</span><span class="sxs-lookup"><span data-stu-id="bee41-164">Registering SPNs when you use a virtual host name</span></span>

<span data-ttu-id="bee41-165">Si configura MBAM con un nombre de host virtual que sea un nombre de dominio completo, registre solo un SPN para el nombre de host virtual.</span><span class="sxs-lookup"><span data-stu-id="bee41-165">If you configure MBAM with a virtual host name that is a fully qualified domain name, register only one SPN for the virtual host name.</span></span> <span data-ttu-id="bee41-166">Si el nombre de host virtual que configure no es un nombre de dominio completo, debe crear un segundo SPN que especifique el nombre de dominio completo, como se describe en los siguientes ejemplos.</span><span class="sxs-lookup"><span data-stu-id="bee41-166">If the virtual host name that you configure is not a fully qualified domain name, you must create a second SPN that specifies the fully qualified domain name, as described in the following examples.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bee41-167">Lo que debe hacer</span><span class="sxs-lookup"><span data-stu-id="bee41-167">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="bee41-168">Ejemplos y más información</span><span class="sxs-lookup"><span data-stu-id="bee41-168">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee41-169">Si el nombre de host virtual es un nombre de dominio completo, como en este ejemplo, registre solo un SPN.</span><span class="sxs-lookup"><span data-stu-id="bee41-169">If your virtual host name is a fully qualified domain name, as in this example, register only one SPN.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="bee41-170">En el ejemplo, el nombre de host virtual es <strong> mbamvirtual.contoso.com </strong> y la cuenta de dominio que se usa para el grupo de aplicaciones web es <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="bee41-170">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee41-171">Registre este SPN adicional si el nombre de host virtual no es un nombre de dominio completo.</span><span class="sxs-lookup"><span data-stu-id="bee41-171">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="bee41-172">En el ejemplo, el nombre de host virtual es <strong> mbamvirtual </strong> y la cuenta de dominio que se usa para el grupo de aplicaciones web es <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="bee41-172">In the example, the virtual host name is <strong>mbamvirtual</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee41-173">Registre este SPN adicional si el nombre de host virtual no es un nombre de dominio completo.</span><span class="sxs-lookup"><span data-stu-id="bee41-173">Register this additional SPN if your virtual host name is not a fully qualified domain name.</span></span></p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p><span data-ttu-id="bee41-174">En el ejemplo, el nombre de host virtual es <strong> mbamvirtual.contoso.com </strong> y la cuenta de dominio que se usa para el grupo de aplicaciones web es <strong> contoso\mbamapppooluser </strong> .</span><span class="sxs-lookup"><span data-stu-id="bee41-174">In the example, the virtual host name is <strong>mbamvirtual.contoso.com</strong>, and the domain account used for the web application pool is <strong>contoso\mbamapppooluser</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee41-175">En el servidor DNS (servidor de nombres de dominio), cree un "registro" para el nombre de host personalizado y señale a un servidor web o a un equilibrador de carga.</span><span class="sxs-lookup"><span data-stu-id="bee41-175">On the Domain Name Server (DNS) server, create an “A record” for the custom host name and point it to a web server or a load balancer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee41-176">Consulte la sección "para configurar registros de host A DNS" en <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> configurar registros de host DNS </a> .</span><span class="sxs-lookup"><span data-stu-id="bee41-176">See the “To configure DNS Host A Records” section in <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)">Configure DNS Host Records</a>.</span></span></p>
<p><span data-ttu-id="bee41-177">Le recomendamos que use un registro en lugar de CNAMES.</span><span class="sxs-lookup"><span data-stu-id="bee41-177">We recommend that you use A records instead of CNAMES.</span></span> <span data-ttu-id="bee41-178">Si usa CNAMES para apuntar a la dirección de dominio, también debe registrar los SPN para el nombre del servidor Web en la cuenta del grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bee41-178">If you use CNAMES to point to the domain address, you must also register SPNs for the web server name in the application pool account.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee41-179">Configure la delegación restringida para los SPN que está registrando para la cuenta del grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bee41-179">Configure constrained delegation for the SPNs that you are registering for the application pool account.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)"><span data-ttu-id="bee41-180">Configuración de la delegación restringida</span><span class="sxs-lookup"><span data-stu-id="bee41-180">Configuring Constrained Delegation</span></span></a></p>
<p><span data-ttu-id="bee41-181">Este requisito solo se aplica a MBAM 2,5; no es necesario en MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="bee41-181">This requirement only applies to MBAM 2.5; it is not necessary in MBAM 2.5 SP1.</span></span></p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a><span data-ttu-id="bee41-182">Registrar un SPN al actualizar de versiones anteriores de MBAM</span><span class="sxs-lookup"><span data-stu-id="bee41-182">Registering an SPN when you upgrade from previous versions of MBAM</span></span>

<span data-ttu-id="bee41-183">Complete los pasos de esta sección solo si desea:</span><span class="sxs-lookup"><span data-stu-id="bee41-183">Complete the steps in this section only if you want to:</span></span>

-   <span data-ttu-id="bee41-184">Actualizar desde una versión anterior de MBAM.</span><span class="sxs-lookup"><span data-stu-id="bee41-184">Upgrade from a previous version of MBAM.</span></span>

-   <span data-ttu-id="bee41-185">Ejecute los sitios web en MBAM 2,5 en una configuración distribuida o con equilibrio de carga, y actualmente está ejecutando una configuración que no tiene equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="bee41-185">Run the websites in MBAM 2.5 in a load-balanced or distributed configuration, and you are currently running in a configuration that is not load balanced.</span></span>

<span data-ttu-id="bee41-186">Si ya ha registrado SPN en la cuenta del equipo, en lugar de en una cuenta del grupo de aplicaciones, MBAM usa los SPN existentes y no puede configurar los sitios web en una configuración distribuida o con equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="bee41-186">If you already registered SPNs on the machine account rather than in an application pool account, MBAM uses the existing SPNs, and you cannot configure the websites in a load-balanced or distributed configuration.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bee41-187">Lo que debe hacer</span><span class="sxs-lookup"><span data-stu-id="bee41-187">What you need to do</span></span></th>
<th align="left"><span data-ttu-id="bee41-188">Ejemplos y más información</span><span class="sxs-lookup"><span data-stu-id="bee41-188">Examples and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee41-189">Crear una cuenta de grupo de aplicaciones en los servicios de dominio de Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="bee41-189">Create an application pool account in Active Directory Domain Services (AD DS).</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee41-190">Quitar los sitios web y servicios web actualmente instalados.</span><span class="sxs-lookup"><span data-stu-id="bee41-190">Remove the currently installed websites and web services.</span></span></p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)"><span data-ttu-id="bee41-191">Quitar las funciones o software de servidor MBAM</span><span class="sxs-lookup"><span data-stu-id="bee41-191">Removing MBAM Server Features or Software</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee41-192">Quitar SPN de la cuenta de la máquina.</span><span class="sxs-lookup"><span data-stu-id="bee41-192">Remove SPNs from the machine account.</span></span></p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee41-193">Registrar SPN en la cuenta del grupo de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bee41-193">Register SPNs in the application pool account.</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee41-194">Siga los pasos para <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)"> registrar SPN cuando usa un nombre de host virtual </a> .</span><span class="sxs-lookup"><span data-stu-id="bee41-194">Follow the steps for <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)">Registering SPNs when you use a virtual host name</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="bee41-195">Vuelva a configurar las aplicaciones web y los servicios Web.</span><span class="sxs-lookup"><span data-stu-id="bee41-195">Reconfigure the web applications and web services.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)"><span data-ttu-id="bee41-196">Cómo configurar las aplicaciones web de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="bee41-196">How to Configure the MBAM 2.5 Web Applications</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="bee41-197">Siga uno de estos procedimientos, según el método que use para la configuración:</span><span class="sxs-lookup"><span data-stu-id="bee41-197">Do one of the following, depending on the method you use for the configuration:</span></span></p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="bee41-198">Método</span><span class="sxs-lookup"><span data-stu-id="bee41-198">Method</span></span></th>
<th align="left"><span data-ttu-id="bee41-199">Detalles</span><span class="sxs-lookup"><span data-stu-id="bee41-199">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="bee41-200">Asistente para la configuración del servidor de MBAM</span><span class="sxs-lookup"><span data-stu-id="bee41-200">MBAM Server Configuration wizard</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="bee41-201">Escriba la cuenta del grupo de aplicaciones en el <strong> campo de cuenta de dominio del grupo de aplicaciones de servicio Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="bee41-201">Enter the application pool account in the <strong>Web service application pool domain account</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> <span data-ttu-id="bee41-202">Cmdlet de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bee41-202">Windows PowerShell cmdlet</span></span></p></td>
<td align="left"><p><span data-ttu-id="bee41-203">Escriba la cuenta en el <code>WebServiceApplicationPoolCredential</code> parámetro.</span><span class="sxs-lookup"><span data-stu-id="bee41-203">Enter the account in the <code>WebServiceApplicationPoolCredential</code> parameter.</span></span></p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="bee41-204">Importante</span><span class="sxs-lookup"><span data-stu-id="bee41-204">Important</span></span></strong><br/><p><span data-ttu-id="bee41-205">El nombre de host que escriba debe tener el mismo nombre que el nombre de host virtual para el que está creando los SPN.</span><span class="sxs-lookup"><span data-stu-id="bee41-205">The host name that you enter must be the same name as the virtual host name for which you are creating the SPNs.</span></span> <span data-ttu-id="bee41-206">Además, en su granja de servidores Web, los nombres de host y las credenciales del grupo de aplicaciones deben ser los mismos en todos los servidores que esté configurando.</span><span class="sxs-lookup"><span data-stu-id="bee41-206">Also, in your web farm, the host names and the application pool credentials must be the same on every server that you are configuring.</span></span></p>
</div>
<div>

</div>
<p><span data-ttu-id="bee41-207">Cuando MBAM configura las aplicaciones Web, intentará registrar los SPN, pero puede hacerlo solo si tiene derechos de administrador de dominio en el servidor en el que está instalando MBAM.</span><span class="sxs-lookup"><span data-stu-id="bee41-207">When MBAM configures the web applications, it will try to register the SPNs for you, but it can do so only if you have Domain Admin rights on the server on which you are installing MBAM.</span></span> <span data-ttu-id="bee41-208">Si no tiene estos derechos, puede completar la configuración, pero tendrá que configurar los SPN antes o después de configurar MBAM.</span><span class="sxs-lookup"><span data-stu-id="bee41-208">If you do not have these rights, you can complete the configuration, but you will have to set the SPNs before or after you configure MBAM.</span></span></p></td>
</tr>
</tbody>
</table>

## <span data-ttu-id="bee41-209">Configuración de filtrado de solicitudes obligatorias</span><span class="sxs-lookup"><span data-stu-id="bee41-209">Required Request Filtering Settings</span></span>

 <span data-ttu-id="bee41-210">Para que la aplicación funcione según lo esperado, es necesario ' permitir extensiones de nombre de archivo que no se hayan puesto en la lista '.</span><span class="sxs-lookup"><span data-stu-id="bee41-210">'Allow unlisted file name extensions' is required for the application to operate as expected.</span></span>  <span data-ttu-id="bee41-211">Para ello, vaya a la ' supervisión y administración de Microsoft BitLocker '-> filtrar solicitudes: > configuración de características de edición.</span><span class="sxs-lookup"><span data-stu-id="bee41-211">This can be found by navigating to the 'Microsoft BitLocker Administration and Monitoring' -> Request Filtering -> Edit Feature Settings.</span></span>


## <span data-ttu-id="bee41-212">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bee41-212">Related topics</span></span>


[<span data-ttu-id="bee41-213">Preparación del entorno para MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="bee41-213">Preparing your Environment for MBAM 2.5</span></span>](preparing-your-environment-for-mbam-25.md)

[<span data-ttu-id="bee41-214">Requisitos previos de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="bee41-214">MBAM 2.5 Deployment Prerequisites</span></span>](mbam-25-deployment-prerequisites.md)





## <span data-ttu-id="bee41-215">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="bee41-215">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="bee41-216">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="bee41-216">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="bee41-217">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="bee41-217">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>



