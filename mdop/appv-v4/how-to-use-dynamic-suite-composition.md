---
title: Cómo usar Dynamic Suite Composition
description: Cómo usar Dynamic Suite Composition
author: dansimp
ms.assetid: 24147feb-a0a8-4791-a8e5-cbe5fe13c762
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3bff4c9721352785cf6db5c497234ceaa3c5e448
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816420"
---
# <span data-ttu-id="fb7c2-103">Cómo usar Dynamic Suite Composition</span><span class="sxs-lookup"><span data-stu-id="fb7c2-103">How To Use Dynamic Suite Composition</span></span>


<span data-ttu-id="fb7c2-104">La composición de conjuntos dinámicos en la virtualización de aplicaciones le permite definir una aplicación como dependiente de otra aplicación, como un middleware o un complemento.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-104">Dynamic Suite Composition in Application Virtualization enables you to define an application as being dependent on another application, such as middleware or a plug-in.</span></span> <span data-ttu-id="fb7c2-105">Esto permite que la aplicación interactúe con el middleware o el complemento en el entorno virtual, donde normalmente esto se evita.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-105">This enables the application to interact with the middleware or plug-in in the virtual environment, where typically this is prevented.</span></span> <span data-ttu-id="fb7c2-106">Esto es útil porque un paquete de aplicación secundario se puede usar con varias aplicaciones, conocidas como *aplicaciones principales*, lo que permite que cada aplicación principal haga referencia al mismo paquete secundario.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-106">This is useful because a secondary application package can be used with several other applications, referred to as the *primary applications*, which enables each primary application to reference the same secondary package.</span></span>

<span data-ttu-id="fb7c2-107">Puede usar la composición de conjuntos dinámicos cuando secuencia aplicaciones que dependen de complementos, como controles ActiveX o para aplicaciones que dependen de middleware, como OLE DB o Java Runtime Environment (JRE).</span><span class="sxs-lookup"><span data-stu-id="fb7c2-107">You can use Dynamic Suite Composition when you sequence applications that depend on plug-ins such as ActiveX controls or for applications that depend on middleware such as OLE DB or the Java Runtime Environment (JRE).</span></span> <span data-ttu-id="fb7c2-108">Si todas las aplicaciones que usaban estos componentes dependientes requirieron secuencias, incluidos los componentes, las actualizaciones de esos componentes requerirían volver a secuenciar todas las aplicaciones principales.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-108">If each application that used these dependent components required sequencing, including the components, updates to those components would require re-sequencing all the primary applications.</span></span> <span data-ttu-id="fb7c2-109">Si se hace una secuencia de las aplicaciones principales sin los componentes y después se secuencia el middleware o el complemento como un paquete secundario, solo debe actualizarse el paquete secundario.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-109">If you sequence the primary applications without the components and then sequence the middleware or plug-in as a secondary package, then only the secondary package must be updated.</span></span>

<span data-ttu-id="fb7c2-110">Una ventaja de este enfoque es que reduce el tamaño de los paquetes principales.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-110">One advantage of this approach is that it reduces the size of the primary packages.</span></span> <span data-ttu-id="fb7c2-111">Otra ventaja es que le proporciona un mayor control de los permisos de acceso en las aplicaciones secundarias.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-111">Another advantage is that it provides you with better control of access permissions on the secondary applications.</span></span> <span data-ttu-id="fb7c2-112">Tenga en cuenta que la aplicación secundaria se puede transmitir de la forma habitual y no es necesario que esté en la memoria caché completa para ejecutarla.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-112">Note that the secondary application can be streamed in the regular way and does not have to be fully cached to run.</span></span>

<span data-ttu-id="fb7c2-113">Un paquete principal puede tener más de un paquete secundario.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-113">A primary package can have more than one secondary package.</span></span> <span data-ttu-id="fb7c2-114">Sin embargo, solo se admite un nivel de dependencia, por lo que no puede definir un paquete secundario como dependiente de otro paquete secundario.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-114">However, only one level of dependency is supported, so you cannot define a secondary package as dependent on another secondary package.</span></span> <span data-ttu-id="fb7c2-115">Además, la aplicación secundaria solo puede ser middleware o un complemento, y no puede ser otro producto de software completo.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-115">Also the secondary application can only be middleware or a plug-in and cannot be another full software product.</span></span>

