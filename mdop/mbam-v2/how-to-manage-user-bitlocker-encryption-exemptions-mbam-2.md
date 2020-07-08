---
title: Cómo administrar exenciones de cifrado de BitLocker de usuario
description: Cómo administrar exenciones de cifrado de BitLocker de usuario
author: dansimp
ms.assetid: 1bfd9d66-6a9a-4d0e-b54a-e5a6627f5ada
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4d5530701fd208d42dc1f6774fac11ee9ca2036b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825071"
---
# Cómo administrar exenciones de cifrado de BitLocker de usuario


La administración y supervisión de Microsoft BitLocker (MBAM) se puede usar para administrar la protección de BitLocker al eximir a los usuarios si hay usuarios que no necesitan o quieren que sus unidades estén cifradas.

Para excluir a los usuarios de la protección de BitLocker, una organización tendrá que crear una infraestructura para admitir usuarios excluidos, como asignar al usuario un número de teléfono de contacto, una página web o una dirección de correo para solicitar una exención. Además, será necesario agregar un usuario exento a un grupo de seguridad para un objeto de directiva de grupo creado específicamente para los usuarios excluidos. Cuando los miembros de este grupo de seguridad inician sesión en un equipo, la configuración de directiva de grupo del usuario muestra que el usuario está exento de la protección de BitLocker. La configuración de directiva de grupo del usuario sobrescribe la Directiva de equipo, y el equipo permanecerá exento del cifrado de BitLocker.

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
<td align="left"><p>Se exige la protección de BitLocker en el equipo</p></td>
<td align="left"><p>No se exige la protección de BitLocker en el equipo</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Exención de usuarios</strong></p></td>
<td align="left"><p>No se exige la protección de BitLocker en el equipo</p></td>
<td align="left"><p>No se exige la protección de BitLocker en el equipo</p></td>
</tr>
</tbody>
</table>

 

**Para eximir a un usuario del cifrado de BitLocker**

1.  Cree un grupo de seguridad ActiveDirectoryDomainServices que se usará para administrar las exenciones de usuario de los requisitos de cifrado de BitLocker.

2.  Cree una configuración de objeto de directiva de grupo con la plantilla de directiva de grupo supervisión y administración de BitLocker de Microsoft y asóciela al grupo de Active Directory que creó en el paso anterior. La configuración de directiva para excluir a los usuarios puede encontrarse en **UserConfiguration\\Administrative Templates\\Windows COMPONENTS\\MDOP MBAM (administración de BitLocker)**.

3.  Después de crear un grupo de seguridad para los usuarios exentos de BitLocker, agregue a este grupo los nombres de los usuarios que solicitan una exención. Cuando los usuarios inicien sesión en un equipo controlado por BitLocker, el cliente de MBAM verificará la configuración de la Directiva de exención de usuarios y se suspenderá la protección en función de si el usuario forma parte del grupo de seguridad de exención de BitLocker.

    **Importante**  Los escenarios de equipos compartidos requieren una consideración especial al usar exenciones de usuario. Si un usuario no exento inicia sesión en un equipo compartido con un usuario exento, el equipo se puede cifrar.

     

**Para permitir a los usuarios solicitar una exención del cifrado de BitLocker**

1.  Si ha configurado directivas de exención de usuarios mediante la plantilla de directiva MBAM, un usuario puede solicitar una exención de la protección de BitLocker a través del cliente de MBAM.

2.  Cuando los usuarios inician sesión en un equipo que debe estar cifrado, reciben una notificación de que se va a cifrar su equipo. Pueden seleccionar **solicitar exención** y posponer el cifrado seleccionando **más tarde**, o bien seleccionar **iniciar** para aceptar el cifrado de BitLocker.

    **Nota:**  Al seleccionar **exención de solicitud** , se pospone la protección de BitLocker hasta el tiempo máximo establecido en la Directiva de exención de usuarios.

     

3.  Si los usuarios seleccionan la **solicitud de exención**, recibirán una notificación para indicarles que se pongan en contacto con el grupo de administración de BitLocker de su organización. En función de la configuración de la directiva configurar excepciones de usuario, los usuarios disponen de uno o varios de los siguientes métodos de contacto:

    -   Número de teléfono

    -   Dirección URL de la página web

    -   Dirección de correo

    Una vez recibida la solicitud de exención, el administrador de MBAM puede decidir si es adecuado agregar el usuario al grupo de Active Directory de exención de BitLocker.

    **Nota:**  Una vez que un usuario envía una solicitud de exención, el agente de MBAM notifica al usuario como "no disponible temporalmente" y, a continuación, espera un número configurable de días antes de comprobar de nuevo la conformidad del equipo. Si el administrador de MBAM rechaza la solicitud de exención, la opción de solicitud de exención está desactivada, lo que evita que el usuario pueda volver a solicitar la exención.

     

## Temas relacionados


[Administración de funciones de MBAM 2.0](administering-mbam-20-features-mbam-2.md)

 

 





