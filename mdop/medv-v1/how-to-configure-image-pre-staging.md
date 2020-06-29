---
title: Cómo configurar un ensayo previo de imagen
description: Cómo configurar un ensayo previo de imagen
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826410"
---
# <span data-ttu-id="be58e-103">Cómo configurar un ensayo previo de imagen</span><span class="sxs-lookup"><span data-stu-id="be58e-103">How to Configure Image Pre-staging</span></span>


<span data-ttu-id="be58e-104">**Nota:**  La preprueba previa de imagen solo es útil para la descarga de imagen inicial.</span><span class="sxs-lookup"><span data-stu-id="be58e-104">**Note** Image pre-staging is useful only for the initial image download.</span></span> <span data-ttu-id="be58e-105">No es compatible con la actualización de la imagen.</span><span class="sxs-lookup"><span data-stu-id="be58e-105">It is not supported for image update.</span></span>

 

## <span data-ttu-id="be58e-106">Cómo configurar un ensayo previo de imagen</span><span class="sxs-lookup"><span data-stu-id="be58e-106">How to Configure Image Pre-staging</span></span>


**<span data-ttu-id="be58e-107">Para configurar el ensayo previo de la imagen</span><span class="sxs-lookup"><span data-stu-id="be58e-107">To configure image pre-staging</span></span>**

1.  <span data-ttu-id="be58e-108">En el equipo cliente, en el directorio del almacén de imágenes, cree una carpeta para la imagen de preensayo y asígnele el nombre *imágenes de MED-V*.</span><span class="sxs-lookup"><span data-stu-id="be58e-108">On the client computer, under the image store directory, create a folder for the pre-staging image, and name it *MED-V Images*.</span></span>

    <span data-ttu-id="be58e-109">**Nota:**  Esta carpeta debe llamarse *imágenes de MED-V*.</span><span class="sxs-lookup"><span data-stu-id="be58e-109">**Note** This folder must be called *MED-V Images*.</span></span>

     

2.  <span data-ttu-id="be58e-110">En la carpeta imágenes de MED-V, cree una subcarpeta y asígnele el nombre *PrestagedImages*.</span><span class="sxs-lookup"><span data-stu-id="be58e-110">Inside the MED-V Images folder, create a subfolder and name it *PrestagedImages*.</span></span>

    <span data-ttu-id="be58e-111">**Nota:**  Esta carpeta debe llamarse *PrestagedImages*.</span><span class="sxs-lookup"><span data-stu-id="be58e-111">**Note** This folder must be called *PrestagedImages*.</span></span>

     

3.  <span data-ttu-id="be58e-112">Para aplicar la seguridad de las listas de control de acceso (ACL) a la carpeta *imágenes de MED-V* , establezca la siguiente ACL:</span><span class="sxs-lookup"><span data-stu-id="be58e-112">To apply Access Control Lists (ACL) security to the *MED-V Images* folder, set the following ACL:</span></span>

    **<span data-ttu-id="be58e-113">Usuarios de NT AUTHORITY\\Authenticated: (OI) (CI) (acceso especial:)</span><span class="sxs-lookup"><span data-stu-id="be58e-113">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 <span data-ttu-id="be58e-114">ARCHIVO \ _APPEND \ _DATA</span><span class="sxs-lookup"><span data-stu-id="be58e-114">FILE\_APPEND\_DATA</span></span>**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **<span data-ttu-id="be58e-115">NT AUTHORITY\\SYSTEM: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="be58e-115">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="be58e-116">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="be58e-116">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="be58e-117">**Nota:**  Se recomienda aplicar la seguridad de ACL a la carpeta de *imágenes de MED-V* .</span><span class="sxs-lookup"><span data-stu-id="be58e-117">**Note** It is recommended to apply ACL security to the *MED-V Images* folder.</span></span>

     

