---
title: Cómo configurar la configuración de máquina virtual para un área de trabajo de MED-V
description: Cómo configurar la configuración de máquina virtual para un área de trabajo de MED-V
author: dansimp
ms.assetid: 50bbf58b-842c-4b63-bb93-3783903f6c7d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0ba24f0e9aa5befeaf385acf06273a53feaae29
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827071"
---
# Cómo configurar la configuración de máquina virtual para un área de trabajo de MED-V


Todas las opciones de configuración de la configuración de la máquina virtual se configuran en el módulo de **directivas** , en la pestaña **configuración de VM** .

## Cómo configurar la configuración de la máquina virtual para un área de trabajo de MED-V persistente


**Para configurar la configuración de la máquina virtual para un área de trabajo de MED-V persistente**

1.  Haga clic en un área de trabajo de MED-V que desee configurar.

2.  En la sección **configuración de VM persistente** , configure las propiedades tal y como se describe en la tabla siguiente.

    **Nota**  
    Las propiedades de configuración de VM persistentes solo se habilitan para un área de trabajo de MED-V persistente.



3.  En el menú **Directiva** , seleccione **confirmar**.

**Propiedades de configuración de VM persistentes**

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
<td align="left"><p>Ejecutar configuración de VM</p></td>
<td align="left"><p>Seleccione esta casilla para ejecutar un script de configuración la primera vez que se ejecuta el área de trabajo de MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Editor de scripts</p></td>
<td align="left"><p>Haga clic para configurar el script de configuración. Para obtener más información, consulte <a href="how-to-set-up-script-actions.md" data-raw-source="[How to Set Up Script Actions](how-to-set-up-script-actions.md)"> Cómo configurar acciones de script </a> .</p>
<div class="alert">
<strong>Nota</strong><br/><p>Este botón solo está habilitado cuando <strong> se selecciona ejecutar script de configuración de VM </strong> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Mensaje que aparece cuando se ejecuta el script</p></td>
<td align="left"><p>Mensaje que se mostrará mientras se ejecuta el script. Si se deja en blanco, se muestra el mensaje predeterminado.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Este campo solo está habilitado cuando la <strong> secuencia de comandos ejecutar configuración de VM </strong> está activada.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Cómo configurar la configuración de la máquina virtual para un área de trabajo revertida de MED-V


**Para configurar la configuración de la máquina virtual para un área de trabajo revertida de MED-V**

1.  Haga clic en un área de trabajo revertida de MED-V para configurar.

2.  En la sección configuración de la **VM revertida** , configure las propiedades tal y como se describe en la tabla siguiente.

    **Nota**  
    Las propiedades de configuración de VM revertidas solo se habilitan para un área de trabajo de MED-V revertida.



3.  En el menú **Directiva** , seleccione **confirmar**.

**Propiedades de configuración de VM revertidas**

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
<td align="left"><p>Cambiar el nombre de la máquina virtual según el patrón de nombre del equipo</p></td>
<td align="left"><p>Seleccione esta casilla para asignar un nombre único a cada equipo con el área de trabajo MED-V, de modo que pueda diferenciar entre varios equipos con el mismo área de trabajo de MED-V.</p>
<p>Para obtener más información sobre la configuración de nombres de imagen de equipos, consulte <a href="how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md" data-raw-source="[How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)"> Cómo configurar las propiedades del patrón de nombre de equipo VM </a> .</p></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Uso de la interfaz de usuario de la consola de administración de MED-V](using-the-med-v-management-console-user-interface.md)

[Creación de un área de trabajo de MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Ejemplos de configuraciones de máquina Virtual](examples-of-virtual-machine-configurationsv2.md)









