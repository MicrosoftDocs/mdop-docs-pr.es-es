---
title: Configuración de administración de App-V para entorno distribuido
description: Configuración de administración de App-V para entorno distribuido
author: dansimp
ms.assetid: 53971fa9-8319-435c-be74-c37feb9af1da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c1a638d6afde9270859c8aa98fc9f421c39cfc72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821911"
---
# <span data-ttu-id="0db37-103">Configuración de administración de App-V para entorno distribuido</span><span class="sxs-lookup"><span data-stu-id="0db37-103">Configuring App-V Administration for a Distributed Environment</span></span>


<span data-ttu-id="0db37-104">Al diseñar la infraestructura de su organización específica, puede instalar el servicio Web de administración de App-V en un equipo que no sea el equipo en el que instala el servidor de administración de App-V.</span><span class="sxs-lookup"><span data-stu-id="0db37-104">When designing the infrastructure for your specific organization, you can install the App-V Management Web Service on a computer other than the computer where you install the App-V Management Server.</span></span> <span data-ttu-id="0db37-105">Algunas de las razones comunes para separar estos componentes de App-V son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="0db37-105">Common reasons for separating these App-V components include the following:</span></span>

-   <span data-ttu-id="0db37-106">Rendimiento</span><span class="sxs-lookup"><span data-stu-id="0db37-106">Performance</span></span>

-   <span data-ttu-id="0db37-107">Confiabilidad</span><span class="sxs-lookup"><span data-stu-id="0db37-107">Reliability</span></span>

-   <span data-ttu-id="0db37-108">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="0db37-108">Availability</span></span>

-   <span data-ttu-id="0db37-109">Escalabilidad</span><span class="sxs-lookup"><span data-stu-id="0db37-109">Scalability</span></span>

<span data-ttu-id="0db37-110">Separar el servidor de administración y el servicio Web de administración requiere configuración adicional para que la infraestructura funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="0db37-110">Separating the Management Server and Management Web Service requires additional configuration for the infrastructure to operate correctly.</span></span> <span data-ttu-id="0db37-111">Cuando separe estas dos características pero no complete los procedimientos que se describen en este tema, la consola de administración se conectará al servicio Web de administración, pero no podrá autenticar correctamente con el almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="0db37-111">When you separate these two features but do not complete the procedures described in this topic, the Management Console will connect to the Management Web Service but will not be able to properly authenticate with the data store.</span></span> <span data-ttu-id="0db37-112">La consola de administración no se cargará correctamente y el administrador no podrá completar ninguna tarea administrativa.</span><span class="sxs-lookup"><span data-stu-id="0db37-112">The Management Console will not load properly, and the administrator will not be able to complete any administrative tasks.</span></span>

<span data-ttu-id="0db37-113">Este comportamiento se produce porque el servicio Web de administración no puede usar las credenciales que se le han pasado desde la consola de administración para acceder al almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="0db37-113">This behavior occurs because the Management Web Service cannot use the credentials, passed to it from the Management Console, to access the data store.</span></span> <span data-ttu-id="0db37-114">La solución es configurar el servidor de servicio Web de administración para que sea "de confianza para la delegación".</span><span class="sxs-lookup"><span data-stu-id="0db37-114">The solution is to configure the Management Web Service server to be “Trusted for delegation.”</span></span>

## <span data-ttu-id="0db37-115">Configuración de servicios de dominio de Active Directory</span><span class="sxs-lookup"><span data-stu-id="0db37-115">Configuring Active Directory Domain Services</span></span>


<span data-ttu-id="0db37-116">También es necesario configurar correctamente los servicios de dominio de Active Directory para que funcionen en un entorno distribuido.</span><span class="sxs-lookup"><span data-stu-id="0db37-116">It is also necessary to configure Active Directory Domain Services properly to work in a distributed environment.</span></span> <span data-ttu-id="0db37-117">Esta sección incluye la información que necesita para configurar los servicios de dominio de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0db37-117">This section includes the information you need configure Active Directory Domain Services.</span></span>

### <span data-ttu-id="0db37-118">Cuando el servicio SQL usa una cuenta de sistema local</span><span class="sxs-lookup"><span data-stu-id="0db37-118">When SQL Service Uses Local System account</span></span>

<span data-ttu-id="0db37-119">Para configurar el entorno en el que el servicio SQL usa la cuenta del sistema local, cambie las propiedades de la cuenta del equipo del servicio Web de administración para que sea de confianza para la delegación.</span><span class="sxs-lookup"><span data-stu-id="0db37-119">To set up the environment where the SQL Service uses the local system account, change the properties of the machine account of the Management Web Service to be trusted for delegation.</span></span> <span data-ttu-id="0db37-120">Para obtener procedimientos detallados sobre cómo hacer esto, consulte [Cómo configurar el servidor para que sea de confianza para la delegación](how-to-configure-the-server-to-be-trusted-for-delegation.md)</span><span class="sxs-lookup"><span data-stu-id="0db37-120">For detailed procedures about how to do this, see [How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)</span></span>

### <span data-ttu-id="0db37-121">Cuando el servicio SQL usa una cuenta basada en el dominio</span><span class="sxs-lookup"><span data-stu-id="0db37-121">When SQL Service Uses Domain-Based Account</span></span>

<span data-ttu-id="0db37-122">Para configurar el entorno en el que los servidores SQL usan cuentas de servicio basadas en el dominio, debe considerar si se aplican diversos factores, entre los que se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="0db37-122">To set up the environment where SQL Servers use domain-based service accounts, you need to consider whether or not a variety of factors apply, including the following:</span></span>

-   <span data-ttu-id="0db37-123">Agrupación de SQL Server</span><span class="sxs-lookup"><span data-stu-id="0db37-123">Clustering of SQL Server</span></span>

-   <span data-ttu-id="0db37-124">Replicación</span><span class="sxs-lookup"><span data-stu-id="0db37-124">Replication</span></span>

-   <span data-ttu-id="0db37-125">Tareas automatizadas</span><span class="sxs-lookup"><span data-stu-id="0db37-125">Automated tasks</span></span>

-   <span data-ttu-id="0db37-126">Servidores vinculados</span><span class="sxs-lookup"><span data-stu-id="0db37-126">Linked servers</span></span>

<span data-ttu-id="0db37-127">Para obtener información sobre cómo configurar los servicios de dominio de Active Directory cuando el servicio SQL usa una cuenta basada en el dominio, consulte <https://go.microsoft.com/fwlink/?LinkId=151968> .</span><span class="sxs-lookup"><span data-stu-id="0db37-127">For information about configuring Active Directory Domain Services when the SQL service uses a domain-based account, see <https://go.microsoft.com/fwlink/?LinkId=151968>.</span></span>

 

 





