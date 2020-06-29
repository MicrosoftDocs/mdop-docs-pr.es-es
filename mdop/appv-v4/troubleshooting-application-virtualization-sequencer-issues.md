---
title: Solución de problemas del secuenciador de virtualización de aplicaciones
description: Solución de problemas del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 2712094b-a0bc-4643-aced-5415535f3fec
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8b84f37217f29ff2c08a2254d7f54ce74348d2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815241"
---
# <span data-ttu-id="a4a77-103">Solución de problemas del secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a4a77-103">Troubleshooting Application Virtualization Sequencer Issues</span></span>


<span data-ttu-id="a4a77-104">En este tema se incluye información que puede usar para solucionar problemas generales en el secuenciador de Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="a4a77-104">This topic includes information that you can use to help troubleshoot general issues on the Application Virtualization (App-V) Sequencer.</span></span>

## <span data-ttu-id="a4a77-105">Crear un archivo SFTD mediante el secuenciador de App-V aumenta el número de versión de forma inesperada</span><span class="sxs-lookup"><span data-stu-id="a4a77-105">Creating an SFTD File by Using the App-V Sequencer Increases the Version Number Unexpectedly</span></span>


<span data-ttu-id="a4a77-106">Use la línea de comandos para generar un nuevo archivo. SFT.</span><span class="sxs-lookup"><span data-stu-id="a4a77-106">Use the command line to generate a new .sft file.</span></span> <span data-ttu-id="a4a77-107">Para crear el archivo. SFT con la línea de comandos, escriba lo siguiente en un símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="a4a77-107">To create the .sft file by using the command line, enter the following at a command prompt:</span></span>

**<span data-ttu-id="a4a77-108">Nombre de archivo de mkdiffpkg.exe &lt; base SFT &gt; &lt; diff SFT nombre de archivo&gt;</span><span class="sxs-lookup"><span data-stu-id="a4a77-108">mkdiffpkg.exe &lt;base SFT file name&gt; &lt;diff SFT file name&gt;</span></span>**

## <a href="" id="file-name-in-osd-file-is-not-correct-after-package-upgrade-"></a><span data-ttu-id="a4a77-109">El nombre de archivo del archivo OSD no es correcto después de actualizar el paquete</span><span class="sxs-lookup"><span data-stu-id="a4a77-109">File Name in OSD File Is Not Correct After Package Upgrade</span></span>


<span data-ttu-id="a4a77-110">Cuando abre un paquete para la actualización, debe especificar la unidad raíz de Q:\\ como la ubicación de salida del paquete.</span><span class="sxs-lookup"><span data-stu-id="a4a77-110">When you open a package for upgrade, you should specify the root Q:\\ drive as the output location for the package.</span></span> <span data-ttu-id="a4a77-111">No especifique un nombre de archivo asociado con la ubicación de salida.</span><span class="sxs-lookup"><span data-stu-id="a4a77-111">Do not specify an associated file name with the output location.</span></span>

## <span data-ttu-id="a4a77-112">La instalación predeterminada de Microsoft Word2003 provoca un error cuando se transmite a un cliente</span><span class="sxs-lookup"><span data-stu-id="a4a77-112">Microsoft Word2003 Default Install Results in an Error When Streamed to a Client</span></span>


<span data-ttu-id="a4a77-113">Al transmitir Microsoft Word2003 a un cliente, se devuelve un error, pero Microsoft Word continúa ejecutándose.</span><span class="sxs-lookup"><span data-stu-id="a4a77-113">When you stream Microsoft Word2003 to a client, an error is returned, but Microsoft Word continues to run.</span></span>

**<span data-ttu-id="a4a77-114">Solución</span><span class="sxs-lookup"><span data-stu-id="a4a77-114">Solution</span></span>**

<span data-ttu-id="a4a77-115">Reordene el paquete de aplicación virtual y seleccione **instalación completa**.</span><span class="sxs-lookup"><span data-stu-id="a4a77-115">Resequence the virtual application package and select **Full Install**.</span></span>

## <span data-ttu-id="a4a77-116">La actualización activa no funciona al crear un paquete dependiente</span><span class="sxs-lookup"><span data-stu-id="a4a77-116">Active Upgrade Does Not Work When You Create a Dependent Package</span></span>


