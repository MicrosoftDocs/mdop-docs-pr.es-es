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
# Administrar la configuración de área de trabajo de MED-V mediante el uso de un WMI


Puede usar el instrumental de administración de Windows (WMI) en Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 para administrar la configuración actual.

## Para administrar la configuración del área de trabajo de MED-V con un WMI


Una herramienta de navegación de WMI le permite ver y editar la configuración en un área de trabajo de MED-V. El proveedor WMI se implementa mediante el marco de extensiones del proveedor WMI de Microsoft .NET Framework 3,5.

El proveedor WMI se implementa en el espacio de nombres **root\\microsoft\\medv** e implementa la **configuración**de clase. La **configuración** de clase contiene propiedades que corresponden a la configuración del registro del sistema que se encuentra en la clave de registro HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv.

**PRECAUCIÓN**  Las herramientas de exploración de WMI se pueden usar para eliminar o modificar clases e instancias. Eliminar o modificar determinadas clases e instancias puede provocar la pérdida de datos valiosos y hacer que MED-V funcione de manera impredecible.

 

Puede usar la herramienta de navegación WMI que prefiera para ver y editar las opciones de configuración de MED-V siguiendo estos pasos.

1.  Abre la herramienta de navegación WMI que prefieras con permisos de administrador.

2.  Conéctese al espacio de nombres **root\\microsoft\\medv**.

3.  Enumera las instancias para conectarte a la instancia que se está ejecutando. Desea conectarse a la instancia de la **configuración**de la clase.

    Se abrirá una ventana del **Editor de objetos** . La configuración de MED-V se muestra como **propiedades**.

Realice los siguientes pasos para editar una configuración de MED-V en el WMI.

1.  En la lista de **propiedades** de la ventana **Editor de objetos** , haga doble clic en el nombre de la opción de configuración que desea editar. Por ejemplo, para editar la información de redireccionamiento de la dirección URL de MED-V, haga doble clic en la propiedad **UxRedirectUrls**.

    Se abrirá una ventana del **Editor de propiedades** .

2.  Edite el valor para actualizar la información de configuración. Por ejemplo, para editar la información de redirección de la dirección URL de MED-V, agregue o quite una dirección Web de la lista.

3.  Guardar la configuración de propiedades actualizada.

Cuando haya terminado de ver o editar la configuración de configuración de MED-V, cierre la herramienta de navegación de WMI.

**Importante**  En algunos casos, es necesario reiniciar el área de trabajo de MED-V para que los cambios de la configuración de MED-V surtan efecto.

 

En el código siguiente se muestra el archivo de formato de objetos administrados (MOF) que define la clase de **configuración** .

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

La clase **Setting** se hereda de la clase **ConfigValueProvider** . En el código siguiente se muestra el archivo de formato de objetos administrados (MOF) que define la clase **ConfigValueProvider** .

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

## Temas relacionados


[Administrar opciones de configuración de área de trabajo de MED-V](managing-med-v-workspace-configuration-settings.md)

[Administrar la configuración del área de trabajo de MED-V](manage-med-v-workspace-settings.md)

 

 





