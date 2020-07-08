---
title: Cómo configurar las acciones de script
description: Cómo configurar las acciones de script
author: dansimp
ms.assetid: 367e28f1-d8c2-4845-a01b-2fff9128ccfd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bfa264be447a0a8560e4af16ccaadc2ec1db3f6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812390"
---
# Cómo configurar las acciones de script


El editor de acciones de script permite al administrador crear acciones para realizarlas durante la configuración del área de trabajo de MED-V, así como para definir el orden en el que se realizan.

A continuación se muestra una lista de las acciones que se pueden agregar al script de configuración de dominio:

-   **Reinicie Windows**— y reinicie Windows.

-   **Unirse al dominio**: si se une a un dominio, incluya esta acción y configure el nombre de usuario, la contraseña, el nombre de dominio completo, el nombre de dominio NetBIOS y la unidad organizativa (opcional).

-   **Comprobar conectividad**: configurar un servidor para que se conecte con un recurso de red (como el servidor de dominio) y verifique que el área de trabajo de MED-V pueda conectarse a él.

-   **Línea de comandos**: configure un script en el área de trabajo de MED-V y escriba una línea de comandos que incluya la ruta de acceso de la secuencia de comandos y los argumentos de la secuencia de comandos.

-   **Cambiar nombre de equipo**: cambie el nombre del equipo de la máquina virtual según la configuración definida.

-   **Deshabilitar el inicio de sesión automático**: deshabilitar el inicio de sesión automático de Windows. Esta acción debe agregarse al final de las secuencias de comandos que agregan el equipo al dominio.

## <a href="" id="how-to-set-up-script-actions-"></a>Cómo configurar las acciones de script


**Para configurar acciones de script**

1.  En la pestaña **configuración de VM** , haga clic en editor de **scripts**.

2.  En el cuadro de diálogo **acciones de script** , haga clic en **Agregar**y, en el submenú, haga clic en las acciones que desee.

