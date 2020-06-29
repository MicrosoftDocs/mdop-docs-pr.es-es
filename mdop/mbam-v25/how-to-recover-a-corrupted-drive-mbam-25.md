---
title: Cómo recuperar una unidad dañada
description: Cómo recuperar una unidad dañada
author: dansimp
ms.assetid: fa5b846b-dda6-4ae4-bf6c-39e4f1d8aa00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fd9fd8a65d57cbfe965197fa26b57319ee046784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822551"
---
# <span data-ttu-id="e5c6b-103">Cómo recuperar una unidad dañada</span><span class="sxs-lookup"><span data-stu-id="e5c6b-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="e5c6b-104">Puede usar este procedimiento con el sitio web de administración y supervisión (también se conoce como soporte técnico) para recuperar una unidad dañada que está protegida por BitLocker.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-104">You can use this procedure with the Administration and Monitoring Website (also referred to as the Help Desk) Website to recover a corrupted drive that is protected by BitLocker.</span></span> <span data-ttu-id="e5c6b-105">Para ello, completará las tareas indicadas en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-105">To do this, you will complete the tasks outlined in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e5c6b-106">Tarea</span><span class="sxs-lookup"><span data-stu-id="e5c6b-106">Task</span></span></th>
<th align="left"><span data-ttu-id="e5c6b-107">Detalles y más información</span><span class="sxs-lookup"><span data-stu-id="e5c6b-107">Details and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5c6b-108">Para crear un archivo de paquete de claves de recuperación, acceda al <strong> </strong> área de recuperación de unidades del sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-108">Create a recovery key package file by accessing the <strong>Drive Recovery</strong> area of the Administration and Monitoring Website.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5c6b-109">Para acceder al <strong> área de recuperación de unidades </strong> , debe tener asignado el rol de usuarios del Departamento de soporte técnico de MBAM o el rol de usuarios avanzados de soporte técnico de MBAM.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-109">To access the <strong>Drive Recovery</strong> area, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="e5c6b-110">Es posible que haya dado a estos roles nombres diferentes al crearlos.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-110">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="e5c6b-111">Para obtener más información, consulte <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)"> planificación de grupos y cuentas de MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="e5c6b-111">For more information, see <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)">Planning for MBAM 2.5 Groups and Accounts</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="e5c6b-112">Copie el archivo de paquete en el equipo que contiene la unidad dañada.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-112">Copy the package file to the computer that contains the corrupted drive.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="e5c6b-113">Use el <code>repair-bde</code> comando para completar el proceso de recuperación.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-113">Use the <code>repair-bde</code> command to complete the recovery process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="e5c6b-114">Para evitar una posible pérdida de datos, se recomienda encarecidamente que revise el <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)"> comando Manage-BDE </a> antes de usarlo.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-114">To avoid a potential loss of data, it is strongly recommended that you review the <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)">Manage-bde</a> command before using it.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="e5c6b-115">Para recuperar una unidad dañada</span><span class="sxs-lookup"><span data-stu-id="e5c6b-115">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="e5c6b-116">Abra un explorador Web y vaya al **sitio web de administración y supervisión**.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="e5c6b-117">En el panel izquierdo, seleccione **recuperación de unidades** para abrir la página **recuperar el acceso a una unidad cifrada** .</span><span class="sxs-lookup"><span data-stu-id="e5c6b-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="e5c6b-118">Escriba el nombre de usuario y el dominio de inicio de sesión de Windows del usuario final, el motivo por el que se desbloquea la unidad y el identificador de contraseña de recuperación del usuario final.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-118">Enter the end user’s Windows log-on domain and user name, the reason for unlocking the drive, and the end user’s recovery password ID.</span></span>

    <span data-ttu-id="e5c6b-119">**Nota:**  Si es miembro del grupo de acceso avanzado de usuarios del servicio de asistencia al usuario, no tiene que escribir el nombre de dominio o el nombre de usuario del usuario.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-119">**Note** If you are a member of the Advanced Helpdesk Users access group, you do not have to enter the user’s domain name or user name.</span></span>

     

4.  <span data-ttu-id="e5c6b-120">Haz clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-120">Click **Submit**.</span></span> <span data-ttu-id="e5c6b-121">Se mostrará la clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-121">The recovery key will be displayed.</span></span>

5.  <span data-ttu-id="e5c6b-122">Haga clic en **Guardar**y, a continuación, seleccione **paquete de claves de recuperación**.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-122">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="e5c6b-123">Se creará el paquete de claves de recuperación en el equipo.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-123">The recovery key package will be created on your computer.</span></span>

6.  <span data-ttu-id="e5c6b-124">Copie el paquete de claves de recuperación en el equipo que tiene la unidad dañada.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-124">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

7.  <span data-ttu-id="e5c6b-125">Abre un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-125">Open an elevated command prompt.</span></span> <span data-ttu-id="e5c6b-126">Para ello, haga clic en **Inicio** y escriba `cmd` en el cuadro de texto **Buscar programas y archivos** .</span><span class="sxs-lookup"><span data-stu-id="e5c6b-126">To do this, click **Start** and type `cmd` in the **Search programs and files** text box.</span></span> <span data-ttu-id="e5c6b-127">Haga clic con el botón derecho en **cmd.exe**y seleccione **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-127">Right-click **cmd.exe**, and select **Run as Administrator**.</span></span>

8.  <span data-ttu-id="e5c6b-128">En el símbolo del sistema, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e5c6b-128">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="e5c6b-129">**Nota:**  Reemplazar &lt; una *unidad fija* &gt; por una unidad de disco duro disponible que tenga un espacio libre igual o mayor que los datos de la unidad dañada.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-129">**Note** Replace &lt;*fixed drive*&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="e5c6b-130">Los datos de la unidad dañada se recuperan y se mueven a la unidad de disco duro especificada.</span><span class="sxs-lookup"><span data-stu-id="e5c6b-130">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     


## <span data-ttu-id="e5c6b-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5c6b-131">Related topics</span></span>


[<span data-ttu-id="e5c6b-132">Realización de la administración de BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="e5c6b-132">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="e5c6b-133">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="e5c6b-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="e5c6b-134">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="e5c6b-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="e5c6b-135">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="e5c6b-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





