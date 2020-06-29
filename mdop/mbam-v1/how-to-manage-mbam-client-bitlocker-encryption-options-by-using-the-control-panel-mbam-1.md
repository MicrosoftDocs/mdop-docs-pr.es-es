---
title: Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control
description: Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control
author: dansimp
ms.assetid: c08077e1-5529-468f-9370-c3b33fc258f3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 271147d0e5581f6ce49fe0b46aa83dae6ae4556b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812958"
---
# <span data-ttu-id="0ee6f-103">Cómo administrar opciones de cifrado de BitLocker de cliente MBAM mediante el Panel de Control</span><span class="sxs-lookup"><span data-stu-id="0ee6f-103">How to Manage MBAM Client BitLocker Encryption Options by Using the Control Panel</span></span>


<span data-ttu-id="0ee6f-104">Una aplicación de panel de control de administración y supervisión de Microsoft BitLocker (MBAM), que se denomina opciones de cifrado de BitLocker, estará disponible en **sistema y seguridad** cuando se instale el cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-104">A Microsoft BitLocker Administration and Monitoring (MBAM) control panel application, called BitLocker Encryption Options, will be available under **System and Security** when the MBAM Client is installed.</span></span> <span data-ttu-id="0ee6f-105">Este panel de control personalizado de MBAM reemplaza al panel de control predeterminado de BitLocker de Windows.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-105">This customized MBAM control panel replaces the default Windows BitLocker control panel.</span></span> <span data-ttu-id="0ee6f-106">El panel de control de MBAM te permite desbloquear unidades cifradas (fijas y extraíbles) y también te ayuda a administrar tu PIN o tu contraseña.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-106">The MBAM control panel enables you to unlock encrypted drives (fixed and removable), and also helps you manage your PIN or password.</span></span> <span data-ttu-id="0ee6f-107">Para obtener más información sobre cómo habilitar el panel de control de MBAM, consulta [cómo ocultar el cifrado de BitLocker predeterminado en el panel de control de Windows](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).</span><span class="sxs-lookup"><span data-stu-id="0ee6f-107">For more information about enabling the MBAM control panel, see [How to Hide Default BitLocker Encryption in The Windows Control Panel](how-to-hide-default-bitlocker-encryption-in-the-windows-control-panel.md).</span></span>

<span data-ttu-id="0ee6f-108">**Nota:**  Para el cliente de BitLocker, los archivos de registro operativos y de administración se encuentran en el visor de eventos, en **registros de aplicaciones y servicios**de  /  **Microsoft**  /  **Windows**  /  **BitLockerManagement**.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-108">**Note** For the BitLocker client, the Admin and Operational log files are located in Event Viewer, under **Application and Services Logs** / **Microsoft** / **Windows** / **BitLockerManagement**.</span></span>

 

**<span data-ttu-id="0ee6f-109">Para usar el panel de control del cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="0ee6f-109">To use the MBAM Client Control Panel</span></span>**

1.  <span data-ttu-id="0ee6f-110">Para abrir las opciones de cifrado de BitLocker, haga clic en **Inicio**y seleccione **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-110">To open BitLocker Encryption Options, click **Start**, and then select **Control Panel**.</span></span> <span data-ttu-id="0ee6f-111">Cuando se abra el **Panel de control** , seleccione **sistema y seguridad**.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-111">When **Control Panel** opens, select **System and Security**.</span></span>

2.  <span data-ttu-id="0ee6f-112">Haga doble clic en **Opciones de cifrado de BitLocker** para abrir el panel de control MBAM personalizado.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-112">Double-click **BitLocker Encryption Options** to open the customized MBAM control panel.</span></span> <span data-ttu-id="0ee6f-113">Verá una lista de todas las unidades de disco duro del equipo y su estado de cifrado.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-113">You will see a list of all the hard disk drives on the computer and their encryption status.</span></span> <span data-ttu-id="0ee6f-114">También verá una opción para administrar su PIN o sus contraseñas.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-114">You will also see an option to manage your PIN or passwords.</span></span>

3.  <span data-ttu-id="0ee6f-115">Use la lista de unidades de disco duro del equipo para comprobar el estado de cifrado, desbloquear una unidad o solicitar una exención para la protección de BitLocker si se han implementado las directivas de exención de usuario y equipo.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-115">Use the list of hard disk drives on the computer to verify the encryption status, unlock a drive, or request an exemption for BitLocker protection if the User and Computer Exemption policies have been deployed.</span></span>

4.  <span data-ttu-id="0ee6f-116">Los usuarios que no sean administradores pueden usar el panel de control de las opciones de cifrado de BitLocker para administrar PIN o contraseñas.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-116">Non-administrators can use the BitLocker Encryption Options control panel to manage PINs or passwords.</span></span> <span data-ttu-id="0ee6f-117">Un usuario puede seleccionar **administrar PIN** y, a continuación, escribir un PIN actual y un nuevo PIN.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-117">A user can select **Manage PIN,** and then enter both a current PIN and a new PIN.</span></span> <span data-ttu-id="0ee6f-118">Los usuarios también pueden confirmar su nuevo PIN.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-118">Users can also confirm their new PIN.</span></span> <span data-ttu-id="0ee6f-119">La función **Actualizar PIN** restablecerá el PIN al nuevo que selecciona el usuario.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-119">The **Update PIN** function will reset the PIN to the new one that the user selects.</span></span>

5.  <span data-ttu-id="0ee6f-120">Para administrar la contraseña, seleccione **desbloquear unidad** e introduzca la contraseña actual.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-120">To manage your password, select **Unlock drive** and enter your current password.</span></span> <span data-ttu-id="0ee6f-121">Tan pronto como se desbloquee la unidad, seleccione **Restablecer contraseña** para cambiar la contraseña actual.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-121">As soon as the drive is unlocked, select **Reset Password** to change your current password.</span></span>

## <span data-ttu-id="0ee6f-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0ee6f-122">Related topics</span></span>


[<span data-ttu-id="0ee6f-123">Administración de funciones de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="0ee6f-123">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





