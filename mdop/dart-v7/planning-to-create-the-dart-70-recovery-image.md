---
title: Planificación de creación de imagen para recuperación de DaRT 7.0
description: Planificación de creación de imagen para recuperación de DaRT 7.0
author: dansimp
ms.assetid: e5d49bee-ae4e-467b-9976-c1203f6355f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c370d2a69ec8ccea217696045e64e9a0ae724815
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821331"
---
# Planificación de creación de imagen para recuperación de DaRT 7.0


Use la información de esta sección cuando Planee la creación de la imagen de recuperación de Microsoft Diagnostics and Recovery Toolset (DaRT) 7.

## Planificación para crear la imagen de recuperación de DaRT 7


Al crear la imagen de recuperación de DaRT, debe decidir qué herramientas incluir en la imagen. Cuando tome esta decisión, recuerde que es posible que los usuarios finales tengan acceso ocasionalmente a las diversas herramientas de DaRT. Para obtener más información sobre las herramientas de DaRT, consulte [información general sobre las herramientas de dart 7,0](overview-of-the-tools-in-dart-70-new-ia.md). Para obtener más información sobre cómo crear una imagen de recuperación segura, consulte [consideraciones de seguridad para DaRT 7,0](security-considerations-for-dart-70-dart-7.md).

Cuando cree la imagen de recuperación de DaRT, también deberá especificar si desea incluir archivos o drivers adicionales. Determine la ubicación de cualquier controlador o archivo adicional que desee incluir en la imagen de recuperación de DaRT.

## Requisitos previos


Se requieren o se recomiendan los siguientes elementos para crear la imagen de recuperación de DaRT:

-   Archivos de origen de Windows 7

    Debe proporcionar la ruta de acceso de un DVD de Windows 7 o de un archivo de origen de Windows 7. Los archivos de origen de Windows 7 son necesarios para crear la imagen de recuperación de DaRT.

-   Herramientas de depuración de Windows para su plataforma

    Las herramientas de depuración de Windows son necesarias cuando se ejecuta el **analizador de bloqueos** para determinar la causa de un bloqueo del equipo. Le recomendamos que especifique la ruta de las herramientas de depuración de Windows en el momento de crear la imagen de recuperación de DaRT. Si es necesario, puede descargar las herramientas de depuración de Windows aquí: [Descargar e instalar herramientas de depuración para Windows](https://go.microsoft.com/fwlink/?LinkId=99934).

-   Opcional: definiciones de **limpieza del sistema independiente**

    Al ejecutar esta herramienta, se necesitan las definiciones más recientes de la herramienta de **limpieza del sistema independiente** . Aunque puede descargar las definiciones cuando ejecuta el **sistema de limpieza independiente**, le recomendamos que descargue las definiciones más recientes en el momento de crear la imagen de recuperación de DART. De esta manera, aún puede ejecutar la herramienta con las definiciones más recientes incluso si el problema no tiene conexión de red.

-   Opcional: archivos de símbolos de Windows para usar con el **analizador de bloqueos**

    Normalmente, la información de depuración se almacena en un archivo de símbolos que es independiente del ejecutable. Debe tener acceso a la información de símbolos Cuando depure una aplicación que ha dejado de responder, por ejemplo, si se ha bloqueado. Para obtener más información, consulte [diagnosticar errores del sistema con el analizador de bloqueos](diagnosing-system-failures-with-crash-analyzer--dart-7.md).

## Temas relacionados


[Planificación de la implementación de DaRT 7.0](planning-to-deploy-dart-70.md)

 

 





