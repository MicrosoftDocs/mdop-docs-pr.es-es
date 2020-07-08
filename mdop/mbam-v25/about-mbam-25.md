---
title: Acerca de MBAM 2.5
description: Acerca de MBAM 2.5
author: dansimp
ms.assetid: 1ce218ec-4d2e-4a75-8d1a-68d737a8f3c9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: d4c9ff0bc5ee3f7dc51a56cc428081a7c3783694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824211"
---
# Acerca de MBAM 2.5


Administración y supervisión de Microsoft BitLocker (MBAM) 2,5 proporciona una interfaz administrativa simplificada para el cifrado de unidad BitLocker. BitLocker ofrece una protección mejorada contra el robo de datos o la exposición de datos para equipos que se han perdido o robado. BitLocker cifra todos los datos que se almacenan en el sistema operativo Windows volúmenes y unidades de datos configurados.

## Información general de MBAM


MBAM 2,5 tiene las siguientes características:

-   Permite a los administradores automatizar el proceso de cifrado de volúmenes en los equipos cliente en toda la empresa.

-   Permite que los responsables de seguridad determinen rápidamente el estado de cumplimiento de equipos individuales o incluso de la empresa.

-   Proporciona administración de informes y hardware centralizada con Microsoft System Center Configuration Manager.

-   Reduce la carga de trabajo del Departamento de soporte técnico para ayudar a los usuarios finales con PIN de BitLocker y solicitudes de clave de recuperación.

-   Permite a los usuarios finales recuperar dispositivos cifrados de forma independiente mediante el Portal de autoservicio.

-   Permite a los responsables de seguridad auditar fácilmente el acceso para recuperar información clave.

-   Permite a los usuarios de Windows Enterprise continuar trabajando en cualquier lugar con la garantía de que sus datos de la empresa están protegidos.

MBAM exige las opciones de directiva de cifrado de BitLocker que haya establecido para su empresa, supervisa la compatibilidad de equipos cliente con esas directivas e informa del estado de cifrado de los equipos de la empresa y de los individuos. Además, MBAM le permite acceder a la información de la clave de recuperación cuando los usuarios olvidan su PIN o su contraseña, o cuando sus registros de arranque o BIOS cambian.

Es posible que los siguientes grupos estén interesados en usar MBAM para administrar BitLocker:

-   Administradores, profesionales de la seguridad de ti y responsables del cumplimiento responsables de garantizar que los datos confidenciales no se revelen sin autorización

-   Administradores responsables de la seguridad del equipo en oficinas remotas o sucursales

-   Administradores responsables de equipos cliente que ejecutan Windows

**Nota:**  BitLocker no se explica detalladamente en esta documentación de MBAM. Para obtener más información, consulte [Introducción al cifrado de unidad BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).

 

## <a href="" id="what-s-new-in-mbam-2-5"></a>Novedades de MBAM 2,5


En esta sección se describen las nuevas características de MBAM 2,5.

### Compatibilidad con Microsoft SQL Server 2014

MBAM agrega compatibilidad con Microsoft SQL Server 2014, además del mismo software que se admite en versiones anteriores de MBAM.

### <a href="" id="-------------mbam-group-policy-templates-downloaded-separately"></a> MBAM plantillas de directiva de grupo descargadas por separado

