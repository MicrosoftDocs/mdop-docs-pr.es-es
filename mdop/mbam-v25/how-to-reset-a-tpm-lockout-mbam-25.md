---
title: Cómo restablecer un bloqueo de TPM
description: Cómo restablecer un bloqueo de TPM
author: dansimp
ms.assetid: dd20a728-c52e-48e6-9f6c-1311c71dee74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5aea277e80c54fb01d1a6c00b62f0c617d1ad12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823321"
---
# <span data-ttu-id="17b3e-103">Cómo restablecer un bloqueo de TPM</span><span class="sxs-lookup"><span data-stu-id="17b3e-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="17b3e-104">En este tema se explica cómo usar el sitio web de administración y supervisión (también conocido como soporte técnico) para restablecer un bloqueo de TPM.</span><span class="sxs-lookup"><span data-stu-id="17b3e-104">This topic explains how to use the Administration and Monitoring Website (also referred to as the Help Desk) to reset a TPM lockout.</span></span> <span data-ttu-id="17b3e-105">Los bloqueos de TPM pueden producirse si un usuario final escribe el PIN incorrecto demasiadas veces.</span><span class="sxs-lookup"><span data-stu-id="17b3e-105">TPM lockouts can occur if an end user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="17b3e-106">El número de veces que un usuario puede escribir un PIN incorrecto antes de que los bloqueos de TPM varíen de un fabricante a otro.</span><span class="sxs-lookup"><span data-stu-id="17b3e-106">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span>

<span data-ttu-id="17b3e-107">Desde el área **administrar TPM** del sitio web administración y supervisión, puede acceder al sistema centralizado de datos de recuperación de claves, que proporciona un archivo de contraseña de propietario de TPM cuando se proporciona un identificador de equipo y un identificador de usuario asociado.</span><span class="sxs-lookup"><span data-stu-id="17b3e-107">From the **Manage TPM** area of the Administration and Monitoring Website, you can access the centralized Key Recovery data system, which provides a TPM owner password file when you supply a computer ID and associated user identifier.</span></span>

<span data-ttu-id="17b3e-108">Para acceder al área administrar TPM del sitio web de administración y supervisión, debe tener asignado el rol de usuarios del Departamento de soporte técnico de MBAM o el rol de usuarios avanzados de soporte técnico de MBAM.</span><span class="sxs-lookup"><span data-stu-id="17b3e-108">To access the Manage TPM area of the Administration and Monitoring Website, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="17b3e-109">Estos roles son grupos que los administradores crean en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="17b3e-109">These roles are groups that administrators create in Active Directory.</span></span> <span data-ttu-id="17b3e-110">Puede usar cualquier nombre para estos grupos.</span><span class="sxs-lookup"><span data-stu-id="17b3e-110">You can use any name for these groups.</span></span> <span data-ttu-id="17b3e-111">Para obtener más información, consulte [planificación de grupos y cuentas de MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span><span class="sxs-lookup"><span data-stu-id="17b3e-111">For more information, see [Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).</span></span>

<span data-ttu-id="17b3e-112">Para obtener información sobre la propiedad de MBAM y TPM, consulte [consideraciones de seguridad de MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).</span><span class="sxs-lookup"><span data-stu-id="17b3e-112">For information about MBAM and TPM ownership, see [MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm).</span></span>

**<span data-ttu-id="17b3e-113">Para restablecer un bloqueo de TPM</span><span class="sxs-lookup"><span data-stu-id="17b3e-113">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="17b3e-114">Abra un explorador Web y vaya al **sitio web de administración y supervisión**.</span><span class="sxs-lookup"><span data-stu-id="17b3e-114">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="17b3e-115">En el panel de la izquierda, haga clic en **administrar TPM** para abrir la página **administrar TPM** .</span><span class="sxs-lookup"><span data-stu-id="17b3e-115">In the left pane, click **Manage TPM** to open the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="17b3e-116">Escriba el nombre de dominio completo del equipo y el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="17b3e-116">Enter the fully qualified domain name for the computer and the computer name.</span></span>

4.  <span data-ttu-id="17b3e-117">Escriba el nombre de usuario y el dominio de inicio de sesión de Windows del usuario final para recuperar el archivo de contraseña de propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="17b3e-117">Enter the end user’s Windows log-on domain and user name to retrieve the TPM owner password file.</span></span>

    <span data-ttu-id="17b3e-118">**Nota:**  Si se encuentra en el grupo de usuarios del servicio de asistencia MBAM avanzado, los campos dominio del usuario e identificador de usuario no son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="17b3e-118">**Note** If you are in the MBAM Advanced Helpdesk Users group, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="17b3e-119">En la lista de **archivos de contraseña de propietario de TPM** , seleccione un motivo para la solicitud y haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="17b3e-119">From the **Reason for requesting TPM owner password file** list, select a reason for the request, and click **Submit**.</span></span>

    <span data-ttu-id="17b3e-120">MBAM devuelve una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="17b3e-120">MBAM returns one of the following:</span></span>

    -   <span data-ttu-id="17b3e-121">Mensaje de error si no se encuentra ningún archivo de contraseña de propietario de TPM coincidente</span><span class="sxs-lookup"><span data-stu-id="17b3e-121">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="17b3e-122">El archivo de contraseña de propietario de TPM para el equipo enviado</span><span class="sxs-lookup"><span data-stu-id="17b3e-122">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="17b3e-123">Después de que se recupera la contraseña de propietario de TPM, se muestra la contraseña de propietario.</span><span class="sxs-lookup"><span data-stu-id="17b3e-123">After the TPM owner password is retrieved, the owner password is displayed.</span></span>

6.  <span data-ttu-id="17b3e-124">Para guardar la contraseña en un archivo. TPM, haga clic en el botón **Guardar** .</span><span class="sxs-lookup"><span data-stu-id="17b3e-124">To save the password to a .tpm file, click the **Save** button.</span></span>

7.  <span data-ttu-id="17b3e-125">En el área **administrar TPM** del **sitio web de administración y supervisión**, seleccione la opción **restablecer el bloqueo de TPM** y proporcione el archivo de contraseña de propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="17b3e-125">In the **Manage TPM** area of the **Administration and Monitoring Website**, select the **Reset TPM lockout** option and provide the TPM owner password file.</span></span>

    <span data-ttu-id="17b3e-126">Se restablece el bloqueo de TPM y se restaura el acceso del usuario final.</span><span class="sxs-lookup"><span data-stu-id="17b3e-126">The TPM lockout is reset and the end user’s access is restored.</span></span>

    <span data-ttu-id="17b3e-127">**Importante**  No asigne el valor de hash de TPM o el archivo de contraseña de propietario de TPM a los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="17b3e-127">**Important** Do not give the TPM hash value or TPM owner password file to end users.</span></span> <span data-ttu-id="17b3e-128">Debido a que la información de TPM no cambia, ofrecer el archivo a los usuarios finales supone un riesgo de seguridad.</span><span class="sxs-lookup"><span data-stu-id="17b3e-128">Because the TPM information does not change, giving the file to end users creates a security risk.</span></span>

     



## <span data-ttu-id="17b3e-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17b3e-129">Related topics</span></span>


[<span data-ttu-id="17b3e-130">Realización de la administración de BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="17b3e-130">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 

## <span data-ttu-id="17b3e-131">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="17b3e-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="17b3e-132">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="17b3e-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="17b3e-133">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="17b3e-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





