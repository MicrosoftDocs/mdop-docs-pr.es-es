---
title: Cómo administrar exenciones de cifrado de BitLocker de usuario
description: Cómo administrar exenciones de cifrado de BitLocker de usuario
author: dansimp
ms.assetid: f582ab82-5bb5-4cd3-ad7c-483240533cf9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4224a0fb6d905c2362659efe7cf05e16756f7c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826791"
---
# Cómo administrar exenciones de cifrado de BitLocker de usuario


Administración y supervisión de Microsoft BitLocker (MBAM) le permite excluir a los usuarios de los requisitos de cifrado de unidad BitLocker.

Para excluir a los usuarios de la protección de BitLocker, tiene que:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Crear una infraestructura para admitir usuarios excluidos.</p></td>
<td align="left"><p>Algunos ejemplos de esta infraestructura son proporcionar a los usuarios un número de teléfono de contacto, una página web o una dirección de correo que puedan usar para solicitar una exención.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Agregue el usuario excluido a un grupo de seguridad para un objeto de directiva de grupo que está configurado específicamente para los usuarios excluidos.</p></td>
<td align="left"><p>Cuando los miembros de este grupo de seguridad inician sesión en un equipo, la configuración de directiva de grupo del usuario exime al usuario de la protección de BitLocker. La configuración de directiva de grupo del usuario sobrescribe la Directiva de equipo, y el equipo permanecerá exento del cifrado de BitLocker.</p>
<div class="alert">
<strong>Nota</strong><br/><p>MBAM no establece la Directiva de cifrado si el equipo ya está protegido por BitLocker y el usuario está exento. Sin embargo, si otro usuario no está exento de la Directiva de cifrado inicia sesión en el equipo, tendrá lugar el cifrado.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



Los pasos siguientes describen lo que ocurre cuando los usuarios finales solicitan una exención del proceso de exención del cifrado de unidad BitLocker a través del cliente MBAM o de cualquier proceso que use su organización. Debe configurar la configuración de directiva de grupo de MBAM para permitir que los usuarios finales soliciten una exención del cifrado de unidad BitLocker.

1.  Cuando los usuarios finales inician sesión en un equipo que debe estar cifrado, reciben una notificación de que el equipo se va a cifrar. Pueden seleccionar **exención de solicitud** y posponer el cifrado seleccionando **posponer**o pueden seleccionar **iniciar cifrado** para aceptar el cifrado de BitLocker.

    **Nota**  
    Al seleccionar **exención de solicitud** , se pospone la protección de BitLocker hasta el tiempo máximo establecido en la Directiva de exención de usuarios.



2.  Si los usuarios finales seleccionan **exención de solicitud**, recibirán una notificación que les indicará que se pongan en contacto con el grupo de administración de BitLocker de la organización. En función de la configuración de la **directiva configurar excepciones de usuario** , los usuarios disponen de uno o varios de los siguientes métodos de contacto:

    -   Número de teléfono

    -   Dirección URL de la página web

    -   Dirección de correo

3.  Una vez recibida la solicitud de exención, el administrador de MBAM decide si quiere agregar el usuario al grupo servicios de dominio de Active Directory (AD DS) de exención de BitLocker.

4.  Después de que un usuario final envía una solicitud de exención, el cliente de MBAM notifica al usuario como "se ha eximido temporalmente". Después, el cliente espera un número determinado de días, que los administradores de TI han configurado, antes de volver a comprobar el cumplimiento del equipo. Si el administrador de MBAM rechaza la solicitud de exención, la opción de solicitud de exención está desactivada, lo que impide que el usuario vuelva a solicitar la exención.

Administración y supervisión de Microsoft BitLocker (MBAM) le permite excluir a los usuarios de los requisitos de cifrado de unidad BitLocker.

