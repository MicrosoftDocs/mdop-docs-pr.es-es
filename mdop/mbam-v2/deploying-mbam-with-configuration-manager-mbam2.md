---
title: Implementación de MBAM con Administrador de configuración
description: Implementación de MBAM con Administrador de configuración
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823451"
---
# <span data-ttu-id="7192d-103">Implementación de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="7192d-103">Deploying MBAM with Configuration Manager</span></span>


<span data-ttu-id="7192d-104">Los procedimientos siguientes describen cómo implementar Microsoft BitLocker Administration and Monitoring (MBAM) con Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager por conel configuración recomendada, que se describe en [Introducción: uso de MBAM con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span><span class="sxs-lookup"><span data-stu-id="7192d-104">The following procedures describe how to deploy Microsoft BitLocker Administration and Monitoring (MBAM) with Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager by usingthe recommended configuration, which is described in [Getting Started - Using MBAM with Configuration Manager](getting-started---using-mbam-with-configuration-manager.md).</span></span> <span data-ttu-id="7192d-105">La configuración recomendada es instalar las características de administración y supervisión en uno o varios servidores de supervisión y administración de Microsoft BitLocker, e instalar Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager en un servidor independiente.</span><span class="sxs-lookup"><span data-stu-id="7192d-105">The recommended configuration is to install the Administration and Monitoring features on one or more Microsoft BitLocker Administration and Monitoring servers, and install Microsoft System Center Configuration Manager 2007 or MicrosoftSystemCenter2012 ConfigurationManager on a separate server.</span></span>

<span data-ttu-id="7192d-106">Antes de iniciar la instalación, asegúrese de que cumple con los requisitos previos y los requisitos de hardware y software para instalar MBAM con Configuration Manager revisando la [planificación para implementar MBAM con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span><span class="sxs-lookup"><span data-stu-id="7192d-106">Before you start the installation, ensure that you have met the prerequisites and hardware and software requirements for installing MBAM with Configuration Manager by reviewing [Planning to Deploy MBAM with Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).</span></span>

<span data-ttu-id="7192d-107">Si alguna vez necesita volver a instalar MBAM con la topología del administrador de configuración, tendrá que quitar los objetos de Configuration Manager en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="7192d-107">If you ever have to reinstall MBAM with the Configuration Manager topology, you will need to remove certain Configuration Manager objects first.</span></span> <span data-ttu-id="7192d-108">Lea el [artículo](https://go.microsoft.com/fwlink/?LinkId=286306) de la Knowledge base para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="7192d-108">Read the [Knowledge Base article](https://go.microsoft.com/fwlink/?LinkId=286306) for more information.</span></span>

<span data-ttu-id="7192d-109">Los pasos para instalar MBAM con Configuration Manager se agrupan en las siguientes categorías.</span><span class="sxs-lookup"><span data-stu-id="7192d-109">The steps to install MBAM with Configuration Manager are grouped into the following categories.</span></span> <span data-ttu-id="7192d-110">Complete los pasos de cada categoría para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="7192d-110">Complete the steps for each category to complete the installation.</span></span>

## <span data-ttu-id="7192d-111">Cómo crear o editar los archivos mof</span><span class="sxs-lookup"><span data-stu-id="7192d-111">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="7192d-112">Para permitir que los equipos cliente informen detalles de compatibilidad con BitLocker a través de los informes de MBAM Configuration Manager, tiene que editar el archivo **Configuration. mof** y editar o crear el archivo Sms \ _def. mof, en función de la versión de Configuration Manager que esté usando.</span><span class="sxs-lookup"><span data-stu-id="7192d-112">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the **Configuration.mof** file, and either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

[<span data-ttu-id="7192d-113">Cómo crear o editar los archivos mof</span><span class="sxs-lookup"><span data-stu-id="7192d-113">How to Create or Edit the mof Files</span></span>](how-to-create-or-edit-the-mof-files.md)

## <span data-ttu-id="7192d-114">Cómo instalar MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="7192d-114">How to Install MBAM with Configuration Manager</span></span>


<span data-ttu-id="7192d-115">En esta sección se describen los pasos para instalar lo siguiente: MBAM en el servidor de Configuration Manager; las bases de datos de recuperación y auditoría en el servidor de base de datos; y las características de servidor de administración y supervisión en el servidor de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="7192d-115">This section provides steps about how to install the following: MBAM on the Configuration Manager Server; the Recovery and Audit Databases on the Database Server; and the Administration and Monitoring Server features on the Administration and Monitoring Server.</span></span>

[<span data-ttu-id="7192d-116">Cómo instalar MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="7192d-116">How to Install MBAM with Configuration Manager</span></span>](how-to-install-mbam-with-configuration-manager.md)

## <span data-ttu-id="7192d-117">Cómo validar la instalación de características del servidor de MBAM en el servidor de Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="7192d-117">How to Validate the MBAM Server Feature Installation on the Configuration Manager Server</span></span>


<span data-ttu-id="7192d-118">Una vez completada la instalación de administración y supervisión de Microsoft BitLocker, valide que la instalación haya configurado correctamente todas las características de MBAM necesarias para el servidor de Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="7192d-118">When the Microsoft BitLocker Administration and Monitoring installation is complete, validate that the installation has successfully set up all the necessary MBAM features required for the Configuration Manager Server.</span></span>

[<span data-ttu-id="7192d-119">Cómo validar la instalación de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="7192d-119">How to Validate the MBAM Installation with Configuration Manager</span></span>](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## <span data-ttu-id="7192d-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7192d-120">Related topics</span></span>


[<span data-ttu-id="7192d-121">Uso de MBAM con Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="7192d-121">Using MBAM with Configuration Manager</span></span>](using-mbam-with-configuration-manager.md)

 

 





