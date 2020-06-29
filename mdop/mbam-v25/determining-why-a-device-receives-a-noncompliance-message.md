---
title: Determinación de por qué un dispositivo recibe un mensaje de no conformidad
description: Determinación de por qué un dispositivo recibe un mensaje de no conformidad
author: dansimp
ms.assetid: 793df330-a0ee-4759-b53a-95618ac74428
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/22/2017
ms.openlocfilehash: ce1d344676ebf4328506228f1bfa87c76e8036f9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824571"
---
# <span data-ttu-id="30171-103">Determinación de por qué un dispositivo recibe un mensaje de no conformidad</span><span class="sxs-lookup"><span data-stu-id="30171-103">Determining why a Device Receives a Noncompliance Message</span></span>


<span data-ttu-id="30171-104">Los siguientes códigos de no cumplimiento son proporcionados por WMI y describen las razones por las que MBAM no cumple un determinado dispositivo.</span><span class="sxs-lookup"><span data-stu-id="30171-104">The following noncompliance codes are provided by WMI and describe the reasons why a particular device is reported by MBAM as noncompliant.</span></span>

<span data-ttu-id="30171-105">Puede usar su método preferido para ver WMI.</span><span class="sxs-lookup"><span data-stu-id="30171-105">You can use your preferred method to view WMI.</span></span> <span data-ttu-id="30171-106">Si usa PowerShell, ejecute `gwmi -class mbam_volume -Namespace root\microsoft\mbam` desde un símbolo del sistema de PowerShell y busque ReasonsForNoncompliance.</span><span class="sxs-lookup"><span data-stu-id="30171-106">If you use PowerShell, run `gwmi -class mbam_volume -Namespace root\microsoft\mbam` from a PowerShell prompt and search for ReasonsForNoncompliance.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="30171-107">Código de no conformidad</span><span class="sxs-lookup"><span data-stu-id="30171-107">Non-Compliance Code</span></span></th>
<th align="left"><span data-ttu-id="30171-108">Motivo del incumplimiento</span><span class="sxs-lookup"><span data-stu-id="30171-108">Reason for Non-Compliance</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30171-109">,0</span><span class="sxs-lookup"><span data-stu-id="30171-109">0</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-110">Intensidad de cifrado no AES 256.</span><span class="sxs-lookup"><span data-stu-id="30171-110">Cipher strength not AES 256.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30171-111">uno</span><span class="sxs-lookup"><span data-stu-id="30171-111">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-112">La Directiva MBAM requiere que este volumen se Cifre, pero no lo está.</span><span class="sxs-lookup"><span data-stu-id="30171-112">MBAM Policy requires this volume to be encrypted but it is not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30171-113">1</span><span class="sxs-lookup"><span data-stu-id="30171-113">2</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-114">La Directiva MBAM requiere que este volumen no se Cifre, pero sí.</span><span class="sxs-lookup"><span data-stu-id="30171-114">MBAM Policy requires this volume to NOT be encrypted, but it is.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30171-115">2</span><span class="sxs-lookup"><span data-stu-id="30171-115">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-116">La Directiva MBAM requiere que este volumen use un protector TPM, pero no lo hace.</span><span class="sxs-lookup"><span data-stu-id="30171-116">MBAM Policy requires this volume use a TPM protector, but it does not.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30171-117">cuatro</span><span class="sxs-lookup"><span data-stu-id="30171-117">4</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-118">La Directiva MBAM requiere que este volumen use un protector de TPM + PIN, pero no lo hace.</span><span class="sxs-lookup"><span data-stu-id="30171-118">MBAM Policy requires this volume use a TPM+PIN protector, but it does not.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30171-119">4</span><span class="sxs-lookup"><span data-stu-id="30171-119">5</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-120">La Directiva MBAM no permite que las máquinas que no sean de TPM se comuniquen como compatibles.</span><span class="sxs-lookup"><span data-stu-id="30171-120">MBAM Policy does not allow non TPM machines to report as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30171-121">6</span><span class="sxs-lookup"><span data-stu-id="30171-121">6</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-122">El volumen tiene un protector de TPM pero el TPM no está visible (se arranca con la clave de recuperación después de deshabilitar TPM en el BIOS?).</span><span class="sxs-lookup"><span data-stu-id="30171-122">Volume has a TPM protector but the TPM is not visible (booted with recover key after disabling TPM in BIOS?).</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30171-123">siete</span><span class="sxs-lookup"><span data-stu-id="30171-123">7</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-124">La Directiva MBAM requiere que este volumen use un protector de contraseña, pero no tiene una.</span><span class="sxs-lookup"><span data-stu-id="30171-124">MBAM Policy requires this volume use a password protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30171-125">4,8</span><span class="sxs-lookup"><span data-stu-id="30171-125">8</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-126">La Directiva MBAM requiere que este volumen no use un protector de contraseña, pero tiene uno.</span><span class="sxs-lookup"><span data-stu-id="30171-126">MBAM Policy requires this volume NOT use a password protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30171-127">99,999</span><span class="sxs-lookup"><span data-stu-id="30171-127">9</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-128">La Directiva MBAM requiere que este volumen use un protector de desbloqueo automático, pero no tiene una.</span><span class="sxs-lookup"><span data-stu-id="30171-128">MBAM Policy requires this volume use an auto-unlock protector, but it does not have one.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30171-129">base10</span><span class="sxs-lookup"><span data-stu-id="30171-129">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-130">La Directiva MBAM requiere que este volumen no use un protector de desbloqueo automático, pero tiene uno.</span><span class="sxs-lookup"><span data-stu-id="30171-130">MBAM Policy requires this volume NOT use an auto-unlock protector, but it has one.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30171-131">once</span><span class="sxs-lookup"><span data-stu-id="30171-131">11</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-132">Se detectó un conflicto de directiva que impide que MBAM informe de este volumen como compatible.</span><span class="sxs-lookup"><span data-stu-id="30171-132">Policy conflict detected preventing MBAM from reporting this volume as compliant.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30171-133">2007</span><span class="sxs-lookup"><span data-stu-id="30171-133">12</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-134">Se necesita un volumen del sistema para cifrar el volumen del sistema operativo, pero no está presente.</span><span class="sxs-lookup"><span data-stu-id="30171-134">A system volume is needed to encrypt the OS volume but it is not present.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30171-135">13</span><span class="sxs-lookup"><span data-stu-id="30171-135">13</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-136">Se ha suspendido la protección del volumen.</span><span class="sxs-lookup"><span data-stu-id="30171-136">Protection is suspended for the volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30171-137">n°</span><span class="sxs-lookup"><span data-stu-id="30171-137">14</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-138">Desbloqueo automático a menos que el volumen del sistema operativo esté cifrado.</span><span class="sxs-lookup"><span data-stu-id="30171-138">AutoUnlock unsafe unless the OS volume is encrypted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="30171-139">4,5</span><span class="sxs-lookup"><span data-stu-id="30171-139">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-140">La Directiva requiere una intensidad de cifrado mínima es XTS-AES-128 bit, la intensidad de cifrado real es más débil.</span><span class="sxs-lookup"><span data-stu-id="30171-140">Policy requires minimum cypher strength is XTS-AES-128 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="30171-141">apartado</span><span class="sxs-lookup"><span data-stu-id="30171-141">16</span></span></p></td>
<td align="left"><p><span data-ttu-id="30171-142">La Directiva requiere una intensidad de cifrado mínima es XTS-AES-256 bit, la intensidad de cifrado real es más débil.</span><span class="sxs-lookup"><span data-stu-id="30171-142">Policy requires minimum cypher strength is XTS-AES-256 bit, actual cypher strength is weaker than that.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="30171-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30171-143">Related topics</span></span>


[<span data-ttu-id="30171-144">Referencia técnica de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="30171-144">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="30171-145">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="30171-145">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 
## <span data-ttu-id="30171-146">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="30171-146">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="30171-147">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="30171-147">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="30171-148">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="30171-148">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





