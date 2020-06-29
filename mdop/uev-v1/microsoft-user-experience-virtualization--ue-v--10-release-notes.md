---
title: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0
description: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0
author: dansimp
ms.assetid: 920f3fae-e9b5-4b94-beda-32c19d31e94b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9f9942eef7ea84cf7010a0c0173427827a512216
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812487"
---
# <span data-ttu-id="bb161-103">Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0</span><span class="sxs-lookup"><span data-stu-id="bb161-103">Microsoft User Experience Virtualization (UE-V) 1.0 Release Notes</span></span>


<span data-ttu-id="bb161-104">Para buscar las notas de la versión de virtualización de Microsoft User Experience (UE-V), presione Ctrl + F.</span><span class="sxs-lookup"><span data-stu-id="bb161-104">To search Microsoft User Experience Virtualization (UE-V) release notes, press Ctrl+F.</span></span>

<span data-ttu-id="bb161-105">Debe leer estas notas de la versión minuciosamente antes de instalar UE-V.</span><span class="sxs-lookup"><span data-stu-id="bb161-105">You should read these release notes thoroughly before you install UE-V.</span></span> <span data-ttu-id="bb161-106">Las notas de la versión contienen información necesaria para instalar correctamente la virtualización de la experiencia del usuario y contienen información adicional que no está disponible en la documentación del producto.</span><span class="sxs-lookup"><span data-stu-id="bb161-106">The release notes contain information that is required to successfully install User Experience Virtualization, and contain additional information that is not available in the product documentation.</span></span> <span data-ttu-id="bb161-107">Si hay diferencias entre estas notas de la versión y otra documentación de UE-V, el cambio más reciente debe considerarse autoritario.</span><span class="sxs-lookup"><span data-stu-id="bb161-107">If there are differences between these release notes and other UE-V documentation, the latest change should be considered authoritative.</span></span> <span data-ttu-id="bb161-108">Estas notas de la versión reemplazan el contenido que se incluye con este producto.</span><span class="sxs-lookup"><span data-stu-id="bb161-108">These release notes supersede the content that is included with this product.</span></span>

## <span data-ttu-id="bb161-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bb161-109">Providing feedback</span></span>


