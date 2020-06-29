---
title: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0 SP1
description: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0 SP1
author: dansimp
ms.assetid: 447fae0c-fe87-4d1c-b616-6f92fbdaf6d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8584999d9fdbdfccc3e9b2b1486cb97635475747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812486"
---
# <span data-ttu-id="adfa9-103">Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0 SP1</span><span class="sxs-lookup"><span data-stu-id="adfa9-103">Microsoft User Experience Virtualization (UE-V) 1.0 SP1 Release Notes</span></span>


<span data-ttu-id="adfa9-104">Para buscar las notas de versión de Microsoft User Experience Virtualization (UE-V) 1,0 Service Pack 1, presione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="adfa9-104">To search Microsoft User Experience Virtualization (UE-V) 1.0 Service Pack 1 release notes, press Ctrl+F.</span></span>

<span data-ttu-id="adfa9-105">Debe leer estas notas de la versión minuciosamente antes de instalar UE-V.</span><span class="sxs-lookup"><span data-stu-id="adfa9-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="adfa9-106">Las notas de la versión contienen información necesaria para instalar correctamente la virtualización de la experiencia del usuario y contienen información adicional que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="adfa9-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="adfa9-107">Si hay diferencias entre estas notas de la versión y otra documentación de UE-V, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="adfa9-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="adfa9-108">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="adfa9-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="adfa9-109">Problemas conocidos de UE-V</span><span class="sxs-lookup"><span data-stu-id="adfa9-109">UE-V known issues</span></span>


<span data-ttu-id="adfa9-110">Esta sección contiene notas de la versión para la experiencia del usuario de virtualización de 1,0 SP1.</span><span class="sxs-lookup"><span data-stu-id="adfa9-110">This section contains release notes for User Experience Virtualization 1.0 SP1.</span></span>

### <span data-ttu-id="adfa9-111">La configuración del registro no se sincroniza entre App-V y aplicaciones nativas en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="adfa9-111">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="adfa9-112">Cuando un equipo tiene una aplicación que está disponible a través de la aplicación Application Virtualization (App-V) y de una aplicación de instalación nativa instalada con un Windows Installer (archivo. msi), la configuración basada en el registro no se sincroniza entre las tecnologías.</span><span class="sxs-lookup"><span data-stu-id="adfa9-112">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application installed with a Windows Installer (.msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="adfa9-113">SOLUCIÓN alternativa: para resolver este problema, ejecute la aplicación seleccionando una de las dos tecnologías, pero no ambas.</span><span class="sxs-lookup"><span data-stu-id="adfa9-113">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <a href="" id="windows-8-setting-synchronization-fails-when-network-share-is-outside-user-s-domain"></a><span data-ttu-id="adfa9-114">Se produce un error en la sincronización de configuración de Windows 8 cuando el recurso compartido de red está fuera del dominio del usuario</span><span class="sxs-lookup"><span data-stu-id="adfa9-114">Windows 8 setting synchronization fails when network share is outside user’s domain</span></span>

<span data-ttu-id="adfa9-115">Cuando Windows® 8 intenta la sincronización de configuración del sistema operativo, se produce un error en synchrnization con el siguiente mensaje de error: **Boost:: filesystem:: EXISTS:: nombre de usuario o contraseña incorrectos**.</span><span class="sxs-lookup"><span data-stu-id="adfa9-115">When Windows® 8 attempts operating system settings synchronization, the synchrnization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="adfa9-116">Este error puede indicar que el recurso compartido de red está fuera del dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="adfa9-116">This error can indicate that the network share is outside the user’s domain.</span></span> <span data-ttu-id="adfa9-117">Para buscar eventos de registro operativos, abra el **visor de eventos** y vaya a **registros de aplicaciones y servicios**  /  **Microsoft**  /  **User Experience virtualización**  /  **Logging**  /  **operativo**.</span><span class="sxs-lookup"><span data-stu-id="adfa9-117">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="adfa9-118">Los recursos compartidos de red que se usan para la configuración de UE-V las ubicaciones de almacenamiento deben residir en el mismo dominio de Active Directory que el usuario.</span><span class="sxs-lookup"><span data-stu-id="adfa9-118">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span>

