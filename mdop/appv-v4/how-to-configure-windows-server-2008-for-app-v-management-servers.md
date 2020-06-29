---
title: Cómo configurar Windows Server 2008 para servidores de administración de App-V
description: Cómo configurar Windows Server 2008 para servidores de administración de App-V
author: dansimp
ms.assetid: 38b4016f-de82-4209-9159-387d20ddee25
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2d1cd7e84ffc0036c98e70a9a0ee1fd3a4ade790
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817721"
---
# <span data-ttu-id="8b6c1-103">Cómo configurar Windows Server 2008 para servidores de administración de App-V</span><span class="sxs-lookup"><span data-stu-id="8b6c1-103">How to Configure Windows Server 2008 for App-V Management Servers</span></span>


<span data-ttu-id="8b6c1-104">El servidor de Windows Server 2008 en el que se instala el servicio Web de administración de Microsoft Application Virtualization (App-V) requiere que los servicios de Internet Information Services (IIS) se instalen como un rol en el servidor.</span><span class="sxs-lookup"><span data-stu-id="8b6c1-104">The Windows Server 2008 server on which you install the Microsoft Application Virtualization (App-V) Management Web Service requires Internet Information Services (IIS) to be installed as a role on the server.</span></span> <span data-ttu-id="8b6c1-105">Use el siguiente procedimiento para configurar Windows Server 2008 para admitir la instalación de App-vServer.</span><span class="sxs-lookup"><span data-stu-id="8b6c1-105">Use the following procedure to configure Windows Server 2008 to support App-Vserver installation.</span></span>

**<span data-ttu-id="8b6c1-106">Para instalar IIS en un equipo con Windows Server2008</span><span class="sxs-lookup"><span data-stu-id="8b6c1-106">To install IIS on a Windows Server2008 computer</span></span>**

1.  <span data-ttu-id="8b6c1-107">En el equipo con Windows Server2008, haga clic en **Inicio**, haga clic en **todos los programas**, en **herramientas administrativas**y, a continuación, haga clic en **Administrador de servidores** para iniciar el administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="8b6c1-107">On the Windows Server2008 computer, click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Server Manager** to start Server Manager.</span></span> <span data-ttu-id="8b6c1-108">En Administrador del servidor, haga clic con el botón secundario en el nodo **roles** y haga clic en **Agregar roles** para iniciar el **Asistente para agregar roles**.</span><span class="sxs-lookup"><span data-stu-id="8b6c1-108">In Server Manager, right-click the **Roles** node, and click **Add Roles** to start the **Add Roles Wizard**.</span></span>

2.  <span data-ttu-id="8b6c1-109">En el **Asistente para agregar roles**, en la página **Seleccionar roles de servidor** , seleccione **servidor Web (IIS)**.</span><span class="sxs-lookup"><span data-stu-id="8b6c1-109">In the **Add Roles Wizard**, on the **Select Server Roles** page, select **Web Server (IIS)**.</span></span> <span data-ttu-id="8b6c1-110">Cuando se le solicite, haga clic en **Agregar características obligatorias** para agregar las características dependientes.</span><span class="sxs-lookup"><span data-stu-id="8b6c1-110">When prompted, click **Add Required Features** to add the dependent features.</span></span>

3.  <span data-ttu-id="8b6c1-111">En la página **Seleccionar roles de servidor** , haga clic en **siguiente**y, después, vuelva a hacer clic en **siguiente** .</span><span class="sxs-lookup"><span data-stu-id="8b6c1-111">On the **Select Server Roles** page, Click **Next**, and then click **Next** again.</span></span>

4.  <span data-ttu-id="8b6c1-112">En el **Asistente para agregar roles**, en la página **seleccionar servicios de rol** :</span><span class="sxs-lookup"><span data-stu-id="8b6c1-112">In the **Add Roles Wizard**, on the **Select Role Services** page:</span></span>

    1.  <span data-ttu-id="8b6c1-113">En **desarrollo de aplicaciones**, seleccione **ASP.net** y, cuando se le solicite, haga clic en **Agregar servicios de rol obligatorios** para agregar las características y los servicios de roles dependientes.</span><span class="sxs-lookup"><span data-stu-id="8b6c1-113">Under **Application Development**, select **ASP.NET** and, when prompted, click **Add Required Role Services** to add the dependent roles services and features.</span></span>

    2.  <span data-ttu-id="8b6c1-114">En **seguridad**, seleccione **autenticación de Windows**.</span><span class="sxs-lookup"><span data-stu-id="8b6c1-114">Under **Security**, select **Windows Authentication**.</span></span>

    3.  <span data-ttu-id="8b6c1-115">En el nodo **herramientas de administración** , seleccione **herramientas y scripts de administración de IIS**.</span><span class="sxs-lookup"><span data-stu-id="8b6c1-115">In the **Management Tools** node, select **IIS Management Scripts and Tools**.</span></span> <span data-ttu-id="8b6c1-116">En **compatibilidad con Iis6 Management**, asegúrese de que estén seleccionadas la compatibilidad con IIS de **IIS6 metabase Compatibility** y **IIS6** y, después, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="8b6c1-116">Under **IIS6 Management Compatibility**, ensure that both **IIS6 Metabase Compatibility** and **IIS6 WMI Compatibility** are selected, and then click **Next**.</span></span>

5.  <span data-ttu-id="8b6c1-117">En la página **confirmar selecciones de instalación** , haga clic en **instalar**y, a continuación, complete el resto del asistente.</span><span class="sxs-lookup"><span data-stu-id="8b6c1-117">On the **Confirm Installation Selections** page, click **Install**, and then complete the rest of the wizard.</span></span>

6.  <span data-ttu-id="8b6c1-118">Haga clic en **cerrar** para salir del **Asistente para agregar roles**y, a continuación, cierre el administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="8b6c1-118">Click **Close** to exit the **Add Roles Wizard**, and then close Server Manager.</span></span>

## <span data-ttu-id="8b6c1-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b6c1-119">Related topics</span></span>


[<span data-ttu-id="8b6c1-120">Requisitos de implementación de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8b6c1-120">Application Virtualization Deployment Requirements</span></span>](application-virtualization-deployment-requirements.md)

[<span data-ttu-id="8b6c1-121">Implementación de virtualización de aplicaciones y listas de comprobación de actualización</span><span class="sxs-lookup"><span data-stu-id="8b6c1-121">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





