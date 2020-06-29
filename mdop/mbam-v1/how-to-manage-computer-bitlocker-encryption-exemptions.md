---
title: Cómo administrar exenciones de cifrado de BitLocker de equipo
description: Cómo administrar exenciones de cifrado de BitLocker de equipo
author: dansimp
ms.assetid: d4400a0d-b36b-4cf5-a294-1f53ec47f9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51b93061468508900eaee7fce8a7827e2db61d19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825680"
---
# <span data-ttu-id="3a3e1-103">Cómo administrar exenciones de cifrado de BitLocker de equipo</span><span class="sxs-lookup"><span data-stu-id="3a3e1-103">How to Manage Computer BitLocker Encryption Exemptions</span></span>


<span data-ttu-id="3a3e1-104">La administración y supervisión de Microsoft BitLocker (MBAM) se puede usar para excluir determinados equipos de la protección de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3a3e1-104">Microsoft BitLocker Administration and Monitoring (MBAM) can be used to exempt certain computers from BitLocker protection.</span></span> <span data-ttu-id="3a3e1-105">Por ejemplo, una organización puede decidir controlar la exención de BitLocker entre equipos.</span><span class="sxs-lookup"><span data-stu-id="3a3e1-105">For example, an organization may decide to control BitLocker exemption on a computer-by-computer basis.</span></span>

<span data-ttu-id="3a3e1-106">Para eximir a un equipo del cifrado de BitLocker, debe agregar el equipo a un grupo de seguridad en ActiveDirectoryDomainServices para omitir las reglas de protección de BitLocker basadas en equipos.</span><span class="sxs-lookup"><span data-stu-id="3a3e1-106">To exempt a computer from BitLocker encryption, you must add the computer to a security group in ActiveDirectoryDomainServices in order to bypass any computer-based BitLocker protection rules.</span></span>

<span data-ttu-id="3a3e1-107">**Nota:**  Si el equipo ya está protegido por BitLocker, la Directiva de exención de equipos no surte efecto.</span><span class="sxs-lookup"><span data-stu-id="3a3e1-107">**Note** If the computer is already BitLocker-protected, the computer exemption policy has no effect.</span></span>

 

**<span data-ttu-id="3a3e1-108">Para excluir un equipo del cifrado de BitLocker</span><span class="sxs-lookup"><span data-stu-id="3a3e1-108">To exempt a computer from BitLocker encryption</span></span>**

1.  <span data-ttu-id="3a3e1-109">Agregue la cuenta de equipo que desea que esté exenta a un grupo de seguridad en ActiveDirectoryDomainServices.</span><span class="sxs-lookup"><span data-stu-id="3a3e1-109">Add the computer account that you want to be exempted to a security group in ActiveDirectoryDomainServices.</span></span> <span data-ttu-id="3a3e1-110">Esto le permite omitir cualquier regla de protección de BitLocker basada en el equipo.</span><span class="sxs-lookup"><span data-stu-id="3a3e1-110">This allows you to bypass any computer-based BitLocker protection rules.</span></span>

2.  <span data-ttu-id="3a3e1-111">Cree un objeto de directiva de grupo con la plantilla de directiva de grupo MBAM, a continuación, asocie el objeto de directiva de grupo con el grupo de Active Directory que creó en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="3a3e1-111">Create a Group Policy Object by using the MBAM Group Policy template, then associate the Group Policy Object with the Active Directory group that you created in the previous step.</span></span> <span data-ttu-id="3a3e1-112">Para obtener más información acerca de la creación de los objetos de directiva de grupo necesarios, consulte [implementar objetos de directiva de grupo de MBAM 1,0](deploying-mbam-10-group-policy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3a3e1-112">For more information about creating the necessary Group Policy Objects, see [Deploying MBAM 1.0 Group Policy Objects](deploying-mbam-10-group-policy-objects.md).</span></span>

3.  <span data-ttu-id="3a3e1-113">Cuando se inicia un equipo excluido, el cliente de MBAM comprueba la configuración de la Directiva de exención de equipos y suspende la protección en función de si el equipo forma parte del grupo de seguridad de exención de BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3a3e1-113">When an exempted computer starts, the MBAM client checks the Computer Exemption Policy setting and suspends protection based on whether the computer is part of the BitLocker exemption security group.</span></span>

## <span data-ttu-id="3a3e1-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a3e1-114">Related topics</span></span>


[<span data-ttu-id="3a3e1-115">Administración de funciones de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="3a3e1-115">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





