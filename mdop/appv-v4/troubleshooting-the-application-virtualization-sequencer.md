---
title: Solución de problemas del secuenciador de virtualización de aplicaciones
description: Solución de problemas del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 12ea8367-0b84-44e1-a885-e0539486556b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60c47b853c74d90afc21e9ca172c0eec2a2c7a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815181"
---
# <span data-ttu-id="14701-103">Solución de problemas del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="14701-103">Troubleshooting the Application Virtualization Sequencer</span></span>


<span data-ttu-id="14701-104">En este tema se incluye información que puede usar para solucionar problemas generales en el secuenciador de Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="14701-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="14701-105">Crear un archivo SFTD mediante el secuenciador de App-V aumenta el número de versión de forma inesperada</span><span class="sxs-lookup"><span data-stu-id="14701-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="14701-106">El número de versión asociado a un archivo de SFTD se incrementa de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="14701-106">The version number associated with an SFTD file increases unexpectedly.</span></span>

**<span data-ttu-id="14701-107">Solución</span><span class="sxs-lookup"><span data-stu-id="14701-107">Solution</span></span>**

<span data-ttu-id="14701-108">Use la línea de comandos para generar un nuevo archivo. SFT.</span><span class="sxs-lookup"><span data-stu-id="14701-108">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="14701-109">Para crear el archivo. SFT con la línea de comandos, escriba lo siguiente en un símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="14701-109">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="14701-110">Nombre de archivo de mkdiffpkg.exe &lt; base SFT &gt; &lt; diff SFT nombre de archivo&gt;</span><span class="sxs-lookup"><span data-stu-id="14701-110">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="14701-111">El nombre de archivo del archivo OSD no es correcto después de actualizar el paquete</span><span class="sxs-lookup"><span data-stu-id="14701-111">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="14701-112">Después de actualizar un paquete existente, el nombre de archivo no es correcto.</span><span class="sxs-lookup"><span data-stu-id="14701-112">After you upgrade an existing package, the file name is not correct.</span></span>

**<span data-ttu-id="14701-113">Solución</span><span class="sxs-lookup"><span data-stu-id="14701-113">Solution</span></span>**

<span data-ttu-id="14701-114">Cuando abre un paquete para la actualización, debe especificar la unidad raíz de Q:\\ como la ubicación de salida del paquete.</span><span class="sxs-lookup"><span data-stu-id="14701-114">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="14701-115">No especifique un nombre de archivo asociado con la ubicación de salida.</span><span class="sxs-lookup"><span data-stu-id="14701-115">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="14701-116">La instalación predeterminada de Microsoft Word2003 provoca un error cuando se transmite a un cliente</span><span class="sxs-lookup"><span data-stu-id="14701-116">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="14701-117">Al transmitir Microsoft Word2003 a un cliente, se devuelve un error pero Microsoft Word continúa ejecutándose.</span><span class="sxs-lookup"><span data-stu-id="14701-117">When you stream Microsoft Word2003 to a client, an error is returned but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="14701-118">Solución</span><span class="sxs-lookup"><span data-stu-id="14701-118">Solution</span></span>**

<span data-ttu-id="14701-119">Reordene el paquete de aplicación virtual y seleccione **instalación completa**.</span><span class="sxs-lookup"><span data-stu-id="14701-119">Resequence the virtual application package, and select **Full Install**.</span></span>

## <span data-ttu-id="14701-120">La actualización del paquete no funciona al crear un paquete dependiente</span><span class="sxs-lookup"><span data-stu-id="14701-120">Package Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="14701-121">Cuando se crea un paquete dependiente mediante la actualización de un paquete y se agregan nuevas entradas del registro, parece que funciona correctamente, pero las entradas del registro actualizadas no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="14701-121">When you create a dependent package by using package upgrade and add new registry entries, it appears to function correctly but the updated registry entries are not available.</span></span>

**<span data-ttu-id="14701-122">Solución</span><span class="sxs-lookup"><span data-stu-id="14701-122">Solution</span></span>**

<span data-ttu-id="14701-123">La configuración del registro siempre se almacena con la versión original del paquete, por lo que las actualizaciones del paquete no estarán disponibles a menos que repares el paquete original.</span><span class="sxs-lookup"><span data-stu-id="14701-123">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="14701-124">Error al intentar realizar la secuencia. NET 2.0</span><span class="sxs-lookup"><span data-stu-id="14701-124">Error When Trying to Sequence .NET2.0</span></span>


<span data-ttu-id="14701-125">Al secuenciar un paquete que lo requiera. NET 2.0, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="14701-125">When you sequence a package that requires .NET2.0, you get an error.</span></span>

**<span data-ttu-id="14701-126">Solución</span><span class="sxs-lookup"><span data-stu-id="14701-126">Solution</span></span>**

<span data-ttu-id="14701-127">Secuencias de paquetes que requieren. NET 2.0 no es compatible.</span><span class="sxs-lookup"><span data-stu-id="14701-127">Sequencing packages that require .NET2.0 is not supported.</span></span>

## <span data-ttu-id="14701-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="14701-128">Related topics</span></span>


[<span data-ttu-id="14701-129">Secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="14701-129">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





