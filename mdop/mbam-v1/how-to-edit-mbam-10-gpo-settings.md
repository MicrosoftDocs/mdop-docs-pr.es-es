---
title: Cambiar la configuración del GPO de MBAM 1.0
description: Cambiar la configuración del GPO de MBAM 1.0
author: dansimp
ms.assetid: 03d12fbc-4302-43fc-9b38-440607d778a1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 824fbc2fe0d8f2b00c32de177733e4e327cf4d44
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824281"
---
# Cambiar la configuración del GPO de MBAM 1.0


Para implementar correctamente administración y supervisión de Microsoft BitLocker (MBAM), primero debe determinar las directivas de grupo que usará en la implementación de administración y supervisión de Microsoft BitLocker. Para obtener más información sobre las diversas directivas disponibles, consulte [requisitos de la Directiva de grupo planificación de MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md). Una vez que haya determinado las directivas que va a usar, debe modificar uno o varios objetos de directiva de grupo (GPO) que incluyan la configuración de directiva MBAM.

Los pasos siguientes describen cómo configurar la configuración de objeto de directiva de grupo (GPO) básica y recomendada para permitir que MBAM administre el cifrado de BitLocker para los equipos cliente de su organización.

**Para editar la configuración de GPO del cliente de MBAM**

1.  En un equipo que tenga instalada una plantilla de directiva de grupo de MBAM, asegúrese de que los servicios de MBAM estén habilitados.

2.  Use la consola de administración de directivas de grupo (GPMC. msc) o el producto de MDOP de administración avanzada de directivas de grupo (AGPM) para estas acciones: seleccione **configuración del equipo**, seleccione **directivas**, haga clic en **plantillas administrativas**, seleccione **componentes de Windows**y, a continuación, haga clic en **MDOP MBAM (administración de BitLocker)**.

3.  Edite la configuración del objeto de directiva de grupo que se requiere para habilitar los servicios de cliente de MBAM en los equipos cliente. Para cada directiva de la tabla que sigue, seleccione **grupo de directivas**, haga clic en la **Directiva**y, a continuación, configure la **opción**.

    Grupo de directivas

    Directiva

    Configuración

    Administración de cliente

    Configurar servicios de MBAM

    Habilitada. Configure el **extremo del servicio de hardware y recuperación de MBAM** y **Seleccione información de recuperación de BitLocker para almacenar**.

    Establezca el **extremo del servicio de cumplimiento normativo de MBAM** e introduzca la **frecuencia del informe de estado en (minutos)**.

    Permitir la comprobación de compatibilidad de hardware

    Deshabilitado. Esta directiva está habilitada de forma predeterminada, pero no es necesaria para una implementación básica de MBAM.

    Unidad de sistema operativo

    Configuración de cifrado de unidad del sistema operativo

    Habilitada. Establezca el **protector seleccionado para la unidad del sistema operativo**. Esto es necesario para guardar los datos de la unidad del sistema operativo en el servidor de recuperación de claves MBAM.

    Unidad extraíble

    Controlar el uso de BitLocker en unidades extraíbles

    Habilitada. Esto es necesario si MBAM guardará los datos de unidades extraíbles en el servidor de recuperación de claves de MBAM.

    Unidad fija

    Controlar el uso de BitLocker en unidades fijas

    Habilitada. Esto es necesario si MBAM guardará los datos del disco fijo en el servidor de recuperación de claves de MBAM.

    Establecer: **Elija cómo se pueden recuperar las unidades protegidas con BitLocker** y **permitir el agente de recuperación de datos**.



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 1.0 Group Policy Requirements](planning-for-mbam-10-group-policy-requirements.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## Temas relacionados


[Implementación de objetos de directiva de grupo de MBAM 1.0](deploying-mbam-10-group-policy-objects.md)









