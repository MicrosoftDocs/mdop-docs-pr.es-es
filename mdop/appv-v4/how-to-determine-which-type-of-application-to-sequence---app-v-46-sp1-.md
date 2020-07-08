---
title: Cómo determinar qué tipo de aplicación se va a secuenciar (App-V 4,6 SP1)
description: Cómo determinar qué tipo de aplicación se va a secuenciar (App-V 4,6 SP1)
author: dansimp
ms.assetid: 936abee2-98f1-45fb-9f0d-786e1d7464b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 001f6afa36ca28eb1b8e0cc2ccc161cef4194d24
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817490"
---
# Cómo determinar qué tipo de aplicación se va a secuenciar (App-V 4,6 SP1)


Puede hacer una secuencia de tres tipos básicos de aplicaciones con Microsoft Application Virtualization (App-V) Sequencer.

## Para determinar qué tipo de aplicación se va a secuenciar


Use la tabla siguiente para determinar qué tipo de aplicación debe secuenciar y obtener más información sobre cómo hacer una secuencia de la aplicación.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de aplicación</th>
<th align="left">Descripción</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Standard</p></td>
<td align="left"><p>Seleccione esta opción para crear un paquete que contenga una aplicación o un conjunto de aplicaciones. Debe seleccionar esta opción para la mayoría de las aplicaciones que planea secuenciar.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-standard-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Standard Application (App-V 4.6 SP1)](how-to-sequence-a-new-standard-application--app-v-46-sp1-.md)">Cómo secuenciar una nueva aplicación estándar (App-V 4.6 SP1)</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>Complemento o complemento</p></td>
<td align="left"><p>Seleccione esta opción para crear un paquete que extienda la funcionalidad de una aplicación estándar, por ejemplo, un complemento de Microsoft Excel. Además, puede usar complementos para aplicaciones instaladas de forma nativa u otro paquete vinculado mediante la composición dinámica de conjuntos. Para obtener más información sobre la composición de conjuntos dinámicos, vea <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> Cómo usar la composición de conjunto dinámico </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Add-on or Plug-in Application (App-V 4.6 SP1)](how-to-sequence-a-new-add-on-or-plug-in-application--app-v-46-sp1-.md)">Cómo secuenciar un nuevo complemento o aplicación de complemento (App-V 4.6 SP1)</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Cabe</p></td>
<td align="left"><p>Seleccione esta opción para crear un paquete necesario para una aplicación estándar, por ejemplo, Microsoft .NET Framework. Los paquetes de middleware se usan para vincular a otros paquetes mediante la composición de conjunto dinámico. Para obtener más información sobre la composición de conjuntos dinámicos, vea <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="[How To Use Dynamic Suite Composition](https://go.microsoft.com/fwlink/?LinkId=203804)"> Cómo usar la composición de conjunto dinámico </a> ( <a href="https://go.microsoft.com/fwlink/?LinkId=203804" data-raw-source="https://go.microsoft.com/fwlink/?LinkId=203804"> https://go.microsoft.com/fwlink/?LinkId=203804 </a> ).</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md" data-raw-source="[How to Sequence a New Middleware Application (App-V 4.6 SP1)](how-to-sequence-a-new-middleware-application--app-v-46-sp1-.md)">Cómo secuenciar una nueva aplicación de software intermedio (App-V 4.6 SP1)</a></p></td>
</tr>
</tbody>
</table>

 

## Temas relacionados


[Tareas del secuenciador de virtualización de aplicaciones (App-V 4.6 SP1)](tasks-for-the-application-virtualization-sequencer--app-v-46-sp1-.md)

 

 





