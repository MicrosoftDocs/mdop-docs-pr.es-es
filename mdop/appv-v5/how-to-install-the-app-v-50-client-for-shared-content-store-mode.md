---
title: Cómo instalar el cliente de App-V 5.0 para el modo de almacén de contenido compartido
description: Cómo instalar el cliente de App-V 5.0 para el modo de almacén de contenido compartido
author: dansimp
ms.assetid: 88f09e6f-19e7-48ea-965a-907052d1a02f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 704ea6c1e4b1ba4670a4e52d754b8e6e5a9fb8f4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814055"
---
# Cómo instalar el cliente de App-V 5.0 para el modo de almacén de contenido compartido


Use el siguiente procedimiento para instalar el cliente de Microsoft Application Virtualization (App-V) 5,0 de modo que use el modo de almacén de contenido compartido (SCS) de App-V 5,0. Debe asegurarse de que todos los requisitos previos necesarios estén instalados en el equipo en el que planea instalar. Use el siguiente vínculo para los [requisitos previos de App-V 5,0](app-v-50-prerequisites.md).

**Nota:**  Antes de realizar este procedimiento, si es necesario, desinstale las versiones existentes del cliente de App-V 5,0.

 

Para más información sobre el modo SCS, vea [almacenamiento de contenido compartido en Microsoft App-V 5,0](https://go.microsoft.com/fwlink/?LinkId=316879) , entre bastidores ( https://go.microsoft.com/fwlink/?LinkId=316879) .

**Instalar y configurar el cliente de App-V 5,0 para el modo SCS**

1.  Copie los archivos de instalación del cliente App-V 5,0 en el equipo en el que se instalará. Abra una línea de comandos y, desde el directorio donde se guardan los archivos de instalación, escriba una de las siguientes opciones en función de la versión del cliente que esté instalando:

    -   Para instalar la versión de RDS del tipo de cliente App-V 5,0: **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**

    -   Para instalar la versión estándar del tipo de cliente App-V 5,0: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**

        **Importante**  Debe realizar una instalación silenciosa o se producirá un error en la instalación.

         

2.  Después de completar la instalación, puede implementar paquetes en el equipo en el que se ejecuta el cliente y todo el contenido del paquete se transmitirá a través de la red.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Implementación del secuenciador y del cliente de App-V 5.0](deploying-the-app-v-50-sequencer-and-client.md)

 

 





