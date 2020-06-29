---
title: Uso de Windows PowerShell para administrar MBAM 2.5
description: Uso de Windows PowerShell para administrar MBAM 2.5
author: dansimp
ms.assetid: 64668e76-2cba-433d-8d2d-50df0a4b2997
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 8db305bfbdf79723da2b186dd5cc00406a4089cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812735"
---
# <span data-ttu-id="27ac1-103">Uso de Windows PowerShell para administrar MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="27ac1-103">Using Windows PowerShell to Administer MBAM 2.5</span></span>


<span data-ttu-id="27ac1-104">En este tema se describen los cmdlets de Windows PowerShell para administración y supervisión de Microsoft BitLocker (MBAM) que se relacionan con la recuperación de equipos o unidades cuando los usuarios se bloquean.</span><span class="sxs-lookup"><span data-stu-id="27ac1-104">This topic describes Windows PowerShell cmdlets for Microsoft BitLocker Administration and Monitoring (MBAM) that relate to recovering computers or drives when users get locked out.</span></span>

<span data-ttu-id="27ac1-105">Para conocer los cmdlets que usa para configurar las características del servidor de MBAM, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="27ac1-105">For cmdlets that you use to configure MBAM Server features, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

## <a href="" id="cmdlets-for-recovering-computers-or-drives-that-are-managed-by-mbam-"></a><span data-ttu-id="27ac1-106">Cmdlets para recuperar equipos o unidades administrados por MBAM</span><span class="sxs-lookup"><span data-stu-id="27ac1-106">Cmdlets for recovering computers or drives that are managed by MBAM</span></span>


<span data-ttu-id="27ac1-107">Use los siguientes cmdlets de Windows PowerShell para recuperar equipos o unidades administrados por MBAM.</span><span class="sxs-lookup"><span data-stu-id="27ac1-107">Use the following Windows PowerShell cmdlets to recover computers or drives that are managed by MBAM.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27ac1-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="27ac1-108">Name</span></span></th>
<th align="left"><span data-ttu-id="27ac1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="27ac1-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="27ac1-110">Get-MbamBitLockerRecoveryKey</span><span class="sxs-lookup"><span data-stu-id="27ac1-110">Get-MbamBitLockerRecoveryKey</span></span></p></td>
<td align="left"><p><span data-ttu-id="27ac1-111">Solicita una clave de recuperación de MBAM que permite a los usuarios desbloquear un equipo o una unidad cifrada.</span><span class="sxs-lookup"><span data-stu-id="27ac1-111">Requests an MBAM recovery key that enables users to unlock a computer or encrypted drive.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="27ac1-112">Get-MbamTPMOwnerPassword</span><span class="sxs-lookup"><span data-stu-id="27ac1-112">Get-MbamTPMOwnerPassword</span></span></p></td>
<td align="left"><p><span data-ttu-id="27ac1-113">Proporciona a los usuarios una contraseña de propietario de TPM que pueden usar para desbloquear un módulo de plataforma segura (TPM) cuando el TPM ha bloqueado y ya no aceptan su PIN.</span><span class="sxs-lookup"><span data-stu-id="27ac1-113">Provides users with a TPM owner password that they can use to unlock a Trusted Platform Module (TPM) when the TPM has locked them out and will no longer accept their PIN.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------mbam-cmdlet-help"></a> <span data-ttu-id="27ac1-114">Ayuda del cmdlet MBAM</span><span class="sxs-lookup"><span data-stu-id="27ac1-114">MBAM cmdlet Help</span></span>


<span data-ttu-id="27ac1-115">La ayuda de Windows PowerShell para cmdlets de MBAM está disponible en los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="27ac1-115">Windows PowerShell Help for MBAM cmdlets is available in the following formats:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="27ac1-116">Formato de ayuda de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="27ac1-116">Windows PowerShell Help format</span></span></th>
<th align="left"><span data-ttu-id="27ac1-117">Más información</span><span class="sxs-lookup"><span data-stu-id="27ac1-117">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="27ac1-118">En un símbolo del sistema de Windows PowerShell, escriba <strong> </strong> &lt; <em> cmdlet Get-Help</em>&gt;</span><span class="sxs-lookup"><span data-stu-id="27ac1-118">At a Windows PowerShell command prompt, type <strong>Get-Help</strong> &lt;<em>cmdlet</em>&gt;</span></span></p></td>
<td align="left"><p><span data-ttu-id="27ac1-119">Para cargar los cmdlets de Windows PowerShell más recientes, siga las instrucciones de <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)"> configuración de las características de servidor de MBAM 2,5 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="27ac1-119">To upload the latest Windows PowerShell cmdlets, follow the instructions in <a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="27ac1-120">En TechNet como páginas web</span><span class="sxs-lookup"><span data-stu-id="27ac1-120">On TechNet as webpages</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="27ac1-121">En el centro de descarga como un archivo. docx de Word</span><span class="sxs-lookup"><span data-stu-id="27ac1-121">On the Download Center as a Word .docx file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="27ac1-122">En el centro de descarga como un archivo. pdf</span><span class="sxs-lookup"><span data-stu-id="27ac1-122">On the Download Center as a .pdf file</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 



## <span data-ttu-id="27ac1-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="27ac1-123">Related topics</span></span>


[<span data-ttu-id="27ac1-124">Administración de funciones de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="27ac1-124">Administering MBAM 2.5 Features</span></span>](administering-mbam-25-features.md)

[<span data-ttu-id="27ac1-125">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="27ac1-125">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

 

## <span data-ttu-id="27ac1-126">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="27ac1-126">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="27ac1-127">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="27ac1-127">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="27ac1-128">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="27ac1-128">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





