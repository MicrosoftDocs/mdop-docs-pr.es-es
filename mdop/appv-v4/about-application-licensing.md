---
title: Acerca de las licencias de aplicaciones
description: Acerca de las licencias de aplicaciones
author: dansimp
ms.assetid: 6b487641-1627-4e91-b829-04f001008176
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546bc630b95fe52f960c7bdfb771d3e2561f9318
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820100"
---
# <span data-ttu-id="0968a-103">Acerca de las licencias de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="0968a-103">About Application Licensing</span></span>


<span data-ttu-id="0968a-104">Puede administrar las licencias de aplicación directamente desde la consola de administración de Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="0968a-104">You can manage application licenses directly from the Application Virtualization Server Management Console.</span></span>

## <span data-ttu-id="0968a-105">Tipos de licencia</span><span class="sxs-lookup"><span data-stu-id="0968a-105">License Types</span></span>


<span data-ttu-id="0968a-106">El sistema de virtualización de System Center Application es compatible actualmente con los siguientes tipos de licencias:</span><span class="sxs-lookup"><span data-stu-id="0968a-106">The System Center Application Virtualization System currently supports the following license types:</span></span>

-   <span data-ttu-id="0968a-107">**Licencia ilimitada**: permite el acceso a la aplicación por parte de cualquier número de usuarios simultáneos.</span><span class="sxs-lookup"><span data-stu-id="0968a-107">**Unlimited License**—Allows access to the application by any number of simultaneous users.</span></span> <span data-ttu-id="0968a-108">Este método de licencias es adecuado cuando desea asociar una licencia de toda la empresa con una aplicación.</span><span class="sxs-lookup"><span data-stu-id="0968a-108">This method of licensing is appropriate when you want to associate an enterprise-wide license with an application.</span></span>

-   <span data-ttu-id="0968a-109">**Licencia concurrente**: le permite definir la cantidad máxima de usuarios simultáneos que pueden usar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0968a-109">**Concurrent License**—Enables you to define the maximum number of concurrent users who are allowed to use the application.</span></span>

-   <span data-ttu-id="0968a-110">**Licencia con nombre**: le permite asignar una licencia a un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="0968a-110">**Named License**—Enables you to assign a license to an individual user.</span></span> <span data-ttu-id="0968a-111">Una licencia con nombre se puede usar para asegurarse de que un usuario determinado siempre pueda ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0968a-111">A named license can be used to ensure that a particular user will always be able to run the application.</span></span>

<span data-ttu-id="0968a-112">Puede combinar licencias simultáneas y con nombre para la misma aplicación.</span><span class="sxs-lookup"><span data-stu-id="0968a-112">You can combine concurrent and named licenses for the same application.</span></span>

<span data-ttu-id="0968a-113">La licencia está deshabilitada de forma predeterminada, pero puede habilitarla desde la pestaña **canalización del proveedor** del cuadro de diálogo **propiedades del proveedor** .</span><span class="sxs-lookup"><span data-stu-id="0968a-113">Licensing is disabled by default, but you can enable it from the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span> <span data-ttu-id="0968a-114">Para obtener más información sobre cómo habilitar y deshabilitar licencias, consulte [Cómo configurar o deshabilitar licencias de aplicaciones](how-to-set-up-or-disable-application-licensing.md).</span><span class="sxs-lookup"><span data-stu-id="0968a-114">For details about enabling and disabling licensing, see [How to Set Up or Disable Application Licensing](how-to-set-up-or-disable-application-licensing.md).</span></span>

## <span data-ttu-id="0968a-115">Directivas de proveedor</span><span class="sxs-lookup"><span data-stu-id="0968a-115">Provider Policies</span></span>