<span data-ttu-id="adfa9-119">SOLUCIÓN: Use recursos compartidos de red del mismo dominio de Active Directory que el usuario.</span><span class="sxs-lookup"><span data-stu-id="adfa9-119">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="adfa9-120">.</span><span class="sxs-lookup"><span data-stu-id="adfa9-120">.</span></span>

### <span data-ttu-id="adfa9-121">Itinerancia de la firma de correo electrónico para Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="adfa9-121">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="adfa9-122">UE-V moverá los archivos de firma de Outlook 2010 entre dispositivos.</span><span class="sxs-lookup"><span data-stu-id="adfa9-122">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="adfa9-123">Sin embargo, las opciones de firma predeterminadas para los mensajes nuevos y las respuestas y reenvíos no se mueven.</span><span class="sxs-lookup"><span data-stu-id="adfa9-123">However, the default signature options for new messages and replies/forwards are not roamed.</span></span> <span data-ttu-id="adfa9-124">Estas dos opciones de configuración se almacenan en el perfil de Outlook, que UE-V no se mueve.</span><span class="sxs-lookup"><span data-stu-id="adfa9-124">These two settings are stored in the Outlook profile, which UE-V does not roam.</span></span>

<span data-ttu-id="adfa9-125">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="adfa9-125">WORKAROUND: None.</span></span>

### <span data-ttu-id="adfa9-126">La configuración de sincronización no se sincroniza en el intervalo esperado cuando se ejecuta en modo de vínculo de baja velocidad</span><span class="sxs-lookup"><span data-stu-id="adfa9-126">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="adfa9-127">En condiciones normales, configuración las ubicaciones de almacenamiento deberían estar disponibles a través de una conexión de red de vínculo rápido.</span><span class="sxs-lookup"><span data-stu-id="adfa9-127">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="adfa9-128">En el modo de vínculo de baja velocidad, la sincronización solo se realizará de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="adfa9-128">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="adfa9-129">De forma predeterminada, la programación de sincronización del modo de vínculos lentos se establece en cada 360 minutos.</span><span class="sxs-lookup"><span data-stu-id="adfa9-129">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="adfa9-130">SOLUCIÓN: para cambiar la frecuencia de la sincronización en segundo plano para equipos en modo de vínculo de baja velocidad, puede configurar la Directiva de grupo para la Directiva de sincronización en segundo plano para **archivos sin conexión**.</span><span class="sxs-lookup"><span data-stu-id="adfa9-130">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="adfa9-131">Los caracteres especiales no se sincronizan</span><span class="sxs-lookup"><span data-stu-id="adfa9-131">Special characters do not synchronize</span></span>

<span data-ttu-id="adfa9-132">Ciertos caracteres, como los símbolos de moneda, no se sincronizan entre equipos con Windows 7 y Windows 8 que ejecutan el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="adfa9-132">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="adfa9-133">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="adfa9-133">WORKAROUND: None.</span></span>

### <span data-ttu-id="adfa9-134">UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="adfa9-134">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="adfa9-135">Le recomendamos que instale la versión de 32 bits de Microsoft Office para sistemas operativos de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="adfa9-135">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="adfa9-136">Para elegir la versión de Microsoft Office que necesita, haga clic aquí ( [http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623) ).</span><span class="sxs-lookup"><span data-stu-id="adfa9-136">To choose the Microsoft Office version that you need, click here ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="adfa9-137">UE-V admite la configuración de itinerancia entre versiones de arquitectura idénticas de Office.</span><span class="sxs-lookup"><span data-stu-id="adfa9-137">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="adfa9-138">Por ejemplo, la configuración de Office de 32 bits se transferirá entre todas las instancias de Office de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="adfa9-138">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="adfa9-139">UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="adfa9-139">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="adfa9-140">SOLUCIÓN alternativa: ninguna</span><span class="sxs-lookup"><span data-stu-id="adfa9-140">WORKAROUND: None</span></span>

### <a href="" id="msi-s-are-not-localized"></a><span data-ttu-id="adfa9-141">Los MSI no están localizados</span><span class="sxs-lookup"><span data-stu-id="adfa9-141">MSI’s are not localized</span></span>

