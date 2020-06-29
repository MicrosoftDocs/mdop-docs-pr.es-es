---
title: Cómo crear el directorio raíz del paquete secuenciador
description: Cómo crear el directorio raíz del paquete secuenciador
author: dansimp
ms.assetid: 23fe28f1-c284-43ee-b8b7-1dfbed94eea5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5150e87915202794624b6c51510e56454d2c7d36
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817620"
---
# <span data-ttu-id="bd44c-103">Cómo crear el directorio raíz del paquete secuenciador</span><span class="sxs-lookup"><span data-stu-id="bd44c-103">How to Create the Sequencer Package Root Directory</span></span>


<span data-ttu-id="bd44c-104">El directorio raíz del paquete es el directorio del equipo donde se ejecuta el secuenciador de App-V donde se instalan los archivos de la aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="bd44c-104">The package root directory is the directory on the computer running the App-V Sequencer where files for the sequenced application are installed.</span></span> <span data-ttu-id="bd44c-105">Este directorio también existe prácticamente en el equipo al que se transmitirá una aplicación de secuencia.</span><span class="sxs-lookup"><span data-stu-id="bd44c-105">This directory also exists virtually on the computer to which a sequenced application will be streamed.</span></span> <span data-ttu-id="bd44c-106">Debe crear el directorio raíz del paquete antes de supervisar la instalación de una nueva aplicación.</span><span class="sxs-lookup"><span data-stu-id="bd44c-106">You should create the package root directory before you monitor the installation of a new application.</span></span>

<span data-ttu-id="bd44c-107">Una vez que hayas creado el directorio de raíz del paquete, puedes comenzar a secuenciar las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="bd44c-107">After you have created the package root directory, you can begin sequencing applications.</span></span> <span data-ttu-id="bd44c-108">Para obtener más información sobre la secuenciación de una nueva aplicación, vea [Cómo secuenciar una aplicación](how-to-sequence-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="bd44c-108">For more information about sequencing a new application, see [How to Sequence an Application](how-to-sequence-an-application.md).</span></span>

**<span data-ttu-id="bd44c-109">Para crear el directorio raíz del paquete</span><span class="sxs-lookup"><span data-stu-id="bd44c-109">To create the package root directory</span></span>**

1.  <span data-ttu-id="bd44c-110">Para crear el directorio raíz del paquete, en el equipo que ejecuta el secuenciador de App-V, asigne la unidad Q:\\ a la ubicación de red especificada.</span><span class="sxs-lookup"><span data-stu-id="bd44c-110">To create the package root directory, on the computer running the App-V Sequencer, map the Q:\\ drive to the specified network location.</span></span> <span data-ttu-id="bd44c-111">La ubicación que especifique debe tener suficiente espacio para guardar la aplicación que está transsecuencias.</span><span class="sxs-lookup"><span data-stu-id="bd44c-111">The location you specify should have sufficient space to save the application you are sequencing.</span></span>

2.  <span data-ttu-id="bd44c-112">Para crear un directorio que pueda usar para una nueva aplicación virtual, cree una carpeta en la unidad de Q:\\ y asígnele un nombre.</span><span class="sxs-lookup"><span data-stu-id="bd44c-112">To create a directory that you can use for a new virtual application, create a folder on the Q:\\ drive and assign it a name.</span></span>

    <span data-ttu-id="bd44c-113">**Importante**  El nombre que asigne a los archivos de aplicación virtual que se guardarán en el directorio raíz del paquete debe usar el formato de nombre 8,3.</span><span class="sxs-lookup"><span data-stu-id="bd44c-113">**Important** The name you assign to virtual application files that will be saved in the package root directory should use the 8.3 naming format.</span></span> <span data-ttu-id="bd44c-114">Los nombres de archivo no deben tener más de 8 caracteres con una extensión de nombre de archivo de tres caracteres.</span><span class="sxs-lookup"><span data-stu-id="bd44c-114">The file names should be no longer than 8 characters with a three-character file name extension.</span></span>

     

## <span data-ttu-id="bd44c-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bd44c-115">Related topics</span></span>


[<span data-ttu-id="bd44c-116">Secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="bd44c-116">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

[<span data-ttu-id="bd44c-117">Cómo modificar la ubicación del directorio de registro</span><span class="sxs-lookup"><span data-stu-id="bd44c-117">How to Modify the Log Directory Location</span></span>](how-to-modify-the-log-directory-location.md)

[<span data-ttu-id="bd44c-118">Cómo modificar la ubicación del directorio temporal</span><span class="sxs-lookup"><span data-stu-id="bd44c-118">How to Modify the Scratch Directory Location</span></span>](how-to-modify-the-scratch-directory-location.md)

 

 





