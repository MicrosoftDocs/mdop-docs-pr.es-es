---
title: Quitar las funciones o software de servidor MBAM
description: Quitar las funciones o software de servidor MBAM
author: dansimp
ms.assetid: 5212ba3f-124d-43c5-824a-608e9a192e86
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e6e57c3d2a62a4e01242ade7a82a7bfa551da83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824980"
---
# Quitar las funciones o software de servidor MBAM


Estas instrucciones explican cómo quitar el software y las características de administración y supervisión de Microsoft BitLocker (MBAM). Si quita las características de MBAM Server, solo se quitan del servidor las características configuradas, no el software de servidor de MBAM. Si quita el software de servidor MBAM, se eliminarán el software y las características de MBAM Server que haya configurado en ese servidor.

**Nota:**  Para evitar la eliminación accidental de datos, MBAM no proporciona ningún mecanismo para quitar las bases de datos; debe hacerlo manualmente.

 

## <a href="" id="bkmk-removeserverfeatures"></a>Quitar las características de MBAM Server


Puede usar cualquiera de los métodos siguientes para quitar las características de MBAM Server que haya configurado:

-   Asistente para la configuración del servidor de MBAM

-   Cmdlets de Windows PowerShell

### Usar el Asistente para la configuración del servidor de MBAM para quitar características

Siga estas instrucciones para usar el Asistente para la configuración del servidor de MBAM para quitar las características de servidor de MBAM configuradas de un servidor.

**Para quitar características de MBAM mediante el asistente**

1.  En el servidor en el que desea quitar las características, seleccione **configuración del servidor de MBAM** para abrir el Asistente para la configuración.

2.  Haga clic en **quitar características**, seleccione las características que desee quitar y, a continuación, haga clic en **siguiente**. Una página de **Resumen** muestra las características que seleccionó para la eliminación.

3.  Haga clic en **quitar** para empezar a quitar las características y, a continuación, haga clic en **cerrar**.

### Usar Windows PowerShell para quitar características

Use los pasos siguientes como guía general para quitar características de MBAM Server mediante los cmdlets de Windows PowerShell.

**Para quitar características de MBAM mediante Windows PowerShell**

1.  Antes de quitar las características, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) para revisar los requisitos previos para usar Windows PowerShell.

2.  Use los siguientes cmdlets para quitar las características del servidor de MBAM:

    -   Disable-MbamReport

    -   Disable-MbamWebApplication

    -   Disable-MbamCMIntegration

    Para obtener ayuda con los cmdlets de Windows PowerShell, escriba cmdlet **Get-Help** &lt; *cmdlet* &gt; o consulte la página de [automatización de Microsoft Desktop Optimization Pack con Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) para los cmdlets de Windows PowerShell de MBAM.

## Quitar el software de servidor de MBAM


Siga estos pasos para quitar el software de servidor de MBAM y cualquier característica de MBAM Server que haya configurado en ese servidor.

**Para quitar el software de servidor de MBAM**

1.  En el servidor en el que desea desinstalar el software de servidor MBAM, ejecute **MBAMserversetup.exe** para iniciar el Asistente para la configuración de administración y supervisión de Microsoft BitLocker.

2.  Seleccione **desinstalar**y siga las indicaciones restantes para completar el proceso de desinstalación del software de servidor MBAM.



## Temas relacionados


[Implementación de MBAM 2.5](deploying-mbam-25.md)

 

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



