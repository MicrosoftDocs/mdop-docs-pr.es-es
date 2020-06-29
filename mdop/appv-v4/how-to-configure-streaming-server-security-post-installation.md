---
title: Cómo configurar la postinstalación de seguridad del servidor de streaming
description: Cómo configurar la postinstalación de seguridad del servidor de streaming
author: dansimp
ms.assetid: 9bde3677-d1aa-4dcc-904e-bb49a268d748
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1945b38da5dd50c0bd2fb0c741bd92012e78586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817901"
---
# <span data-ttu-id="c1413-103">Cómo configurar la postinstalación de seguridad del servidor de streaming</span><span class="sxs-lookup"><span data-stu-id="c1413-103">How to Configure Streaming Server Security Post-Installation</span></span>


<span data-ttu-id="c1413-104">Configure el servidor de streaming de App-V para mejorar la seguridad a través del registro.</span><span class="sxs-lookup"><span data-stu-id="c1413-104">Configure the App-V Streaming Server for enhanced security through the registry.</span></span> <span data-ttu-id="c1413-105">Al igual que con el servidor de administración de App-V, se debe aprovisionar correctamente un certificado con el identificador de EKU correcto para la autenticación del servidor antes de completar el siguiente procedimiento posterior a la instalación.</span><span class="sxs-lookup"><span data-stu-id="c1413-105">As with the App-V Management Server, a certificate must be correctly provisioned with the correct EKU identifier for Server Authentication before you complete the following post-installation procedure.</span></span>

**<span data-ttu-id="c1413-106">Para configurar la seguridad del servidor de streaming después de la instalación</span><span class="sxs-lookup"><span data-stu-id="c1413-106">To configure Streaming Server security post-installation</span></span>**

1.  <span data-ttu-id="c1413-107">Cree una consola MMC, agregue el complemento **certificados** y seleccione almacén de **certificados de la máquina local**.</span><span class="sxs-lookup"><span data-stu-id="c1413-107">Create an MMC, add the **Certificates** snap-in, and select **Local Machine certificate store**.</span></span>

2.  <span data-ttu-id="c1413-108">Abra los certificados **personales** para el equipo y abra el certificado suministrado para App-V.</span><span class="sxs-lookup"><span data-stu-id="c1413-108">Open the **Personal** certificates for the computer, and open the certificate provisioned for App-V.</span></span>

3.  <span data-ttu-id="c1413-109">En la pestaña **detalles** , desplácese hasta la huella digital y copie el hash en el panel de detalles.</span><span class="sxs-lookup"><span data-stu-id="c1413-109">On the **Details** tab, scroll down to the thumbprint and copy the hash in the details pane.</span></span>

4.  <span data-ttu-id="c1413-110">Abra el editor del registro y vaya a `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server` .</span><span class="sxs-lookup"><span data-stu-id="c1413-110">Open the registry editor, and navigate to `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server`.</span></span>

5.  <span data-ttu-id="c1413-111">Edite el `X509CertHash` valor, pegue el hash de la huella digital en el campo de valor y quite todos los espacios.</span><span class="sxs-lookup"><span data-stu-id="c1413-111">Edit the `X509CertHash` value, paste the thumbprint hash in the value field, and remove all spaces.</span></span> <span data-ttu-id="c1413-112">Haga clic en **Aceptar** para aceptar la edición.</span><span class="sxs-lookup"><span data-stu-id="c1413-112">Click **OK** to accept the edit.</span></span>

6.  <span data-ttu-id="c1413-113">En el editor del registro, vaya a `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts` .</span><span class="sxs-lookup"><span data-stu-id="c1413-113">In the registry editor, navigate to `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts`.</span></span>

7.  <span data-ttu-id="c1413-114">Cree un nuevo valor de **DWORD** denominado "322" y, a continuación, escriba el valor decimal como 322 o el valor hexadecimal como 142.</span><span class="sxs-lookup"><span data-stu-id="c1413-114">Create a new **DWORD** value named "322," and then enter the decimal value as 322 or the hexadecimal value as 142.</span></span>

8.  <span data-ttu-id="c1413-115">Reinicie el servicio de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="c1413-115">Restart the streaming service.</span></span>

## <span data-ttu-id="c1413-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c1413-116">Related topics</span></span>


[<span data-ttu-id="c1413-117">Cómo configurar la postinstalación de seguridad del servidor de administración</span><span class="sxs-lookup"><span data-stu-id="c1413-117">How to Configure Management Server Security Post-Installation</span></span>](how-to-configure-management-server-security-post-installation.md)

[<span data-ttu-id="c1413-118">Solución de problemas de permisos de certificado</span><span class="sxs-lookup"><span data-stu-id="c1413-118">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)

 

 





