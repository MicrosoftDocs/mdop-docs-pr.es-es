---
title: Lista de comprobación de preinstalación de App-V
description: Lista de comprobación de preinstalación de App-V
author: dansimp
ms.assetid: 3af609b1-2c09-4edb-b083-b913b6d5e8c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 70e71d3dea02daeadedb4cff78c58302ac743dda
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819790"
---
# <span data-ttu-id="6bb76-103">Lista de comprobación de preinstalación de App-V</span><span class="sxs-lookup"><span data-stu-id="6bb76-103">App-V Pre-Installation Checklist</span></span>


<span data-ttu-id="6bb76-104">La siguiente lista de comprobación tiene el propósito de proporcionar una lista de alto nivel de los elementos que se deben tener en cuenta y describe los pasos que debe realizar antes de instalar los servidores de Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="6bb76-104">The following checklist is intended to provide a high-level list of items to consider and outlines the steps you should take before you install the Microsoft Application Virtualization (App-V) servers.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="6bb76-105">Paso</span><span class="sxs-lookup"><span data-stu-id="6bb76-105">Step</span></span></th>
<th align="left"><span data-ttu-id="6bb76-106">Referencia</span><span class="sxs-lookup"><span data-stu-id="6bb76-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6bb76-107">Asegúrese de que su entorno de equipos cumpla con las configuraciones admitidas para App-V.</span><span class="sxs-lookup"><span data-stu-id="6bb76-107">Ensure your computing environment meets the supported configurations required for App-V.</span></span></p></td>
<td align="left"><p><a href="application-virtualization-deployment-requirements.md" data-raw-source="[Application Virtualization Deployment Requirements](application-virtualization-deployment-requirements.md)"><span data-ttu-id="6bb76-108">Requisitos de implementación de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="6bb76-108">Application Virtualization Deployment Requirements</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6bb76-109">Configure los grupos y las cuentas de Active Directory necesarios.</span><span class="sxs-lookup"><span data-stu-id="6bb76-109">Configure the necessary Active Directory groups and accounts.</span></span></p></td>
<td align="left"><p><a href="configuring-prerequisite-groups-in-active-directory-for-app-v.md" data-raw-source="[Configuring Prerequisite Groups in Active Directory for App-V](configuring-prerequisite-groups-in-active-directory-for-app-v.md)"><span data-ttu-id="6bb76-110">Configurar grupos de requisitos previos en Active Directory para App-V</span><span class="sxs-lookup"><span data-stu-id="6bb76-110">Configuring Prerequisite Groups in Active Directory for App-V</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6bb76-111">Establezca la configuración de Internet Information Services (IIS) en el servidor que ejecuta IIS.</span><span class="sxs-lookup"><span data-stu-id="6bb76-111">Configure the Internet Information Services (IIS) settings on the server that is running IIS.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-windows-server-2008-for-app-v-management-servers.md" data-raw-source="[How to Configure Windows Server 2008 for App-V Management Servers](how-to-configure-windows-server-2008-for-app-v-management-servers.md)"><span data-ttu-id="6bb76-112">Cómo configurar Windows Server 2008 para servidores de administración de App-V</span><span class="sxs-lookup"><span data-stu-id="6bb76-112">How to Configure Windows Server 2008 for App-V Management Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="6bb76-113">Configure el servidor en el que se está ejecutando IIS para que sea de confianza para la delegación.</span><span class="sxs-lookup"><span data-stu-id="6bb76-113">Configure the server that is running IIS to be trusted for delegation.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="6bb76-114">Nota</span><span class="sxs-lookup"><span data-stu-id="6bb76-114">Note</span></span></strong><br/><p><span data-ttu-id="6bb76-115">Esto solo es necesario si instalas el servidor de administración de App-V mediante una arquitectura de sistema distribuida, es decir, si instalas la consola de administración de App-V, el servicio Web de administración y la base de datos en diferentes equipos.</span><span class="sxs-lookup"><span data-stu-id="6bb76-115">This is required only if you are installing the App-V Management Server by using a distributed system architecture, that is, if you install the App-V Management Console, the Management Web Service, and the database on different computers.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-configure-the-server-to-be-trusted-for-delegation.md" data-raw-source="[How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)"><span data-ttu-id="6bb76-116">Cómo configurar el servidor para que sea de confianza para delegación</span><span class="sxs-lookup"><span data-stu-id="6bb76-116">How to Configure the Server to be Trusted for Delegation</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="6bb76-117">Instale Microsoft SQL Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6bb76-117">Install Microsoft SQL Server 2008.</span></span></p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="[Install SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=181924)"><span data-ttu-id="6bb76-118">Instale SQL Server 2008 </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924"> https://go.microsoft.com/fwlink/?LinkId=181924 </a> ).</span><span class="sxs-lookup"><span data-stu-id="6bb76-118">Install SQL Server 2008</a> (<a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924">https://go.microsoft.com/fwlink/?LinkId=181924</a>).</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="6bb76-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6bb76-119">Related topics</span></span>


[<span data-ttu-id="6bb76-120">Implementación de virtualización de aplicaciones y listas de comprobación de actualización</span><span class="sxs-lookup"><span data-stu-id="6bb76-120">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

[<span data-ttu-id="6bb76-121">Lista de comprobación de instalación de App-V</span><span class="sxs-lookup"><span data-stu-id="6bb76-121">App-V Installation Checklist</span></span>](app-v-installation-checklist.md)









