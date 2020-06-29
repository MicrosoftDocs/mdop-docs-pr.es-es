---
title: Ocultación del elemento de Cifrado de unidad BitLocker predeterminado en el Panel de Control
description: Ocultación del elemento de Cifrado de unidad BitLocker predeterminado en el Panel de Control
author: dansimp
ms.assetid: 6e2a9a02-a809-43a1-80a3-1b03c7192c89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af395928ca8934bfea4eeb848bbd4ee377987293
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823100"
---
# <span data-ttu-id="f6e11-103">Ocultación del elemento de Cifrado de unidad BitLocker predeterminado en el Panel de Control</span><span class="sxs-lookup"><span data-stu-id="f6e11-103">Hiding the Default BitLocker Drive Encryption Item in Control Panel</span></span>


<span data-ttu-id="f6e11-104">En este tema se describe cómo ocultar el elemento del panel de control del **cifrado de unidad BitLocker** , que aparece de forma predeterminada en el panel de control como parte del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="f6e11-104">This topic describes how to hide the **BitLocker Drive Encryption** Control Panel item, which appears by default on Control Panel as part of the Windows operating system.</span></span>

<span data-ttu-id="f6e11-105">**Nota:**  Administración y supervisión de Microsoft BitLocker (MBAM) crea un elemento de panel de control adicional personalizado, denominado **Opciones de cifrado de BitLocker**, que permite a los usuarios finales administrar su PIN y contraseña, Activar BitLocker para una unidad y comprobar el cifrado.</span><span class="sxs-lookup"><span data-stu-id="f6e11-105">**Note** Microsoft BitLocker Administration and Monitoring (MBAM) creates an additional, custom Control Panel item, called **BitLocker Encryption Options**, which enables end users to manage their PIN and password, turn on BitLocker for a drive, and check encryption.</span></span>

 

<span data-ttu-id="f6e11-106">Consulte [comprender las opciones de cifrado de BitLocker y los elementos de cifrado de unidad BitLocker en el panel de control](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) para obtener información sobre:</span><span class="sxs-lookup"><span data-stu-id="f6e11-106">See [Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md) to read about:</span></span>

-   <span data-ttu-id="f6e11-107">Diferencias entre el MBAM y los elementos predeterminados del panel de control</span><span class="sxs-lookup"><span data-stu-id="f6e11-107">Differences between the MBAM and the default Control Panel items</span></span>

-   <span data-ttu-id="f6e11-108">Menú contextual de **Administración de BitLocker** que aparece al hacer clic con el botón secundario en una unidad en el explorador de Windows</span><span class="sxs-lookup"><span data-stu-id="f6e11-108">**Manage BitLocker** shortcut menu that appears when you right-click a drive in Windows Explorer</span></span>

<span data-ttu-id="f6e11-109">**Importante**  No cambie la configuración de directiva de grupo en el nodo **cifrado de unidad BitLocker** .</span><span class="sxs-lookup"><span data-stu-id="f6e11-109">**Important** Do not change the Group Policy settings in the **BitLocker Drive Encryption** node.</span></span> <span data-ttu-id="f6e11-110">Si lo hace, MBAM no funcionará correctamente.</span><span class="sxs-lookup"><span data-stu-id="f6e11-110">If you do, MBAM will not work correctly.</span></span> <span data-ttu-id="f6e11-111">Al establecer la configuración de directiva de grupo en el nodo de **MBAM de MDOP (administración de BitLocker)** , MBAM configura automáticamente la configuración de **cifrado de unidad BitLocker** para usted.</span><span class="sxs-lookup"><span data-stu-id="f6e11-111">When you configure the Group Policy settings in the **MDOP MBAM (BitLocker Management)** node, MBAM automatically configures the **BitLocker Drive Encryption** settings for you.</span></span>

 

**<span data-ttu-id="f6e11-112">Para ocultar el elemento de cifrado de unidad BitLocker predeterminado en el panel de control</span><span class="sxs-lookup"><span data-stu-id="f6e11-112">To hide the default BitLocker Drive Encryption item in Control Panel</span></span>**

1.  <span data-ttu-id="f6e11-113">En la consola de administración de directivas de grupo (GPMC) o en administración avanzada de directivas de grupo, vaya a directivas de **configuración de usuario** en el &gt; **Policies** &gt; Panel de control **plantillas administrativas** &gt; **Control Panel**.</span><span class="sxs-lookup"><span data-stu-id="f6e11-113">In the Group Policy Management Console (GPMC) or in Advanced Group Policy Management, browse to **User configuration** &gt; **Policies** &gt; **Administrative Templates** &gt; **Control Panel**.</span></span>

2.  <span data-ttu-id="f6e11-114">En el panel de **detalles** , haga doble clic en **Ocultar elementos especificados del panel de control**y, a continuación, haga clic en **habilitado**.</span><span class="sxs-lookup"><span data-stu-id="f6e11-114">In the **Details** pane, double-click **Hide specified Control Panel items**, and then click **Enabled**.</span></span>

3.  <span data-ttu-id="f6e11-115">Haga clic en **Mostrar**, en **Agregar**y, a continuación, escriba **Microsoft. BitLockerDriveEncryption**.</span><span class="sxs-lookup"><span data-stu-id="f6e11-115">Click **Show**, click **Add**, and then type **Microsoft.BitLockerDriveEncryption**.</span></span>



## <span data-ttu-id="f6e11-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6e11-116">Related topics</span></span>


[<span data-ttu-id="f6e11-117">Comprender las opciones de cifrado de BitLocker y elementos de Cifrado de unidad BitLocker en el Panel de Control</span><span class="sxs-lookup"><span data-stu-id="f6e11-117">Understanding the BitLocker Encryption Options and BitLocker Drive Encryption Items in Control Panel</span></span>](understanding-the-bitlocker-encryption-options-and-bitlocker-drive-encryption-items-in-control-panel.md)

[<span data-ttu-id="f6e11-118">Implementación de objetos de directiva de grupo de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="f6e11-118">Deploying MBAM 2.5 Group Policy Objects</span></span>](deploying-mbam-25-group-policy-objects.md)

 

## <span data-ttu-id="f6e11-119">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="f6e11-119">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="f6e11-120">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="f6e11-120">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="f6e11-121">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="f6e11-121">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span> 





