---
title: Administración de MBAM 2.0 con PowerShell
description: Administración de MBAM 2.0 con PowerShell
author: dansimp
ms.assetid: d785a8df-0a8c-4d70-abd2-93a762b4f3de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 736943e707b5d033b8ba6c26641393f02f0cdaf8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823501"
---
# <span data-ttu-id="837a5-103">Administración de MBAM 2.0 con PowerShell</span><span class="sxs-lookup"><span data-stu-id="837a5-103">Administering MBAM 2.0 Using PowerShell</span></span>


<span data-ttu-id="837a5-104">Administración y supervisión de Microsoft BitLocker (MBAM) proporciona el siguiente conjunto de cmdlets de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="837a5-104">Microsoft BitLocker Administration and Monitoring (MBAM) provides the following listed set of Windows PowerShell cmdlets.</span></span> <span data-ttu-id="837a5-105">Los administradores pueden usar estos cmdlets de PowerShell para realizar diversas tareas de servidor de supervisión y administración de Microsoft BitLocker desde la línea de comandos en lugar de desde el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="837a5-105">Administrators can use these PowerShell cmdlets to perform various Microsoft BitLocker Administration and Monitoring server tasks from the command line rather than from the MBAM administration website.</span></span>

## <span data-ttu-id="837a5-106">Cómo administrar MBAM con PowerShell</span><span class="sxs-lookup"><span data-stu-id="837a5-106">How to Administer MBAM Using PowerShell</span></span>


<span data-ttu-id="837a5-107">Use los cmdlets de PowerShell que se describen aquí para administrar MBAM.</span><span class="sxs-lookup"><span data-stu-id="837a5-107">Use the PowerShell cmdlets described here to administer MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="837a5-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="837a5-108">Name</span></span></th>
<th align="left"><span data-ttu-id="837a5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="837a5-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="837a5-110">Install-Mbam</span><span class="sxs-lookup"><span data-stu-id="837a5-110">Install-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="837a5-111">Instala las características de MBAM que proporcionan políticas avanzadas, cifrado, recuperación de claves y reporting de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="837a5-111">Installs the MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="837a5-112">Desinstalar-Mbam</span><span class="sxs-lookup"><span data-stu-id="837a5-112">Uninstall-Mbam</span></span></p></td>
<td align="left"><p><span data-ttu-id="837a5-113">Elimina las características de MBAM que proporcionan Directivas avanzadas, cifrado, recuperación de claves y herramientas de creación de informes de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="837a5-113">Removes the MBAM features that provide advanced policy, encryption, key recovery, and compliance reporting tools.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="837a5-114">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="837a5-114">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="837a5-115">Solicita una clave de recuperación de MBAM que permitirá a los usuarios desbloquear un equipo o una unidad cifrada.</span><span class="sxs-lookup"><span data-stu-id="837a5-115">Requests an MBAM recovery key that will enable users to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="837a5-116">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="837a5-116">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="837a5-117">Proporciona a los usuarios una contraseña de propietario de TPM que pueden usar para desbloquear un módulo de plataforma segura (TPM) cuando el TPM ha bloqueado y ya no aceptan su PIN.</span><span class="sxs-lookup"><span data-stu-id="837a5-117">Provides users with a TPM owner password that they can use to unlock a Trusted Platform Module (TPM) when the TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="837a5-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="837a5-118">Related topics</span></span>


[<span data-ttu-id="837a5-119">Operaciones para MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="837a5-119">Operations for MBAM 2.0</span></span>](operations-for-mbam-20-mbam-2.md)

 

 





