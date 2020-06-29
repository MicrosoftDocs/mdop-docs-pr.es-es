---
title: Restauración de la aplicación y la configuración de Windows sincronizadas con UE-V 1.0
description: Restauración de la aplicación y la configuración de Windows sincronizadas con UE-V 1.0
author: dansimp
ms.assetid: 254a16b1-f186-44a4-8e22-49a4ee87c734
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ae83e0a44f98b66a9930f8c5db2231992a4700
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812375"
---
# <span data-ttu-id="bc341-103">Restauración de la aplicación y la configuración de Windows sincronizadas con UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="bc341-103">Restoring Application and Windows Settings Synchronized with UE-V 1.0</span></span>


<span data-ttu-id="bc341-104">Las características de WMI y PowerShell de la virtualización de la experiencia del usuario de Microsoft (UE-V) proporcionan la capacidad de restaurar paquetes de configuración.</span><span class="sxs-lookup"><span data-stu-id="bc341-104">WMI and PowerShell features of Microsoft User Experience Virtualization (UE-V) provide the ability to restore settings packages.</span></span> <span data-ttu-id="bc341-105">Los comandos WMI y PowerShell le permiten restaurar la configuración de la aplicación y de Windows a los valores de configuración que se encontraban en el equipo la primera vez que se inició la aplicación después de la instalación de UE-V Agent.</span><span class="sxs-lookup"><span data-stu-id="bc341-105">WMI and PowerShell commands allow you to restore application and Windows settings to the settings values that were on the computer the first time the application launched after the UE-V Agent was installed.</span></span> <span data-ttu-id="bc341-106">Esta acción de restauración se realiza en función de la configuración de Windows o de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bc341-106">This restoring action is performed on a per-application or Windows settings basis.</span></span> <span data-ttu-id="bc341-107">La configuración se restaurará la próxima vez que se ejecute la aplicación o cuando el usuario inicie sesión en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="bc341-107">The settings are restored the next time that the application is run or when the user logs on to the operating system.</span></span>

**<span data-ttu-id="bc341-108">Para restaurar la configuración de la aplicación y la configuración de Windows con PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc341-108">To restore application settings and Windows settings with PowerShell</span></span>**

1.  <span data-ttu-id="bc341-109">Abra la ventana de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bc341-109">Open the Windows PowerShell window.</span></span> <span data-ttu-id="bc341-110">Para importar el módulo de PowerShell de Microsoft UE-V, escriba el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="bc341-110">To import the Microsoft UE-V PowerShell module, enter the following command:</span></span>

    ``` syntax
    Import-module UEV
    ```

2.  <span data-ttu-id="bc341-111">Escriba el siguiente cmdlet de PowerShell para restaurar la configuración de la aplicación y la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="bc341-111">Enter the following PowerShell cmdlet to restore the application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="bc341-112">Cmdlet de PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc341-112">PowerShell cmdlet</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="bc341-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc341-113">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="bc341-114">Restore-UevUserSetting</span><span class="sxs-lookup"><span data-stu-id="bc341-114">Restore-UevUserSetting</span></span></p></td>
    <td align="left"><p><span data-ttu-id="bc341-115">Restaura la configuración de usuario de una aplicación o restaura un grupo de configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="bc341-115">Restores the user settings for an application or restores a group of Windows settings</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="bc341-116">Para restaurar la configuración de la aplicación y la configuración de Windows con WMI</span><span class="sxs-lookup"><span data-stu-id="bc341-116">To restore application settings and Windows settings with WMI</span></span>**

1.  <span data-ttu-id="bc341-117">Abra una ventana de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bc341-117">Open a PowerShell window.</span></span>

2.  <span data-ttu-id="bc341-118">Escriba el siguiente comando WMI para restaurar la configuración de la aplicación y la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="bc341-118">Enter the following WMI command to restore application settings and Windows settings.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><strong><span data-ttu-id="bc341-119">Comando WMI</span><span class="sxs-lookup"><span data-stu-id="bc341-119">WMI command</span></span></strong></th>
    <th align="left"><strong><span data-ttu-id="bc341-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc341-120">Description</span></span></strong></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="bc341-121">Invoke-WmiMethod-namespace root\Microsoft\UEV-Name RestoreByTemplateId-ArgumentList &lt; template_ID&gt;</span><span class="sxs-lookup"><span data-stu-id="bc341-121">Invoke-WmiMethod -Namespace root\Microsoft\UEV -Class UserSettings -Name RestoreByTemplateId -ArgumentList &lt;template_ID&gt;</span></span></p></td>
    <td align="left"><p><span data-ttu-id="bc341-122">Restaura la configuración de usuario de una aplicación o restaura un grupo de configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="bc341-122">Restores the user settings for an application or restores a group of Windows settings</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="bc341-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bc341-123">Related topics</span></span>


[<span data-ttu-id="bc341-124">Administración de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="bc341-124">Administering UE-V 1.0</span></span>](administering-ue-v-10.md)

[<span data-ttu-id="bc341-125">Operaciones de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="bc341-125">Operations for UE-V 1.0</span></span>](operations-for-ue-v-10.md)

 

 





