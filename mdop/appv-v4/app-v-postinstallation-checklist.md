---
title: Lista de comprobación de postinstalación de App-V
description: Lista de comprobación de postinstalación de App-V
author: dansimp
ms.assetid: 74db297e-a744-4287-bcc6-0e096ca8b57a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 79728bd2043076b20eb37ba0b1fa6f834a0d94bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819801"
---
# Lista de comprobación de postinstalación de App-V


La siguiente lista de comprobación proporciona una lista de elementos de nivel superior para considerar y esquematiza los pasos que debe realizar una vez completada la instalación del servidor de administración de Microsoft Application Virtualization (App-V), el servidor de streaming de App-V y el cliente de escritorio de App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paso</th>
<th align="left">Referencia</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Cree excepciones de Firewall para el servidor de administración de App-V o servicios de servidor de streaming.</p></td>
<td align="left"><p><a href="configuring-the-firewall-for-the-app-v-servers.md" data-raw-source="[Configuring the Firewall for the App-V Servers](configuring-the-firewall-for-the-app-v-servers.md)">Configurar el firewall para los servidores de App-V</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Verifique que el sistema App-V funcione correctamente mediante la publicación, la transmisión y la prueba de la aplicación predeterminada.</p></td>
<td align="left"><p><a href="how-to-install-and-configure-the-default-application.md" data-raw-source="[How to Install and Configure the Default Application](how-to-install-and-configure-the-default-application.md)">Cómo instalar y configurar la aplicación predeterminada</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configure el cliente de App-V para usar el servidor de streaming de App-V u otro servidor para la transmisión por medio de la <strong> configuración de ApplicationSourceRoot </strong> , <strong> IconSourceRoot </strong> y <strong> OSDSourceRoot </strong> .</p></td>
<td align="left"><p><a href="how-to-configure-the-client-for-application-package-retrieval.md" data-raw-source="[How to Configure the Client for Application Package Retrieval](how-to-configure-the-client-for-application-package-retrieval.md)">Cómo configurar al cliente para la recuperación del paquete de aplicación</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Aprenda a usar la versión de archivo. msi de paquetes de aplicaciones secuenciadas para la implementación sin conexión.</p></td>
<td align="left"><p><a href="how-to-publish-a-virtual-application-on-the-client.md" data-raw-source="[How to Publish a Virtual Application on the Client](how-to-publish-a-virtual-application-on-the-client.md)">Cómo publicar una aplicación virtual en el cliente</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Faculta Configure la creación de reflejo de la base de datos de SQL Server para la base de datos de App-V.</p></td>
<td align="left"><p><a href="how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md" data-raw-source="[How to Configure Microsoft SQL Server Mirroring Support for App-V](how-to-configure-microsoft-sql-server-mirroring-support-for-app-v.md)">Cómo configurar el soporte técnico en duplicación de Microsoft SQL Server para App-V</a></p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Implementación de virtualización de aplicaciones y listas de comprobación de actualización](application-virtualization-deployment-and-upgrade-checklists.md)

 

 





