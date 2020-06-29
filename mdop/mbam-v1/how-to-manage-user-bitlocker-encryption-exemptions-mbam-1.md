---
title: Cómo administrar exenciones de cifrado de BitLocker de usuario
description: Cómo administrar exenciones de cifrado de BitLocker de usuario
author: dansimp
ms.assetid: 48d69721-504f-4524-8a04-b9ce213ac9b4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8c3d70558a65c3288174413d6c36cc9c77bc9eaa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812966"
---
# Cómo administrar exenciones de cifrado de BitLocker de usuario


La administración y supervisión de Microsoft BitLocker (MBAM) se puede usar para administrar la protección de BitLocker al eximir a los usuarios que no necesitan o quieren que sus unidades estén cifradas.

Para eximir a los usuarios de la protección de BitLocker, una organización debe crear primero una infraestructura que admita estas exenciones. La infraestructura auxiliar puede incluir un número de teléfono de contacto, una página web o una dirección de correo para solicitar la exención. Además, se deberá agregar a cualquier usuario exento a un grupo de seguridad para la Directiva de grupo creada específicamente para los usuarios excluidos. Cuando los miembros de este grupo de seguridad inician sesión en un equipo, la Directiva de grupo de usuarios muestra que el usuario está exento de la protección de BitLocker. La Directiva de usuario sobrescribe la Directiva de equipo y el equipo permanecerá exento del cifrado de BitLocker.

**Nota:**  Si el equipo ya está protegido por BitLocker, la Directiva de exención de usuarios no surte efecto.

 

En la tabla siguiente se muestra cómo se aplica la protección de BitLocker en función de la configuración de las exenciones.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Estado de usuario</th>
<th align="left">Equipo no exento</th>
<th align="left">Exención de equipo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>El usuario no está exento</strong></p></td>
<td align="left"><p>La protección de BitLocker se aplica en el equipo.</p></td>
<td align="left"><p>La protección de BitLocker no se exige en el equipo.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Exención de usuarios</strong></p></td>
<td align="left"><p>La protección de BitLocker no se exige en el equipo.</p></td>
<td align="left"><p>La protección de BitLocker no se exige en el equipo.</p></td>
</tr>
</tbody>
</table>

 

**Para eximir a un usuario del cifrado de BitLocker**

1.  Cree un grupo de seguridad ActiveDirectoryDomainServices que se usará para administrar las exenciones de usuario del cifrado de BitLocker.

2.  Cree una configuración de objeto de directiva de grupo con la plantilla de directiva de grupo MBAM. Asocie el objeto de directiva de grupo con el grupo de Active Directory que creó en el paso anterior. Para obtener más información sobre las opciones de directiva necesarias para permitir a los usuarios solicitar la exención del cifrado de BitLocker, consulte la sección configurar directivas de exención de usuarios en [planeamiento de los requisitos de la Directiva de grupo de MBAM 1,0](planning-for-mbam-10-group-policy-requirements.md).

3.  Después de crear un grupo de seguridad para los usuarios exentos de BitLocker, agregue a este grupo los nombres de los usuarios que solicitan exención. Cuando un usuario inicia sesión en un equipo controlado por BitLocker, el cliente de MBAM verificará la configuración de la Directiva de exención de usuarios y se suspenderá en función de si el usuario forma parte del grupo de seguridad de exención de BitLocker.

    **Nota:**  Los escenarios de equipos compartidos requieren consideraciones especiales sobre la exención de usuarios. Si un usuario no exento inicia sesión en un equipo compartido con un usuario exento, el equipo se puede cifrar.

     

**Para permitir a los usuarios solicitar la exención del cifrado de BitLocker**

1.  Una vez que haya configurado las directivas de exención de usuarios mediante la usingwith de la plantilla de directiva de MBAM, un usuario puede solicitar la exención de la protección de BitLocker a través del cliente de MBAM.

2.  Cuando un usuario inicia sesión en un equipo que está marcado como **compatible** en la lista de compatibilidad de hardware de MBAM, el sistema presenta al usuario una notificación que indica que el equipo se va a cifrar. El usuario puede seleccionar **solicitar exención** y posponer el cifrado seleccionando **más tarde**o seleccionar **iniciar** para aceptar el cifrado de BitLocker.

    **Nota:**  La selección de la **exención de solicitud** pospondrá la protección de BitLocker hasta el límite máximo establecido en la Directiva de exención de usuarios.

     

3.  Cuando un usuario selecciona **solicitar exención**, el usuario recibe una notificación para que se comunique con el grupo de administración de BitLocker de la organización. En función de la configuración de la directiva configurar excepciones de usuario, los usuarios disponen de uno o varios de los siguientes métodos de contacto:

    -   Número de teléfono

    -   Dirección URL de la página web

    -   Dirección de correo

    Después de enviar la solicitud, el administrador de MBAM puede decidir si es adecuado agregar el usuario al grupo de Active Directory de exención de BitLocker.

    **Nota:**  Una vez que haya expirado el límite de tiempo de la Directiva de exención de usuarios, los usuarios no verán la opción de solicitar exención a la Directiva de cifrado. En este momento, los usuarios deben ponerse en contacto con el administrador de MBAM directamente para recibir exención de la protección de BitLocker.

     

## Temas relacionados


[Administración de funciones de MBAM 1.0](administering-mbam-10-features.md)

 

 