3.  Configure las acciones según se describe en las tablas siguientes.

    **Nota:** 
     **Cambiar el nombre del equipo** está configurado en la pestaña **configuración de VM** . Para obtener más información, consulte [Cómo configurar las propiedades del patrón de nombre de equipo VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

     

~~~
**Note**  
To rename a computer, Windows must be restarted. It is recommended to add a Restart Windows action following a Rename Computer action.
~~~



4. Establezca el orden de las acciones seleccionando una acción y haciendo clic en **arriba** o **abajo**.

5. Haz clic en **Aceptar**.

**Nota**  
Al ejecutar el script de dominio de unirse, para que el script funcione, el usuario que ha iniciado sesión en la máquina virtual del área de trabajo MED-V debe tener derechos de administrador local.



**Nota**  
Cuando se ejecuta el script deshabilitar el inicio de sesión automático, se recomienda deshabilitar la cuenta de invitado local que se usa para el inicio de sesión automático una vez completada la configuración inicial.



### <a href="" id="bkmk-joindomainproperties"></a>

**Unirse a propiedades de dominio**

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
<td align="left"><p>Credenciales que se deben usar al unir la máquina virtual al dominio</p></td>
<td align="left"><p>Seleccione una de las siguientes credenciales para usarla al unir la VM al dominio:</p>
<ul>
<li><p><strong>Use las credenciales de MED-V </strong> : las credenciales de usuario final.</p></li>
<li><p><strong>Use las credenciales siguientes </strong> : las credenciales especificadas; escriba un nombre de usuario y una contraseña en los campos correspondientes.</p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>Las credenciales que escriba están visibles para todos los usuarios del área de trabajo de MED-V. No se recomienda proporcionar credenciales de administrador de dominio.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Dominio al que unirse</p></td>
<td align="left"><p>Selecciona uno de los motivos siguientes:</p>
<ul>
<li><p><strong>Use el nombre de dominio que se usa para iniciar el área de trabajo </strong> : Únase al dominio introducido por el usuario final al iniciar sesión en el cliente de MED-V.</p>
<p>Para definir la asignación de NetBIOS a nombres de dominio completos, haga clic en <strong> tabla global de asignación de dominios </strong> . En la tabla de asignación de dominios global, haga clic en <strong> agregar </strong> , escriba un <strong> nombre de dominio NetBIOS </strong> y un <strong> nombre de dominio completo </strong> , y haga clic en <strong> Aceptar </strong> .</p></li>
<li><p><strong>Usar el siguiente nombre de dominio </strong> : Únase al dominio especificado; escriba un nombre de dominio y un nombre de dominio NetBIOS en los campos correspondientes.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Unidad de organización</p></td>
<td align="left"><p>Se puede especificar una unidad organizativa (OU) para unir el equipo a una unidad organizativa específica. El formato debe seguir a un nombre distintivo de Uo: OU = organización de la &lt; organización &gt; , &lt; controlador &gt; de dominio (por ejemplo, ou = QATest, DC = Il, DC = MED-V, DC = com).</p>
<div class="alert">
<strong>Advertencia</strong><br/><p>Solo se admite una OU de un solo nivel, tal y como se muestra en el ejemplo anterior.</p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-checkconnectivityproperties"></a>

**Comprobar propiedades de conectividad**

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
<td align="left"><p>Dirección IP</p></td>
<td align="left"><p>La dirección IP del servidor con el que está comprobando la conexión.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Port</p></td>
<td align="left"><p>El puerto del servidor al que está comprobando la conexión.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Tiempo de espera agotado</p></td>
<td align="left"><p>Número de segundos que se espera una respuesta antes de que se agote el tiempo de espera.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-commandlineproperties"></a>

**Propiedades de la línea de comandos**

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
<td align="left"><p>Ruta de acceso</p></td>
<td align="left"><p>La ruta de acceso de la línea de comandos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Argumentos</p></td>
<td align="left"><p>Argumentos de la línea de comandos.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Esperar salida</p></td>
<td align="left"><p>Seleccione la casilla de verificación para esperar una devolución antes de continuar con las acciones de script.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Error en el error</p></td>
<td align="left"><p>Seleccione esta casilla si la respuesta es algo menos el valor especificado.</p>
<p>Escriba el valor que indicará el comando como un éxito.</p>
<p>Valor predeterminado: <strong> 0</strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Realizar una sola vez</p></td>
<td align="left"><p>Seleccione esta casilla para ejecutar la línea de comandos solo una vez. Si se produce un error en el script o se cancela, este comando no se volverá a ejecutar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Esta línea de comandos provoca el reinicio de las ventanas en el área de trabajo.</p></td>
<td align="left"><p>Seleccione esta casilla si la línea de comandos provoca el reinicio después de la finalización.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Permitir interacción</p></td>
<td align="left"><p>Seleccione esta casilla si el comando necesitará la interacción del usuario.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Mensaje de progreso</p></td>
<td align="left"><p>Mensaje que se mostrará al usuario mientras se ejecuta el comando.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Mensaje de error</p></td>
<td align="left"><p>Mensaje que se mostrará al usuario si se produce un error en el comando.</p></td>
</tr>
</tbody>
</table>

 

Al configurar la acción de línea de comandos, se pueden usar varias variables, tal y como se define en la tabla siguiente.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parámetro</th>
<th align="left">Valor</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>%MEDVUser%</p></td>
<td align="left"><p>Un nombre de usuario autenticado.</p></td>
<td align="left"><p>Nombre de usuario autenticado MED-V. El nombre de usuario y la contraseña se pueden usar en el script de configuración de VM de dominio combinado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>%MEDVPassword%</p></td>
<td align="left"><p>Una contraseña autenticada.</p></td>
<td align="left"><p>Contraseña autenticada MED-V. El nombre de usuario y la contraseña se pueden usar en el script de configuración de VM de dominio combinado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>%MEDVDomain%</p></td>
<td align="left"><p>Dominio configurado.</p></td>
<td align="left"><p>El dominio configurado en la autenticación de MED-V. Puede usarse en el script de configuración de VM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>%DesiredMachineName%</p></td>
<td align="left"><p>Nombre del equipo.</p></td>
<td align="left"><p>El nombre de equipo único configurado en la aplicación de administración. Puede usarse en el script de configuración de VM.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Cómo configurar la configuración de máquina virtual para un área de trabajo de MED-V](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[Cómo configurar las propiedades del patrón de nombre de equipo de VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

 

 





