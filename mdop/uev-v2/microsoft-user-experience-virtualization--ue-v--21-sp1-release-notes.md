---
title: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1 SP1
description: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1 SP1
author: dansimp
ms.assetid: 561988c4-cc5c-4e15-970b-16e942c8f2ef
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 03/30/2017
ms.openlocfilehash: 974914421c61c829b5a32e336bddf8ea1addf514
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825531"
---
# <span data-ttu-id="fb148-103">Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1 SP1</span><span class="sxs-lookup"><span data-stu-id="fb148-103">Microsoft User Experience Virtualization (UE-V) 2.1 SP1 Release Notes</span></span>


<span data-ttu-id="fb148-104">Para buscar las notas de la versión de virtualización de Microsoft User Experience Virtualization 2,1, presione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="fb148-104">To search Microsoft User Experience Virtualization 2.1 SP1 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="fb148-105">Debe leer estas notas de la versión minuciosamente antes de instalar UE-V.</span><span class="sxs-lookup"><span data-stu-id="fb148-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="fb148-106">Las notas de la versión contienen información necesaria para instalar correctamente la virtualización de la experiencia del usuario y contienen información adicional que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="fb148-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="fb148-107">Si hay diferencias entre estas notas de la versión y otra documentación de UE-V, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="fb148-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="fb148-108">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="fb148-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="fb148-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb148-109">Providing feedback</span></span>


<span data-ttu-id="fb148-110">Díganos lo que piensa sobre nuestra documentación de MDOP enviándonos sus comentarios y comentarios.</span><span class="sxs-lookup"><span data-stu-id="fb148-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="fb148-111">Envíe sus comentarios sobre la documentación a [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="fb148-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="fb148-112">Problemas conocidos de UE-V</span><span class="sxs-lookup"><span data-stu-id="fb148-112">UE-V known issues</span></span>


<span data-ttu-id="fb148-113">Esta sección contiene notas de la versión para la experiencia del usuario de virtualización de 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="fb148-113">This section contains release notes for User Experience Virtualization 2.1 SP1.</span></span>

### <span data-ttu-id="fb148-114">Configuración de UE-V las plantillas de ubicación de Skype hacen que Skype se bloquee</span><span class="sxs-lookup"><span data-stu-id="fb148-114">UE-V settings location templates for Skype cause Skype to crash</span></span>

<span data-ttu-id="fb148-115">Cuando un usuario genera una plantilla de ubicación de configuración válida para la aplicación de escritorio de Skype, la registra y, a continuación, inicia la aplicación de escritorio de Skype, Skype se bloquea.</span><span class="sxs-lookup"><span data-stu-id="fb148-115">When a user generates a valid settings location template for the Skype desktop application, registers it, and then launches the Skype desktop application, Skype crashes.</span></span> <span data-ttu-id="fb148-116">Un _VIOLATION de ACCESS se graba en el registro de eventos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fb148-116">An ACCESS\_VIOLATION is recorded in the Application Event Log.</span></span>

<span data-ttu-id="fb148-117">SOLUCIÓN alternativa: quite o anule el registro de la plantilla de Skype para que Skype pueda volver a trabajar.</span><span class="sxs-lookup"><span data-stu-id="fb148-117">WORKAROUND: Remove or unregister the Skype template to allow Skype to work again.</span></span>

### <span data-ttu-id="fb148-118">Los scripts existentes para instalaciones silenciosas de UE-V pueden fallar</span><span class="sxs-lookup"><span data-stu-id="fb148-118">Existing scripts for silent installations of UE-V may fail</span></span>

