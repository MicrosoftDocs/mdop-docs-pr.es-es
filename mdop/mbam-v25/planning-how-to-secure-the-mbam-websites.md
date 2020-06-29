---
title: Planificación de cómo proteger los sitios web MBAM.
description: Planificación de cómo proteger los sitios web MBAM.
author: dansimp
ms.assetid: aea1d137-62cf-4da4-9989-541e0b5ad8d8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 223c9397ad7933e11051c289c3dbcab63940fbc5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825021"
---
# Planificación de cómo proteger los sitios web MBAM.


En este tema se describen los siguientes métodos para proteger el sitio web de administración y supervisión de Microsoft BitLocker (MBAM) 2,5 y el portal de autoservicio:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">¿Obligatorio u opcional?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Uso de certificados para proteger sitios web de MBAM</p></td>
<td align="left"><p>Opcional, pero muy recomendable</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registrar nombres principales de servicio (SPN) para la cuenta del grupo de aplicaciones</p></td>
<td align="left"><p>Obligatorio</p></td>
</tr>
</tbody>
</table>



Para obtener más información sobre cómo proteger la implementación de MBAM, consulte [consideraciones de seguridad de MBAM 2,5](mbam-25-security-considerations.md).

## Uso de certificados para proteger sitios web de MBAM


Le recomendamos que use un certificado para asegurar la comunicación entre:

-   Cliente de MBAM y servicios Web

-   Explorador y el sitio web de administración y supervisión, y los sitios web del portal de autoservicio

