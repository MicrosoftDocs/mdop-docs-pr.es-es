---
title: Acerca de cómo usar la línea de comandos del secuenciador
description: Acerca de cómo usar la línea de comandos del secuenciador
author: dansimp
ms.assetid: 0fd5f81b-17f9-4065-bce2-8785e8aac7c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: afb3fb8608c78a3b9237a80529a6c22d792661ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819901"
---
# <span data-ttu-id="b291d-103">Acerca de cómo usar la línea de comandos del secuenciador</span><span class="sxs-lookup"><span data-stu-id="b291d-103">About Using the Sequencer Command Line</span></span>


<span data-ttu-id="b291d-104">Puede usar la línea de comandos para crear paquetes de aplicaciones secuenciados.</span><span class="sxs-lookup"><span data-stu-id="b291d-104">You can use the command line to create sequenced application packages.</span></span> <span data-ttu-id="b291d-105">El uso de la línea de comandos para crear aplicaciones virtuales es útil en los siguientes escenarios:</span><span class="sxs-lookup"><span data-stu-id="b291d-105">Using the command line to create virtual applications is useful in the following scenarios:</span></span>

-   <span data-ttu-id="b291d-106">Necesita crear un gran número de paquetes de aplicación secuenciados.</span><span class="sxs-lookup"><span data-stu-id="b291d-106">You need to create a large number of sequenced application packages.</span></span>

-   <span data-ttu-id="b291d-107">Es necesario crear un paquete de aplicación con secuencia de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="b291d-107">You need to create a sequenced application package on a recurring basis.</span></span>

<span data-ttu-id="b291d-108">**Importante**  La secuenciación en el símbolo del sistema solo permite la secuenciación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b291d-108">**Important** Sequencing at the command prompt allows for default sequencing only.</span></span> <span data-ttu-id="b291d-109">Si necesita cambiar los parámetros de secuenciación predeterminados, debe modificar manualmente un paquete de aplicación secuencial o volver a crear una secuencia de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b291d-109">If you need to change default sequencing parameters, you must either manually modify a sequenced application package or re-sequence the application.</span></span>

 

<span data-ttu-id="b291d-110">Todas las modificaciones posteriores de los paquetes de aplicaciones secuenciadas existentes deben realizarse mediante el Asistente para secuenciación.</span><span class="sxs-lookup"><span data-stu-id="b291d-110">All subsequent modifications to existing sequenced application packages must be made using the sequencing wizard.</span></span>

## <span data-ttu-id="b291d-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b291d-111">Prerequisites</span></span>


<span data-ttu-id="b291d-112">Para ordenar una aplicación mediante el símbolo del sistema, se deben cumplir las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="b291d-112">To sequence an application by using the command prompt, the following conditions must be met:</span></span>

-   <span data-ttu-id="b291d-113">La aplicación que se va a secuenciar no debe requerir cambios ni soluciones alternativas para el instalador o el paquete de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b291d-113">The application that is about to be sequenced must not require changes or workarounds made to it outside the installer or Windows Installer package.</span></span>

-   <span data-ttu-id="b291d-114">Antes de la secuenciación, debe preparar una lista de archivos por lotes para crear los paquetes de aplicación secuenciados.</span><span class="sxs-lookup"><span data-stu-id="b291d-114">Before sequencing, you must prepare a list of batch files for creating the sequenced application packages.</span></span>

-   <span data-ttu-id="b291d-115">Revise para obtener más información sobre los parámetros de la línea de comandos, consulte [parámetros de la línea de comandos](command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b291d-115">Review For more information about the command line parameters, see [Command-Line Parameters](command-line-parameters.md).</span></span>

-   <span data-ttu-id="b291d-116">Revise los errores que se pueden mostrar al crear un paquete de aplicación de secuencia con la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="b291d-116">Review the errors that might be displayed when creating a sequenced application package by using the command line.</span></span> <span data-ttu-id="b291d-117">Para obtener más información, vea estos errores en [errores de la línea de comandos](command-line-errors.md).</span><span class="sxs-lookup"><span data-stu-id="b291d-117">For more information, see these errors, see [Command-Line Errors](command-line-errors.md).</span></span>

## <span data-ttu-id="b291d-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b291d-118">Related topics</span></span>


[<span data-ttu-id="b291d-119">Cómo administrar aplicaciones virtuales con la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="b291d-119">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





