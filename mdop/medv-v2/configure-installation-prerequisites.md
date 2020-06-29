---
title: Configurar los requisitos previos de instalación
description: Configurar los requisitos previos de instalación
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819310"
---
# <span data-ttu-id="80206-103">Configurar los requisitos previos de instalación</span><span class="sxs-lookup"><span data-stu-id="80206-103">Configure Installation Prerequisites</span></span>


<span data-ttu-id="80206-104">Las siguientes instrucciones son los requisitos previos para instalar y usar Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:</span><span class="sxs-lookup"><span data-stu-id="80206-104">The following instructions are prerequisites for installing and using Microsoft Enterprise Desktop Virtualization (MED-V) 2.0:</span></span>

[<span data-ttu-id="80206-105">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="80206-105">Windows Virtual PC</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[<span data-ttu-id="80206-106">Actualización de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="80206-106">Windows Virtual PC Update</span></span>](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[<span data-ttu-id="80206-107">Configuración de software antivirus y de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="80206-107">Antivirus/Backup Software Configuration</span></span>](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a><span data-ttu-id="80206-108">Cómo instalar y configurar Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="80206-108">How to Install and Configure Windows Virtual PC</span></span>


<span data-ttu-id="80206-109">**Importante**  Si ya existe una versión de Virtual PC para Windows en el equipo host, debe desinstalarla antes de instalar Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="80206-109">**Important** If a version of Virtual PC for Windows already exists on the host computer, you must uninstall it before you install Windows Virtual PC.</span></span>

 

**<span data-ttu-id="80206-110">Para instalar Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="80206-110">To install Windows Virtual PC</span></span>**

1.  <span data-ttu-id="80206-111">Descargue [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) desde el centro de descarga de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=195918) .</span><span class="sxs-lookup"><span data-stu-id="80206-111">Download [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) from the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195918).</span></span>

2.  <span data-ttu-id="80206-112">Ejecute el archivo de instalación en el equipo host y siga los pasos del asistente.</span><span class="sxs-lookup"><span data-stu-id="80206-112">Run the installation file on the host computer, and follow the steps in the wizard.</span></span>

<span data-ttu-id="80206-113">**Importante**  Windows Virtual PC incluye el paquete de componentes de integración, que proporciona características que mejoran la interacción entre el entorno virtual y el equipo físico.</span><span class="sxs-lookup"><span data-stu-id="80206-113">**Important** Windows Virtual PC includes the Integration Components package, which provides features that improve the interaction between the virtual environment and the physical computer.</span></span> <span data-ttu-id="80206-114">Por ejemplo, permite que el ratón se mueva entre el host y los equipos invitados.</span><span class="sxs-lookup"><span data-stu-id="80206-114">For example, it lets your mouse move between the host and the guest computers.</span></span> <span data-ttu-id="80206-115">MED-V requiere la instalación del paquete de componentes de integración.</span><span class="sxs-lookup"><span data-stu-id="80206-115">MED-V requires the installation of the Integration Components package.</span></span>

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a><span data-ttu-id="80206-116">Cómo instalar y configurar la actualización de Virtual PC de Windows</span><span class="sxs-lookup"><span data-stu-id="80206-116">How to Install and Configure the Windows Virtual PC Update</span></span>


<span data-ttu-id="80206-117">La actualización de Microsoft Update asociada con el artículo KB977206 habilita el modo de Windows XP para los equipos sin tecnología de virtualización asistida por hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="80206-117">The Microsoft update associated with article KB977206 enables Windows XP Mode for computers without hardware-assisted virtualization (HAV) technology.</span></span> <span data-ttu-id="80206-118">Le recomendamos que instale esta actualización porque es posible que algunas características de integración no funcionen correctamente si el paquete de componentes de integración en el sistema operativo invitado no coincide con la versión de Windows Virtual PC que está instalada en el equipo host.</span><span class="sxs-lookup"><span data-stu-id="80206-118">We recommended that you install this update because some integration features might not work correctly if the Integration Components package in the guest operating system do not match the version of Windows Virtual PC that is installed on the host computer.</span></span>

<span data-ttu-id="80206-119">**Importante**  No tiene que instalar esta actualización cuando está instalando MED-V en equipos host que ejecutan Windows 7 con Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="80206-119">**Important** You do not have to install this update when you are installing MED-V on host computers that are running Windows 7 with Service Pack 1.</span></span>

 

<span data-ttu-id="80206-120">**Sugerencia**  Además de la actualización que se muestra aquí, le recomendamos que revise todas las actualizaciones disponibles de Virtual PC de Windows y que aplique las actualizaciones apropiadas o necesarias para su entorno.</span><span class="sxs-lookup"><span data-stu-id="80206-120">**Tip** In addition to the update listed here, we recommend that you review all available Windows Virtual PC updates and apply those updates that are appropriate or necessary for your environment.</span></span>

 

**<span data-ttu-id="80206-121">Para instalar la actualización de Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="80206-121">To install the Windows Virtual PC Update</span></span>**

1.  <span data-ttu-id="80206-122">Descargue la actualización de Windows Virtual PC requerida desde el centro de descarga de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="80206-122">Download the required Windows Virtual PC update from the Microsoft Download Center.</span></span>

    <span data-ttu-id="80206-123">[actualización de 32](https://go.microsoft.com/fwlink/?LinkId=195919) bits ( https://go.microsoft.com/fwlink/?LinkId=195919) .</span><span class="sxs-lookup"><span data-stu-id="80206-123">[32-bit Update](https://go.microsoft.com/fwlink/?LinkId=195919) (https://go.microsoft.com/fwlink/?LinkId=195919).</span></span>

    <span data-ttu-id="80206-124">[actualización de 64](https://go.microsoft.com/fwlink/?LinkId=195920) bits ( https://go.microsoft.com/fwlink/?LinkId=195920) .</span><span class="sxs-lookup"><span data-stu-id="80206-124">[64-bit Update](https://go.microsoft.com/fwlink/?LinkId=195920) (https://go.microsoft.com/fwlink/?LinkId=195920).</span></span>

2.  <span data-ttu-id="80206-125">Ejecute el archivo de instalación en el equipo host en modo elevado y siga los pasos que se indican en el asistente.</span><span class="sxs-lookup"><span data-stu-id="80206-125">Run the installation file on the host computer in elevated mode, and follow the steps in the wizard.</span></span>

    <span data-ttu-id="80206-126">Para obtener más información sobre el paquete de revisiones para Windows Virtual PC, consulte el [artículo 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ( https://go.microsoft.com/fwlink/?LinkId=195921) .</span><span class="sxs-lookup"><span data-stu-id="80206-126">For more information about the hotfix package for Windows Virtual PC, see [article 977206](https://go.microsoft.com/fwlink/?LinkId=195921) (https://go.microsoft.com/fwlink/?LinkId=195921).</span></span>

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a><span data-ttu-id="80206-127">Cómo configurar el software antivirus y de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="80206-127">How to Configure Antivirus/Backup Software</span></span>


<span data-ttu-id="80206-128">Para evitar que la actividad antivirus afecte el rendimiento del escritorio virtual, le recomendamos, donde puede excluir los siguientes tipos de archivo de máquina virtual de cualquier proceso de copia de seguridad o antivirus que se ejecute en el equipo host:</span><span class="sxs-lookup"><span data-stu-id="80206-128">To prevent antivirus activity from affecting the performance of the virtual desktop, we recommend, where you can, to exclude the following virtual machine file types from any antivirus or backup process that is running on the host computer:</span></span>

-   <span data-ttu-id="80206-129">\*. VMC</span><span class="sxs-lookup"><span data-stu-id="80206-129">\*.VMC</span></span>

-   <span data-ttu-id="80206-130">\*. VUD</span><span class="sxs-lookup"><span data-stu-id="80206-130">\*.VUD</span></span>

-   <span data-ttu-id="80206-131">\*. VSV</span><span class="sxs-lookup"><span data-stu-id="80206-131">\*.VSV</span></span>

-   <span data-ttu-id="80206-132">\*. EXPIRA</span><span class="sxs-lookup"><span data-stu-id="80206-132">\*.VHD</span></span>

## <span data-ttu-id="80206-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="80206-133">Related topics</span></span>


[<span data-ttu-id="80206-134">Configurar los requisitos previos de entorno</span><span class="sxs-lookup"><span data-stu-id="80206-134">Configure Environment Prerequisites</span></span>](configure-environment-prerequisites.md)

[<span data-ttu-id="80206-135">Arquitectura de alto nivel</span><span class="sxs-lookup"><span data-stu-id="80206-135">High-Level Architecture</span></span>](high-level-architecturemedv2.md)

[<span data-ttu-id="80206-136">Configuraciones admitidas de MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="80206-136">MED-V 2.0 Supported Configurations</span></span>](med-v-20-supported-configurations.md)

 

 





