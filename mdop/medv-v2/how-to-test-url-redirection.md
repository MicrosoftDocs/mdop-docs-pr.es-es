---
title: Cómo comprobar el redireccionamiento de la dirección URL
description: Cómo comprobar el redireccionamiento de la dirección URL
author: dansimp
ms.assetid: 38d80088-da1d-4098-b27e-76f9e78f81dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d964cf9d0114d3085d7e8952eebc82486b7b76cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824450"
---
# <span data-ttu-id="1ac54-103">Cómo comprobar el redireccionamiento de la dirección URL</span><span class="sxs-lookup"><span data-stu-id="1ac54-103">How to Test URL Redirection</span></span>


<span data-ttu-id="1ac54-104">Después de que finalice la prueba de la primera configuración, puede comprobar que la funcionalidad de redireccionamiento de la dirección URL funciona según lo esperado realizando las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="1ac54-104">After your test of first time setup finishes, you can verify that the URL redirection functionality is working as expected by performing the following tasks.</span></span>

<span data-ttu-id="1ac54-105">**Importante**  El agente de host MED-V debe estar ejecutándose para que el redireccionamiento de direcciones URL funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="1ac54-105">**Important** The MED-V Host Agent must be running for URL redirection to function correctly.</span></span>

<a href="" id="bkmk-urlredir"></a>**<span data-ttu-id="1ac54-106">Para probar el redireccionamiento de URL</span><span class="sxs-lookup"><span data-stu-id="1ac54-106">To test URL Redirection</span></span>**

1.  <span data-ttu-id="1ac54-107">Abra un explorador Internet Explorer en el equipo host y escriba una dirección URL que especificó para el redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="1ac54-107">Open an Internet Explorer browser in the host computer and enter a URL that you specified for redirection.</span></span>

2.  <span data-ttu-id="1ac54-108">Compruebe que la página web está abierta en Internet Explorer en la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="1ac54-108">Verify that the webpage is opened in Internet Explorer on the guest virtual machine.</span></span>

3.  <span data-ttu-id="1ac54-109">Repita este proceso para cada dirección URL que quiera probar.</span><span class="sxs-lookup"><span data-stu-id="1ac54-109">Repeat this process for each URL that you want to test.</span></span>

**<span data-ttu-id="1ac54-110">Para comprobar que se puede Agregar o quitar una dirección URL</span><span class="sxs-lookup"><span data-stu-id="1ac54-110">To test that a URL can be added or removed</span></span>**

1.  <span data-ttu-id="1ac54-111">Agregue o quite una dirección URL del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="1ac54-111">Add or remove a URL from the MED-V workspace.</span></span>

    <span data-ttu-id="1ac54-112">Para obtener información sobre cómo agregar y quitar direcciones URL para el redireccionamiento en un área de trabajo de MED-V, consulte [Manage Med-v URL Redirection](manage-med-v-url-redirection.md).</span><span class="sxs-lookup"><span data-stu-id="1ac54-112">For information about how to add and remove URLs for redirection on a MED-V workspace, see [Manage MED-V URL Redirection](manage-med-v-url-redirection.md).</span></span>

2.  <span data-ttu-id="1ac54-113">Si ha agregado una dirección URL a la lista de redireccionamiento, repita los pasos de [para probar el redireccionamiento de URL](#bkmk-urlredir) para comprobar que la nueva dirección URL redirige de la forma prevista.</span><span class="sxs-lookup"><span data-stu-id="1ac54-113">If you added a URL to the redirection list, repeat the steps in [To Test URL Redirection](#bkmk-urlredir) to verify that the new URL redirects as intended.</span></span>

3.  <span data-ttu-id="1ac54-114">Si ha quitado una dirección URL de la lista de redirección, compruebe que se ha quitado siguiendo estos pasos:</span><span class="sxs-lookup"><span data-stu-id="1ac54-114">If you removed a URL from the redirection list, verify that it is removed by following these steps:</span></span>

    1.  <span data-ttu-id="1ac54-115">Abra un explorador Internet Explorer en el equipo host y escriba la dirección URL que quitó de la lista de redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="1ac54-115">Open an Internet Explorer browser in the host computer and enter the URL that you removed from the redirection list.</span></span>

    2.  <span data-ttu-id="1ac54-116">Compruebe que la página web se abre en Internet Explorer en el equipo host en lugar de en la máquina virtual invitada.</span><span class="sxs-lookup"><span data-stu-id="1ac54-116">Verify that the webpage is opened in Internet Explorer on the host computer instead of on the guest virtual machine.</span></span>

        <span data-ttu-id="1ac54-117">**Nota:**  Pueden pasar varios segundos hasta que tengan lugar los cambios en el redireccionamiento de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="1ac54-117">**Note** It can take several seconds for the URL redirection changes to take place.</span></span>

<span data-ttu-id="1ac54-118">**Nota:**  Si encuentra algún problema al comprobar la configuración de redireccionamiento de la dirección URL, consulte [solución de problemas de operaciones](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="1ac54-118">**Note** If you encounter any problems when verifying your URL redirection settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

<span data-ttu-id="1ac54-119">Después de completar la comprobación de la redirección de URL en el área de trabajo de MED-V, puede probar otras configuraciones para comprobar que funcionan según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="1ac54-119">After you have completed testing URL redirection in your MED-V workspace, you can test other configurations to verify that they function as intended.</span></span>

<span data-ttu-id="1ac54-120">Una vez que haya completado la prueba de su paquete de área de trabajo MED-V y haya comprobado que funciona como se espera, puede implementar el área de trabajo de MED-V en su empresa.</span><span class="sxs-lookup"><span data-stu-id="1ac54-120">After you have completed testing your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="1ac54-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1ac54-121">Related topics</span></span>

[<span data-ttu-id="1ac54-122">Cómo probar la publicación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="1ac54-122">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="1ac54-123">Cómo comprobar la configuración de instalación de primera vez</span><span class="sxs-lookup"><span data-stu-id="1ac54-123">How to Verify First Time Setup Settings</span></span>](how-to-verify-first-time-setup-settings.md)

[<span data-ttu-id="1ac54-124">Implementación del paquete del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="1ac54-124">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

 

 





