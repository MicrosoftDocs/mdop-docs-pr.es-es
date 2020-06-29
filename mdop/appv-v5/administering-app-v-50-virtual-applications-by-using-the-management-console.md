---
title: Administrar aplicaciones virtuales de App-V 5.0 con la consola de administración
description: Administrar aplicaciones virtuales de App-V 5.0 con la consola de administración
author: dansimp
ms.assetid: e9280dbd-782b-493a-b495-daab25247795
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 10/03/2016
ms.openlocfilehash: 7a71f7c0fd82f8ef9d1efd5b978591b6838a648a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814870"
---
# Administrar aplicaciones virtuales de App-V 5.0 con la consola de administración


Use el servidor de administración de Microsoft Application Virtualization (App-V) 5,0 para administrar paquetes, grupos de conexión y acceso al paquete en su entorno. El servidor publica los iconos de la aplicación, los accesos directos y las asociaciones de tipos de archivo en los equipos autorizados que ejecutan el cliente de App-V 5,0. Uno o varios servidores de administración suelen compartir un almacén de datos común para la información de configuración y del paquete.

El servidor de administración usa grupos de servicios de dominio de Active Directory (AD DS) para administrar la autorización del usuario y tiene instalado SQL Server para administrar la base de datos y el almacén de datos.

Debido a que los servidores de administración transmiten las aplicaciones a los usuarios finales a petición, estos servidores son ideales para las configuraciones del sistema que tienen LAN fiables de alto ancho de banda. El servidor de administración consta de los siguientes componentes:

-   Servidor de administración: Use el servidor de administración para administrar paquetes y grupos de conexión.

-   Publishing Server: Use el servidor de publicación para implementar paquetes en equipos que ejecuten el cliente de App-V 5,0.

-   Base de datos de administración: Use la base de datos de administración para administrar el acceso al paquete y para publicar la sincronización del servidor con el servidor de administración.

## Tareas de la consola de administración


Las tareas más comunes que puede realizar con la consola de administración de App-V 5,0 son:

-   [Cómo conectarse a la consola de administración](how-to-connect-to-the-management-console-beta.md)

-   [Cómo agregar o actualizar paquetes mediante el uso de la consola de administración](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md)

-   [Cómo configurar el acceso a los paquetes mediante el uso de la consola de administración](how-to-configure-access-to-packages-by-using-the-management-console-50.md)

-   [Cómo publicar un paquete mediante el uso de la consola de administración](how-to-publish-a-package-by-using-the-management-console-50.md)

-   [Cómo eliminar un paquete de la consola de administración](how-to-delete-a-package-in-the-management-console-beta.md)

-   [Cómo agregar o quitar un administrador mediante el uso de la consola de administración](how-to-add-or-remove-an-administrator-by-using-the-management-console.md)

-   [Cómo registrar y anular el registro de un servidor de publicación mediante el uso de la consola de administración](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console.md)

-   [Cómo crear un archivo de configuración personalizado mediante el uso de la consola de administración de App-V 5.0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md)

-   [Cómo transferir configuraciones y acceso a otra versión de un paquete mediante el uso de la consola de administración](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console.md)

-   [Cómo personalizar las extensiones de aplicaciones virtuales de un grupo AD específico mediante el uso de la consola de administración](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console.md)

-   [Configurar aplicaciones y extensiones de aplicaciones virtuales predeterminadas en la consola de administración](configure-applications-and-default-virtual-application-extensions-in-management-console.md)

Los elementos principales de la consola de administración de App-V 5,0 son:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Pestaña de consola de administración</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Introducción</p></td>
<td align="left"><p></p>
<ul>
<li><p><strong>Secuenciador de App-V </strong> - Seleccione esta opción para revisar la información general sobre el uso del secuenciador de 5,0 de App-v.</p></li>
<li><p><strong>Biblioteca de paquetes </strong> de aplicaciones: Seleccione esta opción para abrir la <strong> </strong> Página paquetes de la consola de administración. Use esta página para revisar los paquetes que se han agregado al servidor. También puede administrar los grupos de conexión, así como agregar o actualizar paquetes.</p></li>
<li><p><strong>SERVIDORES </strong> : Seleccione esta opción para abrir la <strong> </strong> Página servidores de la consola de administración. Use esta página para revisar la lista de servidores que se han registrado con la infraestructura de App-V 5,0.</p></li>
<li><p><strong>CLIENTES </strong> : Seleccione esta opción para revisar la información general sobre los clientes de App-V 5,0.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Ficha paquetes</p></td>
<td align="left"><p>Use la <strong> </strong> pestaña Paquetes para agregar o actualizar paquetes. También puede administrar grupos de conexión haciendo clic en <strong> grupos de conexión </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pestaña servidores</p></td>
<td align="left"><p>Use la <strong> </strong> pestaña servidores para registrar un nuevo servidor.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ficha administradores</p></td>
<td align="left"><p>Use la <strong> pestaña administradores </strong> para registrar, agregar o quitar administradores en el entorno de App-V 5,0.</p></td>
</tr>
</tbody>
</table>

 






## <a href="" id="other-resources-for-this-app-v-5-0-deployment-"></a>Otros recursos para esta implementación de App-V 5,0


-   [Guía del administrador de Microsoft Application Virtualization 5,0](microsoft-application-virtualization-50-administrators-guide.md)

-   [Operaciones de App-V 5.0](operations-for-app-v-50.md)

 

 





