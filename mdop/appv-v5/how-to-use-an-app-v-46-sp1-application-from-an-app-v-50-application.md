---
ms.reviewer: ''
title: Cómo usar una aplicación de App-V 4,6 desde una aplicación de App-V 5,0
description: Cómo usar una aplicación de App-V 4,6 desde una aplicación de App-V 5,0
ms.assetid: 4e78cb32-9c8b-478e-ae8b-c474a7e42487
author: msfttracyp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 8b29e861b97d18e427f6a8247a1f731be2dc0889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813646"
---
# <span data-ttu-id="aae0d-103">Cómo usar una aplicación de App-V 4,6 desde una aplicación de App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="aae0d-103">How to Use an App-V 4.6 Application From an App-V 5.0 Application</span></span>

<span data-ttu-id="aae0d-104">*Nota:*\* App-V 4,6 ha salido del soporte técnico estándar.</span><span class="sxs-lookup"><span data-stu-id="aae0d-104">*Note:*\* App-V 4.6 has exited Mainstream support.</span></span> <span data-ttu-id="aae0d-105">Lo siguiente se aplica a un paquete de App-V 4,6 SP3.</span><span class="sxs-lookup"><span data-stu-id="aae0d-105">The following applies to an App-V 4.6 SP3 package.</span></span>

<span data-ttu-id="aae0d-106">Use el siguiente procedimiento para ejecutar una aplicación de App-V 4.6 con aplicaciones de App-V 5,0 en un cliente independiente.</span><span class="sxs-lookup"><span data-stu-id="aae0d-106">Use the following procedure to run an App-V4.6 application with App-V 5.0 applications on a standalone client.</span></span>

**<span data-ttu-id="aae0d-107">Para ejecutar aplicaciones en un cliente independiente</span><span class="sxs-lookup"><span data-stu-id="aae0d-107">To run applications on a standalone client</span></span>**

1.  <span data-ttu-id="aae0d-108">Seleccione dos aplicaciones de su entorno que se pueden abrir entre sí.</span><span class="sxs-lookup"><span data-stu-id="aae0d-108">Select two applications in your environment that can be opened from one another.</span></span> <span data-ttu-id="aae0d-109">Por ejemplo, Microsoft Outlook y Adobe Acrobat Reader.</span><span class="sxs-lookup"><span data-stu-id="aae0d-109">For example, Microsoft Outlook and Adobe Acrobat Reader.</span></span> <span data-ttu-id="aae0d-110">Puede acceder a un archivo adjunto de correo electrónico creado con Adobe Acrobat.</span><span class="sxs-lookup"><span data-stu-id="aae0d-110">You can access an email attachment created using Adobe Acrobat.</span></span>

2.  <span data-ttu-id="aae0d-111">Convierta los paquetes o cree un nuevo paquete para cualquiera de las aplicaciones con el formato de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="aae0d-111">Convert the packages, or create a new package for either of the applications using the App-V 5.0 format.</span></span> <span data-ttu-id="aae0d-112">Para obtener más información sobre la conversión de paquetes, consulte [Cómo migrar puntos de extensión desde un paquete de App-v 4,6 a un paquete de App-v 5,0 convertido para todos los usuarios de un equipo específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md) o [Cómo migrar puntos de extensión desde un paquete de app-v 4,6 a App-v 5,0 para un usuario específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span><span class="sxs-lookup"><span data-stu-id="aae0d-112">For more information about converting packages see, [How to Migrate Extension Points From an App-V 4.6 Package to a Converted App-V 5.0 Package for All Users on a Specific Computer](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md) or [How to Migrate Extension Points From an App-V 4.6 Package to App-V 5.0 for a Specific User](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md).</span></span>

3.  <span data-ttu-id="aae0d-113">Agregue y aprovisione el paquete con la consola de administración de App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="aae0d-113">Add and provision the package using the App-V 5.0 management console.</span></span> <span data-ttu-id="aae0d-114">Para obtener más información sobre agregar y aprovisionar paquetes, consulte [Cómo agregar o actualizar paquetes mediante la consola de administración](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) y [Cómo configurar el acceso a los paquetes mediante la consola de administración](how-to-configure-access-to-packages-by-using-the-management-console-50.md).</span><span class="sxs-lookup"><span data-stu-id="aae0d-114">For more information adding and provisioning packages see, [How to Add or Upgrade Packages by Using the Management Console](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md) and [How to Configure Access to Packages by Using the Management Console](how-to-configure-access-to-packages-by-using-the-management-console-50.md).</span></span>

4.  <span data-ttu-id="aae0d-115">La aplicación convertida ahora se ejecuta con App-V 5,0 y puede abrir una aplicación de la otra.</span><span class="sxs-lookup"><span data-stu-id="aae0d-115">The converted application now runs using App-V 5.0 and you can open one application from the other.</span></span> <span data-ttu-id="aae0d-116">Por ejemplo, si ha convertido un paquete de Microsoft Office en un paquete de App-V 5,0 y Adobe Acrobat aún se está ejecutando como un paquete de App-V 4.6, puede abrir un archivo adjunto de Adobe Acrobat Reader con Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="aae0d-116">For example, if you converted a Microsoft Office package to an App-V 5.0 package and Adobe Acrobat is still running as an App-V4.6 package, you can open an Adobe Acrobat Reader attachment using Microsoft Outlook.</span></span>

    <span data-ttu-id="aae0d-117">**¿Tiene una sugerencia para App-V**?</span><span class="sxs-lookup"><span data-stu-id="aae0d-117">**Got a suggestion for App-V**?</span></span> <span data-ttu-id="aae0d-118">Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span><span class="sxs-lookup"><span data-stu-id="aae0d-118">Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization).</span></span> **<span data-ttu-id="aae0d-119">¿Tiene un problema de App-V?</span><span class="sxs-lookup"><span data-stu-id="aae0d-119">Got an App-V issue?</span></span>** <span data-ttu-id="aae0d-120">Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span><span class="sxs-lookup"><span data-stu-id="aae0d-120">Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).</span></span>

## <span data-ttu-id="aae0d-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aae0d-121">Related topics</span></span>


[<span data-ttu-id="aae0d-122">Operaciones de App-V 5.0</span><span class="sxs-lookup"><span data-stu-id="aae0d-122">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 