<span data-ttu-id="fb148-119">Dos cambios realizados en el instalador de UE-V pueden hacer que los scripts de instalación silenciosa que funcionaban en versiones anteriores de UE-V fallaran al instalar UE-V 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="fb148-119">Two changes made to the UE-V installer can cause silent installation scripts that worked for previous versions of UE-V to fail when installing UE-V 2.1 SP1.</span></span> <span data-ttu-id="fb148-120">La primera es un nuevo requisito que los usuarios deben aceptar los términos de licencia y aceptar o rechazar la participación en el programa para la mejora de la experiencia del usuario (CEIP), incluso durante una instalación silenciosa.</span><span class="sxs-lookup"><span data-stu-id="fb148-120">The first is a new requirement that users must accept the license terms and agree to or decline participation in the Customer Experience Improvement Program (CEIP), even during a silent installation.</span></span> <span data-ttu-id="fb148-121">El uso del parámetro/q ya no es suficiente para indicar la aceptación de los términos de licencia y el contrato para participar en el CEIP.</span><span class="sxs-lookup"><span data-stu-id="fb148-121">Using the /q parameter is no longer sufficient to indicate acceptance of the license terms and agreement to participate in CEIP.</span></span>

<span data-ttu-id="fb148-122">En segundo lugar, el instalador fuerza el reinicio del equipo después de instalar el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fb148-122">Second, the installer now forces a computer restart after installing the UE-V Agent.</span></span> <span data-ttu-id="fb148-123">Esto puede provocar errores en un script de instalación si no espera reiniciar (por ejemplo, instala el agente UE-V Agent en primer lugar y, después, instala inmediatamente el generador).</span><span class="sxs-lookup"><span data-stu-id="fb148-123">This can cause an install script to fail if it is not expecting the restart (for example, it installs the UE-V Agent first and then immediately installs the generator).</span></span>

<span data-ttu-id="fb148-124">SOLUCIÓN: el instalador de UE-V (. msi) tiene dos nuevos parámetros de la línea de comandos que admiten instalaciones silenciosas.</span><span class="sxs-lookup"><span data-stu-id="fb148-124">WORKAROUND: The UE-V installer (.msi) has two new command-line parameters that support silent installations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="fb148-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fb148-125">Parameter</span></span></th>
<th align="left"><span data-ttu-id="fb148-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb148-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="fb148-127">/ACCEPTLICENSETERMS = true</span><span class="sxs-lookup"><span data-stu-id="fb148-127">/ACCEPTLICENSETERMS=True</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb148-128">Establezca este parámetro en <strong> true </strong> para instalar UE-V silenciosamente.</span><span class="sxs-lookup"><span data-stu-id="fb148-128">Set this parameter to <strong>True</strong> to install UE-V silently.</span></span> <span data-ttu-id="fb148-129">Agregar este parámetro implica que el usuario acepta los términos de licencia de UE-V, que se encuentran de forma predeterminada:%ProgramFiles%\Microsoft User Experience Virtualization\Agent</span><span class="sxs-lookup"><span data-stu-id="fb148-129">Adding this parameter implies that the user accepts the UE-V license terms, which are found (by default) here: %ProgramFiles%\Microsoft User Experience Virtualization\Agent</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="fb148-130">/NORESTART</span><span class="sxs-lookup"><span data-stu-id="fb148-130">/NORESTART</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="fb148-131">Este parámetro impide el reinicio obligatorio una vez instalado el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fb148-131">This parameter prevents the mandatory restart after the UE-V agent is installed.</span></span> <span data-ttu-id="fb148-132">Un código devuelto de 3010 indica que es necesario reiniciar antes de usar UE-V.</span><span class="sxs-lookup"><span data-stu-id="fb148-132">A return code of 3010 indicates that a restart is required prior to using UE-V.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="fb148-133">La configuración del registro no se sincroniza entre App-V y aplicaciones nativas en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="fb148-133">Registry settings do not synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="fb148-134">Cuando un equipo tiene una aplicación que se instala a través de virtualización de aplicaciones (App-V) y de forma local con un archivo de Windows Installer (. msi), la configuración basada en el registro no se sincroniza entre las tecnologías.</span><span class="sxs-lookup"><span data-stu-id="fb148-134">When a computer has an application that is installed through both Application Virtualization (App-V) and locally with a Windows Installer (.msi) file, the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="fb148-135">SOLUCIÓN alternativa: para resolver este problema, ejecute la aplicación seleccionando una de las dos tecnologías, pero no ambas.</span><span class="sxs-lookup"><span data-stu-id="fb148-135">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <span data-ttu-id="fb148-136">Resultados imprevisibles con Office 2010 y Office 2013 instalados</span><span class="sxs-lookup"><span data-stu-id="fb148-136">Unpredictable results with both Office 2010 and Office 2013 installed</span></span>

