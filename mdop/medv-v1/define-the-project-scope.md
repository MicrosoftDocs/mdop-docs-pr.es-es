---
title: Definir el ámbito del proyecto
description: Definir el ámbito del proyecto
author: dansimp
ms.assetid: 84637d2a-2e30-417d-b150-dc81f414b3a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4f33562452327bba9036f56d9f6f96650f00c1f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823641"
---
# Definir el ámbito del proyecto


Cuando defina el ámbito del proyecto, determine lo siguiente:

1.  Los usuarios finales de MED-V: la ubicación y el número de usuarios finales se usan para determinar la ubicación de las instalaciones de cliente MED-V y la cantidad de instancias de MED-v, así como el número y la ubicación de los repositorios de imágenes de MED-V.

2.  Las imágenes de la máquina virtual (VM) que se administran por MED-V, para determinar el método de distribución de las imágenes y la ubicación de los repositorios de imágenes.

3.  Las expectativas de nivel de servicio de la organización para determinar los requisitos de rendimiento y tolerancia a errores para el servidor y la base de datos de MED-V, así como para el repositorio de imágenes.

4.  Validar con el negocio: Asegúrese de que haya una comprensión completa de cómo la infraestructura planeada afecta a la empresa.

## Definir los usuarios finales de MED-V


En primer lugar, determine dónde se encuentran los usuarios finales, así como el número de usuarios en cada ubicación. En segundo lugar, obtenga un diagrama de infraestructura de red que muestre las ubicaciones de los usuarios y el ancho de banda disponible para esas ubicaciones. Por último, averigüe si los usuarios viajan entre ubicaciones. Si los usuarios viajan, es posible que se necesite capacidad adicional en el diseño de la infraestructura del servidor y de los repositorios de imágenes.

## Determinar las imágenes de MED-V que se administran en MED-V


Una vez que se hayan definido los usuarios finales de MED-V, determine qué máquinas virtuales administrará MED-V para los usuarios de cada ubicación.

Si cualquiera de las máquinas virtuales está almacenada en una biblioteca centralizada, determine la ubicación de la biblioteca para que se pueda evaluar su uso como repositorio de MED-V.

## <a href="" id="determine-the-organization-s-service-level-expectations"></a>Determinar las expectativas de nivel de servicio de la organización


Para cada área de trabajo de MED-V, anote el tiempo aceptable para que se cargue una nueva imagen y el intervalo de tiempo para que se implementen las actualizaciones críticas.

Si procede, registre las expectativas de nivel de servicio para los informes de MED-V, que se usarán en el diseño de la infraestructura del servidor.

## Validar con la empresa


Pida a las partes interesadas y a los propietarios de la aplicación las siguientes preguntas:

-   ¿Hay alguna imagen que se pueda combinar? Por ejemplo, si la aplicación A de WindowsXP es una imagen de VPC y la aplicación B en WindowsXP es otra imagen de VPC, tal vez una sola imagen puede contener ambas aplicaciones, lo que reduce el espacio del repositorio y el ancho de banda necesario para la descarga de imágenes.

-   ¿Las aplicaciones dentro del ámbito se pueden conceder a licencias y se pueden admitir si se entregan en una VM por MED-V? Consulte con el proveedor de la aplicación para asegurarse de que no se infringirán los términos de licencia y soporte al entregar la aplicación a través de MED-V.

 

 





