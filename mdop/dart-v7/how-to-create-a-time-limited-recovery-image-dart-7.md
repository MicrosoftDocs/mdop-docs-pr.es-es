---
title: Cómo crear una imagen para recuperación de límite de tiempo
description: Cómo crear una imagen para recuperación de límite de tiempo
author: dansimp
ms.assetid: d2e29cac-c24c-4239-997f-0320b8a830ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a11891753f80d41f0089311771b906865950337c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812631"
---
# <span data-ttu-id="ea42d-103">Cómo crear una imagen para recuperación de límite de tiempo</span><span class="sxs-lookup"><span data-stu-id="ea42d-103">How to Create a Time Limited Recovery Image</span></span>


<span data-ttu-id="ea42d-104">Puede crear una imagen de recuperación de DaRT que solo se puede usar durante un número determinado de días después de su generación.</span><span class="sxs-lookup"><span data-stu-id="ea42d-104">You can create a DaRT recovery image that can only be used for a certain number of days after it is generated.</span></span> <span data-ttu-id="ea42d-105">Para hacerlo, debe ejecutar el Asistente de **imagen de recuperación de DART** en un símbolo del sistema y especificar el número de días.</span><span class="sxs-lookup"><span data-stu-id="ea42d-105">To do this, you must run the **DaRT Recovery Image Wizard** at a command prompt and specify the number of days.</span></span>

**<span data-ttu-id="ea42d-106">Para crear una imagen de recuperación que tenga un límite de tiempo</span><span class="sxs-lookup"><span data-stu-id="ea42d-106">To create a recovery image that has a time limit</span></span>**

1.  <span data-ttu-id="ea42d-107">Abra un símbolo del sistema con credenciales de administrador.</span><span class="sxs-lookup"><span data-stu-id="ea42d-107">Open a Command Prompt with administrator credentials.</span></span>

2.  <span data-ttu-id="ea42d-108">Cambie el directorio a la ubicación del programa de ERDC.exe.</span><span class="sxs-lookup"><span data-stu-id="ea42d-108">Change the directory to the location of the ERDC.exe program.</span></span>

3.  <span data-ttu-id="ea42d-109">Con la siguiente sintaxis, ejecute el **Asistente de imagen de recuperación de DART**.</span><span class="sxs-lookup"><span data-stu-id="ea42d-109">Using the following syntax, run the **DaRT Recovery Image Wizard**.</span></span> <span data-ttu-id="ea42d-110">*NumberOfDays* es un entero positivo que representa el número de días que se puede usar la imagen de recuperación de DART.</span><span class="sxs-lookup"><span data-stu-id="ea42d-110">*NumberOfDays* is a positive integer that represents the number of days that the DaRT recovery image will be usable.</span></span>

    ``` syntax
    ERDC /e NumberOfDays
    ```

## <span data-ttu-id="ea42d-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ea42d-111">Related topics</span></span>


[<span data-ttu-id="ea42d-112">Creación de la imagen para recuperación de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="ea42d-112">Creating the DaRT 7.0 Recovery Image</span></span>](creating-the-dart-70-recovery-image-dart-7.md)

 

 





