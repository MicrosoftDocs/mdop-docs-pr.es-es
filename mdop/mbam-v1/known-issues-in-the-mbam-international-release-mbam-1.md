---
title: Problemas conocidos de la versión internacional de MBAM.
description: Problemas conocidos de la versión internacional de MBAM.
author: dansimp
ms.assetid: bbf888dc-93c1-4323-b43c-0ded098e9b93
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: af32551135ff297d25930f94b40bf04c0fcaaafe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825790"
---
# <span data-ttu-id="d6109-103">Problemas conocidos de la versión internacional de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d6109-103">Known Issues in the MBAM International Release</span></span>

<span data-ttu-id="d6109-104">Esta sección contiene problemas conocidos con la versión internacional de administración y supervisión de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="d6109-104">This section contains known issues for Microsoft BitLocker Administration and Monitoring (MBAM) International Release.</span></span>

## <span data-ttu-id="d6109-105">Problemas conocidos de la versión internacional de MBAM.</span><span class="sxs-lookup"><span data-stu-id="d6109-105">Known Issues in the MBAM International Release</span></span>

### <span data-ttu-id="d6109-106">El proceso de instalación no especifica Update</span><span class="sxs-lookup"><span data-stu-id="d6109-106">The Installation Process Does Not Specify Update</span></span>

<span data-ttu-id="d6109-107">Después de actualizar el servidor o servidores de administración de Microsoft BitLocker, el programa de instalación no indica que se está instalando una actualización.</span><span class="sxs-lookup"><span data-stu-id="d6109-107">Upon updating the Microsoft BitLocker Administration and Monitoring server or servers, the Setup program does not state that an update is being installed.</span></span>

<span data-ttu-id="d6109-108">**Solución alternativa**: ninguno.</span><span class="sxs-lookup"><span data-stu-id="d6109-108">**Workaround**: None.</span></span>

### <span data-ttu-id="d6109-109">Certificados que se usan para el rol de servidor administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="d6109-109">Certificates Used for the Administration and Monitoring Server Role</span></span>

<span data-ttu-id="d6109-110">Si está usando un certificado para la autenticación entre servidores MBAM, después de actualizar el servidor de administración y supervisión de MBAM debe asegurarse de que el certificado es válido y no ha sido revocado ni ha expirado.</span><span class="sxs-lookup"><span data-stu-id="d6109-110">If you are using a certificate for authentication between MBAM servers, after updating the MBAM Administration and Monitoring server you must ensure that the certificate is valid and not revoked or expired.</span></span>

<span data-ttu-id="d6109-111">**Solución alternativa**: ninguno.</span><span class="sxs-lookup"><span data-stu-id="d6109-111">**Workaround**: None.</span></span>

### <span data-ttu-id="d6109-112">MBAM Svclog archivo llenado de disco</span><span class="sxs-lookup"><span data-stu-id="d6109-112">MBAM Svclog File Filling Disk Space</span></span>

<span data-ttu-id="d6109-113">Si ha seguido el [artículo 2668170 de Knowledge Base](https://go.microsoft.com/fwlink/?LinkID=247277), es posible que tenga que repetir los pasos de KB después de instalar esta actualización.</span><span class="sxs-lookup"><span data-stu-id="d6109-113">If you have followed [Knowledge Base article 2668170](https://go.microsoft.com/fwlink/?LinkID=247277), you might have to repeat the KB steps after you install this update.</span></span>

<span data-ttu-id="d6109-114">**Solución alternativa**: ninguno.</span><span class="sxs-lookup"><span data-stu-id="d6109-114">**Workaround**: None.</span></span>

## <span data-ttu-id="d6109-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d6109-115">Related topics</span></span>

[<span data-ttu-id="d6109-116">Implementación de la actualización de versión de idioma de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="d6109-116">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





