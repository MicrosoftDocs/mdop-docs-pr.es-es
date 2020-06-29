---
title: Cómo recuperar una unidad dañada
description: Cómo recuperar una unidad dañada
author: dansimp
ms.assetid: b0457a00-f72e-4ad8-ab3b-7701851ca87e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5bbd4c2a1f5ef3fde78a9f72c1f77ccb0cdea377
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822871"
---
# <span data-ttu-id="47dd7-103">Cómo recuperar una unidad dañada</span><span class="sxs-lookup"><span data-stu-id="47dd7-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="47dd7-104">Para recuperar una unidad dañada protegida por BitLocker, un usuario del servicio de asistencia de supervisión y administración de Microsoft BitLocker (MBAM) necesitará crear un archivo de paquete de claves de recuperación.</span><span class="sxs-lookup"><span data-stu-id="47dd7-104">To recover a corrupted drive protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) Help Desk user will need to create a recovery key package file.</span></span> <span data-ttu-id="47dd7-105">Este archivo de paquete puede copiarse en el equipo que contiene la unidad dañada y, a continuación, usarse para recuperar la unidad.</span><span class="sxs-lookup"><span data-stu-id="47dd7-105">This package file can then be copied to the computer that contains the corrupted drive, and then used to recover the drive.</span></span> <span data-ttu-id="47dd7-106">Use el procedimiento siguiente para los pasos necesarios para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="47dd7-106">Use the following procedure for the steps needed to do this.</span></span>

<span data-ttu-id="47dd7-107">**Importante**  Para evitar una posible pérdida de datos, se recomienda encarecidamente que lea la ayuda "repair-BDE" y entienda claramente cómo usar el comando antes de completar las siguientes instrucciones.</span><span class="sxs-lookup"><span data-stu-id="47dd7-107">**Important** To avoid a potential loss of data, it is strongly recommended that you read the “repair-bde” help and clearly understand how to use the command before completing the following instructions.</span></span>

 

**<span data-ttu-id="47dd7-108">Para recuperar una unidad dañada</span><span class="sxs-lookup"><span data-stu-id="47dd7-108">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="47dd7-109">Para crear el paquete de claves de recuperación necesario para recuperar una unidad dañada, inicie un explorador Web y abra el sitio web de administración y supervisión de MBAM.</span><span class="sxs-lookup"><span data-stu-id="47dd7-109">To create the recovery key package necessary to recover a corrupted drive, start a web browser and open the MBAM Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="47dd7-110">Seleccione **recuperación de unidades** en el panel de navegación izquierdo.</span><span class="sxs-lookup"><span data-stu-id="47dd7-110">Select **Drive Recovery** from the left navigation pane.</span></span> <span data-ttu-id="47dd7-111">Escriba el nombre de dominio del usuario, el nombre de usuario, el motivo de desbloqueo de la unidad y el identificador de contraseña de recuperación del usuario.</span><span class="sxs-lookup"><span data-stu-id="47dd7-111">Enter the user’s domain name, user name, reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="47dd7-112">**Nota:**  Si es miembro del rol de administradores del servicio de asistencia, no es necesario que escriba el nombre de dominio o el nombre de usuario del usuario.</span><span class="sxs-lookup"><span data-stu-id="47dd7-112">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="47dd7-113">Haz clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="47dd7-113">Click **Submit**.</span></span> <span data-ttu-id="47dd7-114">Se mostrará la clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="47dd7-114">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="47dd7-115">Haga clic en **Guardar**y, a continuación, seleccione **paquete de claves de recuperación**.</span><span class="sxs-lookup"><span data-stu-id="47dd7-115">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="47dd7-116">Se creará el paquete de claves de recuperación en el equipo.</span><span class="sxs-lookup"><span data-stu-id="47dd7-116">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="47dd7-117">Copie el paquete de claves de recuperación en el equipo que tiene la unidad dañada.</span><span class="sxs-lookup"><span data-stu-id="47dd7-117">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="47dd7-118">Abre un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="47dd7-118">Open an elevated command prompt.</span></span> <span data-ttu-id="47dd7-119">Para ello, haga clic en **Inicio** y escriba `cmd` en el **cuadro Buscar programas y archivos**.</span><span class="sxs-lookup"><span data-stu-id="47dd7-119">To do this, click **Start** and type `cmd` in the **Search programs and files box**.</span></span> <span data-ttu-id="47dd7-120">Haga clic con el botón derecho en **cmd.exe** y seleccione **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="47dd7-120">Right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="47dd7-121">En el símbolo del sistema, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="47dd7-121">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="47dd7-122">**Nota:**  Reemplazar &lt; una unidad fija &gt; por una unidad de disco duro disponible que tenga un espacio libre igual o mayor que los datos de la unidad dañada.</span><span class="sxs-lookup"><span data-stu-id="47dd7-122">**Note** Replace &lt;fixed drive&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="47dd7-123">Los datos de la unidad dañada se recuperan y se mueven a la unidad de disco duro especificada.</span><span class="sxs-lookup"><span data-stu-id="47dd7-123">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     

## <span data-ttu-id="47dd7-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="47dd7-124">Related topics</span></span>


[<span data-ttu-id="47dd7-125">Realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="47dd7-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





