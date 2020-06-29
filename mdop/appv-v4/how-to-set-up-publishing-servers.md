---
title: Cómo configurar servidores de publicación
description: Cómo configurar servidores de publicación
author: dansimp
ms.assetid: 2111f079-c202-4c49-b2a6-f4237068b2dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f060d862fd1449f5240ad495b53a1fa4e97697f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816530"
---
# <span data-ttu-id="3c21b-103">Cómo configurar servidores de publicación</span><span class="sxs-lookup"><span data-stu-id="3c21b-103">How to Set Up Publishing Servers</span></span>


<span data-ttu-id="3c21b-104">Puede usar los procedimientos siguientes para agregar y configurar servidores de virtualización de aplicaciones directamente desde la consola de administración de clientes.</span><span class="sxs-lookup"><span data-stu-id="3c21b-104">You can use the following procedures to add and configure Application Virtualization Servers directly from the Client Management Console.</span></span>

**<span data-ttu-id="3c21b-105">Para agregar un servidor de publicación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="3c21b-105">To add an application publishing server</span></span>**

1.  <span data-ttu-id="3c21b-106">En el panel de **resultados** , haga clic con el botón secundario del mouse y seleccione **nuevo servidor** en el menú emergente para iniciar el nuevo Asistente para servidor de virtualización de aplicaciones, o bien, haga clic con el botón derecho en el nodo **Publishing Server** y seleccione **nuevo servidor** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="3c21b-106">In the **Results** pane, right-click and select **New Server** from the pop-up-menu to start the New Application Virtualization Server Wizard, or alternatively, right-click the **Publishing Server** node and select **New Server** from the pop-up-menu.</span></span>

2.  <span data-ttu-id="3c21b-107">En la página uno del asistente, escriba el nombre del servidor en el campo **nombre para mostrar** y seleccione el tipo de servidor de la lista desplegable **tipo** .</span><span class="sxs-lookup"><span data-stu-id="3c21b-107">On page one of the wizard, enter the name of the server in the **Display Name** field and select the server type from the **Type** drop-down list.</span></span> <span data-ttu-id="3c21b-108">Puede elegir **Application Virtualization Server**, **servidor de virtualización de aplicaciones de seguridad mejorada**, servidor **http estándar**o **servidor HTTP de seguridad mejorado** de la lista desplegable de tipos de servidor.</span><span class="sxs-lookup"><span data-stu-id="3c21b-108">You can choose **Application Virtualization Server**, **Enhanced Security Application Virtualization Server**, **Standard HTTP Server**, or **Enhanced Security HTTP Server** from the drop-down list of server types.</span></span>

3.  <span data-ttu-id="3c21b-109">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3c21b-109">Click **Next**.</span></span>

4.  <span data-ttu-id="3c21b-110">En la página dos del asistente, escriba la información adecuada en los campos **nombre de host** y **Puerto** .</span><span class="sxs-lookup"><span data-stu-id="3c21b-110">On page two of the wizard, type the appropriate information into the **Host Name** and **Port** fields.</span></span> <span data-ttu-id="3c21b-111">El campo **path** no se puede editar en servidores de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="3c21b-111">The **Path** field is not editable for Application Virtualization Servers.</span></span> <span data-ttu-id="3c21b-112">Debes escribir una ruta de acceso para el servidor HTTP estándar o el servidor HTTP de seguridad mejorado.</span><span class="sxs-lookup"><span data-stu-id="3c21b-112">You must enter a path for Standard HTTP Server or Enhanced Security HTTP Server.</span></span>

5.  <span data-ttu-id="3c21b-113">Haga clic en **Finalizar** para agregar el servidor.</span><span class="sxs-lookup"><span data-stu-id="3c21b-113">Click **Finish** to add the server.</span></span>

**<span data-ttu-id="3c21b-114">Para configurar un servidor de publicación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="3c21b-114">To set up an application publishing server</span></span>**

1.  <span data-ttu-id="3c21b-115">En el panel de **resultados** , haga clic con el botón derecho en el servidor deseado y seleccione **propiedades** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="3c21b-115">In the **Results** pane, right-click the desired server and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="3c21b-116">Haga clic en la pestaña **General** , donde puede cambiar el nombre del servidor, seleccionar un tipo de la lista desplegable de tipos de servidor y especificar el nombre de host y el puerto.</span><span class="sxs-lookup"><span data-stu-id="3c21b-116">Click the **General** tab, where you can change the server name, select a type from the drop-down list of server types, and specify the host name and port.</span></span> <span data-ttu-id="3c21b-117">Cuando el tipo de servidor es un servidor HTTP estándar o un servidor HTTP de seguridad mejorado, el campo **ruta** también se puede editar.</span><span class="sxs-lookup"><span data-stu-id="3c21b-117">When the server type is Standard HTTP Server or Enhanced Security HTTP Server, the **Path** field is also editable.</span></span>

3.  <span data-ttu-id="3c21b-118">Haga clic en la pestaña **Actualizar** , donde la casilla **de verificación actualizar la publicación en el inicio de sesión del usuario** está activada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3c21b-118">Click the **Refresh** tab, where the **Refresh publishing on user login** check box is selected by default.</span></span> <span data-ttu-id="3c21b-119">Para cambiar la frecuencia de actualización, active la casilla **Actualizar publicación cada** y escriba un número que represente la frecuencia en el campo.</span><span class="sxs-lookup"><span data-stu-id="3c21b-119">To change the refresh rate, select the **Refresh publishing every** check box and enter a number that represents the frequency in the field.</span></span> <span data-ttu-id="3c21b-120">A continuación, seleccione **minutos**, **horas**y **días** en el menú desplegable.</span><span class="sxs-lookup"><span data-stu-id="3c21b-120">Then select **Minutes**, **Hours**, **Days** from the drop-down menu.</span></span> <span data-ttu-id="3c21b-121">(La cantidad mínima de tiempo que puedes introducir es de 30 minutos).</span><span class="sxs-lookup"><span data-stu-id="3c21b-121">(The minimum amount of time you can enter is 30 minutes.)</span></span>

4.  <span data-ttu-id="3c21b-122">Haga clic en **aplicar** para cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="3c21b-122">Click **Apply** to change the configuration.</span></span>

5.  <span data-ttu-id="3c21b-123">Cuando haya terminado de publicar, haga clic en **Aceptar** para salir del cuadro de diálogo y volver a la consola de administración de cliente.</span><span class="sxs-lookup"><span data-stu-id="3c21b-123">When you are finished publishing, click **OK** to exit the dialog box and return to the Client Management Console.</span></span>

## <span data-ttu-id="3c21b-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3c21b-124">Related topics</span></span>


[<span data-ttu-id="3c21b-125">Cómo deshabilitar o modificar la configuración de modo de operación desconectado</span><span class="sxs-lookup"><span data-stu-id="3c21b-125">How to Disable or Modify Disconnected Operation Mode Settings</span></span>](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





