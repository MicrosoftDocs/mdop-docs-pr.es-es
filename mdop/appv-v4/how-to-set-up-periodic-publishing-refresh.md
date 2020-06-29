---
title: Cómo configurar la actualización periódica de publicación
description: Cómo configurar la actualización periódica de publicación
author: dansimp
ms.assetid: c358c765-cb88-4881-b4e7-0a2e87304870
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a5bbea1c661d6cb5a78f0bb9de29538e0222cda6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816551"
---
# <span data-ttu-id="86c25-103">Cómo configurar la actualización periódica de publicación</span><span class="sxs-lookup"><span data-stu-id="86c25-103">How to Set Up Periodic Publishing Refresh</span></span>


<span data-ttu-id="86c25-104">Puede usar el siguiente procedimiento para configurar que el cliente actualice periódicamente la información de publicación de los servidores de App-V.</span><span class="sxs-lookup"><span data-stu-id="86c25-104">You can use the following procedure to configure the client to periodically refresh the publishing information from the App-V servers.</span></span> <span data-ttu-id="86c25-105">Una vez configurado el cliente, la operación de actualización es automática.</span><span class="sxs-lookup"><span data-stu-id="86c25-105">After the client is configured, the refresh operation is automatic.</span></span> <span data-ttu-id="86c25-106">Esta configuración establece la configuración predeterminada del cliente para que todos los usuarios de este equipo vean la misma configuración.</span><span class="sxs-lookup"><span data-stu-id="86c25-106">These settings configure the default settings for the client so that all users on this computer will see the same settings.</span></span>

<span data-ttu-id="86c25-107">**Nota:**  Una vez que haya realizado este procedimiento, la información de publicación se actualizará de acuerdo con la nueva configuración después de la primera actualización al iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="86c25-107">**Note** After you have performed this procedure, the publishing information will be refreshed according to the new settings after the first refresh at login.</span></span> <span data-ttu-id="86c25-108">Cuando se produce esta primera actualización, el servidor puede invalidar la configuración del equipo con una configuración diferente, en función de cómo esté configurada.</span><span class="sxs-lookup"><span data-stu-id="86c25-108">When this first refresh occurs, the server might override the computer settings with different settings, depending on how it is configured.</span></span> <span data-ttu-id="86c25-109">La pestaña **Actualizar** del cuadro de diálogo **propiedades** muestra la configuración del equipo cliente configurada localmente y la configuración que el servidor de publicación podría haber configurado.</span><span class="sxs-lookup"><span data-stu-id="86c25-109">The **Refresh** tab in the **Properties** dialog box shows the locally configured client computer settings and any settings that might have been configured for the user by the publishing server.</span></span>

 

**<span data-ttu-id="86c25-110">Para actualizar periódicamente la información de publicación de los servidores de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="86c25-110">To periodically refresh the publishing information from the Application Virtualization Servers</span></span>**

1.  <span data-ttu-id="86c25-111">En el panel **ámbito** , haga clic en **servidores de publicación** .</span><span class="sxs-lookup"><span data-stu-id="86c25-111">Click **Publishing Servers** in the **Scope** pane.</span></span>

2.  <span data-ttu-id="86c25-112">En el panel de **resultados** , haga clic con el botón derecho en el servidor deseado y seleccione **propiedades** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="86c25-112">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up-menu.</span></span>

3.  <span data-ttu-id="86c25-113">En el cuadro de diálogo **propiedades** , en la pestaña **Actualizar** , seleccione la casilla de verificación **actualizar la configuración cada** y escriba un número que represente la frecuencia en el campo.</span><span class="sxs-lookup"><span data-stu-id="86c25-113">In the **Properties** dialog box, on the **Refresh** tab, select the **Refresh configuration every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="86c25-114">A continuación, seleccione **minutos**, **horas**y **días** en el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="86c25-114">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span>

    <span data-ttu-id="86c25-115">**Nota:**  Esta configuración hará que el cliente actualice la información de publicación cada vez que transcurre el período configurado.</span><span class="sxs-lookup"><span data-stu-id="86c25-115">**Note** This setting will cause the client to refresh publishing information every time the configured period elapses.</span></span> <span data-ttu-id="86c25-116">Si el usuario no ha iniciado sesión cuando es el momento de realizar una actualización, la actualización se realizará la próxima vez que el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="86c25-116">If the user is not logged in when it's time to do a refresh, the refresh will take place when the user next logs in.</span></span> <span data-ttu-id="86c25-117">A continuación, el temporizador vuelve a iniciarse para el siguiente período.</span><span class="sxs-lookup"><span data-stu-id="86c25-117">The timer is then started again for the next period.</span></span>

     

4.  <span data-ttu-id="86c25-118">Haga clic en **aplicar** para cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="86c25-118">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="86c25-119">Cuando termine de configurar el servidor, haga clic en **Aceptar** para salir del cuadro de diálogo y volver a la consola de administración del cliente de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="86c25-119">When you finish configuring the server, click **OK** to exit the dialog box and return to the Application Virtualization Client Management Console.</span></span>

## <span data-ttu-id="86c25-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86c25-120">Related topics</span></span>


[<span data-ttu-id="86c25-121">Cómo configurar el cliente en la consola de administración del cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="86c25-121">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

 

 





