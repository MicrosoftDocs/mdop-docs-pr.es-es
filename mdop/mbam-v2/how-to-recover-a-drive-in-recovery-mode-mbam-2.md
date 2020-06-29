---
title: Cómo recuperar una unidad en modo de recuperación
description: Cómo recuperar una unidad en modo de recuperación
author: dansimp
ms.assetid: 8b792bc8-b671-4345-9d37-0208db3e5b03
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d5ce509599d0eb800a71360e3be9d0fa3b33f4f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825060"
---
# <span data-ttu-id="9685b-103">Cómo recuperar una unidad en modo de recuperación</span><span class="sxs-lookup"><span data-stu-id="9685b-103">How to Recover a Drive in Recovery Mode</span></span>


<span data-ttu-id="9685b-104">Las características de recuperación de unidades cifradas de administración y supervisión de BitLocker de Microsoft (MBAM) garantizan la captura y el almacenamiento de los datos y la disponibilidad de las herramientas necesarias para acceder a un volumen protegido con BitLocker cuando BitLocker pasa al modo de recuperación.</span><span class="sxs-lookup"><span data-stu-id="9685b-104">The encrypted drive recovery features of Microsoft BitLocker Administration and Monitoring (MBAM) ensure the capture and storage of data and availability of tools required to access a BitLocker-protected volume when BitLocker goes into recovery mode.</span></span> <span data-ttu-id="9685b-105">Un volumen protegido por BitLocker pasa al modo de recuperación cuando se pierde o se olvida una contraseña o un PIN, o cuando el chip de la plataforma de módulo de confianza (TPM) detecta cambios en el BIOS o los archivos de inicio de un equipo.</span><span class="sxs-lookup"><span data-stu-id="9685b-105">A BitLocker-protected volume goes into recovery mode when a PIN or password is lost or forgotten, or when the Trusted Module Platform (TPM) chip detects changes to the BIOS or startup files of a computer.</span></span>

<span data-ttu-id="9685b-106">Use este procedimiento para acceder al sistema de datos de recuperación de claves centralizado, que puede proporcionar una contraseña de recuperación si se proporciona un identificador de contraseña de recuperación y un identificador de usuario asociado.</span><span class="sxs-lookup"><span data-stu-id="9685b-106">Use this procedure to access the centralized key recovery data system, which can provide a recovery password if a recovery password ID and associated user identifier are supplied.</span></span>

**<span data-ttu-id="9685b-107">Importante</span><span class="sxs-lookup"><span data-stu-id="9685b-107">Important</span></span>**  
<span data-ttu-id="9685b-108">Administración y supervisión de Microsoft BitLocker usa claves de recuperación de un solo uso que vencen al usarlas.</span><span class="sxs-lookup"><span data-stu-id="9685b-108">Microsoft BitLocker Administration and Monitoring uses single-use recovery keys that expire upon use.</span></span> <span data-ttu-id="9685b-109">El único uso de una contraseña de recuperación se aplica automáticamente a las unidades de sistema operativo y las unidades fijas.</span><span class="sxs-lookup"><span data-stu-id="9685b-109">The single use of a recovery password is automatically applied to operating system drives and fixed drives.</span></span> <span data-ttu-id="9685b-110">En las unidades extraíbles, se aplica cuando se quita la unidad y, a continuación, se vuelve a insertar y a desbloquear en un equipo que tiene activada la configuración de directiva de grupo para administrar unidades extraíbles.</span><span class="sxs-lookup"><span data-stu-id="9685b-110">On removable drives, it is applied when the drive is removed and then re-inserted and unlocked on a computer that has Group Policy settings activated to manage removable drives.</span></span>



**<span data-ttu-id="9685b-111">Para recuperar una unidad en modo de recuperación</span><span class="sxs-lookup"><span data-stu-id="9685b-111">To recover a drive in recovery mode</span></span>**

1.  <span data-ttu-id="9685b-112">Abra un explorador Web y vaya al sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="9685b-112">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="9685b-113">En el panel de navegación, haga clic en **recuperación de unidades**.</span><span class="sxs-lookup"><span data-stu-id="9685b-113">In the navigation pane, click **Drive Recovery**.</span></span> <span data-ttu-id="9685b-114">Se abrirá la página web "recuperar acceso a una unidad cifrada".</span><span class="sxs-lookup"><span data-stu-id="9685b-114">The “Recover access to an encrypted drive” webpage opens.</span></span>

3.  <span data-ttu-id="9685b-115">Escriba el dominio de inicio de sesión de Windows y el nombre de usuario del usuario para ver la información de recuperación y los primeros ocho dígitos de la identificación de la clave de recuperación para recibir una lista de las posibles claves de recuperación coincidentes o la identificación de la clave de recuperación completa para recibir la clave de recuperación exacta.</span><span class="sxs-lookup"><span data-stu-id="9685b-115">Enter the Windows Logon domain and user name of the user to view recovery information and the first eight digits of the recovery key ID to receive a list of possible matching recovery keys or the entire recovery key ID to receive the exact recovery key.</span></span>

4.  <span data-ttu-id="9685b-116">Seleccione una de las opciones predefinidas de la lista **motivo de desbloqueo de unidades** y, a continuación, haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="9685b-116">Select one of the predefined options from the **Reason for Drive Unlock** list, and then click **Submit**.</span></span>

    **<span data-ttu-id="9685b-117">Nota</span><span class="sxs-lookup"><span data-stu-id="9685b-117">Note</span></span>**  
    <span data-ttu-id="9685b-118">Si es un usuario avanzado de MBAM Helpdesk, no es necesario que las entradas del dominio del usuario y del identificador de usuario.</span><span class="sxs-lookup"><span data-stu-id="9685b-118">If you are an MBAM Advanced Helpdesk user, the user domain and user ID entries are not required.</span></span>



~~~
MBAM returns the following:

-   An error message if no matching recovery password is found

-   Multiple possible matches if the user has multiple matching recovery passwords

-   The recovery password and recovery package for the submitted user

    **Note**  
    If you are recovering a damaged drive, the recovery package option provides BitLocker with critical information that it needs to recover the drive.



After the recovery password and recovery package are retrieved, the recovery password is displayed.
~~~

5. <span data-ttu-id="9685b-119">Para copiar la contraseña, haga clic en **copiar clave**y, a continuación, pegue la contraseña de recuperación en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="9685b-119">To copy the password, click **Copy Key**, and then paste the recovery password into an email message.</span></span> <span data-ttu-id="9685b-120">También puede hacer clic en **Guardar** para guardar la contraseña de recuperación en un archivo.</span><span class="sxs-lookup"><span data-stu-id="9685b-120">Alternatively, click **Save** to save the recovery password to a file.</span></span>

   <span data-ttu-id="9685b-121">Cuando el usuario escribe la contraseña de recuperación en el sistema o usa el paquete de recuperación, la unidad se desbloquea.</span><span class="sxs-lookup"><span data-stu-id="9685b-121">When the user types the recovery password into the system or uses the recovery package, the drive is unlocked.</span></span>

## <span data-ttu-id="9685b-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9685b-122">Related topics</span></span>


[<span data-ttu-id="9685b-123">Realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="9685b-123">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)









