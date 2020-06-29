---
title: Notas de la versión de MBAM 1.0
description: Notas de la versión de MBAM 1.0
author: dansimp
ms.assetid: d82fddde-c360-48ef-86a0-d9b5fe066861
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 705fd1b936da1454081dd14a7f075f642fc4a405
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826030"
---
# <span data-ttu-id="edf10-103">Notas de la versión de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="edf10-103">Release Notes for MBAM 1.0</span></span>


**<span data-ttu-id="edf10-104">Para buscar un problema específico en estas notas de la versión, presione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="edf10-104">To search for a specific issue in these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="edf10-105">Lea estas notas de la versión minuciosamente antes de instalar la administración y supervisión de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="edf10-105">Read these release notes thoroughly before you install Microsoft BitLocker Administration and Monitoring (MBAM).</span></span>

<span data-ttu-id="edf10-106">Estas notas de la versión contienen información necesaria para instalar MBAM correctamente.</span><span class="sxs-lookup"><span data-stu-id="edf10-106">These release notes contain information that is required to successfully install MBAM.</span></span> <span data-ttu-id="edf10-107">Las notas de la versión también contienen información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="edf10-107">The release notes also contain information that is not available in the product documentation.</span></span> <span data-ttu-id="edf10-108">Si hay una diferencia entre estas notas de la versión y otra documentación de MBAM, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="edf10-108">If there is a difference between these release notes and other MBAM documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="edf10-109">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="edf10-109">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="edf10-110">Acerca de la documentación del producto</span><span class="sxs-lookup"><span data-stu-id="edf10-110">About the Product Documentation</span></span>


<span data-ttu-id="edf10-111">Para obtener información sobre la documentación de MBAM, consulte la página de inicio de MBAM en Microsoft TechNet.</span><span class="sxs-lookup"><span data-stu-id="edf10-111">For information about MBAM documentation, see the MBAM home page on Microsoft TechNet.</span></span>

<span data-ttu-id="edf10-112">Para obtener una copia descargable de la documentación de MBAM, consulte <https://go.microsoft.com/fwlink/p/?LinkId=225356> en el centro de descarga de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="edf10-112">To obtain a downloadable copy of the MBAM documentation, see <https://go.microsoft.com/fwlink/p/?LinkId=225356> on the Microsoft Download Center.</span></span>

## <span data-ttu-id="edf10-113">Enviar comentarios</span><span class="sxs-lookup"><span data-stu-id="edf10-113">Provide Feedback</span></span>


<span data-ttu-id="edf10-114">Nos interesan tus comentarios en MBAM.</span><span class="sxs-lookup"><span data-stu-id="edf10-114">We are interested in your feedback on MBAM.</span></span> <span data-ttu-id="edf10-115">Puedes enviar tus comentarios a <mdopdocs@microsoft.com> .</span><span class="sxs-lookup"><span data-stu-id="edf10-115">You can send your feedback to <mdopdocs@microsoft.com>.</span></span>

<span data-ttu-id="edf10-116">**Nota:**  Esta dirección de correo electrónico no es un canal de soporte técnico, pero tus comentarios nos ayudarán a planificar futuros cambios en nuestra documentación y versiones de productos.</span><span class="sxs-lookup"><span data-stu-id="edf10-116">**Note** This email address is not a support channel, but your feedback will help us to plan for future changes in our documentation and product releases.</span></span>

 

