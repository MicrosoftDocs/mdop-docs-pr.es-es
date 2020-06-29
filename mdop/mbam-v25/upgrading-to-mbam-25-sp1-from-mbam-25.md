---
title: Actualización a MBAM 2.5 SP1 desde MBAM 2.5
description: Actualización a MBAM 2.5 SP1 desde MBAM 2.5
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 2/16/2018
ms.openlocfilehash: 19da3df0976b51700e0d10c302a31421a88d17e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812743"
---
# <span data-ttu-id="24aba-103">Actualización a MBAM 2.5 SP1 desde MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="24aba-103">Upgrading to MBAM 2.5 SP1 from MBAM 2.5</span></span>
<span data-ttu-id="24aba-104">En este tema se describe el proceso de actualización del servidor de administración y supervisión de Microsoft BitLocker (MBAM) 2,5 y el cliente de MBAM de 2,5 a MBAM 2,5 SP1.</span><span class="sxs-lookup"><span data-stu-id="24aba-104">This topic describes the process for upgrading the Microsoft BitLocker Administration and Monitoring (MBAM) Server 2.5 and the MBAM Client from 2.5 to MBAM 2.5 SP1.</span></span>

### <span data-ttu-id="24aba-105">Antes de comenzar</span><span class="sxs-lookup"><span data-stu-id="24aba-105">Before you begin</span></span>
#### <span data-ttu-id="24aba-106">Descargar el lanzamiento de servicio de mayo de 2019</span><span class="sxs-lookup"><span data-stu-id="24aba-106">Download the May 2019 servicing release</span></span>
[<span data-ttu-id="24aba-107">Paquete de optimización de escritorio</span><span class="sxs-lookup"><span data-stu-id="24aba-107">Desktop Optimization Pack</span></span>](https://www.microsoft.com/download/details.aspx?id=58345)

#### <span data-ttu-id="24aba-108">Comprobar el documentaion de instalación</span><span class="sxs-lookup"><span data-stu-id="24aba-108">Verify the installation documentaion</span></span>
<span data-ttu-id="24aba-109">Compruebe que tiene la documentación actual de su entorno de MBAM, incluidos los nombres de servidor, los nombres de base de datos, las cuentas de servicio y las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="24aba-109">Verify you have a current documentation of your MBAM environment, including all server names, database names, service accounts and their passwords.</span></span>

### <span data-ttu-id="24aba-110">Pasos de la actualización</span><span class="sxs-lookup"><span data-stu-id="24aba-110">Upgrade steps</span></span>
#### <span data-ttu-id="24aba-111">Pasos para actualizar la base de datos MBAM (SQL Server)</span><span class="sxs-lookup"><span data-stu-id="24aba-111">Steps to upgrade the MBAM Database (SQL Server)</span></span>
1. <span data-ttu-id="24aba-112">Usar el configurador de MBAM; Quite la función Reports del servidor SQL Server o donde se hospede la base de datos de SSRS.</span><span class="sxs-lookup"><span data-stu-id="24aba-112">Using the MBAM Configurator; remove the Reports role from the SQL server, or wherever the SSRS database is hosted.</span></span> <span data-ttu-id="24aba-113">En función de su entorno, puede ser el mismo servidor o uno independiente.</span><span class="sxs-lookup"><span data-stu-id="24aba-113">Depending on your environment, this can be the same server or a separate one.</span></span>
  > [!NOTE]
  > <span data-ttu-id="24aba-114">No verá una opción para quitar las bases de datos; Esto es normal.</span><span class="sxs-lookup"><span data-stu-id="24aba-114">You will not see an option to remove the Databases; this is expected.</span></span>  
2. <span data-ttu-id="24aba-115">Instale 2,5 SP1 (que se encuentra en MDOP-Microsoft Desktop Optimization Pack 2015 desde el sitio del centro de servicios de licencias por volumen:</span><span class="sxs-lookup"><span data-stu-id="24aba-115">Install 2.5 SP1(Located with MDOP - Microsoft Desktop Optimization Pack 2015 from the Volume Licensing Service Center site:</span></span>  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. <span data-ttu-id="24aba-116">No lo configure en este momento</span><span class="sxs-lookup"><span data-stu-id="24aba-116">Do not configure it at this time</span></span> 
4. <span data-ttu-id="24aba-117">Usar el configurador de MBAM; volver a agregar el rol informes</span><span class="sxs-lookup"><span data-stu-id="24aba-117">Using the MBAM Configurator; re-add the Reports role</span></span>
5. <span data-ttu-id="24aba-118">Usar el configurador de MBAM; volver a agregar el rol de base de datos SQL en SQL Server</span><span class="sxs-lookup"><span data-stu-id="24aba-118">Using the MBAM Configurator; re-add the SQL Database role on the SQL Server</span></span>
6. <span data-ttu-id="24aba-119">Al final, se le advertirá de que las bases de DBs ya existen y que no se crearon, pero esto es de esperar</span><span class="sxs-lookup"><span data-stu-id="24aba-119">At the end, you will be warned that the DBs already exist and  weren’t created, but this is expected</span></span>
7. <span data-ttu-id="24aba-120">Este proceso actualiza las bases de datos existentes en la versión actual que se está instalando.</span><span class="sxs-lookup"><span data-stu-id="24aba-120">This process updates the existing databases to the current version being installed.</span></span>              

#### <span data-ttu-id="24aba-121">Pasos para actualizar el servidor de MBAM (ejecutando MBAM e IIS)</span><span class="sxs-lookup"><span data-stu-id="24aba-121">Steps to upgrade the MBAM Server (Running MBAM and IIS)</span></span>
1. <span data-ttu-id="24aba-122">Usar el configurador de MBAM; quitar los portales de administrador y de autoservicio del servidor IIS</span><span class="sxs-lookup"><span data-stu-id="24aba-122">Using the MBAM Configurator; remove the Admin and Self Service Portals from  the IIS server</span></span>
2. <span data-ttu-id="24aba-123">Instalar MBAM 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="24aba-123">Install MBAM 2.5 SP1</span></span>
3. <span data-ttu-id="24aba-124">No lo configure en este momento</span><span class="sxs-lookup"><span data-stu-id="24aba-124">Do not configure it at this time</span></span>  
4. <span data-ttu-id="24aba-125">Usar el configurador de MBAM; volver a agregar los portales de administrador y de autoservicio al servidor IIS</span><span class="sxs-lookup"><span data-stu-id="24aba-125">Using the MBAM Configurator; re-add the Admin and Self Service Portals to the IIS server</span></span> 
5. <span data-ttu-id="24aba-126">Abra un símbolo del sistema con privilegios elevados, escriba **iisreset**y presione Entrar.</span><span class="sxs-lookup"><span data-stu-id="24aba-126">Open an elevated command prompt, type **IISRESET**, and hit Enter.</span></span>
 
#### <span data-ttu-id="24aba-127">Pasos para actualizar los clientes/puntos de conexión de MBAM</span><span class="sxs-lookup"><span data-stu-id="24aba-127">Steps to upgrade the MBAM Clients/Endpoints</span></span>
1. <span data-ttu-id="24aba-128">Desinstalar el agente 2,5 de los puntos de conexión de cliente</span><span class="sxs-lookup"><span data-stu-id="24aba-128">Uninstall the 2.5 Agent from client endpoints</span></span>
2. <span data-ttu-id="24aba-129">Instalar el agente de 2,5 SP1 en los puntos de conexión de cliente</span><span class="sxs-lookup"><span data-stu-id="24aba-129">Install the 2.5 SP1 Agent on the client endpoints</span></span>
3. <span data-ttu-id="24aba-130">Expulsar la actualización de cliente de Resumen de mayo de 2019 a clientes que ejecutan el agente de 2,5 SP1</span><span class="sxs-lookup"><span data-stu-id="24aba-130">Push out the May 2019 Rollup Client update to clients running the 2.5 SP1 Agent</span></span> 
4. <span data-ttu-id="24aba-131">No es necesario desinstalar el cliente existente antes de instalar el Resumen de mayo de 2019.</span><span class="sxs-lookup"><span data-stu-id="24aba-131">There is no need to uninstall the existing client prior to installing the May 2019 Rollup.</span></span>  
