---
title: Cómo editar la configuración del GPO de MBAM 2.0
description: Cómo editar la configuración del GPO de MBAM 2.0
author: dansimp
ms.assetid: f5ffa93d-b4d2-4317-8a1c-7d2be0264fe3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aaf7c7aab4baba66513edbfa2489fbe53c97dda8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824090"
---
# Cómo editar la configuración del GPO de MBAM 2.0


Para implementar correctamente administración y supervisión de Microsoft BitLocker (MBAM), primero tiene que determinar las directivas de grupo que usará en la implementación de administración y supervisión de Microsoft BitLocker. Consulte [planificación de requisitos de la Directiva de grupo de MBAM 2,0](planning-for-mbam-20-group-policy-requirements-mbam-2.md) para obtener más información sobre las diferentes directivas disponibles. Una vez que haya determinado las directivas que va a usar, debe modificar uno o varios objetos de directiva de grupo (GPO) que incluyan la configuración de la Directiva para MBAM.

Puede usar los siguientes pasos para configurar la configuración de GPO recomendada básica para habilitar MBAM para administrar el cifrado de BitLocker para los equipos cliente de su organización.

**Para editar la configuración de GPO del cliente de MBAM**

1.  En un equipo que tenga instalada una plantilla de directiva de grupo de MBAM, asegúrese de que los servicios de MBAM estén habilitados.

2.  Con la consola de administración de directivas de grupo (GPMC. msc) o el producto MDOP de administración avanzada de directivas de grupo (AGPM) en un equipo con la plantilla de directiva de grupo MBAM instalada, seleccione **configuración del equipo**, elija **directivas**, haga clic en **plantillas administrativas**, seleccione **componentes de Windows**y, a continuación, haga clic en **MDOP MBAM (administración de BitLocker)**.

3.  Edite la configuración del objeto de directiva de grupo que se requiere para habilitar los servicios de cliente de MBAM en los equipos cliente. Para cada directiva de la tabla que sigue, seleccione **grupo de directivas**, haga clic en la **Directiva**y, a continuación, configure la **opción**:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Grupo de directivas</th>
    <th align="left">Directiva</th>
    <th align="left">Configuración</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Administración de cliente</p></td>
    <td align="left"><p>Configurar servicios de MBAM</p></td>
    <td align="left"><p>Habilitada. Configure el <strong> extremo del servicio de hardware y recuperación de MBAM </strong> y <strong> Seleccione información de recuperación de BitLocker para almacenar </strong> . Establezca el <strong> extremo del servicio de cumplimiento normativo </strong> de MBAM e introduzca la frecuencia del informe de estado en (minutos).</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Unidad de sistema operativo</p></td>
    <td align="left"><p>Configuración de cifrado de unidad del sistema operativo</p></td>
    <td align="left"><p>Habilitada. Establezca el <strong> protector seleccionado para la unidad del sistema operativo </strong> . Necesario para guardar los datos de la unidad del sistema operativo en el servidor de recuperación de MBAMKey.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Unidad extraíble</p></td>
    <td align="left"><p>Controlar el uso de BitLocker en unidades extraíbles</p></td>
    <td align="left"><p>Habilitada. Necesario si MBAM guardará los datos de unidades extraíbles en el servidor de recuperación de claves de MBAM.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Unidad fija</p></td>
    <td align="left"><p>Controlar el uso de BitLocker en unidades fijas</p></td>
    <td align="left"><p>Habilitada. Necesario si MBAM guardará los datos del disco fijo en el servidor de recuperación de claves de MBAM.</p>
    <p>Establecer <strong> : elija cómo se pueden recuperar las unidades protegidas con BitLocker </strong> y <strong> permitir el agente de recuperación de datos </strong> .</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Important**  
Depending on the policies that your organization decides to deploy, you may have to configure additional policies. See [Planning for MBAM 2.0 Group Policy Requirements](planning-for-mbam-20-group-policy-requirements-mbam-2.md) for Group Policy configuration details for all of the available MBAM GPO policy options.
~~~



## Temas relacionados


[Implementación de objetos de directiva de grupo de MBAM 2.0](deploying-mbam-20-group-policy-objects-mbam-2.md)









