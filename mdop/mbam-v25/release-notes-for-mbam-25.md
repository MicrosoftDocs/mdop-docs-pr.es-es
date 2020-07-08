---
title: Notas de la versión de MBAM 2.5
description: Notas de la versión de MBAM 2.5
author: dansimp
ms.assetid: fcaf03e6-5e39-4771-af3c-a3cd468f3961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4bcc17d6295b14a7f3276146d5630b869b94b7f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824981"
---
# Notas de la versión de MBAM 2.5


Para buscar estas notas de la versión, presione Ctrl + F.

Lea estas notas de la versión minuciosamente antes de instalar Microsoft BitLocker Administration and Monitoring (MBAM) 2,5. Estas notas de la versión contienen información necesaria para instalar MBAM correctamente y pueden contener información que no está disponible en la documentación del producto. Si estas notas de la versión difieren de otra documentación de MBAM 2,5, considere el cambio más reciente para que sea autoritativo. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## <a href="" id="---------mbam-2-5-known-issues"></a> Problemas conocidos de MBAM 2,5


Esta sección contiene notas de la versión para MBAM 2,5.

### Explorador Web ejecutándose como administrador de forma involuntaria

Los vínculos de ayuda de la herramienta de configuración del servidor de MBAM pueden hacer que las ventanas del explorador se abran con derechos de administrador.

**Solución alternativa:** Habilite la configuración de seguridad mejorada de Internet Explorer (IESC) o cierre el explorador Web antes de navegar a otros sitios.

**Nota:**  Esto se ha corregido en MBAM 2,5 SP1.

 

### <a href="" id="-------------mbam-reports-as-noncompliant-a-client-encrypted-with-aes-256-bit-encryption-keys-and-diffuser"></a> MBAM informa de que no es compatible un cliente cifrado con las claves de cifrado y el difusor de AES 256 bits

Si un equipo tiene el cliente MBAM 2,5 instalado y se cifra mediante la norma AES 256 bits con cifrado de difusor, el cliente de MBAM se notifica como no conforme en los informes de cumplimiento de MBAM.