<span data-ttu-id="fb7c2-116">Si tiene previsto hacer varias aplicaciones principales dependientes de un único producto middleware, asegúrese de probar esta configuración para determinar el efecto potencial en el rendimiento del sistema antes de implementarlo.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-116">If you plan to make several primary applications dependent on a single middleware product, make sure that you test this configuration to determine the potential effect on system performance before you deploy it.</span></span>

<span data-ttu-id="fb7c2-117">**Importante**  Las dependencias de paquetes pueden especificarse como obligatorias para una aplicación principal.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-117">**Important** Package dependencies can be specified as mandatory for a primary application.</span></span> <span data-ttu-id="fb7c2-118">Si un paquete secundario se marca como obligatorio y no se puede acceder a él por algún motivo durante la carga, la carga del paquete secundario fallará.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-118">If a secondary package is flagged as mandatory and it cannot be accessed for some reason during loading, the load of the secondary package will fail.</span></span> <span data-ttu-id="fb7c2-119">Además, se producirá un error en la aplicación principal cuando el usuario intente iniciarla.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-119">Also, the primary application will fail when the user tries to start it.</span></span>

 

<span data-ttu-id="fb7c2-120">Puede usar los procedimientos siguientes para crear un paquete secundario, para un complemento o un componente middleware, y luego puede usar el procedimiento final para definir la dependencia en el archivo OSD del paquete secundario.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-120">You can use the following procedures to create a secondary package, for either a plug-in or a middleware component, and then you can use the final procedure to define the dependency in the OSD file of the secondary package.</span></span>

**<span data-ttu-id="fb7c2-121">Para crear un paquete secundario para un complemento con la composición de conjunto dinámico</span><span class="sxs-lookup"><span data-stu-id="fb7c2-121">To create a secondary package for a plug-in by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="fb7c2-122">En un equipo de secuencias que esté configurado con una imagen limpia, instale Application Virtualization Sequencer y guarde el estado del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-122">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="fb7c2-123">Ordene la aplicación principal y guarde el paquete en la carpeta de contenido en el servidor.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-123">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

3.  <span data-ttu-id="fb7c2-124">Restaure el equipo de secuenciación a su estado guardado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-124">Restore the sequencing computer to its saved state from step 1.</span></span>

4.  <span data-ttu-id="fb7c2-125">Instale y configure la aplicación principal de forma local en el equipo de secuencias.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-125">Install and configure the primary application locally on the sequencing computer.</span></span>

    <span data-ttu-id="fb7c2-126">**Importante**  Debes especificar una nueva raíz de paquete para el paquete secundario.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-126">**Important** You must specify a new package root for the secondary package.</span></span>

     

5.  <span data-ttu-id="fb7c2-127">Iniciar la fase de supervisión del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-127">Start the sequencer monitoring phase.</span></span>

6.  <span data-ttu-id="fb7c2-128">Instale el complemento en el equipo de secuenciación y configúrelo según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-128">Install the plug-in on the sequencing computer and configure it as needed.</span></span>

7.  <span data-ttu-id="fb7c2-129">Abra la aplicación principal y confirme que el complemento está funcionando correctamente.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-129">Open the primary application, and confirm that the plug-in is working correctly.</span></span>

8.  <span data-ttu-id="fb7c2-130">En la consola del secuenciador, cree una aplicación ficticia que represente el paquete secundario que contendrá el complemento y seleccione un icono.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-130">In the sequencer console, create a dummy application to represent the secondary package that will contain the plug-in and select an icon.</span></span>

9.  <span data-ttu-id="fb7c2-131">Guarde el paquete en la carpeta de contenido en el servidor.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-131">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="fb7c2-132">**Nota:**  Para ayudar con la administración de paquetes secundarios, se recomienda que el nombre del paquete incluya el término "paquete secundario" para enfatizar que se trata de un paquete que no funcionará como una aplicación independiente; por ejemplo, **el paquete secundario \ [nombre de complemento \]**.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-132">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Plug In Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="fb7c2-133">Para crear un paquete secundario para un software intermedio con composición dinámica Suite</span><span class="sxs-lookup"><span data-stu-id="fb7c2-133">To create a secondary package for middleware by using Dynamic Suite Composition</span></span>**

