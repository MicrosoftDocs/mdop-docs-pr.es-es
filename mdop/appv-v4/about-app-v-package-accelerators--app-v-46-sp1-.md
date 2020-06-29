---
title: Acerca de los aceleradores de paquetes de App-V (App-V 4.6 SP1)
description: Acerca de los aceleradores de paquetes de App-V (App-V 4.6 SP1)
author: manikadhiman
ms.assetid: fc2d2375-8f17-4a6d-b374-771cb947cb8c
ms.reviewer: ''
manager: dansimp
ms.author: v-madhi
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cb7b8e6fa9482838283257843caf4b291c03bf2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820091"
---
# <span data-ttu-id="d6621-103">Acerca de los aceleradores de paquetes de App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="d6621-103">About App-V Package Accelerators (App-V 4.6 SP1)</span></span>


<span data-ttu-id="d6621-104">Puede usar los aceleradores de paquetes de App-V para secuenciar aplicaciones grandes y complejas automáticamente.</span><span class="sxs-lookup"><span data-stu-id="d6621-104">You can use App-V Package Accelerators to automatically sequence large, complex applications.</span></span> <span data-ttu-id="d6621-105">Además, cuando aplica un acelerador de paquetes de App-V, no siempre es necesario instalar manualmente una aplicación para crear el paquete de aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="d6621-105">Additionally, when you apply an App-V Package Accelerator, you are not always required to manually install an application to create the virtual application package.</span></span>

<span data-ttu-id="d6621-106">**Nota:**  En algunos casos, se le solicitará que instale una aplicación de forma local en el equipo que ejecuta el secuenciador de App-V antes de que pueda usar el acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d6621-106">**Note** In some cases, you are prompted to install an application locally to the computer running the App-V Sequencer before you can use the Package Accelerator.</span></span> <span data-ttu-id="d6621-107">Si necesita instalar una aplicación, debe instalar la aplicación en la ubicación predeterminada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d6621-107">If you have to install an application, you must install the application to the application’s default location.</span></span> <span data-ttu-id="d6621-108">El secuenciador de App-V no supervisa esta instalación.</span><span class="sxs-lookup"><span data-stu-id="d6621-108">This installation is not monitored by App-V Sequencer.</span></span> <span data-ttu-id="d6621-109">Cuando se crea el acelerador de paquetes de App-V, el autor del acelerador de paquetes determina si se necesita instalar una aplicación de forma local.</span><span class="sxs-lookup"><span data-stu-id="d6621-109">When the App-V Package Accelerator is created, the author of the Package Accelerator determines whether to install an application locally is required.</span></span>

 

<span data-ttu-id="d6621-110">El secuenciador de App-V extrae los archivos necesarios del acelerador de paquetes de App-V y los medios de instalación asociados para crear un paquete virtual sin tener que supervisar la instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d6621-110">App-V Sequencer extracts the required files from the App-V Package Accelerator and associated installation media to create a virtual package without having to monitor the installation of the application.</span></span>

<span data-ttu-id="d6621-111">**Importante**  Renuncia de responsabilidad: Microsoft Application Virtualization Sequencer no le otorga derechos de licencia a la aplicación de software que está usando para crear un acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d6621-111">**Important** Disclaimer: The Microsoft Application Virtualization Sequencer does not give you any license rights to the software application you are using to create a Package Accelerator.</span></span> <span data-ttu-id="d6621-112">Debe cumplir todos los términos de licencia de usuario final para dicha aplicación.</span><span class="sxs-lookup"><span data-stu-id="d6621-112">You must abide by all end user license terms for such application.</span></span> <span data-ttu-id="d6621-113">Es responsabilidad suya asegurarse de que los términos de licencia de la aplicación de software le permitan crear un acelerador de paquetes con Application Virtualization Sequencer.</span><span class="sxs-lookup"><span data-stu-id="d6621-113">It is your responsibility to make sure the software application’s license terms allow you to create a Package Accelerator using Application Virtualization Sequencer.</span></span>

 

