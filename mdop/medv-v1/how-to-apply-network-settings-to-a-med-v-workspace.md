---
title: Cómo aplicar la configuración de red en un área de trabajo de MED-V
description: Cómo aplicar la configuración de red en un área de trabajo de MED-V
author: dansimp
ms.assetid: 641f46b3-a56f-478a-823b-1d90aa1716b3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a13227518945e74be9e4b3772af97eadbce3fc4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826520"
---
# Cómo aplicar la configuración de red en un área de trabajo de MED-V


Los administradores pueden definir la configuración de red para cada área de trabajo de MED-V.

Todas las opciones de configuración de red se configuran en el módulo **Directiva** , en la pestaña **red** .

**Para aplicar la configuración de red a un área de trabajo de MED-V**

1.  Haga clic en el área de trabajo de MED-V para configurar.

2.  En el panel **red** , configure los valores como se describe en la tabla siguiente.

3.  En el menú **Directiva** , seleccione **confirmar**.

**Propiedades de red de área de trabajo MED-V**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Propiedad</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Propiedades de TCP/IP</p></td>
<td align="left"><ul>
<li><p><strong>Usar la dirección IP del host (NAT) </strong> : el área de trabajo usará NAT para compartir la IP del host para el tráfico saliente.</p></li>
<li><p><strong>Usar una dirección IP diferente a la de host (puente) </strong> : el área de trabajo de MED-V tendrá su propia dirección de red, normalmente obtenida a través de DHCP.</p></li>
</ul>
<p>Active la <strong> casilla asignar varios adaptadores al área </strong> de trabajo cuando el equipo host tenga varios adaptadores. Se recomienda usar esta configuración cuando el host se desplaza entre redes diferentes usando distintos adaptadores.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor DNS</p></td>
<td align="left"><ul>
<li><p><strong>No cambiar </strong> : la configuración de DNS establecida en la máquina virtual del área de trabajo MED-V no se cambiará.</p></li>
<li><p><strong>Usar la dirección DNS del host </strong> : la configuración DNS del área de trabajo de MED-V se sincronizará para coincidir con la configuración del host. La sincronización DNS es dinámica. Se sincroniza periódicamente con el host para que, si se cambia en el host, cambie de forma dinámica en el área de trabajo de MED-V.</p></li>
<li><p><strong>Usar direcciones DNS específicas </strong> : el área de trabajo de MED-V usará un DNS específico, según se especifique.</p>
<p>En los <strong> </strong> campos principal y <strong> secundario </strong> , escriba las direcciones DNS principales y secundarias.</p>
<p>Active la <strong> casilla de verificación anexar direcciones DNS del host </strong> para anexar el host a las direcciones DNS configuradas.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Asignar sufijos DNS</p></td>
<td align="left"><ul>
<li><p><strong>Asignar los siguientes sufijos </strong> : Seleccione esta casilla para asignar sufijos DNS específicos; en el cuadro, escriba un sufijo o varios sufijos separados por comas.</p></li>
<li><p><strong>Anexar sufijos de host </strong> : Seleccione esta casilla para anexar los sufijos de host a la dirección DNS.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Creación de un área de trabajo de MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Uso de la interfaz de usuario de la consola de administración de MED-V](using-the-med-v-management-console-user-interface.md)

 

 





