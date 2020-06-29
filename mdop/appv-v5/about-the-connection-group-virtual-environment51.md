---
title: Información acerca del entorno virtual del grupo de conexión
description: Información acerca del entorno virtual del grupo de conexión
author: dansimp
ms.assetid: b7bb0e3d-8cd5-45a9-b84e-c9ab4196a18c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 43f30c2100fc982170f15c305b03cd338b5d8afd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814886"
---
# Información acerca del entorno virtual del grupo de conexión


**En este tema:**

-   [Cómo se determina la prioridad del paquete](#bkmk-pkg-priority-deter)

-   [Combinación de rutas de paquetes idénticas en un directorio virtual de grupos de conexión](#bkmk-merged-root-ve-exp)

## <a href="" id="bkmk-pkg-priority-deter"></a>Cómo se determina la prioridad del paquete


El entorno virtual y su estado actual están asociados con el grupo de conexión, no con los paquetes individuales. Si se quita un paquete de App-V del grupo de conexiones, el estado que existía como parte del grupo de conexión no se migrará con el paquete.

Si el mismo paquete forma parte de dos grupos de conexión diferentes, debe indicar qué aplicación de grupo de conexión debe usar. Por ejemplo, es posible que tenga dos paquetes en un grupo de conexión para que cada uno de ellos defina el mismo valor DWORD del registro.

El grupo de conexión que se usa se basa en el orden en que un paquete aparece dentro del documento XML **AppConnectionGroup** :

-   El primer paquete tiene la prioridad más alta.

-   El segundo paquete tiene la segunda prioridad más alta.

Considere la siguiente sección de ejemplo:

```xml
<appv:Packages><appv:PackagePackageId="A8731008-4523-4713-83A4-CD1363907160"VersionId="E889951B-7F30-418B-A69C-B37283BC0DB9"/><appv:PackagePackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"VersionId="01F1943B-C778-40AD-BFAD-AC34A695DF3C"/><appv:PackagePackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"/></appv:Packages>
```

Supongamos que el mismo valor DWORD ABC (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region) se define en el primer y tercer paquete, por ejemplo:

-   Paquete 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5

-   Paquete 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 10

Como el paquete 1 aparece primero, el entorno virtual de AppConnectionGroup tendrá el valor DWORD único de 5 (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5). Esto significa que las aplicaciones virtuales del paquete 1, package 2 y Package 3 verán el valor 5 cuando hacen una consulta para HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region.

Otros recursos de entorno virtual se resuelven de forma similar, pero el caso habitual es que las colisiones se producen en el registro.

## <a href="" id="bkmk-merged-root-ve-exp"></a>Combinación de rutas de paquetes idénticas en un directorio virtual de grupos de conexión


Si dos o más paquetes de un grupo de conexiones contienen rutas de directorio idénticas, las rutas se combinan en un único directorio virtual dentro del entorno virtual del grupo de conexión. Esta combinación de rutas permite que una aplicación de un paquete tenga acceso a los archivos de un paquete diferente.

Al quitar un paquete de un grupo de conexiones, las aplicaciones de ese paquete eliminado ya no podrán obtener acceso a los archivos del grupo de conexiones que quede en los demás paquetes.

El orden en el que App-V busca el nombre de un archivo en el grupo de conexión se especifica mediante el orden en el que se muestran los paquetes de App-V en el archivo de manifiesto del grupo de conexión.

En el ejemplo siguiente se muestra el orden y la relación de una búsqueda de nombres de archivo en un grupo de conexión para el **paquete a** y el **paquete B**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Empaquetar una</th>
<th align="left">Paquete B</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>C:\Windows\System32</p></td>
<td align="left"><p>C:\Windows\System32</p></td>
</tr>
<tr class="even">
<td align="left"><p>C:\AppTest</p></td>
<td align="left"><p>C:\AppTest</p></td>
</tr>
</tbody>
</table>

 

En el ejemplo anterior, cuando una aplicación virtualizada intenta encontrar un archivo específico, se busca en primer lugar una ruta de acceso de archivo coincidente. Si no se encuentra una ruta de acceso coincidente, se busca en el paquete B con las siguientes reglas de asignación:

-   Si hay un archivo denominado **test.txt** en la misma jerarquía de carpetas virtuales de ambos paquetes de la aplicación, se usa el primero.

-   Si un archivo denominado **bar.txt** existe en la jerarquía de carpetas virtuales de un paquete de la aplicación, pero no en el otro, se usa el primer archivo coincidente.






## Temas relacionados


[Administración de grupos de conexión](managing-connection-groups51.md)

 

 





