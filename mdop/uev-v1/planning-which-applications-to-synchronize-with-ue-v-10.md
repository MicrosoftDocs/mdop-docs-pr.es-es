---
title: Planificación de las aplicaciones a sincronizar con UE-V 1.0
description: Planificación de las aplicaciones a sincronizar con UE-V 1.0
author: dansimp
ms.assetid: c718274f-87b4-47f3-8ef7-5e1bd5557a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f2b04942588d0f6efad03d5e0249534cd325c09
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812415"
---
# <span data-ttu-id="1dfc9-103">Planificación de las aplicaciones a sincronizar con UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="1dfc9-103">Planning Which Applications to Synchronize with UE-V 1.0</span></span>


<span data-ttu-id="1dfc9-104">La virtualización de la experiencia del usuario de Microsoft (UE-V) usa plantillas de ubicación de configuración (archivos XML) que definen la configuración que captura y aplica UE-V.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="1dfc9-105">UE-V incluye un conjunto de plantillas de ubicación de configuración predefinidas y también permite a los administradores crear plantillas de ubicación de configuración personalizada para aplicaciones de terceros o de línea de negocio que se usan en la empresa.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-105">UE-V includes a set of predefined settings location templates and also allows administrators to create custom settings location templates for third-party or line-of-business applications that are used in the enterprise.</span></span>

<span data-ttu-id="1dfc9-106">Como administrador, cuando considere qué aplicaciones incluir en su solución de UE-V, considere qué opciones puede personalizar un usuario y cómo y dónde se almacenará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-106">As an administrator, when you consider which applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="1dfc9-107">No todas las aplicaciones tienen opciones de configuración que se pueden personalizar o que los usuarios personalizan rutinariamente.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-107">Not all applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="1dfc9-108">Además, no todas las configuraciones de aplicaciones pueden moverse de forma segura en varios equipos o entornos.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-108">In addition, not all applications settings can safely roam across multiple computers or environments.</span></span> <span data-ttu-id="1dfc9-109">Sincronizar la configuración que cumpla los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="1dfc9-109">Synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="1dfc9-110">Configuración que se almacena en ubicaciones accesibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-110">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="1dfc9-111">Por ejemplo, no sincronice la configuración almacenada en la sección de de system32 o exterior HKCU del registro.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-111">For example, do not synchronize settings that are stored in system32 or outside HKCU section of the registry.</span></span>

-   <span data-ttu-id="1dfc9-112">Configuración que no es específica del equipo en particular.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-112">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="1dfc9-113">Por ejemplo, excluya la configuración de red o de hardware.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-113">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="1dfc9-114">Configuración que se puede sincronizar entre equipos sin riesgo de datos dañados.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-114">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="1dfc9-115">Por ejemplo, no use la configuración almacenada en un archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-115">For example, do not use settings that are stored in a database file.</span></span>

## <span data-ttu-id="1dfc9-116">Plantillas de ubicación de configuración incluidas en UE-V</span><span class="sxs-lookup"><span data-stu-id="1dfc9-116">Settings location templates that are included in UE-V</span></span>


**<span data-ttu-id="1dfc9-117">Plantillas de ubicación de configuración de aplicación de UE-V</span><span class="sxs-lookup"><span data-stu-id="1dfc9-117">UE-V application settings location templates</span></span>**