<span data-ttu-id="fb148-137">Cuando un usuario tiene instalado Office 2010 y Office 2013, cualquier configuración común entre las dos versiones de Office se desplazará con UE-V.</span><span class="sxs-lookup"><span data-stu-id="fb148-137">When a user has both Office 2010 and Office 2013 installed, any common settings between the two versions of Office are roamed by UE-V.</span></span> <span data-ttu-id="fb148-138">Esto puede provocar que el tamaño del paquete de Office 2010 sea muy grande o que se produzcan conflictos imprevisibles con 2013, especialmente si se usa Office 365.</span><span class="sxs-lookup"><span data-stu-id="fb148-138">This could cause the Office 2010 package size to be quite large or result in unpredictable conflicts with 2013, particularly if Office 365 is used.</span></span>

<span data-ttu-id="fb148-139">SOLUCIÓN alternativa: instale solo una versión de Office o limite las configuraciones que se sincronizan mediante UE-V.</span><span class="sxs-lookup"><span data-stu-id="fb148-139">WORKAROUND: Install only one version of Office or limit which settings are synchronized by UE-V.</span></span>

### <span data-ttu-id="fb148-140">Desinstalar y volver a instalar la aplicación Windows 8 revierte la configuración al estado inicial</span><span class="sxs-lookup"><span data-stu-id="fb148-140">Uninstall and re-install of Windows 8 app reverts settings to initial state</span></span>

<span data-ttu-id="fb148-141">Al usar la sincronización de configuración de UE-V para una aplicación de Windows 8, si el usuario desinstala la aplicación y, a continuación, vuelve a instalar la aplicación, la configuración de la aplicación vuelve a sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="fb148-141">While using UE-V settings synchronization for a Windows 8 app, if the user uninstalls the app and then reinstalls the app, the app’s settings revert to their default values.</span></span><span data-ttu-id="fb148-142">Esto sucede porque la desinstalación quita la copia local (en caché) de la configuración de la aplicación, pero no quita el paquete de configuración local de UE-V.</span><span class="sxs-lookup"><span data-stu-id="fb148-142"> This happens because the uninstall removes the local (cached) copy of the app’s settings but does not remove the local UE-V settings package.</span></span><span data-ttu-id="fb148-143">Cuando la aplicación se reinstale e inicie, UE-V reúna la configuración de la aplicación que se restableció a los valores predeterminados de la aplicación y, a continuación, cargará la configuración predeterminada en la ubicación de almacenamiento central.</span><span class="sxs-lookup"><span data-stu-id="fb148-143"> When the app is reinstalled and launched, UE-V gather the app settings that were reset to the app defaults and then uploads the default settings to the central storage location.</span></span><span data-ttu-id="fb148-144">Otros equipos que ejecutan la aplicación, descargan la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="fb148-144"> Other computers running the app then download the default settings.</span></span><span data-ttu-id="fb148-145">Este comportamiento es idéntico al comportamiento de las aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="fb148-145"> This behavior is identical to the behavior of desktop applications.</span></span>

<span data-ttu-id="fb148-146">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="fb148-146">WORKAROUND: None.</span></span>

### <span data-ttu-id="fb148-147">UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="fb148-147">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="fb148-148">Le recomendamos que instale la versión de 32 bits de Microsoft Office para sistemas operativos de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fb148-148">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="fb148-149">Para elegir la versión de Microsoft Office que necesita, haga clic aquí.</span><span class="sxs-lookup"><span data-stu-id="fb148-149">To choose the Microsoft Office version that you need, click here.</span></span> <span data-ttu-id="fb148-150">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span><span class="sxs-lookup"><span data-stu-id="fb148-150">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="fb148-151">UE-V admite la configuración de itinerancia entre versiones de arquitectura idénticas de Office.</span><span class="sxs-lookup"><span data-stu-id="fb148-151">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="fb148-152">Por ejemplo, la configuración de Office de 32 bits se transferirá entre todas las instancias de Office de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fb148-152">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="fb148-153">UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="fb148-153">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="fb148-154">SOLUCIÓN alternativa: ninguna</span><span class="sxs-lookup"><span data-stu-id="fb148-154">WORKAROUND: None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="fb148-155">Los MSI no están localizados</span><span class="sxs-lookup"><span data-stu-id="fb148-155">MSI’s are not localized</span></span>

