---
title: Cómo asignar las credenciales correctas para Windows XP
description: Cómo asignar las credenciales correctas para Windows XP
author: dansimp
ms.assetid: cddbd556-d8f9-4981-a947-6e8e3f552b70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 81581b75a9b7d5ce35e1c50fd01e0b7bbd3f7ef5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819321"
---
# <span data-ttu-id="7f174-103">Cómo asignar las credenciales correctas para Windows XP</span><span class="sxs-lookup"><span data-stu-id="7f174-103">How to Assign the Proper Credentials for Windows XP</span></span>


<span data-ttu-id="7f174-104">Use el siguiente procedimiento para configurar el cliente de escritorio de App-V para obtener las credenciales de WindowsXP apropiadas.</span><span class="sxs-lookup"><span data-stu-id="7f174-104">Use the following procedure to configure the App-V Desktop Client for proper WindowsXP credentials.</span></span>

<span data-ttu-id="7f174-105">**Nota:**  Después de finalizar este procedimiento, el cliente que no está unido a un dominio puede realizar una actualización de publicación sin unirse a un dominio.</span><span class="sxs-lookup"><span data-stu-id="7f174-105">**Note** After finishing this procedure, the non-domain joined client can perform a publishing refresh without being joined to a domain.</span></span>

 

**<span data-ttu-id="7f174-106">Para asignar las credenciales correctas para los clientes de App-V que ejecutan WindowsXP</span><span class="sxs-lookup"><span data-stu-id="7f174-106">To assign the proper credentials for App-V clients running WindowsXP</span></span>**

1.  <span data-ttu-id="7f174-107">Con privilegios de administrador en el cliente de App-V que ejecuta WindowsXP, abra el panel de control de **cuentas de usuario** (panel de control clásico).</span><span class="sxs-lookup"><span data-stu-id="7f174-107">With administrator privileges on the App-V Client running WindowsXP, open the **User Accounts** control panel (Classic Control Panel).</span></span>

2.  <span data-ttu-id="7f174-108">Haga clic en la **pestaña Opciones avanzadas**y seleccione **Administrar contraseñas**.</span><span class="sxs-lookup"><span data-stu-id="7f174-108">Click the **Advanced Tab**, and select **Manage Passwords**.</span></span>

3.  <span data-ttu-id="7f174-109">En la pantalla **nombres de usuarios y contraseñas almacenados** , haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="7f174-109">On the **Stored User Names and Passwords** screen, click **Add**.</span></span>

4.  <span data-ttu-id="7f174-110">En la pantalla **propiedades de información de inicio de sesión** , rellene los siguientes campos con información de la infraestructura de App-V:</span><span class="sxs-lookup"><span data-stu-id="7f174-110">On the **Logon Information Properties** screen, fill out the following fields with information from the App-V infrastructure:</span></span>

    1.  <span data-ttu-id="7f174-111">**Server:** Nombre del nombre externo del servidor de publicación.</span><span class="sxs-lookup"><span data-stu-id="7f174-111">**Server:** Name of publishing server external name.</span></span>

    2.  <span data-ttu-id="7f174-112">**Nombre de usuario:** Nombre de usuario para usuario externo en el formulario Domain\\username.</span><span class="sxs-lookup"><span data-stu-id="7f174-112">**User name:** User name for external user in the form Domain\\username.</span></span>

    3.  <span data-ttu-id="7f174-113">**Contraseña:** Contraseña de la cuenta de usuario especificada en el campo **nombre de usuario** .</span><span class="sxs-lookup"><span data-stu-id="7f174-113">**Password:** Password for the user account entered in the **User name** field.</span></span>

5.  <span data-ttu-id="7f174-114">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="7f174-114">Click **OK**.</span></span> <span data-ttu-id="7f174-115">Las credenciales se almacenarán en el cliente.</span><span class="sxs-lookup"><span data-stu-id="7f174-115">The credentials will be stored on the client.</span></span>

## <span data-ttu-id="7f174-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7f174-116">Related topics</span></span>


[<span data-ttu-id="7f174-117">Clientes unidos a un dominio y no unidos a un dominio</span><span class="sxs-lookup"><span data-stu-id="7f174-117">Domain-Joined and Non-Domain-Joined Clients</span></span>](domain-joined-and-non-domain-joined-clients.md)

[<span data-ttu-id="7f174-118">Cómo asignar las credenciales correctas para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f174-118">How to Assign the Proper Credentials for Windows Vista</span></span>](how-to-assign--the-proper-credentials-for-windows-vista.md)

 

 





