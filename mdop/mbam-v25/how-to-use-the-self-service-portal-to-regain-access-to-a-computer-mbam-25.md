---
title: Cómo usar el portal de autoservicio para recuperar el acceso a un equipo
description: Cómo usar el portal de autoservicio para recuperar el acceso a un equipo
author: dansimp
ms.assetid: 3c24b13a-d1b1-4763-8ac0-0b2db46267e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cde9c71a957a5270d69aa8388455895f1cb2432b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826701"
---
# <span data-ttu-id="fd18a-103">Cómo usar el portal de autoservicio para recuperar el acceso a un equipo</span><span class="sxs-lookup"><span data-stu-id="fd18a-103">How to Use the Self-Service Portal to Regain Access to a Computer</span></span>


<span data-ttu-id="fd18a-104">El portal de autoservicio es un sitio web que los administradores de TI pueden configurar como parte de su implementación de administración y supervisión de Microsoft BitLocker (MBAM) 2,5.</span><span class="sxs-lookup"><span data-stu-id="fd18a-104">The Self-Service Portal is a website that IT administrators configure as part of their Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 deployment.</span></span> <span data-ttu-id="fd18a-105">El sitio web permite que los usuarios finales vuelvan a obtener acceso de forma independiente a sus equipos si se bloquean en Windows.</span><span class="sxs-lookup"><span data-stu-id="fd18a-105">The website enables end users to independently regain access to their computers if they get locked out of Windows.</span></span> <span data-ttu-id="fd18a-106">El portal de autoservicio no requiere asistencia del personal del servicio de asistencia.</span><span class="sxs-lookup"><span data-stu-id="fd18a-106">The Self-Service Portal requires no assistance from Help Desk staff.</span></span>

<span data-ttu-id="fd18a-107">Las siguientes instrucciones están escritas a partir de la perspectiva de los usuarios finales, pero la información puede resultar útil para que los administradores de ti la entiendan.</span><span class="sxs-lookup"><span data-stu-id="fd18a-107">The following instructions are written from the perspective of end users, but the information may be useful for IT administrators to understand.</span></span>

<span data-ttu-id="fd18a-108">**Importante**  Un usuario final debe haber iniciado sesión físicamente en el equipo (no de forma remota) al menos una vez como mínimo para poder recuperar su clave con el portal de autoservicio.</span><span class="sxs-lookup"><span data-stu-id="fd18a-108">**Important** An end user must have physically logged on to the computer (not remotely) at least one time successfully to be able to recover their key using the Self-Service Portal.</span></span> <span data-ttu-id="fd18a-109">De lo contrario, deben usar el portal de asistencia para la recuperación de claves.</span><span class="sxs-lookup"><span data-stu-id="fd18a-109">Otherwise, they must use the Helpdesk Portal for key recovery.</span></span>

 

<span data-ttu-id="fd18a-110">Los usuarios finales pueden experimentar bloqueos si:</span><span class="sxs-lookup"><span data-stu-id="fd18a-110">End users may experience lockouts if they:</span></span>

-   <span data-ttu-id="fd18a-111">Olvidar su contraseña o PIN</span><span class="sxs-lookup"><span data-stu-id="fd18a-111">Forget their password or PIN</span></span>

-   <span data-ttu-id="fd18a-112">Cambiar los archivos del sistema operativo, el BIOS o el módulo de plataforma segura (TPM)</span><span class="sxs-lookup"><span data-stu-id="fd18a-112">Change operating system files, the BIOS, or the Trusted Platform Module (TPM)</span></span>

<span data-ttu-id="fd18a-113">**Nota:**  Si el administrador de ti ha configurado el tiempo de espera de un estado de sesión de IIS, se muestra un mensaje en el portal de autoservicio 60 segundos antes del tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="fd18a-113">**Note** If the IT administrator configured an IIS Session State time-out, a message is displayed in the Self-Service Portal 60 seconds prior to the time-out.</span></span>

 

**<span data-ttu-id="fd18a-114">Para usar el portal de autoservicio para recuperar el acceso a un equipo</span><span class="sxs-lookup"><span data-stu-id="fd18a-114">To use the Self-Service Portal to regain access to a computer</span></span>**

1.  <span data-ttu-id="fd18a-115">En el **campo ID de identificación** , escriba un mínimo de ocho dígitos de la clave de bitlocker de 32 dígitos que se muestra en la pantalla de recuperación de BitLocker de su equipo.</span><span class="sxs-lookup"><span data-stu-id="fd18a-115">In the **Recovery KeyId** field, enter a minimum of eight of the 32-digit BitLocker Key ID that is displayed on the BitLocker recovery screen of your computer.</span></span> <span data-ttu-id="fd18a-116">Si los primeros ocho dígitos coinciden con varias claves, se muestra un mensaje que requiere que escriba todos los dígitos de 32 del identificador de la clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="fd18a-116">If the first eight digits match multiple keys, a message displays that requires you to enter all 32 digits of the recovery key ID.</span></span>

2.  <span data-ttu-id="fd18a-117">En el campo **Reason** , seleccione el motivo de la solicitud de la clave de recuperación.</span><span class="sxs-lookup"><span data-stu-id="fd18a-117">In the **Reason** field, select a reason for your request for the recovery key.</span></span>

3.  <span data-ttu-id="fd18a-118">Haga clic en **obtener tecla**.</span><span class="sxs-lookup"><span data-stu-id="fd18a-118">Click **Get Key**.</span></span> <span data-ttu-id="fd18a-119">La clave de recuperación de BitLocker se muestra en el campo **clave de recuperación de BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="fd18a-119">Your BitLocker recovery key is displayed in the **Your BitLocker Recovery Key** field.</span></span>

4.  <span data-ttu-id="fd18a-120">Escribe el código de 48 dígitos en la pantalla de recuperación de BitLocker de tu equipo para recuperar el acceso al equipo.</span><span class="sxs-lookup"><span data-stu-id="fd18a-120">Enter the 48-digit code into the BitLocker recovery screen on your computer to regain access to the computer.</span></span>



## <span data-ttu-id="fd18a-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd18a-121">Related topics</span></span>


[<span data-ttu-id="fd18a-122">Realización de la administración de BitLocker con MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="fd18a-122">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="fd18a-123">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="fd18a-123">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="fd18a-124">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="fd18a-124">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="fd18a-125">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="fd18a-125">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





