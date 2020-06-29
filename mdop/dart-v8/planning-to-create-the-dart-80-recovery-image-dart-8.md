---
title: Planificación de creación de imagen para recuperación de DaRT 8.0
description: Planificación de creación de imagen para recuperación de DaRT 8.0
author: dansimp
ms.assetid: cfd0e1e2-c379-4460-b545-3f7be9f33583
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 1d1dc7dc5b3776638523a282d9216b80d4ce9ce1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824810"
---
# Planificación de creación de imagen para recuperación de DaRT 8.0


Use la información de esta sección cuando planee crear la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 8,0.

## Planificación para crear la imagen de recuperación de DaRT 8,0


Al crear la imagen de recuperación de DaRT, debe decidir qué herramientas incluir en la imagen. Para tomar la decisión, tenga en cuenta que los usuarios finales pueden tener acceso a esas herramientas. Si los ingenieros de soporte técnico van a llevar el medio de la imagen de recuperación a los equipos de los usuarios finales para diagnosticar problemas, es posible que desee instalar todas las herramientas de la imagen de recuperación. Si va a diagnosticar equipos del usuario final de forma remota, es posible que desee deshabilitar algunas de las herramientas, como el barrido de disco y el editor del registro, y, a continuación, habilitar otras herramientas, incluida la conexión remota.

Cuando cree la imagen de recuperación de DaRT, también deberá especificar si desea incluir archivos o drivers adicionales. Determine la ubicación de cualquier controlador o archivo adicional que desee incluir en la imagen de recuperación de DaRT.

Para obtener más información sobre las herramientas de DaRT, consulte [información general sobre las herramientas de dart 8,0](overview-of-the-tools-in-dart-80-dart-8.md). Para obtener más información sobre cómo crear una imagen de recuperación segura, consulte [consideraciones de seguridad para DaRT 8,0](security-considerations-for-dart-80--dart-8.md).

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
<td align="left"><p>Archivos de origen de Windows 8</p></td>
<td align="left"><p>Necesario para crear la imagen de recuperación de DaRT. Proporcione la ruta de acceso de un DVD de Windows 8 o de archivos de origen de Windows 8.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Herramientas de depuración de Windows para su plataforma</p></td>
<td align="left"><p>Necesario cuando ejecuta el <strong> analizador de bloqueos </strong> para determinar la causa de un error en el equipo. Le recomendamos que especifique la ruta de las herramientas de depuración de Windows en el momento de crear la imagen de recuperación de DaRT. Puede descargar las herramientas de depuración de Windows aquí: <a href="https://go.microsoft.com/fwlink/?LinkId=99934" data-raw-source="[Download and Install Debugging Tools for Windows](https://go.microsoft.com/fwlink/?LinkId=99934)"> Descargar e instalar herramientas de depuración para Windows </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Opcional: <strong> definiciones de defender </strong></p></td>
<td align="left"><p>Las definiciones más recientes de <strong> defender </strong> son obligatorias al ejecutar <strong> defender </strong> . Aunque puede descargar las definiciones al ejecutar <strong> defender </strong> , le recomendamos que descargue las definiciones más recientes en el momento de crear la imagen de recuperación de DART, de modo que aún pueda ejecutar la herramienta con las definiciones más recientes incluso si el problema no tiene conectividad de red.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Opcional: archivos de símbolos de Windows para usar con el <strong> analizador de bloqueos</strong></p></td>
<td align="left"><p>Normalmente, la información de depuración se almacena en un archivo de símbolos que es independiente del programa. Debe tener acceso a la información de símbolos Cuando depure una aplicación que ha dejado de responder, por ejemplo, si ha dejado de funcionar. Para obtener más información, consulte <a href="diagnosing-system-failures-with-crash-analyzer--dart-8.md" data-raw-source="[Diagnosing System Failures with Crash Analyzer](diagnosing-system-failures-with-crash-analyzer--dart-8.md)"> diagnosticar errores del sistema con el analizador de bloqueos </a> .</p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Planificación de la implementación de DaRT 8.0](planning-to-deploy-dart-80-dart-8.md)

 

 





