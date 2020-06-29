---
title: Cómo usar el portal de autoservicio para recuperar el acceso a un equipo
description: Cómo usar el portal de autoservicio para recuperar el acceso a un equipo
author: dansimp
ms.assetid: bcf095de-0237-4bb0-b450-da8fb6d6f3d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4abcffcf35e09bd5e24f4715a38dca74518ba29e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826080"
---
# <span data-ttu-id="f744a-103">Cómo usar el portal de autoservicio para recuperar el acceso a un equipo</span><span class="sxs-lookup"><span data-stu-id="f744a-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="f744a-104">Si los usuarios finales se bloquean en Windows mediante BitLocker porque han olvidado su contraseña o su PIN, o porque han cambiado los archivos del sistema operativo o cambiado el BIOS o el módulo de plataforma segura (TPM), pueden usar el portal de autoservicio para recuperar el acceso a Windows sin tener que pedir asistencia al servicio de asistencia.</span><span class="sxs-lookup"><span data-stu-id="f744a-104">If end users get locked out of Windows by BitLocker because they forgot their password or PIN, or because they changed operating system files or changed the BIOS or the Trusted Platform Module (TPM), they can use the Self-Service Portal to regain access to Windows without having to ask their Help Desk for assistance.</span></span>

<span data-ttu-id="f744a-105">**Nota:**  Si el administrador de ti configuró el tiempo de espera de una sesión de IIS, se mostrará un mensaje de error 60 segundos antes de que se agote el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="f744a-105">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed 60 seconds prior to the time-out.</span></span>

 

<span data-ttu-id="f744a-106">**Nota:**  Estas instrucciones están escritas para la perspectiva de los usuarios finales y desde la misma.</span><span class="sxs-lookup"><span data-stu-id="f744a-106">**Note** These instructions are written for and from the perspective of end users.</span></span>

 

**<span data-ttu-id="f744a-107">Para usar el portal de autoservicio para recuperar el acceso a un equipo</span><span class="sxs-lookup"><span data-stu-id="f744a-107">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="f744a-108">En el **campo ID de identificación** , escriba un mínimo de ocho dígitos de la clave de bitlocker de 32 dígitos que se muestra en la pantalla de recuperación de BitLocker de su equipo.</span><span class="sxs-lookup"><span data-stu-id="f744a-108">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span>

    <span data-ttu-id="f744a-109">**Nota:**  Si los primeros ocho dígitos coinciden con varias claves, se muestra un mensaje que requiere que escriba todos los dígitos de 32 del identificador de la clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f744a-109">**Note** If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

     

2.  <span data-ttu-id="f744a-110">En el campo **Reason** , seleccione el motivo de la solicitud de la clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="f744a-110">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="f744a-111">Haga clic en **obtener tecla**.</span><span class="sxs-lookup"><span data-stu-id="f744a-111">Click **Get Key**.</span></span> <span data-ttu-id="f744a-112">La clave de recuperación de BitLocker se muestra en el campo "su clave de recuperación de BitLocker".</span><span class="sxs-lookup"><span data-stu-id="f744a-112">Your BitLocker recovery key is displayed in the “Your BitLocker Recovery Key” field.</span></span>

4.  <span data-ttu-id="f744a-113">Escribe el código de 48 dígitos en la pantalla de recuperación de BitLocker de tu equipo para recuperar el acceso al equipo.</span><span class="sxs-lookup"><span data-stu-id="f744a-113">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>

## <span data-ttu-id="f744a-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f744a-114">Related topics</span></span>


[<span data-ttu-id="f744a-115">Realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="f744a-115">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)

 

 





