---
title: Acerca de cómo usar la línea de comandos del secuenciador
description: Acerca de cómo usar la línea de comandos del secuenciador
author: dansimp
ms.assetid: 0fd5f81b-17f9-4065-bce2-8785e8aac7c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: afb3fb8608c78a3b9237a80529a6c22d792661ba
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819901"
---
# Acerca de cómo usar la línea de comandos del secuenciador


Puede usar la línea de comandos para crear paquetes de aplicaciones secuenciados. El uso de la línea de comandos para crear aplicaciones virtuales es útil en los siguientes escenarios:

-   Necesita crear un gran número de paquetes de aplicación secuenciados.

-   Es necesario crear un paquete de aplicación con secuencia de forma periódica.

**Importante**  La secuenciación en el símbolo del sistema solo permite la secuenciación predeterminada. Si necesita cambiar los parámetros de secuenciación predeterminados, debe modificar manualmente un paquete de aplicación secuencial o volver a crear una secuencia de la aplicación.

 

Todas las modificaciones posteriores de los paquetes de aplicaciones secuenciadas existentes deben realizarse mediante el Asistente para secuenciación.

## Requisitos previos


Para ordenar una aplicación mediante el símbolo del sistema, se deben cumplir las condiciones siguientes:

-   La aplicación que se va a secuenciar no debe requerir cambios ni soluciones alternativas para el instalador o el paquete de Windows Installer.

-   Antes de la secuenciación, debe preparar una lista de archivos por lotes para crear los paquetes de aplicación secuenciados.

-   Revise para obtener más información sobre los parámetros de la línea de comandos, consulte [parámetros de la línea de comandos](command-line-parameters.md).

-   Revise los errores que se pueden mostrar al crear un paquete de aplicación de secuencia con la línea de comandos. Para obtener más información, vea estos errores en [errores de la línea de comandos](command-line-errors.md).

## Temas relacionados


[Cómo administrar aplicaciones virtuales con la línea de comandos](how-to-manage-virtual-applications-using-the-command-line.md)

 

 