<span data-ttu-id="d6621-114">Los aceleradores de paquetes y las plantillas de proyecto de App-V difieren entre sí.</span><span class="sxs-lookup"><span data-stu-id="d6621-114">App-V Package Accelerators and project templates differ from each other.</span></span> <span data-ttu-id="d6621-115">Los aceleradores de paquetes son específicos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d6621-115">Package Accelerators are application-specific.</span></span> <span data-ttu-id="d6621-116">Las plantillas de proyecto permiten a los usuarios guardar las opciones de configuración más comunes específicas de una organización y aplicarlas a varias aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d6621-116">Project templates enable users to save commonly used settings specific to an organization and apply them to multiple applications.</span></span> <span data-ttu-id="d6621-117">También puede crear plantillas de proyecto en el símbolo del sistema, mientras que, en cambio, debe usar la consola del secuenciador de App-V para crear aceleradores de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d6621-117">You can also create project templates at the command prompt, while in contrast, you must use the App-V Sequencer console to create Package Accelerators.</span></span> <span data-ttu-id="d6621-118">Además, no se admite la creación de un paquete mediante un acelerador de paquetes ni la aplicación de una plantilla de proyecto.</span><span class="sxs-lookup"><span data-stu-id="d6621-118">Additionally, creating a package by using a Package Accelerator and applying a project template is not supported.</span></span>

## <span data-ttu-id="d6621-119">Compartir aceleradores de paquetes de App-V</span><span class="sxs-lookup"><span data-stu-id="d6621-119">Sharing App-V Package Accelerators</span></span>


<span data-ttu-id="d6621-120">En esta sección se proporciona información de procedimientos recomendados sobre cómo compartir aceleradores de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d6621-120">This section provides best practice information about how to share Package Accelerators.</span></span> <span data-ttu-id="d6621-121">Si planea compartir aceleradores de paquetes, la información, como los nombres de los equipos, la información de la cuenta de usuario y la información sobre las aplicaciones asociadas, puede estar incluida en los aceleradores de paquetes. en la siguiente lista se describen los métodos que debe tener en cuenta al crear aceleradores de paquetes:</span><span class="sxs-lookup"><span data-stu-id="d6621-121">If you plan to share Package Accelerators, information such as computer names, user account information, and information about the associated applications might be included in the Package Accelerators.The following list describes methods you should consider when creating Package Accelerators:</span></span>

-   <span data-ttu-id="d6621-122">**Nombre de usuario**.</span><span class="sxs-lookup"><span data-stu-id="d6621-122">**User name**.</span></span> <span data-ttu-id="d6621-123">Cuando inicia sesión en el equipo que ejecuta el secuenciador de App-V, debe usar una cuenta de usuario genérica, como la cuenta de **Administrador** integrada para administrar el equipo o el dominio.</span><span class="sxs-lookup"><span data-stu-id="d6621-123">When you log on to the computer running App-V Sequencer, you should use a generic user account, such as the built-in **administrator** account for administering the computer / domain.</span></span> <span data-ttu-id="d6621-124">No debe usar una cuenta basada en un nombre de usuario existente.</span><span class="sxs-lookup"><span data-stu-id="d6621-124">You should not use an account that is based on an existing user name.</span></span>

-   <span data-ttu-id="d6621-125">**Nombre del equipo**.</span><span class="sxs-lookup"><span data-stu-id="d6621-125">**Computer Name**.</span></span> <span data-ttu-id="d6621-126">Especifique un nombre general, no Identificativo, para el equipo que ejecuta el secuenciador.</span><span class="sxs-lookup"><span data-stu-id="d6621-126">Specify a general, non-identifying name for the computer running the Sequencer.</span></span>

-   <span data-ttu-id="d6621-127">**Dirección URL del servidor**.</span><span class="sxs-lookup"><span data-stu-id="d6621-127">**Server URL**.</span></span> <span data-ttu-id="d6621-128">En la consola SPRJ, en la pestaña **implementación** , use la configuración predeterminada para la información de configuración de la dirección URL del servidor.</span><span class="sxs-lookup"><span data-stu-id="d6621-128">In the Sequencer console, on the **Deployment** tab, use the default settings for the server URL configuration information.</span></span>

