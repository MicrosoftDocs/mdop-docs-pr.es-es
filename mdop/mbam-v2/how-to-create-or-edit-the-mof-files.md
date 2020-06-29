---
title: Cómo crear o editar los archivos mof
description: Cómo crear o editar los archivos mof
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825321"
---
# <span data-ttu-id="5a592-103">Cómo crear o editar los archivos mof</span><span class="sxs-lookup"><span data-stu-id="5a592-103">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="5a592-104">Antes de instalar administración y supervisión de Microsoft BitLocker (MBAM) con Configuration Manager, debe editar el archivo Configuration. mof.</span><span class="sxs-lookup"><span data-stu-id="5a592-104">Before you install Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, you need to edit the Configuration.mof file.</span></span> <span data-ttu-id="5a592-105">También necesita editar o crear el archivo SMS \ _def. mof, en función de la versión de Configuration Manager que esté usando.</span><span class="sxs-lookup"><span data-stu-id="5a592-105">You also need to either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

## <span data-ttu-id="5a592-106">Editar el archivo Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="5a592-106">Edit the Configuration.mof File</span></span>


<span data-ttu-id="5a592-107">Para permitir que los equipos cliente informen detalles de compatibilidad con BitLocker a través de los informes de MBAM Configuration Manager, tiene que editar el archivo Configuration. mof para Microsoft System Center Configuration Manager 2007 y SystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="5a592-107">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file for Microsoft System Center Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span>

[<span data-ttu-id="5a592-108">Editar el archivo Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="5a592-108">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="5a592-109">Crear o editar el archivo SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="5a592-109">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="5a592-110">Para permitir que los equipos cliente informen de los detalles de cumplimiento de BitLocker en los informes de MBAM Configuration Manager, tiene que crear o editar el archivo SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="5a592-110">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="5a592-111">En el administrador de configuración 2007, el archivo ya existe, por lo que tendrá que editar, pero no sobrescribir, el archivo existente.</span><span class="sxs-lookup"><span data-stu-id="5a592-111">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span> <span data-ttu-id="5a592-112">Si está usando SystemCenter2012 ConfigurationManager, debe crear el archivo.</span><span class="sxs-lookup"><span data-stu-id="5a592-112">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span>

[<span data-ttu-id="5a592-113">Crear o editar el archivo SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="5a592-113">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file.md)

## <span data-ttu-id="5a592-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5a592-114">Related topics</span></span>


[<span data-ttu-id="5a592-115">Implementación de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="5a592-115">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