<span data-ttu-id="1dfc9-118">El software de instalación de UE-V Agent instala el agente y registra un grupo predeterminado de plantillas de ubicación de configuración para las aplicaciones comunes de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-118">The UE-V agent installation software installs the agent and registers a default group of settings location templates for common Microsoft applications.</span></span> <span data-ttu-id="1dfc9-119">Estas plantillas de ubicación de configuración capturan valores de configuración para las siguientes aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="1dfc9-119">These settings location templates capture settings values for the following applications:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="1dfc9-120">Categoría de aplicación</span><span class="sxs-lookup"><span data-stu-id="1dfc9-120">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="1dfc9-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1dfc9-121">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dfc9-122">Aplicaciones de Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="1dfc9-122">Microsoft Office 2010 applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfc9-123">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="1dfc9-123">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="1dfc9-124">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="1dfc9-124">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="1dfc9-125">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="1dfc9-125">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="1dfc9-126">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="1dfc9-126">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="1dfc9-127">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="1dfc9-127">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="1dfc9-128">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="1dfc9-128">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="1dfc9-129">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="1dfc9-129">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="1dfc9-130">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="1dfc9-130">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="1dfc9-131">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="1dfc9-131">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="1dfc9-132">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="1dfc9-132">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="1dfc9-133">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="1dfc9-133">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="1dfc9-134">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="1dfc9-134">Microsoft OneNote 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dfc9-135">Opciones del explorador (Internet Explorer 8, Internet Explorer 9 e Internet Explorer 10)</span><span class="sxs-lookup"><span data-stu-id="1dfc9-135">Browser options (Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10)</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfc9-136">Favoritos, Página principal, pestañas y barras de herramientas.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-136">Favorites, home page, tabs, and toolbars.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dfc9-137">Accesorios de Windows</span><span class="sxs-lookup"><span data-stu-id="1dfc9-137">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfc9-138">Calculadora, Bloc de notas, WordPad.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-138">Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1dfc9-139">La configuración de la aplicación se aplica a la aplicación cuando se inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-139">Application settings are applied to the application when the application is started.</span></span> <span data-ttu-id="1dfc9-140">Se guardan cuando se cierra la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-140">They are saved when the application closes.</span></span>

**<span data-ttu-id="1dfc9-141">Plantillas de ubicación de configuración de UE-V Windows</span><span class="sxs-lookup"><span data-stu-id="1dfc9-141">UE-V Windows settings location templates</span></span>**

<span data-ttu-id="1dfc9-142">La virtualización de la experiencia del usuario incluye plantillas de ubicación de configuración que capturan valores de configuración para la siguiente configuración de Windows:</span><span class="sxs-lookup"><span data-stu-id="1dfc9-142">User Experience Virtualization includes settings location templates that capture settings values for the following Windows settings:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="1dfc9-143">Configuración de Windows</span><span class="sxs-lookup"><span data-stu-id="1dfc9-143">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="1dfc9-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="1dfc9-144">Description</span></span></th>
<th align="left"><span data-ttu-id="1dfc9-145">Aplicar en</span><span class="sxs-lookup"><span data-stu-id="1dfc9-145">Apply on</span></span></th>
<th align="left"><span data-ttu-id="1dfc9-146">Estado predeterminado</span><span class="sxs-lookup"><span data-stu-id="1dfc9-146">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dfc9-147">Fondo de escritorio</span><span class="sxs-lookup"><span data-stu-id="1dfc9-147">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfc9-148">Actualmente está activo el fondo de escritorio.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-148">Currently active desktop background.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfc9-149">Iniciar sesión, desbloquear, conexión remota.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-149">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfc9-150">Habilitado</span><span class="sxs-lookup"><span data-stu-id="1dfc9-150">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="1dfc9-151">Accesibilidad</span><span class="sxs-lookup"><span data-stu-id="1dfc9-151">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfc9-152">Accesibilidad y configuración de entrada, lupa, narrador y teclado en pantalla.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-152">Accessibility and input settings, magnifier, Narrator, and on-Screen keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfc9-153">Iniciar sesión, desbloquear, conexión remota.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-153">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfc9-154">Deshabilitado</span><span class="sxs-lookup"><span data-stu-id="1dfc9-154">Disabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="1dfc9-155">Configuración del escritorio</span><span class="sxs-lookup"><span data-stu-id="1dfc9-155">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfc9-156">Configuración del menú Inicio y de la barra de tareas, opciones de carpeta, iconos predeterminados del escritorio, relojes adicionales y configuración de región e idioma.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-156">Start menu and Taskbar settings, Folder options, default desktop icons, additional clocks, and region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfc9-157">Solo inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-157">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="1dfc9-158">Deshabilitado</span><span class="sxs-lookup"><span data-stu-id="1dfc9-158">Disabled</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="1dfc9-159">La configuración de la accesibilidad y el fondo de escritorio de Windows se aplica cuando el usuario inicia sesión, cuando el equipo está desbloqueado o cuando se trata de una conexión remota a otro equipo.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-159">The Windows desktop background and Ease of Access settings are applied when the user logs on, when the computer is unlocked, or upon remote connection to another computer.</span></span> <span data-ttu-id="1dfc9-160">El agente guarda esta configuración cuando el usuario cierra la sesión, cuando el equipo está bloqueado o cuando se desconecta una conexión remota.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-160">The agent saves these settings when the user logs off, when the computer is locked, or when a remote connection is disconnected.</span></span> <span data-ttu-id="1dfc9-161">De forma predeterminada, la configuración de fondo de escritorio de Windows se mueve entre equipos con la misma versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-161">By default, Windows desktop background settings are roamed between computers of the same operating system version.</span></span>

