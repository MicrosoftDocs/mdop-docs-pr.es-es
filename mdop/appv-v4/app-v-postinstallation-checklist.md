---
title: Lista de comprobación de postinstalación de App-V
description: Lista de comprobación de postinstalación de App-V
author: dansimp
ms.assetid: 74db297e-a744-4287-bcc6-0e096ca8b57a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79728bd2043076b20eb37ba0b1fa6f834a0d94bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819801"
---
# <span data-ttu-id="a2fee-103">Lista de comprobación de postinstalación de App-V</span><span class="sxs-lookup"><span data-stu-id="a2fee-103">App-V Postinstallation Checklist</span></span>


<span data-ttu-id="a2fee-104">La siguiente lista de comprobación proporciona una lista de elementos de nivel superior para considerar y esquematiza los pasos que debe realizar una vez completada la instalación del servidor de administración de Microsoft Application Virtualization (App-V), el servidor de streaming de App-V y el cliente de escritorio de App-V.</span><span class="sxs-lookup"><span data-stu-id="a2fee-104">The following checklist provides a high-level list of items to consider and outlines the steps you should take after you have completed the installation of the Microsoft Application Virtualization (App-V) Management Server, App-V Streaming Server, and the App-V Desktop Client.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a2fee-105">Paso</span><span class="sxs-lookup"><span data-stu-id="a2fee-105">Step</span></span></th>
<th align="left"><span data-ttu-id="a2fee-106">Referencia</span><span class="sxs-lookup"><span data-stu-id="a2fee-106">Reference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2fee-107">Cree excepciones de Firewall para el servidor de administración de App-V o servicios de servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="a2fee-107">Create firewall exceptions for the App-V Management Server or Streaming Server services.</span></span></p></td>
<td align="left"><p><a href="configuring-the-firewall-for-the-app-v-servers.md" data-raw-source="[Configuring the Firewall for the App-V Servers](configuring-the-firewall-for-the-app-v-servers.md)"><span data-ttu-id="a2fee-108">Configurar el firewall para los servidores de App-V</span><span class="sxs-lookup"><span data-stu-id="a2fee-108">Configuring the Firewall for the App-V Servers</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a2fee-109">Verifique que el sistema App-V funcione correctamente mediante la publicación, la transmisión y la prueba de la aplicación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a2fee-109">Verify that the App-V system is functioning correctly by publishing, streaming, and testing the default application.</span></span></p></td>
<td align="left"><p><a href="how-to-install-and-configure-the-default-application.md" data-raw-source="[How to Install and Configure the Default Application](how-to-install-and-configure-the-default-application.md)"><span data-ttu-id="a2fee-110">Cómo instalar y configurar la aplicación predeterminada</span><span class="sxs-lookup"><span data-stu-id="a2fee-110">How to Install and Configure the Default Application</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2fee-111">Configure el cliente de App-V para usar el servidor de streaming de App-V u otro servidor para la transmisión por medio de la <strong> configuración de ApplicationSourceRoot </strong> , <strong> IconSourceRoot </strong> y <strong> OSDSourceRoot </strong> .</span><span class="sxs-lookup"><span data-stu-id="a2fee-111">Configure the App-V Client to use the App-V Streaming Server or other server for streaming by means of the <strong>ApplicationSourceRoot</strong>, <strong>IconSourceRoot</strong>, and <strong>OSDSourceRoot</strong> settings.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-the-client-for-application-package-retrieval.md" data-raw-source="[How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md)"><span data-ttu-id="a2fee-112">Cómo configurar al cliente para la recuperación del paquete de aplicación</span><span class="sxs-lookup"><span data-stu-id="a2fee-112">How to Configure the Client for Application Package Retrieval</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a2fee-113">Aprenda a usar la versión de archivo. msi de paquetes de aplicaciones secuenciadas para la implementación sin conexión.</span><span class="sxs-lookup"><span data-stu-id="a2fee-113">Understand how to use the .msi file version of sequenced application packages for offline deployment.</span></span></p></td>
<td align="left"><p><a href="how-to-publish-a-virtual-application-on-the-client.md" data-raw-source="[How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md)"><span data-ttu-id="a2fee-114">Cómo publicar una aplicación virtual en el cliente</span><span class="sxs-lookup"><span data-stu-id="a2fee-114">How to Publish a Virtual Application on the Client</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a2fee-115">Faculta Configure la creación de reflejo de la base de datos de SQL Server para la base de datos de App-V.</span><span class="sxs-lookup"><span data-stu-id="a2fee-115">(Optional) Configure SQL Server database mirroring for the App-V database.</span></span></p></td>
<td align="left"><p><a href="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md" data-raw-source="[How to Configure Microsoft SQL Server Mirroring Support for App-V](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)"><span data-ttu-id="a2fee-116">Cómo configurar el soporte técnico en duplicación de Microsoft SQL Server para App-V</span><span class="sxs-lookup"><span data-stu-id="a2fee-116">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span></a></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="a2fee-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a2fee-117">Related topics</span></span>


[<span data-ttu-id="a2fee-118">Implementación de virtualización de aplicaciones y listas de comprobación de actualización</span><span class="sxs-lookup"><span data-stu-id="a2fee-118">Application Virtualization Deployment and Upgrade Checklists</span></span>](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