<span data-ttu-id="bb161-110">Díganos lo que piensa sobre nuestra documentación de MDOP enviándonos sus comentarios y comentarios.</span><span class="sxs-lookup"><span data-stu-id="bb161-110">Tell us what you think about our documentation for MDOP by giving us your feedback and comments.</span></span> <span data-ttu-id="bb161-111">Envíe sus comentarios sobre la documentación a [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span><span class="sxs-lookup"><span data-stu-id="bb161-111">Send your documentation feedback to [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).</span></span>

## <span data-ttu-id="bb161-112">Problemas conocidos de UE-V</span><span class="sxs-lookup"><span data-stu-id="bb161-112">UE-V known issues</span></span>


<span data-ttu-id="bb161-113">Esta sección contiene notas de la versión para la virtualización de la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="bb161-113">This section contains release notes for User Experience Virtualization.</span></span>

### <span data-ttu-id="bb161-114">La configuración del registro no se sincroniza entre App-V y aplicaciones nativas en el mismo equipo</span><span class="sxs-lookup"><span data-stu-id="bb161-114">Registry settings fail to synchronize between App-V and native applications on the same computer</span></span>

<span data-ttu-id="bb161-115">Cuando un equipo tiene una aplicación que está disponible a través de la aplicación Application Virtualization (App-V) y de una aplicación de instalación nativa (instalada con un archivo. msi), la configuración basada en el registro no se sincroniza entre las tecnologías.</span><span class="sxs-lookup"><span data-stu-id="bb161-115">When a computer has an application that is available through both the Application Virtualization (App-V) application and a native installation application (installed with an .msi file), the registry-based settings do not synchronize between the technologies.</span></span>

<span data-ttu-id="bb161-116">SOLUCIÓN alternativa: para resolver este problema, ejecute la aplicación seleccionando una de las dos tecnologías, pero no ambas.</span><span class="sxs-lookup"><span data-stu-id="bb161-116">WORKAROUND: To resolve this problem, run the application by selecting one of the two technologies, but not both.</span></span>

### <span data-ttu-id="bb161-117">Error en la sincronización de configuración de Windows 8: "Boost:: filesystem:: EXISTS:: nombre de usuario o contraseña incorrectos"</span><span class="sxs-lookup"><span data-stu-id="bb161-117">Windows 8 setting synchronization fails with error: "boost::filesystem::exists::Incorrect user name or password"</span></span>

<span data-ttu-id="bb161-118">La sincronización de la configuración del sistema operativo Windows® 8 falla con el siguiente mensaje de error: **Boost:: filesystem:: EXISTS:: nombre de usuario o contraseña incorrectos**.</span><span class="sxs-lookup"><span data-stu-id="bb161-118">The Windows® 8 operating system settings synchronization fails with the following error message: **boost::filesystem::exists::Incorrect user name or password**.</span></span> <span data-ttu-id="bb161-119">Para buscar eventos de registro operativos, abra el **visor de eventos** y vaya a **registros de aplicaciones y servicios**  /  **Microsoft**  /  **User Experience virtualización**  /  **Logging**  /  **operativo**.</span><span class="sxs-lookup"><span data-stu-id="bb161-119">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span> <span data-ttu-id="bb161-120">Los recursos compartidos de red que se usan para la configuración de UE-V las ubicaciones de almacenamiento deben residir en el mismo dominio de Active Directory que el usuario.</span><span class="sxs-lookup"><span data-stu-id="bb161-120">Network shares that are used for UE-V settings storage locations should reside in the same Active Directory domain as the user.</span></span> <span data-ttu-id="bb161-121">De lo contrario, puede producirse el siguiente error: "nombre de usuario o contraseña incorrectos".</span><span class="sxs-lookup"><span data-stu-id="bb161-121">Otherwise, the following error might occur: "Incorrect user name or password".</span></span>

<span data-ttu-id="bb161-122">SOLUCIÓN: Use recursos compartidos de red del mismo dominio de Active Directory que el usuario.</span><span class="sxs-lookup"><span data-stu-id="bb161-122">WORKAROUND: Use network shares from the same Active Directory domain as the user.</span></span> <span data-ttu-id="bb161-123">.</span><span class="sxs-lookup"><span data-stu-id="bb161-123">.</span></span>

### <span data-ttu-id="bb161-124">Itinerancia de la firma de correo electrónico para Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="bb161-124">Email signature roaming for Outlook 2010</span></span>

<span data-ttu-id="bb161-125">UE-V moverá los archivos de firma de Outlook 2010 entre dispositivos.</span><span class="sxs-lookup"><span data-stu-id="bb161-125">UE-V will roam the Outlook 2010 signature files between devices.</span></span> <span data-ttu-id="bb161-126">Sin embargo, las opciones de firma predeterminadas para los mensajes nuevos y las respuestas y reenvíos no son.</span><span class="sxs-lookup"><span data-stu-id="bb161-126">However, the default signature options for new messages and replies/forwards are not.</span></span><span data-ttu-id="bb161-127">Estas dos configuraciones se almacenan en el perfil de Outlook, que UE no Vdoes.</span><span class="sxs-lookup"><span data-stu-id="bb161-127"> These two settings are stored in the Outlook profile, which UE-Vdoes not roam.</span></span>

<span data-ttu-id="bb161-128">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb161-128">WORKAROUND: None.</span></span>

### <span data-ttu-id="bb161-129">La configuración de sincronización no se sincroniza en el intervalo esperado cuando se ejecuta en modo de vínculo de baja velocidad</span><span class="sxs-lookup"><span data-stu-id="bb161-129">Synchronization settings do not synchronize on expected interval when running in slow-link mode</span></span>

<span data-ttu-id="bb161-130">En condiciones normales, configuración las ubicaciones de almacenamiento deberían estar disponibles a través de una conexión de red de vínculo rápido.</span><span class="sxs-lookup"><span data-stu-id="bb161-130">Under normal conditions, settings storage locations should be available over a fast link network connection.</span></span> <span data-ttu-id="bb161-131">En el modo de vínculo de baja velocidad, la sincronización solo se realizará de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="bb161-131">In slow-link mode, synchronization will only occur on a periodic basis.</span></span> <span data-ttu-id="bb161-132">De forma predeterminada, la programación de sincronización del modo de vínculos lentos se establece en cada 360 minutos.</span><span class="sxs-lookup"><span data-stu-id="bb161-132">By default, the slow-link mode synchronization schedule is set to every 360 minutes.</span></span>

<span data-ttu-id="bb161-133">SOLUCIÓN: para cambiar la frecuencia de la sincronización en segundo plano para equipos en modo de vínculo de baja velocidad, puede configurar la Directiva de grupo para la Directiva de sincronización en segundo plano para **archivos sin conexión**.</span><span class="sxs-lookup"><span data-stu-id="bb161-133">WORKAROUND: To change the frequency of the background synchronization for computers in slow-link mode, you can configure the Group Policy for Background Sync policy for **Offline files**.</span></span>

### <span data-ttu-id="bb161-134">Los caracteres especiales no se sincronizan</span><span class="sxs-lookup"><span data-stu-id="bb161-134">Special characters do not synchronize</span></span>

<span data-ttu-id="bb161-135">Ciertos caracteres, como los símbolos de moneda, no se sincronizan entre equipos con Windows 7 y Windows 8 que ejecutan el agente de UE-V.</span><span class="sxs-lookup"><span data-stu-id="bb161-135">Certain characters, such as currency symbols, do not synchronize between Windows 7 and Windows 8 computers that run the UE-V agent.</span></span>

<span data-ttu-id="bb161-136">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb161-136">WORKAROUND: None.</span></span>

### <span data-ttu-id="bb161-137">UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="bb161-137">UE-V does not support roaming settings between 32-bit and 64-bit versions of Microsoft Office</span></span>

<span data-ttu-id="bb161-138">Le recomendamos que instale la versión de 32 bits de Microsoft Office para sistemas operativos de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="bb161-138">We recommend that you install the 32-bit version of Microsoft Office for both 32-bit and 64-bit operating systems.</span></span> <span data-ttu-id="bb161-139">Para elegir la versión de Microsoft Office que necesita, haga clic aquí.</span><span class="sxs-lookup"><span data-stu-id="bb161-139">To choose the Microsoft Office version that you need, click here.</span></span> <span data-ttu-id="bb161-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span><span class="sxs-lookup"><span data-stu-id="bb161-140">([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)).</span></span> <span data-ttu-id="bb161-141">UE-V admite la configuración de itinerancia entre versiones de arquitectura idénticas de Office.</span><span class="sxs-lookup"><span data-stu-id="bb161-141">UE-V supports roaming settings between identical architecture versions of Office.</span></span> <span data-ttu-id="bb161-142">Por ejemplo, la configuración de Office de 32 bits se transferirá entre todas las instancias de Office de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bb161-142">For example, 32-bit Office settings will roam between all 32-bit Office instances.</span></span> <span data-ttu-id="bb161-143">UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Office.</span><span class="sxs-lookup"><span data-stu-id="bb161-143">UE-V does not support roaming settings between 32-bit and 64-bit versions of Office.</span></span>

<span data-ttu-id="bb161-144">SOLUCIÓN alternativa: ninguna</span><span class="sxs-lookup"><span data-stu-id="bb161-144">WORKAROUND: None</span></span>

### <span data-ttu-id="bb161-145">Otras carpetas del recurso compartido con la ubicación de almacenamiento de configuración no están disponibles en modo de conexión lenta</span><span class="sxs-lookup"><span data-stu-id="bb161-145">Other folders on the share with the setting storage location are unavailable in slow-connection mode</span></span>

<span data-ttu-id="bb161-146">La configuración de almacenar recursos compartidos no se encuentra en un recurso compartido de red que se usa para otras carpetas que siempre deben estar disponibles.</span><span class="sxs-lookup"><span data-stu-id="bb161-146">Settings store shares should not be located on a network share that is used for other folders that must always be available.</span></span> <span data-ttu-id="bb161-147">Cuando el recurso compartido de red que hospeda la ubicación de almacenamiento de configuración pasa al modo de conexión lenta, la única carpeta disponible es la de ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="bb161-147">When the network share that hosts the setting storage location goes into slow-connection mode, the only available folder is the settings storage location folder.</span></span> <span data-ttu-id="bb161-148">Otras carpetas del recurso compartido no están disponibles en modo de conexión lenta.</span><span class="sxs-lookup"><span data-stu-id="bb161-148">Other folders on the Share are not available in slow-connection mode.</span></span>

<span data-ttu-id="bb161-149">Solución alternativa: ninguna</span><span class="sxs-lookup"><span data-stu-id="bb161-149">Workaround: None</span></span>

### <span data-ttu-id="bb161-150">Los favicons asociados a los favoritos de Internet Explorer 9 no se mueven</span><span class="sxs-lookup"><span data-stu-id="bb161-150">Favicons that are associated with Internet Explorer 9 favorites do not roam</span></span>

<span data-ttu-id="bb161-151">Los favicons asociados a los favoritos de Internet Explorer 9 no se desplazan por la virtualización de la experiencia del usuario y no aparecen cuando los favoritos aparecen por primera vez en un equipo nuevo.</span><span class="sxs-lookup"><span data-stu-id="bb161-151">The favicons that are associated with Internet Explorer 9 favorites are not roamed by User Experience Virtualization and do not appear when the favorites first appear on a new computer.</span></span>

<span data-ttu-id="bb161-152">SOLUCIÓN: favicons aparecerá con sus favoritos asociados una vez que el marcador se use y se almacene en la memoria caché en el explorador Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bb161-152">WORKAROUND: Favicons will appear with their associated favorites once the bookmark is used and cached in the Internet Explorer 9 browser.</span></span>

### <span data-ttu-id="bb161-153">Las rutas de configuración de archivos se almacenan en el registro</span><span class="sxs-lookup"><span data-stu-id="bb161-153">File settings paths are stored in registry</span></span>

<span data-ttu-id="bb161-154">Algunas opciones de la aplicación almacenan las rutas de los archivos de configuración y configuración como valores en el registro.</span><span class="sxs-lookup"><span data-stu-id="bb161-154">Some application settings store the paths of their configuration and settings files as values in the registry.</span></span> <span data-ttu-id="bb161-155">Los archivos a los que se hace referencia como rutas en el registro se deben sincronizar cuando se mueven los valores de configuración entre equipos.</span><span class="sxs-lookup"><span data-stu-id="bb161-155">The files that are referenced as paths in the registry must be synchronized when settings are roamed between computers.</span></span>

<span data-ttu-id="bb161-156">SOLUCIÓN alternativa: Use el redireccionamiento de carpetas o cualquier otra tecnología para asegurarse de que todos los archivos a los que se hace referencia como rutas de configuración de archivos están presentes y colocados en la misma ubicación en todos los equipos en los que la configuración es móvil.</span><span class="sxs-lookup"><span data-stu-id="bb161-156">WORKAROUND: Use folder redirection or some other technology to ensure that any files that are referenced as file settings paths are present and placed in the same location on all computers where settings roam.</span></span>

### <span data-ttu-id="bb161-157">No se admiten rutas de más de 260 caracteres</span><span class="sxs-lookup"><span data-stu-id="bb161-157">Paths longer than 260 characters are not supported</span></span>

<span data-ttu-id="bb161-158">Las rutas de almacenamiento de configuración con más de 260 caracteres no se admiten.</span><span class="sxs-lookup"><span data-stu-id="bb161-158">Settings storage paths that are longer than 260 characters are not supported.</span></span> <span data-ttu-id="bb161-159">Se producirá un error al copiar los paquetes de configuración de UE-V en las rutas de almacenamiento de configuración de más de 260 caracteres y se generará el siguiente mensaje de excepción en el registro de eventos operativos de UE-V: **\ [Boost:: filesystem:: Copy \ _file: el sistema no puede encontrar la ruta de acceso especificada \]**.</span><span class="sxs-lookup"><span data-stu-id="bb161-159">Copying the UE-V settings packages to settings storage paths that are longer than 260 characters will fail and generate the following exception message in the UE-V operational event log: **\[boost::filesystem::copy\_file: The system cannot find the path specified\]**.</span></span> <span data-ttu-id="bb161-160">Para buscar eventos de registro operativos, abra el **visor de eventos** y vaya a **registros de aplicaciones y servicios**  /  **Microsoft**  /  **User Experience virtualización**  /  **Logging**  /  **operativo**.</span><span class="sxs-lookup"><span data-stu-id="bb161-160">To check for operational log events, open the **Event Viewer** and navigate to **Applications and Services Logs** / **Microsoft** / **User Experience Virtualization** / **Logging** / **Operational**.</span></span>

<span data-ttu-id="bb161-161">Actualmente no se admiten las rutas de configuración de archivo de más de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="bb161-161">File settings paths that are longer than 260 characters are not currently supported.</span></span> <span data-ttu-id="bb161-162">La configuración de archivo a la que se hace referencia en la configuración de UE-V plantillas de ubicación no se puede encontrar en una ruta de directorio que tenga más de 260 caracteres.</span><span class="sxs-lookup"><span data-stu-id="bb161-162">File settings that are referenced in UE-V settings location templates cannot be located in a directory path that is longer than 260 characters.</span></span>

<span data-ttu-id="bb161-163">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb161-163">WORKAROUND: None.</span></span>

### <span data-ttu-id="bb161-164">Los retrasos del agente UE-V al cerrar sesión o iniciar sesión</span><span class="sxs-lookup"><span data-stu-id="bb161-164">UE-V agent delays upon logout or login</span></span>

<span data-ttu-id="bb161-165">Si se produce un inicio de sesión o un cierre de sesión antes de que archivos sin conexión haya determinado que hay un vínculo lento, puede que se retrase el cierre de sesión o el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="bb161-165">If a logon or logout occurs before Offline Files has determined that a slow link is in place, logout or login might be delayed.</span></span> <span data-ttu-id="bb161-166">La característica de archivos sin conexión puede demorar hasta tres minutos en detectar el estado actual de la red.</span><span class="sxs-lookup"><span data-stu-id="bb161-166">The Offline Files feature may take up to three minutes to detect the current network state.</span></span> <span data-ttu-id="bb161-167">Si el inicio de sesión o el apagado se produce antes de que los archivos sin conexión hayan determinado que el equipo está conectado a un vínculo de baja velocidad, el paquete de configuración de UE-V se enviará al servidor en lugar de a la caché local.</span><span class="sxs-lookup"><span data-stu-id="bb161-167">If the logon or shutdown occurs before Offline Files has determined that the computer is connected to a slow link, the UE-V settings package will be sent to the server instead of the local cache.</span></span>

<span data-ttu-id="bb161-168">SOLUCIÓN alternativa: ninguno.</span><span class="sxs-lookup"><span data-stu-id="bb161-168">WORKAROUND: None.</span></span>

### <span data-ttu-id="bb161-169">Conflicto de configuración al intentar trabajar con la configuración del sistema operativo en Windows 8</span><span class="sxs-lookup"><span data-stu-id="bb161-169">Settings conflict when trying to roam operating system settings on Windows 8</span></span>

<span data-ttu-id="bb161-170">En Windows 8, si la sincronización de cuentas de Microsoft está habilitada junto con UE-V para la configuración del sistema operativo, la configuración que se aplica puede ser incoherente.</span><span class="sxs-lookup"><span data-stu-id="bb161-170">On Windows 8 if Microsoft Account Sync is enabled along with UE-V for operating system settings, the settings that are applied may be inconsistent.</span></span>

<span data-ttu-id="bb161-171">SOLUCIÓN alternativa: realice una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="bb161-171">WORKAROUND: Do one of the following:</span></span>

-   <span data-ttu-id="bb161-172">Deshabilitar la sincronización de cuentas de Microsoft si usa la configuración del sistema operativo UE-V para roaming</span><span class="sxs-lookup"><span data-stu-id="bb161-172">Disable Microsoft Account Sync if you are using UE-V to roam operating system settings</span></span>

-   <span data-ttu-id="bb161-173">Deshabilitar UE-V para la configuración del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bb161-173">Disable UE-V for operating system settings</span></span>

### <span data-ttu-id="bb161-174">Algunas configuraciones del sistema operativo solo se mueven entre las versiones del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bb161-174">Some operating system settings only roam between like operating system versions</span></span>

<span data-ttu-id="bb161-175">La configuración del sistema operativo para narrador y los caracteres de moneda específicos de la configuración regional solo se transferirán a las distintas versiones del sistema operativo de Windows.</span><span class="sxs-lookup"><span data-stu-id="bb161-175">Operating system settings for Narrator and currency characters specific to the locale will only roam across like operating system versions of Windows.</span></span> <span data-ttu-id="bb161-176">Por ejemplo, los caracteres de moneda solo se transferirán de Windows 7 a Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bb161-176">For example currency characters will only roam from Windows 7 to Windows 7.</span></span>

<span data-ttu-id="bb161-177">SOLUCIÓN alternativa: ninguna</span><span class="sxs-lookup"><span data-stu-id="bb161-177">WORKAROUND: None</span></span>

### <span data-ttu-id="bb161-178">Los marcadores de Internet Explorer no aparecen en la SmartBar de Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="bb161-178">Internet Explorer bookmarks do not appear in the Internet Explorer smartbar</span></span>

<span data-ttu-id="bb161-179">Cuando los marcadores de Internet Explorer se transfieren de un equipo a otro, el índice del segundo equipo no se puede actualizar, por lo que, cuando se escribe en la barra de direcciones, el favorito no aparecerá como un posible resultado de búsqueda en el equipo 2.</span><span class="sxs-lookup"><span data-stu-id="bb161-179">When Internet Explorer bookmarks roam from one computer to another computer, the index on the second computer cannot update, so when typing in the address bar, the favorite will not appear as a possible search result on computer 2.</span></span>

<span data-ttu-id="bb161-180">SOLUCIÓN alternativa: ninguna</span><span class="sxs-lookup"><span data-stu-id="bb161-180">WORKAROUND: None</span></span>

 

 





