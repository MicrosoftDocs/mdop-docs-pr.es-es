---
title: Cómo implementar el cliente de MBAM mediante el uso de una línea de comandos
description: Cómo implementar el cliente de MBAM mediante el uso de una línea de comandos
author: dansimp
ms.assetid: ac1d4ffe-c26d-41c9-9737-a4f2b37fde24
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 416d76ad876c5114e3a8764111b6a15c879b13b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824490"
---
# Cómo implementar el cliente de MBAM mediante el uso de una línea de comandos


Puede usar una línea de comandos para implementar el software de cliente de supervisión y administración de Microsoft BitLocker (MBAM).

## Línea de comandos para implementar el software de cliente de MBAM


Escriba el siguiente comando en el símbolo del sistema para aceptar automáticamente el contrato de licencia para el usuario final al implementar el software de cliente de MBAM.

**MBAMClientSetup.exe/acceptEula = Yes**

**Nota:**  Las opciones de línea de comandos **/Ju** y **/JM** no se admiten y no se pueden usar para instalar el software de cliente de MBAM.

 

Escriba el siguiente comando en el símbolo del sistema para extraer e instalar el MSP:

**MBAMClientSetup.exe la &lt; ruta de acceso/Extract para extraer MSI &gt; /AcceptEula = Yes**

Después, instale el MSI silenciosamente ejecutando el siguiente comando:

**msiexec/i &lt; ruta para extraído MSI &gt; /qb ALLUSERS = 1 REBOOT = ReallySuppress**

**Nota:**  A partir de MBAM 2,5 SP1, ya no se incluye un MSI aparte con el producto MBAM. Sin embargo, puede extraer el MSI del archivo ejecutable (. exe) que se incluye con el producto, después de aceptar el CLUF.

 

## <a href="" id="optin-for-microsoft-updates-1-command-line-option"></a>OPTIn \ _FOR \ _MICROSOFT \ _UPDATES = 1 opción de línea de comandos


Opcionalmente, puede especificar la opción de línea de comandos `OPTIN_FOR_MICROSOFT_UPDATES=1` durante la instalación del software cliente para instalar automáticamente las actualizaciones de Microsoft en equipos cliente. Al especificar esta opción, Microsoft Update se inicia automáticamente y busca las actualizaciones disponibles para instalarlas una vez finalizada la instalación del software cliente.

Puede usar esta opción de línea de comandos con cualquiera de los siguientes métodos de instalación.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Instale el software de cliente de MBAM con</th>
<th align="left">Ejemplo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>MBAMClientSetup.exe</strong></p></td>
<td align="left"><p><strong>MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES = 1</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>msiexec/i MBAMClient.msi</strong></p></td>
<td align="left"><p><strong>msiexec/i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES = 1</strong></p></td>
</tr>
</tbody>
</table>

 


## Temas relacionados


[Implementación de cliente de MBAM 2.5](deploying-the-mbam-25-client.md)

 

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




