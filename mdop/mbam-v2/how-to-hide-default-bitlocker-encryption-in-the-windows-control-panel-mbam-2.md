---
title: Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows
description: Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows
author: dansimp
ms.assetid: 6674aa51-2b5d-4e4a-8b43-2cc18d008285
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eda8fafbd7b3ebf414520354eba6def2e97f6237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824081"
---
# <span data-ttu-id="f99cf-103">Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows</span><span class="sxs-lookup"><span data-stu-id="f99cf-103">How to Hide Default BitLocker Encryption in the Windows Control Panel</span></span>


<span data-ttu-id="f99cf-104">Administración y supervisión de Microsoft BitLocker (MBAM) ofrece un panel de control personalizado para los equipos cliente de supervisión y administración de Microsoft BitLocker, denominados opciones de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f99cf-104">Microsoft BitLocker Administration and Monitoring (MBAM) offers a customized control panel for Microsoft BitLocker Administration and Monitoring client computers, called BitLocker Encryption Options.</span></span> <span data-ttu-id="f99cf-105">Este panel de control personalizado puede reemplazar el panel de control predeterminado de BitLocker de Windows, que se denomina cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f99cf-105">This customized control panel can replace the default Windows BitLocker control panel, which is called BitLocker Drive Encryption.</span></span> <span data-ttu-id="f99cf-106">El panel de control personalizado, que se encuentra en el panel de control, está en sistema y seguridad, permite a los usuarios administrar su PIN y contraseñas y desbloquear unidades, y oculta la interfaz que permite a los administradores descifrar una unidad o reanudar o reanudar el cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f99cf-106">The customized control panel, which is in Control Panel under System and Security, enables users to manage their PIN and passwords and to unlock drives, and hides the interface that enables administrators to decrypt a drive or to suspend or resume BitLocker drive encryption.</span></span>

**<span data-ttu-id="f99cf-107">Para ocultar el cifrado de unidad BitLocker predeterminado en el panel de control de Windows</span><span class="sxs-lookup"><span data-stu-id="f99cf-107">To hide default BitLocker drive encryption in Windows Control Panel</span></span>**

1.  <span data-ttu-id="f99cf-108">En la consola de administración de directivas de grupo (GPMC), la administración avanzada de directivas de grupo (AGPM) o el editor de directivas de grupo local en el equipo de directivas de grupo de BitLocker, vaya a **configuración de usuario**.</span><span class="sxs-lookup"><span data-stu-id="f99cf-108">In the Group Policy Management Console (GPMC), the Advanced Group Policy Management (AGPM), or the Local Group Policy Editor on the BitLocker Group Policies computer, browse to **User configuration**.</span></span>

2.  <span data-ttu-id="f99cf-109">A continuación, haga clic en **directivas**, seleccione **plantillas administrativas**y, a continuación, haga clic en **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="f99cf-109">Next, click **Policies**, select **Administrative Templates**, and then click **Control Panel**.</span></span>

3.  <span data-ttu-id="f99cf-110">Haga doble clic en **ocultar los elementos especificados del panel de control** en el panel de **detalles** y, a continuación, seleccione **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="f99cf-110">Double-click **Hide specified Control Panel items** in the **Details** pane, and then select **Enabled**.</span></span>

4.  <span data-ttu-id="f99cf-111">Haga clic en **Mostrar**, en **Agregar**y, a continuación, escriba **Microsoft. BitLockerDriveEncryption**.</span><span class="sxs-lookup"><span data-stu-id="f99cf-111">Click **Show**, click **Add**, and then type **Microsoft.BitLockerDriveEncryption**.</span></span> <span data-ttu-id="f99cf-112">Esta directiva oculta la herramienta de administración predeterminada de BitLocker de Windows del panel de control de Windows y, en el panel de control, permite al usuario abrir la herramienta de opciones de cifrado de MBAM BitLocker actualizada en sistema y seguridad.</span><span class="sxs-lookup"><span data-stu-id="f99cf-112">This policy hides the default Windows BitLocker Management tool from the Windows Control Panel and, in Control Panel, lets the user open the updated MBAM BitLocker Encryption Options tool under System and Security.</span></span>

## <span data-ttu-id="f99cf-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f99cf-113">Related topics</span></span>


[<span data-ttu-id="f99cf-114">Implementación de objetos de directiva de grupo de MBAM 2.0</span><span class="sxs-lookup"><span data-stu-id="f99cf-114">Deploying MBAM 2.0 Group Policy Objects</span></span>](deploying-mbam-20-group-policy-objects-mbam-2.md)

 

 





