---
title: Notas de la versión de App-V 4.6 SP1
description: Notas de la versión de App-V 4.6 SP1
author: dansimp
ms.assetid: aeb6784a-864a-4f4e-976b-40c34dcfd8d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7081aaf4a04d52bf288d7a76b4a488e2b200c3d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819840"
---
# <span data-ttu-id="62ed6-103">Notas de la versión de App-V 4.6 SP1</span><span class="sxs-lookup"><span data-stu-id="62ed6-103">App-V 4.6 SP1 Release Notes</span></span>


<span data-ttu-id="62ed6-104">Para buscar estas notas de la versión, presione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="62ed6-104">To search these Release Notes, press CTRL+F.</span></span>

<span data-ttu-id="62ed6-105">**Importante**  Lea estas notas de la versión minuciosamente antes de instalar el sistema de administración de Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="62ed6-105">**Important** Read these Release Notes thoroughly before you install the Microsoft Application Virtualization (App-V) Management System.</span></span> <span data-ttu-id="62ed6-106">Estas notas de la versión contienen información que le ayudará a instalar correctamente Application Virtualization (App-V) 4.6 SP1.</span><span class="sxs-lookup"><span data-stu-id="62ed6-106">These Release Notes contain information that helps you successfully install Application Virtualization (App-V)4.6 SP1.</span></span> <span data-ttu-id="62ed6-107">Este documento contiene información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="62ed6-107">This document contains information that is not available in the product documentation.</span></span> <span data-ttu-id="62ed6-108">Si hay una diferencia entre estas notas de la versión y otra documentación de App-V, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="62ed6-108">If there is a difference between these Release Notes and other App-V documentation, the latest change should be considered authoritative.</span></span>

 

## <span data-ttu-id="62ed6-109">Protegerse contra virus y vulnerabilidades de seguridad</span><span class="sxs-lookup"><span data-stu-id="62ed6-109">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="62ed6-110">Para ayudar a protegerse contra virus y vulnerabilidades de seguridad, es importante instalar las últimas actualizaciones de seguridad disponibles para cualquier nuevo software que se instale.</span><span class="sxs-lookup"><span data-stu-id="62ed6-110">To help protect against security vulnerabilities and viruses, it is important to install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="62ed6-111">Para obtener más información, consulte el [sitio web de seguridad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="62ed6-111">For more information, see the [Microsoft Security website](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="62ed6-112">Problemas conocidos con Application Virtualization 4.6 SP1</span><span class="sxs-lookup"><span data-stu-id="62ed6-112">Known Issues with Application Virtualization4.6 SP1</span></span>


<span data-ttu-id="62ed6-113">Esta sección proporciona la información más actualizada sobre problemas con Microsoft Application Virtualization (App-V) 4.6 SP1.</span><span class="sxs-lookup"><span data-stu-id="62ed6-113">This section provides the most up-to-date information about issues with Microsoft Application Virtualization (App-V)4.6 SP1.</span></span> <span data-ttu-id="62ed6-114">Estos problemas no aparecen en la documentación del producto y, en algunos casos, podrían contradecir la documentación del producto existente.</span><span class="sxs-lookup"><span data-stu-id="62ed6-114">These issues do not appear in the product documentation and in some cases might contradict existing product documentation.</span></span> <span data-ttu-id="62ed6-115">Cuando sea posible, estos problemas se resolverán en versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="62ed6-115">When it is possible, these issues will be addressed in later releases.</span></span>

### <span data-ttu-id="62ed6-116">La ruta de acceso de SPRT se pierde si no termina en una barra diagonal (/)</span><span class="sxs-lookup"><span data-stu-id="62ed6-116">Path from SPRT is lost if it does not end in forward slash ( / )</span></span>

