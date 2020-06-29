---
title: Cómo cambiar los niveles de informes de registro y restablecer los archivos de registro
description: Cómo cambiar los niveles de informes de registro y restablecer los archivos de registro
author: dansimp
ms.assetid: 9561d6fb-b35c-491b-a355-000064583194
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7307dee0030d9c03a8107d9d0ceef2086a94df07
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818050"
---
# <span data-ttu-id="e705a-103">Cómo cambiar los niveles de informes de registro y restablecer los archivos de registro</span><span class="sxs-lookup"><span data-stu-id="e705a-103">How to Change the Log Reporting Levels and Reset the Log Files</span></span>


<span data-ttu-id="e705a-104">Puede usar el siguiente procedimiento para cambiar el nivel de informes de registro del nodo **Application Virtualization** en la consola de administración de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e705a-104">You can use the following procedure to change the log reporting level from the **Application Virtualization** node in the Application Virtualization Management Console.</span></span> <span data-ttu-id="e705a-105">Cuando el archivo de registro alcanza el tamaño máximo (el valor predeterminado es 256 MB), se fuerza el restablecimiento cuando se produce la siguiente escritura en el registro.</span><span class="sxs-lookup"><span data-stu-id="e705a-105">When the log file reaches the maximum size (default is 256 MB), a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="e705a-106">Un restablecimiento hace que se cree un nuevo archivo de registro y el nombre del archivo antiguo es de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e705a-106">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span>

**<span data-ttu-id="e705a-107">Para cambiar el nivel de informes de registro</span><span class="sxs-lookup"><span data-stu-id="e705a-107">To change the log reporting level</span></span>**

1.  <span data-ttu-id="e705a-108">Haga clic con el botón derecho en el nodo de **virtualización de aplicaciones** y seleccione **propiedades** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="e705a-108">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="e705a-109">En la pestaña **General** del cuadro de diálogo **propiedades** , en la lista desplegable **nivel de registro** , seleccione el nivel de registro que desee.</span><span class="sxs-lookup"><span data-stu-id="e705a-109">On the **General** tab in the **Properties** dialog box, from the **Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="e705a-110">**Nota:**  Si elige **detallado** como nivel de registro, los archivos de registro crecerán muy rápidamente.</span><span class="sxs-lookup"><span data-stu-id="e705a-110">**Note** If you choose **Verbose** as the logging level, the log files will grow large very quickly.</span></span> <span data-ttu-id="e705a-111">Esto puede desactivar el rendimiento del cliente, de modo que la práctica recomendada es usar este nivel de registro solo para diagnosticar problemas específicos.</span><span class="sxs-lookup"><span data-stu-id="e705a-111">This might inhibit client performance, so best practice is to use this log level only for diagnosing specific problems.</span></span>

     

3.  <span data-ttu-id="e705a-112">En la pestaña **General** del cuadro de diálogo **propiedades** , en la lista desplegable **nivel de registro del sistema** , seleccione el nivel de registro que desee.</span><span class="sxs-lookup"><span data-stu-id="e705a-112">On the **General** tab in the **Properties** dialog box, from the **System Log Level** drop-down list, select the desired log level.</span></span>

    <span data-ttu-id="e705a-113">**Nota:**  La configuración del **nivel de registro del sistema** controla el nivel de los mensajes enviados al registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="e705a-113">**Note** The **System Log Level** setting controls the level of messages sent to the system event log.</span></span> <span data-ttu-id="e705a-114">Los mensajes registrados son idénticos a los mensajes que se registran en el registro de eventos del cliente, pero se almacenan en una ubicación diferente.</span><span class="sxs-lookup"><span data-stu-id="e705a-114">The logged messages are identical to the messages that get logged to the client event log, but they are stored in a different location.</span></span>

     

4.  <span data-ttu-id="e705a-115">Haga clic en **Aceptar** o **aplicar** para cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="e705a-115">Click **OK** or **Apply** to change the setting.</span></span>

**<span data-ttu-id="e705a-116">Para restablecer el archivo de registro</span><span class="sxs-lookup"><span data-stu-id="e705a-116">To reset the log file</span></span>**

1.  <span data-ttu-id="e705a-117">Haga clic con el botón derecho en el nodo de **virtualización de aplicaciones** y seleccione **propiedades** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="e705a-117">Right-click the **Application Virtualization** node, and select **Properties** from the pop-up menu.</span></span>

2.  <span data-ttu-id="e705a-118">En la pestaña **General** del cuadro de diálogo **propiedades** , haga clic en **restablecer registro** para realizar una copia de seguridad del archivo de registro actual e iniciar inmediatamente un nuevo archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="e705a-118">On the **General** tab in the **Properties** dialog box, click **Reset Log** to back up the current log file and immediately start a new log file.</span></span> <span data-ttu-id="e705a-119">Los archivos de registro de la copia de seguridad se almacenan en la misma carpeta.</span><span class="sxs-lookup"><span data-stu-id="e705a-119">The backup log files are stored in the same folder.</span></span>

3.  <span data-ttu-id="e705a-120">Haga clic en **Aceptar** o **aplicar** para cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="e705a-120">Click **OK** or **Apply** to change the setting.</span></span>

## <span data-ttu-id="e705a-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e705a-121">Related topics</span></span>


[<span data-ttu-id="e705a-122">Cómo configurar el cliente en la consola de administración del cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e705a-122">How to Configure the Client in the Application Virtualization Client Management Console</span></span>](how-to-configure-the-client-in-the-application-virtualization-client-management-console.md)

[<span data-ttu-id="e705a-123">Permisos de acceso de usuario en el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e705a-123">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





