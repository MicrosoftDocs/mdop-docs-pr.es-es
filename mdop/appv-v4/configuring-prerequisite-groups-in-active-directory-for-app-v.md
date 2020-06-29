---
title: Configurar grupos de requisitos previos en Active Directory para App-V
description: Configurar grupos de requisitos previos en Active Directory para App-V
author: dansimp
ms.assetid: 0010d534-46c0-44a3-b5c1-621b4d5e2c31
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aa1ab6393dee20203b715311d4e1dfdc4c22c679
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821861"
---
# Configurar grupos de requisitos previos en Active Directory para App-V


Antes de instalar el servidor de administración de Microsoft Application Virtualization (App-V), debe crear los siguientes objetos en Active Directory. App-V usa grupos de Active Directory para controlar el acceso a las aplicaciones y a las funciones administrativas. Usará estos grupos durante el proceso de instalación del servidor y al publicar aplicaciones.

## Configuración de grupos de requisitos previos en Active Directory para la virtualización de aplicaciones


En esta tabla se enumeran los grupos de Active Directory necesarios para instalar App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Objeto</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Unidad organizativa (OU)</p></td>
<td align="left"><p>Cree una OU en Active Directory para los grupos específicos necesarios para App-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Grupo administrativo de App-V</p></td>
<td align="left"><p>Durante la instalación de App-V Management Server, debe seleccionar un grupo de Active Directory para usarlo como grupo de administradores de App-V para controlar el acceso administrativo a la consola de administración. Cree un grupo de seguridad para los administradores de App-V y agregue a este grupo todos los usuarios que necesiten usar la consola de administración. No puede crear este grupo directamente desde el instalador de App-V Management Server.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Grupo de usuarios de App-V</p></td>
<td align="left"><p>App-V requiere que todas las cuentas de usuario que tengan acceso a las funciones de App-V sean miembros de una directiva de proveedor asociada a un único grupo para el acceso a la plataforma general. Usar un grupo existente; por ejemplo, los usuarios del dominio, si todos los usuarios tienen acceso a App-V, o crear un grupo nuevo.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Grupos de aplicaciones</p></td>
<td align="left"><p>App-V se asocia el derecho de usar una aplicación individual con un grupo de Active Directory. Cree un grupo de Active Directory para cada aplicación y asigne los usuarios a estos grupos según sea necesario para controlar el acceso de los usuarios a las aplicaciones.</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Requisitos de implementación de virtualización de aplicaciones](application-virtualization-deployment-requirements.md)

[Cómo configurar Windows Server 2008 para servidores de administración de App-V](how-to-configure-windows-server-2008-for-app-v-management-servers.md)

 

 





