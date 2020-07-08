---
title: Virtualización de la experiencia del usuario de Microsoft (UE-V) 2. x
description: Virtualización de la experiencia del usuario de Microsoft (UE-V) 2. x
author: dansimp
ms.assetid: b860fed0-b846-415d-bdd6-ba60231a64be
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 04/19/2017
ms.openlocfilehash: 573b8bb2027e5c7f117a8254005a43c656f047a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10795969"
---
# Virtualización de la experiencia del usuario de Microsoft (UE-V) 2. x

>[!NOTE]
>Esta documentación es una para la versión de UE-V que se incluyó en Microsoft Desktop Optimization Pack (MDOP). Para obtener más información sobre la versión más reciente de UE-V, que se incluye en Windows 10 Enterprise, consulte Introducción [a UE-v](https://docs.microsoft.com/windows/configuration/ue-v/uev-getting-started).


Capture y centralice la configuración de la aplicación de los usuarios y la configuración del SO Windows implementando la virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0 o 2,1. Después, aplique esta configuración a los dispositivos a los que los usuarios obtienen acceso a su empresa, como equipos de escritorio, portátiles o sesiones de infraestructura de escritorio virtual (VDI).

**Con UE-V puedes...**

-   Especificar qué configuración de la aplicación y el escritorio se sincronizan

-   Proporcionar la configuración en cualquier momento y en cualquier lugar a los usuarios que trabajan en la empresa

-   Crear plantillas personalizadas para las aplicaciones de línea de negocio o de terceros

-   Recuperar la configuración tras reemplazar el hardware o actualizar, o después de reponer una máquina virtual a su estado inicial

## Componentes de UE-V 2. x


En este diagrama se muestra cómo funcionan conjuntamente los componentes de UE-V para sincronizar la configuración.

![diagrama arquitectónico de uev2](images/uev2archdiagram.gif)

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Componente</th>
<th align="left">Función</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V Agent</strong></p></td>
<td align="left"><p>Instalado en todos los equipos que necesiten sincronizar la configuración, el <strong> agente UE-V </strong> supervisa las aplicaciones registradas y el sistema operativo para los cambios de configuración y luego sincroniza esa configuración entre equipos.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Paquetes de configuración</strong></p></td>
<td align="left"><p>La configuración de la aplicación y la configuración de Windows se almacenan en <strong> paquetes de configuración </strong> creados por el agente de UE-V. Los paquetes de configuración se integran, se almacenan localmente y se copian en la ubicación de almacenamiento de configuración.</p>
<ul>
<li><p>Los valores de configuración de <strong> las aplicaciones de escritorio </strong> se almacenan cuando el usuario cierra la aplicación.</p></li>
<li><p>Los valores de <strong> configuración de Windows </strong> se almacenan cuando el usuario cierra la sesión, cuando el equipo está bloqueado o cuando el usuario se desconecta de forma remota de un equipo.</p></li>
</ul>
<p>El proveedor de sincronización determina cuándo se leen la configuración de la aplicación o del sistema operativo de los <strong> paquetes de configuración </strong> y se sincronizan.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Ubicación de almacenamiento de configuración</strong></p></td>
<td align="left"><p>Este es un recurso compartido de red estándar al que los usuarios pueden tener acceso. El agente UE-V comprueba la ubicación y crea una carpeta de sistema oculta en la que almacenar y recuperar la configuración de usuario.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Plantillas de ubicación de configuración</strong></p></td>
<td align="left"><p>UE-V usa archivos XML como plantillas de ubicación de configuración para supervisar y sincronizar la configuración de la aplicación de escritorio y la configuración del escritorio de Windows entre equipos de usuario. De forma predeterminada, se incluyen algunas plantillas de ubicación de configuración en UE-V. También puede crear, editar o validar plantillas de ubicación de configuración personalizadas si <a href="#customapps" data-raw-source="[managing settings synchronization for custom applications](#customapps)"> administra la sincronización de la configuración de las aplicaciones personalizadas </a> .</p>
<div class="alert">
<strong>Nota</strong><br/><p>Las plantillas de ubicación de configuración no son obligatorias para las aplicaciones de Windows.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Lista de aplicaciones de Windows</strong></p></td>
<td align="left"><p>La configuración de las aplicaciones de Windows se captura y se aplica dinámicamente. El desarrollador de la aplicación especifica la configuración que se sincroniza para cada aplicación. UE-V determina qué aplicaciones de Windows están habilitadas para la sincronización de configuración con una lista administrada de aplicaciones. De forma predeterminada, esta lista incluye la mayoría de las aplicaciones de Windows.</p>
<p>Puede Agregar o quitar aplicaciones en la lista de aplicaciones de Windows siguiendo los procedimientos que se indican <a href="https://technet.microsoft.com/library/dn458925.aspx" data-raw-source="[here](https://technet.microsoft.com/library/dn458925.aspx)"> aquí </a> .</p></td>
</tr>
</tbody>
</table>



### <a href="" id="customapps"></a>Administración de la sincronización de configuración de aplicaciones personalizadas

Use estos componentes de UE-V para crear y administrar plantillas personalizadas para sus aplicaciones de terceros o de línea de negocio.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>UE-V generator</strong></p></td>
<td align="left"><p>Use el <strong> generador de UE-V </strong> para crear plantillas de ubicación de configuración personalizadas que pueda distribuir a los equipos de los usuarios. El generador de UE-V también le permite editar una plantilla existente o validar una plantilla creada con otro editor XML.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Catálogo de plantillas de configuración</strong></p></td>
<td align="left"><p>El <strong> Catálogo de plantillas </strong> de configuración es una ruta de carpeta en equipos UE-V o en un recurso compartido de mensajes de servidor (SMB) que almacena las plantillas de ubicación de configuración personalizada. UE-V Agent comprueba esta ubicación una vez al día, recupera plantillas nuevas o actualizadas y actualiza su comportamiento de sincronización.</p>
<p>Si solo utiliza las plantillas de ubicación de configuración predeterminada de UE-V, no es necesario un catálogo de plantillas de configuración. Para obtener más información sobre los catálogos de implementación de la configuración, vea <a href="https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue" data-raw-source="[Configure a UE-V settings template catalog](https://technet.microsoft.com/library/dn458942.aspx#deploycatalogue)"> configurar un catálogo de plantillas de configuración de UE-V </a> .</p></td>
</tr>
</tbody>
</table>



![proceso de generación de UE-v](images/ue-vgeneratorprocess.gif)

## Configuración sincronizada de forma predeterminada


UE-V sincroniza la configuración de estas aplicaciones de forma predeterminada. Para obtener una lista completa e información más detallada, vea la [configuración que se sincroniza automáticamente en una implementación de UE-V](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings).

Aplicaciones de Microsoft Office 2013 (UE-V 2,1 SP1 y 2,1)

Aplicaciones de Microsoft Office 2010 (UE-V 2,1 SP1, 2,1 y 2,0)

Aplicaciones de Microsoft Office 2007 (UE-V 2,0 solamente)

Internet Explorer 8, 9 y 10

Internet Explorer 11 en UE-V 2,1 SP1 y 2,1

Muchas aplicaciones de Windows, como Xbox

Muchas aplicaciones de escritorio de Windows, como el Bloc de notas

Muchas opciones de configuración de Windows, como el fondo de escritorio o el papel tapiz

**Nota**  
También puede [personalizar UE-V para sincronizar la configuración](https://technet.microsoft.com/library/dn458942.aspx) de aplicaciones distintas de las sincronizadas de forma predeterminada.



## Comparar UE-V con otros productos de Microsoft


Use esta tabla para comparar UE-V para sincronizar perfiles en Windows 7, sincronizar perfiles en Windows 8 y la característica sincronizar configuración de PC de la cuenta de Microsoft.

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Característica</th>
<th align="left">Sincronizar perfiles con Windows 7</th>
<th align="left">Sincronizar perfiles con Windows 8</th>
<th align="left">Sincronizar perfiles con Windows 10</th>
<th align="left">Cuenta de Microsoft</th>
<th align="left">UE-V 2,0</th>
<th align="left">UE-V 2,1 y 2,1 SP1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Sincronizar la configuración entre varios equipos</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sincronizar la configuración entre aplicaciones físicas y virtuales</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizar la configuración de la aplicación Windows</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Administrar a través de WMI</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincronizar los cambios de configuración regularmente</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuración mínima para la configuración</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Compatible con equipos que no estén Unidos a un dominio</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Es compatible con el atributo de Active Directory de equipo principal</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Sincroniza la configuración entre la infraestructura de escritorio virtual (VDI)/Remote servicios de escritorio (RDS) y los escritorios enriquecidos</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Espacio de almacenamiento de configuración sin límites</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Elección de la configuración de la aplicación que se sincronizará</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>●</p></td>
</tr>
<tr class="even">
<td align="left"><p>Backup/restore para profesionales de ti</p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p>●</p></td>
<td align="left"><p>Parcial</p></td>
<td align="left"><p>●</p></td>
</tr>
</tbody>
</table>



## Notas de la versión de UE-V 2. x


Para obtener más información y para obtener noticias de última hora que no se han incorporado en la documentación, consulte

-   [Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1 SP1](microsoft-user-experience-virtualization--ue-v--21-sp1-release-notes.md)

-   [Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

-   [Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.0](microsoft-user-experience-virtualization--ue-v--20-release-notesuevv2.md)

## Otros recursos para este producto


-   [Introducción a UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

-   [Preparar una implementación de UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Administración de UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Solución de problemas de UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Referencia técnica de UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

### Más información

<a href="" id="mdop-techcenter-page"></a>[Página de TechCenter de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=225286) Obtenga más información sobre los recursos y la información más reciente de MDOP.

<a href="" id="mdop-information-experience"></a>[Experiencia de información en MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) Encuentre documentación, vídeos y otros recursos para tecnologías de MDOP. También puede [enviarnos comentarios](mailto:MDOPDocs@microsoft.com) u obtener información acerca de las actualizaciones en [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).














