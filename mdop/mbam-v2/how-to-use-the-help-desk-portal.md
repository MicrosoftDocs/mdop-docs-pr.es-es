---
title: Cómo usar el portal del Departamento de soporte técnico
description: Cómo usar el portal del Departamento de soporte técnico
author: dansimp
ms.assetid: c27f7737-10c8-4164-9de8-57987292c89c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8813fbe9a7b6980b656ecc673ac4ed618c4cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826330"
---
# <span data-ttu-id="87cfd-103">Cómo usar el portal del Departamento de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="87cfd-103">How to Use the Help Desk Portal</span></span>


<span data-ttu-id="87cfd-104">El sitio web de administración y supervisión de MBAM, también conocido como portal de servicio de asistencia, es una interfaz administrativa para el cifrado de unidad BitLocker que se instala como parte de la infraestructura de servidor de administración y supervisión de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="87cfd-104">The MBAM Administration and Monitoring website, also referred to as the Help Desk Portal, is an administrative interface to BitLocker drive encryption that is installed as part of the Microsoft BitLocker Administration and Monitoring (MBAM) server infrastructure.</span></span> <span data-ttu-id="87cfd-105">En las siguientes secciones se describe cómo puede usar este sitio web para revisar informes, recuperar unidades de los usuarios finales y administrar los TPMs de los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="87cfd-105">The following sections describe how you can use this website to review reports, recover end users’ drives, and manage end users’ TPMs.</span></span>

## <a href="" id="bkmk-reports"></a><span data-ttu-id="87cfd-106">Informes</span><span class="sxs-lookup"><span data-stu-id="87cfd-106">Reports</span></span>


