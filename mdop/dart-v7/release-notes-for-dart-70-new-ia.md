---
title: Notas de la versión de DaRT 7.0
description: Notas de la versión de DaRT 7.0
author: dansimp
ms.assetid: fad227d0-5c22-4efd-9187-0e5922f7250b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5114acfe5a46a2c78f722a2bb6394c0dbef55dd4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822761"
---
# <span data-ttu-id="73a24-103">Notas de la versión de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="73a24-103">Release Notes for DaRT 7.0</span></span>


**<span data-ttu-id="73a24-104">Para buscar estas notas de la versión, presione CTRL + F.</span><span class="sxs-lookup"><span data-stu-id="73a24-104">To search these release notes, press CTRL+F.</span></span>**

<span data-ttu-id="73a24-105">Lea estas notas de la versión minuciosamente antes de instalar Microsoft Diagnostics and Recovery Toolset (DaRT) 7.</span><span class="sxs-lookup"><span data-stu-id="73a24-105">Read these release notes thoroughly before you install Microsoft Diagnostics and Recovery Toolset (DaRT)7.</span></span>

## <span data-ttu-id="73a24-106">Acerca del conjunto de herramientas de diagnóstico y recuperación de Microsoft 7,0</span><span class="sxs-lookup"><span data-stu-id="73a24-106">About Microsoft Diagnostics and Recovery Toolset 7.0</span></span>


<span data-ttu-id="73a24-107">Estas notas de la versión contienen información necesaria para instalar DaRT7 correctamente y contienen información que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="73a24-107">These release notes contain information that is required to successfully install DaRT7 and contain information that is not available in the product documentation.</span></span> <span data-ttu-id="73a24-108">Si hay una diferencia entre estas notas de la versión y otra documentación de la plataforma DaRT, el último cambio debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="73a24-108">If there is a difference between these release notes and other DaRT platform documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="73a24-109">Estas notas de la versión reemplazan al contenido incluido en este producto.</span><span class="sxs-lookup"><span data-stu-id="73a24-109">These release notes supersede the content included with this product.</span></span>

## <span data-ttu-id="73a24-110">Acerca de la documentación del producto</span><span class="sxs-lookup"><span data-stu-id="73a24-110">About the Product Documentation</span></span>


<span data-ttu-id="73a24-111">La documentación de Microsoft Diagnostics and Recovery Toolset (DaRT) 7 se distribuye con el producto y en el sitio de Connect.</span><span class="sxs-lookup"><span data-stu-id="73a24-111">Documentation for Microsoft Diagnostics and Recovery Toolset (DaRT)7 is distributed with the product and on the Connect site.</span></span>

<span data-ttu-id="73a24-112">Para obtener ayuda detallada sobre cómo usar las herramientas de DaRT7, vea el archivo de ayuda disponible en el menú conjunto de herramientas de **diagnóstico y recuperación** .</span><span class="sxs-lookup"><span data-stu-id="73a24-112">For detailed help about how to use the tools in DaRT7, see the Help file available on the **Diagnostics and Recovery Toolset** menu.</span></span>

## <span data-ttu-id="73a24-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73a24-113">Providing feedback</span></span>


<span data-ttu-id="73a24-114">Nos interesan tus comentarios en DaRT7.</span><span class="sxs-lookup"><span data-stu-id="73a24-114">We are interested in your feedback on DaRT7.</span></span> <span data-ttu-id="73a24-115">Puedes enviar tus comentarios a dart7feedback@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="73a24-115">You can send your feedback to dart7feedback@microsoft.com.</span></span> <span data-ttu-id="73a24-116">Esta dirección de correo electrónico no es un canal de soporte técnico, pero sus comentarios nos ayudarán a planear los cambios futuros de estas herramientas para que le resulten más útiles en el futuro.</span><span class="sxs-lookup"><span data-stu-id="73a24-116">This email address is not a support channel, but your feedback will help us to plan future changes for these tools to make them more useful to you in the future.</span></span>

## <span data-ttu-id="73a24-117">Protegerse contra virus y vulnerabilidades de seguridad</span><span class="sxs-lookup"><span data-stu-id="73a24-117">Protect Against Security Vulnerabilities and Viruses</span></span>


