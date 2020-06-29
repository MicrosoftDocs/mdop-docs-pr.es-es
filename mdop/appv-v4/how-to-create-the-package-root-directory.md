---
title: Cómo crear el directorio raíz del paquete
description: Cómo crear el directorio raíz del paquete
author: dansimp
ms.assetid: bcfe3bd4-6c60-409a-8ffa-cc22f27194b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c9e1e7be71627d4e55eff7a4e2582a21b834876d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817630"
---
# Cómo crear el directorio raíz del paquete


El directorio raíz del paquete es el directorio del equipo donde se ejecuta el secuenciador de App-V donde se instalan los archivos de la aplicación de secuencia. Este directorio también existe prácticamente en el equipo al que se transmitirá una aplicación de secuencia. Debe crear el directorio raíz del paquete antes de supervisar la instalación de una nueva aplicación.

Una vez que hayas creado el directorio de raíz del paquete, puedes comenzar a secuenciar las aplicaciones. Para obtener más información sobre cómo se puede secuenciar una nueva aplicación, vea [Cómo instalar el secuenciador](how-to-install-the-sequencer.md).

**Para crear el directorio raíz del paquete**

1.  Para crear el directorio raíz del paquete, en el equipo que ejecuta el secuenciador de App-V, asigne la unidad Q:\\ a la ubicación de red especificada. La ubicación que especifique debe tener suficiente espacio para guardar la aplicación que está transsecuencias.

2.  Para crear un directorio que pueda usar para una nueva aplicación virtual, cree una carpeta en la unidad de Q:\\ y asígnele un nombre.

    **Importante**  El nombre que asigne a los archivos de aplicación virtual que se guardarán en el directorio raíz del paquete debe usar el formato de nombre 8,3. Los nombres de archivo no deben tener más de 8 caracteres con una extensión de nombre de archivo de tres caracteres.

     

## Temas relacionados


[Tareas del secuenciador de virtualización de aplicaciones](tasks-for-the-application-virtualization-sequencer.md)

 

 





