---
title: Planificación de creación de imagen para recuperación de DaRT 10
description: Planificación de creación de imagen para recuperación de DaRT 10
author: dansimp
ms.assetid: a0087d93-b88f-454b-81b2-3c7ce3718023
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 44cf052eaffd19645885618da9104e5b0a50cfd5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822980"
---
# Planificación de creación de imagen para recuperación de DaRT 10


Use la información de esta sección cuando planee crear la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 10.

## Planificación para crear la imagen de recuperación de DaRT 10


Al crear la imagen de recuperación de DaRT, debe decidir qué herramientas incluir en la imagen. Para tomar la decisión, tenga en cuenta que los usuarios finales pueden tener acceso a esas herramientas. Si los ingenieros de soporte técnico van a llevar el medio de la imagen de recuperación a los equipos de los usuarios finales para diagnosticar problemas, es posible que desee instalar todas las herramientas de la imagen de recuperación. Si va a diagnosticar equipos del usuario final de forma remota, es posible que desee deshabilitar algunas de las herramientas, como el barrido de disco y el editor del registro, y, a continuación, habilitar otras herramientas, incluida la conexión remota.

Cuando cree la imagen de recuperación de DaRT, también deberá especificar si desea incluir archivos o drivers adicionales. Determine la ubicación de cualquier controlador o archivo adicional que desee incluir en la imagen de recuperación de DaRT.

Para obtener más información sobre las herramientas de DaRT, vea [información general sobre las herramientas de DART 10](overview-of-the-tools-in-dart-10.md). Para obtener más información sobre cómo crear una imagen de recuperación segura, consulte [consideraciones de seguridad para DART 10](security-considerations-for-dart-10.md).

## Requisitos previos para la imagen de recuperación


Se requieren o se recomiendan los siguientes elementos para crear la imagen de recuperación de DaRT:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Como requisito previo</strong></p></td>
<td align="left"><p><strong>Detalles</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Archivos de origen de Windows 10</p></td>
<td align="left"><p>Necesario para crear la imagen de recuperación de DaRT. Proporciona la ruta de acceso de un DVD de Windows 10 o de archivos de origen de Windows 10.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Herramientas de depuración de Windows para su plataforma</p></td>
<td align="left"><p>Necesario cuando ejecuta el <strong> analizador de bloqueos </strong> para determinar la causa de un error en el equipo. Le recomendamos que especifique la ruta de las herramientas de depuración de Windows en el momento de crear la imagen de recuperación de DaRT. Puede descargar las herramientas de depuración de Windows aquí: <a href="https://docs.microsoft.com/windows-hardware/drivers/debugger/" data-raw-source="[Download and Install Debugging Tools for Windows](https://docs.microsoft.com/windows-hardware/drivers/debugger/)"> Descargar e instalar herramientas de depuración para Windows </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Opcional: archivos de símbolos de Windows para usar con el <strong> analizador de bloqueos</strong></p></td>
<td align="left"><p>Normalmente, la información de depuración se almacena en un archivo de símbolos que es independiente del programa. Debe tener acceso a la información de símbolos Cuando depure una aplicación que ha dejado de responder, por ejemplo, si ha dejado de funcionar. Para obtener más información, consulte <a href="diagnosing-system-failures-with-crash-analyzer-dart-10.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer-dart-10.md)"> diagnosticar errores del sistema con el analizador de bloqueos </a> .</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados

[Planificación de la implementación de DaRT 10](planning-to-deploy-dart-10.md)

 

 




