---
title: Cómo agregar un servidor
description: Cómo agregar un servidor
author: dansimp
ms.assetid: 1f31678a-8edf-4d35-a812-e4a2abfd979b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d08b79bcbf34910ce357f39635431d11e3e99bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821390"
---
# <span data-ttu-id="56eed-103">Cómo agregar un servidor</span><span class="sxs-lookup"><span data-stu-id="56eed-103">How to Add a Server</span></span>


<span data-ttu-id="56eed-104">Para ayudarle a administrar los servidores de administración de virtualización de aplicaciones de forma más eficaz, organícelas en grupos de servidores.</span><span class="sxs-lookup"><span data-stu-id="56eed-104">To help you manage your Application Virtualization Management Servers more efficiently, organize them into server groups.</span></span> <span data-ttu-id="56eed-105">Después de crear un grupo de servidores en la consola de administración de Application Virtualization Server, puede usar el siguiente procedimiento para agregar un servidor al grupo.</span><span class="sxs-lookup"><span data-stu-id="56eed-105">After you create a server group in the Application Virtualization Server Management Console, you can use the following procedure to add a server to the group.</span></span>

<span data-ttu-id="56eed-106">**Nota:**  Todos los servidores de un grupo de servidores deben estar conectados al mismo almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="56eed-106">**Note** All servers in a server group must be connected to the same data store.</span></span>

 

**<span data-ttu-id="56eed-107">Para agregar un servidor a un grupo</span><span class="sxs-lookup"><span data-stu-id="56eed-107">To add a server to a group</span></span>**

1.  <span data-ttu-id="56eed-108">Haga clic en el nodo **grupos de servidores** en el panel izquierdo para expandir la lista de grupos de servidores.</span><span class="sxs-lookup"><span data-stu-id="56eed-108">Click the **Server Groups** node in the left pane to expand the list of server groups.</span></span>

2.  <span data-ttu-id="56eed-109">Haga clic con el botón secundario en el grupo de servidores que desee y seleccione **nuevo servidor de administración de virtualización de aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="56eed-109">Right-click the desired server group, and select **New Application Virtualization Management Server**.</span></span>

3.  <span data-ttu-id="56eed-110">En el **Asistente para nuevo grupo de servidores**, escriba el **nombre para mostrar** y el **nombre de host DNS**.</span><span class="sxs-lookup"><span data-stu-id="56eed-110">In the **New Server Group Wizard**, enter the **Display Name** and the **DNS Host Name**.</span></span>

4.  <span data-ttu-id="56eed-111">Deje los valores predeterminados en el campo **asignación de memoria máxima** para la caché del servidor y el campo de **asignación de memoria** de advertencia para especificar el nivel de advertencia de umbral.</span><span class="sxs-lookup"><span data-stu-id="56eed-111">Leave the default values in the **Maximum Memory Allocation** field for the server cache and the **Warn Memory Allocation** field to specify the threshold warning level.</span></span>

5.  <span data-ttu-id="56eed-112">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="56eed-112">Click **Next**.</span></span>

6.  <span data-ttu-id="56eed-113">En el cuadro de diálogo **modo de seguridad de conexión** , active la casilla **usar seguridad mejorada** para seleccionar el modo de seguridad mejorada, si lo desea.</span><span class="sxs-lookup"><span data-stu-id="56eed-113">In the **Connection Security Mode** dialog, check the **Use enhanced security** box to select enhanced security mode, if desired.</span></span> <span data-ttu-id="56eed-114">Si es necesario, complete el **Asistente para certificados** o vea los certificados existentes.</span><span class="sxs-lookup"><span data-stu-id="56eed-114">If necessary, complete the **Certificate Wizard** or view existing certificates.</span></span>

7.  <span data-ttu-id="56eed-115">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="56eed-115">Click **Next**.</span></span>

8.  <span data-ttu-id="56eed-116">En el cuadro de diálogo **configuración de puerto de virt de aplicaciones** , seleccione el botón usar el **puerto predeterminado** o el botón de radio **Puerto personalizado de usuario** y escriba el número de Puerto personalizado.</span><span class="sxs-lookup"><span data-stu-id="56eed-116">In the **App Virt Port Setting** dialog, select the **Use Default Port** or the **User Custom Port** radio button and enter the custom port number.</span></span>

9.  <span data-ttu-id="56eed-117">Haz clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="56eed-117">Click **Finish**.</span></span>

## <span data-ttu-id="56eed-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="56eed-118">Related topics</span></span>


[<span data-ttu-id="56eed-119">Cómo crear un grupo de servidores</span><span class="sxs-lookup"><span data-stu-id="56eed-119">How to Create a Server Group</span></span>](how-to-create-a-server-group.md)

[<span data-ttu-id="56eed-120">Cómo quitar un servidor</span><span class="sxs-lookup"><span data-stu-id="56eed-120">How to Remove a Server</span></span>](how-to-remove-a-server.md)

 

 





