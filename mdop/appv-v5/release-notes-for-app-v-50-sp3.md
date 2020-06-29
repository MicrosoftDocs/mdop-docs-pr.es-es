---
title: Notas de la versión de App-V 5.0 SP3
description: Notas de la versión de App-V 5.0 SP3
author: dansimp
ms.assetid: bc4806e0-2aba-4c7b-9ecc-1b2cc54af1d0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b6d5834e4d0c953365f955922403c1a7a2058b1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813326"
---
# <span data-ttu-id="a2905-103">Notas de la versión de App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="a2905-103">Release Notes for App-V 5.0 SP3</span></span>


<span data-ttu-id="a2905-104">A continuación se muestran algunos problemas conocidos de Microsoft Application Virtualization (App-V) 5,0 SP3.</span><span class="sxs-lookup"><span data-stu-id="a2905-104">The following are known issues in Microsoft Application Virtualization (App-V) 5.0 SP3.</span></span>

## <span data-ttu-id="a2905-105">Los archivos del servidor no se pueden eliminar después de una nueva instalación de App-V 5,0 SP3 Server</span><span class="sxs-lookup"><span data-stu-id="a2905-105">Server files fail to get deleted after a new App-V 5.0 SP3 Server installation</span></span>


<span data-ttu-id="a2905-106">Si desinstala el servidor de App-V 5,0 SP1 y luego instala el servidor de App-V 5,0 SP3, se producirá un error en la instalación y se instalará la versión incorrecta del servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="a2905-106">If you uninstall the App-V 5.0 SP1 Server and then install the App-V 5.0 SP3 Server, the installation fails and the wrong version of the Management server is installed.</span></span> <span data-ttu-id="a2905-107">Se muestran los siguientes errores:</span><span class="sxs-lookup"><span data-stu-id="a2905-107">The following errors are displayed:</span></span>

`[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {bee44f0f-05be-48e4-81dd-d34a83600b95}, type: Upgrade, scope: PerMachine, version: 5.0.1218.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.``[0A5C:06F8][2014-09-12T19:08:00]i102: Detected related bundle: {e1ca9d65-0ebf-4fd5-98e5-00d6453967a4}, type: Upgrade, scope: PerMachine, version: 5.0.1224.0, operation: MajorUpgrade``[0A5C:06F8][2014-09-12T19:08:00]i000: AppvUX: A previous version of this product is installed; requesting upgrade.`

<span data-ttu-id="a2905-108">El problema se produce porque los archivos del servidor no se eliminan al desinstalar App-V 5,0 SP1, por lo que el proceso de instalación de App-V 5,0 SP3 realiza una actualización errónea en lugar de una instalación nueva.</span><span class="sxs-lookup"><span data-stu-id="a2905-108">The issue occurs because the Server files are not being deleted when you uninstall App-V 5.0 SP1, so the App-V 5.0 SP3 installation process erroneously does an upgrade instead of a new installation.</span></span>

<span data-ttu-id="a2905-109">**Solución alternativa**: Elimine la siguiente clave del registro antes de empezar a instalar App-V 5,0 SP3:</span><span class="sxs-lookup"><span data-stu-id="a2905-109">**Workaround**: Delete the following registry key before you start installing App-V 5.0 SP3:</span></span>

`HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Windows\CurrentVersion\Uninstall`

## <span data-ttu-id="a2905-110">Consultar AD DS puede hacer que algunas aplicaciones no funcionen correctamente</span><span class="sxs-lookup"><span data-stu-id="a2905-110">Querying AD DS can cause some applications to work incorrectly</span></span>


<span data-ttu-id="a2905-111">Cuando recibe paquetes actualizados consultando los servicios de dominio de Active Directory para obtener la pertenencia a grupos actualizados, puede hacer que algunas aplicaciones no funcionen correctamente si las aplicaciones dependen del token de acceso del usuario.</span><span class="sxs-lookup"><span data-stu-id="a2905-111">When you receive updated packages by querying Active Directory Domain Services for updated group memberships, it can cause some applications to work incorrectly if the applications depend on the user’s access token.</span></span> <span data-ttu-id="a2905-112">Además, las consultas de pertenencia a grupos frecuentes pueden provocar la sobrecarga del controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="a2905-112">In addition, frequent group membership queries can cause the domain controller to overload.</span></span> <span data-ttu-id="a2905-113">Para obtener más información sobre los tokens de acceso de usuario, consulte [tokens de Access](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).</span><span class="sxs-lookup"><span data-stu-id="a2905-113">For more information about user access tokens, see [Access Tokens](https://msdn.microsoft.com/library/windows/desktop/aa374909.aspx).</span></span>

<span data-ttu-id="a2905-114">**Solución**: Espere a que el usuario cierre sesión y vuelva a iniciarla antes de consultar las pertenencias a grupos actualizadas.</span><span class="sxs-lookup"><span data-stu-id="a2905-114">**Workaround**: Wait until the user logs off and then logs back on before you query for updated group memberships.</span></span> <span data-ttu-id="a2905-115">No use la clave del registro, que se describe en el [paquete de Hotfix 2 para Microsoft Application virtualization 5,0 Service Pack 1](https://support.microsoft.com/kb/2897087), para consultar las pertenencias a grupos actualizadas.</span><span class="sxs-lookup"><span data-stu-id="a2905-115">Do not use the registry key, described in [Hotfix Package 2 for Microsoft Application Virtualization 5.0 Service Pack 1](https://support.microsoft.com/kb/2897087), to query for updated group memberships.</span></span>






## <span data-ttu-id="a2905-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2905-116">Related topics</span></span>


[<span data-ttu-id="a2905-117">Acerca de App-V 5.0 SP3</span><span class="sxs-lookup"><span data-stu-id="a2905-117">About App-V 5.0 SP3</span></span>](about-app-v-50-sp3.md)

 

 





