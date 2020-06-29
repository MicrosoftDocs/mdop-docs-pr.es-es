---
title: Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows
description: Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows
author: dansimp
ms.assetid: c8503743-220c-497c-9785-e2feeca484d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 67a61763e556f8c3b93825220dbbd61a14b7d6f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824510"
---
# <span data-ttu-id="08651-103">Cómo ocultar el cifrado predeterminado de BitLocker en el Panel de Control de Windows</span><span class="sxs-lookup"><span data-stu-id="08651-103">How to Hide Default BitLocker Encryption in The Windows Control Panel</span></span>


<span data-ttu-id="08651-104">Administración y supervisión de Microsoft BitLocker (MBAM) ofrece un panel de control personalizado para los equipos cliente de MBAM denominados opciones de cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="08651-104">Microsoft BitLocker Administration and Monitoring (MBAM) offers a customized control panel for MBAM client computers that is named called BitLocker Encryption Options.</span></span> <span data-ttu-id="08651-105">Este panel de control personalizado puede reemplazar el panel de control predeterminado de BitLocker de Windows, denominado cifrado de unidad BitLocker.</span><span class="sxs-lookup"><span data-stu-id="08651-105">This customized control panel can replace the default Windows BitLocker control panel that is named BitLocker Drive Encryption.</span></span> <span data-ttu-id="08651-106">El panel de control de las opciones de cifrado de BitLocker, que se encuentra en sistema y seguridad en el panel de control de Windows, permite a los usuarios administrar su PIN y contraseñas, desbloquear unidades y ocultar la interfaz que permite a los administradores descifrar una unidad o reanudar o reanudar el cifrado de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="08651-106">The BitLocker Encryption Options control panel, located under System and Security in the Windows control panel, enables users to manage their PIN and passwords, unlock drives, and hides the interface that allows administrators to decrypt a drive or to suspend or resume BitLocker encryption.</span></span>

**<span data-ttu-id="08651-107">Para ocultar el cifrado de BitLocker predeterminado en el panel de control de Windows</span><span class="sxs-lookup"><span data-stu-id="08651-107">To hide default BitLocker Encryption in the Windows Control Panel</span></span>**

1.  <span data-ttu-id="08651-108">Vaya a **configuración de usuario** mediante la consola de administración de directivas de grupo (GPMC), la administración de directivas de grupo avanzada (AGPM) o el editor de directivas de grupo local en el equipo de directivas de grupo de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="08651-108">Browse to **User configuration** by using the Group Policy Management Console (GPMC), the Advanced Group Policy Management (AGPM), or the Local Group Policy Editor on the BitLocker Group Policies computer.</span></span>

2.  <span data-ttu-id="08651-109">Haga clic en **directivas**, seleccione **plantillas administrativas**y, a continuación, haga clic en **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="08651-109">Click **Policies**, select **Administrative Templates**, and then click **Control Panel**.</span></span>

3.  <span data-ttu-id="08651-110">En el panel de **detalles** , haga doble clic en **Ocultar elementos especificados del panel de control**y, a continuación, seleccione **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="08651-110">In the **Details** pane, double-click **Hide specified Control Panel items**, and then select **Enabled**.</span></span>

4.  <span data-ttu-id="08651-111">Haga clic en **Mostrar**, **haga clic en Agregar...** y, a continuación, escriba Microsoft. BitLockerDriveEncryption.</span><span class="sxs-lookup"><span data-stu-id="08651-111">Click **Show**, **click Add…**, and then type Microsoft.BitLockerDriveEncryption.</span></span> <span data-ttu-id="08651-112">Esta directiva oculta la herramienta de administración predeterminada de BitLocker de Windows del panel de control de Windows y permite al usuario abrir la herramienta de opciones de cifrado de MBAM BitLocker actualizada en el panel de control de Windows.</span><span class="sxs-lookup"><span data-stu-id="08651-112">This policy hides the default Windows BitLocker Management tool from the Windows Control Panel and allows the user to open the updated MBAM BitLocker Encryption Options tool from the Windows Control Panel.</span></span>

## <span data-ttu-id="08651-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08651-113">Related topics</span></span>


[<span data-ttu-id="08651-114">Implementación de objetos de directiva de grupo de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="08651-114">Deploying MBAM 1.0 Group Policy Objects</span></span>](deploying-mbam-10-group-policy-objects.md)

 

 