4.  <span data-ttu-id="be58e-118">Para aplicar la seguridad de la ACL a la carpeta *PrestagedImages* , establezca la siguiente ACL:</span><span class="sxs-lookup"><span data-stu-id="be58e-118">To apply ACL security to the *PrestagedImages* folder, set the following ACL:</span></span>

    **<span data-ttu-id="be58e-119">Usuarios de NT AUTHORITY\\Authenticated: (OI) (CI) (acceso especial:)</span><span class="sxs-lookup"><span data-stu-id="be58e-119">NT AUTHORITY\\Authenticated Users:(OI)(CI)(special access:)</span></span>**

    **<span data-ttu-id="be58e-120">LEER \ _CONTROL</span><span class="sxs-lookup"><span data-stu-id="be58e-120">READ\_CONTROL</span></span>**

    **<span data-ttu-id="be58e-121">REALIZA</span><span class="sxs-lookup"><span data-stu-id="be58e-121">SYNCHRONIZE</span></span>**

    **<span data-ttu-id="be58e-122">ARCHIVO \ _GENERIC \ _READ</span><span class="sxs-lookup"><span data-stu-id="be58e-122">FILE\_GENERIC\_READ</span></span>**

    **<span data-ttu-id="be58e-123">ARCHIVO \ _READ \ _DATA</span><span class="sxs-lookup"><span data-stu-id="be58e-123">FILE\_READ\_DATA</span></span>**

    **<span data-ttu-id="be58e-124">ARCHIVO \ _READ \ _EA</span><span class="sxs-lookup"><span data-stu-id="be58e-124">FILE\_READ\_EA</span></span>**

    **<span data-ttu-id="be58e-125">ARCHIVO \ _READ \ _ATTRIBUTES</span><span class="sxs-lookup"><span data-stu-id="be58e-125">FILE\_READ\_ATTRIBUTES</span></span>**

    **<span data-ttu-id="be58e-126">NT AUTHORITY\\SYSTEM: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="be58e-126">NT AUTHORITY\\SYSTEM:(OI)(CI)F</span></span>**

    **<span data-ttu-id="be58e-127">BUILTIN\\Administrators: (OI) (CI) F</span><span class="sxs-lookup"><span data-stu-id="be58e-127">BUILTIN\\Administrators:(OI)(CI)F</span></span>**

    <span data-ttu-id="be58e-128">**Nota:**  Se recomienda aplicar la seguridad de ACL a la carpeta *PrestagedImages* .</span><span class="sxs-lookup"><span data-stu-id="be58e-128">**Note** It is recommended to apply ACL security to the *PrestagedImages* folder.</span></span>

     

5.  <span data-ttu-id="be58e-129">Inserta los archivos de imagen (CKM y los archivos de índice) en la carpeta *PrestagedImages*</span><span class="sxs-lookup"><span data-stu-id="be58e-129">Push the image files (CKM and INDEX files) to the *PrestagedImages* folder.</span></span>

    <span data-ttu-id="be58e-130">**Nota:**  Una vez que los archivos de imagen se hayan insertado en la carpeta prestage, se recomienda ejecutar una comprobación de integridad de datos y marcar los archivos como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="be58e-130">**Note** After the image files have been pushed to the pre-stage folder, it is recommended to run a data integrity check and to mark the files as read-only.</span></span>

     

6.  <span data-ttu-id="be58e-131">Incluya el siguiente parámetro en la instalación del cliente MED-V: *Client.MSI VMSFOLDER = "C:\\MED-V imágenes"*.</span><span class="sxs-lookup"><span data-stu-id="be58e-131">Include the following parameter in the MED-V client installation: *Client.MSI VMSFOLDER=”C:\\MED-V Images”*.</span></span>

## <span data-ttu-id="be58e-132">Cómo actualizar la ubicación previa a la fase</span><span class="sxs-lookup"><span data-stu-id="be58e-132">How to Update the Pre-stage Location</span></span>


**<span data-ttu-id="be58e-133">Para actualizar la ubicación previa a la fase</span><span class="sxs-lookup"><span data-stu-id="be58e-133">To update the pre-stage location</span></span>**

1.  <span data-ttu-id="be58e-134">La clave del registro *PrestagedImagesPath*, señala a la ubicación predeterminada de la imagen.</span><span class="sxs-lookup"><span data-stu-id="be58e-134">The registry key, *PrestagedImagesPath*, points to the default image location.</span></span> <span data-ttu-id="be58e-135">Se encuentra en el siguiente directorio:</span><span class="sxs-lookup"><span data-stu-id="be58e-135">It is located in the following directory:</span></span>

    -   <span data-ttu-id="be58e-136">En un procesador x86</span><span class="sxs-lookup"><span data-stu-id="be58e-136">On an x86 -</span></span> `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   <span data-ttu-id="be58e-137">En un x64</span><span class="sxs-lookup"><span data-stu-id="be58e-137">On an x64 -</span></span> `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  <span data-ttu-id="be58e-138">Si la imagen está en una ubicación diferente, cambie la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="be58e-138">If the image is in a different location, change the path.</span></span>

 

 





