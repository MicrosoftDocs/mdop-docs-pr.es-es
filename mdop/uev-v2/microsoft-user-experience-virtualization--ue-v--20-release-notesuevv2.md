---
title: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.0
description: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.0
author: dansimp
ms.assetid: 5ef66cd1-ba2b-4383-9f45-e7cde41f1ba1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ad3deffa5cd567a70711e5447197e630f04ea254
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825281"
---
# <span data-ttu-id="1f305-103">Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.0</span><span class="sxs-lookup"><span data-stu-id="1f305-103">Microsoft User Experience Virtualization (UE-V) 2.0 Release Notes</span></span>


<span data-ttu-id="1f305-104">Para buscar las notas de la versión de virtualización de Microsoft User Experience (UE-V) 2,0, presione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="1f305-104">To search Microsoft User Experience Virtualization (UE-V) 2.0 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="1f305-105">Debe leer estas notas de la versión minuciosamente antes de instalar UE-V.</span><span class="sxs-lookup"><span data-stu-id="1f305-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="1f305-106">Las notas de la versión contienen información necesaria para instalar correctamente la virtualización de la experiencia del usuario y contienen información adicional que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="1f305-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="1f305-107">Si hay diferencias entre estas notas de la versión y otra documentación de UE-V, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="1f305-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="1f305-108">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="1f305-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="1f305-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1f305-109">Providing feedback</span></span>


<span data-ttu-id="1f305-110">Díganos lo que piensa sobre nuestra documentación de MDOP enviándonos sus comentarios y comentarios.</span><span class="sxs-lookup"><span data-stu-id="1f305-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="1f305-111">Envíe sus comentarios sobre la documentación a [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="1f305-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="1f305-112">Problemas conocidos de UE-V</span><span class="sxs-lookup"><span data-stu-id="1f305-112">UE-V known issues</span></span>


<span data-ttu-id="1f305-113">Esta sección contiene notas de la versión para la virtualización de la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="1f305-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="1f305-114">La configuración del registro no se sincroniza entre App-V y aplicaciones nativas en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="1f305-114">Registry settings do not synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="1f305-115">Cuando un equipo tiene una aplicación que se instala a través de virtualización de aplicaciones (App-V) y de forma local con un archivo de Windows Installer (. msi), la configuración basada en el registro no se sincroniza entre las tecnologías.</span><span class="sxs-lookup"><span data-stu-id="1f305-115">When a computer has an application that is installed through both Application Virtualization (App-V) and a locally with a Windows Installer (.msi) file, the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="1f305-116">**Solución alternativa:** Para resolver este problema, ejecute la aplicación seleccionando una de las dos tecnologías, pero no ambas.</span><span class="sxs-lookup"><span data-stu-id="1f305-116">**WORKAROUND:** To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="settings-do-not-synchronization-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="1f305-117">La configuración no se sincroniza cuando el recurso compartido de red está fuera del dominio del usuario</span><span class="sxs-lookup"><span data-stu-id="1f305-117">Settings do not synchronization when network share is outside user’s domain</span></span>

<span data-ttu-id="1f305-118">Cuando Windows® 8 intenta la sincronización de configuración del sistema operativo, se produce un error en la sincronización con el siguiente mensaje de error: **Boost:: filesystem:: EXISTS:: nombre de usuario o contraseña incorrectos**.</span><span class="sxs-lookup"><span data-stu-id="1f305-118">When Windows® 8 attempts operating system settings synchronization, the synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="1f305-119">Este error puede indicar que el recurso compartido de red está fuera del dominio del usuario o un dominio con una relación de confianza a ese dominio.</span><span class="sxs-lookup"><span data-stu-id="1f305-119">This error can indicate that the network share is outside the user’s domain or a domain with a trust relationship to that domain.</span></span> <span data-ttu-id="1f305-120">Para buscar eventos de registro operativos, abra el **visor de eventos** y vaya a **registros de aplicaciones y servicios**  /  **Microsoft**  /  **User Experience virtualización**  /  **Logging**  /  **operativo**.</span><span class="sxs-lookup"><span data-stu-id="1f305-120">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="1f305-121">Los recursos compartidos de red que se usan para la configuración de UE-V las ubicaciones de almacenamiento deben residir en el mismo dominio de Active Directory que el usuario o un dominio de confianza del dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="1f305-121">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user or a trusted domain of the user’s domain.</span></span>