1.  <span data-ttu-id="fb7c2-134">En un equipo de secuencias que esté configurado con una imagen limpia, instale Application Virtualization Sequencer y guarde el estado del equipo.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-134">On a sequencing computer that is set up with a clean image, install Application Virtualization Sequencer and save the computer state.</span></span>

2.  <span data-ttu-id="fb7c2-135">Instale el middleware de forma local en el equipo de secuenciación y configúrelo.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-135">Install the middleware locally on the sequencing computer, and configure it.</span></span>

3.  <span data-ttu-id="fb7c2-136">Ordene la aplicación principal y guarde el paquete en la carpeta de contenido en el servidor.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-136">Sequence the primary application, and save the package to the Content folder on the server.</span></span>

4.  <span data-ttu-id="fb7c2-137">Restaure el equipo de secuenciación a su estado guardado en el paso 1.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-137">Restore the sequencing computer to its saved state from step 1.</span></span>

5.  <span data-ttu-id="fb7c2-138">Inicie el secuenciador para crear un nuevo paquete.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-138">Start the sequencer to create a new package.</span></span>

6.  <span data-ttu-id="fb7c2-139">Iniciar la fase de supervisión del secuenciador.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-139">Start the sequencer monitoring phase.</span></span>

7.  <span data-ttu-id="fb7c2-140">Instale la aplicación middleware en el equipo de secuenciación y configúrela como en una instalación típica.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-140">Install the middleware application on the sequencing computer, and configure it as in a typical installation.</span></span>

8.  <span data-ttu-id="fb7c2-141">Complete el proceso de secuenciación.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-141">Complete the sequencing process.</span></span>

9.  <span data-ttu-id="fb7c2-142">Guarde el paquete en la carpeta de contenido en el servidor.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-142">Save the package to the Content folder on the server.</span></span>

    <span data-ttu-id="fb7c2-143">**Nota:**  Para ayudar con la administración de paquetes secundarios, se recomienda que el nombre del paquete incluya el término "paquete secundario" para enfatizar que se trata de un paquete que no funcionará como una aplicación independiente, por ejemplo, un **paquete secundario de \ [nombre del middleware \]**.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-143">**Note** To assist with management of secondary packages, it is recommended that the package name include the term “Secondary package” to emphasize that this is a package that will not function as a stand-alone application—for example, **\[Middleware Name\] Secondary package**.</span></span>

     

**<span data-ttu-id="fb7c2-144">Para definir la dependencia en el paquete principal</span><span class="sxs-lookup"><span data-stu-id="fb7c2-144">To define the dependency in the primary package</span></span>**

1. <span data-ttu-id="fb7c2-145">En el servidor, abra el archivo OSD del paquete secundario para su edición.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-145">On the server, open the OSD file of the secondary package for editing.</span></span> <span data-ttu-id="fb7c2-146">(Es una buena idea usar un editor XML para realizar cambios en el archivo OSD; sin embargo, puede usar el Bloc de notas como alternativa).</span><span class="sxs-lookup"><span data-stu-id="fb7c2-146">(It is a good idea to use an XML editor to make changes to the OSD file; however, you can use Notepad as an alternative.)</span></span>

2. <span data-ttu-id="fb7c2-147">Copie la línea **href del código base** desde ese archivo.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-147">Copy the **CODEBASE HREF** line from that file.</span></span>

3. <span data-ttu-id="fb7c2-148">Abra el archivo OSD del paquete principal para su edición.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-148">Open the OSD file of the primary package for editing.</span></span>

4. <span data-ttu-id="fb7c2-149">Inserte la <strong> &lt; etiqueta dependencies &gt; </strong> después de cerrar la etiqueta \*\* &lt; /ENVLIST &gt; \*\* al final de la sección \*\* &lt; VIRTUALENV &gt; \*\* justo antes de la etiqueta \*\* &lt; /VIRTUALENV &gt; \*\* .</span><span class="sxs-lookup"><span data-stu-id="fb7c2-149">Insert the <strong>&lt;DEPENDENCIES&gt;</strong>tag after the close of **&lt;/ENVLIST&gt;** tag at the end of the **&lt;VIRTUALENV&gt;** section just before the **&lt;/VIRTUALENV&gt;** tag.</span></span>

