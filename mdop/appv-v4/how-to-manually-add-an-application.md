---
title: Cómo agregar manualmente una aplicación
description: Cómo agregar manualmente una aplicación
author: dansimp
ms.assetid: c635b07a-5c7f-4ab2-ba18-366457146cb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 868939553fae6172ccca549ddc3f08aa76ee3c56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817100"
---
# <span data-ttu-id="c2284-103">Cómo agregar manualmente una aplicación</span><span class="sxs-lookup"><span data-stu-id="c2284-103">How to Manually Add an Application</span></span>


<span data-ttu-id="c2284-104">Al agregar una aplicación al servidor de administración de virtualización de la aplicación, se recomienda que la importe.</span><span class="sxs-lookup"><span data-stu-id="c2284-104">When adding an application to the Application Virtualization Management Server, it is recommended that you import it.</span></span> <span data-ttu-id="c2284-105">Puede Agregar una aplicación manualmente, pero debe proporcionar la información precisa y detallada sobre la aplicación a la que se ha llamado en esta sección.</span><span class="sxs-lookup"><span data-stu-id="c2284-105">You can add an application manually, but you must provide the precise, detailed information about the application called for in this section.</span></span>

**<span data-ttu-id="c2284-106">Para agregar manualmente una nueva aplicación</span><span class="sxs-lookup"><span data-stu-id="c2284-106">To manually add a new application</span></span>**

1.  <span data-ttu-id="c2284-107">En el panel de la izquierda, haga clic con el botón derecho en el nodo **aplicaciones** y elija **nueva aplicación**.</span><span class="sxs-lookup"><span data-stu-id="c2284-107">In the left pane, right-click the **Applications** node and choose **New Application**.</span></span>

2.  <span data-ttu-id="c2284-108">En el **Asistente para nueva aplicación**, complete el cuadro de diálogo **información general** :</span><span class="sxs-lookup"><span data-stu-id="c2284-108">In the **New Application Wizard**, complete the **General Information** dialog box:</span></span>

    1.  <span data-ttu-id="c2284-109">**Nombre**de la aplicación: escriba el nombre que desea que vean los usuarios.</span><span class="sxs-lookup"><span data-stu-id="c2284-109">**Application Name**—Type the name you want the users to see.</span></span>

    2.  <span data-ttu-id="c2284-110">**Versión**: escriba la versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2284-110">**Version**—Type the application version.</span></span>

    3.  <span data-ttu-id="c2284-111">**Habilitado**: este cuadro debe estar seleccionado para transmitir la aplicación después de crearla.</span><span class="sxs-lookup"><span data-stu-id="c2284-111">**Enabled**—This box must be selected to stream the application after you create it.</span></span>

    4.  <span data-ttu-id="c2284-112">**Descripción**: escriba una descripción opcional para el uso administrativo.</span><span class="sxs-lookup"><span data-stu-id="c2284-112">**Description**—Type an optional description for administrative use.</span></span>

    5.  <span data-ttu-id="c2284-113">**Ruta de acceso a OSD**: examine la red hasta el archivo descriptor de software abierto (OSD) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2284-113">**OSD Path**—Browse the network to the application's Open Software Descriptor (OSD) file.</span></span> <span data-ttu-id="c2284-114">Este archivo debe estar en una carpeta de red compartida.</span><span class="sxs-lookup"><span data-stu-id="c2284-114">This file must be in a shared network folder.</span></span>

    6.  <span data-ttu-id="c2284-115">**Ruta de icono**: Busque el archivo ICO de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2284-115">**Icon Path**—Browse to the application's ICO file.</span></span>

    7.  <span data-ttu-id="c2284-116">**Grupo de licencias de aplicación**: Si ha configurado grupos de licencias, puede asignar la aplicación a una si la selecciona en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="c2284-116">**Application License Group**—If you have set up license groups, you can assign the application to one by selecting it in the pull-down list.</span></span>

    8.  <span data-ttu-id="c2284-117">**Grupo de servidores**: Si tiene varios servidores de virtualización de aplicaciones, puede asignar la aplicación a uno seleccionándolo en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="c2284-117">**Server Group**—If you have multiple Application Virtualization Servers, you can assign the application to one by selecting it in the pull-down list.</span></span>

3.  <span data-ttu-id="c2284-118">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="c2284-118">Click **Next**.</span></span>

4.  <span data-ttu-id="c2284-119">En el cuadro de diálogo **seleccionar paquete** , seleccione el paquete relacionado y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="c2284-119">In the **Select Package** dialog box, select the related package and click **Next**.</span></span>

5.  <span data-ttu-id="c2284-120">En la pantalla **accesos directos publicados** , seleccione las casillas de las ubicaciones en las que desea que aparezcan los accesos directos de la aplicación en los equipos cliente y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="c2284-120">On the **Published Shortcuts** screen, select the boxes for the locations where you would like the application shortcuts to appear on the client computers and click **Next**.</span></span>

6.  <span data-ttu-id="c2284-121">En la pantalla **asociaciones de archivos** , puede agregar nuevas asociaciones de archivo de tipo a esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="c2284-121">In the **File Associations** screen, you can add new type file associations to this application.</span></span> <span data-ttu-id="c2284-122">Para ello, haga clic en **Agregar**, escriba la extensión (sin un punto anterior), escriba una descripción y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c2284-122">To do so, click **Add**, enter the extension (without a preceding dot), enter a description, and click **OK**.</span></span>

7.  <span data-ttu-id="c2284-123">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="c2284-123">Click **Next**.</span></span>

8.  <span data-ttu-id="c2284-124">En el cuadro de diálogo **permisos de acceso** , haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="c2284-124">In the **Access Permissions** dialog box, click **Add**.</span></span>

9.  <span data-ttu-id="c2284-125">En el cuadro de diálogo **Agregar/editar grupo de usuarios** , vaya al grupo de usuarios.</span><span class="sxs-lookup"><span data-stu-id="c2284-125">In the **Add/Edit User Group** dialog box, navigate to the user group.</span></span> <span data-ttu-id="c2284-126">También puede especificar el dominio y el grupo escribiendo la información en los campos respectivos.</span><span class="sxs-lookup"><span data-stu-id="c2284-126">You can also enter the domain and group by typing the information in the respective fields.</span></span> <span data-ttu-id="c2284-127">Cuando termine, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="c2284-127">When you finish, click **OK**.</span></span> <span data-ttu-id="c2284-128">Puede agregar otros grupos con las mismas páginas.</span><span class="sxs-lookup"><span data-stu-id="c2284-128">You can add other groups with the same pages.</span></span>

10. <span data-ttu-id="c2284-129">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="c2284-129">Click **Next**.</span></span>

11. <span data-ttu-id="c2284-130">En la pantalla **Resumen** , puede revisar la configuración de importación.</span><span class="sxs-lookup"><span data-stu-id="c2284-130">On the **Summary** screen, you can review the import settings.</span></span> <span data-ttu-id="c2284-131">Haga clic en **Finalizar** para agregar la aplicación, haga clic en **atrás** para cambiar la información, o haga clic en **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="c2284-131">Click **Finish** to add the application, click **Back** to change the information, or click **Cancel**.</span></span>

## <span data-ttu-id="c2284-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c2284-132">Related topics</span></span>


[<span data-ttu-id="c2284-133">Cómo administrar aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="c2284-133">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





