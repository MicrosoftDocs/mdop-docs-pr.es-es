---
title: Edición de configuración de directiva de grupo de MBAM 2.5
description: Edición de configuración de directiva de grupo de MBAM 2.5
author: dansimp
ms.assetid: a50b6b0c-6818-4419-8447-d0520a533dba
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0f6d180cba6dc721ff7de1607d57f90184303d88
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812598"
---
# Edición de configuración de directiva de grupo de MBAM 2.5


Para implementar correctamente administración y supervisión de Microsoft BitLocker (MBAM), tiene que:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Copie las plantillas de directiva de grupo MBAM 2,5.</p></td>
<td align="left"><p><a href="copying-the-mbam-25-group-policy-templates.md" data-raw-source="[Copying the MBAM 2.5 Group Policy Templates](copying-the-mbam-25-group-policy-templates.md)">Copia de plantillas de directiva de grupo de MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Determine los objetos de directiva de grupo (GPO) que desea usar en la implementación de MBAM. Según las necesidades de su organización, es posible que tenga que configurar otras opciones de directiva de grupo.</p></td>
<td align="left"><p><a href="planning-for-mbam-25-group-policy-requirements.md" data-raw-source="[Planning for MBAM 2.5 Group Policy Requirements](planning-for-mbam-25-group-policy-requirements.md)">Planificación de requisitos de la Directiva de grupo de MBAM 2,5 </a> : contiene descripciones de los GPO</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Establezca la configuración de directiva de grupo para su organización.</p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

**Importante**  No cambie la configuración de directiva de grupo en el nodo **cifrado de unidad BitLocker** o MBAM no funcionará correctamente. Al establecer la configuración de directiva de grupo en el nodo de **MBAM de MDOP (administración de BitLocker)** , MBAM configura automáticamente la configuración de **cifrado de unidad BitLocker** para usted.

 

**Para editar la configuración de directiva de grupo del cliente de MBAM**

1.  En un equipo que tenga instaladas las plantillas de directiva de grupo MBAM, asegúrese de que los servicios de MBAM estén habilitados.

2.  Con la consola de administración de directivas de grupo (GPMC. msc) o el producto MDOP de administración avanzada de directivas de grupo de Microsoft en un equipo que tenga instaladas las plantillas de directiva de grupo MBAM, seleccione directivas de **configuración de equipo** de &gt; **Policies** &gt; **Administrative Templates** &gt; **Windows Components** &gt; **MDOP MBAM (administración de BitLocker)**.

3.  Edite la configuración de directiva de grupo que se requiere para habilitar los servicios de cliente de MBAM en los equipos cliente. Para cada directiva de la tabla siguiente, seleccione **grupo de directivas**, haga clic en la **Directiva** que desee y, a continuación, configure las opciones.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Grupo de directivas</th>
    <th align="left">Directiva</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Administración de cliente</p></td>
    <td align="left"><p>Configurar servicios de MBAM</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Unidad de sistema operativo</p></td>
    <td align="left"><p>Configuración de cifrado de unidad del sistema operativo</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Unidad extraíble</p></td>
    <td align="left"><p>Controlar el uso de BitLocker en unidades extraíbles</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Unidad fija</p></td>
    <td align="left"><p>Controlar el uso de BitLocker en unidades fijas</p></td>
    </tr>
    </tbody>
    </table>

     

## Temas relacionados


[Planificación para requisitos de directiva de grupo de MBAM 2.5](planning-for-mbam-25-group-policy-requirements.md)

[Copia de plantillas de directiva de grupo de MBAM 2.5](copying-the-mbam-25-group-policy-templates.md)

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





