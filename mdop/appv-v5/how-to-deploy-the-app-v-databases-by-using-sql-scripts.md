---
title: Cómo implementar las bases de datos de App-V mediante el uso de scripts SQL
description: Cómo implementar las bases de datos de App-V mediante el uso de scripts SQL
author: dansimp
ms.assetid: 23637936-475f-4ca5-adde-76bb27d2372b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 511d1020571eead25af9e9591fe1834a9f97f068
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814111"
---
# Cómo implementar las bases de datos de App-V mediante el uso de scripts SQL


Use las siguientes instrucciones para usar secuencias de comandos SQL, en lugar de Windows Installer, para:

-   Instalar las bases de datos de App-V 5,0

-   Actualizar las bases de datos de 5,0 a una versión posterior

**Cómo instalar las bases de datos de App-V con scripts SQL**

1. Antes de instalar los scripts de base de datos, revise y mantenga una copia de los términos de licencia de App-V. Al ejecutar los scripts de base de datos, aceptas los términos de licencia. Si no la aceptas, no deberías usar este software.

2. Copie el **appv\_server\_setup.exe** de los medios de versión de App-V en una ubicación temporal.

3. Desde un símbolo del sistema, ejecute **appv\_server\_setup.exe** y especifique una ubicación temporal para extraer los scripts de base de datos.

   Ejemplo: appv\_server\_setup.exe/layout c:\\ &lt; ruta de acceso de ubicación temporal&gt;

4. Vaya a la ubicación temporal que ha creado, abra la carpeta **DatabaseScripts** extraída y revise el archivo de Readme.txt correspondiente para obtener instrucciones:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Base de datos</th>
   <th align="left">Ubicación de Readme.txt archivo para usar</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Base de datos de administración</p></td>
   <td align="left"><p>Subcarpeta ManagementDatabase</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Si está actualizando o instalando la base de datos de administración de App-V 5,0 SP3, consulte <a href="https://support.microsoft.com/kb/3031340" data-raw-source="[SQL scripts to install or upgrade the App-V 5.0 SP3 Management Server database fail](https://support.microsoft.com/kb/3031340)"> scripts SQL para instalar o actualizar la base de datos del servidor de administración de App-v 5,0 SP3 </a> .</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Base de datos de informes</p></td>
   <td align="left"><p>Subcarpeta ReportingDatabase</p></td>
   </tr>
   </tbody>
   </table>



~~~
**Got a suggestion for App-V**? Add or vote on suggestions [here](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **Got an App-V issue?** Use the [App-V TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).
~~~

## Temas relacionados


[Implementación del servidor de App-V 5.0](deploying-the-app-v-50-server.md)

[Cómo implementar el servidor de App-V 5.0](how-to-deploy-the-app-v-50-server-50sp3.md)









