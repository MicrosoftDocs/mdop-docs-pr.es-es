---
title: Requisitos previos para clientes MBAM 2.5
description: Requisitos previos para clientes MBAM 2.5
author: dansimp
ms.assetid: fc230679-9c84-4b99-a77c-bae7e7bf8145
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: ac5e211e5ea038f47db3d5e68155eb5af38aa231
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826970"
---
# <span data-ttu-id="97d63-103">Requisitos previos para clientes MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="97d63-103">Prerequisites for MBAM 2.5 Clients</span></span>


<span data-ttu-id="97d63-104">Antes de instalar el software de cliente de MBAM en los equipos de los usuarios finales, asegúrese de que el entorno y los equipos cliente cumplan los siguientes requisitos previos.</span><span class="sxs-lookup"><span data-stu-id="97d63-104">Before you install the MBAM Client software on end users' computers, ensure that your environment and the client computers meet the following prerequisites.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="97d63-105">Como requisito previo</span><span class="sxs-lookup"><span data-stu-id="97d63-105">Prerequisite</span></span></th>
<th align="left"><span data-ttu-id="97d63-106">Detalles</span><span class="sxs-lookup"><span data-stu-id="97d63-106">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="97d63-107">El dominio de la empresa debe contener al menos un controlador de dominio de Windows Server 2008 (o posterior).</span><span class="sxs-lookup"><span data-stu-id="97d63-107">The enterprise domain must contain at least one Windows Server 2008 (or later) domain controller.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="97d63-108">El equipo cliente debe haber iniciado sesión en la intranet de la empresa.</span><span class="sxs-lookup"><span data-stu-id="97d63-108">The client computer must be logged on to the enterprise intranet.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="97d63-109">Solo para equipos cliente de Windows 7: cada cliente debe tener capacidad de módulo de plataforma segura (TPM) (TPM 1,2 o posterior).</span><span class="sxs-lookup"><span data-stu-id="97d63-109">For Windows 7 client computers only: Each client must have Trusted Platform Module (TPM) capability (TPM 1.2 or later).</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="97d63-110">Para equipos cliente con Windows 8,1, Windows 10 RTM o Windows 10 versión 1511 solamente: Si desea que MBAM pueda almacenar y administrar las claves de recuperación de TPM, el aprovisionamiento automático de TPM debe estar desactivado, y MBAM debe estar configurado como propietario de TPM antes de implementar MBAM.</span><span class="sxs-lookup"><span data-stu-id="97d63-110">For Windows 8.1, Windows 10 RTM or Windows 10 version 1511 client computers only: If you want MBAM to be able to store and manage the TPM recovery keys, TPM auto-provisioning must be turned off, and MBAM must be set as the owner of the TPM before you deploy MBAM.</span></span></p>
<p><span data-ttu-id="97d63-111">Solo en el SP1 de MBAM 2,5, ya no necesita desactivar el aprovisionamiento automático de TPM, pero debe asegurarse de que los objetos de directiva de grupo de TPM estén establecidos en no custodiar TPM OwnerAuth a Active Directory.</span><span class="sxs-lookup"><span data-stu-id="97d63-111">In MBAM 2.5 SP1 only, you no longer need to turn off TPM auto-provisioning, but you must make sure that the TPM Group Policy Objects are set to not escrow TPM OwnerAuth to Active Directory.</span></span></p></td>
<td align="left"><p><a href="mbam-25-security-considerations.md#bkmk-tpm" data-raw-source="[MBAM 2.5 Security Considerations](mbam-25-security-considerations.md#bkmk-tpm)"><span data-ttu-id="97d63-112">Consideraciones sobre seguridad de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="97d63-112">MBAM 2.5 Security Considerations</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="97d63-113">Para Windows 10, versión 1607 o posterior, solo Windows puede tomar posesión de TPM.</span><span class="sxs-lookup"><span data-stu-id="97d63-113">For Windows 10, version 1607 or later, only Windows can take ownership of the TPM.</span></span> <span data-ttu-id="97d63-114">En addiiton, Windows no conservará la contraseña de propietario de TPM al aprovisionar el TPM.</span><span class="sxs-lookup"><span data-stu-id="97d63-114">In addiiton, Windows will not retain the TPM owner password when provisioning the TPM.</span></span></p>
<p><span data-ttu-id="97d63-115">En MBAM 2,5 SP1, debe activar el aprovisionamiento automático.</span><span class="sxs-lookup"><span data-stu-id="97d63-115">In MBAM 2.5 SP1, you must turn on auto-provisioning.</span></span></p>
</p></td>
<td align="left"><p><span data-ttu-id="97d63-116">Para obtener más información, consulta la <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)"> contraseña </a> de propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="97d63-116">See <a href="https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password" data-raw-source="[TPM owner password](https://technet.microsoft.com/itpro/windows/keep-secure/change-the-tpm-owner-password)">TPM owner password</a> for further details.</span></span>
</p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="97d63-117">El chip TPM debe estar activado en el BIOS y puede reestablecerse desde el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="97d63-117">The TPM chip must be turned on in the BIOS and be resettable from the operating system.</span></span></p></td>
<td align="left"><p><span data-ttu-id="97d63-118">Para obtener más información, consulta la documentación del BIOS.</span><span class="sxs-lookup"><span data-stu-id="97d63-118">See the BIOS documentation for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="97d63-119">El disco duro del equipo debe tener al menos dos particiones y debe tener el formato del sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="97d63-119">The computer’s hard disk must have at least two partitions and must be formatted with the NTFS file system.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="97d63-120">El disco duro del equipo debe tener un BIOS que sea compatible con el TPM y que admita dispositivos USB durante el inicio del equipo.</span><span class="sxs-lookup"><span data-stu-id="97d63-120">The computer’s hard disk must have a BIOS that is compatible with TPM and that supports USB devices during computer startup.</span></span></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="97d63-121">Nota</span><span class="sxs-lookup"><span data-stu-id="97d63-121">Note</span></span></strong><br/><p><span data-ttu-id="97d63-122">Asegúrese de que el teclado, el vídeo o el ratón estén directamente conectados y no sean administrados mediante un teclado, un vídeo o un conmutador de ratón (KVM).</span><span class="sxs-lookup"><span data-stu-id="97d63-122">Ensure that the keyboard, video, or mouse are directly connected and not managed through a keyboard, video, or mouse (KVM) switch.</span></span> <span data-ttu-id="97d63-123">Un conmutador KVM puede interferir con la capacidad del equipo de detectar la presencia física del hardware.</span><span class="sxs-lookup"><span data-stu-id="97d63-123">A KVM switch can interfere with the ability of the computer to detect the physical presence of hardware.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="97d63-124">Si usas un proxy, debe estar visible en el contexto del sistema.</span><span class="sxs-lookup"><span data-stu-id="97d63-124">If you use a proxy, it must be visible in the system context.</span></span> <span data-ttu-id="97d63-125">MBAM se ejecuta en el contexto del sistema, no en el contexto del usuario.</span><span class="sxs-lookup"><span data-stu-id="97d63-125">MBAM runs under the system context, not the user context.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>



**<span data-ttu-id="97d63-126">Importante</span><span class="sxs-lookup"><span data-stu-id="97d63-126">Important</span></span>**  
<span data-ttu-id="97d63-127">Si se usó BitLocker sin MBAM, MBAM se puede instalar y usar la información del TPM existente.</span><span class="sxs-lookup"><span data-stu-id="97d63-127">If BitLocker was used without MBAM, MBAM can be installed and utilize the existing TPM information.</span></span>




## <span data-ttu-id="97d63-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97d63-128">Related topics</span></span>


[<span data-ttu-id="97d63-129">Configuraciones admitidas de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="97d63-129">MBAM 2.5 Supported Configurations</span></span>](mbam-25-supported-configurations.md)

[<span data-ttu-id="97d63-130">Planificación de implementación de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="97d63-130">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)


## <span data-ttu-id="97d63-131">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="97d63-131">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="97d63-132">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="97d63-132">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="97d63-133">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="97d63-133">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>






