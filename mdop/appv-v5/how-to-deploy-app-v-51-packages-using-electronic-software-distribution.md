---
title: Cómo implementar paquetes de App-V 5.1 con la distribución electrónica de software
description: Cómo implementar paquetes de App-V 5.1 con la distribución electrónica de software
author: dansimp
ms.assetid: e1957a5a-1f18-42da-b2c1-a5ae5a4cca7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a9ed5fbb264f8fb9676d7fa18fe4de8019ea8e79
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814183"
---
# Cómo implementar paquetes de App-V 5.1 con la distribución electrónica de software


Puede usar un sistema de distribución electrónica de software (ESD) para implementar aplicaciones virtuales de App-V 5,1 en clientes de App-V. Para obtener más información, consulte la documentación disponible con el ESD que está usando.

Para conocer los requisitos de componente y las opciones para usar un ESD para implementar paquetes de App-V, consulte [planificación para implementar App-v 5,1 con un sistema electrónico de distribución de software](planning-to-deploy-app-v-51-with-an-electronic-software-distribution-system.md).

Use uno de los siguientes métodos para publicar paquetes en equipos cliente de App-V con un ESD:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Método</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Funcionalidad proporcionada por una tercera parte ESD</p></td>
<td align="left"><p>Usar la funcionalidad en un ESD de terceros.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Installer independiente</p></td>
<td align="left"><p>Instale la aplicación en el equipo cliente de destino con el archivo de Windows Installer (. msi) asociado que se crea al momento de la secuencia de una aplicación. El archivo de Windows Installer contiene la información del archivo de paquete de App-V 5,1 asociada para configurar un paquete y copiar los archivos de paquete necesarios en el cliente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>Use los cmdlets de PowerShell para implementar aplicaciones virtualizadas. Para obtener más información sobre cómo usar PowerShell y App-V 5,1, vea <a href="administering-app-v-51-by-using-powershell.md" data-raw-source="[Administering App-V 5.1 by Using PowerShell](administering-app-v-51-by-using-powershell.md)"> Administración de App-v 5,1 con PowerShell </a> .</p></td>
</tr>
</tbody>
</table>

 

**Para implementar paquetes de App-V 5,1 con un ESD**

1.  Instale el secuenciador de 5,1 de App-V en un equipo de su entorno. Para obtener más información sobre cómo instalar el secuenciador, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer-51beta-gb18030.md).

2.  Use el secuenciador de aplicaciones-V 5,1 para crear una aplicación virtual. Para obtener información sobre la creación de una aplicación virtual, vea [crear y administrar aplicaciones virtualizadas de App-V 5,1](creating-and-managing-app-v-51-virtualized-applications.md).

3.  Después de crear la aplicación virtual, implemente el paquete con la solución de ESD.

    Si está usando System Center Configuration Manager, empiece por revisar la [Introducción a administración de aplicaciones en Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=281816) para obtener información sobre el uso de App-V 5,1 y System Center2012 Configuration Manager.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Operaciones de App-V 5.1](operations-for-app-v-51.md)

 

 





