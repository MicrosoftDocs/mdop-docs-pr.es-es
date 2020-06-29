---
title: Información acerca del archivo del grupo de conexión
description: Información acerca del archivo del grupo de conexión
author: dansimp
ms.assetid: 1f4df515-f5f6-4b58-91a8-c71598cb3ea4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31ef9dc9c4465ed8f261b73518348c05ceb78d15
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814927"
---
# Información acerca del archivo del grupo de conexión


**En este tema:**

-   [Ubicación y propósito del archivo de grupo de conexión](#bkmk-cg-purpose-loc)

-   [Estructura del archivo XML del grupo de conexiones](#bkmk-define-cg-5-0sp3)

-   [Configuración de la prioridad de paquetes en un grupo de conexión](#bkmk-config-pkg-priority-incg)

-   [Configuraciones de conexión de aplicaciones virtuales compatibles](#bkmk-va-conn-configs)

## <a href="" id="bkmk-cg-purpose-loc"></a>Ubicación y propósito del archivo de grupo de conexión


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Propósito de grupo de conexión</p></td>
<td align="left"><p>Un grupo de conexión es una característica de App-V que le permite agrupar paquetes para crear un entorno virtual en el que las aplicaciones de esos paquetes puedan interactuar entre sí.</p>
<p>Ejemplo: desea usar complementos con Microsoft Office. Puede crear un paquete que contenga los complementos, crear otro paquete que contenga Office y, a continuación, agregar ambos paquetes a un grupo de conexión para que Office pueda usar esos complementos.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cómo funciona el archivo de grupo de conexión</p></td>
<td align="left"><p>Cuando se aplica un archivo de grupo de conexión de App-V 5,1, los paquetes que se enumeran en el archivo se combinan en tiempo de ejecución en un solo entorno virtual. Use el archivo de grupo de conexión de Microsoft Application Virtualization (App-V) 5,1 para configurar grupos de conexión existentes de la versión 5,1 de App-V.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Ejemplo de ruta de archivo</p></td>
<td align="left"><p>%APPDATA%\Microsoft\AppV\Client\Catalog\PackageGroups {6CCC7575-162E-4152-9407-ED411DA138F4} {4D1E16E1-8EF8-41ED-92D5-8910A8527F96}.</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-define-cg-5-0sp3"></a>Estructura del archivo XML del grupo de conexiones


**En esta sección:**

-   [Parámetros que definen el grupo de conexión](#bkmk-params-define-cg)

-   [Parámetros que definen los paquetes en el grupo de conexión](#bkmk-params-define-pkgs-incg)

-   [Archivo XML de grupo de conexión de ejemplo de App-V](#bkmk-50sp3-exp-cg-xml)

-   [Archivo XML de grupo de conexión de aplicación-V 5,0 a través de App-V 5,0 SP2](#bkmk-50thru50sp2-exp-cg-xm)

### <a href="" id="bkmk-params-define-cg"></a>Parámetros que definen el grupo de conexión

En la siguiente tabla se describen los parámetros del archivo XML que definen el grupo de conexiones en sí, no los paquetes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Nombre del esquema</p></td>
<td align="left"><p>Nombre del esquema.</p>
<p><strong>Aplicable a partir de App-V 5,0 SP3 </strong> : Si desea usar las nuevas características "paquetes opcionales" y "usar cualquier versión" que se describen en esta tabla, debe especificar el siguiente esquema en el archivo XML:</p>
<p><code>xmlns=&quot;<a href="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot" data-raw-source="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&amp;quot">https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup&quot</a>;</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>AppConnectionGroupId</p></td>
<td align="left"><p>Identificador GUID único para este grupo de conexiones. El estado del grupo de conexiones está asociado con este identificador. Especifique este identificador solo cuando cree el grupo de conexión.</p>
<p>Puede crear un nuevo GUID escribiendo: <strong>[Guid]::NewGuid()</strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>VersionId</p></td>
<td align="left"><p>Identificador GUID de versión de esta versión del grupo de conexiones.</p>
<p>Cuando actualice un grupo de conexión (por ejemplo, agregando o actualizando un paquete nuevo), debe actualizar el GUID de versión para que refleje la nueva versión.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DisplayName</p></td>
<td align="left"><p>Nombre para mostrar del grupo de conexiones.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Prioridad</p></td>
<td align="left"><p>Campo de prioridad opcional para el grupo de conexión.</p>
<p><strong>"0" </strong> - indica la prioridad más alta.</p>
<p>Si se requiere una prioridad, pero no se ha configurado, el paquete fallará porque no se puede determinar el grupo de conexión correcto.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-params-define-pkgs-incg"></a>Parámetros que definen los paquetes en el grupo de conexión

En la &lt; sección Packages &gt; del archivo XML del grupo de conexión, enumere los paquetes miembro del grupo de conexión especificando el identificador de paquete único de cada paquete y el identificador de versión, tal y como se describe en la tabla siguiente. El primer paquete de la lista tiene la prioridad más alta.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>PackageId</p></td>
<td align="left"><p>Identificador GUID único para este paquete. Este GUID no cambia cuando se publican versiones más recientes del paquete.</p></td>
</tr>
<tr class="even">
<td align="left"><p>VersionId</p></td>
<td align="left"><p>Identificador GUID único de la versión del paquete.</p>
<p><strong>Aplicable a partir de App-V 5,0 SP3 </strong> : Si especifica <strong> "*" </strong> para la versión del paquete, se insertará dinámicamente el GUID de la última versión del paquete disponible.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>IsOptional</p></td>
<td align="left"><p><strong>Aplicable a partir de App-V 5,0 SP3 </strong> : parámetro que le permite hacer un paquete opcional dentro del grupo de conexiones. Las entradas válidas son:</p>
<ul>
<li><p><strong>"true" </strong> : el paquete es opcional en el grupo de conexión</p></li>
<li><p><strong>"falso" </strong> : el paquete es obligatorio en el grupo de conexión</p></li>
</ul>
<p>Consulte <a href="how-to-use-optional-packages-in-connection-groups51.md" data-raw-source="[How to Use Optional Packages in Connection Groups](how-to-use-optional-packages-in-connection-groups51.md)"> Cómo usar paquetes opcionales en grupos de conexión </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-50sp3-exp-cg-xml"></a>Archivo XML de grupo de conexión de ejemplo de App-V

En el siguiente ejemplo de archivo XML de grupo de conexiones se muestran ejemplos de los campos de las tablas anteriores y se resaltan los elementos que son nuevos desde App-V 5,0 SP3.

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup 
  xmlns="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2014/virtualapplicationconnectiongroup"  
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"  
  DisplayName="Sample Connection Group">
  <appv:Packages>    
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="*"
      IsOptional="true"    
    />
    <appv:Package
      PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
      VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
      IsOptional="false"    
    />  
  </appv:Packages>
</appv:AppConnectionGroup>
```

### <a href="" id="bkmk-50thru50sp2-exp-cg-xm"></a>Archivo XML de grupo de conexión de aplicación-V 5,0 a través de App-V 5,0 SP2

El siguiente ejemplo de archivo XML de grupo de conexión se aplica a App-V 5,0 mediante App-V 5,0 SP2. Muestra ejemplos de los campos de la tabla anterior, pero excluye los cambios descritos anteriormente para App-V 5,0 SP3.

```XML
<?xml version="1.0" encoding="UTF-16">
<appv:AppConnectionGroup
  xmlns="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  xmlns:appv="https://schemas.microsoft.com/appv/2010/virtualapplicationconnectiongroup"
  AppConnectionGroupId="61BE9B14-D2B4-41CE-A6E3-A1B658DE7000"
  VersionId="E6B6AA57-F2A7-49C9-ADF8-F2B5B3C8A42F"
  Priority="0"
  DisplayName="Sample Connection Group">
  <appv:Packages>
    <appv:Package
      PackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"
      VersionId="C7DF4F63-5288-439C-ACEF-EF06BF401EC5"
    />
    <appv:Package
     PackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"
     VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"
   />
 </appv:Packages>
<appv:AppConnectionGroup>
```

## <a href="" id="bkmk-config-pkg-priority-incg"></a>Configuración de la prioridad de paquetes en un grupo de conexión


La prioridad del paquete se configura con el orden de la lista de paquetes. El primer paquete del documento tiene la prioridad más alta. Los paquetes siguientes de la lista tienen prioridad descendente.

Prioridad de los paquetes es la resolución de conflictos de recursos, por lo demás, inevitables durante la inicialización del entorno virtual. Por ejemplo, si dos paquetes que se abren en el mismo entorno virtual definen el mismo valor DWORD del registro, el paquete con la prioridad más alta determina el valor que se establece.

Puede usar el archivo de grupo de conexión para configurar cada grupo de conexiones con los métodos siguientes:

-   Especificar prioridades en tiempo de ejecución para grupos de conexión. Para editar la prioridad mediante la consola de administración de App-V, haga clic en el grupo de conexiones y, a continuación, haga clic en **Editar**.

    **Nota:**  La prioridad solo es necesaria si el paquete está asociado a más de un grupo de conexión.

     

-   Especifique la prioridad de los paquetes en el grupo de conexión.

El campo Priority es obligatorio cuando una aplicación virtual en ejecución se inicia desde una solicitud de aplicación nativa, por ejemplo, el explorador de Microsoft Windows. El cliente de App-V usa la prioridad para determinar qué entorno virtual de grupo de conexiones debe ejecutar la aplicación. Esta situación se produce si una aplicación virtual forma parte de varios grupos de conexión.

Si se abre una aplicación virtual con otra aplicación virtual, se usará el entorno virtual de la aplicación virtual original. El campo Priority no se usa en este caso.

**Por ejemplo:**

La aplicación virtual Microsoft Outlook se está ejecutando en el entorno virtual **XYZ**. Al abrir un documento de Microsoft Word adjunto, se abrirá una versión virtualizada de Microsoft Word en el entorno virtual **XYZ**, independientemente de los grupos de conexiones o las prioridades de tiempo de ejecución asociados con Microsoft Word virtualizado.

## <a href="" id="bkmk-va-conn-configs"></a>Configuraciones de conexión de aplicaciones virtuales compatibles


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuración</th>
<th align="left">Escenario de ejemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Ninguna. archivo exe y complemento (. dll)</p></td>
<td align="left"><ul>
<li><p>Desea distribuir Microsoft Office a todos los usuarios, pero distribuir un complemento de Microsoft Excel solo a un subconjunto de usuarios.</p></li>
<li><p>Habilitar el grupo de conexión para los usuarios adecuados.</p></li>
<li><p>Actualice cada paquete individualmente según sea necesario.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Ninguna. exe y una aplicación de middleware</p></td>
<td align="left"><ul>
<li><p>Tiene una aplicación que requiere una aplicación de middleware o varias aplicaciones que dependen de la misma versión de tiempo de ejecución de middleware.</p></li>
<li><p>Todos los equipos que requieren una o más de las aplicaciones reciben los grupos de conexión con la aplicación y el motor en tiempo de ejecución de aplicaciones middleware.</p></li>
<li><p>De manera opcional, puede combinar varias aplicaciones middleware en un único grupo de conexiones.</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Ejemplo</th>
<th align="left">Descripción del ejemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Grupo de conexión de aplicación virtual para la división financiera</p></td>
<td align="left"><ul>
<li><p>Aplicación de middleware 1</p></li>
<li><p>Aplicación de middleware 2</p></li>
<li><p>Aplicación de middleware 3</p></li>
<li><p>Tiempo de ejecución de aplicaciones middleware</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Grupo de conexión de aplicación virtual para división de RRHH</p></td>
<td align="left"><ul>
<li><p>Aplicación de middleware 5</p></li>
<li><p>Aplicación de middleware 6</p></li>
<li><p>Tiempo de ejecución de aplicaciones middleware</p></li>
</ul></td>
</tr>
</tbody>
</table>
<p> </p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Ninguna. exe y un archivo. exe</p></td>
<td align="left"><p>Tiene una aplicación que se basa en otra aplicación y desea mantener los paquetes separados en cuanto a eficacia operativa, restricciones de licencias o escalas de tiempo de implementación.</p>
<p><strong>Por ejemplo:</strong></p>
<p>Si va a implementar Microsoft Lync 2010, puede usar tres paquetes:</p>
<ul>
<li><p>Microsoft Office2010</p></li>
<li><p>Microsoft Communicator2007</p></li>
<li><p>Microsoft Lync2010</p></li>
</ul>
<p>Puede administrar la implementación con los siguientes grupos de conexión:</p>
<ul>
<li><p>Microsoft Office2010 y Microsoft Communicator2007</p></li>
<li><p>Microsoft Office2010 y Microsoft Lync2010</p></li>
</ul>
<p>Una vez completada la implementación, puede crear un nuevo paquete de Microsoft Office2010 + Microsoft Lync2010, o bien, conservarlos y mantenerlos como paquetes independientes e implementarlos con un grupo de conexión.</p></td>
</tr>
</tbody>
</table>

 






## Temas relacionados


[Administración de grupos de conexión](managing-connection-groups51.md)

 

 