<span data-ttu-id="edf10-117">Para obtener la información más reciente acerca de MDOP y recursos de aprendizaje adicionales, consulte la página [experiencia de información de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .</span><span class="sxs-lookup"><span data-stu-id="edf10-117">For the latest information about MDOP and additional learning resources, see the [MDOP Information Experience](https://go.microsoft.com/fwlink/p/?LinkId=236032) page.</span></span>

<span data-ttu-id="edf10-118">Para obtener más información sobre las nuevas actualizaciones o para proporcionar comentarios, síganos en [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span><span class="sxs-lookup"><span data-stu-id="edf10-118">For more information about new updates or to provide feedback, follow us on [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) or [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).</span></span>

## <span data-ttu-id="edf10-119">Problemas conocidos con MBAM 1,0</span><span class="sxs-lookup"><span data-stu-id="edf10-119">Known Issues with MBAM 1.0</span></span>


<span data-ttu-id="edf10-120">Esta sección contiene notas de la versión sobre problemas conocidos relacionados con la instalación y la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="edf10-120">This section contains release notes about the known issues with MBAM setup and installation.</span></span>

### <a href="" id="if-you-select-the--use-a-certificate-to-encrypt-the-network-communication--option-during-setup--existing-database-connections-and-dependent-applications-can-stop-functioning-"></a><span data-ttu-id="edf10-121">Si selecciona la opción "usar un certificado para cifrar la comunicación de red" durante la configuración, las conexiones de base de datos existentes y las aplicaciones dependientes pueden dejar de funcionar</span><span class="sxs-lookup"><span data-stu-id="edf10-121">If you select the “Use a certificate to encrypt the network communication” option during Setup, existing database connections and dependent applications can stop functioning</span></span>

<span data-ttu-id="edf10-122">Puede configurar MBAM para la **comunicación cifrada de red** después de instalar la base de datos de recuperación y de hardware o las características de la base de datos de estado de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="edf10-122">You can configure MBAM for **Encrypted network communication** after you install either the Recovery and Hardware Database or the Compliance Status Database features.</span></span> <span data-ttu-id="edf10-123">Si opta por configurar MBAM para la comunicación cifrada de la red, MBAM configuración configura la instancia del motor de base de datos de SQL Server para usar la capa de sockets seguros (SSL) para la comunicación entre la base de datos aplicable y el servidor de administración y las características de servidor de informes de cumplimiento y de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="edf10-123">If you choose to configure MBAM for Encrypted network communication, MBAM Setup configures the instance of the SQL Server Database Engine to use Secure Sockets Layer (SSL) for communication between the applicable database and both the Administration and Monitoring Server and the Compliance and Audit Report Server features.</span></span>

-   <span data-ttu-id="edf10-124">Si la instancia del motor de base de datos de SQL Server aún no está configurada para usar SSL, el programa de instalación de MBAM la configura para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="edf10-124">If the instance of the SQL Server Database Engine is not already configured to use SSL, MBAM Setup configures it to do so.</span></span> <span data-ttu-id="edf10-125">Esto puede impedir que las aplicaciones que intentan usar bases de datos que no sean de MBAM en la instancia del motor de base de datos de SQL Server se comuniquen con sus bases de datos.</span><span class="sxs-lookup"><span data-stu-id="edf10-125">This can prevent applications that try to use non-MBAM databases on the instance of the SQL Server Database Engine from communicating with their databases.</span></span>

-   <span data-ttu-id="edf10-126">Si la instancia del motor de base de datos de SQL Server ya está configurada para usar SSL, está configurada para usar el certificado seleccionado por el usuario durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="edf10-126">If the instance of the SQL Server Database Engine is already configured to use SSL, it is configured to use the certificate that the user selected during setup.</span></span> <span data-ttu-id="edf10-127">Si este certificado difiere del que ya estaba en uso, puede impedir que se ejecuten las aplicaciones que usan bases de datos de SQL Server en la instancia del motor de base de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="edf10-127">If this certificate differs from the one that was already in use, it can prevent applications that use SQL Server databases on the instance of the SQL Server Database Engine from running.</span></span>

<span data-ttu-id="edf10-128">**Solución alternativa:** Nada</span><span class="sxs-lookup"><span data-stu-id="edf10-128">**WORKAROUND:** None</span></span>

### <span data-ttu-id="edf10-129">Se produce un error en la instalación de MBAM durante la instalación cuando usa una cuenta de administrador local</span><span class="sxs-lookup"><span data-stu-id="edf10-129">MBAM Setup fails during installation when you use a local Administrator account</span></span>

<span data-ttu-id="edf10-130">MBAM se produce un error al usar una cuenta de administrador local.</span><span class="sxs-lookup"><span data-stu-id="edf10-130">MBAM Setup fails when you use a local Administrator account.</span></span> <span data-ttu-id="edf10-131">El archivo de registro contiene la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="edf10-131">The log file contains the following information:</span></span>

``` syntax
Locating group 'MBAM Report Users'
Adding <GUID>' to group 'MBAM Report Users'
Locating group 'MBAM Recovery and Hardware DB Access'
Adding 'S-1-5-20' to group 'MBAM Recovery and Hardware DB Access'
Exception: A new member could not be added to a local group because the member has the wrong account type.
 
  StackTrace:    at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SDSUtils.ApplyChangesToDirectory(Principal p, StoreCtx storeCtx, GroupMembershipUpdater updateGroupMembership, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.Update(Principal p)
   at Microsoft.Windows.Mdop.BitlockerManagement.Setup.Groups.CreateGroupsDeferred(Session session)
  InnerException:Exception: A new member could not be added to a local group because the member has the wrong account type.
 
    InnerException:StackTrace:    at System.DirectoryServices.AccountManagement.UnsafeNativeMethods.IADsGroup.Add(String bstrNewItem)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
CustomAction MbamCreateGroupsDeferred returned actual error code 1603 (note this may not be 100% accurate if translation happened inside sandbox)
Action ended 11:41:29: InstallExecute. Return value 3.
```

<span data-ttu-id="edf10-132">**Solución alternativa:** Use una cuenta de dominio con credenciales administrativas en el equipo servidor cuando instale MBAM.</span><span class="sxs-lookup"><span data-stu-id="edf10-132">**WORKAROUND:** Use a domain account with administrative credentials on the server computer when you install MBAM.</span></span>

### <span data-ttu-id="edf10-133">El programa de instalación de MBAM reconfigura la instancia del motor de base de datos de SQL Server para que no use SSL si selecciona "do not Cifre Network Communication"</span><span class="sxs-lookup"><span data-stu-id="edf10-133">MBAM Setup reconfigures the instance of the SQL Server Database Engine to not use SSL if you select “Do not encrypt network communication”</span></span>

<span data-ttu-id="edf10-134">Al instalar la base de datos de recuperación y de hardware o la base de datos de estado de cumplimiento, puede usar el programa de instalación al seleccionar **comunicación de red cifrada**.</span><span class="sxs-lookup"><span data-stu-id="edf10-134">When you install either the Recovery and Hardware Database or the Compliance Status Database, you can use Setup to configure MBAM by selecting **Encrypted network communication**.</span></span> <span data-ttu-id="edf10-135">Si decide no cifrar la comunicación de red, el programa de instalación de MBAM vuelve a configurar la instancia del motor de base de datos de SQL Server para que no use SSL.</span><span class="sxs-lookup"><span data-stu-id="edf10-135">If you decide not to encrypt the network communication, MBAM Setup reconfigures the instance of the SQL Server Database Engine so that it does not use SSL.</span></span>

-   <span data-ttu-id="edf10-136">Si la instancia del motor de base de datos de SQL Server ya está configurada para usar SSL, el programa de instalación de MBAM deshabilita SSL en la instancia del motor de base de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="edf10-136">If the instance of the SQL Server Database Engine is already configured to use SSL, MBAM Setup disables SSL on the instance of the SQL Server Database Engine.</span></span> <span data-ttu-id="edf10-137">Esto cambia la seguridad de la comunicación entre las aplicaciones que usan bases de datos que no están relacionadas con bases de datos de MBAM en la instancia del motor de base de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="edf10-137">This changes the communication security between the applications that use databases that are not related to MBAM databases on the instance of the SQL Server Database Engine.</span></span>

<span data-ttu-id="edf10-138">**Solución alternativa:** Nada</span><span class="sxs-lookup"><span data-stu-id="edf10-138">**WORKAROUND:** None</span></span>

### <span data-ttu-id="edf10-139">Falta el requisito previo de las secuencias de comandos de administración de Internet Information Services (IIS) y las características de servidor Web</span><span class="sxs-lookup"><span data-stu-id="edf10-139">Missing prerequisite for the Internet Information Services (IIS) Management Scripts and Tools web server feature</span></span>

<span data-ttu-id="edf10-140">El programa de instalación de MBAM depende de la característica de servidor Web de scripts y herramientas de administración de IIS, pero no es un requisito previo obligatorio.</span><span class="sxs-lookup"><span data-stu-id="edf10-140">MBAM Setup is dependent on the IIS Management Scripts and Tools web server feature, but it is not an enforced prerequisite.</span></span> <span data-ttu-id="edf10-141">La configuración del servidor le permite instalar MBAM cuando falta esta característica.</span><span class="sxs-lookup"><span data-stu-id="edf10-141">Server setup lets you install MBAM when this feature is missing.</span></span> <span data-ttu-id="edf10-142">Sin embargo, esto hará que el servicio de copia de seguridad MBAM VSS Writer se inicie y se detenga, ya que no puede ubicar el instrumental de administración de Windows (WMI) ni el proveedor de servicios de Internet Information Server (IIS).</span><span class="sxs-lookup"><span data-stu-id="edf10-142">However, this will cause the backup service MBAM VSS Writer to start and then stop, because it cannot locate the Windows Management Instrumentation (WMI) and the Internet Information Services (IIS) provider.</span></span> <span data-ttu-id="edf10-143">No hay ningún mensaje de error para esta condición, excepto el que aparece en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="edf10-143">There is no error message for this condition, except that which occurs in the event log.</span></span> <span data-ttu-id="edf10-144">La instalación de MBAM sin scripts de administración y herramientas de administración de IIS hace que las operaciones de copia de seguridad no se ejecuten para MBAM.</span><span class="sxs-lookup"><span data-stu-id="edf10-144">Installation of MBAM without IIS Management Scripts and Tools causes the backup operations not to run for MBAM.</span></span>

<span data-ttu-id="edf10-145">**Solución alternativa:** Asegúrese de que la característica de servidor Web herramientas y scripts de administración de IIS esté instalada antes de iniciar la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="edf10-145">**WORKAROUND:** Ensure that the IIS Management Scripts and Tools web server feature is installed before you start the MBAM Setup.</span></span>

### <a href="" id="mbam-setup-stops-responding-during-the--installing-selected-features--phase-when-setup-is-configured-to-use-a-certificate"></a><span data-ttu-id="edf10-146">El programa de instalación de MBAM deja de responder durante la fase "instalar las características seleccionadas" cuando la configuración está configurada para usar un certificado</span><span class="sxs-lookup"><span data-stu-id="edf10-146">MBAM Setup stops responding during the “Installing selected features” phase when setup is configured to use a certificate</span></span>

<span data-ttu-id="edf10-147">El programa de instalación de MBAM deja de responder durante la fase de instalación de **las características seleccionadas** de la instalación.</span><span class="sxs-lookup"><span data-stu-id="edf10-147">MBAM Setup stops responding during the **Installing selected features** phase of setup.</span></span> <span data-ttu-id="edf10-148">Esto se produce durante la instalación de la base de datos de recuperación y hardware o de la base de datos de estado de cumplimiento, después de seleccionar la opción **usar un certificado para cifrar la comunicación de red** .</span><span class="sxs-lookup"><span data-stu-id="edf10-148">This occurs during the installation of the Recovery and Hardware Database or the Compliance Status Database, after you select the **Use a certificate to encrypt the network communication** option.</span></span> <span data-ttu-id="edf10-149">Además, el programa de instalación de MBAM deja de responder si la instancia del motor de base de datos de SQL Server no puede acceder al certificado que se especificó durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="edf10-149">Furthermore, the MBAM Setup stops responding if the instance of the SQL Server Database Engine cannot access the certificate that was specified during setup.</span></span>

<span data-ttu-id="edf10-150">**Solución alternativa:** Actualice los permisos del certificado para que el servicio de Windows para la instancia aplicable del motor de base de datos de SQL Server pueda obtener acceso al certificado.</span><span class="sxs-lookup"><span data-stu-id="edf10-150">**WORKAROUND:** Update the permissions on the certificate, so that the Windows service for the applicable instance of the SQL Server Database Engine can access the certificate.</span></span> <span data-ttu-id="edf10-151">También puede cambiar la cuenta en la que se ejecuta la instancia del motor de base de datos de SQL Server para que el motor de base de datos use el certificado.</span><span class="sxs-lookup"><span data-stu-id="edf10-151">You can also change the account under which the instance of the SQL Server Database Engine runs, for the database engine to use the certificate.</span></span> <span data-ttu-id="edf10-152">Para determinar los permisos para el certificado, escriba el siguiente comando en el símbolo del sistema: **certutil-v-Store My**</span><span class="sxs-lookup"><span data-stu-id="edf10-152">To determine the permissions for the certificate, type the following command at the command prompt: **certutil -v -store MY**</span></span>

### <span data-ttu-id="edf10-153">El programa de instalación de MBAM se detiene durante la instalación de SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="edf10-153">MBAM Setup pauses when you install SQL Server Reporting Services</span></span>

<span data-ttu-id="edf10-154">Durante la instalación de MBAM, al seleccionar una instancia de SQL Server Reporting Services (SSRS) y la instancia de SSRS no está disponible, la configuración de MBAM puede detenerse durante un minuto mientras intenta comunicarse con la instancia de SSRS.</span><span class="sxs-lookup"><span data-stu-id="edf10-154">During MBAM installation, when you select an instance of SQL Server Reporting Services (SSRS) and SSRS instance is not available or it is configured incorrectly, the MBAM Setup might pause for up to one minute while it attempts to communicate with the SSRS instance.</span></span>

<span data-ttu-id="edf10-155">**Solución alternativa:** Espere al menos un minuto para que la configuración de MBAM se reanude mientras el programa de instalación intente ponerse en contacto con la instancia de SSRS.</span><span class="sxs-lookup"><span data-stu-id="edf10-155">**WORKAROUND:** Wait for at least one minute for MBAM Setup to resume while the Setup program attempts to contact the instance of SSRS.</span></span>

### <a href="" id="administration-and-monitoring-server-does-not-run-after-setup-"></a><span data-ttu-id="edf10-156">El servidor de administración y supervisión no se ejecuta después de la instalación</span><span class="sxs-lookup"><span data-stu-id="edf10-156">Administration and Monitoring Server does not run after setup</span></span>

<span data-ttu-id="edf10-157">Después de que el programa de instalación de MBAM instale correctamente la característica de servidor de administración y supervisión, MBAM mostrará mensajes de error cuando intente acceder al sitio web del administrador de MBAM.</span><span class="sxs-lookup"><span data-stu-id="edf10-157">After MBAM Setup successfully installs the Administration and Monitoring Server feature, MBAM displays error messages when you try to access the MBAM administrator website.</span></span> <span data-ttu-id="edf10-158">Este problema se produce por uno de los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="edf10-158">This issue occurs for one of the following reasons:</span></span>

-   <span data-ttu-id="edf10-159">Una o más de las condiciones previas del servidor de administración y supervisión se quitaron después de la instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="edf10-159">One or more prerequisites on the Administration and Monitoring Server were removed after the MBAM installation.</span></span>

-   <span data-ttu-id="edf10-160">Se instalaron uno o varios requisitos previos en el servidor y posteriormente se quitaron antes de ejecutar el programa de instalación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="edf10-160">One or more prerequisites were installed on the server and later they were removed before running the MBAM Setup.</span></span>

<span data-ttu-id="edf10-161">**Solución alternativa:** Revise la documentación de MBAM y confirme que todos los requisitos previos de MBAM estén instalados.</span><span class="sxs-lookup"><span data-stu-id="edf10-161">**WORKAROUND:** Review the MBAM documentation and confirm that all MBAM prerequisites are installed.</span></span>

### <span data-ttu-id="edf10-162">Al hacer clic en los vínculos de documentación durante la instalación se produce un error de aplicación después de finalizar la instalación</span><span class="sxs-lookup"><span data-stu-id="edf10-162">Clicking documentation links during Setup results in an application error after Setup is finished</span></span>

<span data-ttu-id="edf10-163">Al hacer clic en un vínculo de documentación durante la instalación y cerrar el programa de instalación haciendo clic en **Cancelar** o **Finalizar** después de que el programa de instalación haya finalizado correctamente, aparece un mensaje de error de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="edf10-163">When you click a documentation link during setup and then close the Setup program by clicking **Cancel** or **Finish** after Setup has successfully finished, an application error message appears..</span></span> <span data-ttu-id="edf10-164">El problema se debe a un error de infracción de acceso en el programador de tareas de Windows.</span><span class="sxs-lookup"><span data-stu-id="edf10-164">The problem is caused by an access violation error in the Windows Task Scheduler.</span></span>

<span data-ttu-id="edf10-165">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="edf10-165">**WORKAROUND:** None.</span></span> <span data-ttu-id="edf10-166">Puede ignorar este error.</span><span class="sxs-lookup"><span data-stu-id="edf10-166">You can ignore this error.</span></span>

### <span data-ttu-id="edf10-167">Error de MBAM el programa de instalación no quita nuevas bases de datos</span><span class="sxs-lookup"><span data-stu-id="edf10-167">Failed MBAM Setup does not remove new databases</span></span>

<span data-ttu-id="edf10-168">Si se produce un error en el programa de instalación de MBAM, es posible que el programa de instalación no quite las bases de datos recién creadas.</span><span class="sxs-lookup"><span data-stu-id="edf10-168">If the MBAM Setup fails, Setup might not remove the newly created databases.</span></span> <span data-ttu-id="edf10-169">Esto puede provocar errores durante las instalaciones posteriores.</span><span class="sxs-lookup"><span data-stu-id="edf10-169">This can cause failures during subsequent installations.</span></span>

<span data-ttu-id="edf10-170">**Solución alternativa:** Elija un nombre diferente para la instancia de la base de datos durante la instalación posterior.</span><span class="sxs-lookup"><span data-stu-id="edf10-170">**WORKAROUND:** Choose a different name for the database instance during the subsequent installation.</span></span>

### <span data-ttu-id="edf10-171">El programa de instalación de MBAM no reconoce certificados de clúster válidos de equilibrio de carga de red</span><span class="sxs-lookup"><span data-stu-id="edf10-171">MBAM Setup does not recognize valid network load-balancing cluster certificates</span></span>

<span data-ttu-id="edf10-172">Durante la instalación del servidor de administración y supervisión de MBAM con la opción cifrado de red seleccionada, el certificado de clúster no se reconoce como un certificado válido.</span><span class="sxs-lookup"><span data-stu-id="edf10-172">During the MBAM Administration and Monitoring Server installation, with the network encryption option selected, the cluster certificate is not recognized as a valid certificate.</span></span> <span data-ttu-id="edf10-173">Se reconoce como válido cuando el certificado para la comunicación con la base de datos está instalado, pero es rechazado por el clúster de equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="edf10-173">It is recognized as valid when the certificate for communication with the database is installed, but it is rejected for communication by the load-balancing cluster.</span></span>

<span data-ttu-id="edf10-174">**Solución alternativa:** Confirme que la lista de revocación de certificados (CRL) asociada al certificado sea accesible o use un certificado que no requiera validación con la CRL.</span><span class="sxs-lookup"><span data-stu-id="edf10-174">**WORKAROUND:** Confirm that the certificate revocation list (CRL) associated with the certificate is accessible, or use a certificate that does not require validation by using the CRL.</span></span>

## <span data-ttu-id="edf10-175">Información de copyright de notas de versión</span><span class="sxs-lookup"><span data-stu-id="edf10-175">Release Notes Copyright Information</span></span>


<span data-ttu-id="edf10-176">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune y WindowsPowerShell son marcas comerciales del grupo de empresas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="edf10-176">Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune, and WindowsPowerShell are trademarks of the Microsoft group of companies.</span></span> <span data-ttu-id="edf10-177">El resto de marcas comerciales pertenecen a sus respectivos dueños.</span><span class="sxs-lookup"><span data-stu-id="edf10-177">All other trademarks are property of their respective owners.</span></span>



## <span data-ttu-id="edf10-178">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="edf10-178">Related topics</span></span>


[<span data-ttu-id="edf10-179">Acerca de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="edf10-179">About MBAM 1.0</span></span>](about-mbam-10.md)

 

 