<span data-ttu-id="62ed6-117">Cuando la ruta de un elemento HREF de una plantilla de proyecto no termina con una barra diagonal ( **/** ), el href generado no incluye la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="62ed6-117">When the path in an HREF in a project template does not end with a forward slash (**/**), the generated HREF does not include the path.</span></span> <span data-ttu-id="62ed6-118">Esto sucede cuando el usuario manipula manualmente el archivo **. SPRT** .</span><span class="sxs-lookup"><span data-stu-id="62ed6-118">This occurs when the user manually manipulates the **.sprt** file.</span></span> <span data-ttu-id="62ed6-119">Si usa el secuenciador, siempre agrega la barra diagonal ( **/** ) después de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="62ed6-119">If you use the sequencer it always adds the forward slash (**/**) after the path.</span></span>

<span data-ttu-id="62ed6-120">Solución Asegúrese de que la HREF tenga una barra diagonal hacia adelante ( **/** ).</span><span class="sxs-lookup"><span data-stu-id="62ed6-120">WORKAROUND Make sure that the HREF has a trailing forward slash (**/**).</span></span>

### <span data-ttu-id="62ed6-121">El nombre de la carpeta de usuario no se corresponde con el nombre del paquete</span><span class="sxs-lookup"><span data-stu-id="62ed6-121">User folder name do not correspond to the package name</span></span>

<span data-ttu-id="62ed6-122">Las carpetas que contienen archivos. pkg y de usuario ya no incluyen el nombre del paquete.</span><span class="sxs-lookup"><span data-stu-id="62ed6-122">Folders that contain user and global .pkg files no longer include the package name.</span></span> <span data-ttu-id="62ed6-123">Anteriormente, el cliente de App-V usaba el nombre corto de la 8,3 carpeta raíz del paquete como parte del nombre de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="62ed6-123">Previously, the App-V client used to use the package root folder 8.3 short name as part of the folder name.</span></span> <span data-ttu-id="62ed6-124">Esto te permite identificarlo fácilmente.</span><span class="sxs-lookup"><span data-stu-id="62ed6-124">This lets you easily identify it.</span></span> <span data-ttu-id="62ed6-125">Cuando usas el secuenciador App-V 4,6 SP1, los nombres cortos de la 8,3 carpeta raíz del paquete son ahora cadenas aleatorias.</span><span class="sxs-lookup"><span data-stu-id="62ed6-125">When you use the App-V 4.6 SP1 sequencer, the package root folder 8.3 short names are now random strings.</span></span> <span data-ttu-id="62ed6-126">Esto dificulta la identificación de las carpetas que contienen los archivos **. pkg** del paquete en el equipo en el que se ejecuta el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="62ed6-126">This makes it difficult to identify the folders that contain the package’s **.pkg** files on the computer that is running the App-V client.</span></span>

<span data-ttu-id="62ed6-127">SOLUCIÓN use uno de los siguientes métodos para identificar más fácilmente estas carpetas de paquetes:</span><span class="sxs-lookup"><span data-stu-id="62ed6-127">WORKAROUND Use one of the following methods to more easily identify these package folders:</span></span>

1.  <span data-ttu-id="62ed6-128">Cuando cree el paquete mediante el secuenciador, especifique un nombre de carpeta que siga la Convención de nomenclatura de 8,3 para la carpeta principal de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="62ed6-128">When you create the package by using the Sequencer, specify a folder name that follows the 8.3 naming convention for the primary application folder.</span></span> <span data-ttu-id="62ed6-129">Este nombre se usará como parte del nombre de la carpeta de usuario tal y como se mostraba en App-V 4,6.</span><span class="sxs-lookup"><span data-stu-id="62ed6-129">This name will then be used as part of the user folder name as was the case in App-V 4.6.</span></span>

2.  <span data-ttu-id="62ed6-130">El archivo. SPRJ contiene ahora una etiqueta que muestra la cadena que se usa como el principio del nombre de la carpeta de usuario.</span><span class="sxs-lookup"><span data-stu-id="62ed6-130">The .sprj file now contains a tag that displays the string that is used as the beginning of the user folder name.</span></span> <span data-ttu-id="62ed6-131">Puedes usar el elemento **SHORTNAME** del elemento **PACKAGEROOTFOLDER** para determinar el nombre.</span><span class="sxs-lookup"><span data-stu-id="62ed6-131">You can use the **SHORTNAME** element of the **PACKAGEROOTFOLDER** element to determine the name.</span></span>

