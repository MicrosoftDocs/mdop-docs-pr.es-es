---
title: Cómo instalar la actualización de lenguaje MBAM en servidores distribuidos
description: Cómo instalar la actualización de lenguaje MBAM en servidores distribuidos
author: dansimp
ms.assetid: 5ddc64c6-0417-4a04-843e-b5e18d9f1a52
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6758463c6fc038c4d6ea86c0d49804f29bb543d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825700"
---
# <span data-ttu-id="a916a-103">Cómo instalar la actualización de lenguaje MBAM en servidores distribuidos</span><span class="sxs-lookup"><span data-stu-id="a916a-103">How to Install the MBAM Language Update on Distributed Servers</span></span>


<span data-ttu-id="a916a-104">Administración y supervisión de Microsoft BitLocker (MBAM) incluye cuatro roles de servidor que se pueden ejecutar en uno o más equipos.</span><span class="sxs-lookup"><span data-stu-id="a916a-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="a916a-105">Sin embargo, solo dos características de servidor de MBAM requieren que la actualización admita la instalación de la versión de idioma de MBAM 1,0 y la plantilla de directiva de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a916a-105">However, only two MBAM Server features require the update to support the installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="a916a-106">En las configuraciones con las características de servidor de MBAM instaladas en varios equipos, solo es necesario actualizar las siguientes características de servidor:</span><span class="sxs-lookup"><span data-stu-id="a916a-106">In configurations with the MBAM Server features installed on multiple computers, only the following server features need to be updated:</span></span>

-   <span data-ttu-id="a916a-107">Los informes de auditoría y cumplimiento de MBAM</span><span class="sxs-lookup"><span data-stu-id="a916a-107">The MBAM Compliance and Audit Reports</span></span>

-   <span data-ttu-id="a916a-108">El servidor de supervisión y administración de MBAM</span><span class="sxs-lookup"><span data-stu-id="a916a-108">The MBAM Administration and Monitoring Server</span></span>

<span data-ttu-id="a916a-109">**Importante**  Las características del servidor de MBAM deben actualizarse en este orden: informes de cumplimiento y auditoría en primer lugar, y luego el servidor de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="a916a-109">**Important** The MBAM server features must be updated in this order: Compliance and Audit Reports first, and then the Administration and Monitoring Server.</span></span> <span data-ttu-id="a916a-110">Las plantillas de directiva de grupo MBAM se pueden actualizar en cualquier momento, sin preocuparse por la secuencia.</span><span class="sxs-lookup"><span data-stu-id="a916a-110">The MBAM Group Policy templates can be updated at any time without concern for sequence.</span></span>

 

**<span data-ttu-id="a916a-111">Para instalar la actualización de idioma MBAM en la característica de servidor de informes y cumplimiento normativo de MBAM</span><span class="sxs-lookup"><span data-stu-id="a916a-111">To install the MBAM Language Update on the MBAM Compliance and Audit Report Server feature</span></span>**

1.  <span data-ttu-id="a916a-112">En el equipo que ejecuta la función MBAM Compliance and Audit Report, busque y ejecute el Asistente para la configuración de actualización de idioma de MBAM (MBAMsetup.exe).</span><span class="sxs-lookup"><span data-stu-id="a916a-112">On the computer running the MBAM Compliance and Audit Report feature, locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span>

2.  <span data-ttu-id="a916a-113">Complete el Asistente para los informes de comprobación y cumplimiento y, a continuación, cierre el asistente.</span><span class="sxs-lookup"><span data-stu-id="a916a-113">Complete the wizard for the Compliance and Audit Reports and then close the wizard.</span></span>

**<span data-ttu-id="a916a-114">Para instalar la actualización de idioma MBAM en la característica servidor de administración y supervisión de MBAM</span><span class="sxs-lookup"><span data-stu-id="a916a-114">To install the MBAM Language Update on the MBAM Administration and Monitoring Server feature</span></span>**

1.  <span data-ttu-id="a916a-115">En el equipo que ejecuta la característica de administración y supervisión de MBAM, abra la consola de administración de Internet Information Services (IIS), vaya a **sitios**y, a continuación, apague el sitio web de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a916a-115">On the computer that is running the MBAM Administration and Monitoring feature, open the Internet Information Services (IIS) management console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="a916a-116">Elija editar los enlaces para el sitio web de MBAM y, a continuación, modifique los enlaces del sitio.</span><span class="sxs-lookup"><span data-stu-id="a916a-116">Choose to edit the bindings for the MBAM website, and then modify the bindings of the site.</span></span> <span data-ttu-id="a916a-117">Por ejemplo, cambie el puerto de 443 a 9443.</span><span class="sxs-lookup"><span data-stu-id="a916a-117">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="a916a-118">Busque y ejecute el Asistente para la configuración de la actualización de idioma de MBAM (MBAMsetup.exe).</span><span class="sxs-lookup"><span data-stu-id="a916a-118">Locate and run the MBAM Language Update setup wizard (MBAMsetup.exe).</span></span> <span data-ttu-id="a916a-119">Complete el Asistente para la característica servidor de administración y supervisión y, a continuación, cierre el asistente.</span><span class="sxs-lookup"><span data-stu-id="a916a-119">Complete the wizard for the Administration and Monitoring Server feature and then close the wizard.</span></span>

4.  <span data-ttu-id="a916a-120">Después de actualizar la base de datos del servidor, abra la consola de administración de IIS y revise los enlaces del sitio web de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="a916a-120">After you upgrade the server database, open IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="a916a-121">Elimine el enlace anterior y asegúrese de que el enlace restante tenga el nombre de host, el certificado y el número de puerto correctos para la configuración de empresa de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a916a-121">Delete the old binding and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="a916a-122">Reinicie el sitio web de MBAM.</span><span class="sxs-lookup"><span data-stu-id="a916a-122">Restart the MBAM web site.</span></span>

7.  <span data-ttu-id="a916a-123">Pruebe la funcionalidad del sitio web MBAM:</span><span class="sxs-lookup"><span data-stu-id="a916a-123">Test the MBAM web site functionality:</span></span>

    -   <span data-ttu-id="a916a-124">Abra la interfaz Web de MBAM y asegúrese de que puede obtener una clave de recuperación para un cliente.</span><span class="sxs-lookup"><span data-stu-id="a916a-124">Open the MBAM web interface and ensure that you can obtain a recovery key for a client.</span></span>

    -   <span data-ttu-id="a916a-125">Exigir el cifrado de un equipo cliente nuevo o manualmente descifrado.</span><span class="sxs-lookup"><span data-stu-id="a916a-125">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="a916a-126">**Nota:**  El cliente de MBAM se abrirá solo si puede comunicarse con la base de datos de recuperación y hardware.</span><span class="sxs-lookup"><span data-stu-id="a916a-126">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="a916a-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a916a-127">Related topics</span></span>


[<span data-ttu-id="a916a-128">Implementación de la actualización de versión de idioma de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="a916a-128">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





