---
title: Notas de la versión de MED-V 1.0
description: Notas de la versión de MED-V 1.0
author: dansimp
ms.assetid: 006a3537-5c5b-43b5-8df8-4bf6ddd3cd2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 683056f768a3d547828996a9b191d58337c21ad6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826591"
---
# <span data-ttu-id="96cc6-103">Notas de la versión de MED-V 1.0</span><span class="sxs-lookup"><span data-stu-id="96cc6-103">MED-V 1.0 Release Notes</span></span>


## <span data-ttu-id="96cc6-104">Problemas conocidos con MED-V</span><span class="sxs-lookup"><span data-stu-id="96cc6-104">Known Issues with MED-V</span></span>


<span data-ttu-id="96cc6-105">Esta sección proporciona la información más actualizada sobre problemas generales con la plataforma de virtualización de escritorio de Microsoft Enterprise (MED-V).</span><span class="sxs-lookup"><span data-stu-id="96cc6-105">This section provides the most up-to-date information about general issues with the Microsoft Enterprise Desktop Virtualization (MED-V) platform.</span></span> <span data-ttu-id="96cc6-106">Estos problemas no aparecen en la documentación del producto y, en algunos casos, podrían contradecir la documentación del producto existente.</span><span class="sxs-lookup"><span data-stu-id="96cc6-106">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="96cc6-107">Siempre que sea posible, estos problemas se resolverán en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="96cc6-107">Whenever possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="96cc6-108">Las descargas de archivos no siguen las reglas de redireccionamiento web</span><span class="sxs-lookup"><span data-stu-id="96cc6-108">File downloads do not follow Web redirection rules</span></span>

<span data-ttu-id="96cc6-109">Descargas de archivos no siga las reglas de redirección web establecidas en una directiva de área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="96cc6-109">File downloads do not follow Web redirection rules set in a MED-V workspace policy.</span></span>

### <span data-ttu-id="96cc6-110">Al expandir una ventana de aplicación publicada en la consola a pantalla completa, desaparece</span><span class="sxs-lookup"><span data-stu-id="96cc6-110">When expanding a console-published application window to full screen, it disappears</span></span>

<span data-ttu-id="96cc6-111">Si expande la ventana de una aplicación publicada en consola (como cmd.exe) a pantalla completa dentro de un área de trabajo de MED-V configurada en modo de integración transparente, la ventana de la aplicación podría desaparecer o no responder.</span><span class="sxs-lookup"><span data-stu-id="96cc6-111">If you expand a console-published application (such as cmd.exe) window to full screen inside a MED-V workspace configured in seamless integration mode, the application window might disappear or not respond.</span></span>

### <span data-ttu-id="96cc6-112">Al trabajar en el modo de escritorio completo, las ubicaciones de los iconos en el escritorio no se guardan</span><span class="sxs-lookup"><span data-stu-id="96cc6-112">When working in full desktop mode, icon locations on the desktop are not saved</span></span>

<span data-ttu-id="96cc6-113">Al trabajar en modo de escritorio completo, los cambios de ubicación manual de los iconos en el escritorio no se guardan entre las sesiones del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="96cc6-113">When working in full desktop mode, manual location changes of icons on the desktop are not saved between MED-V workspace sessions.</span></span>

### <span data-ttu-id="96cc6-114">No puede existir en el mismo dominio una imagen local y una imagen de prueba con el mismo nombre</span><span class="sxs-lookup"><span data-stu-id="96cc6-114">A local image and a test image with the same name cannot exist in the same domain</span></span>

<span data-ttu-id="96cc6-115">Si una imagen local se une al dominio y el administrador crea una nueva versión de la misma imagen con el mismo nombre de equipo que una imagen de prueba, cuando la imagen de prueba se une al dominio, se produce un error en la acción unirse al dominio o la imagen local se quita del dominio.</span><span class="sxs-lookup"><span data-stu-id="96cc6-115">If a local image is joined to the domain and the administrator creates a new version of the same image with the same computer name as a test image, when the test image joins the domain, either the join domain action fails or it succeeds and the local image is removed from the domain.</span></span>

### <span data-ttu-id="96cc6-116">MED-V no es compatible con las características de Windows Aero</span><span class="sxs-lookup"><span data-stu-id="96cc6-116">MED-V does not support Windows Aero features</span></span>

<span data-ttu-id="96cc6-117">MED-V no es compatible con las características de Windows Aero (como aero Flip 3D).</span><span class="sxs-lookup"><span data-stu-id="96cc6-117">MED-V does not support Windows Aero features (such as Aero Flip 3D).</span></span>

### <span data-ttu-id="96cc6-118">La consola de administración solo la puede usar un usuario de Windows por equipo</span><span class="sxs-lookup"><span data-stu-id="96cc6-118">The management console can be used by only one Windows user per computer</span></span>

<span data-ttu-id="96cc6-119">La consola de administración de MED-V solo la pueden usar los administradores y el usuario de Windows que instaló la aplicación de administración.</span><span class="sxs-lookup"><span data-stu-id="96cc6-119">The MED-V management console can be used only by administrators and the Windows user who installed the management application.</span></span>

### <span data-ttu-id="96cc6-120">La utilidad de configuración del servidor MED-V prueba la conectividad de Microsoft SQL Server en contexto de usuario en lugar de en el contexto de servicio servidor MED-V</span><span class="sxs-lookup"><span data-stu-id="96cc6-120">The MED-V Server configuration utility tests Microsoft SQL Server connectivity under user context rather than under MED-V Server service context</span></span>

<span data-ttu-id="96cc6-121">MED-V usa el contexto de servicio de servidor MED-V para recopilar informes de la base de datos de informes de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="96cc6-121">MED-V uses MED-V Server service context to collect reports from the Microsoft SQL Server reports database.</span></span> <span data-ttu-id="96cc6-122">La utilidad de configuración del servidor MED-V comprueba la base de datos y prueba la cadena de conexión de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="96cc6-122">The MED-V Server configuration utility verifies the database and tests the database connection string.</span></span> <span data-ttu-id="96cc6-123">No valida el acceso del servicio servidor MED-V a la base de datos.</span><span class="sxs-lookup"><span data-stu-id="96cc6-123">It does not validate the access of MED-V Server service to the database.</span></span>

 

 





