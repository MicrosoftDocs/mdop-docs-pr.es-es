---
title: Cómo recuperar una unidad dañada
description: Cómo recuperar una unidad dañada
author: dansimp
ms.assetid: 715491ae-69c0-4fae-ad3f-3bd19a0db2f2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 545ff5c7e6bea29d5f89cce1cf18212b7d0e2870
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812943"
---
# <span data-ttu-id="02cf6-103">Cómo recuperar una unidad dañada</span><span class="sxs-lookup"><span data-stu-id="02cf6-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="02cf6-104">Para recuperar una unidad dañada que ha sido protegida por BitLocker, un usuario del servicio de asistencia de supervisión y administración de Microsoft BitLocker (MBAM) debe crear un archivo de paquete de claves de recuperación.</span><span class="sxs-lookup"><span data-stu-id="02cf6-104">To recover a corrupted drive that has been protected by BitLocker, a Microsoft BitLocker Administration and Monitoring (MBAM) help desk user must create a recovery key package file.</span></span> <span data-ttu-id="02cf6-105">Este archivo de paquete puede copiarse en el equipo que contiene la unidad dañada y, a continuación, usarse para recuperar la unidad.</span><span class="sxs-lookup"><span data-stu-id="02cf6-105">This package file can be copied to the computer that contains the corrupted drive and then used to recover the drive.</span></span> <span data-ttu-id="02cf6-106">Para ello, use el procedimiento siguiente.</span><span class="sxs-lookup"><span data-stu-id="02cf6-106">To accomplish this, use the following procedure.</span></span>

**<span data-ttu-id="02cf6-107">Para recuperar una unidad dañada</span><span class="sxs-lookup"><span data-stu-id="02cf6-107">To Recover a Corrupted Drive</span></span>**

1.  <span data-ttu-id="02cf6-108">Abra el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="02cf6-108">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="02cf6-109">Seleccione **recuperación de unidades** en el panel de navegación.</span><span class="sxs-lookup"><span data-stu-id="02cf6-109">Select **Drive Recovery** from the navigation pane.</span></span> <span data-ttu-id="02cf6-110">Escriba el nombre de dominio y el nombre de usuario del usuario, el motivo por el que se desbloqueó la unidad y el identificador de contraseña de recuperación del usuario.</span><span class="sxs-lookup"><span data-stu-id="02cf6-110">Enter the user’s domain name and user name, the reason for unlocking the drive, and the user’s recovery password ID.</span></span>

    <span data-ttu-id="02cf6-111">**Nota:**  Si es miembro del rol de administradores del servicio de asistencia, no es necesario que escriba el nombre de dominio o el nombre de usuario del usuario.</span><span class="sxs-lookup"><span data-stu-id="02cf6-111">**Note** If you are a member of the Help Desk Administrators role, you do not have to enter the user’s domain name or user name.</span></span>

     

3.  <span data-ttu-id="02cf6-112">Haz clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="02cf6-112">Click **Submit**.</span></span> <span data-ttu-id="02cf6-113">Se mostrará la clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="02cf6-113">The recovery key will be displayed.</span></span>

4.  <span data-ttu-id="02cf6-114">Haga clic en **Guardar**y, a continuación, seleccione **paquete de claves de recuperación**.</span><span class="sxs-lookup"><span data-stu-id="02cf6-114">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="02cf6-115">Se creará el paquete de claves de recuperación en el equipo.</span><span class="sxs-lookup"><span data-stu-id="02cf6-115">The recovery key package will be created on your computer.</span></span>

5.  <span data-ttu-id="02cf6-116">Copie el paquete de claves de recuperación en el equipo que tiene la unidad dañada.</span><span class="sxs-lookup"><span data-stu-id="02cf6-116">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

6.  <span data-ttu-id="02cf6-117">Abre un símbolo del sistema con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="02cf6-117">Open an elevated command prompt.</span></span> <span data-ttu-id="02cf6-118">Para ello, haga clic en **Inicio** y escriba `cmd` en el cuadro **Buscar programas y archivos** .</span><span class="sxs-lookup"><span data-stu-id="02cf6-118">To do this, click **Start** and type `cmd` in the **Search programs and files** box.</span></span> <span data-ttu-id="02cf6-119">En la lista de resultados de la búsqueda, haga clic con el botón derecho en **cmd.exe** y seleccione **Ejecutar como administrador**.</span><span class="sxs-lookup"><span data-stu-id="02cf6-119">In the search results list, right-click **cmd.exe** and select **Run as Administrator**.</span></span>

7.  <span data-ttu-id="02cf6-120">En el símbolo del sistema, escriba lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="02cf6-120">At the command prompt, type the following:</span></span>

    `repair-bde <fixed drive> <corrupted drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="02cf6-121">**Nota:**  Para la &lt; unidad fija &gt; en el comando, especifique un dispositivo de almacenamiento disponible que tenga espacio libre igual o mayor que los datos de la unidad dañada.</span><span class="sxs-lookup"><span data-stu-id="02cf6-121">**Note** For the &lt;fixed drive&gt; in the command, specify an available storage device that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="02cf6-122">Los datos de la unidad dañada se recuperan y se mueven a la unidad fija especificada.</span><span class="sxs-lookup"><span data-stu-id="02cf6-122">Data on the corrupted drive is recovered and moved to the specified fixed drive.</span></span>

     

## <span data-ttu-id="02cf6-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02cf6-123">Related topics</span></span>


[<span data-ttu-id="02cf6-124">Realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="02cf6-124">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





