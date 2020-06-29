---
title: Cómo configurar al cliente para la compatibilidad de dominio Kerberos MIT
description: Cómo configurar al cliente para la compatibilidad de dominio Kerberos MIT
author: dansimp
ms.assetid: 46102f4c-270c-4115-8eb4-7ff5ae3be32d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ae5cd73d00f340bc50070fdd0a5fd3e038cc3789
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817811"
---
# <span data-ttu-id="d3667-103">Cómo configurar al cliente para la compatibilidad de dominio Kerberos MIT</span><span class="sxs-lookup"><span data-stu-id="d3667-103">How to Configure the Client for MIT Kerberos Realm Support</span></span>


<span data-ttu-id="d3667-104">En Application Virtualization (App-V) 4,5 SP1, se agregó compatibilidad para los territorios Kerberos MIT.</span><span class="sxs-lookup"><span data-stu-id="d3667-104">In Application Virtualization (App-V) 4.5 SP1, support was added for MIT Kerberos realms.</span></span> <span data-ttu-id="d3667-105">En este tema, se proporciona información detallada sobre cómo habilitar esa compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="d3667-105">This topic provides detailed information on how to enable that support.</span></span>

**<span data-ttu-id="d3667-106">Para habilitar la compatibilidad con los territorios MIT Kerberos</span><span class="sxs-lookup"><span data-stu-id="d3667-106">To enable support for MIT Kerberos Realms</span></span>**

-   <span data-ttu-id="d3667-107">Cree una nueva clave del registro llamada **UseMitKerberos** del tipo DWORD, como se indica a continuación, y establezca el valor 1.</span><span class="sxs-lookup"><span data-stu-id="d3667-107">Create a new registry key named **UseMitKerberos** of type DWORD, as follows, and then set it to a value of 1.</span></span>

    <span data-ttu-id="d3667-108">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos</span><span class="sxs-lookup"><span data-stu-id="d3667-108">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Network\\UseMitKerberos</span></span>

 

 





