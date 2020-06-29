---
title: Cómo editar un archivo OSD mediante un editor de texto
description: Cómo editar un archivo OSD mediante un editor de texto
author: dansimp
ms.assetid: f4263a1b-824f-49b9-8060-b8229c9d9960
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c83547b38cee7e91e8348689583e0542a88dab83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817441"
---
# <span data-ttu-id="48057-103">Cómo editar un archivo OSD mediante un editor de texto</span><span class="sxs-lookup"><span data-stu-id="48057-103">How to Edit an OSD File Using a Text Editor</span></span>


<span data-ttu-id="48057-104">Use el siguiente procedimiento para editar un archivo de descriptor de software abierto (OSD) con un editor de texto.</span><span class="sxs-lookup"><span data-stu-id="48057-104">Use the following procedure to edit an Open Software Descriptor (OSD) file by using a text editor.</span></span>

**<span data-ttu-id="48057-105">Para editar un archivo OSD con un editor de texto</span><span class="sxs-lookup"><span data-stu-id="48057-105">To edit an OSD file by using a text editor</span></span>**

1.  <span data-ttu-id="48057-106">Abra el archivo OSD con cualquier editor de texto XML o ASCII, por ejemplo, el Bloc de notas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="48057-106">Open the OSD file using any XML or ASCII text editor—for example, Microsoft Notepad.</span></span>

    <span data-ttu-id="48057-107">**Nota:**  Antes de modificar el archivo OSD, lea el esquema preestablecido por el archivo XSD en el directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="48057-107">**Note** Before modifying the OSD file, read the schema prescribed by the XSD file in the install directory.</span></span> <span data-ttu-id="48057-108">Si no sigue este esquema, puede haber errores que impidan que una aplicación secuenciada se inicie correctamente.</span><span class="sxs-lookup"><span data-stu-id="48057-108">Failing to follow this schema might introduce errors that prevent a sequenced application from starting successfully.</span></span>

     

2.  <span data-ttu-id="48057-109">Edite el archivo OSD con el editor de texto XML o ASCII que prefiera, y cumpla con el esquema prescrito y las siguientes pautas:</span><span class="sxs-lookup"><span data-stu-id="48057-109">Edit the OSD file using your XML or ASCII text editor of choice, adhering to the prescribed schema and the following guidelines:</span></span>

    1.  <span data-ttu-id="48057-110">Asegúrese de que los elementos con nombre están anidados dentro del &lt; &gt; elemento raíz SOFTPKG.</span><span class="sxs-lookup"><span data-stu-id="48057-110">Ensure that named elements are nested within the &lt;SOFTPKG&gt; root element.</span></span>

    2.  <span data-ttu-id="48057-111">Asegúrese de que los nombres de los elementos están en mayúsculas.</span><span class="sxs-lookup"><span data-stu-id="48057-111">Ensure that element names are in all uppercase letters.</span></span>

    3.  <span data-ttu-id="48057-112">Ten en cuenta que los valores de atributo distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="48057-112">Be aware that attribute values are case sensitive.</span></span>

    4.  <span data-ttu-id="48057-113">Escriba con cuidado y observe las especificaciones de XML.</span><span class="sxs-lookup"><span data-stu-id="48057-113">Type carefully, and observe the XML specifications.</span></span>

## <span data-ttu-id="48057-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="48057-114">Related topics</span></span>


[<span data-ttu-id="48057-115">Acerca de la pestaña OSD</span><span class="sxs-lookup"><span data-stu-id="48057-115">About the OSD Tab</span></span>](about-the-osd-tab.md)

[<span data-ttu-id="48057-116">Cómo editar un archivo OSD</span><span class="sxs-lookup"><span data-stu-id="48057-116">How to Edit an OSD File</span></span>](how-to-edit-an-osd-file.md)

[<span data-ttu-id="48057-117">Elementos de archivo OSD</span><span class="sxs-lookup"><span data-stu-id="48057-117">OSD File Elements</span></span>](osd-file-elements.md)

 

 