<span data-ttu-id="87cfd-107">MBAM recopila información de equipos de Active Directory y clientes, lo que le permite ejecutar diferentes informes para supervisar el uso de BitLocker y el cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="87cfd-107">MBAM collects information from Active Directory and client computers, which enables you to run different reports to monitor BitLocker usage and compliance.</span></span> <span data-ttu-id="87cfd-108">Con la sección **informes** del sitio web de administración y supervisión, puede generar informes sobre el cumplimiento de la norma empresarial, los equipos individuales y la actividad de recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="87cfd-108">Using the **Reports** section of the Administration and Monitoring website, you can generate reports on enterprise compliance, individual computers, and key recovery activity.</span></span> <span data-ttu-id="87cfd-109">Para obtener una descripción de cada informe, consulte [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="87cfd-109">For a description of each report, see [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).</span></span>

**<span data-ttu-id="87cfd-110">Para obtener acceso a los informes</span><span class="sxs-lookup"><span data-stu-id="87cfd-110">To access reports</span></span>**

1.  <span data-ttu-id="87cfd-111">Abra un explorador Web y vaya al sitio web de administración y supervisión de MBAM.</span><span class="sxs-lookup"><span data-stu-id="87cfd-111">Open a web browser and navigate to the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="87cfd-112">Seleccione **informes** en el panel de la izquierda.</span><span class="sxs-lookup"><span data-stu-id="87cfd-112">Select **Reports** in the left pane.</span></span>

3.  <span data-ttu-id="87cfd-113">En la barra de menús superior, seleccione el tipo de informe que desea generar.</span><span class="sxs-lookup"><span data-stu-id="87cfd-113">From the top menu bar, select the report type you want to generate.</span></span> <span data-ttu-id="87cfd-114">Para guardar los informes, haga clic en el botón **exportar** en la barra de menús informes.</span><span class="sxs-lookup"><span data-stu-id="87cfd-114">To save reports, click the **Export** button on the Reports menu bar.</span></span>

<span data-ttu-id="87cfd-115">Para obtener más información sobre cómo ejecutar informes de MBAM, consulte [Cómo generar informes de MBAM](how-to-generate-mbam-reports-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="87cfd-115">For additional information about how to run MBAM reports, see [How to Generate MBAM Reports](how-to-generate-mbam-reports-mbam-2.md).</span></span>

## <a href="" id="bkmk-drirec"></a><span data-ttu-id="87cfd-116">Recuperación de unidades</span><span class="sxs-lookup"><span data-stu-id="87cfd-116">Drive Recovery</span></span>


<span data-ttu-id="87cfd-117">La característica **recuperación de unidades** del sitio web de supervisión y administración permite a los usuarios con roles de administrador específicos (por ejemplo, usuarios del servicio de asistencia) obtener acceso a datos de claves de recuperación que ha recopilado el cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="87cfd-117">The **Drive Recovery** feature of the Administration and Monitoring website allows users with specific administrator roles (for example, Help Desk Users) to access recovery key data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="87cfd-118">Estos datos se pueden usar para acceder a una unidad protegida con BitLocker cuando BitLocker pasa al modo de recuperación.</span><span class="sxs-lookup"><span data-stu-id="87cfd-118">This data can be used to access a BitLocker-protected drive when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="87cfd-119">Para obtener instrucciones sobre cómo recuperar una unidad que esté en modo de recuperación, consulte [Cómo recuperar una unidad en modo de recuperación](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="87cfd-119">For instructions on how to recover a drive that is in recovery mode, see [How to Recover a Drive in Recovery Mode](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).</span></span>

<span data-ttu-id="87cfd-120">También puede recuperar unidades que se hayan movido o que estén dañadas:</span><span class="sxs-lookup"><span data-stu-id="87cfd-120">You can also recover drives that have been moved or that are corrupted:</span></span>

-   [<span data-ttu-id="87cfd-121">Cómo recuperar una unidad que se ha movido</span><span class="sxs-lookup"><span data-stu-id="87cfd-121">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="87cfd-122">Cómo recuperar una unidad dañada</span><span class="sxs-lookup"><span data-stu-id="87cfd-122">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

<span data-ttu-id="87cfd-123">Para obtener más información sobre cómo recuperar una unidad protegida con BitLocker, consulte [realizar la administración de BitLocker con MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="87cfd-123">For additional information about how to recover a BitLocker-protected drive, see [Performing BitLocker Management with MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).</span></span>

## <a href="" id="bkmk-manatpm"></a><span data-ttu-id="87cfd-124">Administrar TPM</span><span class="sxs-lookup"><span data-stu-id="87cfd-124">Manage TPM</span></span>


<span data-ttu-id="87cfd-125">La característica administrar TPM del sitio web administración y supervisión proporciona a los usuarios que tienen determinados roles de administrador (por ejemplo, "usuarios del Departamento de soporte técnico") el acceso a los datos de TPM recopilados por el cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="87cfd-125">The Manage TPM feature of the Administration and Monitoring website gives users with certain administrator roles (for example, “MBAM Helpdesk Users”) access to TPM data that has been collected by the MBAM Client.</span></span> <span data-ttu-id="87cfd-126">En un bloqueo de TPM, un administrador puede usar el sitio web de administración y supervisión para recuperar el archivo de contraseñas necesario para desbloquear el TPM.</span><span class="sxs-lookup"><span data-stu-id="87cfd-126">In a TPM lockout, an administrator can use the Administration and Monitoring website to retrieve the necessary password file to unlock the TPM.</span></span> <span data-ttu-id="87cfd-127">Para obtener instrucciones sobre cómo restablecer un TPM después de un bloqueo de TPM, consulte [cómo restablecer un bloqueo de TPM](how-to-reset-a-tpm-lockout-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="87cfd-127">For instructions on how to reset a TPM after a TPM lockout, see [How to Reset a TPM Lockout](how-to-reset-a-tpm-lockout-mbam-2.md).</span></span>

## <a href="" id="bkmk-helpdesk"></a> <span data-ttu-id="87cfd-128">Tareas del servicio de asistencia de MBAM</span><span class="sxs-lookup"><span data-stu-id="87cfd-128">MBAM Help Desk Tasks</span></span>


<span data-ttu-id="87cfd-129">Puede usar el sitio web de administración y supervisión para muchas tareas administrativas, como la administración de hardware protegido por BitLocker, la recuperación de unidades y la ejecución de informes.</span><span class="sxs-lookup"><span data-stu-id="87cfd-129">You can use the Administration and Monitoring website for many administrative tasks, such as managing BitLocker-protected hardware, recovering drives, and running reports.</span></span> <span data-ttu-id="87cfd-130">De forma predeterminada, la dirección URL del sitio web de supervisión y administración es http:// &lt; *MBAMAdministrationServername* &gt; , aunque puede personalizarla durante el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="87cfd-130">By default, the URL for the Administration and Monitoring website is http://&lt;*MBAMAdministrationServername*&gt;, although you can customize it during the installation process.</span></span>

<span data-ttu-id="87cfd-131">**Nota:**  Para acceder a las diversas características que ofrece el sitio web de supervisión y supervisión, debe tener las funciones apropiadas asociadas a su cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="87cfd-131">**Note** To access the various features offered by the Administration and Monitoring website, you must have the appropriate roles associated with your user account.</span></span> <span data-ttu-id="87cfd-132">Para obtener más información sobre los roles de usuario, consulte [Cómo administrar los roles de administrador de MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="87cfd-132">For more information about understanding user roles, see [How to Manage MBAM Administrator Roles](how-to-manage-mbam-administrator-roles-mbam-2.md).</span></span>

 

<span data-ttu-id="87cfd-133">Use los siguientes vínculos para buscar información sobre las tareas que puede realizar mediante el sitio web de administración y supervisión:</span><span class="sxs-lookup"><span data-stu-id="87cfd-133">Use the following links to find information about the tasks that you can perform by using the Administration and Monitoring website:</span></span>

-   [<span data-ttu-id="87cfd-134">Cómo restablecer un bloqueo de TPM</span><span class="sxs-lookup"><span data-stu-id="87cfd-134">How to Reset a TPM Lockout</span></span>](how-to-reset-a-tpm-lockout-mbam-2.md)

-   [<span data-ttu-id="87cfd-135">Cómo recuperar una unidad en modo de recuperación</span><span class="sxs-lookup"><span data-stu-id="87cfd-135">How to Recover a Drive in Recovery Mode</span></span>](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

-   [<span data-ttu-id="87cfd-136">Cómo recuperar una unidad que se ha movido</span><span class="sxs-lookup"><span data-stu-id="87cfd-136">How to Recover a Moved Drive</span></span>](how-to-recover-a-moved-drive-mbam-2.md)

-   [<span data-ttu-id="87cfd-137">Cómo recuperar una unidad dañada</span><span class="sxs-lookup"><span data-stu-id="87cfd-137">How to Recover a Corrupted Drive</span></span>](how-to-recover-a-corrupted-drive-mbam-2.md)

-   [<span data-ttu-id="87cfd-138">Cómo determinar el estado de cifrado de BitLocker de equipos perdidos</span><span class="sxs-lookup"><span data-stu-id="87cfd-138">How to Determine BitLocker Encryption State of Lost Computers</span></span>](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

 

 





