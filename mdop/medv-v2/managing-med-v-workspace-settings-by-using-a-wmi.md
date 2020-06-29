---
title: Administrar la configuración de área de trabajo de MED-V mediante el uso de un WMI
description: Administrar la configuración de área de trabajo de MED-V mediante el uso de un WMI
author: dansimp
ms.assetid: 05a665a3-2309-46c1-babb-a3e3bbb0b1f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e74e6fa4944ce0dacd5503baec73044b231abe83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826131"
---
# <span data-ttu-id="513ff-103">Administrar la configuración de área de trabajo de MED-V mediante el uso de un WMI</span><span class="sxs-lookup"><span data-stu-id="513ff-103">Managing MED-V Workspace Settings by Using a WMI</span></span>


<span data-ttu-id="513ff-104">Puede usar el instrumental de administración de Windows (WMI) en Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 para administrar la configuración actual.</span><span class="sxs-lookup"><span data-stu-id="513ff-104">You can use Windows Management Instrumentation (WMI) in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 to manage your current configuration settings.</span></span>

## <span data-ttu-id="513ff-105">Para administrar la configuración del área de trabajo de MED-V con un WMI</span><span class="sxs-lookup"><span data-stu-id="513ff-105">To manage MED-V workspace settings with a WMI</span></span>


<span data-ttu-id="513ff-106">Una herramienta de navegación de WMI le permite ver y editar la configuración en un área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="513ff-106">A WMI browsing tool lets you view and edit the settings in a MED-V workspace.</span></span> <span data-ttu-id="513ff-107">El proveedor WMI se implementa mediante el marco de extensiones del proveedor WMI de Microsoft .NET Framework 3,5.</span><span class="sxs-lookup"><span data-stu-id="513ff-107">The WMI provider is implemented by using the WMI Provider Extension framework from the Microsoft .Net Framework 3.5.</span></span>

<span data-ttu-id="513ff-108">El proveedor WMI se implementa en el espacio de nombres **root\\microsoft\\medv** e implementa la **configuración**de clase.</span><span class="sxs-lookup"><span data-stu-id="513ff-108">The WMI provider is implemented in the **root\\microsoft\\medv** namespace and implements the class **Setting**.</span></span> <span data-ttu-id="513ff-109">La **configuración** de clase contiene propiedades que corresponden a la configuración del registro del sistema que se encuentra en la clave de registro HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv.</span><span class="sxs-lookup"><span data-stu-id="513ff-109">The class **Setting** contains properties that correspond to the settings in the system registry under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv registry key.</span></span>

<span data-ttu-id="513ff-110">**PRECAUCIÓN**  Las herramientas de exploración de WMI se pueden usar para eliminar o modificar clases e instancias.</span><span class="sxs-lookup"><span data-stu-id="513ff-110">**Caution** WMI browsing tools can be used to delete or modify classes and instances.</span></span> <span data-ttu-id="513ff-111">Eliminar o modificar determinadas clases e instancias puede provocar la pérdida de datos valiosos y hacer que MED-V funcione de manera impredecible.</span><span class="sxs-lookup"><span data-stu-id="513ff-111">Deleting or modifying certain classes and instances can result in the loss of valuable data and cause MED-V to function unpredictably.</span></span>

 

<span data-ttu-id="513ff-112">Puede usar la herramienta de navegación WMI que prefiera para ver y editar las opciones de configuración de MED-V siguiendo estos pasos.</span><span class="sxs-lookup"><span data-stu-id="513ff-112">You can use your preferred WMI browsing tool to view and edit MED-V configuration settings by following these steps.</span></span>

1.  <span data-ttu-id="513ff-113">Abre la herramienta de navegación WMI que prefieras con permisos de administrador.</span><span class="sxs-lookup"><span data-stu-id="513ff-113">Open your preferred WMI browsing tool with administrator permissions.</span></span>

2.  <span data-ttu-id="513ff-114">Conéctese al espacio de nombres **root\\microsoft\\medv**.</span><span class="sxs-lookup"><span data-stu-id="513ff-114">Connect to the namespace **root\\microsoft\\medv**.</span></span>

3.  <span data-ttu-id="513ff-115">Enumera las instancias para conectarte a la instancia que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="513ff-115">Enumerate the instances to connect to the running instance.</span></span> <span data-ttu-id="513ff-116">Desea conectarse a la instancia de la **configuración**de la clase.</span><span class="sxs-lookup"><span data-stu-id="513ff-116">You want to connect to the instance of the class **Setting**.</span></span>

    <span data-ttu-id="513ff-117">Se abrirá una ventana del **Editor de objetos** .</span><span class="sxs-lookup"><span data-stu-id="513ff-117">An **Object Editor** window opens.</span></span> <span data-ttu-id="513ff-118">La configuración de MED-V se muestra como **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="513ff-118">The MED-V configuration settings are listed as **Properties**.</span></span>

<span data-ttu-id="513ff-119">Realice los siguientes pasos para editar una configuración de MED-V en el WMI.</span><span class="sxs-lookup"><span data-stu-id="513ff-119">Perform the following steps to edit a MED-V configuration setting in the WMI.</span></span>

1.  <span data-ttu-id="513ff-120">En la lista de **propiedades** de la ventana **Editor de objetos** , haga doble clic en el nombre de la opción de configuración que desea editar.</span><span class="sxs-lookup"><span data-stu-id="513ff-120">In the list of **Properties** on the **Object Editor** window, double-click the name of the configuration setting you want to edit.</span></span> <span data-ttu-id="513ff-121">Por ejemplo, para editar la información de redireccionamiento de la dirección URL de MED-V, haga doble clic en la propiedad **UxRedirectUrls**.</span><span class="sxs-lookup"><span data-stu-id="513ff-121">For example, to edit MED-V URL redirection information, double-click the property **UxRedirectUrls**.</span></span>

    <span data-ttu-id="513ff-122">Se abrirá una ventana del **Editor de propiedades** .</span><span class="sxs-lookup"><span data-stu-id="513ff-122">A **Property Editor** window opens.</span></span>

