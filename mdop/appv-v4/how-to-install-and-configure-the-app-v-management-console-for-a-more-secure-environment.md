---
title: Cómo instalar y configurar la consola de administración de App-V para un entorno más seguro
description: Cómo instalar y configurar la consola de administración de App-V para un entorno más seguro
author: dansimp
ms.assetid: 9d89ef09-cdbf-48fc-99da-b24fc987ef8f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9887787d1e203410b5517439d897260305d7526e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817371"
---
# <span data-ttu-id="3d74b-103">Cómo instalar y configurar la consola de administración de App-V para un entorno más seguro</span><span class="sxs-lookup"><span data-stu-id="3d74b-103">How to Install and Configure the App-V Management Console for a More Secure Environment</span></span>


<span data-ttu-id="3d74b-104">La instalación predeterminada de la consola de administración de App-V incluye compatibilidad con las comunicaciones seguras.</span><span class="sxs-lookup"><span data-stu-id="3d74b-104">The default installation of the App-V Management Console includes support for secure communications.</span></span> <span data-ttu-id="3d74b-105">Cada consola de administración se configura en función de la conexión cuando la consola se inicia por primera vez o cuando se conecta a un servicio de administración web de App-V adicional.</span><span class="sxs-lookup"><span data-stu-id="3d74b-105">Each Management Console is configured on a per-connection basis when the console is started for the first time or when connecting to an additional App-V Web Management Service.</span></span> <span data-ttu-id="3d74b-106">La configuración predeterminada usa SSL sobre el puerto TCP 443.</span><span class="sxs-lookup"><span data-stu-id="3d74b-106">The default configuration uses SSL over TCP port 443.</span></span> <span data-ttu-id="3d74b-107">Puede cambiar el número de puerto si el número de puerto se modificó en el servidor.</span><span class="sxs-lookup"><span data-stu-id="3d74b-107">You can change the port number if the port number was modified on the server.</span></span> <span data-ttu-id="3d74b-108">Puede usar el siguiente procedimiento para conectarse a un servicio de administración web de App-V mediante una conexión segura.</span><span class="sxs-lookup"><span data-stu-id="3d74b-108">You can use the following procedure to connect to an App-V Web Management Service by using a secure connection.</span></span>

**<span data-ttu-id="3d74b-109">Cómo conectarse a un servicio de administración de App-V mediante una conexión SSL</span><span class="sxs-lookup"><span data-stu-id="3d74b-109">How to Connect to an App-V Management Service by Using an SSL Connection</span></span>**

1.  <span data-ttu-id="3d74b-110">Inicie la consola de administración de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="3d74b-110">Start the Application Virtualization Management Console.</span></span>

2.  <span data-ttu-id="3d74b-111">Haga clic en **Configurar conexión** en el panel acciones de la consola.</span><span class="sxs-lookup"><span data-stu-id="3d74b-111">Click **Configure Connection** in the actions pane of the console.</span></span>

3.  <span data-ttu-id="3d74b-112">Escriba el **nombre de host del servicio Web**y asegúrese de que la selección de **Usar conexión segura** está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="3d74b-112">Type the **Web Service Host Name**, and ensure that **Use Secure Connection** is selected.</span></span>

    <span data-ttu-id="3d74b-113">**Importante**  El nombre proporcionado en el nombre de host de servicio Web debe coincidir con el nombre común del certificado o la conexión fallará.</span><span class="sxs-lookup"><span data-stu-id="3d74b-113">**Important** The name provided in the Web Service Host Name must match the common name on the certificate, or the connection will fail.</span></span>

     

4.  <span data-ttu-id="3d74b-114">Seleccione las credenciales de inicio de sesión apropiadas y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="3d74b-114">Select the appropriate login credentials, and click **OK**.</span></span>

## <span data-ttu-id="3d74b-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3d74b-115">Related topics</span></span>


[<span data-ttu-id="3d74b-116">Configuración de certificados para admitir el servicio de administración web de App-V</span><span class="sxs-lookup"><span data-stu-id="3d74b-116">Configuring Certificates to Support the App-V Web Management Service</span></span>](configuring-certificates-to-support-the-app-v-web-management-service.md)

 

 





