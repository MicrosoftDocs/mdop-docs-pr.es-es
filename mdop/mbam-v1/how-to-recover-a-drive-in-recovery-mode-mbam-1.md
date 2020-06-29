---
title: Cómo recuperar una unidad en modo de recuperación
description: Cómo recuperar una unidad en modo de recuperación
author: dansimp
ms.assetid: 09d27e4b-57fa-47c7-a004-8b876a49f27e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c1151ffe7453eb8d07d2aa6dcb4c41f6b3efe6de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812951"
---
# <span data-ttu-id="2a417-103">Cómo recuperar una unidad en modo de recuperación</span><span class="sxs-lookup"><span data-stu-id="2a417-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="2a417-104">Administración y supervisión de Microsoft BitLocker (MBAM) incluye características de recuperación de unidades cifradas.</span><span class="sxs-lookup"><span data-stu-id="2a417-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes Encrypted Drive Recovery features.</span></span> <span data-ttu-id="2a417-105">Estas características garantizan la captura y el almacenamiento de los datos y la disponibilidad de las herramientas necesarias para acceder a un volumen protegido con BitLocker cuando BitLocker coloca ese volumen en modo de recuperación.</span><span class="sxs-lookup"><span data-stu-id="2a417-105">These features ensure the capture and storage of data and availability of tools that are required to access a BitLocker-protected volume when BitLocker puts that volume into recovery mode.</span></span> <span data-ttu-id="2a417-106">Un volumen protegido por BitLocker pasa al modo de recuperación cuando se pierde o se olvida una contraseña o un PIN, o cuando el chip de la plataforma de módulo de confianza (TPM) detecta un cambio en el BIOS o los archivos de inicio del equipo.</span><span class="sxs-lookup"><span data-stu-id="2a417-106">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects a change to the computer's BIOS or startup files.</span></span>

<span data-ttu-id="2a417-107">Use este procedimiento para acceder al sistema centralizado de datos de recuperación de claves que puede proporcionar una contraseña de recuperación cuando se proporciona un identificador de contraseña de recuperación y un identificador de usuario asociado.</span><span class="sxs-lookup"><span data-stu-id="2a417-107">Use this procedure to access the centralized Key Recovery data system that can provide a recovery password when a recovery password ID and associated user identifier are supplied.</span></span>

<span data-ttu-id="2a417-108">**Importante**  MBAM genera claves de recuperación de un solo uso.</span><span class="sxs-lookup"><span data-stu-id="2a417-108">**Important** MBAM generates single-use recovery keys.</span></span> <span data-ttu-id="2a417-109">Bajo esta limitación, una clave de recuperación solo se puede usar una vez y, después, ya no es válida.</span><span class="sxs-lookup"><span data-stu-id="2a417-109">Under this limitation, a recovery key can be used only once and then it is no longer valid.</span></span> <span data-ttu-id="2a417-110">El único uso de una contraseña de recuperación se aplica automáticamente a las unidades de sistema operativo y las unidades fijas.</span><span class="sxs-lookup"><span data-stu-id="2a417-110">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="2a417-111">En las unidades extraíbles, el uso único se aplica cuando se quita la unidad y, a continuación, se vuelve a insertar y a desbloquear en un equipo que tenga activada la configuración de directiva de grupo para administrar unidades extraíbles.</span><span class="sxs-lookup"><span data-stu-id="2a417-111">On removable drives, the single use is applied when the drive is removed and then re-inserted and unlocked on a computer that has the group policy settings activated to manage removable drives.</span></span>

 

**<span data-ttu-id="2a417-112">Para recuperar una unidad en modo de recuperación</span><span class="sxs-lookup"><span data-stu-id="2a417-112">To recover a drive in Recovery Mode</span></span>**

1.  <span data-ttu-id="2a417-113">Abra el sitio web de MBAM.</span><span class="sxs-lookup"><span data-stu-id="2a417-113">Open the MBAM website.</span></span>

2.  <span data-ttu-id="2a417-114">En el panel de navegación, haga clic en **recuperación de unidades**.</span><span class="sxs-lookup"><span data-stu-id="2a417-114">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="2a417-115">Se abrirá la Página Web **recuperar acceso a una unidad cifrada** .</span><span class="sxs-lookup"><span data-stu-id="2a417-115">The **Recover access to an encrypted drive** webpage opens.</span></span>

