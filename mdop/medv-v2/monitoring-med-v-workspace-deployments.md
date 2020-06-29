---
title: Supervisión de las implementaciones de área de trabajo de MED-V
description: Supervisión de las implementaciones de área de trabajo de MED-V
author: dansimp
ms.assetid: 5de0cb06-b8a9-48a5-b8b3-836954295765
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ec4c7c85326e7945aa3d61b7f96872afe24fe37
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827211"
---
# <span data-ttu-id="98cd6-103">Supervisión de las implementaciones de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="98cd6-103">Monitoring MED-V Workspace Deployments</span></span>


<span data-ttu-id="98cd6-104">La característica de supervisión de la virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0 permite ejecutar consultas en áreas de trabajo individuales de MED-V para determinar si la primera configuración se realizó correctamente en toda la empresa después de implementar las áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="98cd6-104">The monitoring feature in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 lets you run queries on individual MED-V workspaces to determine whether first time setup succeeded throughout your enterprise after the MED-V workspaces are deployed.</span></span> <span data-ttu-id="98cd6-105">Supervisar el éxito de la configuración es importante porque MED-V no se encuentra en un estado utilizable hasta que la configuración se complete correctamente por primera vez.</span><span class="sxs-lookup"><span data-stu-id="98cd6-105">Monitoring the success of first time setup is important because MED-V is not in a usable state until first time setup has been completed successfully.</span></span>

<span data-ttu-id="98cd6-106">Esta sección proporciona información e instrucciones para ayudarle a supervisar el éxito o el fracaso de la configuración de la primera vez.</span><span class="sxs-lookup"><span data-stu-id="98cd6-106">This section provides information and instruction to assist you in monitoring the success or failure of first time setup.</span></span>

## <span data-ttu-id="98cd6-107">Para supervisar implementaciones del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="98cd6-107">To monitor MED-V workspace deployments</span></span>


<span data-ttu-id="98cd6-108">La característica de supervisión consiste en un proveedor integrado de instrumental de administración de Windows (WMI) en proceso que puede consultar con el lenguaje de consultas WMI para descubrir el estado de la configuración de primera vez para todos los usuarios finales en un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="98cd6-108">The monitoring feature consists of a coupled in-process Windows Management Instrumentation (WMI) provider that you can query using WMI Query Language to discover the status of first time setup for all end users on a MED-V workspace.</span></span>

<span data-ttu-id="98cd6-109">El proveedor WMI se implementa mediante el marco de extensiones del proveedor WMI de Microsoft .NET Framework 3,5.</span><span class="sxs-lookup"><span data-stu-id="98cd6-109">The WMI provider is implemented by using the WMI Provider Extension framework from the Microsoft .Net Framework 3.5.</span></span> <span data-ttu-id="98cd6-110">El proveedor WMI se ejecuta en el contexto de LocalService y almacena el estado de la configuración por primera vez en \\ProgramData.</span><span class="sxs-lookup"><span data-stu-id="98cd6-110">The WMI provider executes in the context of LocalService and stores the first time setup state securely under \\ProgramData.</span></span>

<span data-ttu-id="98cd6-111">El proveedor WMI se implementa en el espacio de nombres **root\\microsoft\\medv** e implementa la clase **FTS \ _Status**, que expone el método **SetFtsState**.</span><span class="sxs-lookup"><span data-stu-id="98cd6-111">The WMI provider is implemented in the **root\\microsoft\\medv** namespace and implements the class **FTS\_Status**, which exposes the method **SetFtsState**.</span></span> <span data-ttu-id="98cd6-112">MED-V usa **SetFtsState** para establecer el estado de configuración de la primera vez.</span><span class="sxs-lookup"><span data-stu-id="98cd6-112">MED-V uses **SetFtsState** to set the first time setup state.</span></span>

