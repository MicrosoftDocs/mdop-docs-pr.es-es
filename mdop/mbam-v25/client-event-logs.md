---
title: Registros de eventos de cliente
description: Registros de eventos de cliente
author: dansimp
ms.assetid: d5c2f270-db6a-45f1-8557-8c6fb28fd568
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7324d07bf018944fcbe24168bba2e9abea9cea41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824191"
---
# <span data-ttu-id="db674-103">Registros de eventos de cliente</span><span class="sxs-lookup"><span data-stu-id="db674-103">Client Event Logs</span></span>

<span data-ttu-id="db674-104">Los registros de eventos de MBAM se encuentran en visor de eventos: registros de aplicaciones y servicios – Microsoft – Windows – MBAM-Operational path.</span><span class="sxs-lookup"><span data-stu-id="db674-104">MBAM Client event logs are located in Event Viewer – Applications and Services Logs – Microsoft – Windows – MBAM - Operational path.</span></span>
<span data-ttu-id="db674-105">La tabla siguiente contiene los identificadores de eventos que se pueden producir en el cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="db674-105">The following table contains event IDs that can occur on the MBAM Client.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="db674-106">Id. de evento</span><span class="sxs-lookup"><span data-stu-id="db674-106">Event ID</span></span></th>
<th align="left"><span data-ttu-id="db674-107">Canal</span><span class="sxs-lookup"><span data-stu-id="db674-107">Channel</span></span></th>
<th align="left"><span data-ttu-id="db674-108">Símbolo de evento</span><span class="sxs-lookup"><span data-stu-id="db674-108">Event symbol</span></span></th>
<th align="left"><span data-ttu-id="db674-109">Mensaje</span><span class="sxs-lookup"><span data-stu-id="db674-109">Message</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-110">uno</span><span class="sxs-lookup"><span data-stu-id="db674-110">1</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-111">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-111">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-112">VolumeEnactmentSuccessful</span><span class="sxs-lookup"><span data-stu-id="db674-112">VolumeEnactmentSuccessful</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-113">Las directivas de MBAM se aplicaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="db674-113">The MBAM policies were applied successfully.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-114">1</span><span class="sxs-lookup"><span data-stu-id="db674-114">2</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-115">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-115">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-116">VolumeEnactmentFailed</span><span class="sxs-lookup"><span data-stu-id="db674-116">VolumeEnactmentFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-117">Se produjo un error al aplicar las directivas de MBAM.</span><span class="sxs-lookup"><span data-stu-id="db674-117">An error occurred while applying MBAM policies.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-118">2</span><span class="sxs-lookup"><span data-stu-id="db674-118">3</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-119">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-119">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-120">TransferStatusDataSuccessful</span><span class="sxs-lookup"><span data-stu-id="db674-120">TransferStatusDataSuccessful</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-121">Los datos de estado de cifrado se enviaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="db674-121">The encryption status data was sent successfully.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-122">cuatro</span><span class="sxs-lookup"><span data-stu-id="db674-122">4</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-123">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-123">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-124">TransferStatusDataFailed</span><span class="sxs-lookup"><span data-stu-id="db674-124">TransferStatusDataFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-125">Se produjo un error al enviar datos de estado de cifrado.</span><span class="sxs-lookup"><span data-stu-id="db674-125">An error occurred while sending encryption status data.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-126">4,8</span><span class="sxs-lookup"><span data-stu-id="db674-126">8</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-127">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-127">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-128">SystemVolumeNotFound</span><span class="sxs-lookup"><span data-stu-id="db674-128">SystemVolumeNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-129">Falta el volumen del sistema.</span><span class="sxs-lookup"><span data-stu-id="db674-129">The system volume is missing.</span></span> <span data-ttu-id="db674-130">SystemVolume es necesario para cifrar la unidad del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="db674-130">SystemVolume is needed to encrypt the operating system drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-131">99,999</span><span class="sxs-lookup"><span data-stu-id="db674-131">9</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-132">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-132">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-133">TPMNotFound</span><span class="sxs-lookup"><span data-stu-id="db674-133">TPMNotFound</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-134">Falta el hardware TPM.</span><span class="sxs-lookup"><span data-stu-id="db674-134">The TPM hardware is missing.</span></span> <span data-ttu-id="db674-135">Se necesita TPM para cifrar la unidad del sistema operativo con cualquier protector de TPM.</span><span class="sxs-lookup"><span data-stu-id="db674-135">TPM is needed to encrypt the operating system drive with any TPM protector.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-136">base10</span><span class="sxs-lookup"><span data-stu-id="db674-136">10</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-137">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-137">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-138">MachineHWExempted</span><span class="sxs-lookup"><span data-stu-id="db674-138">MachineHWExempted</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-139">El equipo está exento del cifrado.</span><span class="sxs-lookup"><span data-stu-id="db674-139">The computer is exempted from Encryption.</span></span> <span data-ttu-id="db674-140">Estado del hardware de la máquina: excluido</span><span class="sxs-lookup"><span data-stu-id="db674-140">Machine’s hardware status: Exempted</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-141">once</span><span class="sxs-lookup"><span data-stu-id="db674-141">11</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-142">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-142">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-143">MachineHWUnknown</span><span class="sxs-lookup"><span data-stu-id="db674-143">MachineHWUnknown</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-144">El equipo está exento del cifrado.</span><span class="sxs-lookup"><span data-stu-id="db674-144">The computer is exempted from encryption.</span></span> <span data-ttu-id="db674-145">Estado del hardware de la máquina: desconocido</span><span class="sxs-lookup"><span data-stu-id="db674-145">Machine’s hardware status: Unknown</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-146">2007</span><span class="sxs-lookup"><span data-stu-id="db674-146">12</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-147">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-147">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-148">HWCheckFailed</span><span class="sxs-lookup"><span data-stu-id="db674-148">HWCheckFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-149">Error al comprobar la exención de hardware.</span><span class="sxs-lookup"><span data-stu-id="db674-149">Hardware exemption check failed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-150">13</span><span class="sxs-lookup"><span data-stu-id="db674-150">13</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-151">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-151">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-152">UserIsExempted</span><span class="sxs-lookup"><span data-stu-id="db674-152">UserIsExempted</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-153">El usuario está exento del cifrado.</span><span class="sxs-lookup"><span data-stu-id="db674-153">The user is exempt from encryption.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-154">n°</span><span class="sxs-lookup"><span data-stu-id="db674-154">14</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-155">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-155">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-156">UserIsWaiting</span><span class="sxs-lookup"><span data-stu-id="db674-156">UserIsWaiting</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-157">El usuario solicitó una exención.</span><span class="sxs-lookup"><span data-stu-id="db674-157">The user requested an exemption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-158">4,5</span><span class="sxs-lookup"><span data-stu-id="db674-158">15</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-159">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-159">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-160">UserExemptionCheckFailed</span><span class="sxs-lookup"><span data-stu-id="db674-160">UserExemptionCheckFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-161">Error en la comprobación de exención de usuario.</span><span class="sxs-lookup"><span data-stu-id="db674-161">User exemption check failed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-162">apartado</span><span class="sxs-lookup"><span data-stu-id="db674-162">16</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-163">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-163">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-164">UserPostponed</span><span class="sxs-lookup"><span data-stu-id="db674-164">UserPostponed</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-165">El usuario pospuso el proceso de cifrado.</span><span class="sxs-lookup"><span data-stu-id="db674-165">The user postponed the encryption process.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-166">apartado</span><span class="sxs-lookup"><span data-stu-id="db674-166">17</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-167">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-167">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-168">TPMInitializationFailed</span><span class="sxs-lookup"><span data-stu-id="db674-168">TPMInitializationFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-169">Error al inicializar TPM.</span><span class="sxs-lookup"><span data-stu-id="db674-169">TPM initialization failed.</span></span> <span data-ttu-id="db674-170">El usuario rechazó los cambios de BIOS.</span><span class="sxs-lookup"><span data-stu-id="db674-170">The user rejected the BIOS changes.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-171">18</span><span class="sxs-lookup"><span data-stu-id="db674-171">18</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-172">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-172">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-173">CoreServiceDown</span><span class="sxs-lookup"><span data-stu-id="db674-173">CoreServiceDown</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-174">No se puede conectar con el servicio de hardware y recuperación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="db674-174">Unable to connect to the MBAM Recovery and Hardware service.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-175">19</span><span class="sxs-lookup"><span data-stu-id="db674-175">19</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-176">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-176">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-177">CoreServiceUp</span><span class="sxs-lookup"><span data-stu-id="db674-177">CoreServiceUp</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-178">Se ha conectado correctamente al servicio de hardware y recuperación de MBAM.</span><span class="sxs-lookup"><span data-stu-id="db674-178">Successfully connected to the MBAM Recovery and Hardware service.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-179">veinte</span><span class="sxs-lookup"><span data-stu-id="db674-179">20</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-180">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-180">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-181">PolicyMismatch</span><span class="sxs-lookup"><span data-stu-id="db674-181">PolicyMismatch</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-182">La Directiva MBAM está en conflicto o está dañada.</span><span class="sxs-lookup"><span data-stu-id="db674-182">The MBAM policy is in conflict or corrupt.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-183">21Vianet</span><span class="sxs-lookup"><span data-stu-id="db674-183">21</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-184">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-184">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-185">ConflictingOSVolumePolicies</span><span class="sxs-lookup"><span data-stu-id="db674-185">ConflictingOSVolumePolicies</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-186">Se detectaron conflictos de directivas de cifrado de volumen de so.</span><span class="sxs-lookup"><span data-stu-id="db674-186">Detected OS volume encryption policies conflict.</span></span> <span data-ttu-id="db674-187">Comprobar las directivas de BitLocker y MBAM relacionadas con los protectores de unidad de OS.</span><span class="sxs-lookup"><span data-stu-id="db674-187">Check BitLocker and MBAM policies related to OS drive protectors.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-188">23</span><span class="sxs-lookup"><span data-stu-id="db674-188">22</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-189">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-189">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-190">ConflictingFDDVolumePolicies</span><span class="sxs-lookup"><span data-stu-id="db674-190">ConflictingFDDVolumePolicies</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-191">Se detectaron conflictos de directivas de cifrado de volumen de unidad de datos fijos.</span><span class="sxs-lookup"><span data-stu-id="db674-191">Detected Fixed Data Drive volume encryption policies conflict.</span></span> <span data-ttu-id="db674-192">Comprobar las directivas de BitLocker y MBAM relacionadas con protectores de unidad FDD.</span><span class="sxs-lookup"><span data-stu-id="db674-192">Check BitLocker and MBAM policies related to FDD drive protectors.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-193">,27</span><span class="sxs-lookup"><span data-stu-id="db674-193">27</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-194">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-194">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-195">EncryptionFailedNoDra</span><span class="sxs-lookup"><span data-stu-id="db674-195">EncryptionFailedNoDra</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-196">Se produjo un error durante el cifrado.</span><span class="sxs-lookup"><span data-stu-id="db674-196">An error occurred while encrypting.</span></span> <span data-ttu-id="db674-197">Es necesario un protector de agente de recuperación de datos (DRA) en el modo FIPS para equipos anteriores a Windows 8,1.</span><span class="sxs-lookup"><span data-stu-id="db674-197">A Data Recovery Agent (DRA) protector is required in FIPS mode for pre-Windows 8.1 machines.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-198">apartado</span><span class="sxs-lookup"><span data-stu-id="db674-198">28</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-199">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-199">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-200">TpmOwnerAuthEscrowed</span><span class="sxs-lookup"><span data-stu-id="db674-200">TpmOwnerAuthEscrowed</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-201">El TPM OwnerAuth se ha enviado a un depósito de garantía.</span><span class="sxs-lookup"><span data-stu-id="db674-201">The TPM OwnerAuth has been escrowed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-202">32</span><span class="sxs-lookup"><span data-stu-id="db674-202">29</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-203">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-203">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-204">RecoveryKeyEscrowed</span><span class="sxs-lookup"><span data-stu-id="db674-204">RecoveryKeyEscrowed</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-205">La clave de recuperación de BitLocker para el volumen se ha enviado un depósito de garantía.</span><span class="sxs-lookup"><span data-stu-id="db674-205">The BitLocker recovery key for the volume has been escrowed.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-206">0,30</span><span class="sxs-lookup"><span data-stu-id="db674-206">30</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-207">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-207">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-208">RecoveryKeyReset</span><span class="sxs-lookup"><span data-stu-id="db674-208">RecoveryKeyReset</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-209">La clave de recuperación de BitLocker para el volumen se ha actualizado.</span><span class="sxs-lookup"><span data-stu-id="db674-209">The BitLocker recovery key for the volume has been updated.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-210">35</span><span class="sxs-lookup"><span data-stu-id="db674-210">31</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-211">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-211">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-212">EnforcePolicyDateSet</span><span class="sxs-lookup"><span data-stu-id="db674-212">EnforcePolicyDateSet</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-213">Se ha establecido la fecha de cumplimiento de la fecha, la fecha, <em> &lt; &gt; </em> para el volumen</span><span class="sxs-lookup"><span data-stu-id="db674-213">The enforce policy date, <em>&lt;date&gt;</em>, has been set for the volume</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-214">32</span><span class="sxs-lookup"><span data-stu-id="db674-214">32</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-215">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-215">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-216">EnforcePolicyDateCleared</span><span class="sxs-lookup"><span data-stu-id="db674-216">EnforcePolicyDateCleared</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-217">Se <em> &lt; ha borrado la fecha de cumplimiento de la fecha y la fecha &gt; </em> de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="db674-217">The enforce policy date, <em>&lt;date&gt;</em>, has been cleared for the volume.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-218">33</span><span class="sxs-lookup"><span data-stu-id="db674-218">33</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-219">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-219">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-220">TpmLockOutResetSucceeded</span><span class="sxs-lookup"><span data-stu-id="db674-220">TpmLockOutResetSucceeded</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-221">Se restableció correctamente el bloqueo de TPM.</span><span class="sxs-lookup"><span data-stu-id="db674-221">Successfully reset TPM lockout.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-222">34</span><span class="sxs-lookup"><span data-stu-id="db674-222">34</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-223">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-223">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-224">TpmLockOutResetFailed</span><span class="sxs-lookup"><span data-stu-id="db674-224">TpmLockOutResetFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-225">Error al restablecer el bloqueo de TPM.</span><span class="sxs-lookup"><span data-stu-id="db674-225">Failed to reset TPM lockout.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-226">35</span><span class="sxs-lookup"><span data-stu-id="db674-226">35</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-227">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-227">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-228">TpmOwnerAuthRetrievalSucceeded</span><span class="sxs-lookup"><span data-stu-id="db674-228">TpmOwnerAuthRetrievalSucceeded</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-229">OwnerAuth de TPM recuperados correctamente de los servicios de MBAM.</span><span class="sxs-lookup"><span data-stu-id="db674-229">Successfully retrieved TPM OwnerAuth from MBAM services.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-230">36</span><span class="sxs-lookup"><span data-stu-id="db674-230">36</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-231">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-231">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-232">TpmOwnerAuthRetrievalFailed</span><span class="sxs-lookup"><span data-stu-id="db674-232">TpmOwnerAuthRetrievalFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-233">Error al recuperar el TPM OwnerAuth de los servicios de MBAM.</span><span class="sxs-lookup"><span data-stu-id="db674-233">Failed to retrieve TPM OwnerAuth from MBAM services.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-234">37</span><span class="sxs-lookup"><span data-stu-id="db674-234">37</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-235">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-235">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-236">WmiProviderDllSearchPathUpdateFailed</span><span class="sxs-lookup"><span data-stu-id="db674-236">WmiProviderDllSearchPathUpdateFailed</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-237">Error al actualizar la ruta de búsqueda de archivos DLL para el proveedor WMI.</span><span class="sxs-lookup"><span data-stu-id="db674-237">Failed to update the DLL search path for WMI provider.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-238">38</span><span class="sxs-lookup"><span data-stu-id="db674-238">38</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-239">Administrador</span><span class="sxs-lookup"><span data-stu-id="db674-239">Admin</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-240">TimedOutWaitingForWmiProvider</span><span class="sxs-lookup"><span data-stu-id="db674-240">TimedOutWaitingForWmiProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-241">El agente se ha detenido: ha agotado el tiempo de espera para la instancia de proveedor WMI de MBAM.</span><span class="sxs-lookup"><span data-stu-id="db674-241">Agent Stopping - Timed-out waiting for MBAM WMI Provider Instance.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-242">39</span><span class="sxs-lookup"><span data-stu-id="db674-242">39</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-243">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-243">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-244">RemovableDriveMounted</span><span class="sxs-lookup"><span data-stu-id="db674-244">RemovableDriveMounted</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-245">Se montó la unidad extraíble.</span><span class="sxs-lookup"><span data-stu-id="db674-245">Removable drive was mounted.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-246">40</span><span class="sxs-lookup"><span data-stu-id="db674-246">40</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-247">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-247">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-248">RemovableDriveDismounted</span><span class="sxs-lookup"><span data-stu-id="db674-248">RemovableDriveDismounted</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-249">Se desmontó la unidad extraíble.</span><span class="sxs-lookup"><span data-stu-id="db674-249">Removable drive was unmounted.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-250">41</span><span class="sxs-lookup"><span data-stu-id="db674-250">41</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-251">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-251">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-252">FailedToEnactEndpointUnreachable</span><span class="sxs-lookup"><span data-stu-id="db674-252">FailedToEnactEndpointUnreachable</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-253">Si se produce un error al conectarse al servicio de hardware y recuperación de MBAM no se pudieron aplicar al volumen las directivas de MBAM correctamente.</span><span class="sxs-lookup"><span data-stu-id="db674-253">Failure to connect to the MBAM Recovery and Hardware service prevented MBAM policies from being applied successfully to the volume.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="db674-254">42</span><span class="sxs-lookup"><span data-stu-id="db674-254">42</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-255">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-255">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-256">FailedToEnactLockedVolume</span><span class="sxs-lookup"><span data-stu-id="db674-256">FailedToEnactLockedVolume</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-257">El estado de volumen bloqueado evitó que las directivas de MBAM se aplicaran correctamente al volumen.</span><span class="sxs-lookup"><span data-stu-id="db674-257">Locked volume state prevented MBAM policies from being applied successfully to the volume.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="db674-258">43</span><span class="sxs-lookup"><span data-stu-id="db674-258">43</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-259">Funcionamiento</span><span class="sxs-lookup"><span data-stu-id="db674-259">Operational</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-260">TransferStatusDataFailedEndpointUnreachable</span><span class="sxs-lookup"><span data-stu-id="db674-260">TransferStatusDataFailedEndpointUnreachable</span></span></p></td>
<td align="left"><p><span data-ttu-id="db674-261">Si se produce un error al conectarse al servicio de cumplimiento y estado de MBAM, no se podrán transferir los datos de estado de cifrado.</span><span class="sxs-lookup"><span data-stu-id="db674-261">Failure to connect to the MBAM Compliance and Status service prevented the transfer of encryption status data.</span></span></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="db674-262">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db674-262">Related topics</span></span>
[<span data-ttu-id="db674-263">Referencia técnica de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="db674-263">Technical Reference for MBAM 2.5</span></span>](technical-reference-for-mbam-25.md)

[<span data-ttu-id="db674-264">Registros de eventos de servidor</span><span class="sxs-lookup"><span data-stu-id="db674-264">Server Event Logs</span></span>](server-event-logs.md)

 


## <span data-ttu-id="db674-265">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="db674-265">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="db674-266">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="db674-266">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="db674-267">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="db674-267">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





