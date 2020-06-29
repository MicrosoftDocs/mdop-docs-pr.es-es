---
title: Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control
description: Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control
author: dansimp
ms.assetid: e2ff153e-5770-4a12-b79d-cda998b8a8ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a42901ac9d8a1a3527712f4cf342b5c0ca9ffdfd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825110"
---
# <span data-ttu-id="c6eb5-103">Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control</span><span class="sxs-lookup"><span data-stu-id="c6eb5-103">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="c6eb5-104">Una aplicación del panel de control administración y supervisión de Microsoft BitLocker (MBAM), que se denomina opciones de cifrado de BitLocker, estará disponible en **sistema y seguridad** cuando esté instalado el cliente de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-104">A Microsoft BitLocker Administration and Monitoring (MBAM) control panel application, called BitLocker Encryption Options, will be available under **System and Security** when the Microsoft BitLocker Administration and Monitoring Client is installed.</span></span> <span data-ttu-id="c6eb5-105">Este panel de control personalizado de MBAM es un panel de control adicional.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-105">This custom MBAM control panel is an additional control panel.</span></span> <span data-ttu-id="c6eb5-106">No reemplaza el panel de control predeterminado de BitLocker de Windows.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-106">It does not replace the default Windows BitLocker control panel.</span></span> <span data-ttu-id="c6eb5-107">El panel de control de MBAM se puede usar para desbloquear unidades cifradas y extraíbles, y también para administrar su PIN o contraseña.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-107">The MBAM control panel can be used to unlock encrypted fixed and removable drives, and also manage your PIN or password.</span></span> <span data-ttu-id="c6eb5-108">Para obtener más información sobre cómo habilitar el panel de control de MBAM, consulta [cómo ocultar el cifrado de BitLocker predeterminado en el panel de control de Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).</span><span class="sxs-lookup"><span data-stu-id="c6eb5-108">For more information about enabling the MBAM control panel, see [How to Hide Default BitLocker Encryption in the Windows Control Panel](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel-mbam-2.md).</span></span>

**<span data-ttu-id="c6eb5-109">Para usar el panel de control del cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="c6eb5-109">To use the MBAM Client Control Panel</span></span>**

1.  <span data-ttu-id="c6eb5-110">Para abrir las opciones de cifrado de BitLocker, haga clic en **Inicio** y seleccione **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-110">To open BitLocker Encryption Options, click **Start** and then select **Control Panel**.</span></span> <span data-ttu-id="c6eb5-111">Cuando se abra el **Panel de control** , seleccione **sistema y seguridad**.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-111">When **Control Panel** opens, select **System and Security**.</span></span>

2.  <span data-ttu-id="c6eb5-112">Haga doble clic en **Opciones de cifrado de BitLocker** para abrir el panel de control MBAM personalizado.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-112">Double-click **BitLocker Encryption Options** to open the customized MBAM control panel.</span></span> <span data-ttu-id="c6eb5-113">Verá una lista de todas las unidades de disco duro del equipo y su estado de cifrado, además de una opción para administrar su PIN o contraseñas.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-113">You will see a list of all the hard disk drives on the computer and their encryption status, in addition to an option to manage your PIN or passwords.</span></span>

    <span data-ttu-id="c6eb5-114">La lista de unidades de disco duro se puede usar para comprobar el estado del cifrado, desbloquear una unidad o solicitar una exención para la protección de BitLocker si se han implementado las directivas de exención de usuario y equipo.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-114">The list of hard disk drives on the computer can be used to verify encryption status, unlock a drive, or request an exemption for BitLocker protection if the User and Computer Exemption policies have been deployed.</span></span>

    <span data-ttu-id="c6eb5-115">El panel de control de las opciones de cifrado de BitLocker también permite que los usuarios que no sean administradores administren sus PIN o contraseñas.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-115">The BitLocker Encryption Options control panel also allows for non-administrator users to manage their PIN or passwords.</span></span> <span data-ttu-id="c6eb5-116">Al seleccionar **administrar PIN**, a los usuarios se les pide que introduzcan un PIN actual y un nuevo PIN (además de confirmar el nuevo PIN).</span><span class="sxs-lookup"><span data-stu-id="c6eb5-116">By selecting **Manage PIN**, users are prompted to enter both a current PIN and a new PIN (in addition to confirming the new PIN).</span></span> <span data-ttu-id="c6eb5-117">Al seleccionar **Actualizar PIN** se restablecerá el PIN al nuevo que han seleccionado los usuarios.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-117">Selecting **Update PIN** will reset the PIN to the new one that the users selected.</span></span>

    <span data-ttu-id="c6eb5-118">Para administrar la contraseña, seleccione **desbloquear unidad** e introduzca la contraseña actual.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-118">To manage your password, select **Unlock drive** and enter your current password.</span></span> <span data-ttu-id="c6eb5-119">Tan pronto como se desbloquee la unidad, seleccione **Restablecer contraseña** para cambiar la contraseña actual.</span><span class="sxs-lookup"><span data-stu-id="c6eb5-119">As soon as the drive is unlocked, select **Reset Password** to change your current password.</span></span>

## <span data-ttu-id="c6eb5-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c6eb5-120">Related topics</span></span>


[<span data-ttu-id="c6eb5-121">Administración de funciones de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="c6eb5-121">Administering MBAM 2.0 Features</span></span>](administering-mbam-20-features-mbam-2.md)

 

 