<span data-ttu-id="a4a77-117">Cuando se crea un paquete dependiente mediante una actualización activa y se agregan nuevas entradas del registro, parece que funciona correctamente, pero las entradas del registro actualizadas no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="a4a77-117">When you create a dependent package by using active upgrade and add new registry entries, it appears to function correctly, but the updated registry entries are not available.</span></span>

**<span data-ttu-id="a4a77-118">Solución</span><span class="sxs-lookup"><span data-stu-id="a4a77-118">Solution</span></span>**

<span data-ttu-id="a4a77-119">La configuración del registro siempre se almacena con la versión original del paquete, por lo que las actualizaciones del paquete no estarán disponibles a menos que repares el paquete original.</span><span class="sxs-lookup"><span data-stu-id="a4a77-119">Registry settings are always stored with the original version of the package, so updates to the package will not appear to be available unless you repair the original package.</span></span>

## <span data-ttu-id="a4a77-120">No se puede ver la información detallada de los documentos de Microsoft Office2007 mediante la página de propiedades</span><span class="sxs-lookup"><span data-stu-id="a4a77-120">Detailed information is not visible for Microsoft Office2007 documents by using the properties page</span></span>


<span data-ttu-id="a4a77-121">Cuando intenta ver información detallada asociada a un documento de Microsoft Office2007 mediante la página Propiedades, la información detallada no está visible.</span><span class="sxs-lookup"><span data-stu-id="a4a77-121">When you try to view detailed information associated with a Microsoft Office2007 document by using the properties page, the detailed information is not visible.</span></span>

**<span data-ttu-id="a4a77-122">Solución</span><span class="sxs-lookup"><span data-stu-id="a4a77-122">Solution</span></span>**

<span data-ttu-id="a4a77-123">App-V no es compatible con las extensiones de Shell necesarias para estas páginas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="a4a77-123">App-V does not support the required shell extensions for these property pages.</span></span>

## <span data-ttu-id="a4a77-124">Algunas claves de registro no se capturan al secuenciar aplicaciones de 16 bits</span><span class="sxs-lookup"><span data-stu-id="a4a77-124">Some registry keys are not captured when you sequence 16-bit applications</span></span>


<span data-ttu-id="a4a77-125">En App-V 4,5, el enlace de registro se ha movido del modo de núcleo al modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="a4a77-125">In App-V 4.5, registry hooking has been moved from kernel mode to user mode.</span></span> <span data-ttu-id="a4a77-126">Si desea secuenciar una aplicación de 16 bits o una aplicación que use un instalador de 16 bits, primero debe configurar el equipo secuenciador de modo que el proceso se ejecute en su propia copia de la máquina DOS virtual de Windows NT (NTVDM).</span><span class="sxs-lookup"><span data-stu-id="a4a77-126">If you want to sequence a 16-bit application or an application that uses a 16-bit installer, you must first configure the sequencer computer so that the process runs in its own copy of the Windows NT Virtual DOS Machine (NTVDM).</span></span>

**<span data-ttu-id="a4a77-127">Solución</span><span class="sxs-lookup"><span data-stu-id="a4a77-127">Solution</span></span>**

<span data-ttu-id="a4a77-128">Antes de secuenciar la aplicación, establezca el siguiente valor de la clave del registro global REGSZ en "sí" en el equipo de secuenciación:</span><span class="sxs-lookup"><span data-stu-id="a4a77-128">Before you sequence the application, set the following global REGSZ registry key value to "yes" on the sequencing computer:</span></span>

<span data-ttu-id="a4a77-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span><span class="sxs-lookup"><span data-stu-id="a4a77-129">HKLM\\SYSTEM\\CurrentControlSet\\Control\\WOW\\DefaultSeparateVDM</span></span>

<span data-ttu-id="a4a77-130">Debe reiniciar el equipo antes de que esto surta efecto.</span><span class="sxs-lookup"><span data-stu-id="a4a77-130">You must restart the computer before this takes effect.</span></span>

## <span data-ttu-id="a4a77-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a4a77-131">Related topics</span></span>


[<span data-ttu-id="a4a77-132">Secuenciador de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="a4a77-132">Application Virtualization Sequencer</span></span>](application-virtualization-sequencer.md)

 

 





