---
title: Cómo restablecer un bloqueo de TPM
description: Cómo restablecer un bloqueo de TPM
author: dansimp
ms.assetid: 20719ab2-18ae-4d3b-989a-539341909816
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6453473ec09c2033346c7e464c08dbfdfe046d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825051"
---
# <span data-ttu-id="7bffb-103">Cómo restablecer un bloqueo de TPM</span><span class="sxs-lookup"><span data-stu-id="7bffb-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="7bffb-104">La característica de recuperación de unidades cifradas de administración y supervisión de BitLocker de Microsoft (MBAM) engloba la captura y el almacenamiento de datos, así como la disponibilidad de las herramientas necesarias para administrar el módulo de plataforma segura (TPM).</span><span class="sxs-lookup"><span data-stu-id="7bffb-104">The Encrypted Drive Recovery feature of Microsoft BitLocker Administration and Monitoring (MBAM) encompasses both the capture and storage of data and the availability for tools that are needed to manage the Trusted Platform Module (TPM).</span></span> <span data-ttu-id="7bffb-105">En este tema, se explica cómo acceder al sistema de datos de recuperación de claves centralizado en el sitio web de administración y supervisión, que puede proporcionar un archivo de contraseña de propietario de TPM cuando se proporciona un identificador de equipo y el identificador de usuario asociado.</span><span class="sxs-lookup"><span data-stu-id="7bffb-105">This topic covers how to access the centralized Key Recovery data system in the Administration and Monitoring website, which can provide a TPM owner password file when a computer ID and associated user identifier are supplied.</span></span>

<span data-ttu-id="7bffb-106">Puede producirse un bloqueo de TPM si un usuario escribe un PIN incorrecto demasiadas veces.</span><span class="sxs-lookup"><span data-stu-id="7bffb-106">A TPM lockout can occur if a user enters the incorrect PIN too many times.</span></span> <span data-ttu-id="7bffb-107">El número de veces que un usuario puede escribir un PIN incorrecto antes de que los bloqueos de TPM varíen de un fabricante a otro.</span><span class="sxs-lookup"><span data-stu-id="7bffb-107">The number of times that a user can enter an incorrect PIN before the TPM locks varies from manufacturer to manufacturer.</span></span>

<span data-ttu-id="7bffb-108">Puede restablecer un bloqueo de TPM solo si MBAM es propietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="7bffb-108">You can reset a TPM lockout only if MBAM owns the TPM.</span></span>

**<span data-ttu-id="7bffb-109">Para restablecer un bloqueo de TPM</span><span class="sxs-lookup"><span data-stu-id="7bffb-109">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="7bffb-110">Abra un explorador Web y vaya al sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="7bffb-110">Open a web browser and navigate to the Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="7bffb-111">En el panel de navegación izquierdo, seleccione **administrar TPM** para abrir la página **administrar TPM** .</span><span class="sxs-lookup"><span data-stu-id="7bffb-111">In the left navigation pane, select **Manage TPM** to open the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="7bffb-112">Escriba el nombre de dominio completo del equipo y el nombre del equipo, y escriba el dominio de inicio de sesión de Windows del usuario y el nombre de usuario del usuario para recuperar el archivo de contraseña de propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="7bffb-112">Enter the fully qualified domain name for the computer and the computer name, and enter the user’s Windows logon domain and the user’s user name to retrieve the TPM owner password file.</span></span>

4.  <span data-ttu-id="7bffb-113">En la lista de **archivos de contraseña de propietario de TPM** , seleccione un motivo para la solicitud y haga clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="7bffb-113">From the **Reason for requesting TPM owner password file** list, select a reason for the request, and click **Submit**.</span></span>

    <span data-ttu-id="7bffb-114">MBAM devuelve una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="7bffb-114">MBAM returns one of the following:</span></span>

    -   <span data-ttu-id="7bffb-115">Un mensaje de error, si no se encuentra ningún archivo de contraseña de propietario de TPM coincidente</span><span class="sxs-lookup"><span data-stu-id="7bffb-115">An error message, if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="7bffb-116">El archivo de contraseña de propietario de TPM para el equipo enviado</span><span class="sxs-lookup"><span data-stu-id="7bffb-116">The TPM owner password file for the submitted computer</span></span>

    **<span data-ttu-id="7bffb-117">Nota</span><span class="sxs-lookup"><span data-stu-id="7bffb-117">Note</span></span>**  
    <span data-ttu-id="7bffb-118">Si es un usuario avanzado del servicio de asistencia, los campos dominio del usuario e identificador de usuario no son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="7bffb-118">If you are an Advanced Helpdesk user, the user domain and user ID fields are not required.</span></span>



~~~
After the TPM owner password is retrieved, the owner password is displayed.
~~~

5. <span data-ttu-id="7bffb-119">Para guardar la contraseña en un archivo. TPM, haga clic en el botón **Guardar** .</span><span class="sxs-lookup"><span data-stu-id="7bffb-119">To save the password to a .tpm file, click the **Save** button.</span></span>

   <span data-ttu-id="7bffb-120">El usuario ejecutará la consola de administración de TPM, selecciona la opción **restablecer el bloqueo de TPM** y proporciona el archivo de contraseña de propietario de TPM para restablecer el bloqueo de TPM.</span><span class="sxs-lookup"><span data-stu-id="7bffb-120">The user will run the TPM management console, select the **Reset TPM lockout** option, and provide the TPM owner password file to reset the TPM lockout.</span></span>

   **<span data-ttu-id="7bffb-121">Importante</span><span class="sxs-lookup"><span data-stu-id="7bffb-121">Important</span></span>**  
   <span data-ttu-id="7bffb-122">Los administradores del servicio de asistencia no deben conceder el valor de hash de TPM o el archivo de contraseña de propietario de TPM a los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="7bffb-122">Help Desk administrators should not give the TPM hash value or TPM owner password file to end users.</span></span> <span data-ttu-id="7bffb-123">La información del TPM no cambia, por lo que puede suponer un riesgo de seguridad si el archivo se proporciona a los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="7bffb-123">The TPM information does not change, so it could pose a security risk if the file is given to end users.</span></span>



## <span data-ttu-id="7bffb-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7bffb-124">Related topics</span></span>


[<span data-ttu-id="7bffb-125">Realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="7bffb-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam-mbam-2.md)









