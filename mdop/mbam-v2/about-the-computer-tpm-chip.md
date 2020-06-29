---
title: Información sobre el Chip TPM del equipo
description: Información sobre el Chip TPM del equipo
author: dansimp
ms.assetid: 6f1cf18c-277a-4932-886d-14202ca8d175
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f6df54dc8085c398bacc508fdbbb79a30b0e4204
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823531"
---
# <span data-ttu-id="83463-103">Información sobre el Chip TPM del equipo</span><span class="sxs-lookup"><span data-stu-id="83463-103">About the Computer TPM Chip</span></span>


<span data-ttu-id="83463-104">BitLocker proporciona protección adicional cuando se usa con un chip módulo de plataforma segura (TPM).</span><span class="sxs-lookup"><span data-stu-id="83463-104">BitLocker provides additional protection when it is used with a Trusted Platform Module (TPM) chip.</span></span> <span data-ttu-id="83463-105">El chip de TPM es un componente de hardware que los fabricantes del equipo instalan en muchos equipos nuevos.</span><span class="sxs-lookup"><span data-stu-id="83463-105">The TPM chip is a hardware component that is installed in many newer computers by the computer manufacturers.</span></span> <span data-ttu-id="83463-106">Administración y supervisión de Microsoft BitLocker (MBAM) usa BitLocker, además del chip de TPM, para proporcionar protección adicional de los datos y asegurarse de que su equipo no ha sido manipulado.</span><span class="sxs-lookup"><span data-stu-id="83463-106">Microsoft BitLocker Administration and Monitoring (MBAM) uses BitLocker, in addition to the TPM chip, to help provide additional protection of your data and to make sure that your computer has not been tampered with.</span></span>

## <span data-ttu-id="83463-107">Cómo configurar su TPM</span><span class="sxs-lookup"><span data-stu-id="83463-107">How to Set Up Your TPM</span></span>


<span data-ttu-id="83463-108">Al iniciar el Asistente para el cifrado de unidad BitLocker en el equipo, BitLocker busca un chip de TPM si su organización ha configurado BitLocker para usar un chip de TPM.</span><span class="sxs-lookup"><span data-stu-id="83463-108">When you start the BitLocker Drive Encryption wizard on your computer, BitLocker checks for a TPM chip if your organization has configured BitLocker to use a TPM chip.</span></span> <span data-ttu-id="83463-109">Si BitLocker encuentra un chip TPM compatible, es posible que se le pida que reinicie el equipo para habilitar el chip TPM para usarlo.</span><span class="sxs-lookup"><span data-stu-id="83463-109">If BitLocker finds a compatible TPM chip, you may be prompted to restart your computer to enable the TPM chip for use.</span></span> <span data-ttu-id="83463-110">Tan pronto como se haya reiniciado el equipo, siga las instrucciones para configurar el chip TPM en el BIOS (el BIOS es una capa anterior a Windows del software de su equipo).</span><span class="sxs-lookup"><span data-stu-id="83463-110">As soon as your computer has restarted, follow the instructions to configure the TPM chip in the BIOS (the BIOS is a pre-Windows layer of your computer software).</span></span>

<span data-ttu-id="83463-111">Después de configurar BitLocker, puede obtener acceso a información adicional sobre el chip de TPM si abre la herramienta opciones de cifrado de BitLocker en el panel de control de Windows y, a continuación, selecciona **Administración de TPM**.</span><span class="sxs-lookup"><span data-stu-id="83463-111">After BitLocker is configured, you can access additional information about the TPM chip by opening the BitLocker Encryption Options tool in the Windows Control Panel, and then selecting **TPM Administration**.</span></span>

<span data-ttu-id="83463-112">**Nota:**  Para tener acceso a esta herramienta, debe tener credenciales administrativas en el equipo.</span><span class="sxs-lookup"><span data-stu-id="83463-112">**Note** You must have administrative credentials on your computer to access this tool.</span></span>

 

<span data-ttu-id="83463-113">En un error de TPM, un cambio en el BIOS o ciertas actualizaciones de Windows, BitLocker bloqueará el equipo y le será necesario que se comunique con el servicio de asistencia para desbloquearlo.</span><span class="sxs-lookup"><span data-stu-id="83463-113">In a TPM failure, a change in the BIOS, or certain Windows Updates, BitLocker will lock your computer and require you to contact your Help Desk to unlock it.</span></span> <span data-ttu-id="83463-114">Debe proporcionar el nombre del equipo, así como el dominio del equipo.</span><span class="sxs-lookup"><span data-stu-id="83463-114">You have to provide the name of your computer as well as your computer’s domain.</span></span> <span data-ttu-id="83463-115">El servicio de asistencia puede proporcionarle un archivo de contraseñas que puede usar para desbloquear el equipo.</span><span class="sxs-lookup"><span data-stu-id="83463-115">Help Desk can give you a password file that can be used to unlock your computer.</span></span>

## <span data-ttu-id="83463-116">Solución de problemas de TPM</span><span class="sxs-lookup"><span data-stu-id="83463-116">Troubleshooting TPM Issues</span></span>


<span data-ttu-id="83463-117">Si se produce un error de TPM, el cambio en el BIOS o ciertas actualizaciones de Windows, BitLocker bloqueará el equipo y tendrá que ponerse en contacto con el Departamento de soporte técnico para desbloquearlo.</span><span class="sxs-lookup"><span data-stu-id="83463-117">If a TPM failure, change in the BIOS, or certain Windows Updates occur, BitLocker will lock your computer and require you to contact your Help Desk to unlock it.</span></span> <span data-ttu-id="83463-118">Debe proporcionar el nombre del equipo, así como el dominio del equipo.</span><span class="sxs-lookup"><span data-stu-id="83463-118">You have to provide the name of your computer as well as your computer’s domain.</span></span> <span data-ttu-id="83463-119">El servicio de asistencia puede proporcionarle un archivo de contraseñas que puede usar para desbloquear el equipo.</span><span class="sxs-lookup"><span data-stu-id="83463-119">The Help Desk can give you a password file that you can use to unlock your computer.</span></span>

## <span data-ttu-id="83463-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="83463-120">Related topics</span></span>


[<span data-ttu-id="83463-121">Ayuda a los usuarios finales para administrar BitLocker</span><span class="sxs-lookup"><span data-stu-id="83463-121">Helping End Users Manage BitLocker</span></span>](helping-end-users-manage-bitlocker.md)

[<span data-ttu-id="83463-122">Uso del PIN o contraseña</span><span class="sxs-lookup"><span data-stu-id="83463-122">Using Your PIN or Password</span></span>](using-your-pin-or-password.md)

 

 





