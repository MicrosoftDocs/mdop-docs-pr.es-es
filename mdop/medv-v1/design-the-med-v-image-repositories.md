---
title: Diseñar los repositorios de imagen MED-V
description: Diseñar los repositorios de imagen MED-V
author: dansimp
ms.assetid: e153154d-2751-4990-b94d-a2d76242c15f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0c59a0dd2d1b3a78bd211c6a6353a86c77d8fc2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823611"
---
# Diseñar los repositorios de imagen MED-V


Después de crear y empaquetar las imágenes de MED-V, se pueden almacenar en un servidor de archivos en cualquier ubicación. Los archivos pueden enviarse a través de HTTP o HTTPS por uno o más servidores de IIS. El repositorio de imágenes se puede compartir con varias instancias de MED-V.

Para diseñar los repositorios de imágenes, primero debe decidir cómo se implementarán las imágenes en cada cliente y, a continuación, si el cliente necesita un repositorio de imágenes local. A continuación, cada repositorio se diseña y se coloca junto con el servidor IIS que lo acompaña.

## Determinar cómo se implementarán las imágenes


Para cada área de trabajo de MED-V, decida cómo desea implementar las imágenes de MED-V en el cliente. Esto es importante para determinar cuántos repositorios son necesarios para almacenar las imágenes empaquetadas, dónde se colocarán los repositorios y, a continuación, para diseñar esos repositorios.

Las imágenes empaquetadas se pueden implementar de las siguientes maneras:

-   Descargarse a través de la red desde un servidor de distribución de imágenes, que incluye un servidor de archivos y un servidor IIS.

-   En medios extraíbles, como una unidad USB o un DVD.

-   Preconfigurada en un directorio de almacenamiento de imágenes en el equipo cliente mediante un centro de distribución de software empresarial.

Decida qué método (o métodos) se usará para implementar imágenes de MED-V en cada uno de los clientes y si la ubicación necesitará un repositorio de imágenes.

## Determinar el número de repositorios de imágenes


Ahora que ha determinado la cantidad mínima de repositorios que necesita, añada más si se aplica alguno de los siguientes criterios:

-   Razones organizativas o reglamentarias para separar las imágenes de MED-V: es posible que algunas imágenes de MED-V no puedan coexistir en el mismo repositorio. Por ejemplo, los datos personales confidenciales pueden requerir almacenamiento en un servidor que solo esté disponible para un conjunto limitado de empleados que necesiten acceder a los datos.

-   Clientes en redes aisladas: si las imágenes se van a implementar a través de la red, determine si las redes están aisladas y requieren un repositorio independiente. Por ejemplo, las organizaciones suelen aislar las redes de laboratorio de las redes de producción.

-   Clientes en redes remotas: si las imágenes se van a implementar a través de la red, algunos equipos cliente pueden estar separados del repositorio por vínculos de red que no tienen suficiente ancho de banda para proporcionar una experiencia adecuada cuando un cliente carga un área de trabajo de MED-V. Si es necesario, diseñe instancias adicionales de MED-V para satisfacer estas necesidades.

Agregue estos repositorios al diseño. Decidir un nombre para cada repositorio y el motivo de su diseño. Decidir qué imágenes de MED-V guardarán los repositorios y qué clientes de MED-V cargarán áreas de trabajo de MED-V con imágenes del repositorio.

## Diseñar y colocar los repositorios de imágenes


Cuando una imagen nueva está disponible para los clientes, los clientes comienzan a descargar la imagen, posiblemente de forma simultánea. Esto crea una demanda elevada en el repositorio y se debe tener en cuenta al diseñar el repositorio de la imagen.

Para cada repositorio, determine la cantidad de datos que se van a almacenar. Suma los tamaños de las imágenes que se almacenarán en el repositorio. Este es el valor del espacio en disco requerido en el servidor de archivos.

Después, suma el número de clientes que pueden descargar imágenes de MED-V del repositorio. Este es el número máximo de descargas simultáneas que se pueden producir cuando se carga una nueva imagen de MED-V en el repositorio. El servidor de archivos debe estar diseñado con un subsistema de disco que pueda cumplir con las demandas de e/s que creará.

El repositorio de imágenes puede residir en el mismo sistema que el servidor MED-V y en el servidor que ejecuta SQL Server, o bien en un recurso compartido de archivos remoto. También puede ejecutarla en una máquina virtual de Hyper-V de Windows Server2008. Compruebe la ubicación de red de los clientes a los que dará servicio el repositorio de imágenes y coloque el repositorio en una ubicación de red en la que tendrá suficiente ancho de banda para cumplir con las expectativas de nivel de servicio de esos clientes.

### Tolerancia a errores

Si el repositorio de imágenes no está disponible, los clientes no podrán descargar imágenes de MED-V nuevas o actualizadas. Para diseñar las opciones de tolerancia a errores para el servidor de archivos y los discos tolerantes a errores, consulte la guía de [planificación y diseño de la infraestructura de Microsoft SQL server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) .

## Diseñar y colocar los servidores IIS


Esta sección solo es relevante si los clientes van a descargar los archivos de imagen a través de la red mediante HTTP o HTTPS.

El servidor IIS puede coexistir en el mismo sistema que el servidor MED-V y en el servidor que ejecuta SQL Server. También puede ejecutarse en una VM Hyper-V de Windows Server2008. La infraestructura del servidor IIS debe tener el rendimiento suficiente para proporcionar imágenes a los clientes dentro de las expectativas de nivel de servicio de la organización. Debe estar diseñado con un subsistema de disco que pueda cumplir con las demandas de e/s que crea.

Para cada repositorio de imágenes, suma el número de clientes que pueden descargar imágenes de MED-V con IIS. Este es el número máximo de descargas simultáneas que pueden producirse cuando se carga una imagen en el repositorio. Use la suma de rendimiento y las expectativas de nivel de servicio determinadas en [definir el ámbito del proyecto](define-the-project-scope.md) para planear el diseño de la infraestructura del servidor IIS y para determinar la cantidad de ancho de banda adecuada que se debe asignar al repositorio.

Para diseñar la infraestructura de IIS, consulte la guía [planeamiento y diseño de la infraestructura de Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .

### Tolerancia a errores

Si la infraestructura de servidor IIS no está disponible, los clientes no podrán descargar imágenes nuevas o actualizadas. Para configurar la tolerancia a errores, el servidor IIS basado en Windows Server2008 se puede colocar en un clúster de conmutación por error. Para diseñar la tolerancia a errores para la infraestructura del servidor IIS, consulte la guía de [planificación y diseño de la infraestructura de Microsoft Internet Information Services](https://go.microsoft.com/fwlink/?LinkId=160826) .

## Temas relacionados


[Implementación de un área de trabajo de MED-V mediante un sistema de distribución de software de empresa](deploying-a-med-v-workspace-using-an-enterprise-software-distribution-system.md)

[Implementación de un área de trabajo de MED-V mediante un paquete de implementación](deploying-a-med-v-workspace-using-a-deployment-package.md)

 

 





