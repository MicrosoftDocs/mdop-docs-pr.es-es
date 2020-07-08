---
title: Administrar aplicaciones virtuales de App-V 5.1 con la consola de administración
description: Administrar aplicaciones virtuales de App-V 5.1 con la consola de administración
author: dansimp
ms.assetid: a4d078aa-ec54-4fa4-9463-bfb3b971d724
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63ec965519bedef08b09c961dc5d1c90e1d8d694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814863"
---
# Administrar aplicaciones virtuales de App-V 5.1 con la consola de administración


Use el servidor de administración de Microsoft Application Virtualization (App-V) 5,1 para administrar paquetes, grupos de conexión y acceso al paquete en su entorno. El servidor publica los iconos de la aplicación, los accesos directos y las asociaciones de tipos de archivo en los equipos autorizados que ejecutan el cliente de App-V 5,1. Uno o varios servidores de administración suelen compartir un almacén de datos común para la información de configuración y del paquete.

El servidor de administración usa grupos de servicios de dominio de Active Directory (AD DS) para administrar la autorización del usuario y tiene instalado SQL Server para administrar la base de datos y el almacén de datos.

Debido a que los servidores de administración transmiten las aplicaciones a los usuarios finales a petición, estos servidores son ideales para las configuraciones del sistema que tienen LAN fiables de alto ancho de banda. El servidor de administración consta de los siguientes componentes:

-   Servidor de administración: Use el servidor de administración para administrar paquetes y grupos de conexión.

-   Publishing Server: Use el servidor de publicación para implementar paquetes en equipos que ejecuten el cliente de App-V 5,1.

-   Base de datos de administración: Use la base de datos de administración para administrar el acceso al paquete y para publicar la sincronización del servidor con el servidor de administración.

## Tareas de la consola de administración


Las tareas más comunes que puede realizar con la consola de administración de App-V 5,1 son:

-   [Cómo conectarse a la consola de administración](how-to-connect-to-the-management-console-51.md)

-   [Cómo agregar o actualizar paquetes mediante el uso de la consola de administración](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [Cómo configurar el acceso a los paquetes mediante el uso de la consola de administración](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [Cómo publicar un paquete mediante el uso de la consola de administración](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [Cómo eliminar un paquete de la consola de administración](how-to-delete-a-package-in-the-management-console-51.md)

-   [Cómo agregar o quitar un administrador mediante el uso de la consola de administración](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [Cómo registrar y anular el registro de un servidor de publicación mediante el uso de la consola de administración](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [Cómo crear un archivo de configuración personalizado mediante el uso de la consola de administración de App-V 5.1](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [Cómo transferir configuraciones y acceso a otra versión de un paquete mediante el uso de la consola de administración](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [Cómo personalizar las extensiones de aplicaciones virtuales de un grupo AD específico mediante el uso de la consola de administración](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [Cómo ver y configurar aplicaciones y extensiones de la aplicación virtual predeterminada mediante el uso de la consola de administración](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

Los elementos principales de la consola de administración de App-V 5,1 son:

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
<td align="left"><p>Ficha paquetes</p></td>
<td align="left"><p>Use la <strong> </strong> pestaña Paquetes para agregar o actualizar paquetes.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ficha grupos de conexión</p></td>
<td align="left"><p>Use la <strong> pestaña grupos </strong> de conexión para administrar grupos de conexión.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Pestaña servidores</p></td>
<td align="left"><p>Use la <strong> </strong> pestaña servidores para registrar un nuevo servidor.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Ficha administradores</p></td>
<td align="left"><p>Use la <strong> pestaña administradores </strong> para registrar, agregar o quitar administradores en el entorno de App-V 5,1.</p></td>
</tr>
</tbody>
</table>

 

**Importante**  JavaScript debe estar habilitado en el explorador que abre la consola de administración web.

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a>Otros recursos para esta implementación de App-V 5,1


-   [Guía del administrador de Microsoft Application Virtualization 5,1](microsoft-application-virtualization-51-administrators-guide.md)

-   [Operaciones de App-V 5.1](operations-for-app-v-51.md)

 

 