3.  <span data-ttu-id="2a417-116">Escriba el nombre de usuario y el dominio de inicio de sesión de Windows del usuario y los primeros ocho dígitos del identificador de la clave de recuperación para obtener una lista de las posibles claves de recuperación coincidentes.</span><span class="sxs-lookup"><span data-stu-id="2a417-116">Enter the user's Windows Logon domain and user name and the first eight digits of the recovery key ID, to receive a list of possible matching recovery keys.</span></span> <span data-ttu-id="2a417-117">También puede escribir la identificación de la clave de recuperación completa para recibir la clave de recuperación exacta.</span><span class="sxs-lookup"><span data-stu-id="2a417-117">Alternatively, enter the entire recovery key ID to receive the exact recovery key.</span></span> <span data-ttu-id="2a417-118">Seleccione una de las opciones predefinidas en la lista desplegable **motivo del bloqueo de la unidad** y, a continuación, haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="2a417-118">Select one of the predefined options in the **Reason for Drive Unlock** drop-down list, and then click **Submit**.</span></span>

    <span data-ttu-id="2a417-119">**Nota:**  Si es un usuario avanzado de MBAM Helpdesk, no es necesario que las entradas del dominio del usuario y del identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="2a417-119">**Note** If you are an MBAM Advanced Helpdesk User, the user domain and user ID entries are not required.</span></span>

     

4.  <span data-ttu-id="2a417-120">MBAM devuelve lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="2a417-120">MBAM returns the following:</span></span>

    1.  <span data-ttu-id="2a417-121">Mensaje de error si no se encuentra ninguna contraseña de recuperación coincidente</span><span class="sxs-lookup"><span data-stu-id="2a417-121">An error message if no matching recovery password is found</span></span>

    2.  <span data-ttu-id="2a417-122">Varias coincidencias posibles si el usuario tiene varias contraseñas de recuperación coincidentes</span><span class="sxs-lookup"><span data-stu-id="2a417-122">Multiple possible matches if the user has multiple matching recovery passwords</span></span>

    3.  <span data-ttu-id="2a417-123">La contraseña de recuperación y el paquete de recuperación para el usuario enviado</span><span class="sxs-lookup"><span data-stu-id="2a417-123">The recovery password and recovery package for the submitted user</span></span>

        <span data-ttu-id="2a417-124">**Nota:**  Si está recuperando una unidad dañada, la opción paquete de recuperación proporciona BitLocker con la información crítica necesaria para intentar la recuperación.</span><span class="sxs-lookup"><span data-stu-id="2a417-124">**Note** If you are recovering a damaged drive, the recovery package option provides BitLocker with the critical information necessary to attempt the recovery.</span></span>

         

5.  <span data-ttu-id="2a417-125">Después de recuperar la contraseña de recuperación y el paquete de recuperación, aparecerá la contraseña de recuperación.</span><span class="sxs-lookup"><span data-stu-id="2a417-125">After the recovery password and recovery package are retrieved, the recovery password is displayed.</span></span> <span data-ttu-id="2a417-126">Para copiar la contraseña, haga clic en **copiar clave**y, a continuación, pegue la contraseña de recuperación en un correo electrónico u otro archivo de texto para su almacenamiento temporal.</span><span class="sxs-lookup"><span data-stu-id="2a417-126">To copy the password, click **Copy Key**, and then paste the recovery password into an email or other text file for temporary storage.</span></span> <span data-ttu-id="2a417-127">O bien, para guardar la contraseña de recuperación en un archivo, haga clic en **Guardar**.</span><span class="sxs-lookup"><span data-stu-id="2a417-127">Or, to save the recovery password to a file, click **Save**.</span></span>

6.  <span data-ttu-id="2a417-128">Cuando el usuario escribe la contraseña de recuperación en el sistema o usa el paquete de recuperación, la unidad se desbloquea.</span><span class="sxs-lookup"><span data-stu-id="2a417-128">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="2a417-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2a417-129">Related topics</span></span>


[<span data-ttu-id="2a417-130">Realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="2a417-130">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