### <span data-ttu-id="62ed6-132">Ejecución de App-V 4,6 SP1 en equipos con más de 64 procesadores</span><span class="sxs-lookup"><span data-stu-id="62ed6-132">Running App-V 4.6 SP1 on computers that have more than 64 processors</span></span>

<span data-ttu-id="62ed6-133">Cuando ejecuta App-V 4,6 SP1 en equipos que tienen más de 64 procesadores instalados, se produce un error en el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="62ed6-133">When you run App-V 4.6 SP1 on computers that have more than 64 processors installed, the App-V client fails.</span></span>

<span data-ttu-id="62ed6-134">SOLUCIÓN ninguna.</span><span class="sxs-lookup"><span data-stu-id="62ed6-134">WORKAROUND None.</span></span> <span data-ttu-id="62ed6-135">Esta configuración no es compatible.</span><span class="sxs-lookup"><span data-stu-id="62ed6-135">This configuration is not supported.</span></span> <span data-ttu-id="62ed6-136">Debe ejecutar los equipos con App-V 4,6 SP1on que tengan menos de 64 procesadores.</span><span class="sxs-lookup"><span data-stu-id="62ed6-136">You must run App-V 4.6 SP1on computers that have fewer than 64 processors.</span></span>

### <span data-ttu-id="62ed6-137">La actualización de Application Virtualization 4,6 SP1 no se ofrece en todas las configuraciones regionales que usan Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="62ed6-137">Application Virtualization 4.6 SP1 update is not offered on all locales that use Microsoft Update</span></span>

<span data-ttu-id="62ed6-138">Cuando usa Microsoft Update, la actualización de App-V 4,6 SP1 no está disponible para las siguientes configuraciones regionales de idioma:</span><span class="sxs-lookup"><span data-stu-id="62ed6-138">When you use Microsoft Update, the update for App-V 4.6 SP1 is not available for the following language locales:</span></span>

-   <span data-ttu-id="62ed6-139">Kazajo</span><span class="sxs-lookup"><span data-stu-id="62ed6-139">Kazakh</span></span>

-   <span data-ttu-id="62ed6-140">Hindi</span><span class="sxs-lookup"><span data-stu-id="62ed6-140">Hindi</span></span>

-   <span data-ttu-id="62ed6-141">Serbio-cirílico</span><span class="sxs-lookup"><span data-stu-id="62ed6-141">Serbian-Cyrillic</span></span>

<span data-ttu-id="62ed6-142">SOLUCIÓN alternativa si usa Microsoft Windows Server Update Services (WSUS), use la versión en Inglés de la actualización o descargue la actualización desde el catálogo de Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="62ed6-142">WORKAROUND If you are using Microsoft Windows Server Update Services (WSUS) use the English version of the update or download the update from the Microsoft Update Catalog.</span></span>

### <span data-ttu-id="62ed6-143">Después de expandir el paquete primario, no se puede secuenciar un complemento con componentes en paralelo</span><span class="sxs-lookup"><span data-stu-id="62ed6-143">After expanding the parent package, you cannot sequence a plug-in with side by side components</span></span>

<span data-ttu-id="62ed6-144">Al expandir un paquete principal con herramientas que **Tools**  /  **expanda el paquete a un sistema local** en la consola del secuenciador de App-V y se secuencia un complemento con componentes en paralelo, se devolverá un error de instalación.</span><span class="sxs-lookup"><span data-stu-id="62ed6-144">When you expand a parent package by using **Tools** / **Expand Package to Local System** in the App-V Sequencer console and you sequence a plug-in with side by side components, an installation error is returned.</span></span> <span data-ttu-id="62ed6-145">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="62ed6-145">For example:</span></span>

