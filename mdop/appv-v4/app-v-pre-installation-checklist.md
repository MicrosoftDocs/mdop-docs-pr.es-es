---
title: Lista de comprobación de preinstalación de App-V
description: Lista de comprobación de preinstalación de App-V
author: dansimp
ms.assetid: 3af609b1-2c09-4edb-b083-b913b6d5e8c4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 70e71d3dea02daeadedb4cff78c58302ac743dda
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819790"
---
# Lista de comprobación de preinstalación de App-V


La siguiente lista de comprobación tiene el propósito de proporcionar una lista de alto nivel de los elementos que se deben tener en cuenta y describe los pasos que debe realizar antes de instalar los servidores de Microsoft Application Virtualization (App-V).

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
<td align="left"><p>Asegúrese de que su entorno de equipos cumpla con las configuraciones admitidas para App-V.</p></td>
<td align="left"><p><a href="application-virtualization-deployment-requirements.md" data-raw-source="[Application Virtualization Deployment Requirements](application-virtualization-deployment-requirements.md)">Requisitos de implementación de virtualización de aplicaciones</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configure los grupos y las cuentas de Active Directory necesarios.</p></td>
<td align="left"><p><a href="configuring-prerequisite-groups-in-active-directory-for-app-v.md" data-raw-source="[Configuring Prerequisite Groups in Active Directory for App-V](configuring-prerequisite-groups-in-active-directory-for-app-v.md)">Configurar grupos de requisitos previos en Active Directory para App-V</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Establezca la configuración de Internet Information Services (IIS) en el servidor que ejecuta IIS.</p></td>
<td align="left"><p><a href="how-to-configure-windows-server-2008-for-app-v-management-servers.md" data-raw-source="[How to Configure Windows Server 2008 for App-V Management Servers](how-to-configure-windows-server-2008-for-app-v-management-servers.md)">Cómo configurar Windows Server 2008 para servidores de administración de App-V</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Configure el servidor en el que se está ejecutando IIS para que sea de confianza para la delegación.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Esto solo es necesario si instalas el servidor de administración de App-V mediante una arquitectura de sistema distribuida, es decir, si instalas la consola de administración de App-V, el servicio Web de administración y la base de datos en diferentes equipos.</p>
</div>
<div>

</div></td>
<td align="left"><p><a href="how-to-configure-the-server-to-be-trusted-for-delegation.md" data-raw-source="[How to Configure the Server to be Trusted for Delegation](how-to-configure-the-server-to-be-trusted-for-delegation.md)">Cómo configurar el servidor para que sea de confianza para delegación</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Instale Microsoft SQL Server 2008.</p></td>
<td align="left"><p><a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="[Install SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=181924)">Instale SQL Server 2008 </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=181924" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=181924"> https://go.microsoft.com/fwlink/?LinkId=181924 </a> ).</p></td>
</tr>
</tbody>
</table>



## Temas relacionados


[Implementación de virtualización de aplicaciones y listas de comprobación de actualización](application-virtualization-deployment-and-upgrade-checklists.md)

[Lista de comprobación de instalación de App-V](app-v-installation-checklist.md)









