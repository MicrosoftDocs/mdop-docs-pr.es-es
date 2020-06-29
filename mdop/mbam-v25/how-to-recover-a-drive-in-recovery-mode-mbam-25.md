---
title: Cómo recuperar una unidad en modo de recuperación
description: Cómo recuperar una unidad en modo de recuperación
author: dansimp
ms.assetid: e126eaf8-9ae7-40fe-a28e-dbd78d26859e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d15f33f461e60fceeed3acbce3a0c82b02b56f98
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823370"
---
# <span data-ttu-id="4e4ce-103">Cómo recuperar una unidad en modo de recuperación</span><span class="sxs-lookup"><span data-stu-id="4e4ce-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="4e4ce-104">En este tema se explica cómo usar el sitio web de administración y supervisión (también conocido como servicio de asistencia) para obtener una contraseña de recuperación que conceder a los usuarios finales si su unidad protegida con BitLocker pasa al modo de recuperación.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to get a recovery password to give to end users if their BitLocker-protected drive goes into recovery mode.</span></span> <span data-ttu-id="4e4ce-105">Las unidades entran en el modo de recuperación si los usuarios pierden su PIN o su contraseña, o si el chip de la plataforma de módulo de confianza (TPM) detecta cambios en el BIOS o los archivos de inicio de un equipo.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-105">Drives go into recovery mode if users lose or forget their PIN or password or if the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="4e4ce-106">Para obtener una contraseña de recuperación, use el área de **recuperación de Drive** del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-106">To get a recovery password, use the **Drive Recovery** area of the Administration and Monitoring Website.</span></span> <span data-ttu-id="4e4ce-107">Para acceder a esta área del sitio web, debe tener asignados los roles de usuarios de soporte técnico de MBAM o el rol de usuarios avanzados de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-107">You must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role to access this area of the website.</span></span>

**<span data-ttu-id="4e4ce-108">Nota</span><span class="sxs-lookup"><span data-stu-id="4e4ce-108">Note</span></span>**  
<span data-ttu-id="4e4ce-109">Es posible que haya dado a estos roles nombres diferentes al crearlos.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-109">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="4e4ce-110">Para obtener más información, consulte [planificación de grupos y cuentas de MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="4e4ce-110">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>



**<span data-ttu-id="4e4ce-111">Importante</span><span class="sxs-lookup"><span data-stu-id="4e4ce-111">Important</span></span>**  
<span data-ttu-id="4e4ce-112">Las contraseñas de recuperación vencen después de un solo uso.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-112">Recovery passwords expire after a single use.</span></span> <span data-ttu-id="4e4ce-113">En las unidades de sistema operativo y las unidades de datos fijas, la regla de uso único se aplica automáticamente.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-113">On operating system drives and fixed data drives, the single-use rule is applied automatically.</span></span> <span data-ttu-id="4e4ce-114">En las unidades extraíbles, se aplica cuando se quita la unidad y se vuelve a insertar y a desbloquear en un equipo que tiene activada la configuración de directiva de grupo para administrar unidades extraíbles.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-114">On removable drives, it is applied when the drive is removed and then reinserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="4e4ce-115">Para recuperar una unidad en modo de recuperación</span><span class="sxs-lookup"><span data-stu-id="4e4ce-115">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="4e4ce-116">Abra un explorador Web y vaya al **sitio web de administración y supervisión**.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="4e4ce-117">En el panel izquierdo, seleccione **recuperación de unidades** para abrir la página **recuperar el acceso a una unidad cifrada** .</span><span class="sxs-lookup"><span data-stu-id="4e4ce-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="4e4ce-118">Escriba el nombre de usuario y el dominio de inicio de sesión de Windows del usuario final para ver la información de recuperación.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-118">Enter the end user’s Windows log-on domain and user name to view recovery information.</span></span>

    **<span data-ttu-id="4e4ce-119">Nota</span><span class="sxs-lookup"><span data-stu-id="4e4ce-119">Note</span></span>**  
    <span data-ttu-id="4e4ce-120">Si se encuentra en el grupo de usuarios del servicio de asistencia MBAM avanzado, los campos dominio del usuario e identificador de usuario no son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-120">If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>



4.  <span data-ttu-id="4e4ce-121">Escriba los primeros ocho dígitos de la identificación de la clave de recuperación para ver una lista de las posibles claves de recuperación coincidentes, o bien escriba la identificación de la clave de recuperación completa para obtener la clave de recuperación exacta.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-121">Enter the first eight digits of the recovery key ID to see a list of possible matching recovery keys, or enter the entire recovery key ID to get the exact recovery key.</span></span>

5.  <span data-ttu-id="4e4ce-122">En la lista **motivo de desbloqueo** de la unidad, seleccione una de las opciones predefinidas y, a continuación, haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-122">From the **Reason for Drive Unlock** list, select one of the predefined options, and then click **Submit**.</span></span>

    <span data-ttu-id="4e4ce-123">MBAM devuelve lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4e4ce-123">MBAM returns the following:</span></span>

    -   <span data-ttu-id="4e4ce-124">Mensaje de error si no se encuentra ninguna contraseña de recuperación coincidente</span><span class="sxs-lookup"><span data-stu-id="4e4ce-124">An error message if no matching recovery password is found</span></span>

    -   <span data-ttu-id="4e4ce-125">Varias coincidencias posibles si el usuario tiene varias contraseñas de recuperación coincidentes</span><span class="sxs-lookup"><span data-stu-id="4e4ce-125">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    -   <span data-ttu-id="4e4ce-126">La contraseña de recuperación y el paquete de recuperación para el usuario enviado</span><span class="sxs-lookup"><span data-stu-id="4e4ce-126">The recovery password and recovery package for the submitted user</span></span>

        **<span data-ttu-id="4e4ce-127">Nota</span><span class="sxs-lookup"><span data-stu-id="4e4ce-127">Note</span></span>**  
        <span data-ttu-id="4e4ce-128">Si está recuperando una unidad dañada, la opción paquete de recuperación proporciona a BitLocker información crítica que necesita para recuperar la unidad.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-128">If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.</span></span>



~~~
After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

6. <span data-ttu-id="4e4ce-129">Para copiar la contraseña, haga clic en **copiar clave**y, a continuación, pegue la contraseña de recuperación en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-129">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="4e4ce-130">También puede hacer clic en **Guardar** para guardar la contraseña de recuperación en un archivo.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-130">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="4e4ce-131">Cuando el usuario escribe la contraseña de recuperación en el sistema o usa el paquete de recuperación, la unidad se desbloquea.</span><span class="sxs-lookup"><span data-stu-id="4e4ce-131">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>



## <span data-ttu-id="4e4ce-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4e4ce-132">Related topics</span></span>


[<span data-ttu-id="4e4ce-133">Realización de la administración de BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="4e4ce-133">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)



## <span data-ttu-id="4e4ce-134">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="4e4ce-134">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="4e4ce-135">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="4e4ce-135">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="4e4ce-136">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="4e4ce-136">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





