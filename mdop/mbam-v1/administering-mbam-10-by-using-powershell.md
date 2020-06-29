---
title: Administración de MBAM 1.0 mediante el uso de PowerShell
description: Administración de MBAM 1.0 mediante el uso de PowerShell
author: dansimp
ms.assetid: 3bf2eca5-4ab7-4e84-9e80-c0c7d709647b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3547bee9b2efc58252bb6f0a1cb0aa4c484e4e80
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825140"
---
# <span data-ttu-id="f4dbc-103">Administración de MBAM 1.0 mediante el uso de PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4dbc-103">Administering MBAM 1.0 by Using PowerShell</span></span>


<span data-ttu-id="f4dbc-104">Administración y supervisión de Microsoft BitLocker (MBAM) proporciona el siguiente conjunto de cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4dbc-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="f4dbc-105">Los administradores pueden usar estos cmdlets de PowerShell para realizar varias tareas de servidor MBAM desde el símbolo del sistema en lugar de desde el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4dbc-105">Administrators can use these PowerShell cmdlets to perform various MBAM server tasks from the command prompt rather than from the MBAM administration website.</span></span>

## <span data-ttu-id="f4dbc-106">Cómo administrar MBAM mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="f4dbc-106">How to administer MBAM by using PowerShell</span></span>


<span data-ttu-id="f4dbc-107">Use los cmdlets de PowerShell que se describen aquí para administrar MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4dbc-107">Use the PowerShell cmdlets described here to administer MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f4dbc-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="f4dbc-108">Name</span></span></th>
<th align="left"><span data-ttu-id="f4dbc-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4dbc-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4dbc-110">Add-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="f4dbc-110">Add-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4dbc-111">Agrega un nuevo modelo de hardware al inventario de hardware de MBAM.</span><span class="sxs-lookup"><span data-stu-id="f4dbc-111">Adds a new hardware model to the MBAM hardware inventory.</span></span> <span data-ttu-id="f4dbc-112">Este cmdlet también puede especificar si el hardware es compatible o no compatible con el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f4dbc-112">This cmdlet can also specify whether the hardware is supported or unsupported for BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4dbc-113">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="f4dbc-113">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4dbc-114">Solicita una clave de recuperación de MBAM que permitirá a un usuario desbloquear un equipo o una unidad cifrada.</span><span class="sxs-lookup"><span data-stu-id="f4dbc-114">Requests an MBAM recovery key that will enable a user to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4dbc-115">Get-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="f4dbc-115">Get-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4dbc-116">Obtiene un inventario de hardware maestro que contiene datos que indican si los modelos de hardware son compatibles o incompatibles con el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f4dbc-116">Gets a master hardware inventory that contains data that indicates whether hardware models are compatible or incompatible with BitLocker drive encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4dbc-117">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="f4dbc-117">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4dbc-118">Proporciona una contraseña de propietario de TPM para que un usuario pueda administrar su acceso de TPM (módulo de plataforma segura).</span><span class="sxs-lookup"><span data-stu-id="f4dbc-118">Provides a TPM owner password for a user to manage their TPM (Trusted Platform Module) access.</span></span> <span data-ttu-id="f4dbc-119">Ayuda a los usuarios cuando el TPM ha bloqueado y ya no acepta su PIN.</span><span class="sxs-lookup"><span data-stu-id="f4dbc-119">Helps users when TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4dbc-120">Install-Mbam</span><span class="sxs-lookup"><span data-stu-id="f4dbc-120">Install-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4dbc-121">Instala características de MBAM que proporcionan directivas de grupo avanzadas, cifrado, recuperación de claves y herramientas de creación de informes de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="f4dbc-121">Installs MBAM features that provide advanced group policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4dbc-122">Remove-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="f4dbc-122">Remove-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4dbc-123">Quita los modelos de hardware del inventario de hardware.</span><span class="sxs-lookup"><span data-stu-id="f4dbc-123">Removes the hardware models from the hardware inventory.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f4dbc-124">Set-MbamHardwareType</span><span class="sxs-lookup"><span data-stu-id="f4dbc-124">Set-MbamHardwareType</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4dbc-125">Permite la administración de un inventario de hardware maestro para designar si los modelos de hardware son compatibles o incompatibles con el cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f4dbc-125">Allows management of a master hardware inventory to designate whether or not hardware models are capable or incapable to perform BitLocker encryption.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="f4dbc-126">Desinstalar-Mbam</span><span class="sxs-lookup"><span data-stu-id="f4dbc-126">Uninstall-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="f4dbc-127">Elimina las características de MBAM instaladas anteriormente que proporcionan Directivas avanzadas, cifrado, recuperación de claves y herramientas de creación de informes de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="f4dbc-127">Removes previously installed MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="f4dbc-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4dbc-128">Related topics</span></span>


[<span data-ttu-id="f4dbc-129">Operaciones para MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="f4dbc-129">Operations for MBAM 1.0</span></span>](operations-for-mbam-10.md)

 

 