<span data-ttu-id="73a24-118">Para ayudarle a protegerse contra virus y vulnerabilidades de seguridad, le recomendamos que instale las últimas actualizaciones de seguridad disponibles para cualquier software nuevo que se instale.</span><span class="sxs-lookup"><span data-stu-id="73a24-118">To help protect against security vulnerabilities and viruses, we recommend that you install the latest available security updates for any new software being installed.</span></span> <span data-ttu-id="73a24-119">Para obtener más información, consulte [seguridad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .</span><span class="sxs-lookup"><span data-stu-id="73a24-119">For more information, see [Microsoft Security](https://go.microsoft.com/fwlink/?LinkId=3482) (https://go.microsoft.com/fwlink/?LinkId=3482).</span></span>

## <span data-ttu-id="73a24-120">Problemas conocidos con DaRT 7,0</span><span class="sxs-lookup"><span data-stu-id="73a24-120">Known Issues with DaRT 7.0</span></span>


### <span data-ttu-id="73a24-121">No se puede iniciar el examen de SFC si el sistema de limpieza independiente está abierto</span><span class="sxs-lookup"><span data-stu-id="73a24-121">SFC Scan cannot start if Standalone System Sweeper is open</span></span>

<span data-ttu-id="73a24-122">Si el sistema de limpieza independiente se está ejecutando, el examen de SFC no puede iniciarse ni ejecutarse debido a un conflicto de recursos entre las dos herramientas.</span><span class="sxs-lookup"><span data-stu-id="73a24-122">If the Standalone System Sweeper is running, SFC Scan cannot start or run because of a resource conflict between the two tools.</span></span>

<span data-ttu-id="73a24-123">**Solución alternativa:** Cierre el sistema independiente de limpieza antes de intentar abrir o ejecutar la herramienta de análisis de SFC.</span><span class="sxs-lookup"><span data-stu-id="73a24-123">**Workaround:** Close the Standalone System Sweeper before you try to open or run the SFC Scan tool.</span></span>

### <span data-ttu-id="73a24-124">Es posible que los caracteres Unicode no se muestren en los nombres de archivo</span><span class="sxs-lookup"><span data-stu-id="73a24-124">Unicode characters may not be displayed in file names</span></span>

<span data-ttu-id="73a24-125">Si elimina un archivo que tiene caracteres Unicode en el nombre de archivo e intenta restaurar el archivo con la herramienta de restauración de archivos, no se encuentra el archivo.</span><span class="sxs-lookup"><span data-stu-id="73a24-125">If you delete a file that has Unicode characters in its file name and try to restore the file by using the File Restore tool, the file is not found.</span></span> <span data-ttu-id="73a24-126">Esto solo se produce cuando usa caracteres de un idioma distinto del idioma del DVD de Windows que se usó para crear la imagen de recuperación.</span><span class="sxs-lookup"><span data-stu-id="73a24-126">This only occurs when you use characters from a language other than the language of the Windows DVD that was used to create the recovery image.</span></span>

<span data-ttu-id="73a24-127">**Solución alternativa:** Asegúrese de que el idioma que usa DaRT coincida con el idioma que usa el sistema operativo desde el que está intentando restaurar los archivos.</span><span class="sxs-lookup"><span data-stu-id="73a24-127">**Workaround:** Make sure that the language that is used by DaRT matches the language that is used by the operating system from which it is trying to restore files.</span></span>

### <span data-ttu-id="73a24-128">La instalación de la línea de comandos de DaRT puede fallar silenciosamente</span><span class="sxs-lookup"><span data-stu-id="73a24-128">DaRT command-line installation may fail silently</span></span>

<span data-ttu-id="73a24-129">Se produce un error en la instalación de línea de comandos de DaRT si se ejecuta con el modo silencioso, a menos que se ejecute con permisos de administrador elevados.</span><span class="sxs-lookup"><span data-stu-id="73a24-129">DaRT command-line installation fails silently if run with the quiet mode option unless it is run by using elevated administrator permissions.</span></span>

<span data-ttu-id="73a24-130">**Solución alternativa:** Ejecute la instalación de línea de comandos con permisos elevados de administrador.</span><span class="sxs-lookup"><span data-stu-id="73a24-130">**Workaround:** Run the command-line installation by using elevated administrator permissions.</span></span> <span data-ttu-id="73a24-131">La instalación de DaRT es compatible con las opciones típicas de Windows Installer para la instalación desde la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="73a24-131">DaRT installation supports the typical Windows Installer options for command-line installation.</span></span> <span data-ttu-id="73a24-132">Para obtener más información sobre los distintos modificadores disponibles, consulte [las opciones](https://go.microsoft.com/fwlink/?LinkId=160689) de la línea de comandos de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="73a24-132">Please see [Command-Line Options](https://go.microsoft.com/fwlink/?LinkId=160689) for Windows Installer for more information about the several available switches.</span></span>

### <span data-ttu-id="73a24-133">La búsqueda de archivos no puede mover una carpeta a un volumen diferente</span><span class="sxs-lookup"><span data-stu-id="73a24-133">File Search cannot move a folder to a different volume</span></span>

<span data-ttu-id="73a24-134">El movimiento de carpetas entre volúmenes no es compatible con la aplicación de búsqueda de archivos.</span><span class="sxs-lookup"><span data-stu-id="73a24-134">Moving folders between volumes is not supported by the File Search application.</span></span> <span data-ttu-id="73a24-135">Si intenta mover una carpeta a un volumen diferente en la búsqueda de archivos, se devuelve el siguiente error: "se ha producido un error al escribir el \* &lt; nombre &gt; \*de archivo del archivo.</span><span class="sxs-lookup"><span data-stu-id="73a24-135">If you try to move a folder to a different volume in File Search, the following error is returned: "An error occurred while writing the file *&lt;filename&gt;*.</span></span> <span data-ttu-id="73a24-136">Asegúrese de que la unidad tiene suficiente espacio y que la ruta de destino es accesible.</span><span class="sxs-lookup"><span data-stu-id="73a24-136">Make sure that the drive has sufficient space and the destination path is accessible."</span></span>

<span data-ttu-id="73a24-137">**Solución alternativa:** Use el explorador para mover una carpeta a un volumen diferente.</span><span class="sxs-lookup"><span data-stu-id="73a24-137">**Workaround:** Use the Explorer to move a folder to a different volume.</span></span>

### <span data-ttu-id="73a24-138">Es posible que algunos datos no estén disponibles en los equipos en los que se reasignan las letras de unidad</span><span class="sxs-lookup"><span data-stu-id="73a24-138">Some data may not be available on computers where the drive letters are remapped</span></span>

<span data-ttu-id="73a24-139">Este problema puede ocurrir en equipos habilitados para BitLocker y equipos de inicio múltiple.</span><span class="sxs-lookup"><span data-stu-id="73a24-139">This problem can occur on BitLocker-enabled computers and multiboot computers.</span></span> <span data-ttu-id="73a24-140">Esto se debe a que parte de la información del registro sin conexión tiene Letras de unidad no modificables y DaRT usa diferentes letras para los mismos volúmenes.</span><span class="sxs-lookup"><span data-stu-id="73a24-140">This occurs because some information in the offline registry has hard-coded drive letters, and DaRT uses different letters for the same volumes.</span></span> <span data-ttu-id="73a24-141">Entre los efectos típicos se incluyen no tener acceso a determinadas cuentas de usuario locales en el editor del registro.</span><span class="sxs-lookup"><span data-stu-id="73a24-141">The typical effects include not having access to certain local user accounts in Registry Editor.</span></span> <span data-ttu-id="73a24-142">Además, es posible que algunas herramientas no puedan obtener propiedades que dependan de la resolución de rutas de archivo.</span><span class="sxs-lookup"><span data-stu-id="73a24-142">Additionally, some tools may be unable to obtain properties that rely on resolving file paths.</span></span>

<span data-ttu-id="73a24-143">**Solución alternativa:** Use la opción para reasignar las letras de unidad como se inicia DaRT.</span><span class="sxs-lookup"><span data-stu-id="73a24-143">**Workaround:** Use the option to remap the drive letters as DaRT starts.</span></span> <span data-ttu-id="73a24-144">Normalmente, esto alinea las letras de unidad típicas con lo que se espera.</span><span class="sxs-lookup"><span data-stu-id="73a24-144">This usually aligns the typical drive letters to what is expected.</span></span>

### <span data-ttu-id="73a24-145">Es posible que el Hotfix desinstalado no desinstale determinadas actualizaciones</span><span class="sxs-lookup"><span data-stu-id="73a24-145">Hotfix Uninstall might not uninstall certain updates</span></span>

<span data-ttu-id="73a24-146">Algunas actualizaciones y Service Packs no se pueden desinstalar porque están marcados como desinstalables o porque es necesario desinstalarlos en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="73a24-146">Some updates and service packs cannot be uninstalled because they are marked as un-installable or because they need to be uninstalled from within Windows 7.</span></span> <span data-ttu-id="73a24-147">En estos casos, la herramienta de desinstalación de Hotfix puede indicar que estas actualizaciones se han desinstalado, aunque no se hayan realizado.</span><span class="sxs-lookup"><span data-stu-id="73a24-147">In these instances, the Hotfix Uninstall tool may indicate that these updates have been uninstalled even though they have not been.</span></span>

<span data-ttu-id="73a24-148">**Solución alternativa:** Desinstale estas actualizaciones problemáticas de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="73a24-148">**Workaround:** Uninstall these problematic updates from Windows 7.</span></span>

### <span data-ttu-id="73a24-149">Borrado de disco: no se pueden eliminar los discos con volúmenes distribuidos, volúmenes seccionados ni volúmenes reflejados</span><span class="sxs-lookup"><span data-stu-id="73a24-149">Disk Wipe: Disks with spanned volumes, striped volumes, or mirrored volumes cannot be deleted</span></span>

<span data-ttu-id="73a24-150">El borrado de disco no es compatible con la eliminación de discos distribuidos, reflejados o particionados en uno o más volúmenes.</span><span class="sxs-lookup"><span data-stu-id="73a24-150">Disk Wipe does not support deleting disks that are spanned, mirrored, or striped across one or more volumes.</span></span>

<span data-ttu-id="73a24-151">**Solución alternativa:** Seleccione y elimine cada disco del volumen por separado.</span><span class="sxs-lookup"><span data-stu-id="73a24-151">**Workaround:** Select and delete each disk in the volume separately.</span></span>

## <span data-ttu-id="73a24-152">Información de copyright de notas de versión</span><span class="sxs-lookup"><span data-stu-id="73a24-152">Release Notes Copyright Information</span></span>


<span data-ttu-id="73a24-153">Este documento se proporciona "tal cual".</span><span class="sxs-lookup"><span data-stu-id="73a24-153">This document is provided “as-is”.</span></span> <span data-ttu-id="73a24-154">La información y las vistas expresadas en este documento, incluidas las direcciones URL y otras referencias a sitios web de Internet, pueden cambiar sin previo aviso.</span><span class="sxs-lookup"><span data-stu-id="73a24-154">Information and views expressed in this document, including URL and other Internet website references, may change without notice.</span></span> <span data-ttu-id="73a24-155">Usted asume el riesgo de su uso.</span><span class="sxs-lookup"><span data-stu-id="73a24-155">You bear the risk of using it.</span></span>

<span data-ttu-id="73a24-156">Algunos ejemplos que se describen en este artículo se proporcionan solo para la ilustración y son ficticios.</span><span class="sxs-lookup"><span data-stu-id="73a24-156">Some examples depicted herein are provided for illustration only and are fictitious.</span></span><span data-ttu-id="73a24-157">No se pretende ni se debe deducir ninguna asociación o conexión real.</span><span class="sxs-lookup"><span data-stu-id="73a24-157">No real association or connection is intended or should be inferred.</span></span>

<span data-ttu-id="73a24-158">Este documento no le proporciona derechos legales sobre ninguna propiedad intelectual en ningún producto de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="73a24-158">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="73a24-159">Este documento es confidencial y propiedad de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="73a24-159">This document is confidential and proprietary to Microsoft.</span></span> <span data-ttu-id="73a24-160">Se revela y se puede usar únicamente en virtud de un contrato de no divulgación.</span><span class="sxs-lookup"><span data-stu-id="73a24-160">It is disclosed and can be used only pursuant to a nondisclosure agreement.</span></span>



<span data-ttu-id="73a24-161">Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer y Windows Vista son marcas comerciales del grupo de compañías Microsoft.</span><span class="sxs-lookup"><span data-stu-id="73a24-161">Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer, and Windows Vista are trademarks of the Microsoft group of companies.</span></span>

<span data-ttu-id="73a24-162">El resto de marcas comerciales pertenecen a sus respectivos dueños.</span><span class="sxs-lookup"><span data-stu-id="73a24-162">All other trademarks are property of their respective owners.</span></span>

## <span data-ttu-id="73a24-163">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73a24-163">Related topics</span></span>


[<span data-ttu-id="73a24-164">Acerca de DaRT 7.0</span><span class="sxs-lookup"><span data-stu-id="73a24-164">About DaRT 7.0</span></span>](about-dart-70-new-ia.md)

 

 