-   **<span data-ttu-id="62ed6-146">HRESULT 0x80073712</span><span class="sxs-lookup"><span data-stu-id="62ed6-146">HRESULT 0x80073712</span></span>**

<span data-ttu-id="62ed6-147">Esto se debe a que el secuenciador escribe el componente en paralelo en el registro, pero no borra el valor de la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="62ed6-147">This is caused when the sequencer writes the side-by-side component to the registry but does not clear the value for the following registry key:</span></span>

<span data-ttu-id="62ed6-148">HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty</span><span class="sxs-lookup"><span data-stu-id="62ed6-148">HKEY\_LOCAL\_MACHINE\\COMPONENTS\\StoreDirty</span></span>

<span data-ttu-id="62ed6-149">SOLUCIÓN alternativa después de expandir el paquete principal en el equipo que ejecuta el secuenciador, tiene que eliminar el valor de la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="62ed6-149">WORKAROUND After expanding the parent package on the computer that is running the sequencer, you have to delete the value for the following registry key:</span></span>

<span data-ttu-id="62ed6-150">HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty</span><span class="sxs-lookup"><span data-stu-id="62ed6-150">HKEY\_LOCAL\_MACHINE\\COMPONENTS\\StoreDirty</span></span>

<span data-ttu-id="62ed6-151">Una vez que haya eliminado el valor, ordene el complemento.</span><span class="sxs-lookup"><span data-stu-id="62ed6-151">After you have deleted the value, sequence the plug-in.</span></span>

### <span data-ttu-id="62ed6-152">Información de copyright de notas de versión</span><span class="sxs-lookup"><span data-stu-id="62ed6-152">Release Notes Copyright Information</span></span>

<span data-ttu-id="62ed6-153">Este documento se proporciona "tal cual".</span><span class="sxs-lookup"><span data-stu-id="62ed6-153">This document is provided “as-is”.</span></span> <span data-ttu-id="62ed6-154">La información y las vistas expresadas en este documento, como direcciones URL y otras referencias de sitios web de Internet, pueden cambiar sin previo aviso.</span><span class="sxs-lookup"><span data-stu-id="62ed6-154">Information and views expressed in this document, such as URL and other Internet website references, may change without notice.</span></span> <span data-ttu-id="62ed6-155">Usted asume el riesgo de su uso.</span><span class="sxs-lookup"><span data-stu-id="62ed6-155">You bear the risk of using it.</span></span>

<span data-ttu-id="62ed6-156">Algunos ejemplos que se describen en este artículo se proporcionan solo para la ilustración y son ficticios.</span><span class="sxs-lookup"><span data-stu-id="62ed6-156">Some examples depicted herein are provided for illustration only and are fictitious.</span></span> <span data-ttu-id="62ed6-157">No se pretende ni se debe deducir ninguna asociación o conexión real.</span><span class="sxs-lookup"><span data-stu-id="62ed6-157">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="62ed6-158">Este documento no le proporciona derechos legales sobre ninguna propiedad intelectual en ningún producto de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62ed6-158">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="62ed6-159">Puede copiar y usar este documento para su referencia interna.</span><span class="sxs-lookup"><span data-stu-id="62ed6-159">You may copy and use this document for your internal, reference purposes.</span></span> <span data-ttu-id="62ed6-160">Puede modificar este documento para su referencia interna.</span><span class="sxs-lookup"><span data-stu-id="62ed6-160">You may modify this document for your internal, reference purposes.</span></span>



<span data-ttu-id="62ed6-161">Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server y Windows Vista son marcas comerciales del grupo de empresas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="62ed6-161">Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server, and Windows Vista are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="62ed6-162">El resto de marcas comerciales pertenecen a sus respectivos dueños.</span><span class="sxs-lookup"><span data-stu-id="62ed6-162">All other trademarks are property of their respective owners.</span></span>

 

 





