---
title: Configurar la conexión del servidor AGPM
description: Configurar la conexión del servidor AGPM
author: dansimp
ms.assetid: 74e8f348-a8ed-4d69-a8e0-9c974aaeca2d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83a2437ee8c2fe562141ff167cb85c6a06b7cefe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818920"
---
# <span data-ttu-id="45a41-103">Configurar la conexión del servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="45a41-103">Configure the AGPM Server Connection</span></span>


<span data-ttu-id="45a41-104">Para asegurarse de que está conectado al archivo central correcto, revise la configuración de la conexión del servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="45a41-104">To ensure that you are connected to the correct central archive, review the configuration of the AGPM Server connection.</span></span> <span data-ttu-id="45a41-105">Si un administrador de AGPM (control total) no ha configurado la conexión del servidor de AGPM, debe configurarlo manualmente.</span><span class="sxs-lookup"><span data-stu-id="45a41-105">If an AGPM Administrator (Full Control) has not configured the AGPM Server connection for you, then you must manually configure it.</span></span>

**<span data-ttu-id="45a41-106">Para seleccionar un servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="45a41-106">To select an AGPM Server</span></span>**

1.  <span data-ttu-id="45a41-107">En el árbol de **consola de administración de directivas de grupo** , haga clic en **Cambiar control** en el bosque y el dominio en el que desea administrar los GPO.</span><span class="sxs-lookup"><span data-stu-id="45a41-107">In the **Group Policy Management Console** tree, click **Change Control** in the forest and domain in which you want to manage GPOs.</span></span>

2.  <span data-ttu-id="45a41-108">En el panel de detalles, haga clic en la pestaña **servidor de AGPM** :</span><span class="sxs-lookup"><span data-stu-id="45a41-108">In the details pane, click the **AGPM Server** tab:</span></span>

    -   <span data-ttu-id="45a41-109">Si las opciones de la pestaña **servidor de AGPM** no están disponibles, un administrador de AGPM las ha configurado de forma centralizada.</span><span class="sxs-lookup"><span data-stu-id="45a41-109">If the options on the **AGPM Server** tab are unavailable, they have been centrally configured by an AGPM Administrator.</span></span>

    -   <span data-ttu-id="45a41-110">Si las opciones de la pestaña **servidor de AGPM** están disponibles, escriba el nombre de equipo completo para el servidor de AGPM (por ejemplo, Server.contoso.com) y el puerto en el que el servicio AGPM escucha (de forma predeterminada, el puerto 4600).</span><span class="sxs-lookup"><span data-stu-id="45a41-110">If the options on the **AGPM Server** tab are available, type the fully-qualified computer name for the AGPM Server (for example, server.contoso.com) and the port on which the AGPM Service listens (by default, port 4600).</span></span> <span data-ttu-id="45a41-111">Haga clic en **aplicar**y, a continuación, en **sí** para confirmar.</span><span class="sxs-lookup"><span data-stu-id="45a41-111">Click **Apply**, then click **Yes** to confirm.</span></span>

### <span data-ttu-id="45a41-112">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="45a41-112">Additional considerations</span></span>

-   <span data-ttu-id="45a41-113">Los servidores de AGPM seleccionados determinan qué objetos de directiva de grupo se muestran en la pestaña **contenido** y en qué ubicación se aplica la configuración de la pestaña **delegación de dominios** .</span><span class="sxs-lookup"><span data-stu-id="45a41-113">The AGPM Servers selected determine which GPOs are displayed on the **Contents** tab and to what location the **Domain Delegation** tab settings are applied.</span></span> <span data-ttu-id="45a41-114">Si no se administra de forma centralizada a través de la plantilla administrativa, cada administrador de directivas de grupo debe configurar esta opción para que apunte al servidor de AGPM para el dominio.</span><span class="sxs-lookup"><span data-stu-id="45a41-114">If not centrally managed through the Administrative template, each Group Policy administrator must configure this setting to point to the AGPM Server for the domain.</span></span>

### <span data-ttu-id="45a41-115">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="45a41-115">Additional references</span></span>

-   [<span data-ttu-id="45a41-116">Realización de tareas de editor</span><span class="sxs-lookup"><span data-stu-id="45a41-116">Performing Editor Tasks</span></span>](performing-editor-tasks.md)

-   [<span data-ttu-id="45a41-117">Realización de tareas del Aprobador</span><span class="sxs-lookup"><span data-stu-id="45a41-117">Performing Approver Tasks</span></span>](performing-approver-tasks.md)

-   [<span data-ttu-id="45a41-118">Realización de tareas de revisor</span><span class="sxs-lookup"><span data-stu-id="45a41-118">Performing Reviewer Tasks</span></span>](performing-reviewer-tasks.md)

 

 





