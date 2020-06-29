---
title: Comprender las opciones de cifrado de BitLocker y elementos de Cifrado de unidad BitLocker en el Panel de Control
description: Comprender las opciones de cifrado de BitLocker y elementos de Cifrado de unidad BitLocker en el Panel de Control
author: dansimp
ms.assetid: f8a01cc2-0c77-48b9-8351-8194e80b0cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 739b65680ebfdf19f006ee8f3079f7c7e602f697
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812774"
---
# Comprender las opciones de cifrado de BitLocker y elementos de Cifrado de unidad BitLocker en el Panel de Control


En este tema se describen las **Opciones de cifrado de BitLocker** y los elementos del panel de control del **cifrado de unidad BitLocker** , y se explica lo siguiente:

-   Cómo se crean estos elementos

-   Tareas que le permiten realizar

-   **Administrar BitLocker** menú contextual "hacer clic con el botón secundario", cuando está visible frente a oculto y cómo configurarlo para que esté visible de forma predeterminada

## Opciones de cifrado de BitLocker y elementos del panel de control de cifrado de unidad BitLocker


En la siguiente tabla se enumeran las tareas que puede realizar en cada elemento del panel de control y se describe cómo se crean estos elementos.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Opciones de cifrado de BitLocker (MBAM)</th>
<th align="left">Cifrado de unidad BitLocker (Windows)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Tareas que puede realizar</p></td>
<td align="left"><ul>
<li><p>Cambiar el PIN o la contraseña</p></li>
<li><p>Comprobar el estado del cifrado de una unidad</p></li>
<li><p>Abrir la consola de administración de TPM</p></li>
<li><p>Activar BitLocker</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Suspender la protección de una unidad</p></li>
<li><p>Realizar una copia de seguridad de la clave de recuperación</p></li>
<li><p>Cambiar el PIN</p></li>
<li><p>Desactivar BitLocker en una unidad</p></li>
<li><p>Activar BitLocker en una unidad</p></li>
<li><p>Abrir la consola de administración de TPM</p></li>
<li><p>Descifrar una unidad de disco (solo aparece si el cliente de MBAM no está instalado)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Cómo se crea el elemento del panel de control</p></td>
<td align="left"><p>Creado en el panel de control al instalar el cliente de MBAM. Este elemento no se puede ocultar.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Este elemento aparece además de, pero no reemplaza, el elemento predeterminado del panel de control del cifrado de unidad BitLocker.</p>
</div>
<div>

</div></td>
<td align="left"><p>Aparece de forma predeterminada en el panel de control como parte del sistema operativo Windows, pero puede ocultarlo.</p>
<p>Para ocultarlo, vea <a href="hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md" data-raw-source="[Hiding the Default BitLocker Drive Encryption Item in Control Panel](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)"> ocultar el elemento de cifrado de unidad BitLocker predeterminado en el panel de control </a> .</p></td>
</tr>
</tbody>
</table>



## <a href="" id="-manage-bitlocker--shortcut-menu"></a>Menú contextual "Administrar BitLocker"


En la siguiente tabla se describe cómo difiere el menú de acceso directo **Administrar BitLocker** en función de si el cliente MBAM está instalado. El término "menú contextual" se refiere a las opciones que aparecen al hacer clic con el botón secundario en una unidad en el explorador de Windows.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"></th>
<th align="left">Cuando está instalado MBAM cliente</th>
<th align="left">Cuando el cliente de MBAM no está instalado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Visibilidad del menú contextual</p></td>
<td align="left"><p>La opción Administrar BitLocker está oculta.</p>
<p>Para que la opción Administrar BitLocker esté visible en el menú contextual, que muestra la opción para descifrar una unidad, elimine la siguiente clave del registro:</p>
<pre class="syntax" space="preserve"><code>HKEY_CLASSES_ROOT\Drive\Shell\manage-bde \REG_SZ LegacyDisable</code></pre></td>
<td align="left"><p>La opción Administrar BitLocker aparece en el menú contextual.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Lo que pueden hacer los usuarios</p></td>
<td align="left"><p>Con el acceso directo oculto, los usuarios pueden abrir el elemento del panel de control del cifrado de unidad BitLocker, pero la opción para descifrar una unidad no está disponible.</p></td>
<td align="left"><p>Con el acceso directo visible, al seleccionar la <strong> opción Administrar BitLocker </strong> se abre el elemento panel de control del cifrado de unidad BitLocker, que muestra la opción de descifrar una unidad.</p></td>
</tr>
</tbody>
</table>




## Temas relacionados


[Administración de funciones de MBAM 2.5](administering-mbam-25-features.md)



## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





