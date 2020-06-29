---
title: Cómo agregar o quitar la información de redireccionamiento de dirección URL en un área de trabajo de MED-V implementada
description: Cómo agregar o quitar la información de redireccionamiento de dirección URL en un área de trabajo de MED-V implementada
author: dansimp
ms.assetid: bf55848d-bf77-452e-aaa5-4dd4868ff5bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: f0892b16bfc10e6b3f28fe99c51c2c5cedb73d7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826441"
---
# <span data-ttu-id="08a41-103">Cómo agregar o quitar la información de redireccionamiento de dirección URL en un área de trabajo de MED-V implementada</span><span class="sxs-lookup"><span data-stu-id="08a41-103">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>


<span data-ttu-id="08a41-104">Para editar la información de redireccionamiento de la dirección URL en un área de trabajo de MED-V implementada, le recomendamos que actualice el registro del sistema mediante la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="08a41-104">To edit URL redirection information in a deployed MED-V workspace, we recommend that you update the system registry by using Group Policy.</span></span> <span data-ttu-id="08a41-105">Aunque no lo recomendamos, también puede volver a crear e implementar el área de trabajo de MED-V con la información de redireccionamiento de la dirección URL actualizada.</span><span class="sxs-lookup"><span data-stu-id="08a41-105">Although we do not recommend it, you can also rebuild and redeploy the MED-V workspace with the updated URL redirection information.</span></span>

<span data-ttu-id="08a41-106">La clave del registro suele encontrarse en:</span><span class="sxs-lookup"><span data-stu-id="08a41-106">The registry key is usually located at:</span></span>

<span data-ttu-id="08a41-107">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="08a41-107">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="08a41-108">El siguiente valor de cadena múltiple debe estar presente:</span><span class="sxs-lookup"><span data-stu-id="08a41-108">The following multi-string value must be present:</span></span> `RedirectUrls`

<span data-ttu-id="08a41-109">El valor datos para `RedirectUrls` es una lista de todas las direcciones URL que especificó para el redireccionamiento cuando compiló el paquete de área de trabajo Med-v con el **Empaquetador de área de trabajo Med-v**.</span><span class="sxs-lookup"><span data-stu-id="08a41-109">The value data for `RedirectUrls` is a list of all of the URLs that you specified for redirection when you built the MED-V workspace package by using the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="08a41-110">Para obtener más información, vea [crear un paquete de área de trabajo de MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="08a41-110">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="08a41-111">Puede Agregar y quitar información de redirección de la dirección URL realizando una de las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="08a41-111">You can add and remove URL redirection information by performing one of the following tasks:</span></span>

-   [<span data-ttu-id="08a41-112">Editar la clave de registro de redireccionamiento de URL e implementar con la Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="08a41-112">Edit the URL Redirection Registry Key and Deploy Using Group Policy</span></span>](#bkmk-editreg)

-   [<span data-ttu-id="08a41-113">Editar el archivo de texto de redirección de la dirección URL y volver a crear el área de trabajo MED-V</span><span class="sxs-lookup"><span data-stu-id="08a41-113">Edit the URL Redirection Text File and Rebuild the MED-V Workspace</span></span>](#bkmk-edittext)

<a href="" id="bkmk-editreg"></a>**<span data-ttu-id="08a41-114">Para actualizar la información de redireccionamiento de URL mediante Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="08a41-114">To update URL Redirection information by using Group Policy</span></span>**

1.  <span data-ttu-id="08a41-115">Edite el valor de cadena múltiple de clave del registro que tiene el nombre `RedirectUrls` .</span><span class="sxs-lookup"><span data-stu-id="08a41-115">Edit the registry key multi-string value that is named `RedirectUrls`.</span></span> <span data-ttu-id="08a41-116">Este valor suele encontrarse en:</span><span class="sxs-lookup"><span data-stu-id="08a41-116">This value is typically located at:</span></span>

    <span data-ttu-id="08a41-117">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="08a41-117">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

    <span data-ttu-id="08a41-118">Si va a agregar direcciones URL a la clave del registro, escríbala una por línea, tal y como se necesita al crear el paquete de área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="08a41-118">If you are adding URLs to the registry key, enter them one per line, as was required when you built the MED-V workspace package.</span></span> <span data-ttu-id="08a41-119">Para obtener más información, vea [crear un paquete de área de trabajo de MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="08a41-119">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

2.  <span data-ttu-id="08a41-120">Implemente la clave del registro actualizada con la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="08a41-120">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="08a41-121">Para obtener más información acerca de cómo usar la Directiva de grupo, consulte [instalación de software de directiva de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="08a41-121">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

<span data-ttu-id="08a41-122">**Nota:**  Este método de edición de la información de redireccionamiento de URL es una práctica recomendada de MED-V.</span><span class="sxs-lookup"><span data-stu-id="08a41-122">**Note** This method of editing URL redirection information is a MED-V best practice.</span></span>

 

<a href="" id="bkmk-edittext"></a>**<span data-ttu-id="08a41-123">Para volver a crear el área de trabajo de MED-V con un archivo de texto de dirección URL actualizado</span><span class="sxs-lookup"><span data-stu-id="08a41-123">To rebuild the MED-V workspace by using an updated URL text file</span></span>**

-   <span data-ttu-id="08a41-124">Otra forma de agregar y quitar direcciones URL de la lista de redirección es actualizar el archivo de texto de redireccionamiento de URL y, a continuación, usarlo para crear un nuevo área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="08a41-124">Another method of adding and removing URLs from the redirection list is to update the URL redirection text file and then use it to build a new MED-V workspace.</span></span> <span data-ttu-id="08a41-125">Después, puede volver a implementar el área de trabajo de MED-V como antes, mediante el proceso de implementación estándar, como un sistema ESD.</span><span class="sxs-lookup"><span data-stu-id="08a41-125">You can then redeploy the MED-V workspace as before, by using your standard process of deployment, such as an ESD system.</span></span>

    <span data-ttu-id="08a41-126">**Importante**  No se recomienda este método de edición de la información de redireccionamiento de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="08a41-126">**Important** We do not recommend this method of editing URL redirection information.</span></span> <span data-ttu-id="08a41-127">Además, siempre que vuelva a implementar el área de trabajo de MED-V en su empresa, la configuración debe volver a ejecutarse y todos los datos guardados en la máquina virtual se perderán.</span><span class="sxs-lookup"><span data-stu-id="08a41-127">In addition, any time that you redeploy the MED-V workspace back out to your enterprise, first time setup must run again, and any data saved in the virtual machine is lost.</span></span>

     

## <span data-ttu-id="08a41-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08a41-128">Related topics</span></span>


[<span data-ttu-id="08a41-129">Cómo comprobar el redireccionamiento de la dirección URL</span><span class="sxs-lookup"><span data-stu-id="08a41-129">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="08a41-130">Administración de aplicaciones implementadas en áreas de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="08a41-130">Managing Applications Deployed to MED-V Workspaces</span></span>](managing-applications-deployed-to-med-v-workspaces.md)

[<span data-ttu-id="08a41-131">Crear un paquete de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="08a41-131">Create a MED-V Workspace Package</span></span>](create-a-med-v-workspace-package.md)

 

 