Para excluir a los usuarios de la protección de BitLocker, tiene que:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Crear una infraestructura para admitir usuarios excluidos.</p></td>
<td align="left"><p>Algunos ejemplos de esta infraestructura son proporcionar a los usuarios un número de teléfono de contacto, una página web o una dirección de correo que puedan usar para solicitar una exención.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Agregue el usuario excluido a un grupo de seguridad para un objeto de directiva de grupo que está configurado específicamente para los usuarios excluidos.</p></td>
<td align="left"><p>Cuando los miembros de este grupo de seguridad inician sesión en un equipo, la configuración de directiva de grupo del usuario exime al usuario de la protección de BitLocker. La configuración de directiva de grupo del usuario sobrescribe la Directiva de equipo, y el equipo permanecerá exento del cifrado de BitLocker.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Si el equipo ya está protegido por BitLocker, la Directiva de exención de usuarios no surte efecto. Además, si otro usuario inicia sesión en un equipo que no está exento de la Directiva de cifrado, tendrá lugar el cifrado.</p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



Los pasos siguientes describen lo que ocurre cuando los usuarios finales solicitan una exención del proceso de exención del cifrado de unidad BitLocker a través del cliente MBAM o de cualquier proceso que use su organización. Debe configurar la configuración de directiva de grupo de MBAM para permitir que los usuarios finales soliciten una exención del cifrado de unidad BitLocker.

1.  Cuando los usuarios finales inician sesión en un equipo que debe estar cifrado, reciben una notificación de que el equipo se va a cifrar. Pueden seleccionar **exención de solicitud** y posponer el cifrado seleccionando **posponer**o pueden seleccionar **iniciar cifrado** para aceptar el cifrado de BitLocker.

    **Nota**  
    Al seleccionar **exención de solicitud** , se pospone la protección de BitLocker hasta el tiempo máximo establecido en la Directiva de exención de usuarios.



2.  Si los usuarios finales seleccionan **exención de solicitud**, recibirán una notificación que les indicará que se pongan en contacto con el grupo de administración de BitLocker de la organización. En función de la configuración de la **directiva configurar excepciones de usuario** , los usuarios disponen de uno o varios de los siguientes métodos de contacto:

    -   Número de teléfono

    -   Dirección URL de la página web

    -   Dirección de correo

3.  Una vez recibida la solicitud de exención, el administrador de MBAM decide si quiere agregar el usuario al grupo servicios de dominio de Active Directory (AD DS) de exención de BitLocker.

4.  Después de que un usuario final envía una solicitud de exención, el cliente de MBAM notifica al usuario como "se ha eximido temporalmente". Después, el cliente espera un número determinado de días, que los administradores de TI han configurado, antes de volver a comprobar el cumplimiento del equipo. Si el administrador de MBAM rechaza la solicitud de exención, la opción de solicitud de exención está desactivada, lo que impide que el usuario vuelva a solicitar la exención.

**Para eximir a un usuario del cifrado de unidad BitLocker**

1.  Cree un grupo de seguridad de AD DS que se usará para administrar las exenciones de usuario de los requisitos de cifrado de BitLocker.

2.  Crear un objeto de directiva de grupo mediante las plantillas de directiva de Grupo administración y supervisión de BitLocker de Microsoft.

3.  Asocie el objeto de directiva de grupo con el grupo de AD DS que creó en el paso anterior. La configuración de directiva para excluir a los usuarios se encuentra en: **UserConfiguration** &gt; **Administrative templates** &gt; **Windows Components** &gt; **MDOP MBAM (administración de BitLocker)**.

4.  Para el grupo de seguridad que ha creado para usuarios exentos de BitLocker, agregue los nombres de los usuarios que solicitan una exención.

    Cuando un usuario inicia sesión en un equipo controlado por BitLocker, el cliente de MBAM comprueba la configuración de la Directiva de exención de usuarios. Si el equipo ya está cifrado, la protección de BitLocker no se suspende. Si el equipo no está cifrado, MBAM no le pide al usuario que lo cifre.

    **Importante**  
    Los escenarios de equipos compartidos requieren una consideración especial cuando se usan exenciones de usuario de BitLocker. Si un usuario no exento inicia sesión en un equipo que está compartido con un usuario exento, el equipo puede estar cifrado.




## Temas relacionados


[Administración de funciones de MBAM 2.5](administering-mbam-25-features.md)

[Planificación para requisitos de directiva de grupo de MBAM 2.5](planning-for-mbam-25-group-policy-requirements.md)




## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




