---
title: Cómo configurar el servidor de distribución de imagen web
description: Cómo configurar el servidor de distribución de imagen web
author: dansimp
ms.assetid: 2d32ae79-dff5-4c05-a412-dd15452b6007
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8a21b14fbaca6bbc09d4c35b4d8fb86365c42e3b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825160"
---
# Cómo configurar el servidor de distribución de imagen web


Un repositorio de imágenes es un servidor opcional que se usa para la distribución de imágenes (donde los administradores cargan las imágenes nuevas y los equipos cliente comprueban el servidor cada 15 minutos y actualizan su imagen si hay una nueva disponible).

## <a href="" id="bkmk-configuringanimagereporitoryusingiis"></a>


Un servidor de distribución de imágenes requiere lo siguiente:

-   Servicios de Internet Information Server (IIS): para obtener información, vea [servicios de información de Internet](https://go.microsoft.com/fwlink/?LinkId=142995).

    Durante la instalación de IIS, al agregar servicios de rol, seleccione los siguientes métodos de autenticación admitidos:

    -   **Autenticación básica**

    -   **Autenticación de Windows**

    -   **Autenticación de asignación de certificado de cliente**

    Al configurar IIS, incluya lo siguiente:

    -   Agregue un directorio virtual, con el alias denominado **MEDVImages**. La ruta de acceso física debe apuntar a la ubicación de las imágenes.

    -   Habilitar BITS.

    -   Agregue los siguientes tipos MIME:

        -   **. CKM (aplicación/flujo de octetos)**

        -   **. Indice (aplicación/flujo de octetos**)

    -   En el sitio MED-V, agregue permisos de lectura a **todos los usuarios**.

    -   Reinicie IIS.

-   Extensiones de servidor BITS para IIS: para obtener información, consulte [instalar extensiones de servidor bits](https://go.microsoft.com/fwlink/?LinkId=142996).

## Temas relacionados


[Configuraciones admitidas](supported-configurationsmedv-orientation.md)

[Diseñar los repositorios de imagen MED-V](design-the-med-v-image-repositories.md)

 

 





