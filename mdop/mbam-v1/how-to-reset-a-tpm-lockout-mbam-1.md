---
title: Cómo restablecer un bloqueo de TPM
description: Cómo restablecer un bloqueo de TPM
author: dansimp
ms.assetid: 91ec6666-1ae2-4e76-9459-ad65c405f639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde77a12e97d050777dac15d4106124ec111b3cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812919"
---
# <span data-ttu-id="66cc4-103">Cómo restablecer un bloqueo de TPM</span><span class="sxs-lookup"><span data-stu-id="66cc4-103">How to Reset a TPM Lockout</span></span>


<span data-ttu-id="66cc4-104">La característica de recuperación de unidades cifradas de administración y supervisión de BitLocker de Microsoft (MBAM) engloba la captura y el almacenamiento de datos, así como la disponibilidad de las herramientas necesarias para administrar el módulo de plataforma segura (TPM).</span><span class="sxs-lookup"><span data-stu-id="66cc4-104">The Encrypted Drive Recovery feature of Microsoft BitLocker Administration and Monitoring (MBAM) encompasses both the capture and storage of data and the availability for tools that are required to manage the Trusted Platform Module (TPM).</span></span> <span data-ttu-id="66cc4-105">En este tema, se explica cómo acceder al sistema centralizado de datos de recuperación de claves en el _admmon \ _tlanextref sitio web de administración.</span><span class="sxs-lookup"><span data-stu-id="66cc4-105">This topic covers how to access the centralized Key Recovery data system in the bit\_admmon\_tlanextref administration website.</span></span> <span data-ttu-id="66cc4-106">El sistema de datos de recuperación de claves puede proporcionar un archivo de contraseña de propietario de TPM cuando se proporciona la identidad del equipo y el identificador de usuario asociado.</span><span class="sxs-lookup"><span data-stu-id="66cc4-106">The Key Recovery data system can provide a TPM owner password file when the computer identity and the associated user identifier are supplied.</span></span>

<span data-ttu-id="66cc4-107">Puede producirse un bloqueo de TPM si un usuario escribe un PIN incorrecto demasiadas veces.</span><span class="sxs-lookup"><span data-stu-id="66cc4-107">A TPM lockout can occur if a user enters an incorrect PIN too many times.</span></span> <span data-ttu-id="66cc4-108">El número de veces que un usuario puede escribir un PIN incorrecto antes de que el bloqueo de TPM se base en la especificación del fabricante del equipo.</span><span class="sxs-lookup"><span data-stu-id="66cc4-108">The number of times that a user can enter an incorrect PIN before the TPM lockout is based on the computer manufacturer's specification.</span></span>

**<span data-ttu-id="66cc4-109">Para restablecer un bloqueo de TPM</span><span class="sxs-lookup"><span data-stu-id="66cc4-109">To reset a TPM lockout</span></span>**

1.  <span data-ttu-id="66cc4-110">Abra el sitio web de administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="66cc4-110">Open the MBAM administration website.</span></span>

2.  <span data-ttu-id="66cc4-111">En el panel de navegación, seleccione **administrar TPM**.</span><span class="sxs-lookup"><span data-stu-id="66cc4-111">In the navigation pane, select **Manage TPM**.</span></span> <span data-ttu-id="66cc4-112">Se abrirá la página **Manage TPM** .</span><span class="sxs-lookup"><span data-stu-id="66cc4-112">This opens the **Manage TPM** page.</span></span>

3.  <span data-ttu-id="66cc4-113">Escriba el nombre de dominio completo (FQDN) del equipo y el nombre del equipo.</span><span class="sxs-lookup"><span data-stu-id="66cc4-113">Enter the fully qualified domain name (FQDN) for the computer and the computer name.</span></span> <span data-ttu-id="66cc4-114">Escriba el dominio de inicio de sesión de Windows del usuario y el nombre de usuario del usuario.</span><span class="sxs-lookup"><span data-stu-id="66cc4-114">Enter the user’s Windows Logon domain and the user’s user name.</span></span> <span data-ttu-id="66cc4-115">Seleccione una de las opciones predefinidas en el menú desplegable motivo por el que se **solicita un archivo de contraseña de propietario de TPM** .</span><span class="sxs-lookup"><span data-stu-id="66cc4-115">Select one of the predefined options in the **Reason for requesting TPM owner password file** drop-down menu.</span></span> <span data-ttu-id="66cc4-116">Haz clic en **Enviar**.</span><span class="sxs-lookup"><span data-stu-id="66cc4-116">Click **Submit**.</span></span>

4.  <span data-ttu-id="66cc4-117">MBAM devolverá una de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="66cc4-117">MBAM will return one of the following:</span></span>

    -   <span data-ttu-id="66cc4-118">Mensaje de error si no se encuentra ningún archivo de contraseña de propietario de TPM coincidente</span><span class="sxs-lookup"><span data-stu-id="66cc4-118">An error message if no matching TPM owner password file is found</span></span>

    -   <span data-ttu-id="66cc4-119">El archivo de contraseña de propietario de TPM para el equipo enviado</span><span class="sxs-lookup"><span data-stu-id="66cc4-119">The TPM owner password file for the submitted computer</span></span>

    <span data-ttu-id="66cc4-120">**Nota:**  Si es un usuario avanzado del servicio de asistencia, los campos dominio del usuario e identificador de usuario no son obligatorios.</span><span class="sxs-lookup"><span data-stu-id="66cc4-120">**Note** If you are an Advanced Helpdesk User, the user domain and user ID fields are not required.</span></span>

     

5.  <span data-ttu-id="66cc4-121">Después de la recuperación, se muestra la contraseña de propietario.</span><span class="sxs-lookup"><span data-stu-id="66cc4-121">Upon retrieval, the owner password is displayed.</span></span> <span data-ttu-id="66cc4-122">Para guardar esta contraseña en un archivo. TPM, haga clic en el botón **Guardar** .</span><span class="sxs-lookup"><span data-stu-id="66cc4-122">To save this password to a .tpm file, click the **Save** button.</span></span>

6.  <span data-ttu-id="66cc4-123">El usuario ejecutará la consola de administración de TPM y seleccionará la opción **restablecer el bloqueo de TPM** y proporcionará el archivo de contraseña de propietario de TPM para restablecer el bloqueo de TPM.</span><span class="sxs-lookup"><span data-stu-id="66cc4-123">The user will run the TPM management console and select the **Reset TPM lockout** option and provide the TPM owner password file to reset the TPM lockout.</span></span>

## <span data-ttu-id="66cc4-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66cc4-124">Related topics</span></span>


[<span data-ttu-id="66cc4-125">Realizar la administración de BitLocker con MBAM</span><span class="sxs-lookup"><span data-stu-id="66cc4-125">Performing BitLocker Management with MBAM</span></span>](performing-bitlocker-management-with-mbam.md)

 

 