5. <span data-ttu-id="fb7c2-150">Pegue la línea **href de código base** desde el paquete secundario después de la etiqueta de \*\* &lt; &gt; dependencias\*\* que acaba de crear.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-150">Paste the **CODEBASE HREF** line from the secondary package after the **&lt;DEPENDENCIES&gt;** tag you just created.</span></span>

6. <span data-ttu-id="fb7c2-151">Si el paquete secundario es un paquete obligatorio, lo que significa que debe iniciarse antes de que se inicie el paquete principal, agregue la propiedad **obligatoria = "true"** dentro de la etiqueta **codebase** .</span><span class="sxs-lookup"><span data-stu-id="fb7c2-151">If the secondary package is a mandatory package, which means that it must be started before the primary package is started, add the **MANDATORY=”TRUE”** property inside the **CODEBASE** tag.</span></span> <span data-ttu-id="fb7c2-152">Si no es obligatoria, se puede omitir la propiedad.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-152">If it is not mandatory, the property can be omitted.</span></span>

7. <span data-ttu-id="fb7c2-153">Para cerrar la etiqueta \*\* &lt; dependencies &gt; \*\* , inserte lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fb7c2-153">Close the **&lt;DEPENDENCIES&gt;** tag by inserting the following:</span></span>

   **<span data-ttu-id="fb7c2-154">&lt;/DEPENDENCIES&gt;</span><span class="sxs-lookup"><span data-stu-id="fb7c2-154">&lt;/DEPENDENCIES&gt;</span></span>**

8. <span data-ttu-id="fb7c2-155">Revise los cambios realizados en el archivo OSD y, a continuación, guarde y cierre el archivo.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-155">Review the changes that you made to the OSD file, and then save and close the file.</span></span> <span data-ttu-id="fb7c2-156">En el ejemplo siguiente se muestra cómo debería aparecer la sección agregada.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-156">The following example shows how the added section should appear.</span></span> <span data-ttu-id="fb7c2-157">Los valores de la etiqueta que se muestran aquí solo son por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-157">The tag values shown here are for example only.</span></span>

   **<span data-ttu-id="fb7c2-158">&lt;VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="fb7c2-158">&lt;VIRTUALENV&gt;</span></span>**

        **&lt;ENVLIST&gt;**

   **<span data-ttu-id="fb7c2-159">…</span><span class="sxs-lookup"><span data-stu-id="fb7c2-159">…</span></span>**

        **&lt;/ENVLIST&gt;**

        **&lt;DEPENDENCIES&gt;**

             **&lt;CODEBASE HREF="rtsp://virt\_apps/package.1/package.1.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.1\\osguard.cp"/&gt;**

             **&lt;CODEBASE HREF="rtsp://sample\_apps/package.2/sample.sft" GUID="D54C80FA-9DFF-459D-AA33-DD852C9FBFBA" SYSGUARDFILE="package.2\\osguard.cp" MANDATORY="TRUE" /&gt;**

        **&lt;/DEPENDENCIES&gt;**

   **<span data-ttu-id="fb7c2-160">&lt;/VIRTUALENV&gt;</span><span class="sxs-lookup"><span data-stu-id="fb7c2-160">&lt;/VIRTUALENV&gt;</span></span>**

9. <span data-ttu-id="fb7c2-161">Si el paquete secundario tiene entradas en la sección \*\* &lt; ENVLIST &gt; \*\* del archivo OSD, debe copiarlas en la misma sección del paquete principal.</span><span class="sxs-lookup"><span data-stu-id="fb7c2-161">If the secondary package has any entries in the **&lt;ENVLIST&gt;** section of the OSD file, you must copy those entries to the same section in the primary package.</span></span>

## <span data-ttu-id="fb7c2-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb7c2-162">Related topics</span></span>


[<span data-ttu-id="fb7c2-163">Cómo crear o actualizar aplicaciones virtuales con el secuenciador de App-V</span><span class="sxs-lookup"><span data-stu-id="fb7c2-163">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





