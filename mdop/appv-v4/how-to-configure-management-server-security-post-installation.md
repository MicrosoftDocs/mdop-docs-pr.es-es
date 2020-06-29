---
title: Cómo configurar la postinstalación de seguridad del servidor de administración
description: Cómo configurar la postinstalación de seguridad del servidor de administración
author: dansimp
ms.assetid: 71979fa6-3d0b-4a8b-994e-cb728d013090
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 521e72ead78055a7d3261664ccb75d454c22e622
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817940"
---
# <span data-ttu-id="cf188-103">Cómo configurar la postinstalación de seguridad del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="cf188-103">How to Configure Management Server Security Post-Installation</span></span>


<span data-ttu-id="cf188-104">Use la consola de administración de App-V para agregar el certificado y configurar el servidor de administración de App-V para mejorar la seguridad.</span><span class="sxs-lookup"><span data-stu-id="cf188-104">Use the App-V Management Console to add the certificate and configure the App-V Management Server for enhanced security.</span></span> <span data-ttu-id="cf188-105">Puede usar el siguiente procedimiento para configurar la seguridad después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="cf188-105">You can use the following procedure to configure security post-installation.</span></span>

**<span data-ttu-id="cf188-106">Para configurar la seguridad del servidor de administración después de la instalación</span><span class="sxs-lookup"><span data-stu-id="cf188-106">To configure Management Server security post-installation</span></span>**

1.  <span data-ttu-id="cf188-107">Abra la consola de administración de App-V y conéctese al **servicio de administración** con privilegios de administrador de App-v.</span><span class="sxs-lookup"><span data-stu-id="cf188-107">Open the App-V Management Console, and connect to the **Management Service** with App-V administrator privileges.</span></span>

2.  <span data-ttu-id="cf188-108">Expanda el servidor, expanda **grupos de servidores**y, a continuación, seleccione el grupo de servidores adecuado con el que se registró el servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="cf188-108">Expand the server, expand **Server Groups**, and then select the appropriate server group with which the Management Server was registered.</span></span>

3.  <span data-ttu-id="cf188-109">Haga clic con el botón secundario en el objeto servidor de administración y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="cf188-109">Right-click the Management Server object, and select **Properties**.</span></span>

4.  <span data-ttu-id="cf188-110">En la pestaña **puertos** , haga clic en **certificado de servidor** y complete el Asistente para seleccionar el certificado que se aprovisionó correctamente.</span><span class="sxs-lookup"><span data-stu-id="cf188-110">On the **Ports** tab, click **Server Certificate** and complete the wizard to select the properly provisioned certificate.</span></span>

    <span data-ttu-id="cf188-111">**Nota:**  Si no se muestran certificados en el asistente, significa que no se ha aprovisionado un certificado o que el certificado cumple los requisitos de App-V.</span><span class="sxs-lookup"><span data-stu-id="cf188-111">**Note** If no certificates are displayed in the wizard, a certificate has not been provisioned or the certificate does meet the requirements of App-V.</span></span>

     

5.  <span data-ttu-id="cf188-112">Haga clic en **siguiente** para continuar con la página **Asistente para certificados** .</span><span class="sxs-lookup"><span data-stu-id="cf188-112">Click **Next** to continue on to the **Welcome To Certificate Wizard** page.</span></span>

6.  <span data-ttu-id="cf188-113">Seleccione el certificado correcto en la pantalla **certificados disponibles** .</span><span class="sxs-lookup"><span data-stu-id="cf188-113">Select the correct certificate in the **Available Certificates** screen.</span></span>

7.  <span data-ttu-id="cf188-114">Haz clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="cf188-114">Click **Finish**.</span></span>

8.  <span data-ttu-id="cf188-115">Después de completar el asistente, desactive **RTSP** como puerto de escucha disponible.</span><span class="sxs-lookup"><span data-stu-id="cf188-115">After completing the wizard, clear **RTSP** as an available listening port.</span></span> <span data-ttu-id="cf188-116">Esto evita que se realicen conexiones a través de un canal de comunicación no seguro.</span><span class="sxs-lookup"><span data-stu-id="cf188-116">This prevents connections from being made over a non-secure communication channel.</span></span>

9.  <span data-ttu-id="cf188-117">Haga clic en **aplicar**y reinicie el servicio **servidor de aplicaciones virtual de Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="cf188-117">Click **Apply**, and restart the **Microsoft Virtual Application Server** service.</span></span> <span data-ttu-id="cf188-118">Use el complemento MMC del servicio para realizar esta tarea.</span><span class="sxs-lookup"><span data-stu-id="cf188-118">Use the service’s MMC snap-in to accomplish this task.</span></span>

## <span data-ttu-id="cf188-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf188-119">Related topics</span></span>


[<span data-ttu-id="cf188-120">Cómo configurar la postinstalación de seguridad del servidor de streaming</span><span class="sxs-lookup"><span data-stu-id="cf188-120">How to Configure Streaming Server Security Post-Installation</span></span>](how-to-configure-streaming-server-security-post-installation.md)

[<span data-ttu-id="cf188-121">Solución de problemas de permisos de certificado</span><span class="sxs-lookup"><span data-stu-id="cf188-121">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)

 

 