<span data-ttu-id="0968a-116">Las directivas de proveedor se han desarrollado para el modelo de proveedor de servicios de aplicaciones (ASP).</span><span class="sxs-lookup"><span data-stu-id="0968a-116">Provider policies were developed for the Application Service Provider (ASP) model.</span></span> <span data-ttu-id="0968a-117">En este modelo, un único ASP puede hospedar un único sistema de virtualización de aplicaciones para varios clientes, en el que cada cliente debe permanecer aislado.</span><span class="sxs-lookup"><span data-stu-id="0968a-117">In this model, a single ASP can host a single Application Virtualization System for multiple clients, where each client needs to remain isolated.</span></span> <span data-ttu-id="0968a-118">Los clientes pueden tener muy diversos requisitos, por ejemplo, un cliente puede requerir autenticación, mientras que otro no.</span><span class="sxs-lookup"><span data-stu-id="0968a-118">Clients might have dramatically different requirements—for example, one client might require authentication while another does not.</span></span> <span data-ttu-id="0968a-119">Puede usar directivas de proveedor para asociar permisos con clientes para que solo los usuarios autorizados puedan tener acceso a cada aplicación virtual o paquete de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="0968a-119">You can use provider policies to associate permissions with clients so that only the approved users can access each virtual application or virtual application package.</span></span>

<span data-ttu-id="0968a-120">Para el cliente empresarial, puede usar esta característica cuando tenga requisitos de licencia estrictos para una o más aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0968a-120">For the enterprise customer, you can use this feature when you have strict licensing requirements for one or more applications.</span></span> <span data-ttu-id="0968a-121">En esta situación, el componente de licencias está deshabilitado en la pestaña **canalización del proveedor** del cuadro de diálogo **propiedades del proveedor** .</span><span class="sxs-lookup"><span data-stu-id="0968a-121">Under this situation, the licensing component is disabled on the **Provider Pipeline** tab of the **Provider Properties** dialog.</span></span>

<span data-ttu-id="0968a-122">La ficha **proveedor de proveedores** también tiene casillas para habilitar la autenticación, autorización (**exigir permisos de acceso a la configuración**) y medición (**información sobre el uso de registros**).</span><span class="sxs-lookup"><span data-stu-id="0968a-122">The **Provider Pipeline** tab also has check boxes to enable authentication, authorization (**Enforce Access Permission Settings**), and metering (**Log Usage Information**).</span></span> <span data-ttu-id="0968a-123">Si su configuración tiene requisitos especiales, puede escribir sus propios componentes de canalización y agregarlos al sistema haciendo clic en el botón **avanzadas** .</span><span class="sxs-lookup"><span data-stu-id="0968a-123">If your configuration has special requirements, you can write your own pipeline components and add them to the system by clicking the **Advanced** button.</span></span>

## <span data-ttu-id="0968a-124">Autoridades de cuenta</span><span class="sxs-lookup"><span data-stu-id="0968a-124">Account Authorities</span></span>


<span data-ttu-id="0968a-125">La autoridad de cuentas es el dominio en el que está instalado el servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="0968a-125">The account authority is the domain in which the Application Virtualization Server is installed.</span></span> <span data-ttu-id="0968a-126">A medida que avance por la instalación del servidor, se le pedirá que proporcione un nombre de dominio; el dominio en el que está instalado el equipo se detecta y se usa de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="0968a-126">As you proceed through the server installation, you are prompted to supply a domain name; the domain in which the computer is installed is detected and used by default.</span></span> <span data-ttu-id="0968a-127">Cuando los usuarios intentan iniciar sesión en el sistema, se les pide sus credenciales para poder acceder a ese dominio.</span><span class="sxs-lookup"><span data-stu-id="0968a-127">When users attempt to log in to the system, they are prompted for their credentials before they can access that domain.</span></span>

<span data-ttu-id="0968a-128">El sistema de virtualización de aplicaciones admite varios dominios.</span><span class="sxs-lookup"><span data-stu-id="0968a-128">The Application Virtualization System supports multiple domains.</span></span> <span data-ttu-id="0968a-129">Puede conceder acceso a la aplicación a grupos de usuarios en otros dominios si se establece una relación de confianza entre dominios.</span><span class="sxs-lookup"><span data-stu-id="0968a-129">You can grant application access to user groups in other domains if a trust relationship is established between domains.</span></span> <span data-ttu-id="0968a-130">Los usuarios deben proporcionar credenciales reconocidas por cada dominio.</span><span class="sxs-lookup"><span data-stu-id="0968a-130">Users must supply credentials that are recognized by each domain.</span></span>

