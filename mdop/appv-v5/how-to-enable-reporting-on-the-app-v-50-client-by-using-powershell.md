---
title: Cómo habilitar los informes en el cliente de App-V 5.0 mediante PowerShell
description: Cómo habilitar los informes en el cliente de App-V 5.0 mediante PowerShell
author: dansimp
ms.assetid: a7aaf553-0f83-4cd0-8df8-93a5f1ebe497
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c004b4900a9814a11cb2706659a2edb99de6cc1b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814087"
---
# Cómo habilitar los informes en el cliente de App-V 5.0 mediante PowerShell


Use el siguiente procedimiento para configurar el 5,0 de App-V para informes.

**Para configurar el equipo que ejecuta el cliente de App-V 5,0 para informes**

1. Instale el cliente de App-V 5,0. Para obtener más información sobre la instalación del cliente [, consulte Cómo implementar el cliente de App-V](how-to-deploy-the-app-v-client-gb18030.md).

2. Después de instalar el cliente de App-V 5,0, use el PowerShell **set-AppvClientConfiguration** para configurar las opciones de configuración de informes apropiadas:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Configuración</th>
   <th align="left">Descripción</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>ReportingEnabled</p></td>
   <td align="left"><p>Permite al cliente devolver información a un servidor de informes. Esta configuración es necesaria para que el cliente recopile los datos de informes en el cliente.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingServerURL</p></td>
   <td align="left"><p>Especifica la ubicación en el servidor de informes donde se guarda la información del cliente. Por ejemplo, http:// &lt; reportingservername &gt; : &lt; reportingportnumber &gt; .</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Este es el número de puerto que se asignó durante la configuración del servidor de informes</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Hora de inicio de informes</p></td>
   <td align="left"><p>Se establece para programar el cliente para que envíe los datos al servidor automáticamente. Esta configuración indicará la hora a la que los datos de informes comenzarán a enviarse. Se encuentra en el formato de 24 horas y tomará un número entre 0-23.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingRandomDelay</p></td>
   <td align="left"><p>Especifica el retraso máximo (en minutos) para que los datos se envíen al servidor de informes. Cuando se inicia la tarea programada, el cliente genera una demora aleatoria entre 0 y ReportingRandomDelay, y esperará la duración especificada antes de enviar los datos.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingInterval</p></td>
   <td align="left"><p>Especifica el intervalo de reintento que usará el cliente para volver a enviar datos al servidor de informes.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReportingDataCacheLimit</p></td>
   <td align="left"><p>Especifica el tamaño máximo en megabytes (MB) de la caché XML para almacenar información de informes. El tamaño se aplica a la memoria caché en memoria. Cuando se alcance el límite, el archivo de registro se retirará.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ReportingDataBlockSize</p></td>
   <td align="left"><p>Especifica el tamaño máximo en megabytes (MB) de la caché XML para almacenar información de informes. El tamaño se aplica a la memoria caché en memoria. Cuando se alcance el límite, el archivo de registro se retirará.</p></td>
   </tr>
   </tbody>
   </table>



3. Una vez que se haya configurado la configuración adecuada, el equipo que ejecuta el cliente de App-V 5,0 recopilará los datos automáticamente y los enviará de vuelta al servidor de informes.

   Además, los administradores pueden volver a enviar los datos de forma manual mediante el cmdlet de PowerShell **send-AppvClientReport** .

   **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Administración de App-V mediante el uso de PowerShell](administering-app-v-by-using-powershell.md)









