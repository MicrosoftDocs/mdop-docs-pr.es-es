---
title: Cómo configurar la actualización de publicación en el inicio de sesión
description: Cómo configurar la actualización de publicación en el inicio de sesión
author: dansimp
ms.assetid: 196448db-7645-4fd5-a854-ef6405b15db4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dd131ab5acbb8224e60077dfcc4272d4aa132b5e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816560"
---
# <span data-ttu-id="00e94-103">Cómo configurar la actualización de publicación en el inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="00e94-103">How to Set Up Publishing Refresh on Login</span></span>


<span data-ttu-id="00e94-104">Puede usar el siguiente procedimiento para configurar el cliente de Application Virtualization (App-V) para actualizar la información de publicación del servidor cada vez que inicie sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="00e94-104">You can use the following procedure to configure the Application Virtualization (App-V) Client to refresh the publishing information from the server each time you log in to the computer.</span></span> <span data-ttu-id="00e94-105">Una vez configurado el cliente, la operación de actualización es automática.</span><span class="sxs-lookup"><span data-stu-id="00e94-105">After the client is configured, the refresh operation is automatic.</span></span>

**<span data-ttu-id="00e94-106">Para actualizar la información de publicación al iniciar sesión</span><span class="sxs-lookup"><span data-stu-id="00e94-106">To refresh the publishing information on login</span></span>**

1.  <span data-ttu-id="00e94-107">En el panel **ámbito** , haga clic en **servidores de publicación** .</span><span class="sxs-lookup"><span data-stu-id="00e94-107">Click **Publishing Servers** in the **Scope** pane.</span></span>

2.  <span data-ttu-id="00e94-108">En el panel de **resultados** , haga clic con el botón derecho en el servidor deseado y seleccione **propiedades** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="00e94-108">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up-menu.</span></span>

3.  <span data-ttu-id="00e94-109">En el cuadro de diálogo **propiedades** , en la pestaña **Actualizar** , active la casilla **actualizar el servidor de configuración al inicio de sesión de usuario** .</span><span class="sxs-lookup"><span data-stu-id="00e94-109">In the **Properties** dialog box, on the **Refresh** tab, select the **Refresh configuration server on user login** check box.</span></span>

4.  <span data-ttu-id="00e94-110">Haga clic en **aplicar** para cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="00e94-110">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="00e94-111">Cuando termine de configurar los valores, haga clic en **Aceptar** para salir del cuadro de diálogo y volver a la consola de administración de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="00e94-111">When you finish configuring the settings, click **OK** to exit the dialog box and return to the Application Virtualization Management Console.</span></span>

    <span data-ttu-id="00e94-112">La información de publicación se actualizará cada vez que inicie sesión en el sistema.</span><span class="sxs-lookup"><span data-stu-id="00e94-112">The publishing information will now be refreshed each time you log in to the system.</span></span>

## <span data-ttu-id="00e94-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="00e94-113">Related topics</span></span>


[<span data-ttu-id="00e94-114">Cómo configurar el cliente en la consola de administración del cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="00e94-114">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