<span data-ttu-id="1dfc9-162">La configuración del escritorio de Windows y de accesibilidad se aplica al iniciar sesión antes de que se presente al usuario el escritorio.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-162">Windows desktop and Ease of Access settings are applied at logon before the desktop is presented to the user.</span></span> <span data-ttu-id="1dfc9-163">Para optimizar la experiencia de inicio de sesión, esta configuración no se mueve de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-163">To optimize the logon experience, these settings are not roamed by default.</span></span> <span data-ttu-id="1dfc9-164">La configuración del escritorio y la facilidad de acceso se puede habilitar mediante la Directiva de grupo, PowerShell y WMI.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-164">Desktop and Ease of Access settings can be enabled by using Group Policy, PowerShell, and WMI.</span></span>

<span data-ttu-id="1dfc9-165">UE-V no admite la itinerancia de configuración entre sistemas operativos con distintos idiomas.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-165">UE-V does not support the roaming of settings between operating systems with different languages.</span></span> <span data-ttu-id="1dfc9-166">Por ejemplo, no es compatible con la sincronización entre el inglés y el alemán.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-166">For example, synchronization between English and German is not supported.</span></span> <span data-ttu-id="1dfc9-167">El idioma de todos los equipos a los que UE-V roaming la configuración del usuario debe coincidir.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-167">The language of all computers to which UE-V roams the user settings must match.</span></span>

<span data-ttu-id="1dfc9-168">**Nota:**  Si cambia las plantillas de ubicación de configuración que proporciona Microsoft, es posible que la característica de virtualización de la experiencia del usuario no funcione correctamente para el grupo de configuración de Windows o la aplicación designada.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-168">**Note** If you change the settings location templates that are provided by Microsoft, User Experience Virtualization might not work properly for the designated application or Windows settings group.</span></span>

 

## <a href="" id="prevent-unintentional-user-settings-configuration-"></a><span data-ttu-id="1dfc9-169">Evitar la configuración de un usuario no intencionado</span><span class="sxs-lookup"><span data-stu-id="1dfc9-169">Prevent unintentional user Settings configuration</span></span>


<span data-ttu-id="1dfc9-170">La virtualización de la experiencia del usuario comprueba la información de la nueva configuración de usuario y la descarga según corresponda desde una ubicación de almacenamiento de configuración.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-170">User Experience Virtualization checks for new user settings information, and downloads that information accordingly from a settings storage location.</span></span> <span data-ttu-id="1dfc9-171">A continuación, aplica la configuración al equipo local en los casos siguientes:</span><span class="sxs-lookup"><span data-stu-id="1dfc9-171">Then, it applies the settings to the local computer in the following cases:</span></span>

-   <span data-ttu-id="1dfc9-172">Cada vez que se inicia una aplicación que tiene una plantilla registrada de UE-V.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-172">Every time an application is launched that has a registered UE-V template.</span></span>

-   <span data-ttu-id="1dfc9-173">Cuando un usuario inicia sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-173">When a user logs on to their computer.</span></span>

-   <span data-ttu-id="1dfc9-174">Cuando un usuario desbloquea su equipo.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-174">When a user unlocks their computer.</span></span>

-   <span data-ttu-id="1dfc9-175">Cuando se establece una conexión con un equipo de escritorio remoto que tiene UE-V instalado.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-175">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

