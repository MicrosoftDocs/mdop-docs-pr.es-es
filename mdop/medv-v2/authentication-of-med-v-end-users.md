---
title: Autenticación de los usuarios finales de MED-V
description: Autenticación de los usuarios finales de MED-V
author: dansimp
ms.assetid: aaf96eb6-91d1-4f4d-9854-5fc73c7ae7ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14c1e95a94f2da76b6b6c5ebd9d4cf14dcf839a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824890"
---
# Autenticación de los usuarios finales de MED-V


La autenticación de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 usuarios finales es un problema de seguridad muy importante. En este contexto, la autenticación hace referencia a comprobar la identidad del usuario final de MED-V.

En la sección siguiente se proporciona información y orientación sobre la autenticación de usuario final en MED-V.

## Autenticación de usuario en MED-V


Normalmente, la autenticación en MED-V se produce en dos niveles: cuando un usuario accede por primera vez a MED-V y cada vez que cambian su contraseña.

En función de cómo haya configurado la configuración de MED-V para la autenticación, normalmente se le solicitará al usuario final que escriba su contraseña, ya sea la primera vez que se inicie MED-V o la primera vez que intenten abrir una aplicación publicada.

Existen varios aspectos de la autenticación de usuario final que puede controlar, entre los que se incluyen los siguientes:

Si las credenciales que escribe el usuario final se almacenan en el administrador de credenciales

En qué forma se presenta al usuario final la opción de escribir y guardar su contraseña

Según el proceso preferido de su empresa para administrar la autenticación de usuario final, puede especificar si el almacenamiento en caché de las credenciales se produce para un área de trabajo de MED-V en particular. El almacenamiento en caché de las credenciales de un usuario final es útil porque solo se le solicitan una vez para su contraseña. Si el usuario final no tiene permiso para guardar su contraseña o decide no hacerlo, cada vez que inicie una nueva sesión de MED-V, debe escribirla de nuevo. Por ejemplo, si MED-V está configurado para iniciarse cuando el usuario final inicia sesión en el host pero la autenticación está deshabilitada, el usuario final solo se le solicita una vez durante el inicio de sesión. En este caso, las credenciales son válidas hasta que el usuario final cierra la sesión en el host.

Si es necesario, puede usar el administrador de credenciales para quitar todas las credenciales de usuario final almacenadas.

De forma predeterminada, el almacenamiento de credenciales está deshabilitado, pero puede cambiar esta configuración mediante uno de los siguientes métodos:

**Mientras crea el paquete de área de trabajo MED-V**. Para obtener más información, vea [crear un paquete de área de trabajo de MED-V](create-a-med-v-workspace-package.md).

**Después de implementar el área de trabajo de MED-V**. Edite el parámetro del cmdlet MED-V UxCredentialCacheEnabled para establecer la clave del registro de servicios de Terminal Server. Para obtener más información, vea la ayuda de Windows PowerShell.

Después de la implementación del área de trabajo de MED-V, puede establecer su preferencia para la autenticación de usuarios finales modificando la Directiva de servicios de Terminal Server denominada DisablePasswordSaving. DisablePasswordSaving controla si la casilla de verificación de contraseñas se ve en la ventana del cuadro de diálogo del cliente RDP y si se muestra el símbolo del sistema de credenciales MED-V.

A continuación se encuentra la ruta de directiva para la Directiva de servicios de Terminal Server denominada DisablePasswordSaving.

**Regedit**

HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving

**Nota**  
Los cambios que realice en DisablePasswordSaving solo afectan al símbolo del sistema de RDP a una máquina virtual.



En la tabla siguiente se enumeran las diferentes maneras en las que puede configurar las opciones de almacenamiento de credenciales y los efectos de las distintas configuraciones:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Valor</th>
<th align="left">Configuración</th>
<th align="left">Resultado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>DisablePasswordSaving</p></td>
<td align="left"><p><strong>Deshabilitado</strong></p></td>
<td align="left"><p>Se presenta el símbolo del sistema MED-V y la casilla para aceptar está disponible y desactivada. Si el usuario final activa la casilla, las credenciales se almacenan en caché para usarlas posteriormente. El usuario final también tiene la ventaja de que solo se le pregunte cuando la contraseña venza.</p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>Si el usuario final no activa la casilla, se muestra el mensaje de cliente de conexión a escritorio remoto (RDC) en lugar del símbolo de MED-V y la casilla de verificación aceptar está desactivada. Si el usuario final activa la casilla, la credencial del cliente RDC se almacena para su uso posterior.</p>
<div class="alert">
<strong>Importante</strong><br/><p>RDC no valida las credenciales cuando el usuario final las especifica. Si el usuario final almacena en caché las credenciales a través del símbolo de línea RDC, hay un riesgo de que se almacenen Credenciales incorrectas. En este caso, se deben eliminar las credenciales incorrectas en el administrador de credenciales de Windows.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>DisablePasswordSaving</p></td>
<td align="left"><p><strong>Habilitado</strong></p></td>
<td align="left"><div class="alert">
<strong>Nota</strong><br/><p>Esta configuración es más segura porque no permite almacenar las credenciales de usuario final.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



De forma predeterminada, la instalación de MED-V configura una clave del registro en el invitado para suprimir el mensaje "la contraseña está a punto de expirar". El usuario final solo tiene que cambiar la contraseña en el host. Las credenciales que se actualizan en el host se pasan al invitado.

**Actúe**  
Si usa una directiva de grupo en su entorno, sabrá que puede invalidar la clave del registro, lo que provocará que las solicitudes de contraseña del invitado vuelvan a aparecer.



### Problemas de seguridad con la autenticación

Aunque el almacenamiento en caché de las credenciales del usuario final proporcione la mejor experiencia de usuario, debe tener en cuenta los riesgos implicados.

Cuando el almacenamiento en caché de credenciales está habilitado, la credencial de dominio del usuario final se almacena en un formato reversible dentro del administrador de credenciales de Windows. Como resultado, un atacante podría escribir una herramienta que se ejecute como un proceso de nivel de sistema o un proceso de usuario final y que recupere las credenciales del usuario final. Solo puede reducir este riesgo si establece DisablePasswordSaving en **Enabled**.

Esta misma preocupación se produce cuando la autenticación de MED-V está deshabilitada, pero la configuración de directiva de servicios de Terminal Server está habilitada.

## Temas relacionados


[Procedimientos recomendados de seguridad para las operaciones de MED-V](security-best-practices-for-med-v-operations.md)