-   <span data-ttu-id="d6621-129">**Las aplicaciones**.</span><span class="sxs-lookup"><span data-stu-id="d6621-129">**Applications**.</span></span> <span data-ttu-id="d6621-130">Si no desea compartir la lista de aplicaciones que se instalaron en el equipo que ejecuta el secuenciador cuando creó el acelerador de paquetes, debe eliminar el archivo de **appv\_manifest.xml** .</span><span class="sxs-lookup"><span data-stu-id="d6621-130">If you do not want to share the list of applications that were installed on the computer running the Sequencer when you created the Package Accelerator, you must delete the **appv\_manifest.xml** file.</span></span> <span data-ttu-id="d6621-131">Este archivo se encuentra en el directorio raíz del paquete de la aplicación virtual.</span><span class="sxs-lookup"><span data-stu-id="d6621-131">This file is located in the package root directory of the virtual application package.</span></span>

<span data-ttu-id="d6621-132">También debe revisar cualquier configuración o archivos de configuración asociados con el paquete de aplicación virtual para asegurarse de que las aplicaciones no contienen información personal.</span><span class="sxs-lookup"><span data-stu-id="d6621-132">You should also review any settings or configuration files associated with the virtual application package to ensure the applications do not contain any personal information.</span></span>

## <span data-ttu-id="d6621-133">Proteger los aceleradores de paquetes de App-V</span><span class="sxs-lookup"><span data-stu-id="d6621-133">Securing App-V Package Accelerators</span></span>


<span data-ttu-id="d6621-134">Guarda siempre los aceleradores de paquetes de App-V y cualquier medio de instalación asociado en una ubicación segura de la red para proteger los aceleradores de paquetes de App-V y los archivos de instalación para que no se manipulen o dañen.</span><span class="sxs-lookup"><span data-stu-id="d6621-134">Always save App-V Package Accelerators and any associated installation media in a secure location on the network to protect the App-V Package Accelerators and the installation files from being tampered with or becoming corrupted.</span></span> <span data-ttu-id="d6621-135">Dado que los aceleradores de paquetes también pueden contener contraseña e información específica del usuario, debe guardar los aceleradores de paquetes de App-V en una ubicación segura y debe firmar digitalmente el acelerador de paquetes después de crearlo para que se pueda comprobar el editor cuando se aplique el acelerador de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d6621-135">Because Package Accelerators can also contain password and user-specific information, you must save App-V Package Accelerators in a secure location, and you must digitally sign the Package Accelerator after you create it so that the publisher can be verified when the Package Accelerator is applied.</span></span> <span data-ttu-id="d6621-136">Para obtener más información sobre las firmas digitales, consulte [directrices de la aplicación de las prácticas de firma digital para la seguridad de criterios comunes](https://go.microsoft.com/fwlink/?LinkId=204705) ( https://go.microsoft.com/fwlink/?LinkId=204705) .</span><span class="sxs-lookup"><span data-stu-id="d6621-136">For more information about digital signatures, see [Application Guidelines on Digital Signature Practices for Common Criteria Security](https://go.microsoft.com/fwlink/?LinkId=204705) (https://go.microsoft.com/fwlink/?LinkId=204705).</span></span>

## <span data-ttu-id="d6621-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d6621-137">Related topics</span></span>


[<span data-ttu-id="d6621-138">Cómo crear aceleradores de paquetes de App-V (App-V 4.6 SP1)</span><span class="sxs-lookup"><span data-stu-id="d6621-138">How to Create App-V Package Accelerators (App-V 4.6 SP1)</span></span>](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)

[<span data-ttu-id="d6621-139">Cómo aplicar un acelerador de paquetes para crear un paquete de aplicaciones virtual (App-V 4,6 SP1)</span><span class="sxs-lookup"><span data-stu-id="d6621-139">How to Apply a Package Accelerator to Create a Virtual Application Package (App-V 4.6 SP1)</span></span>](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)

 

 