<span data-ttu-id="1dfc9-176">Si UE-V está instalado en el equipo a y en el equipo B, y la configuración deseada para la aplicación en el equipo A, el equipo a debe abrir y cerrar la aplicación en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-176">If UE-V is installed on computer A and computer B, and the desired settings for the application are on computer A, then computer A must open and close the application first.</span></span> <span data-ttu-id="1dfc9-177">Si una aplicación se abre y cierra en el equipo B, la configuración de la aplicación en el equipo a se configurará para que sea la misma que la configuración de la aplicación en el equipo B.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-177">If an application is opened and closed on computer B first, then the application settings on computer A will be configured to be the same as the application settings on computer B.</span></span>

<span data-ttu-id="1dfc9-178">Este escenario también se aplica a la configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-178">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="1dfc9-179">Si la configuración de Windows en el equipo B debe ser la misma que la configuración de Windows del equipo A, entonces el usuario debe iniciar sesión y cerrar la sesión en primer lugar.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-179">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should logon and logoff computer A first.</span></span>

<span data-ttu-id="1dfc9-180">Si la configuración de usuario deseada se aplica en el orden equivocado, se puede recuperar ejecutando una operación de restauración para la aplicación específica o configuración de Windows en el equipo en el que se sobrescribió la configuración.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-180">If the desired user settings are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="1dfc9-181">Para obtener más información, consulte restauración de la [aplicación y configuración de Windows sincronizada con UE-V 1,0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="1dfc9-181">For more information, see [Restoring Application and Windows Settings Synchronized with UE-V 1.0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).</span></span>

## <span data-ttu-id="1dfc9-182">Plantillas de ubicación de configuración personalizada de UE-V</span><span class="sxs-lookup"><span data-stu-id="1dfc9-182">Custom UE-V settings location templates</span></span>


<span data-ttu-id="1dfc9-183">Puede crear plantillas de ubicación de configuración personalizadas con el generador de UE-V.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-183">You can create custom settings location templates by using the UE-V Generator.</span></span> <span data-ttu-id="1dfc9-184">Después de crear y probar una plantilla de ubicación de configuración personalizada en un entorno de prueba, puede implementar las plantillas de ubicación de configuración en los equipos de la empresa.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-184">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span> <span data-ttu-id="1dfc9-185">Las plantillas de ubicación de configuración personalizada deben implementarse con una infraestructura de implementación existente, como el método de distribución de software empresarial (ESD), con preferencias, o mediante la configuración de un catálogo de plantillas de configuración de UE-V.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-185">Custom settings location templates must be deployed with an existing deployment infrastructure, such as enterprise software distribution (ESD) method, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="1dfc9-186">Las plantillas implementadas con ESD o una directiva de grupo se deben registrar con el WMI o PowerShell de UE-V.</span><span class="sxs-lookup"><span data-stu-id="1dfc9-186">Templates that are deployed with ESD or Group Policy must be registered by using UE-V WMI or PowerShell.</span></span> <span data-ttu-id="1dfc9-187">Para obtener más información sobre las plantillas de ubicación de configuración personalizada, consulte [planificación de la implementación de plantillas personalizadas para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="1dfc9-187">For more information about custom settings location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

<span data-ttu-id="1dfc9-188">Para obtener instrucciones sobre si debe sincronizarse una aplicación de línea de negocio, vea [lista de comprobación para evaluar las aplicaciones de línea de negocio de UE-V 1,0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="1dfc9-188">For guidance on whether a line-of-business application should be synchronized, see [Checklist for Evaluating Line-of-Business Applications for UE-V 1.0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).</span></span>

## <span data-ttu-id="1dfc9-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1dfc9-189">Related topics</span></span>


[<span data-ttu-id="1dfc9-190">Planificación de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="1dfc9-190">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="1dfc9-191">Planificación de la implementación de la plantilla personalizada para UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="1dfc9-191">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

[<span data-ttu-id="1dfc9-192">Implementación de UE-V 1.0</span><span class="sxs-lookup"><span data-stu-id="1dfc9-192">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

 

 





