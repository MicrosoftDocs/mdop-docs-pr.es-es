---
title: Cómo configurar el Firewall de Windows Server 2003 para App-V
description: Cómo configurar el Firewall de Windows Server 2003 para App-V
author: dansimp
ms.assetid: 2c0e80f8-41e9-4164-ac83-b23b132b489a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af75479504b454851ee2efc7ca2638d2daf45053
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817730"
---
# <span data-ttu-id="5399e-103">Cómo configurar el Firewall de Windows Server 2003 para App-V</span><span class="sxs-lookup"><span data-stu-id="5399e-103">How to Configure Windows Server 2003 Firewall for App-V</span></span>


<span data-ttu-id="5399e-104">Use el siguiente procedimiento para configurar el Firewall de WindowsServer 2003 para App-V.</span><span class="sxs-lookup"><span data-stu-id="5399e-104">Use the following procedure to configure the WindowsServer 2003 firewall for App-V.</span></span>

**<span data-ttu-id="5399e-105">Para configurar Firewall de WindowsServer 2003 para App-V</span><span class="sxs-lookup"><span data-stu-id="5399e-105">To configure WindowsServer 2003 firewall for App-V</span></span>**

1.  <span data-ttu-id="5399e-106">En el **Panel de control**, abra el Firewall de **Windows**.</span><span class="sxs-lookup"><span data-stu-id="5399e-106">In **Control Panel**, open the **Windows Firewall**.</span></span>

    <span data-ttu-id="5399e-107">**Nota:**  Si el servidor no se ha configurado para ejecutar el servicio de Firewall antes de este paso, se le pedirá que inicie el servicio de Firewall.</span><span class="sxs-lookup"><span data-stu-id="5399e-107">**Note** If the server has not been configured to run the firewall service before this step, you will be prompted to start the firewall service.</span></span>

     

2.  <span data-ttu-id="5399e-108">Si los archivos ICO y OSD se publican a través de SMB, asegúrese de que el **uso compartido de impresoras y archivos** está habilitado en la pestaña **excepciones** .</span><span class="sxs-lookup"><span data-stu-id="5399e-108">If ICO and OSD files are published through SMB, ensure that **File and Printer Sharing** is enabled on the **Exceptions** tab.</span></span>

    <span data-ttu-id="5399e-109">**Nota:**  Si los archivos ICO y OSD se publican a través de HTTP/HTTPS en el servidor de administración, es posible que tenga que agregar una excepción para HTTP o HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5399e-109">**Note** If ICO and OSD files are published through HTTP/HTTPS on the Management Server, you might need to add an exception for HTTP or HTTPS.</span></span> <span data-ttu-id="5399e-110">Si el servidor IIS que hospeda los archivos ICO y OSD está alojado en un equipo independiente del servidor de administración, debe agregar la excepción a ese equipo.</span><span class="sxs-lookup"><span data-stu-id="5399e-110">If the IIS server hosting the ICO and OSD files is hosted on a computer separate from the Management Server, you need to add the exception to that computer.</span></span> <span data-ttu-id="5399e-111">Para maximizar el rendimiento, le recomendamos que aloje los archivos ICO y OSD en un servidor independiente del servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="5399e-111">To maximize performance, it is recommended that you host the ICO and OSD files on a separate server from the Management Server.</span></span>

     

3.  <span data-ttu-id="5399e-112">Agregue una excepción de programa para `sghwdsptr.exe` , que es el ejecutable del servicio servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="5399e-112">Add a program exception for `sghwdsptr.exe`, which is the Management Server service executable.</span></span> <span data-ttu-id="5399e-113">La ruta de acceso predeterminada para este archivo ejecutable es `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .</span><span class="sxs-lookup"><span data-stu-id="5399e-113">The default path to this executable is `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

    <span data-ttu-id="5399e-114">**Nota:**  Si el servidor de administración usa RTSP para la comunicación, también debe agregar una excepción de programa para `sghwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="5399e-114">**Note** If the Management Server uses RTSP for communication, you must also add a program exception for `sghwsvr.exe`.</span></span>

    <span data-ttu-id="5399e-115">El servidor de streaming de App-V requiere una excepción `sglwdsptr.exe` de programa para la comunicación de rtsps.</span><span class="sxs-lookup"><span data-stu-id="5399e-115">The App-V Streaming Server requires a program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="5399e-116">El servidor de streaming de App-V que usa RTSP para la comunicación también necesita una excepción de programa para `sglwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="5399e-116">The App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

     

4.  <span data-ttu-id="5399e-117">Asegúrese de que se ha configurado el ámbito adecuado para cada excepción.</span><span class="sxs-lookup"><span data-stu-id="5399e-117">Ensure that the proper scope is configured for each exception.</span></span> <span data-ttu-id="5399e-118">Para reducir el riesgo, quite cualquier equipo y limite estrictamente las direcciones IP a las que responderá el servidor.</span><span class="sxs-lookup"><span data-stu-id="5399e-118">To reduce risk, remove any computer and strictly limit the IP addresses to which the server will respond.</span></span>

## <span data-ttu-id="5399e-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5399e-119">Related topics</span></span>


[<span data-ttu-id="5399e-120">Cómo configurar el Firewall de Windows Server 2008 para App-V</span><span class="sxs-lookup"><span data-stu-id="5399e-120">How to Configure Windows Server 2008 Firewall for App-V</span></span>](how-to-configure-windows-server-2008-firewall-for-app-v.md)

 

 