**Solución alternativa:** Instale el Hotfix en [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> MBAM no cifra un volumen e informa de un error Si estableces un protector de TPM + PIN en un dispositivo de tableta

Si los usuarios finales intentan establecer un protector de anclaje + PIN en un dispositivo de tableta, MBAM no se cifrará y notificará un error. Este problema se produce porque los dispositivos de tableta no tienen un teclado de entorno de preinicialización.

**Solución alternativa:** Habilite la configuración **Habilitar el uso de la autenticación de BitLocker que requiera la entrada del teclado de prearranque en tabletas** . Esta opción es una configuración de directiva de grupo de BitLocker y no está disponible en las plantillas de directiva de grupo MBAM.

### El nombre principal de usuario es necesario para todas las cuentas de servicio

Debe establecerse un nombre principal de usuario (UPN) para todas las cuentas de servicio en MBAM. Si no puede crear un UPN para una cuenta, aparecerá un mensaje de error durante el proceso de configuración para indicar que el usuario o grupo no se pudo encontrar en Active Directory.

**Solución alternativa:** Agregue el UPN a la cuenta de servicio.

### El portal de autoservicio requiere una configuración adicional si los equipos cliente no pueden obtener acceso a la red de entrega de contenido de Microsoft Ajax

Si los equipos cliente no tienen acceso a la red de entrega de contenido (CDN) de Microsoft Ajax, lo que proporciona al portal de autoservicio el acceso que necesita a determinados archivos JavaScript, debe configurar el portal de autoservicio para hacer referencia a los archivos de JavaScript desde un origen accesible. Si no configura el portal de autoservicio cuando los equipos cliente no pueden obtener acceso a la red CDN, solo se mostrará el nombre de la compañía y la cuenta con la que inició sesión. No aparece ningún mensaje de error.

**Solución alternativa:** Instale MBAM 2,5 SP1. o configurar el portal de autoservicio siguiendo estas instrucciones: [Cómo configurar el portal de autoservicio cuando los equipos cliente no pueden obtener acceso a la red de entrega de contenido de Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).

### El portal de autoservicio y el sitio web de administración y supervisión no se abren después de actualizar IIS a .NET Framework 4,5

Al actualizar Internet Information Services (IIS) a Microsoft .NET Framework 4,5, el portal de autoservicio y el sitio web de administración y supervisión no se abren.

**Solución alternativa:** Vea el artículo [mensaje de error después de instalar .NET Framework 4,0: "no se pudo cargar el tipo ' System. ServiceModel. Activation. HttpModule '](https://go.microsoft.com/fwlink/?LinkId=393568).

### Sitio web de supervisión y administración muestra el mensaje de error "no se puede encontrar el informe" cuando no se han configurado los informes

Si configura el sitio web de administración y supervisión y, a continuación, intenta ver un informe sin configurar la característica informes en primer lugar, un mensaje de error indica que no se puede encontrar el informe.

**Solución alternativa:** Configure la característica informes antes de configurar las aplicaciones Web.

### Los informes del sitio web de administración y supervisión muestran una advertencia si SSL no está configurado en SSRS

Si SQL Server Reporting Services (SSRS) no se configuró para usar la capa de sockets seguros (SSL), la dirección URL de la característica de informes se establecerá en HTTP en lugar de en HTTPS al configurar el servidor MBAM. Si abre el sitio web de administración y supervisión y selecciona un informe, aparece el siguiente mensaje de error: "solo se muestra el contenido seguro".

**Solución alternativa:** Para mostrar el informe, haga clic en **Mostrar todo el contenido**. Para corregir este problema, vaya al equipo MBAM donde está instalado SQL Server Reporting Services, ejecute el **Administrador de configuración de Reporting Services**y, a continuación, haga clic en **URL de servicio Web**. Seleccione el certificado SSL adecuado para el servidor, escriba el puerto SSL adecuado (el puerto predeterminado es 443) y, a continuación, haga clic en **aplicar**.

### Al hacer clic en "atrás" en el informe Resumen de compatibilidad de BitLocker, se puede producir un error

Si explora en profundidad un informe de Resumen de cumplimiento de BitLocker y luego hace clic en el vínculo **atrás** en el informe de SSRS, se puede producir un error.

**Solución alternativa:** Nada.

### El cifrado de espacio usado no funciona correctamente

Si cifra un equipo por primera vez después de instalar el cliente de MBAM y ha configurado una opción de directiva de grupo para implementar el cifrado solo de espacio usado, MBAM cifra todo el disco erróneamente en lugar de cifrar solo el espacio usado por el disco. Si un equipo ya está cifrado con el espacio usado solo cuando instala el cliente MBAM y ha configurado la misma configuración de directiva de grupo, MBAM informa que la unidad está cifrada correctamente y no intenta volver a cifrar la unidad.

**Solución alternativa:** Nada.

### La intensidad de cifrado no se muestra correctamente en el informe de cumplimiento de equipos con BitLocker

Si no establece una intensidad de cifrado específica en el **método elegir cifrado de unidad y** el objeto de directiva de grupo intensidad de cifrado, el informe de cumplimiento de BitLocker Computer en la topología de integración del administrador de configuración siempre muestra "desconocido" para la intensidad de cifrado, incluso si la intensidad de cifrado usa el valor predeterminado de cifrado de 128 bits. El informe muestra la intensidad de cifrado correcta si establece una intensidad de cifrado específica en el objeto de directiva de grupo.

**Solución alternativa:** Establezca siempre una intensidad de cifrado específica en el **método elegir cifrado de unidad y** el objeto de directiva de grupo intensidad de cifrado.

### La distribución del estado de cumplimiento por tipo de unidad muestra datos antiguos después de actualizar los elementos de configuración

Después de actualizar los elementos de configuración de MBAM en SystemCenter2012 ConfigurationManager, el gráfico de barras distribución del estado de cumplimiento por tipo de unidad del panel de cumplimiento de la empresa de BitLocker muestra datos que se basan en información de versiones anteriores de los elementos de configuración.

**Solución alternativa:** Nada. No se admite la modificación de los elementos de configuración MBAM y es posible que el informe no se muestre de la forma esperada.

### La configuración de seguridad mejorada puede provocar que los informes muestren un mensaje de error incorrectamente

Si la configuración de seguridad mejorada de Internet Explorer (ESC) está activada, es posible que aparezca un mensaje de error "acceso denegado" cuando intente ver informes en el servidor de MBAM. De forma predeterminada, ESC se activa para proteger el servidor disminuyendo la exposición del servidor ante posibles ataques que pueden producirse a través de contenido web y secuencias de comandos de aplicaciones.

**Solución alternativa:** Si aparece el mensaje de error "acceso denegado" al intentar ver informes en el servidor de MBAM, puede establecer un objeto de directiva de grupo o cambiar el valor predeterminado manualmente en la imagen para deshabilitar la configuración de seguridad mejorada. También puede ver los informes desde otro equipo en el que la ESC no está habilitada.

## <a href="" id="hotfixes-and-knowledge-base-articles-for-mbam-2-5-"></a>Revisiones y artículos de Knowledge base para MBAM 2,5


En esta tabla se enumeran los Hotfix y los artículos de KB para MBAM 2,5.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Artículo de KB</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2975636</p></td>
<td align="left"><p>Paquete de Hotfix 1 para administración y supervisión de Microsoft BitLocker 2,5</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975636/EN-US" data-raw-source="[support.microsoft.com/kb/2975636/EN-US](https://support.microsoft.com/kb/2975636/EN-US)">support.microsoft.com/kb/2975636/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>3015477</p></td>
<td align="left"><p>Paquete de revisiones 2 para administración y supervisión de BitLocker 2,5</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3015477" data-raw-source="[support.microsoft.com/kb/3015477](https://support.microsoft.com/kb/3015477)">support.microsoft.com/kb/3015477</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>3011022</p></td>
<td align="left"><p>Se produce un error en la instalación de MBAM 2,5 o en los informes de Configuration Manager si el nombre de la instancia SSRS contiene un guión bajo</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3011022/EN-US" data-raw-source="[support.microsoft.com/kb/3011022/EN-US](https://support.microsoft.com/kb/3011022/EN-US)">support.microsoft.com/kb/3011022/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2756402</p></td>
<td align="left"><p>El cliente de MBAM no funcionaba con el identificador de evento 4 y el código de error 0x8004100E en la descripción del evento</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Error al abrir informes de cumplimiento de los equipos o de la empresa en MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>Error de instalación de MBAM 2,0 durante el escenario de integración de Configuration Manager con SQL Server 2008</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2975472</p></td>
<td align="left"><p>Interbloqueos de SQL cuando muchos clientes de MBAM se conectan a la base de datos de recuperación de MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975472/EN-US" data-raw-source="[support.microsoft.com/kb/2975472/EN-US](https://support.microsoft.com/kb/2975472/EN-US)">support.microsoft.com/kb/2975472/EN-US</a></p></td>
</tr>
</tbody>
</table>

 


## Temas relacionados


[Acerca de MBAM 2.5](about-mbam-25.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





