---
title: Cómo crear un grupo de conexión con los paquetes publicados por el usuario y lo publicados globalmente
description: Cómo crear un grupo de conexión con los paquetes publicados por el usuario y lo publicados globalmente
author: dansimp
ms.assetid: 82f7ea7f-7b14-4506-8940-fdcd6c3e117f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: c98981180133881909db17d19cb42771f94bd66a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814351"
---
# Cómo crear un grupo de conexión con los paquetes publicados por el usuario y lo publicados globalmente
Puede crear grupos de conexión con el usuario titulado que contengan paquetes publicados por el usuario y de forma global, mediante uno de los métodos siguientes:

-   [Cómo usar los cmdlets de PowerShell para crear grupos de conexión con el título del usuario](#bkmk-posh-userentitled-cg)

-   [Cómo usar el servidor de App-V para crear grupos de conexión con el titular del usuario](#bkmk-appvserver-userentitled-cg)

**Qué debe saber antes de empezar:**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Escenarios no compatibles y posibles problemas</th>
<th align="left">Resultado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>No puede incluir paquetes publicados por el usuario en grupos de conexión con derecho global.</p></td>
<td align="left"><p>Se producirá un error en el grupo de conexión.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Si publica un paquete globalmente y, a continuación, crea un grupo de conexión publicado por el usuario en el que lo ha hecho no es opcional, aún puede ejecutar <strong> la anulación de publicación: &lt; paquete AppvClientPackage &gt; -global </strong> para anular la publicación del paquete, incluso cuando ese paquete se está usando en otro grupo de conexión.</p></td>
<td align="left"><p>Si cualquier otro grupo de conexión está usando ese paquete, el paquete no se ejecutará en esos grupos de conexión.</p>
<p>Para evitar la eliminación inadvertida de la publicación de un paquete no opcional que se está usando en otro grupo de conexión, le recomendamos que realice un seguimiento de los grupos de conexión en los que ha usado un paquete no opcional.</p></td>
</tr>
</tbody>
</table>

 
<a href="" id="bkmk-posh-userentitled-cg"></a>**Cómo usar los cmdlets de PowerShell para crear grupos de conexión titulados por el usuario**

1.  Agregue y publique paquetes con los siguientes comandos:

    **Add-AppvClientPackage package1 \ _AppV \ _file \ _Path**

    **Add-AppvClientPackage package2 \ _AppV \ _file \ _Path**

    **Publish-AppvClientPackage-PackageId package1 \ _ID-VersionId package1 \ _Version ID: global**

    **Publish-AppvClientPackage-PackageId package2 \ _ID-VersionIdPackage2 \ _ID**

2.  Cree el archivo XML del grupo de conexiones. Para obtener más información, consulte [acerca del archivo de grupo de conexión](about-the-connection-group-file.md).

3.  Agregue y publique el grupo de conexión con los siguientes comandos:

    **Add-AppvClientConnectionGroup conexión \ _Group \ _XML \ _file \ _Path**

    **Enable-AppvClientConnectionGroup-GroupId CG \ _Group \ _ID-VersionId CG \ _Version \ _ID**

<a href="" id="bkmk-appvserver-userentitled-cg"></a>**Cómo usar el servidor de App-V para crear grupos de conexión titulados por el usuario**

1.  Abra la consola de administración de App-V 5,0.

2.  Siga las instrucciones que encontrará en [Cómo publicar un paquete mediante la consola de administración](how-to-publish-a-package-by-using-the-management-console-50.md) para publicar paquetes de forma global y para el usuario.

3.  Siga las instrucciones que encontrará en [Cómo crear un grupo de conexiones](how-to-create-a-connection-group.md) para crear el grupo de conexiones y agregue los paquetes publicados por el usuario y los que se hayan publicado de forma global.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Administración de grupos de conexión](managing-connection-groups.md)

[Cómo usar los paquetes opcionales en grupos de conexión](how-to-use-optional-packages-in-connection-groups.md)

 

 