<span data-ttu-id="1f305-122">**Solución alternativa:** Use recursos compartidos de red del mismo dominio de Active Directory que el usuario.</span><span class="sxs-lookup"><span data-stu-id="1f305-122">**WORKAROUND:** Use network shares from the same Active Directory domain as the user.</span></span>

### <span data-ttu-id="1f305-123">Resultados imprevisibles con Office 2010 y Office 2013 instalados</span><span class="sxs-lookup"><span data-stu-id="1f305-123">Unpredictable results with both Office 2010 and Office 2013 installed</span></span>

<span data-ttu-id="1f305-124">Cuando un usuario tiene instalado Office 2010 y Office 2013, cualquier configuración común entre las dos versiones de Office se desplazará con UE-V.</span><span class="sxs-lookup"><span data-stu-id="1f305-124">When a user has both Office 2010 and Office 2013 installed, any common settings between the two versions of Office are roamed by UE-V.</span></span> <span data-ttu-id="1f305-125">Esto puede provocar que el tamaño del paquete de Office 2010 sea muy grande o que se produzcan conflictos imprevisibles con 2013, especialmente si se usa Office 365.</span><span class="sxs-lookup"><span data-stu-id="1f305-125">This could cause the Office 2010 package size to be quite large or result in unpredictable conflicts with 2013, particularly if Office 365 is used.</span></span>

<span data-ttu-id="1f305-126">**Solución alternativa:** Instale solo una versión de Office o limite las opciones de configuración que se van a sincronizar mediante UE-V.</span><span class="sxs-lookup"><span data-stu-id="1f305-126">**WORKAROUND:** Install only one version of Office or limit which settings are synchronized by UE-V.</span></span>

### <span data-ttu-id="1f305-127">Desinstalar y volver a instalar la aplicación Windows 8 revierte la configuración al estado inicial</span><span class="sxs-lookup"><span data-stu-id="1f305-127">Uninstall and re-install of Windows 8 app reverts settings to initial state</span></span>

<span data-ttu-id="1f305-128">Al usar la sincronización de configuración de UE-V para una aplicación de Windows 8, si el usuario desinstala la aplicación y, a continuación, vuelve a instalar la aplicación, la configuración de la aplicación vuelve a sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="1f305-128">While using UE-V settings synchronization for a Windows 8 app, if the user uninstalls the app and then reinstalls the app, the app’s settings revert to their default values.</span></span><span data-ttu-id="1f305-129">Esto sucede porque la desinstalación quita la copia local (en caché) de la configuración de la aplicación, pero no quita el paquete de configuración local de UE-V.</span><span class="sxs-lookup"><span data-stu-id="1f305-129"> This happens because the uninstall removes the local (cached) copy of the app’s settings but does not remove the local UE-V settings package.</span></span><span data-ttu-id="1f305-130">Cuando la aplicación se reinstale e inicie, UE-V reúna la configuración de la aplicación que se restableció a los valores predeterminados de la aplicación y, a continuación, cargará la configuración predeterminada en la ubicación de almacenamiento central.</span><span class="sxs-lookup"><span data-stu-id="1f305-130"> When the app is reinstalled and launched, UE-V gather the app settings that were reset to the app defaults and then uploads the default settings to the central storage location.</span></span><span data-ttu-id="1f305-131">Otros equipos que ejecutan la aplicación, descargan la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1f305-131"> Other computers running the app then download the default settings.</span></span><span data-ttu-id="1f305-132">Este comportamiento es idéntico al comportamiento de las aplicaciones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="1f305-132"> This behavior is identical to the behavior of desktop applications.</span></span>

