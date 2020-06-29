---
title: Cómo modificar una aplicación publicada con la configuración avanzada
description: Cómo modificar una aplicación publicada con la configuración avanzada
author: dansimp
ms.assetid: 06a79049-9ce9-490f-aad7-fd4fdf185590
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 843aebb38f54959f209e742b398e3979acac3334
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827000"
---
# Cómo modificar una aplicación publicada con la configuración avanzada


Después de agregar y configurar una aplicación publicada, se puede editar la aplicación publicada y configurar otras opciones avanzadas.

**Para editar una aplicación publicada con la configuración avanzada**

1.  En el panel **aplicaciones** , agregue y configure una aplicación publicada.

2.  Seleccione la aplicación publicada para editar.

3.  Haz clic en **Editar**.

4.  En el cuadro de diálogo **aplicación publicada** , configure los parámetros tal y como se describe en la tabla siguiente.

5.  Haga clic en **Aceptar**.

6.  En el menú **Directiva** , seleccione **confirmar**.

**Editar las propiedades de la aplicación publicada**

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
<td align="left"><p>Nombre para mostrar</p></td>
<td align="left"><p>El nombre del acceso directo en el menú Inicio del usuario&#39;s de Windows.</p>
<div class="alert">
<strong>Nota</strong><br/><p>El nombre para mostrar <strong> no distingue </strong> entre mayúsculas y minúsculas.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>Descripción del menú publicado.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Iniciar en</p></td>
<td align="left"><p>El directorio desde el que se inicia la aplicación.</p>
<div class="alert">
<strong>Nota</strong><br/><p>La ruta de acceso no necesita incluir comillas.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Línea de comandos</p></td>
<td align="left"><p>El comando con el que se ejecutará la aplicación desde el área de trabajo de MED-V.</p>
<p>La ruta de acceso completa es obligatoria, y los parámetros se pueden pasar a la aplicación de manera similar, como en cualquier otro comando de Windows.</p>
<p>En una configuración de dominio, una unidad compartida suele existir en el servidor al que se asignan todos los equipos del dominio. El directorio debe asignarse aquí, y si se trata de una carpeta que requiere autenticación de usuario, la <strong> casilla usar credenciales de MED-V para ejecutar esta aplicación </strong> debe estar activada.</p>
<p>En un área de trabajo revertida de MED-V, puede asignar una unidad de red con sintaxis MapNetworkDrive: &quot; <em> MapNetworkDrive &lt; &gt; &lt; ruta de acceso de unidad, &gt; </em> &quot; por ejemplo, &quot; <em> MapNetworkDrive t: \tux\data </em> &quot; .</p>
<p>Por ejemplo, para publicar el explorador de Windows, use la sintaxis siguiente: &quot; <em> c: &amp; quot; o &quot; c:\Windows </em> &quot; .</p>
<div class="alert">
<strong>Nota</strong><br/><p>Para tener una resolución de nombres, debe realizar una de las siguientes acciones:</p>
</div>
<div>

</div>
<ul>
<li><p>Configure el DNS en la imagen del área de trabajo base MED-V.</p></li>
<li><p>Compruebe que la resolución DNS está definida en el host y configúrela para usar el DNS de host.</p></li>
<li><p>Use el IP para definir la unidad de red.</p></li>
</ul>
<div class="alert">
<strong>Nota</strong><br/><p>Si la ruta de acceso incluye espacios, toda la ruta debe estar entre comillas.</p>
</div>
<div>

</div>
<div class="alert">
<strong>Nota</strong><br/><p>La ruta de acceso no debe terminar con una barra diagonal inversa ().</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>Agregar un acceso directo en el menú Inicio de Windows</p></td>
<td align="left"><p>Seleccione esta casilla para crear un acceso directo para la aplicación en el menú Inicio del usuario&#39;s Windows.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Iniciar esta aplicación cuando se inicie el área de trabajo</p></td>
<td align="left"><p>Active esta casilla para ejecutar la aplicación automáticamente cuando se inicia el área de trabajo de MED-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Usar las credenciales de MED-V para ejecutar esta aplicación</p></td>
<td align="left"><p>Seleccione esta casilla para autenticar las aplicaciones que solicitan un nombre de usuario y una contraseña usando las credenciales de MED-V en lugar de las credenciales establecidas para la aplicación.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Al usar SSO, la línea de comandos debe ser <strong>C:\Windows\Explorer.exe ruta de acceso a la &quot; carpeta &quot; </strong> . Cuando no se usa el SSO, la línea de comandos debe ser la ruta de acceso a la &quot; <strong> carpeta </strong> &quot; .</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Cómo configurar las aplicaciones publicadas](how-to-configure-published-applicationsmedvv2.md)