<span data-ttu-id="adfa9-142">UE-V 1,0 SP1 incluye un programa de instalación localizado para UE-V Agent y UE-v generator.</span><span class="sxs-lookup"><span data-stu-id="adfa9-142">UE-V 1.0 SP1 includes a localized setup program for both the UE-V Agent and UE-V generator.</span></span> <span data-ttu-id="adfa9-143">Estos archivos MSI siguen estando disponibles, pero la interfaz de usuario está minimizada y la de MSI solo se muestra en inglés.</span><span class="sxs-lookup"><span data-stu-id="adfa9-143">These MSI files are still available but the user interface is minimized and the MSI’s only display in English.</span></span> <span data-ttu-id="adfa9-144">A pesar de que el archivo está en inglés, el programa de instalación instala todos los idiomas admitidos durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="adfa9-144">Despite the file being in English, the setup program installs all supported languages during the installation.</span></span>

<span data-ttu-id="adfa9-145">SOLUCIÓN alternativa: ninguna</span><span class="sxs-lookup"><span data-stu-id="adfa9-145">WORKAROUND: None</span></span>

### <span data-ttu-id="adfa9-146">Otras carpetas del recurso compartido con la ubicación de almacenamiento de configuración no están disponibles en modo de conexión lenta</span><span class="sxs-lookup"><span data-stu-id="adfa9-146">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="adfa9-147">La configuración de almacenar recursos compartidos no se encuentra en un recurso compartido de red que se usa para otras carpetas que siempre deben estar disponibles.</span><span class="sxs-lookup"><span data-stu-id="adfa9-147">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="adfa9-148">Cuando el recurso compartido de red que hospeda la ubicación de almacenamiento de configuración pasa al modo de conexión lenta, la única carpeta disponible es la de ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="adfa9-148">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="adfa9-149">Otras carpetas del recurso compartido no están disponibles en modo de conexión lenta.</span><span class="sxs-lookup"><span data-stu-id="adfa9-149">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="adfa9-150">Solución alternativa: ninguna</span><span class="sxs-lookup"><span data-stu-id="adfa9-150">Workaround: None</span></span>

### <span data-ttu-id="adfa9-151">Los favicons asociados a los favoritos de Internet Explorer 9 no se mueven</span><span class="sxs-lookup"><span data-stu-id="adfa9-151">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="adfa9-152">Los favicons asociados a los favoritos de Internet Explorer 9 no se desplazan por la virtualización de la experiencia del usuario y no aparecen cuando los favoritos aparecen por primera vez en un equipo nuevo.</span><span class="sxs-lookup"><span data-stu-id="adfa9-152">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="adfa9-153">SOLUCIÓN: favicons aparecerá con sus favoritos asociados una vez que el marcador se use y se almacene en la memoria caché en el explorador Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="adfa9-153">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="adfa9-154">Las rutas de configuración de archivos se almacenan en el registro</span><span class="sxs-lookup"><span data-stu-id="adfa9-154">File settings paths are stored in registry</span></span>

<span data-ttu-id="adfa9-155">Algunas opciones de la aplicación almacenan las rutas de los archivos de configuración y configuración como valores en el registro.</span><span class="sxs-lookup"><span data-stu-id="adfa9-155">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="adfa9-156">Los archivos a los que se hace referencia como rutas en el registro se deben sincronizar cuando se mueven los valores de configuración entre equipos.</span><span class="sxs-lookup"><span data-stu-id="adfa9-156">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="adfa9-157">SOLUCIÓN alternativa: Use el redireccionamiento de carpetas o cualquier otra tecnología para asegurarse de que todos los archivos a los que se hace referencia como rutas de configuración de archivos están presentes y colocados en la misma ubicación en todos los equipos en los que la configuración es móvil.</span><span class="sxs-lookup"><span data-stu-id="adfa9-157">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="adfa9-158">Las rutas de almacenamiento de configuración largas pueden provocar un error</span><span class="sxs-lookup"><span data-stu-id="adfa9-158">Long Settings Storage Paths could cause an error</span></span>

