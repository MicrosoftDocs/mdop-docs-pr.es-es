---
title: Cómo configurar el servidor de distribución de imagen web
description: Cómo configurar el servidor de distribución de imagen web
author: dansimp
ms.assetid: 2d32ae79-dff5-4c05-a412-dd15452b6007
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a21b14fbaca6bbc09d4c35b4d8fb86365c42e3b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825160"
---
# <span data-ttu-id="fb84d-103">Cómo configurar el servidor de distribución de imagen web</span><span class="sxs-lookup"><span data-stu-id="fb84d-103">How to Configure the Image Web Distribution Server</span></span>


<span data-ttu-id="fb84d-104">Un repositorio de imágenes es un servidor opcional que se usa para la distribución de imágenes (donde los administradores cargan las imágenes nuevas y los equipos cliente comprueban el servidor cada 15 minutos y actualizan su imagen si hay una nueva disponible).</span><span class="sxs-lookup"><span data-stu-id="fb84d-104">An image repository is an optional server that is used for image distribution (where administrators upload new images and client computers check the server every 15 minutes and update their image if a new one is available).</span></span>

## <a href="" id="bkmk-configuringanimagereporitoryusingiis"></a>


<span data-ttu-id="fb84d-105">Un servidor de distribución de imágenes requiere lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb84d-105">An image distribution server requires the following:</span></span>

-   <span data-ttu-id="fb84d-106">Servicios de Internet Information Server (IIS): para obtener información, vea [servicios de información de Internet](https://go.microsoft.com/fwlink/?LinkId=142995).</span><span class="sxs-lookup"><span data-stu-id="fb84d-106">Internet Information Services (IIS)—For information, see [Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=142995).</span></span>

    <span data-ttu-id="fb84d-107">Durante la instalación de IIS, al agregar servicios de rol, seleccione los siguientes métodos de autenticación admitidos:</span><span class="sxs-lookup"><span data-stu-id="fb84d-107">During the IIS installation, when adding role services, select the following supported authentication methods:</span></span>

    -   **<span data-ttu-id="fb84d-108">Autenticación básica</span><span class="sxs-lookup"><span data-stu-id="fb84d-108">Basic Authentication</span></span>**

    -   **<span data-ttu-id="fb84d-109">Autenticación de Windows</span><span class="sxs-lookup"><span data-stu-id="fb84d-109">Windows Authentication</span></span>**

    -   **<span data-ttu-id="fb84d-110">Autenticación de asignación de certificado de cliente</span><span class="sxs-lookup"><span data-stu-id="fb84d-110">Client Certificate Mapping Authentication</span></span>**

    <span data-ttu-id="fb84d-111">Al configurar IIS, incluya lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb84d-111">When configuring IIS, include the following:</span></span>

    -   <span data-ttu-id="fb84d-112">Agregue un directorio virtual, con el alias denominado **MEDVImages**.</span><span class="sxs-lookup"><span data-stu-id="fb84d-112">Add a virtual directory, with the alias named **MEDVImages**.</span></span> <span data-ttu-id="fb84d-113">La ruta de acceso física debe apuntar a la ubicación de las imágenes.</span><span class="sxs-lookup"><span data-stu-id="fb84d-113">The physical path should point to the location of the images.</span></span>

    -   <span data-ttu-id="fb84d-114">Habilitar BITS.</span><span class="sxs-lookup"><span data-stu-id="fb84d-114">Enable BITS.</span></span>

    -   <span data-ttu-id="fb84d-115">Agregue los siguientes tipos MIME:</span><span class="sxs-lookup"><span data-stu-id="fb84d-115">Add the following MIME types:</span></span>

        -   **<span data-ttu-id="fb84d-116">. CKM (aplicación/flujo de octetos)</span><span class="sxs-lookup"><span data-stu-id="fb84d-116">.ckm (application/octet-stream)</span></span>**

        -   <span data-ttu-id="fb84d-117">**. Indice (aplicación/flujo de octetos**)</span><span class="sxs-lookup"><span data-stu-id="fb84d-117">**.index (application/octet-stream**)</span></span>

    -   <span data-ttu-id="fb84d-118">En el sitio MED-V, agregue permisos de lectura a **todos los usuarios**.</span><span class="sxs-lookup"><span data-stu-id="fb84d-118">On the MED-V site, add read permissions to **Everyone**.</span></span>

    -   <span data-ttu-id="fb84d-119">Reinicie IIS.</span><span class="sxs-lookup"><span data-stu-id="fb84d-119">Restart IIS.</span></span>

-   <span data-ttu-id="fb84d-120">Extensiones de servidor BITS para IIS: para obtener información, consulte [instalar extensiones de servidor bits](https://go.microsoft.com/fwlink/?LinkId=142996).</span><span class="sxs-lookup"><span data-stu-id="fb84d-120">BITS Server Extensions for IIS—For information, see [Install BITS Server Extensions](https://go.microsoft.com/fwlink/?LinkId=142996).</span></span>

## <span data-ttu-id="fb84d-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb84d-121">Related topics</span></span>


[<span data-ttu-id="fb84d-122">Configuraciones admitidas</span><span class="sxs-lookup"><span data-stu-id="fb84d-122">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="fb84d-123">Diseñar los repositorios de imagen MED-V</span><span class="sxs-lookup"><span data-stu-id="fb84d-123">Design the MED-V Image Repositories</span></span>](design-the-med-v-image-repositories.md)

 

 