<span data-ttu-id="0968a-131">En la consola de administración de Application Virtualization Server, puede cambiar el dominio principal (autoridad de cuentas) y las credenciales que se usan para obtener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="0968a-131">In the Application Virtualization Server Management Console, you can change the primary domain (account authority) and the credentials that are used to access it.</span></span>

## <span data-ttu-id="0968a-132">Autenticación</span><span class="sxs-lookup"><span data-stu-id="0968a-132">Authentication</span></span>


<span data-ttu-id="0968a-133">La autenticación es el mecanismo que se usa para confirmar la identidad de un usuario.</span><span class="sxs-lookup"><span data-stu-id="0968a-133">Authentication is the mechanism used to confirm a user's identity.</span></span> <span data-ttu-id="0968a-134">Cualquier usuario con un nombre de usuario y contraseña reconocidos tiene acceso.</span><span class="sxs-lookup"><span data-stu-id="0968a-134">Any user with a recognized user name and password has access.</span></span>

<span data-ttu-id="0968a-135">En el sistema de virtualización de aplicaciones, puede habilitar o deshabilitar la autenticación mediante una casilla de verificación en la pestaña **proveedor de canalizaciones** . De forma predeterminada, la autenticación de Windows está habilitada.</span><span class="sxs-lookup"><span data-stu-id="0968a-135">In the Application Virtualization System, you can enable or disable authentication through a check box on the **Provider Pipeline** tab. By default, Windows Authentication is enabled.</span></span>

## <span data-ttu-id="0968a-136">Authorization</span><span class="sxs-lookup"><span data-stu-id="0968a-136">Authorization</span></span>


<span data-ttu-id="0968a-137">La autorización es el proceso que se usa para confirmar la identidad de un usuario.</span><span class="sxs-lookup"><span data-stu-id="0968a-137">Authorization is the process used to confirm a user’s identity.</span></span> <span data-ttu-id="0968a-138">Después de confirmar la identidad del usuario, el sistema determina si se le ha concedido acceso al usuario al sistema y a qué aplicaciones se les ha concedido acceso.</span><span class="sxs-lookup"><span data-stu-id="0968a-138">After confirming the user's identity, the system determines whether the user was granted access to the system and to which applications the user was granted access.</span></span> <span data-ttu-id="0968a-139">La consola de administración de Application Virtualization Server tiene una casilla de verificación **exigir permisos de acceso** en la pestaña **canalización del proveedor** para habilitar o deshabilitar la autorización.</span><span class="sxs-lookup"><span data-stu-id="0968a-139">The Application Virtualization Server Management Console has an **Enforce Access Permission Settings** check box on the **Provider Pipeline** tab to enable or disable authorization.</span></span>

<span data-ttu-id="0968a-140">En el sistema de virtualización de aplicaciones, el acceso se concede a un grupo de usuarios, no a usuarios individuales.</span><span class="sxs-lookup"><span data-stu-id="0968a-140">In the Application Virtualization System, access is granted to a user group only, not to individual users.</span></span>

## <span data-ttu-id="0968a-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0968a-141">Related topics</span></span>


[<span data-ttu-id="0968a-142">Cómo administrar licencias de aplicaciones en la consola de administración de servidor</span><span class="sxs-lookup"><span data-stu-id="0968a-142">How to Manage Application Licenses in the Server Management Console</span></span>](how-to-manage-application-licenses-in-the-server-management-console.md)

[<span data-ttu-id="0968a-143">Cómo configurar o deshabilitar las licencias de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="0968a-143">How to Set Up or Disable Application Licensing</span></span>](how-to-set-up-or-disable-application-licensing.md)

[<span data-ttu-id="0968a-144">Consola de administración de servidor: Nodo de directivas de proveedor</span><span class="sxs-lookup"><span data-stu-id="0968a-144">Server Management Console: Provider Policies Node</span></span>](server-management-console-provider-policies-node.md)

 

 





