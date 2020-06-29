---
title: Cómo denegar acceso a una aplicación
description: Cómo denegar acceso a una aplicación
author: dansimp
ms.assetid: 14f5e201-7265-462c-b738-57938dc3fc30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 56a89669ea8c6323023b585d6d58620cd203fc00
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817520"
---
# <span data-ttu-id="b4ffb-103">Cómo denegar acceso a una aplicación</span><span class="sxs-lookup"><span data-stu-id="b4ffb-103">How to Deny Access to an Application</span></span>


<span data-ttu-id="b4ffb-104">Los usuarios deben estar en la lista de **permisos de acceso** de una aplicación para cargar y usar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b4ffb-104">Users must be in an application's **Access Permissions** list to load and use the application.</span></span> <span data-ttu-id="b4ffb-105">Aunque la consola de administración del servidor de virtualización de aplicaciones no admite la denegación explícita de acceso de un grupo de usuarios a una aplicación, puede quitar los grupos de usuarios de las propiedades de una aplicación para lograrlo.</span><span class="sxs-lookup"><span data-stu-id="b4ffb-105">Although the Application Virtualization Server Management Console does not support explicitly denying a user group access to an application, you can remove the user groups from an application’s properties to achieve this.</span></span>

**<span data-ttu-id="b4ffb-106">Para denegar el acceso a una aplicación</span><span class="sxs-lookup"><span data-stu-id="b4ffb-106">To deny access to an application</span></span>**

1.  <span data-ttu-id="b4ffb-107">Para una aplicación existente, haga clic en el nodo **aplicaciones** en el panel izquierdo.</span><span class="sxs-lookup"><span data-stu-id="b4ffb-107">For an existing application, click the **Applications** node in the left pane.</span></span>

2.  <span data-ttu-id="b4ffb-108">Haga clic con el botón derecho en una aplicación en el panel derecho y elija **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="b4ffb-108">Right-click an application in the right pane, and choose **Properties**.</span></span> <span data-ttu-id="b4ffb-109">A continuación, seleccione la pestaña **permisos de acceso** .</span><span class="sxs-lookup"><span data-stu-id="b4ffb-109">Then select the **Access Permissions** tab.</span></span>

3.  <span data-ttu-id="b4ffb-110">Para quitar el acceso para un grupo de usuarios, resalte el grupo de usuarios y haga clic en **quitar**.</span><span class="sxs-lookup"><span data-stu-id="b4ffb-110">To remove access for a user group, highlight the user group and click **Remove**.</span></span>

4.  <span data-ttu-id="b4ffb-111">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b4ffb-111">Click **OK**.</span></span>

    <span data-ttu-id="b4ffb-112">**Nota:**  Para controlar el acceso a las aplicaciones, también puede limitar las licencias de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b4ffb-112">**Note** To control access to applications, you can also limit the application licenses.</span></span> <span data-ttu-id="b4ffb-113">La configuración de los grupos de usuarios adecuados en servicios de dominio de Active Directory proporciona la manera más sencilla de conceder y denegar el acceso a conjuntos de usuarios específicos.</span><span class="sxs-lookup"><span data-stu-id="b4ffb-113">Setting up the proper user groups in Active Directory Domain Services provides the easiest way to grant and deny access to specific sets of users.</span></span>

     

## <span data-ttu-id="b4ffb-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4ffb-114">Related topics</span></span>


[<span data-ttu-id="b4ffb-115">Cómo conceder acceso a una aplicación</span><span class="sxs-lookup"><span data-stu-id="b4ffb-115">How to Grant Access to an Application</span></span>](how-to-grant-access-to-an-application.md)

[<span data-ttu-id="b4ffb-116">Cómo administrar licencias de aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="b4ffb-116">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="b4ffb-117">Cómo administrar aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="b4ffb-117">How to Manage Applications in the Server Management Console</span></span>](how-to-manage-applications-in-the-server-management-console.md)

 

 





