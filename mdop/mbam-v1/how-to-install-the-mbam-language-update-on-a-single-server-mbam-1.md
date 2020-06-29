---
title: Cómo instalar la actualización de lenguaje MBAM en un único servidor
description: Cómo instalar la actualización de lenguaje MBAM en un único servidor
author: dansimp
ms.assetid: e6fe59a3-a3e1-455c-a059-1f23ee083cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94814158335430aba433c180cdba83d0cf15b760
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824751"
---
# <span data-ttu-id="2c66d-103">Cómo instalar la actualización de lenguaje MBAM en un único servidor</span><span class="sxs-lookup"><span data-stu-id="2c66d-103">How to Install the MBAM Language Update on a Single Server</span></span>


<span data-ttu-id="2c66d-104">Administración y supervisión de Microsoft BitLocker (MBAM) incluye cuatro roles de servidor que se pueden ejecutar en uno o más equipos.</span><span class="sxs-lookup"><span data-stu-id="2c66d-104">Microsoft BitLocker Administration and Monitoring (MBAM) includes four server roles that can be run on one or more computers.</span></span> <span data-ttu-id="2c66d-105">Sin embargo, solo dos características de servidor de MBAM requieren que la actualización admita la instalación de la versión de idioma de MBAM 1,0 y la plantilla de directiva de MBAM.</span><span class="sxs-lookup"><span data-stu-id="2c66d-105">However, only two MBAM Server features require the update to support installation of the MBAM 1.0 language release and the MBAM Policy Template.</span></span> <span data-ttu-id="2c66d-106">Para actualizar las tres características MBAM necesarias para instalarlas en un equipo, siga los pasos que se describen en este tema.</span><span class="sxs-lookup"><span data-stu-id="2c66d-106">To update all three of the required MBAM features to be installed on one computer, perform the steps described in this topic.</span></span>

**<span data-ttu-id="2c66d-107">Para instalar la actualización de idioma MBAM en un solo servidor</span><span class="sxs-lookup"><span data-stu-id="2c66d-107">To install the MBAM language update on a single server</span></span>**

1.  <span data-ttu-id="2c66d-108">Abra la consola de administración de Internet Information Services (IIS), vaya a **sitios**y, a continuación, apague el sitio web de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2c66d-108">Open the Internet Information Services (IIS) Management Console, go to **Sites**, and then shut down the Microsoft BitLocker Administration and Monitoring website.</span></span>

2.  <span data-ttu-id="2c66d-109">Edite los enlaces para el sitio web MBAM y, a continuación, modifique temporalmente los enlaces del sitio.</span><span class="sxs-lookup"><span data-stu-id="2c66d-109">Edit the bindings for the MBAM website, and then temporarily modify the bindings of the site.</span></span> <span data-ttu-id="2c66d-110">Por ejemplo, cambie el puerto de 443 a 9443.</span><span class="sxs-lookup"><span data-stu-id="2c66d-110">For example, change the port from 443 to 9443.</span></span>

3.  <span data-ttu-id="2c66d-111">Busque y ejecute el Asistente de instalación de MBAM (MBAMsetup.exe) y seleccione las tres características siguientes:</span><span class="sxs-lookup"><span data-stu-id="2c66d-111">Locate and run the MBAM setup wizard (MBAMsetup.exe) and select the following three features:</span></span>

    1.  <span data-ttu-id="2c66d-112">Informes de cumplimiento y cumplimiento</span><span class="sxs-lookup"><span data-stu-id="2c66d-112">Compliance and Audit Reports</span></span>

    2.  <span data-ttu-id="2c66d-113">Servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="2c66d-113">Administration and Monitoring Server</span></span>

    3.  <span data-ttu-id="2c66d-114">Plantillas de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="2c66d-114">Group Policy Templates</span></span>

    <span data-ttu-id="2c66d-115">**Importante**  Las características del servidor de MBAM deben actualizarse en el siguiente orden: informes de auditoría y cumplimiento en primer lugar, a continuación, el servidor de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="2c66d-115">**Important** The MBAM server features must be updated in the following order: Compliance and Audit Reports first, then Administration and Monitoring Server.</span></span> <span data-ttu-id="2c66d-116">Las plantillas de directiva de grupo se pueden actualizar en cualquier momento sin preocuparse por la secuencia.</span><span class="sxs-lookup"><span data-stu-id="2c66d-116">The Group Policy templates can be updated at any time without concern for sequence.</span></span>

     

4.  <span data-ttu-id="2c66d-117">Después de actualizar la base de datos del servidor, abra la consola de administración de IIS y revise los enlaces del sitio web de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="2c66d-117">After you upgrade the server database, open the IIS Management Console and review the bindings of the Microsoft BitLocker Administration and Monitoring website.</span></span>

5.  <span data-ttu-id="2c66d-118">Elimine uno de los enlaces y asegúrese de que el enlace restante tenga el nombre de host, el certificado y el número de puerto correctos para la configuración de empresa de MBAM.</span><span class="sxs-lookup"><span data-stu-id="2c66d-118">Delete one of the bindings and ensure that the remaining binding has the correct host name, certificate, and port number for the MBAM enterprise configuration.</span></span>

6.  <span data-ttu-id="2c66d-119">Reinicie el sitio web de MBAM.</span><span class="sxs-lookup"><span data-stu-id="2c66d-119">Restart the MBAM website.</span></span>

7.  <span data-ttu-id="2c66d-120">Pruebe la funcionalidad del sitio web de MBAM:</span><span class="sxs-lookup"><span data-stu-id="2c66d-120">Test the MBAM website functionality:</span></span>

    -   <span data-ttu-id="2c66d-121">Abra la interfaz Web de MBAM y asegúrese de que puede obtener una clave de recuperación para un cliente.</span><span class="sxs-lookup"><span data-stu-id="2c66d-121">Open the MBAM web interface and ensure you can fetch a recovery key for a client.</span></span>

    -   <span data-ttu-id="2c66d-122">Exigir el cifrado de un equipo cliente nuevo o manualmente descifrado.</span><span class="sxs-lookup"><span data-stu-id="2c66d-122">Enforce encryption of a new or manually decrypted client computer.</span></span>

        <span data-ttu-id="2c66d-123">**Nota:**  El cliente de MBAM se abrirá solo si puede comunicarse con la base de datos de recuperación y hardware.</span><span class="sxs-lookup"><span data-stu-id="2c66d-123">**Note** The MBAM client opens only if it can communicate with the Recovery and Hardware database.</span></span>

         

## <span data-ttu-id="2c66d-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c66d-124">Related topics</span></span>


[<span data-ttu-id="2c66d-125">Implementación de la actualización de versión de idioma de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="2c66d-125">Deploying the MBAM 1.0 Language Release Update</span></span>](deploying-the-mbam-10-language-release-update.md)

 

 





