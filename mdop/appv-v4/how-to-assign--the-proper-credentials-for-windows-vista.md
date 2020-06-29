---
title: Cómo asignar las credenciales correctas para Windows Vista
description: Cómo asignar las credenciales correctas para Windows Vista
author: dansimp
ms.assetid: cc11d2af-a350-4d16-ba7b-f9c1d89e14b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 111dafea505133f123cf8531a2891a452e725ac2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821370"
---
# <span data-ttu-id="8aca0-103">Cómo asignar las credenciales correctas para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8aca0-103">How to Assign the Proper Credentials for Windows Vista</span></span>


<span data-ttu-id="8aca0-104">Use el siguiente procedimiento para configurar el cliente de escritorio de App-V para obtener las credenciales de vista correctas.</span><span class="sxs-lookup"><span data-stu-id="8aca0-104">Use the following procedure to configure the App-V Desktop Client for proper WindowsVista credentials.</span></span>

<span data-ttu-id="8aca0-105">**Nota:**  Este procedimiento debe completarse en todos los equipos que no pertenezcan al dominio.</span><span class="sxs-lookup"><span data-stu-id="8aca0-105">**Note** This procedure must be completed on each non-domain joined computer.</span></span> <span data-ttu-id="8aca0-106">En función del número de equipos que no estén conectados a un dominio en su entorno, podría ser una operación muy tediosa.</span><span class="sxs-lookup"><span data-stu-id="8aca0-106">Depending on the number of non-domain joined computers in your environment, this could be a very tedious operation.</span></span> <span data-ttu-id="8aca0-107">Puede usar scripts y la interfaz de línea de comandos de Credential Manager para ayudar a los administradores a automatizar este proceso.</span><span class="sxs-lookup"><span data-stu-id="8aca0-107">You can use scripts and the command-line interface for Credential Manager to help administrators automate this process.</span></span>

 

**<span data-ttu-id="8aca0-108">Para asignar las credenciales correctas para los clientes de App-V que ejecutan Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8aca0-108">To assign the proper credentials for App-V clients running Windows Vista</span></span>**

1.  <span data-ttu-id="8aca0-109">Con privilegios de administrador en el cliente de escritorio de App-V que ejecuta Windows Vista, abra el panel de control de **cuentas de usuario** (panel de control clásico).</span><span class="sxs-lookup"><span data-stu-id="8aca0-109">With administrator privileges on the App-V Desktop Client running Windows Vista, open the **User Accounts** control panel (Classic Control Panel).</span></span>

2.  <span data-ttu-id="8aca0-110">Seleccione **administrar las contraseñas de red** desde **cuentas de usuario** en el panel tareas de la izquierda.</span><span class="sxs-lookup"><span data-stu-id="8aca0-110">Select **Manage your network passwords** from **User Accounts** in the left tasks pane.</span></span>

3.  <span data-ttu-id="8aca0-111">Seleccione **Agregar** en la pantalla **nombres de usuarios y contraseñas almacenados** .</span><span class="sxs-lookup"><span data-stu-id="8aca0-111">Select **Add** on the **Stored User Names and Passwords** screen.</span></span>

4.  <span data-ttu-id="8aca0-112">En la pantalla **propiedades de credenciales almacenadas** , proporcione la información de la infraestructura de App-V:</span><span class="sxs-lookup"><span data-stu-id="8aca0-112">On the **Stored Credential Properties** screen, provide the information for the App-V infrastructure:</span></span>

    1.  <span data-ttu-id="8aca0-113">**Inicie sesión en:** Nombre externo del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="8aca0-113">**Log on to:** External name of the publishing server.</span></span>

    2.  <span data-ttu-id="8aca0-114">**Nombre de usuario:** Nombre de usuario del usuario externo en el formulario Domain\\Username.</span><span class="sxs-lookup"><span data-stu-id="8aca0-114">**User name:** User name for the external user in the form Domain\\Username.</span></span>

    3.  <span data-ttu-id="8aca0-115">**Contraseña:** Contraseña de la cuenta de usuario especificada en el campo **nombre de usuario** .</span><span class="sxs-lookup"><span data-stu-id="8aca0-115">**Password:** Password for the user account entered in the **User name** field.</span></span>

    4.  <span data-ttu-id="8aca0-116">Deje seleccionado **tipo de credencial** y haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="8aca0-116">Leave **Credential Type** selected, and click **OK**.</span></span>

5.  <span data-ttu-id="8aca0-117">Haz clic en **Cerrar**.</span><span class="sxs-lookup"><span data-stu-id="8aca0-117">Click **Close**.</span></span> <span data-ttu-id="8aca0-118">Las credenciales se almacenan en el almacén de credenciales para la autenticación correcta en la infraestructura de App-V.</span><span class="sxs-lookup"><span data-stu-id="8aca0-118">The credentials are stored in the credential store for proper authentication to the App-V infrastructure.</span></span>

## <span data-ttu-id="8aca0-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8aca0-119">Related topics</span></span>


[<span data-ttu-id="8aca0-120">Clientes unidos a un dominio y no unidos a un dominio</span><span class="sxs-lookup"><span data-stu-id="8aca0-120">Domain-Joined and Non-Domain-Joined Clients</span></span>](domain-joined-and-non-domain-joined-clients.md)

[<span data-ttu-id="8aca0-121">Cómo asignar las credenciales correctas para Windows XP</span><span class="sxs-lookup"><span data-stu-id="8aca0-121">How to Assign the Proper Credentials for Windows XP</span></span>](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





