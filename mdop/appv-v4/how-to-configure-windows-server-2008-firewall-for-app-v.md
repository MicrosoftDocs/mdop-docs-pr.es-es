---
title: Cómo configurar el Firewall de Windows Server 2008 para App-V
description: Cómo configurar el Firewall de Windows Server 2008 para App-V
author: dansimp
ms.assetid: 57f4ed17-0651-4a3c-be1e-29d9520c6aeb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 19e4cda9ac3b908f68e4f69b9663033d8a21ae41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817720"
---
# <span data-ttu-id="9beb0-103">Cómo configurar el Firewall de Windows Server 2008 para App-V</span><span class="sxs-lookup"><span data-stu-id="9beb0-103">How to Configure Windows Server 2008 Firewall for App-V</span></span>


<span data-ttu-id="9beb0-104">Con la introducción de Windows Server2008, los componentes de Firewall e IPsec se han fusionado en un solo servicio y se han mejorado las capacidades de este servicio.</span><span class="sxs-lookup"><span data-stu-id="9beb0-104">With the introduction of Windows Server2008, the firewall and IPsec components were merged into one service, and the capabilities of this service were enhanced.</span></span> <span data-ttu-id="9beb0-105">El nuevo servicio de Firewall admite la inspección de estado entrante y saliente.</span><span class="sxs-lookup"><span data-stu-id="9beb0-105">The new firewall service supports incoming and outgoing stateful inspection.</span></span> <span data-ttu-id="9beb0-106">Además, puede configurar reglas de firewall y directivas de IPsec específicas mediante directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="9beb0-106">Also, you can configure specific firewall rules and IPsec policies through group policies.</span></span> <span data-ttu-id="9beb0-107">Para obtener más información sobre el Firewall de Windows en Windows Server2008, consulte <https://go.microsoft.com/fwlink/?LinkId=151980> .</span><span class="sxs-lookup"><span data-stu-id="9beb0-107">For additional information about the Windows firewall in Windows Server2008, see <https://go.microsoft.com/fwlink/?LinkId=151980>.</span></span>

<span data-ttu-id="9beb0-108">El procedimiento siguiente no incluye agregar una excepción para la publicación de ICO y OSD a través de SMB o HTTP/HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9beb0-108">The following procedure does not include adding an exception for ICO and OSD publishing through SMB or HTTP/HTTPS.</span></span> <span data-ttu-id="9beb0-109">Dichas excepciones se agregan automáticamente según el perfil de red y los roles instalados en el Firewall de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9beb0-109">Those exceptions are automatically added based on the network profile and roles installed on the Windows Server 2008 firewall.</span></span>

<span data-ttu-id="9beb0-110">**Nota:**  Si el servidor de administración está configurado para usar RTSP, repita este procedimiento para agregar el `sghwsvr.exe` programa como una excepción.</span><span class="sxs-lookup"><span data-stu-id="9beb0-110">**Note** If the Management Server is configured to use RTSP, repeat this procedure to add the `sghwsvr.exe` program as an exception.</span></span>

<span data-ttu-id="9beb0-111">El servidor de streaming de App-V requiere la excepción del programa `sglwdsptr.exe` para la comunicación de rtsps.</span><span class="sxs-lookup"><span data-stu-id="9beb0-111">The App-V Streaming Server requires the program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="9beb0-112">Un servidor de streaming de App-V que use RTSP para la comunicación también necesita una excepción de programa para `sglwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="9beb0-112">An App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

 

**<span data-ttu-id="9beb0-113">Para configurar Firewall de Windows Server2008 para App-V</span><span class="sxs-lookup"><span data-stu-id="9beb0-113">To configure Windows Server2008 firewall for App-V</span></span>**

1.  <span data-ttu-id="9beb0-114">Abra el **firewall de Windows con** la consola de administración de seguridad avanzada mediante el panel de control o escribiendo `wf.msc` en la línea ejecutar.</span><span class="sxs-lookup"><span data-stu-id="9beb0-114">Open the **Windows Firewall with Advanced Security** management console through the Control Panel or by typing `wf.msc` on the Run line.</span></span>

2.  <span data-ttu-id="9beb0-115">Cree una nueva regla de entrada y seleccione **programa**.</span><span class="sxs-lookup"><span data-stu-id="9beb0-115">Create a new inbound rule, and select **Program**.</span></span>

3.  <span data-ttu-id="9beb0-116">Seleccione la ruta de acceso del programa y vaya a `sghwdsptr.exe` , que se encuentra de forma predeterminada en `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .</span><span class="sxs-lookup"><span data-stu-id="9beb0-116">Select the program path, and browse to `sghwdsptr.exe`, which is located by default at `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

4.  <span data-ttu-id="9beb0-117">Haz clic en **Siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9beb0-117">Click **Next**.</span></span>

5.  <span data-ttu-id="9beb0-118">En la página de **acciones** , seleccione **permitir la conexión**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="9beb0-118">On the **Action** page, select **Allow the connection**, and then click **Next**.</span></span>

6.  <span data-ttu-id="9beb0-119">Seleccione los **perfiles** que desea aplicar a la regla de entrada.</span><span class="sxs-lookup"><span data-stu-id="9beb0-119">Select the appropriate **Profiles** to apply to the inbound rule.</span></span>

7.  <span data-ttu-id="9beb0-120">Proporcione un nombre y una descripción para la regla y haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="9beb0-120">Provide a name and description for the rule, and click **Finish**.</span></span>

## <span data-ttu-id="9beb0-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9beb0-121">Related topics</span></span>


[<span data-ttu-id="9beb0-122">Cómo configurar el Firewall de Windows Server 2003 para App-V</span><span class="sxs-lookup"><span data-stu-id="9beb0-122">How to Configure Windows Server 2003 Firewall for App-V</span></span>](how-to-configure-windows-server-2003-firewall-for-app-v.md)

 

 