Las plantillas de directiva de grupo MBAM deben descargarse por separado de la instalación de MBAM. En versiones anteriores de MBAM, el instalador de MBAM incluía una plantilla de directiva de MBAM, que contenía los objetos de directiva de grupo (GPO) de MBAM obligatorios que definen MBAM la configuración de implementación para el cifrado de unidad BitLocker. Estos GPO se quitaron del instalador de MBAM. Ahora descarga los GPO de [Cómo obtener plantillas de la Directiva de grupo de MDOP (. admx)](https://go.microsoft.com/fwlink/p/?LinkId=393941) y copiarlas en un servidor o una estación de trabajo antes de iniciar la instalación del cliente de MBAM. Puede copiar las plantillas de directiva de grupo en cualquier servidor o estación de trabajo que ejecute una versión compatible del sistema operativo Windows Server o Windows.

**Importante**  No cambie la configuración de directiva de grupo en el nodo **cifrado de unidad BitLocker** o MBAM no funcionará correctamente. Al establecer la configuración de directiva de grupo en el nodo de **MBAM de MDOP (administración de BitLocker)** , MBAM configura automáticamente la configuración de cifrado de unidad BitLocker para usted.

 

Los archivos de plantilla que necesita copiar a un servidor o a una estación de trabajo son:

-   BitLockerManagement. ADML

-   BitLockerManagement. ADMX

-   BitLockerUserManagement. ADML

-   BitLockerUserManagement. ADMX

Copie los archivos de plantilla en la ubicación que mejor se adapte a sus necesidades. Para los archivos específicos del idioma, que se deben copiar en una carpeta específica del idioma, se necesita la consola de administración de directivas de grupo para ver los archivos.

- Para instalar los archivos de plantilla de forma local en un servidor o una estación de trabajo, copie los archivos en una de las siguientes ubicaciones.

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left">Tipo de archivo</th>
  <th align="left">Ubicación del archivo</th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p>idioma neutro (. admx)</p></td>
  <td align="left"><p><em>% SystemRoot% </em> \policyDefinitions</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>específico de idioma (. ADML)</p></td>
  <td align="left"><p><em>% SystemRoot% </em> \policyDefinitions [ <em> MUIculture </em> ] (por ejemplo, el archivo específico de idioma Inglés de Estados Unidos se almacenará en <em> % systemroot% &lt; /em &gt; policyDefinitions\en-US)</p></td>
  </tr>
  </tbody>
  </table>

     

- Para que las plantillas estén disponibles para todos los administradores de la Directiva de grupo de un dominio, copie los archivos en una de las siguientes ubicaciones en un controlador de dominio.

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <thead>
  <tr class="header">
  <th align="left">Tipo de archivo</th>
  <th align="left">Ubicación del archivo del controlador de dominio</th>
  </tr>
  </thead>
  <tbody>
  <tr class="odd">
  <td align="left"><p>Idioma neutro (. admx)</p></td>
  <td align="left"><p><em>% SystemRoot% </em> sysvol\domain\policies\PolicyDefinitions</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>Específico de idioma (. ADML)</p></td>
  <td align="left"><p><em>% SystemRoot% </em> \sysvol\domain\policies\PolicyDefinitions [ <em> MUIculture </em> ] (por ejemplo, el archivo específico del idioma Inglés de Estados Unidos se almacenará en <em> % systemroot% </em> \sysvol\domain\policies\PolicyDefinitions\en-US)</p></td>
  </tr>
  </tbody>
  </table>

     

Para obtener más información sobre los archivos de plantilla, vea [la guía paso a paso administrar archivos ADMX de directiva de grupo](https://go.microsoft.com/fwlink/?LinkId=392818).

### Capacidad de exigir directivas de cifrado en el sistema operativo y unidades de datos fijas

MBAM 2.5 le permite exigir directivas de cifrado en el sistema operativo y en las unidades de datos fijas de los equipos de su organización y limitar el número de días que los usuarios finales pueden solicitar un aplazamiento del requisito para cumplir con las directivas de cifrado de MBAM.

Para habilitar la configuración del cumplimiento de directiva de cifrado, se ha agregado una nueva configuración de directiva de grupo, denominada configuración de aplicación de directiva de cifrado, para las unidades de sistema operativo y unidades de datos fijas. Esta Directiva se describe en la tabla siguiente.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuración de directiva de grupo</th>
<th align="left">Descripción</th>
<th align="left">Nodo de directiva de grupo usado para establecer esta configuración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Configuración de la aplicación de directivas de cifrado (unidad del sistema operativo)</p></td>
<td align="left"><p>Para esta configuración, use la opción <strong> configurar el número de días del período de gracia de no conformidad para las unidades de sistema operativo </strong> para configurar un período de gracia.</p>
<p>El período de gracia especifica la cantidad de días que los usuarios finales pueden aplazar el cumplimiento de las directivas de MBAM para la unidad del sistema operativo después de que la unidad se detectó por primera vez como no compatible.</p>
<p>Una vez que vence el período de gracia configurado, los usuarios no pueden posponer la acción necesaria ni solicitar una exención de ella.</p>
<p>Si se requiere la interacción del usuario (por ejemplo, si usa el módulo de plataforma segura (TPM) + PIN o con un protector de contraseña), aparece un cuadro de diálogo y los usuarios no pueden cerrarlo hasta que proporcionen la información necesaria. Si el protector es solo TPM, el cifrado comienza inmediatamente en segundo plano sin la intervención del usuario.</p>
<p>Los usuarios no pueden solicitar exenciones mediante el Asistente de cifrado de BitLocker. En su lugar, deben ponerse en contacto con el Departamento de soporte técnico o usar cualquier proceso que su organización use para las solicitudes de exención.</p></td>
<td align="left"><p>Directivas de configuración de equipos &gt; &gt; plantillas administrativas &gt; Windows Components &gt; MDOP MBAM (administración de BitLocker) &gt; unidad del sistema operativo</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuración de la aplicación de directivas de cifrado (unidades de datos fijas)</p></td>
<td align="left"><p>Para esta configuración, use la opción <strong> configurar el número de días del período de gracia de no conformidad para las unidades fijas </strong> para configurar un período de gracia.</p>
<p>El período de gracia especifica la cantidad de días que los usuarios finales pueden aplazar el cumplimiento de las directivas de MBAM para su unidad fija después de que se detecte la unidad por primera vez como no compatible.</p>
<p>El período de gracia comienza cuando se determina que la unidad fija no es compatible. Si está usando el desbloqueo automático, la Directiva no se aplicará hasta que la unidad del sistema operativo sea compatible. Sin embargo, si no está usando el desbloqueo automático, el cifrado de la unidad de datos fija puede empezar antes de que la unidad del sistema operativo se cifre por completo.</p>
<p>Una vez que vence el período de gracia configurado, los usuarios no pueden posponer la acción necesaria ni solicitar una exención de ella. Si se requiere la interacción del usuario, aparece un cuadro de diálogo y los usuarios no pueden cerrarlo hasta que proporcionen la información necesaria.</p></td>
<td align="left"><p>Directivas de configuración de equipos &gt; &gt; plantillas administrativas &gt; componentes de Windows &gt; MDOP MBAM (administración de BitLocker) &gt; unidad fija</p></td>
</tr>
</tbody>
</table>

 

### Capacidad para proporcionar una dirección URL en el Asistente para el cifrado de unidad BitLocker para apuntar a su Directiva de seguridad

Una nueva configuración de directiva de grupo, **proporcionar la dirección URL para el vínculo de directiva de seguridad**, le permite configurar una dirección URL que se presentará a los usuarios finales como un vínculo denominado **Directiva de seguridad**de la compañía. Este vínculo aparecerá cuando MBAM pida a los usuarios que cifren un volumen.

Si habilita esta configuración de Directiva, puede configurar la dirección URL para el vínculo **Directiva de seguridad** de la empresa. Si deshabilita o no establece esta configuración de Directiva, el vínculo de la **Directiva de seguridad** de la empresa no se mostrará a los usuarios.

La nueva configuración de directiva de grupo se encuentra en el siguiente nodo GPO: directivas de **configuración del equipo** &gt; **Policies** &gt; **plantillas administrativas** de &gt; **Windows Components** &gt; **MDOP MBAM (administración de BitLocker) &gt; Administración de clientes**.

### Compatibilidad con claves de recuperación compatibles con FIPS

MBAM 2.5 admite las claves de recuperación de BitLocker estándar de procesamiento federal de información (FIPS) en dispositivos que ejecutan el sistema operativo Windows 8.1. La clave de recuperación no era compatible con FIPS en versiones anteriores de Windows. Esta mejora mejora el proceso de recuperación de unidades en organizaciones que requieren compatibilidad con FIPS porque permite a los usuarios finales usar el portal de autoservicio o el sitio web de supervisión y supervisión (servicio de asistencia) para recuperar sus unidades si olvidan su PIN o su contraseña o se bloquean sus equipos. La nueva característica de cumplimiento de FIPS no se extiende a los protectores de contraseña.

Para habilitar la compatibilidad de FIPS en su organización, debe configurar la configuración de directiva de grupo estándar federal de procesamiento de información (FIPS). Para obtener instrucciones de configuración, consulte Configuración de la [Directiva de grupo de BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).

En el caso de los equipos cliente que ejecutan los sistemas operativos Windows8 o Windows7 sin la [revisión de BitLocker instalada](https://support.microsoft.com/kb/3015477), los administradores de ti seguirán usando el protector de agentes de recuperación de datos (DRA) en entornos compatibles con FIPS. Para obtener más información sobre DRA, consulte [uso de agentes de recuperación de datos con BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).

Vea el [paquete de revisiones 2 para la administración de BitLocker y la supervisión de 2,5](https://support.microsoft.com/kb/3015477) para descargar e instalar la corrección de BitLocker para equipos con Windows 7 y Windows 8.

### Compatibilidad con implementaciones de alta disponibilidad

MBAM admite los siguientes escenarios de alta disponibilidad además de las topologías de integración estándar de dos servidores y de Configuration Manager:

-   Grupos de disponibilidad AlwaysOn de SQL Server

-   Agrupación de SQL Server

-   Equilibrio de carga de red (NLB)

-   Reflejo de SQL Server

-   Copia de seguridad del servicio de instantáneas de volumen (VSS)

Para obtener más información sobre estas características, consulte [planificación de MBAM 2,5 alta disponibilidad](planning-for-mbam-25-high-availability.md).

### <a href="" id="management-of-roles-for-administration-and-monitoring-website-changed-"></a>Administración de roles para el sitio web de supervisión y administración cambiado

En MBAM 2.5, debe crear grupos de seguridad en servicios de dominio de Active Directory (ADDS) para administrar los roles que proporcionan derechos de acceso al sitio web de administración y supervisión. Los roles permiten a los usuarios que están en grupos de seguridad específicos realizar diferentes tareas en el sitio web, como ver informes o ayudar a los usuarios finales a recuperar unidades cifradas. En versiones anteriores de MBAM, los roles se administraban mediante grupos locales.

En MBAM 2.5, el término "roles" sustituye al término "roles de administrador" que se usaba en versiones anteriores de MBAM. Además, en MBAM 2.5, la función "MBAM System Administrators" ha sido eliminada.

En la siguiente tabla se enumeran los grupos de seguridad que debe crear en AD DS. Puede usar cualquier nombre para los grupos de seguridad.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Rol</th>
<th align="left">Derechos de acceso para este rol en el sitio web de administración y supervisión</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Usuarios de MBAM Helpdesk</p></td>
<td align="left"><p>Proporciona acceso a las áreas administrar TPM y recuperación de unidades del sitio web de administración y supervisión de MBAM. Los usuarios que tienen acceso a estas áreas deben rellenar todos los campos cuando usan cualquiera de los dos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Usuarios de informes de MBAM</p></td>
<td align="left"><p>Proporciona acceso a los informes del sitio web de administración y supervisión.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MBAM los usuarios avanzados del servicio de asistencia</p></td>
<td align="left"><p>Proporciona acceso a todas las áreas del sitio web de administración y supervisión. Los usuarios de este grupo tienen que escribir solo la clave de recuperación, no el dominio del usuario final y el nombre de usuario, al ayudar a los usuarios finales a recuperar sus unidades. Si un usuario es miembro del grupo de usuarios del Departamento de soporte técnico de MBAM y del grupo de usuarios del Departamento de soporte técnico avanzado, los permisos del grupo usuarios del servicio de asistencia avanzada anularán los permisos de grupo de los usuarios de MBAM.</p></td>
</tr>
</tbody>
</table>

 

Después de crear los grupos de seguridad en ADICIONes, asigne los usuarios o grupos al grupo de seguridad adecuado para habilitar el nivel correspondiente de acceso al sitio web de administración y supervisión. Para habilitar a los usuarios con cada rol para que tengan acceso al sitio web de supervisión y supervisión, también debe especificar cada grupo de seguridad cuando configure el sitio web de administración y supervisión.

### Cmdlets de Windows PowerShell para configurar las características de MBAM Server

Los cmdlets de Windows PowerShell para MBAM 2.5 le permiten configurar y administrar las características de servidor de MBAM. Cada característica tiene un cmdlet de Windows PowerShell correspondiente que puede usar para habilitar o deshabilitar características, o para obtener información sobre la característica.

Para obtener los requisitos previos y los requisitos previos para usar Windows PowerShell, vea [configurar las características de servidor de MBAM 2,5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

**Para cargar la ayuda de MBAM 2,5 para cmdlets de Windows PowerShell después de instalar el software del servidor de MBAM**

1.  Abra Windows PowerShell o el entorno de scripting integrado de Windows PowerShell (ISE).

2.  Escriba **Update-Help-Module Microsoft. MBAM**.

La ayuda de Windows PowerShell para MBAM está disponible en los siguientes formatos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Formato de ayuda de Windows PowerShell</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>En un símbolo del sistema de Windows PowerShell, escriba <strong> </strong> &lt; <em> cmdlet Get-Help</em>&gt;</p></td>
<td align="left"><p>Para cargar los cmdlets de Windows PowerShell más recientes, siga las instrucciones de la sección anterior sobre cómo cargar la ayuda de Windows PowerShell para MBAM.</p></td>
</tr>
<tr class="even">
<td align="left"><p>En TechNet como páginas web</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393498" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393498">https://go.microsoft.com/fwlink/?LinkId=393498</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>En el centro de descarga como un archivo. docx de Word</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393497" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393497">https://go.microsoft.com/fwlink/?LinkId=393497</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>En el centro de descarga como un archivo. pdf</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=393499" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=393499">https://go.microsoft.com/fwlink/?LinkId=393499</a></p></td>
</tr>
</tbody>
</table>

 

### Compatibilidad con los pin solo ASCII y los pin mejorados y la capacidad de evitar caracteres secuenciales y repetidos

**Permitir PIN mejorados para la configuración de directiva de grupo Inicio**

La configuración de directiva de grupo, **permitir PIN mejorados para el inicio**, le permite configurar si se usan PIN de inicio mejorado con BitLocker. Los pin de inicio mejorados permiten a los usuarios introducir cualquier tecla en un teclado completo, incluidas las letras en mayúsculas y minúsculas, símbolos, números y espacios. Si habilita esta configuración de Directiva, todos los nuevos PIN de inicio de BitLocker que se establezcan serán PIN mejorados. Si deshabilita o no establece esta configuración de Directiva, no se podrán usar los pin mejorados.

No todos los equipos son compatibles con la entrada de pines mejorados en el entorno de ejecución de inicio previo (PXE). Antes de habilitar esta opción de directiva de grupo para su organización, ejecute una comprobación del sistema durante el proceso de configuración de BitLocker para asegurarse de que el BIOS del equipo admite el uso del teclado completo en PXE. Para obtener más información, consulte requisitos de la [Directiva de grupo de planificación de MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).

**Casilla de verificación requerir PIN solo ASCII**

La configuración de directiva **permitir PIN mejorados para inicio** también contiene una casilla de verificación **requerir PIN solo ASCII** . Si los equipos de su organización no admiten el uso del teclado completo en PXE, puede habilitar la opción **permitir PIN mejorados para el inicio** y, a continuación, activar la casilla de verificación **requerir PIN solo ASCII** para requerir que los pin mejorados usen solo caracteres ASCII imprimibles.

**Uso obligatorio de caracteres no secuenciales y no extensibles**

MBAM 2.5 impide que los usuarios finales creen PIN compuestos por números repetitivos (como 1111) o números secuenciales (como 1234). Si los usuarios finales intentan escribir una contraseña que contiene tres o más números secuenciales o secuenciales, el Asistente para el cifrado de unidad BitLocker muestra un mensaje de error y evita que los usuarios escriban un PIN con los caracteres prohibidos.

### Adición de certificado de DRA al informe de cumplimiento de equipos con BitLocker

Un nuevo tipo de protector, el certificado del agente de recuperación de datos (DRA), se ha agregado al informe de cumplimiento de equipos con BitLocker en el administrador de configuración. Este tipo de protector se aplica a las unidades de sistema operativo y aparece en la sección de **volúmenes del equipo** en la columna de **tipos de protector** .

### Compatibilidad con implementaciones de compatibilidad con varios bosques

MBAM 2,5 admite los siguientes tipos de implementaciones con varios bosques:

-   Bosque único con dominio único

-   Un único bosque con un solo árbol y varios dominios

-   Bosque único con varios árboles y espacios de nombres disjuntos

-   Varios bosques en una topología de bosque central

-   Varios bosques en una topología de bosque de recursos

No se admite la migración de bosques (pasando de uno a varios, de varios a uno, de un recurso a otro del bosque, etc.) o de la actualización o la degradación.

Los requisitos previos para implementar MBAM en implementaciones de varios bosques son los siguientes:

-   El bosque debe estar ejecutándose en versiones compatibles de Windows Server.

-   Se necesita una confianza bidireccional o unidireccional. Las relaciones de confianza unidireccionales requieren que el dominio del servidor confíe en el dominio del cliente. En otras palabras, el dominio del servidor se apunta al dominio del cliente.

### Compatibilidad con el cliente de MBAM para unidades de disco duro cifradas

MBAM es compatible con BitLocker en unidades de disco duro cifradas que cumplen los requisitos de especificación de TCG para Opal y las normas IEEE 1667. Cuando BitLocker está habilitado en estos dispositivos, generará claves y realizará funciones de administración en la unidad cifrada. Para obtener más información, consulta [unidad de disco duro cifrada](https://technet.microsoft.com/library/hh831627.aspx) .

## Cómo obtener tecnologías de MDOP


MBAM es parte del paquete de optimización de escritorio de Microsoft (MDOP). MDOP es parte del programa software Assurance de Microsoft. Para obtener más información sobre el programa Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).

## <a href="" id="---------mbam-2-5-release-notes"></a> Notas de la versión de MBAM 2,5


Para obtener más información y novedades de última hora que no se incluyen en esta documentación, consulte [notas de la versión de MBAM 2,5](release-notes-for-mbam-25.md).

## ¿Tiene una sugerencia para MBAM?
- Envíanos tus comentarios [aquí](https://support.microsoft.com/help/4021566/windows-10-send-feedback-to-microsoft-with-feedback-hub). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

## Temas relacionados


[Microsoft BitLocker Administration and Monitoring 2.5](index.md)

[Introducción a MBAM 2.5](getting-started-with-mbam-25.md)

 

 





