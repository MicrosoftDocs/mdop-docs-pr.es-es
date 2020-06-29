---
title: Acerca de Microsoft Application Virtualization4.6SP2
description: Acerca de Microsoft Application Virtualization4.6SP2
author: dansimp
ms.assetid: 1429e314-9c38-472b-8687-3bed6cf0015c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 16303380782a086cfd750c7a8b2f99bf4f4c8b5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820020"
---
# Acerca de Microsoft Application Virtualization4.6SP2


Microsoft Application Virtualization (App-V) 4.6 SP2 proporciona varias mejoras y nuevas características, que se describen en este tema.

**PRECAUCIÓN**  En este tema se describe cómo cambiar el registro de Windows mediante el editor del registro. Si cambia incorrectamente el registro de Windows, puede causar serios problemas que le obliguen a reinstalar Windows. Debe hacer una copia de seguridad de los archivos de registro (System. dat y User. dat) antes de cambiar el registro. Microsoft no puede garantizar que los problemas que puedan surgir al cambiar el registro se puedan resolver. Cambie el registro bajo su propia responsabilidad.

 

**Compatibilidad con Windows 8 y Windows Server 2012**

App-V 4.6 SP2 agrega compatibilidad con servicios de escritorio remoto de Windows 8 y Windows Server 2012.

**Compatibilidad con la coexistencia con el cliente de App-V 5,0**

App-V 4.6 SP2 proporciona compatibilidad para la coexistencia con el cliente de Microsoft Application Virtualization 5,0. Revise la documentación de App-V 5,0 para obtener instrucciones sobre cómo configurar el cliente de App-V 5,0 para la coexistencia con el cliente de App-V 4.6 SP2. Para obtener más información sobre App-V 5,0, vea [Application Virtualization 5](https://go.microsoft.com/fwlink/?LinkId=267599) en TechNet.

**Posibilidad de virtualizar Adobe Reader X con el modo protegido**

Puede virtualizar Adobe Reader X con la característica de modo protegido activada mediante los procedimientos siguientes. Anteriormente, tenía que deshabilitar el modo protegido para virtualizar Adobe Reader X.

Antes de iniciar el secuenciador de App-V, cree el valor de registro siguiente en HKEY \ _LOCAL \ _MACHINE \\SOFTWARE \\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p>Nombre</p></td>
<td align="left"><p>Tipo</p></td>
<td align="left"><p>Datos</p></td>
<td align="left"><p>Descripción</p></td>
</tr>
<tr class="even">
<td align="left"><p>EnableVFSPassthrough</p></td>
<td align="left"><p>DWORD</p></td>
<td align="left"><p>uno</p></td>
<td align="left"><p>Establezca este valor en <strong> 1 para </strong> iniciar Adobe Reader X en modo protegido durante la fase de inicio.</p></td>
</tr>
</tbody>
</table>

 

**Nota:**  En un equipo que ejecute un sistema operativo de 64 bits, cree el valor del registro en HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\Overrides.

 

Para cada archivo OSD de su paquete de Adobe Reader X, agregue los siguientes elementos en el &lt; elemento Policies &gt; :

`<VIRTUAL_FILE_SYSTEM_PASS_THROUGH>TRUE</VIRTUAL_FILE_SYSTEM_PASS_THROUGH>`

`<VIRTUAL_REGISTRY_PASS_THROUGH>TRUE</VIRTUAL_REGISTRY_PASS_THROUGH>`

`<ENFORCE_ACLS_ON_VREG_MODIFY>TRUE</ENFORCE_ACLS_ON_VREG_MODIFY>`

**Nuevo parámetro de línea de comandos de secuenciador**

Al crear un acelerador de paquetes (PA) a través de la GUI secuenciador, puede seleccionar un archivo RTF o TXT que proporcione instrucciones de empaquetado e implementación a los administradores que aplicarán el acelerador de paquetes. Esta funcionalidad ahora está disponible con la CLI SPRJ.

`/ACCELERATORDESCRIPTIONFILE:PathToDescriptionFile`

Especifique una ruta de acceso a un archivo RTF o TXT que proporcione instrucciones de empaquetado e implementación al crear un acelerador de paquetes.

**Los informes de errores de aplicaciones de Microsoft ya no necesitan instalarse**

Al instalar el cliente de App-V 4.6 SP2 con setup.msi, ya no necesita instalar informes de errores de aplicaciones de Microsoft (dw20shared.msi). App-V 4.6 SP2 ahora usa informe de errores de Microsoft. Para obtener más información, vea [Cómo instalar el cliente de App-V con Setup.msi](https://go.microsoft.com/fwlink/?LinkId=267237).

**Comentarios de los clientes y Resumen de revisiones**

App-V 4.6 SP2 incluye un resumen de las correcciones para resolver los problemas encontrados desde el lanzamiento de App-V 4,6 SP1. App-V 4.6 SP2 contiene las últimas revisiones hasta el Hotfix 6 de Microsoft Application Virtualization 4,6 SP1.

## En esta sección


<a href="" id="app-v-4-6-sp2-release-notes"></a>[Notas de la versión de App-V 4.6 SP2](https://go.microsoft.com/fwlink/?LinkId=267600)  
Proporciona la información más actualizada sobre problemas conocidos con App-V 4.6 SP2.

 

 





