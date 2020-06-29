---
title: Configuración de conexión del servidor AGPM
description: Configuración de conexión del servidor AGPM
author: dansimp
ms.assetid: faf78e5b-2b0d-4069-9b8c-910add892200
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d63163de0a1adf744e6d442b8073e5b32352ed67
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813022"
---
# <span data-ttu-id="ecd27-103">Configuración de conexión del servidor AGPM</span><span class="sxs-lookup"><span data-stu-id="ecd27-103">AGPM Server Connection Settings</span></span>


<span data-ttu-id="ecd27-104">Puede usar la configuración de la plantilla administrativa para administración de directivas de grupo (AGPM) avanzada para configurar conexiones de servidor AGPM de forma centralizada para los administradores de directiva de grupo a quienes se aplica un objeto de directiva de grupo (GPO) con esta configuración.</span><span class="sxs-lookup"><span data-stu-id="ecd27-104">You can use Administrative template settings for Advanced Group Policy Management (AGPM) to centrally configure AGPM Server connections for Group Policy administrators to whom a Group Policy object (GPO) with these settings is applied.</span></span>

<span data-ttu-id="ecd27-105">La siguiente configuración está disponible en Configuration\\Administrative de usuario de Templates\\Windows Components\\AGPM al editar un GPO.</span><span class="sxs-lookup"><span data-stu-id="ecd27-105">The following settings are available under User Configuration\\Administrative Templates\\Windows Components\\AGPM when editing a GPO.</span></span> <span data-ttu-id="ecd27-106">Si esta ruta de acceso no está visible, haga clic con el botón secundario en **plantillas administrativas**y agregue la plantilla AGPM. ADMX o AGPM. adm.</span><span class="sxs-lookup"><span data-stu-id="ecd27-106">If this path is not visible, right-click **Administrative Templates**, and add the agpm.admx or agpm.adm template.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="ecd27-107">Configuración</span><span class="sxs-lookup"><span data-stu-id="ecd27-107">Setting</span></span></th>
<th align="left"><span data-ttu-id="ecd27-108">Efecto</span><span class="sxs-lookup"><span data-stu-id="ecd27-108">Effect</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="ecd27-109">Servidor de AGPM (todos los dominios)</span><span class="sxs-lookup"><span data-stu-id="ecd27-109">AGPM Server (all domains)</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ecd27-110">Si se habilita, esta configuración configura de forma centralizada una conexión de servidor de AGPM para su uso por parte de todos los dominios y deshabilita la configuración de la <strong> </strong> pestaña servidor de AGPM para los administradores de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="ecd27-110">If enabled, this setting centrally configures one AGPM Server connection for use by all domains and disables the settings on the <strong>AGPM Server</strong> tab for Group Policy administrators.</span></span> <span data-ttu-id="ecd27-111">Para varios servidores de AGPM, configure esta opción con un servidor predeterminado y, a continuación, configure la <strong> configuración del servidor </strong> de AGPM en la plantilla administrativa para invalidar este servidor para otros dominios.</span><span class="sxs-lookup"><span data-stu-id="ecd27-111">For multiple AGPM Servers, configure this setting with a default server and then configure the <strong>AGPM Server</strong> setting in the Administrative template to override this server for other domains.</span></span></p>
<p><span data-ttu-id="ecd27-112">Si se deshabilita o no se configura, cada administrador de directiva de grupo debe seleccionar el servidor de AGPM que se va a mostrar para cada dominio en la <strong> </strong> pestaña servidor de AGPM en AGPM.</span><span class="sxs-lookup"><span data-stu-id="ecd27-112">If disabled or not configured, each Group Policy administrator must select the AGPM Server to display for each domain on the <strong>AGPM Server</strong> tab in AGPM.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="ecd27-113">Servidor de AGPM</span><span class="sxs-lookup"><span data-stu-id="ecd27-113">AGPM Server</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="ecd27-114">Si se habilita, esta configuración configura de forma centralizada varios servidores de AGPM específicos del dominio, lo que invalida la <strong> configuración del servidor de AGPM (todos los dominios) </strong> en la plantilla administrativa.</span><span class="sxs-lookup"><span data-stu-id="ecd27-114">If enabled, this setting centrally configures multiple domain-specific AGPM Servers, overriding the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span> <span data-ttu-id="ecd27-115">Si su entorno requiere solo un servidor de AGPM, use solo el <strong> valor de servidor de AGPM (todos los dominios) </strong> en la plantilla administrativa.</span><span class="sxs-lookup"><span data-stu-id="ecd27-115">If your environment requires only a single AGPM Server, use only the <strong>AGPM Server (all domains)</strong> setting in the Administrative template.</span></span></p>
<p><span data-ttu-id="ecd27-116">Si se deshabilita o no se configura, la <strong> configuración del servidor de AGPM (todos los dominios) </strong> en la plantilla administrativa configura la conexión del servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="ecd27-116">If disabled or not configured, the <strong>AGPM Server (all domains)</strong> setting in the Administrative template configures the AGPM Server connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="ecd27-117">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="ecd27-117">Additional references</span></span>

-   [<span data-ttu-id="ecd27-118">Configuración de plantilla administrativa</span><span class="sxs-lookup"><span data-stu-id="ecd27-118">Administrative Template Settings</span></span>](administrative-template-settings.md)

-   [<span data-ttu-id="ecd27-119">Realización de tareas del administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="ecd27-119">Performing AGPM Administrator Tasks</span></span>](performing-agpm-administrator-tasks.md)

 

 