<span data-ttu-id="fb148-156">UE-V incluye un programa de instalación localizado para UE-V Agent y UE-V generator.</span><span class="sxs-lookup"><span data-stu-id="fb148-156">UE-V includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="fb148-157">Estos archivos MSI siguen estando disponibles, pero la interfaz de usuario está minimizada y la de MSI solo se muestra en inglés.</span><span class="sxs-lookup"><span data-stu-id="fb148-157">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="fb148-158">A pesar de que el archivo está en inglés, el programa de instalación instala todos los idiomas admitidos durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="fb148-158">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="fb148-159">SOLUCIÓN alternativa: ninguna</span><span class="sxs-lookup"><span data-stu-id="fb148-159">WORKAROUND: None</span></span>

### <span data-ttu-id="fb148-160">Los favicons asociados a los favoritos de Internet Explorer 9 no se mueven</span><span class="sxs-lookup"><span data-stu-id="fb148-160">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="fb148-161">Los favicons asociados a los favoritos de Internet Explorer 9 no se desplazan por la virtualización de la experiencia del usuario y no aparecen cuando los favoritos aparecen por primera vez en un equipo nuevo.</span><span class="sxs-lookup"><span data-stu-id="fb148-161">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="fb148-162">SOLUCIÓN: favicons aparecerá con sus favoritos asociados una vez que el marcador se use y se almacene en la memoria caché en el explorador Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fb148-162">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="fb148-163">Las rutas de configuración de archivos se almacenan en el registro</span><span class="sxs-lookup"><span data-stu-id="fb148-163">File settings paths are stored in registry</span></span>

<span data-ttu-id="fb148-164">Algunas opciones de la aplicación almacenan las rutas de los archivos de configuración y configuración como valores en el registro.</span><span class="sxs-lookup"><span data-stu-id="fb148-164">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="fb148-165">Los archivos a los que se hace referencia como rutas en el registro se deben sincronizar cuando se mueven los valores de configuración entre equipos.</span><span class="sxs-lookup"><span data-stu-id="fb148-165">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="fb148-166">SOLUCIÓN alternativa: Use el redireccionamiento de carpetas o cualquier otra tecnología para asegurarse de que todos los archivos a los que se hace referencia como rutas de configuración de archivos están presentes y colocados en la misma ubicación en todos los equipos en los que la configuración es móvil.</span><span class="sxs-lookup"><span data-stu-id="fb148-166">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="fb148-167">Las rutas de almacenamiento de configuración largas pueden provocar un error</span><span class="sxs-lookup"><span data-stu-id="fb148-167">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="fb148-168">Mantenga las rutas de almacenamiento de configuración tan cortas como sea posible.</span><span class="sxs-lookup"><span data-stu-id="fb148-168">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="fb148-169">Las rutas largas pueden impedir la resolución o la sincronización.</span><span class="sxs-lookup"><span data-stu-id="fb148-169">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="fb148-170">UE-V usa la ruta de acceso de almacenamiento de configuración como parte de la ruta de acceso calculada para almacenar la configuración.</span><span class="sxs-lookup"><span data-stu-id="fb148-170">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="fb148-171">Esa ruta se calcula de la siguiente manera: configuración ruta de almacenamiento + "settingspackages" + paquete DIR (ID. de plantilla) + nombre de paquete (plantilla ID) +. pkgx.</span><span class="sxs-lookup"><span data-stu-id="fb148-171">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID) + .pkgx.</span></span> <span data-ttu-id="fb148-172">Si esa ruta de acceso calculada supera los 260 caracteres, almacenamiento de paquetes fallará y generará el siguiente mensaje de error en el registro de eventos operativos de UE-V:</span><span class="sxs-lookup"><span data-stu-id="fb148-172">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="fb148-173">Para comprobar los eventos de registro operativos, abra el visor de eventos y vaya a registros de aplicaciones y servicios/Microsoft/virtualización de la experiencia de usuario/inicio de sesión/operativo.</span><span class="sxs-lookup"><span data-stu-id="fb148-173">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="fb148-174">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="fb148-174">WORKAROUND: None.</span></span>