2.  <span data-ttu-id="513ff-123">Edite el valor para actualizar la información de configuración.</span><span class="sxs-lookup"><span data-stu-id="513ff-123">Edit the value to update the configuration information.</span></span> <span data-ttu-id="513ff-124">Por ejemplo, para editar la información de redirección de la dirección URL de MED-V, agregue o quite una dirección Web de la lista.</span><span class="sxs-lookup"><span data-stu-id="513ff-124">For example, to edit MED-V URL redirection information, add or remove a web address in the list.</span></span>

3.  <span data-ttu-id="513ff-125">Guardar la configuración de propiedades actualizada.</span><span class="sxs-lookup"><span data-stu-id="513ff-125">Save the updated property settings.</span></span>

<span data-ttu-id="513ff-126">Cuando haya terminado de ver o editar la configuración de configuración de MED-V, cierre la herramienta de navegación de WMI.</span><span class="sxs-lookup"><span data-stu-id="513ff-126">After you have finished viewing or editing MED-V configuration settings, close the WMI browsing tool.</span></span>

<span data-ttu-id="513ff-127">**Importante**  En algunos casos, es necesario reiniciar el área de trabajo de MED-V para que los cambios de la configuración de MED-V surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="513ff-127">**Important** In some cases, a restart of the MED-V workspace is required for changes to MED-V configuration settings to take effect.</span></span>

 

<span data-ttu-id="513ff-128">En el código siguiente se muestra el archivo de formato de objetos administrados (MOF) que define la clase de **configuración** .</span><span class="sxs-lookup"><span data-stu-id="513ff-128">The following code shows the Managed Object Format (MOF) file that defines the **Setting** class.</span></span>

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

<span data-ttu-id="513ff-129">La clase **Setting** se hereda de la clase **ConfigValueProvider** .</span><span class="sxs-lookup"><span data-stu-id="513ff-129">The **Setting** class inherits from the **ConfigValueProvider** class.</span></span> <span data-ttu-id="513ff-130">En el código siguiente se muestra el archivo de formato de objetos administrados (MOF) que define la clase **ConfigValueProvider** .</span><span class="sxs-lookup"><span data-stu-id="513ff-130">The following code shows the Managed Object Format (MOF) file that defines the **ConfigValueProvider** class.</span></span>

``` syntax
[abstract]
class ConfigValueProvider
{
                [write] string DiagEventLogLevel;
                [write] boolean FtsAddUserToAdminGroupEnabled;
                [write] string FtsComputerNameMask;
                [write] sint32 FtsDeleteVMStateTimeout;
                [write] sint32 FtsDetachVfdTimeout;
                [write] string FtsDialogUrl;
                [write] sint32 FtsExplorerTimeout;
                [write] string FtsFailureDialogMsg;
                [write] string FtsLogFilePaths[];
                [write] sint32 FtsMaxPostponeTime;
                [write] sint32 FtsMaxRetryCount;
                [write] string FtsMode;
                [write] sint32 FtsNonInteractiveRetryTimeoutInc;
                [write] sint32 FtsNonInteractiveTimeout;
                [write] string FtsPostponeUtcDateTimeLimit;
                [write] string FtsRetryDialogMsg;
                [write] boolean FtsSetComputerNameEnabled;
                [write] boolean FtsSetJoinDomainEnabled;
                [write] boolean FtsSetMachineObjectOUEnabled;
                [write] boolean FtsSetRegionalSettingsEnabled;
                [write] boolean FtsSetUserDataEnabled;
                [write] string FtsStartDialogMsg;
                [write] sint32 FtsTaskCancelTimeout;
                [write] sint32 FtsTaskVMTurnOffTimeout;
                [write] sint32 FtsUpgradeTimeout;
                [write] boolean UxAppPublishingEnabled;
                [write] boolean UxAudioSharingEnabled;
                [write] boolean UxClipboardSharingEnabled;
                [write] boolean UxCredentialCacheEnabled;
                [write] sint32 UxDialogTimeout;
                [write] sint32 UxHideVmTimeout;
                [write] boolean UxLogonStartEnabled;
                [write] boolean UxPrinterSharingEnabled;
                [write] sint32 UxRebootAbsoluteDelayTimeout;
                [write] string UxRedirectUrls[];
                [write] boolean UxShowExit;
                [write] boolean UxSmartCardLogonEnabled;
                [write] boolean UxSmartCardSharingEnabled;
                [write] boolean UxUSBDeviceSharingEnabled;
                [write] string VmCloseAction;
                [write] sint32 VmGuestMemFromHostMem[];
                [write] sint32 VmGuestUpdateDuration;
                [write] string VmGuestUpdateTime;
                [write] sint32 VmHostMemToGuestMem[];
                [write] boolean VmHostMemToGuestMemCalcEnabled;
                [write] sint32 VmMemory;
                [write] boolean VmMultiUserEnabled;
                [write] string VmNetworkingMode;
                [write] sint32 VmTaskTimeout;
};
```

## <span data-ttu-id="513ff-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="513ff-131">Related topics</span></span>


[<span data-ttu-id="513ff-132">Administrar opciones de configuración de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="513ff-132">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="513ff-133">Administrar la configuración del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="513ff-133">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





