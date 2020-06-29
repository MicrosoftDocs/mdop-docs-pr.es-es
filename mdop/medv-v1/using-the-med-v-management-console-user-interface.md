---
title: Uso de la interfaz de usuario de la consola de administración de MED-V
description: Uso de la interfaz de usuario de la consola de administración de MED-V
author: dansimp
ms.assetid: f42714d7-6f0c-4995-ab31-d4ef0845a22c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22fc98c3edbea48847e1a00369bea21a470e66b7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825850"
---
# <span data-ttu-id="31f05-103">Uso de la interfaz de usuario de la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="31f05-103">Using the MED-V Management Console User Interface</span></span>


<span data-ttu-id="31f05-104">La interfaz de usuario de la consola se divide en las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="31f05-104">The console user interface is divided into the following sections:</span></span>

-   <span data-ttu-id="31f05-105">Los siguientes **botones de administración de MED-V**, que corresponden a los tres módulos:</span><span class="sxs-lookup"><span data-stu-id="31f05-105">The following **MED-V management buttons**, which correspond to the three modules:</span></span>

    -   <span data-ttu-id="31f05-106">**Directiva**: el módulo de **directivas** se usa para definir las áreas de trabajo de MED-V y sus configuraciones y permisos relacionados.</span><span class="sxs-lookup"><span data-stu-id="31f05-106">**Policy**—The **Policy** module is used to define the MED-V workspaces and their related settings and permissions.</span></span>

    -   <span data-ttu-id="31f05-107">**Imágenes**: el módulo **imágenes** se usa para administrar imágenes del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="31f05-107">**Images**—The **Images** module is used to manage MED-V workspace images.</span></span>

    -   <span data-ttu-id="31f05-108">**Informes**: el módulo **informes** se usa para generar y ver informes de áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="31f05-108">**Reports**—The **Reports** module is used for generating and viewing MED-V workspace reports.</span></span>

-   <span data-ttu-id="31f05-109">La **barra de herramientas** muestra los accesos directos relacionados con el botón seleccionado.</span><span class="sxs-lookup"><span data-stu-id="31f05-109">The **toolbar** displays shortcuts relevant to the button selected.</span></span>

-   <span data-ttu-id="31f05-110">El **Panel de información** muestra un módulo correspondiente al botón seleccionado.</span><span class="sxs-lookup"><span data-stu-id="31f05-110">The **display pane** displays a module corresponding to the button that is selected.</span></span>

![](images/medv-ui-console-general.gif)

## <span data-ttu-id="31f05-111">Cómo iniciar sesión en la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="31f05-111">How to Log In to the MED-V Management Console</span></span>


**<span data-ttu-id="31f05-112">Para abrir la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="31f05-112">To open the MED-V management console</span></span>**

-   <span data-ttu-id="31f05-113">En el menú **Inicio** de Windows, seleccione \*\*todos los programas &gt; Administración &gt; \*\*de Med-v Med-v o, en el escritorio, haga doble clic en el icono administración de Med-v.</span><span class="sxs-lookup"><span data-stu-id="31f05-113">On the Windows **Start** menu, select **All Programs &gt; MED-V &gt; MED-V Management**, or on the desktop, double-click the MED-V Management icon.</span></span>

    <span data-ttu-id="31f05-114">Aparece la ventana de **Inicio de sesión de administración de MED-V** .</span><span class="sxs-lookup"><span data-stu-id="31f05-114">The **MED-V Management Login** window appears.</span></span>

<span data-ttu-id="31f05-115">**Nota:**  Por razones de seguridad, el primer usuario que inicie sesión en la consola de administración de MED-V se convertirá en el único usuario de ese equipo que tiene permiso para acceder a la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="31f05-115">**Note** For security reasons, the first user to log in to the MED-V management console will become the only user on that computer allowed to access the management console.</span></span>

 

**<span data-ttu-id="31f05-116">Para iniciar sesión</span><span class="sxs-lookup"><span data-stu-id="31f05-116">To log in</span></span>**

1.  <span data-ttu-id="31f05-117">Escriba sus credenciales de usuario de dominio en el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="31f05-117">Type in your domain user credentials in the following format:</span></span>

    <span data-ttu-id="31f05-118">"dominio \ _name \\user\ _name", "contraseña"</span><span class="sxs-lookup"><span data-stu-id="31f05-118">"domain\_name\\user\_name", "password"</span></span>

    <span data-ttu-id="31f05-119">**Nota:**  Al configurar el servidor, se definen los usuarios con acceso completo y usuarios con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="31f05-119">**Note** When configuring the server, users with full access as well as users with read-only access are defined.</span></span> <span data-ttu-id="31f05-120">Todos los usuarios deben ser usuarios del dominio.</span><span class="sxs-lookup"><span data-stu-id="31f05-120">All users must be domain users.</span></span> <span data-ttu-id="31f05-121">El nombre de usuario y la contraseña del dominio se usan para el inicio de sesión de administración de MED-V.</span><span class="sxs-lookup"><span data-stu-id="31f05-121">The domain user name and password is used for MED-V management login.</span></span>

     

2.  <span data-ttu-id="31f05-122">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="31f05-122">Click **OK**.</span></span>

    <span data-ttu-id="31f05-123">Aparece la consola de **Administración de MED-V** .</span><span class="sxs-lookup"><span data-stu-id="31f05-123">The **MED-V Management** console appears.</span></span>

## <span data-ttu-id="31f05-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31f05-124">Related topics</span></span>


[<span data-ttu-id="31f05-125">Cómo instalar el cliente MED-V y la consola de administración de MED-V</span><span class="sxs-lookup"><span data-stu-id="31f05-125">How to Install MED-V Client and MED-V Management Console</span></span>](how-to-install-med-v-client-and-med-v-management-console.md)

 

 