### <span data-ttu-id="fb148-175">Algunas configuraciones del sistema operativo solo se mueven entre las versiones del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="fb148-175">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="fb148-176">La configuración del sistema operativo para narrador y los caracteres de moneda específicos de la configuración regional (es decir, la configuración regional y de idioma) solo se transferirán a las distintas versiones del sistema operativo de Windows.</span><span class="sxs-lookup"><span data-stu-id="fb148-176">Operating system settings for Narrator and currency characters specific to the locale (i.e. language and regional settings) will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="fb148-177">Por ejemplo, los caracteres de moneda no se mueven entre Windows 7 y Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fb148-177">For example, currency characters will not roam between Windows 7 and Windows 8.</span></span>

<span data-ttu-id="fb148-178">SOLUCIÓN alternativa: ninguna</span><span class="sxs-lookup"><span data-stu-id="fb148-178">WORKAROUND: None</span></span>

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a><span data-ttu-id="fb148-179">UE-V 1 Agent genera errores cuando se ejecutan las plantillas de UE-V 2</span><span class="sxs-lookup"><span data-stu-id="fb148-179">UE-V 1 agent generates errors when running UE-V 2 templates</span></span>

<span data-ttu-id="fb148-180">Si una plantilla de ubicación de configuración de UE-V 2 se distribuye a un equipo instalado con un agente de UE-V 1, algunos ajustes no se sincronizan entre los equipos y el agente informa de errores en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="fb148-180">If a UE-V 2 settings location template is distributed to a computer installed with a UE-V 1 agent, some settings fail to synchronize between computers and the agent reports errors in the event log.</span></span>

<span data-ttu-id="fb148-181">SOLUCIÓN: al migrar de UE-V 1 a UE-V 2 y es probable que tenga equipos en los que se ejecuta la versión anterior del agente, cree un catálogo UE-V 2. x independiente para admitir el agente y las plantillas de UE-V 2. x.</span><span class="sxs-lookup"><span data-stu-id="fb148-181">WORKAROUND: When migrating from UE-V 1 to UE-V 2 and it is likely you’ll have computers running the previous version of the agent, create a separate UE-V 2.x catalog to support the UE-V 2.x Agent and templates.</span></span>

### <span data-ttu-id="fb148-182">Tiempo de cierre de la UE-V</span><span class="sxs-lookup"><span data-stu-id="fb148-182">UE-V logoff delay</span></span>