<span data-ttu-id="98cd6-113">La clase contiene las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="98cd6-113">The class contains the following properties.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="98cd6-114">Propiedad</span><span class="sxs-lookup"><span data-stu-id="98cd6-114">Property</span></span></th>
<th align="left"><span data-ttu-id="98cd6-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="98cd6-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="98cd6-116">Máquina</span><span class="sxs-lookup"><span data-stu-id="98cd6-116">Machine</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="98cd6-117"></strong>Propiedad de solo lectura que contiene el nombre de la máquina virtual invitada aprovisionada por la configuración primera vez.</span><span class="sxs-lookup"><span data-stu-id="98cd6-117">Read Only</strong> property that contains the name of the guest virtual machine provisioned by first time setup.</span></span> <span data-ttu-id="98cd6-118">Esta clave contiene el nombre que el invitado habría tenido en el primer error de configuración.</span><span class="sxs-lookup"><span data-stu-id="98cd6-118">This key contains the name that the guest would have had on first time setup failure.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="98cd6-119">StatusCode</span><span class="sxs-lookup"><span data-stu-id="98cd6-119">StatusCode</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="98cd6-120"></strong>Propiedad de solo lectura que contiene cero si la configuración de la primera vez se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="98cd6-120">Read Only</strong> property that contains zero if first time setup succeeded.</span></span> <span data-ttu-id="98cd6-121">Cualquier otro valor devuelto es igual al identificador de evento del error que se ha registrado.</span><span class="sxs-lookup"><span data-stu-id="98cd6-121">Any other value returned equals the event ID for the error that is logged.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="98cd6-122">Tiempo</span><span class="sxs-lookup"><span data-stu-id="98cd6-122">Time</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="98cd6-123">La hora UTC en que se completó por primera vez la configuración.</span><span class="sxs-lookup"><span data-stu-id="98cd6-123">The UTC time that first time setup completed.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="98cd6-124">Usuario</span><span class="sxs-lookup"><span data-stu-id="98cd6-124">User</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="98cd6-125">El usuario para el que se ejecutó por primera vez la configuración.</span><span class="sxs-lookup"><span data-stu-id="98cd6-125">The user for which first time setup was run.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="98cd6-126">En el código siguiente se muestra el archivo de formato de objetos administrados (MOF) que define la clase **FTS \ _Status** .</span><span class="sxs-lookup"><span data-stu-id="98cd6-126">The following code shows the Managed Object Format (MOF) file that defines the **FTS\_Status** class.</span></span>

``` syntax
[dynamic: ToInstance, provider("MedvWmi, Version=2.0.258.0, Culture=neutral, PublicKeyToken=14986c3f172d1c2c")]
class FTS_Status
{
[read, key] string User;
[read] string Machine;
[read] sint32 StatusCode;
[read] datetime Time;
[static, implemented] void SetFtsState([in] sint32 statusCode, [in] string machine);
};
```

<span data-ttu-id="98cd6-127">Como lo más probable es que la preocupación principal sea que las áreas de trabajo de MED-V no se completen correctamente por primera vez, puede escribir la consulta para que solo devuelva los errores que no se hayan podido configurar por primera vez, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="98cd6-127">Because your main concern is most likely those MED-V workspaces for which first time setup was not completed successfully, you can write your query to only return those that failed first time setup, for example:</span></span>

``` syntax
Select * from FTS_Status where StatusCode != 0
```

<span data-ttu-id="98cd6-128">En este caso, la característica de supervisión devuelve una lista de las áreas de trabajo de MED-V en las que se produjo un error en la configuración de la primera vez, que puede usar para tomar las medidas adecuadas para resolver el error.</span><span class="sxs-lookup"><span data-stu-id="98cd6-128">In this case, the monitoring feature returns a list of those MED-V workspaces that failed first time setup, which you can use to take the appropriate actions to resolve the failure.</span></span>

## <span data-ttu-id="98cd6-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="98cd6-129">Related topics</span></span>


[<span data-ttu-id="98cd6-130">Áreas de trabajo de monitor MED-V</span><span class="sxs-lookup"><span data-stu-id="98cd6-130">Monitor MED-V Workspaces</span></span>](monitor-med-v-workspaces.md)

[<span data-ttu-id="98cd6-131">Cómo comprobar la configuración de instalación de primera vez</span><span class="sxs-lookup"><span data-stu-id="98cd6-131">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

 

 





