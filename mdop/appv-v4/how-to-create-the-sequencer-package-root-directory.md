---
title: Cómo crear el directorio raíz del paquete secuenciador
description: Cómo crear el directorio raíz del paquete secuenciador
author: dansimp
ms.assetid: 23fe28f1-c284-43ee-b8b7-1dfbed94eea5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5150e87915202794624b6c51510e56454d2c7d36
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817620"
---
# Cómo crear el directorio raíz del paquete secuenciador


El directorio raíz del paquete es el directorio del equipo donde se ejecuta el secuenciador de App-V donde se instalan los archivos de la aplicación de secuencia. Este directorio también existe prácticamente en el equipo al que se transmitirá una aplicación de secuencia. Debe crear el directorio raíz del paquete antes de supervisar la instalación de una nueva aplicación.

Una vez que hayas creado el directorio de raíz del paquete, puedes comenzar a secuenciar las aplicaciones. Para obtener más información sobre la secuenciación de una nueva aplicación, vea [Cómo secuenciar una aplicación](how-to-sequence-an-application.md).

**Para crear el directorio raíz del paquete**

1.  Para crear el directorio raíz del paquete, en el equipo que ejecuta el secuenciador de App-V, asigne la unidad Q:\\ a la ubicación de red especificada. La ubicación que especifique debe tener suficiente espacio para guardar la aplicación que está transsecuencias.

2.  Para crear un directorio que pueda usar para una nueva aplicación virtual, cree una carpeta en la unidad de Q:\\ y asígnele un nombre.

    **Importante**  El nombre que asigne a los archivos de aplicación virtual que se guardarán en el directorio raíz del paquete debe usar el formato de nombre 8,3. Los nombres de archivo no deben tener más de 8 caracteres con una extensión de nombre de archivo de tres caracteres.

     

## Temas relacionados


[Secuenciador de virtualización de aplicaciones](application-virtualization-sequencer.md)

[Cómo modificar la ubicación del directorio de registro](how-to-modify-the-log-directory-location.md)

[Cómo modificar la ubicación del directorio temporal](how-to-modify-the-scratch-directory-location.md)

 

 