<span data-ttu-id="fb148-183">Ocasionalmente, al cerrar sesión, UE-V tarda mucho tiempo en sincronizar la configuración.</span><span class="sxs-lookup"><span data-stu-id="fb148-183">Occasionally on logoff, UE-V takes a long time to sync settings.</span></span> <span data-ttu-id="fb148-184">Normalmente, esto se debe a una red de latencia alta o a un uso incorrecto del sistema de archivos de distrubuted (DFS).</span><span class="sxs-lookup"><span data-stu-id="fb148-184">Typically, this is due to a high latency network or incorrect use of Distrubuted File System (DFS).</span></span>
<span data-ttu-id="fb148-185">Para obtener compatibilidad con DFS, consulte [la declaración de soporte de Microsoft sobre los datos de Perfil de usuario replicados](https://support.microsoft.com/kb/2533009) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="fb148-185">For DFS support, see [Microsoft’s Support Statement Around Replicated User Profile Data](https://support.microsoft.com/kb/2533009) for further details.</span></span>

<span data-ttu-id="fb148-186">SOLUCIÓN alternativa: a partir de HF03, se introdujo una nueva clave del registro la siguiente clave del registro proporciona un mecanismo por el cual se puede especificar el retraso máximo de cierre de sesión \\Software\\Microsoft\\UEV\\Agent\\Configuration\\LogOffWaitInterval</span><span class="sxs-lookup"><span data-stu-id="fb148-186">WORKAROUND: Starting with HF03, a new registry key has been introduced The following registry key provides a mechanism by which the maximum logoff delay can be specified \\Software\\Microsoft\\UEV\\Agent\\Configuration\\LogOffWaitInterval</span></span>

<span data-ttu-id="fb148-187">Consulte [la configuración del registro de UE-V](https://support.microsoft.com/kb/2770042) para obtener más información</span><span class="sxs-lookup"><span data-stu-id="fb148-187">See [UE-V registry settings](https://support.microsoft.com/kb/2770042) for further details</span></span>

## <span data-ttu-id="fb148-188">Revisiones y artículos de Knowledge base para UE-V 2,1 SP1</span><span class="sxs-lookup"><span data-stu-id="fb148-188">Hotfixes and Knowledge Base articles for UE-V 2.1 SP1</span></span>


<span data-ttu-id="fb148-189">Esta sección contiene revisiones y artículos de KB para UE-V 2,1 SP1.</span><span class="sxs-lookup"><span data-stu-id="fb148-189">This section contains hotfixes and KB articles for UE-V 2.1 SP1.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="fb148-190">Artículo de KB</span><span class="sxs-lookup"><span data-stu-id="fb148-190">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="fb148-191">Title</span><span class="sxs-lookup"><span data-stu-id="fb148-191">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="fb148-192">Link</span><span class="sxs-lookup"><span data-stu-id="fb148-192">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb148-193">3018608</span><span class="sxs-lookup"><span data-stu-id="fb148-193">3018608</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb148-194">UE-V 2,1-TemplateConsole.exe se bloquea cuando faltan las clases WMI de UE-V</span><span class="sxs-lookup"><span data-stu-id="fb148-194">UE-V 2.1 - TemplateConsole.exe crashes when UE-V WMI classes are missing</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3018608/EN-US" data-raw-source="[support.microsoft.com/kb/3018608/EN-US](https://support.microsoft.com/kb/3018608/EN-US)"><span data-ttu-id="fb148-195">support.microsoft.com/kb/3018608/EN-US</span><span class="sxs-lookup"><span data-stu-id="fb148-195">support.microsoft.com/kb/3018608/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb148-196">2903501</span><span class="sxs-lookup"><span data-stu-id="fb148-196">2903501</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb148-197">UE-V: User Experience Virtualization (UE-V) compatibilidad con perfiles de usuario</span><span class="sxs-lookup"><span data-stu-id="fb148-197">UE-V: User Experience Virtualization (UE-V) compatibility with user profiles</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)"><span data-ttu-id="fb148-198">support.microsoft.com/kb/2903501/EN-US</span><span class="sxs-lookup"><span data-stu-id="fb148-198">support.microsoft.com/kb/2903501/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb148-199">2770042</span><span class="sxs-lookup"><span data-stu-id="fb148-199">2770042</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb148-200">Configuración del registro de UE-V</span><span class="sxs-lookup"><span data-stu-id="fb148-200">UE-V Registry Settings</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)"><span data-ttu-id="fb148-201">support.microsoft.com/kb/2770042/EN-US</span><span class="sxs-lookup"><span data-stu-id="fb148-201">support.microsoft.com/kb/2770042/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb148-202">2847017</span><span class="sxs-lookup"><span data-stu-id="fb148-202">2847017</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb148-203">Configuración de UE-V replicada por Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="fb148-203">UE-V settings replicated by Internet Explorer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)"><span data-ttu-id="fb148-204">support.microsoft.com/kb/2847017/EN-US</span><span class="sxs-lookup"><span data-stu-id="fb148-204">support.microsoft.com/kb/2847017/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb148-205">2769631</span><span class="sxs-lookup"><span data-stu-id="fb148-205">2769631</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb148-206">Cómo reparar una instalación de UE-V dañada</span><span class="sxs-lookup"><span data-stu-id="fb148-206">How to repair a corrupted UE-V install</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)"><span data-ttu-id="fb148-207">support.microsoft.com/kb/2769631/EN-US</span><span class="sxs-lookup"><span data-stu-id="fb148-207">support.microsoft.com/kb/2769631/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb148-208">2850989</span><span class="sxs-lookup"><span data-stu-id="fb148-208">2850989</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb148-209">No se admite la migración de perfiles MAPI con Microsoft UE-V</span><span class="sxs-lookup"><span data-stu-id="fb148-209">Migrating MAPI profiles with Microsoft UE-V is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)"><span data-ttu-id="fb148-210">support.microsoft.com/kb/2850989/EN-US</span><span class="sxs-lookup"><span data-stu-id="fb148-210">support.microsoft.com/kb/2850989/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb148-211">2769586</span><span class="sxs-lookup"><span data-stu-id="fb148-211">2769586</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb148-212">UE-V roaming las carpetas vacías y las claves de registro</span><span class="sxs-lookup"><span data-stu-id="fb148-212">UE-V roams empty folders and registry keys</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)"><span data-ttu-id="fb148-213">support.microsoft.com/kb/2769586/EN-US</span><span class="sxs-lookup"><span data-stu-id="fb148-213">support.microsoft.com/kb/2769586/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb148-214">2782997</span><span class="sxs-lookup"><span data-stu-id="fb148-214">2782997</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb148-215">Cómo habilitar el registro de depuración en la virtualización de la experiencia del usuario de Microsoft (UE-V)</span><span class="sxs-lookup"><span data-stu-id="fb148-215">How To Enable Debug Logging in Microsoft User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)"><span data-ttu-id="fb148-216">support.microsoft.com/kb/2782997/EN-US</span><span class="sxs-lookup"><span data-stu-id="fb148-216">support.microsoft.com/kb/2782997/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb148-217">2769570</span><span class="sxs-lookup"><span data-stu-id="fb148-217">2769570</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb148-218">UE-V no actualiza el tema en sesiones de RDS o VDI</span><span class="sxs-lookup"><span data-stu-id="fb148-218">UE-V does not update the theme on RDS or VDI sessions</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)"><span data-ttu-id="fb148-219">support.microsoft.com/kb/2769570/EN-US</span><span class="sxs-lookup"><span data-stu-id="fb148-219">support.microsoft.com/kb/2769570/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb148-220">2850582</span><span class="sxs-lookup"><span data-stu-id="fb148-220">2850582</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb148-221">Cómo usar la virtualización de la experiencia del usuario de Microsoft con aplicaciones de App-V</span><span class="sxs-lookup"><span data-stu-id="fb148-221">How To Use Microsoft User Experience Virtualization With App-V Applications</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)"><span data-ttu-id="fb148-222">support.microsoft.com/kb/2850582/EN-US</span><span class="sxs-lookup"><span data-stu-id="fb148-222">support.microsoft.com/kb/2850582/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="fb148-223">3041879</span><span class="sxs-lookup"><span data-stu-id="fb148-223">3041879</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb148-224">Versiones de archivo actuales para la virtualización de la experiencia del usuario de Microsoft</span><span class="sxs-lookup"><span data-stu-id="fb148-224">Current file versions for Microsoft User Experience Virtualization</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)"><span data-ttu-id="fb148-225">support.microsoft.com/kb/3041879/EN-US</span><span class="sxs-lookup"><span data-stu-id="fb148-225">support.microsoft.com/kb/3041879/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="fb148-226">2843592</span><span class="sxs-lookup"><span data-stu-id="fb148-226">2843592</span></span></p></td>
<td align="left"><p><span data-ttu-id="fb148-227">Información sobre la virtualización de la experiencia del usuario y alta disponibilidad</span><span class="sxs-lookup"><span data-stu-id="fb148-227">Information on User Experience Virtualization and High Availability</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)"><span data-ttu-id="fb148-228">support.microsoft.com/kb/2843592/EN-US</span><span class="sxs-lookup"><span data-stu-id="fb148-228">support.microsoft.com/kb/2843592/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 






 

 