<span data-ttu-id="adfa9-159">Mantenga las rutas de almacenamiento de configuración tan cortas como sea posible.</span><span class="sxs-lookup"><span data-stu-id="adfa9-159">Keep settings storage paths as short as possible.</span></span> <span data-ttu-id="adfa9-160">Las rutas largas pueden impedir la resolución o la sincronización.</span><span class="sxs-lookup"><span data-stu-id="adfa9-160">Long paths could prevent resolution or synchronization.</span></span> <span data-ttu-id="adfa9-161">UE-V usa la ruta de acceso de almacenamiento de configuración como parte de la ruta de acceso calculada para almacenar la configuración.</span><span class="sxs-lookup"><span data-stu-id="adfa9-161">UE-V uses the Settings storage path as part of the calculated path to store settings.</span></span> <span data-ttu-id="adfa9-162">La ruta de acceso se calcula de la siguiente manera: configuración ruta de almacenamiento + "settingspackages" + paquete DIR (ID. de plantilla) + nombre del paquete (ID. de plantilla).</span><span class="sxs-lookup"><span data-stu-id="adfa9-162">That path is calculated in the following way: settings storage path + “settingspackages” + package dir (template ID) + package name (template ID).</span></span> <span data-ttu-id="adfa9-163">Si esa ruta de acceso calculada supera los 260 caracteres, almacenamiento de paquetes fallará y generará el siguiente mensaje de error en el registro de eventos operativos de UE-V:</span><span class="sxs-lookup"><span data-stu-id="adfa9-163">If that calculated path exceeds 260 characters, package storage will fail and generate the following error message in the UE-V operational event log:</span></span>

`[boost::filesystem::copy_file: The system cannot find the path specified]`

<span data-ttu-id="adfa9-164">Para comprobar los eventos de registro operativos, abra el visor de eventos y vaya a registros de aplicaciones y servicios/Microsoft/virtualización de la experiencia de usuario/inicio de sesión/operativo.</span><span class="sxs-lookup"><span data-stu-id="adfa9-164">To check the operational log events, open the Event Viewer and navigate to Applications and Services Logs / Microsoft / User Experience Virtualization / Logging / Operational.</span></span>

<span data-ttu-id="adfa9-165">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="adfa9-165">WORKAROUND: None.</span></span>

### <span data-ttu-id="adfa9-166">Los retrasos del agente UE-V al cerrar sesión o iniciar sesión</span><span class="sxs-lookup"><span data-stu-id="adfa9-166">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="adfa9-167">Si se produce un inicio de sesión o un cierre de sesión antes de que archivos sin conexión haya determinado que hay un vínculo lento, puede que se retrase el cierre de sesión o el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="adfa9-167">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="adfa9-168">La característica de archivos sin conexión puede demorar hasta tres minutos en detectar el estado actual de la red.</span><span class="sxs-lookup"><span data-stu-id="adfa9-168">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="adfa9-169">Si el inicio de sesión o el apagado se produce antes de que los archivos sin conexión hayan determinado que el equipo está conectado a un vínculo de baja velocidad, el paquete de configuración de UE-V se enviará al servidor en lugar de a la caché local.</span><span class="sxs-lookup"><span data-stu-id="adfa9-169">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="adfa9-170">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="adfa9-170">WORKAROUND: None.</span></span>

### <span data-ttu-id="adfa9-171">Conflicto de configuración al intentar trabajar con la configuración del sistema operativo en Windows 8</span><span class="sxs-lookup"><span data-stu-id="adfa9-171">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="adfa9-172">En Windows 8, si la sincronización de cuentas de Microsoft está habilitada junto con UE-V para la configuración del sistema operativo, la configuración que se aplica puede ser incoherente.</span><span class="sxs-lookup"><span data-stu-id="adfa9-172">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="adfa9-173">SOLUCIÓN alternativa: realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="adfa9-173">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="adfa9-174">Deshabilitar la sincronización de cuentas de Microsoft si usa la configuración del sistema operativo UE-V para roaming</span><span class="sxs-lookup"><span data-stu-id="adfa9-174">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="adfa9-175">Deshabilitar UE-V para la configuración del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="adfa9-175">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="adfa9-176">Algunas configuraciones del sistema operativo solo se mueven entre las versiones del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="adfa9-176">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="adfa9-177">La configuración del sistema operativo para narrador y los caracteres de moneda específicos de la configuración regional solo se transferirán a las distintas versiones del sistema operativo de Windows.</span><span class="sxs-lookup"><span data-stu-id="adfa9-177">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="adfa9-178">Por ejemplo, los caracteres de moneda solo se transferirán de Windows 7 a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="adfa9-178">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="adfa9-179">SOLUCIÓN alternativa: ninguna</span><span class="sxs-lookup"><span data-stu-id="adfa9-179">WORKAROUND: None</span></span>

 

 