Para obtener información sobre cómo solicitar e instalar un certificado, consulte [configuración de certificados de servidor de Internet](https://technet.microsoft.com/library/cc731977.aspx).

**Nota**  
Puede configurar los sitios web y los servicios web en servidores diferentes solo si está usando Windows PowerShell. Si usa el Asistente para la configuración del servidor de MBAM para configurar los sitios web, debe configurar los sitios web y los servicios web en el mismo servidor.



Para proteger la comunicación entre los servicios web y las bases de datos, también recomendamos forzar el cifrado en SQL Server. Para obtener información sobre cómo proteger todas las conexiones a SQL Server, incluida la comunicación entre los servicios web y SQL Server, consulte [consideraciones de seguridad de MBAM 2,5](mbam-25-security-considerations.md#bkmk-secure-databases).

## Registrar SPN para la cuenta del grupo de aplicaciones


Para habilitar los servidores de MBAM para autenticar la comunicación desde el sitio web de administración y supervisión y el portal de autoservicio, debe registrar un nombre principal de servicio (SPN) para el nombre de host en la cuenta de dominio que está usando para el grupo de aplicaciones Web.

Este tema contiene instrucciones sobre cómo registrar SPN para los siguientes tipos de nombres de host:

-   Nombre de dominio completo

-   Nombre NetBIOS

-   Nombre virtual

### Antes de crear SPN para una instalación de MBAM inicial

Revise la información de la siguiente tabla antes de empezar a crear SPN.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea o elemento</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Crear una cuenta de servicio en servicios de dominio de Active Directory (AD DS).</p></td>
<td align="left"><p>La cuenta de servicio es una cuenta de usuario que se crea en AD DS para proporcionar seguridad a los sitios web de MBAM. Los sitios web de MBAM se ejecutan en un grupo de aplicaciones, cuya identidad es el nombre de la cuenta de servicio. Los SPN se registran en la cuenta del grupo de aplicaciones.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Debe usar la misma cuenta de grupo de aplicaciones para todos los servidores Web.</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Compruebe que la cuenta del grupo IIS-IUSRS o la cuenta del grupo de aplicaciones le han concedido los derechos necesarios.</p></td>
<td align="left"><p>Para comprobar esto, siga estos pasos:</p>
<ol>
<li><p>Abra el <strong> Editor de directivas de seguridad local </strong> y expanda el <strong> nodo directivas locales </strong> .</p></li>
<li><p>Seleccione el <strong> nodo asignación de derechos de usuario </strong> y, después, haga doble clic en la <strong> configuración de directiva suplantar a un cliente después de la autenticación </strong> e <strong> iniciar sesión como un trabajo por lotes </strong> en el panel derecho.</p></li>
</ol></td>
</tr>
<tr class="odd">
<td align="left"><p>Si configura los sitios web de MBAM con una cuenta de administrador de dominio, MBAM creará los SPN.</p></td>
<td align="left"><p>Si configura los sitios web de MBAM con una cuenta de administrador de dominio, siga los pasos que se indican en este tema para registrar los SPN manualmente para el tipo de nombre de host que está usando.</p></td>
</tr>
</tbody>
</table>



### Registrar SPN al usar un nombre de host de dominio completo

Si usa un nombre de host de dominio completo al configurar MBAM, debe registrar solo un SPN, como se muestra en el siguiente ejemplo.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Lo que debe hacer</th>
<th align="left">Ejemplos y más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Registre un SPN para el nombre de dominio completo.</p></td>
<td align="left"><p><code>Setspn -s http/mybitlockerrecovery.contoso.com contoso\mbamapppooluser</code></p>
<p>El nombre de host completo es <strong> mybitlockerrecovery.contoso.com </strong> y la cuenta de dominio que se usa para el grupo de aplicaciones web es <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configure la delegación restringida para el SPN que está registrando para la cuenta del grupo de aplicaciones.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Configuración de la delegación restringida</a></p>
<p>Este requisito solo se aplica a MBAM 2,5; no es necesario en MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### Registrar SPN al usar un nombre de host NetBIOS

Si usa un nombre de host NetBIOS al configurar MBAM, registre un SPN para el nombre NetBIOS y otro SPN para el nombre de dominio completo, como se muestra en los siguientes ejemplos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Lo que debe hacer</th>
<th align="left">Ejemplos y más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Registre un SPN para el nombre de host NetBIOS.</p></td>
<td align="left"><p><code>Setspn -s http/nbname01 contoso\mbamapppooluser</code></p>
<p>El nombre de host NetBIOS es <strong> nbname01 </strong> y la cuenta de dominio que se usa para el grupo de aplicaciones web es <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registre un SPN para el nombre de dominio completo.</p></td>
<td align="left"><p><code>Setspn –s http/nbname01.corp.contoso.com contoso\mbamapppooluser</code></p>
<p>El nombre de dominio completo es <strong> nbname01.contoso.com </strong> y la cuenta de dominio que se usa para el grupo de aplicaciones web es <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configure la delegación restringida para los SPN que está registrando para la cuenta del grupo de aplicaciones.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Configuración de la delegación restringida</a></p>
<p>Este requisito solo se aplica a MBAM 2,5; no es necesario en MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-regvirtualspn"></a>Registrar SPN al usar un nombre de host virtual

Si configura MBAM con un nombre de host virtual que sea un nombre de dominio completo, registre solo un SPN para el nombre de host virtual. Si el nombre de host virtual que configure no es un nombre de dominio completo, debe crear un segundo SPN que especifique el nombre de dominio completo, como se describe en los siguientes ejemplos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Lo que debe hacer</th>
<th align="left">Ejemplos y más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Si el nombre de host virtual es un nombre de dominio completo, como en este ejemplo, registre solo un SPN.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>En el ejemplo, el nombre de host virtual es <strong> mbamvirtual.contoso.com </strong> y la cuenta de dominio que se usa para el grupo de aplicaciones web es <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Registre este SPN adicional si el nombre de host virtual no es un nombre de dominio completo.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual contoso\mbamapppooluser</code></p>
<p>En el ejemplo, el nombre de host virtual es <strong> mbamvirtual </strong> y la cuenta de dominio que se usa para el grupo de aplicaciones web es <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Registre este SPN adicional si el nombre de host virtual no es un nombre de dominio completo.</p></td>
<td align="left"><p><code>Setspn -s http/mbamvirtual.contoso.com contoso\mbamapppooluser</code></p>
<p>En el ejemplo, el nombre de host virtual es <strong> mbamvirtual.contoso.com </strong> y la cuenta de dominio que se usa para el grupo de aplicaciones web es <strong> contoso\mbamapppooluser </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>En el servidor DNS (servidor de nombres de dominio), cree un "registro" para el nombre de host personalizado y señale a un servidor web o a un equilibrador de carga.</p></td>
<td align="left"><p>Consulte la sección "para configurar registros de host A DNS" en <a href="https://go.microsoft.com/fwlink/?LinkId=394337" data-raw-source="[Configure DNS Host Records](https://go.microsoft.com/fwlink/?LinkId=394337)"> configurar registros de host DNS </a> .</p>
<p>Le recomendamos que use un registro en lugar de CNAMES. Si usa CNAMES para apuntar a la dirección de dominio, también debe registrar los SPN para el nombre del servidor Web en la cuenta del grupo de aplicaciones.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configure la delegación restringida para los SPN que está registrando para la cuenta del grupo de aplicaciones.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=394335" data-raw-source="[Configuring Constrained Delegation](https://go.microsoft.com/fwlink/?LinkId=394335)">Configuración de la delegación restringida</a></p>
<p>Este requisito solo se aplica a MBAM 2,5; no es necesario en MBAM 2,5 SP1.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-registerspn"></a>Registrar un SPN al actualizar de versiones anteriores de MBAM

Complete los pasos de esta sección solo si desea:

-   Actualizar desde una versión anterior de MBAM.

-   Ejecute los sitios web en MBAM 2,5 en una configuración distribuida o con equilibrio de carga, y actualmente está ejecutando una configuración que no tiene equilibrio de carga.

Si ya ha registrado SPN en la cuenta del equipo, en lugar de en una cuenta del grupo de aplicaciones, MBAM usa los SPN existentes y no puede configurar los sitios web en una configuración distribuida o con equilibrio de carga.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Lo que debe hacer</th>
<th align="left">Ejemplos y más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Crear una cuenta de grupo de aplicaciones en los servicios de dominio de Active Directory (AD DS).</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Quitar los sitios web y servicios web actualmente instalados.</p></td>
<td align="left"><p><a href="removing-mbam-server-features-or-software.md" data-raw-source="[Removing MBAM Server Features or Software](removing-mbam-server-features-or-software.md)">Quitar las funciones o software de servidor MBAM</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Quitar SPN de la cuenta de la máquina.</p></td>
<td align="left"><p><code>Setspn –d http/mbamwebserver mbamwebserver</code></p>
<p><code>Setspn –d http/mbamwebserver.contoso.com mbamwebserver</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Registrar SPN en la cuenta del grupo de aplicaciones.</p></td>
<td align="left"><p>Siga los pasos para <a href="#bkmk-regvirtualspn" data-raw-source="[Registering SPNs when you use a virtual host name](#bkmk-regvirtualspn)"> registrar SPN cuando usa un nombre de host virtual </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Vuelva a configurar las aplicaciones web y los servicios Web.</p></td>
<td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Cómo configurar las aplicaciones web de MBAM 2.5</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Siga uno de estos procedimientos, según el método que use para la configuración:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Asistente para la configuración del servidor de MBAM</strong></p></td>
<td align="left"><p>Escriba la cuenta del grupo de aplicaciones en el <strong> campo de cuenta de dominio del grupo de aplicaciones de servicio Web </strong> .</p></td>
</tr>
<tr class="even">
<td align="left"><p><code>Enable-MbamWebApplication</code> Cmdlet de Windows PowerShell</p></td>
<td align="left"><p>Escriba la cuenta en el <code>WebServiceApplicationPoolCredential</code> parámetro.</p></td>
</tr>
</tbody>
</table>
<p> </p></td>
<td align="left"><div class="alert">
<strong>Importante</strong><br/><p>El nombre de host que escriba debe tener el mismo nombre que el nombre de host virtual para el que está creando los SPN. Además, en su granja de servidores Web, los nombres de host y las credenciales del grupo de aplicaciones deben ser los mismos en todos los servidores que esté configurando.</p>
</div>
<div>

</div>
<p>Cuando MBAM configura las aplicaciones Web, intentará registrar los SPN, pero puede hacerlo solo si tiene derechos de administrador de dominio en el servidor en el que está instalando MBAM. Si no tiene estos derechos, puede completar la configuración, pero tendrá que configurar los SPN antes o después de configurar MBAM.</p></td>
</tr>
</tbody>
</table>

## Configuración de filtrado de solicitudes obligatorias

 Para que la aplicación funcione según lo esperado, es necesario ' permitir extensiones de nombre de archivo que no se hayan puesto en la lista '.  Para ello, vaya a la ' supervisión y administración de Microsoft BitLocker '-> filtrar solicitudes: > configuración de características de edición.


## Temas relacionados


[Preparación del entorno para MBAM 2.5](preparing-your-environment-for-mbam-25.md)

[Requisitos previos de implementación de MBAM 2.5](mbam-25-deployment-prerequisites.md)





## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