<span data-ttu-id="1f305-133">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="1f305-133">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="1f305-134">Itinerancia de la firma de correo electrónico para Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="1f305-134">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="1f305-135">UE-V moverá los archivos de firma de Outlook 2010 entre dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1f305-135">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="1f305-136">Sin embargo, las opciones de firma predeterminadas para los mensajes nuevos y las respuestas o reenvíos no se sincronizan.</span><span class="sxs-lookup"><span data-stu-id="1f305-136">However, the default signature options for new messages and replies or forwards are not synchronized.</span></span> <span data-ttu-id="1f305-137">Estas dos opciones de configuración se almacenan en el perfil de Outlook, que UE-V no se mueve.</span><span class="sxs-lookup"><span data-stu-id="1f305-137">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="1f305-138">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="1f305-138">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="1f305-139">UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="1f305-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="1f305-140">Le recomendamos que instale la versión de 64 bits de Microsoft Office para equipos modernos.</span><span class="sxs-lookup"><span data-stu-id="1f305-140">We recommend that you install the 64-bit version of Microsoft Office for modern computers.</span></span> <span data-ttu-id="1f305-141">Para determinar qué versión necesita, [haga clic aquí](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions).</span><span class="sxs-lookup"><span data-stu-id="1f305-141">To determine which version you need, [click here](https://support.office.com/article/choose-between-the-64-bit-or-32-bit-version-of-office-2dee7807-8f95-4d0c-b5fe-6c6f49b8d261?ui=en-US&rs=en-US&ad=US#32or64Bit=Newer_Versions).</span></span> <span data-ttu-id="1f305-142">UE-V admite la configuración de itinerancia entre versiones de arquitectura idénticas de Office.</span><span class="sxs-lookup"><span data-stu-id="1f305-142">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="1f305-143">Por ejemplo, la configuración de Office de 32 bits se transferirá entre todas las instancias de Office de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1f305-143">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="1f305-144">UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="1f305-144">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="1f305-145">**Solución alternativa:** Nada</span><span class="sxs-lookup"><span data-stu-id="1f305-145">**WORKAROUND:** None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="1f305-146">Los MSI no están localizados</span><span class="sxs-lookup"><span data-stu-id="1f305-146">MSI’s are not localized</span></span>

<span data-ttu-id="1f305-147">UE-V 2,0 incluye un programa de instalación localizado para UE-V Agent y UE-v generator.</span><span class="sxs-lookup"><span data-stu-id="1f305-147">UE-V 2.0 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="1f305-148">Estos archivos MSI siguen estando disponibles, pero la interfaz de usuario está minimizada y la de MSI solo se muestra en inglés.</span><span class="sxs-lookup"><span data-stu-id="1f305-148">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="1f305-149">A pesar de que el archivo está en inglés, el programa de instalación instala todos los idiomas admitidos durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="1f305-149">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="1f305-150">**Solución alternativa:** Nada</span><span class="sxs-lookup"><span data-stu-id="1f305-150">**WORKAROUND:** None</span></span>

### <span data-ttu-id="1f305-151">Los favicons asociados a los favoritos de Internet Explorer 9 no se mueven</span><span class="sxs-lookup"><span data-stu-id="1f305-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="1f305-152">Los favicons asociados a los favoritos de Internet Explorer 9 no se desplazan por la virtualización de la experiencia del usuario y no aparecen cuando los favoritos aparecen por primera vez en un equipo nuevo.</span><span class="sxs-lookup"><span data-stu-id="1f305-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="1f305-153">**Solución alternativa:** Favicons aparecerá con sus favoritos asociados una vez que el marcador se use y se almacene en la memoria caché en el explorador Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1f305-153">**WORKAROUND:** Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="1f305-154">Las rutas de configuración de archivos se almacenan en el registro</span><span class="sxs-lookup"><span data-stu-id="1f305-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="1f305-155">Algunas opciones de la aplicación almacenan las rutas de los archivos de configuración y configuración como valores en el registro.</span><span class="sxs-lookup"><span data-stu-id="1f305-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="1f305-156">Los archivos a los que se hace referencia como rutas en el registro se deben sincronizar cuando se mueven los valores de configuración entre equipos.</span><span class="sxs-lookup"><span data-stu-id="1f305-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="1f305-157">**Solución alternativa:** Use el redireccionamiento de carpetas o cualquier otra tecnología para asegurarse de que todos los archivos a los que se hace referencia como rutas de configuración de archivos están presentes y colocados en la misma ubicación en todos los equipos en los que la configuración es móvil.</span><span class="sxs-lookup"><span data-stu-id="1f305-157">**WORKAROUND:** Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="1f305-158">Las rutas de almacenamiento de configuración largas pueden provocar un error</span><span class="sxs-lookup"><span data-stu-id="1f305-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="1f305-159">Mantenga las rutas de almacenamiento de configuración tan cortas como sea posible.</span><span class="sxs-lookup"><span data-stu-id="1f305-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="1f305-160">Las rutas largas pueden impedir la resolución o la sincronización.</span><span class="sxs-lookup"><span data-stu-id="1f305-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="1f305-161">UE-V usa la ruta de acceso de almacenamiento de configuración como parte de la ruta de acceso calculada para almacenar la configuración.</span><span class="sxs-lookup"><span data-stu-id="1f305-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="1f305-162">Esa ruta se calcula de la siguiente manera: configuración ruta de almacenamiento + "settingspackages" + paquete DIR (ID. de plantilla) + nombre de paquete (plantilla ID) +. pkgx.</span><span class="sxs-lookup"><span data-stu-id="1f305-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID) + .pkgx.</span></span> <span data-ttu-id="1f305-163">Si esa ruta de acceso calculada supera los 260 caracteres, almacenamiento de paquetes fallará y generará el siguiente mensaje de error en el registro de eventos operativos de UE-V:</span><span class="sxs-lookup"><span data-stu-id="1f305-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="1f305-164">Para comprobar los eventos de registro operativos, abra el visor de eventos y vaya a registros de aplicaciones y servicios/Microsoft/virtualización de la experiencia de usuario/inicio de sesión/operativo.</span><span class="sxs-lookup"><span data-stu-id="1f305-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="1f305-165">**Solución alternativa:** Nada.</span><span class="sxs-lookup"><span data-stu-id="1f305-165">**WORKAROUND:** None.</span></span>

### <span data-ttu-id="1f305-166">Algunas configuraciones del sistema operativo solo se mueven entre las versiones del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="1f305-166">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="1f305-167">La configuración del sistema operativo para narrador y los caracteres de moneda específicos de la configuración regional (es decir, la configuración regional y de idioma) solo se transferirán a las distintas versiones del sistema operativo de Windows.</span><span class="sxs-lookup"><span data-stu-id="1f305-167">Operating system settings for Narrator and currency characters specific to the locale (i.e. language and regional settings) will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="1f305-168">Por ejemplo, los caracteres de moneda no se mueven entre Windows 7 y Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1f305-168">For example, currency characters will not roam between Windows 7 and Windows 8.</span></span>

<span data-ttu-id="1f305-169">**Solución alternativa:** Nada</span><span class="sxs-lookup"><span data-stu-id="1f305-169">**WORKAROUND:** None</span></span>

### <span data-ttu-id="1f305-170">Las aplicaciones de Windows 8 no sincronizan la configuración cuando la aplicación se reinicia después de cerrarse de forma inesperada</span><span class="sxs-lookup"><span data-stu-id="1f305-170">Windows 8 apps do not sync settings when the app restarts after closing unexpectedly</span></span>

<span data-ttu-id="1f305-171">Si una aplicación de Windows 8 se cierra inesperadamente muy pronto después del inicio, es posible que la configuración de la aplicación no se sincronice cuando se reinicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1f305-171">If a Windows 8 app closes unexpectedly soon after startup, settings for the application may not be synchronized when the application is restarted.</span></span>

<span data-ttu-id="1f305-172">**Solución alternativa:** Cierre la aplicación Windows 8, cierre y reinicie la aplicación UevAppMonitor.exe (puede usar TaskManager) y, a continuación, reinicie la aplicación Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1f305-172">**WORKAROUND:** Close the Windows 8 app, close and restart the UevAppMonitor.exe application (can use TaskManager), and then restart the Windows 8 app.</span></span>

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a><span data-ttu-id="1f305-173">UE-V 1 Agent genera errores cuando se ejecutan las plantillas de UE-V 2</span><span class="sxs-lookup"><span data-stu-id="1f305-173">UE-V 1 agent generates errors when running UE-V 2 templates</span></span>

<span data-ttu-id="1f305-174">Si una plantilla de ubicación de configuración de UE-V 2 se distribuye a un equipo instalado con un agente de UE-V 1, algunos ajustes no se sincronizan entre los equipos y el agente informa de errores en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="1f305-174">If a UE-V 2 settings location template is distributed to a computer installed with a UE-V 1 agent, some settings fail to synchronize between computers and the agent reports errors in the event log.</span></span>

<span data-ttu-id="1f305-175">**Solución alternativa:** Al migrar de UE-V 1 a UE-V 2 y es posible que tenga equipos con la versión anterior del agente, cree un catálogo independiente de UE-V 2,0 para admitir el agente y las plantillas de UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="1f305-175">**WORKAROUND:** When migrating from UE-V 1 to UE-V 2 and it is likely you’ll have computers running the previous version of the agent, create a separate UE-V 2.0 catalog to support the UE-V 2.0 Agent and templates.</span></span>

## <span data-ttu-id="1f305-176">Revisiones y artículos de Knowledge base para UE-V 2,0</span><span class="sxs-lookup"><span data-stu-id="1f305-176">Hotfixes and Knowledge Base articles for UE-V 2.0</span></span>


<span data-ttu-id="1f305-177">Esta sección contiene revisiones y artículos de KB para UE-V 2,0.</span><span class="sxs-lookup"><span data-stu-id="1f305-177">This section contains hotfixes and KB articles for UE-V 2.0.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="1f305-178">Artículo de KB</span><span class="sxs-lookup"><span data-stu-id="1f305-178">KB Article</span></span></strong></th>
<th align="left"><span data-ttu-id="1f305-179">Title</span><span class="sxs-lookup"><span data-stu-id="1f305-179">Title</span></span></th>
<th align="left"><strong><span data-ttu-id="1f305-180">Link</span><span class="sxs-lookup"><span data-stu-id="1f305-180">Link</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f305-181">2927019</span><span class="sxs-lookup"><span data-stu-id="1f305-181">2927019</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-182">Hotfix 1 para la virtualización de la experiencia del usuario de Microsoft 2,0</span><span class="sxs-lookup"><span data-stu-id="1f305-182">Hotfix Package 1 for Microsoft User Experience Virtualization 2.0</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2927019" data-raw-source="[support.microsoft.com/kb/2927019](https://support.microsoft.com/kb/2927019)"><span data-ttu-id="1f305-183">support.microsoft.com/kb/2927019</span><span class="sxs-lookup"><span data-stu-id="1f305-183">support.microsoft.com/kb/2927019</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1f305-184">2903501</span><span class="sxs-lookup"><span data-stu-id="1f305-184">2903501</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-185">UE-V: User Experience Virtualization (UE-V) compatibilidad con perfiles de usuario</span><span class="sxs-lookup"><span data-stu-id="1f305-185">UE-V: User Experience Virtualization (UE-V) compatibility with user profiles</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)"><span data-ttu-id="1f305-186">support.microsoft.com/kb/2903501/EN-US</span><span class="sxs-lookup"><span data-stu-id="1f305-186">support.microsoft.com/kb/2903501/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f305-187">2770042</span><span class="sxs-lookup"><span data-stu-id="1f305-187">2770042</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-188">Configuración del registro de UE-V</span><span class="sxs-lookup"><span data-stu-id="1f305-188">UE-V Registry Settings</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)"><span data-ttu-id="1f305-189">support.microsoft.com/kb/2770042/EN-US</span><span class="sxs-lookup"><span data-stu-id="1f305-189">support.microsoft.com/kb/2770042/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1f305-190">2847017</span><span class="sxs-lookup"><span data-stu-id="1f305-190">2847017</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-191">Configuración de UE-V replicada por Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="1f305-191">UE-V settings replicated by Internet Explorer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)"><span data-ttu-id="1f305-192">support.microsoft.com/kb/2847017/EN-US</span><span class="sxs-lookup"><span data-stu-id="1f305-192">support.microsoft.com/kb/2847017/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f305-193">2930271</span><span class="sxs-lookup"><span data-stu-id="1f305-193">2930271</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-194">Descripción de las limitaciones de las firmas de itinerancia de Outlook en Microsoft UE-V</span><span class="sxs-lookup"><span data-stu-id="1f305-194">Understanding the limitations of roaming Outlook signatures in Microsoft UE-V</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2930271/EN-US" data-raw-source="[support.microsoft.com/kb/2930271/EN-US](https://support.microsoft.com/kb/2930271/EN-US)"><span data-ttu-id="1f305-195">support.microsoft.com/kb/2930271/EN-US</span><span class="sxs-lookup"><span data-stu-id="1f305-195">support.microsoft.com/kb/2930271/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1f305-196">2769631</span><span class="sxs-lookup"><span data-stu-id="1f305-196">2769631</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-197">Cómo reparar una instalación de UE-V dañada</span><span class="sxs-lookup"><span data-stu-id="1f305-197">How to repair a corrupted UE-V install</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)"><span data-ttu-id="1f305-198">support.microsoft.com/kb/2769631/EN-US</span><span class="sxs-lookup"><span data-stu-id="1f305-198">support.microsoft.com/kb/2769631/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f305-199">2850989</span><span class="sxs-lookup"><span data-stu-id="1f305-199">2850989</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-200">No se admite la migración de perfiles MAPI con Microsoft UE-V</span><span class="sxs-lookup"><span data-stu-id="1f305-200">Migrating MAPI profiles with Microsoft UE-V is not supported</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)"><span data-ttu-id="1f305-201">support.microsoft.com/kb/2850989/EN-US</span><span class="sxs-lookup"><span data-stu-id="1f305-201">support.microsoft.com/kb/2850989/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1f305-202">2769586</span><span class="sxs-lookup"><span data-stu-id="1f305-202">2769586</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-203">UE-V roaming las carpetas vacías y las claves de registro</span><span class="sxs-lookup"><span data-stu-id="1f305-203">UE-V roams empty folders and registry keys</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)"><span data-ttu-id="1f305-204">support.microsoft.com/kb/2769586/EN-US</span><span class="sxs-lookup"><span data-stu-id="1f305-204">support.microsoft.com/kb/2769586/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f305-205">2782997</span><span class="sxs-lookup"><span data-stu-id="1f305-205">2782997</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-206">Cómo habilitar el registro de depuración en la virtualización de la experiencia del usuario de Microsoft (UE-V)</span><span class="sxs-lookup"><span data-stu-id="1f305-206">How To Enable Debug Logging in Microsoft User Experience Virtualization (UE-V)</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)"><span data-ttu-id="1f305-207">support.microsoft.com/kb/2782997/EN-US</span><span class="sxs-lookup"><span data-stu-id="1f305-207">support.microsoft.com/kb/2782997/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1f305-208">2769570</span><span class="sxs-lookup"><span data-stu-id="1f305-208">2769570</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-209">UE-V no actualiza el tema en sesiones de RDS o VDI</span><span class="sxs-lookup"><span data-stu-id="1f305-209">UE-V does not update the theme on RDS or VDI sessions</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)"><span data-ttu-id="1f305-210">support.microsoft.com/kb/2769570/EN-US</span><span class="sxs-lookup"><span data-stu-id="1f305-210">support.microsoft.com/kb/2769570/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f305-211">2901856</span><span class="sxs-lookup"><span data-stu-id="1f305-211">2901856</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-212">La configuración de la aplicación no se sincroniza después de forzar un reinicio en un equipo habilitado para UE-V</span><span class="sxs-lookup"><span data-stu-id="1f305-212">Application settings do not sync after you force a restart on a UE-V-enabled computer</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2901856/EN-US" data-raw-source="[support.microsoft.com/kb/2901856/EN-US](https://support.microsoft.com/kb/2901856/EN-US)"><span data-ttu-id="1f305-213">support.microsoft.com/kb/2901856/EN-US</span><span class="sxs-lookup"><span data-stu-id="1f305-213">support.microsoft.com/kb/2901856/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1f305-214">2850582</span><span class="sxs-lookup"><span data-stu-id="1f305-214">2850582</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-215">Cómo usar la virtualización de la experiencia del usuario de Microsoft con aplicaciones de App-V</span><span class="sxs-lookup"><span data-stu-id="1f305-215">How To Use Microsoft User Experience Virtualization With App-V Applications</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)"><span data-ttu-id="1f305-216">support.microsoft.com/kb/2850582/EN-US</span><span class="sxs-lookup"><span data-stu-id="1f305-216">support.microsoft.com/kb/2850582/EN-US</span></span></a></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1f305-217">3041879</span><span class="sxs-lookup"><span data-stu-id="1f305-217">3041879</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-218">Versiones de archivo actuales para la virtualización de la experiencia del usuario de Microsoft</span><span class="sxs-lookup"><span data-stu-id="1f305-218">Current file versions for Microsoft User Experience Virtualization</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)"><span data-ttu-id="1f305-219">support.microsoft.com/kb/3041879/EN-US</span><span class="sxs-lookup"><span data-stu-id="1f305-219">support.microsoft.com/kb/3041879/EN-US</span></span></a></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1f305-220">2843592</span><span class="sxs-lookup"><span data-stu-id="1f305-220">2843592</span></span></p></td>
<td align="left"><p><span data-ttu-id="1f305-221">Información sobre la virtualización de la experiencia del usuario y alta disponibilidad</span><span class="sxs-lookup"><span data-stu-id="1f305-221">Information on User Experience Virtualization and High Availability</span></span></p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)"><span data-ttu-id="1f305-222">support.microsoft.com/kb/2843592/EN-US</span><span class="sxs-lookup"><span data-stu-id="1f305-222">support.microsoft.com/kb/2843592/EN-US</span></span></a></p></td>
</tr>
</tbody>
</table>

 

 

 





