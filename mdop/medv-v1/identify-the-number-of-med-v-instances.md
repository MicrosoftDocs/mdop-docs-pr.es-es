---
title: Identificar el número de instancias de MED-V
description: Identificar el número de instancias de MED-V
author: dansimp
ms.assetid: edea9bdf-a28c-4d24-9298-7bd6536c3a94
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 22f7d54318d2dc489461474e5531c5162d8c087d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824260"
---
# Identificar el número de instancias de MED-V


Debe determinar el número de instancias de MED-V, así como definir el ámbito de cada instancia para que pueda diseñar la infraestructura del servidor. Una instancia de MED-V incluye lo siguiente:

-   El servidor MED-V y las áreas de trabajo de MED-V almacenadas en el servidor, incluidos los permisos de Active Directory.

-   Una base de datos de SQL Server que almacena eventos de cliente. La base de datos puede estar compartida por varias instancias de MED-V.

-   El repositorio de imágenes de las imágenes de MED-V empaquetadas. El repositorio se puede compartir con varias instancias de MED-V.

-   La consola de administración que se usa para crear y empaquetar imágenes y para crear áreas de trabajo de MED-V. La consola no se puede usar simultáneamente por varias instancias de MED-V, pero se puede desconectar de un servidor MED-V y, a continuación, conectarse a otro servidor MED-V.

-   Clientes de MED-V que reciben áreas de trabajo de MED-V y autorización para usarlas en el servidor.

Las instancias de MED-V independientes no se pueden integrar ni compartir áreas de trabajo de MED-V. Por lo tanto, cada instancia adicional descentraliza la administración de la virtualización.

## Determinar el número de instancias de MED-V necesarias


Para empezar, supongamos que está usando una instancia de MED-V. A continuación, considere las condiciones siguientes y agregue instancias adicionales para cada condición que se aplique a su infraestructura.

-   Número de usuarios admitidos: cada instancia de MED-V puede admitir hasta 5.000 clientes activos de forma simultánea. Activo de forma simultánea significa que el cliente está conectado con el servidor MED-V y envía sondeos al servidor para obtener actualizaciones de directivas e imágenes, así como eventos. Si su infraestructura incluye más de 5.000 usuarios activos, agregue una instancia para cada 5.000 usuarios.

-   Usuarios de dominios que no son de confianza: los permisos de área de trabajo de Med-v Server Associates MED-V con usuarios o grupos de Active Directory. Esto requiere que los usuarios de MED-V existan dentro de los límites de confianza del servidor MED-V. Agregue una instancia de MED-V para cada grupo de usuarios de MED-V que se encuentra en un dominio independiente que no es de confianza.

-   Clientes en redes aisladas: Determine si los clientes residen en redes aisladas y, por lo tanto, requieren una instancia de MED-V independiente. Por ejemplo, las organizaciones suelen aislar las redes de laboratorio de las redes de producción. Agregue una instancia de MED-V para cada red aislada que contendrá clientes de MED-V.

-   Requisitos de la organización: la organización puede requerir que un grupo de clientes sea administrado por una instancia de MED-V independiente por razones de seguridad, como cuando las aplicaciones confidenciales se entregan solo a un conjunto restringido de usuarios dentro de un dominio. Por ejemplo, el Departamento de nóminas puede denegar a los usuarios de otros departamentos el acceso a la instancia de MED-V que almacena la Directiva para el procesamiento de nóminas. Además, si la organización usa un modelo de administración distribuida, se puede requerir una instancia de MED-V independiente para cada grupo empresarial que tiene clientes de MED-V para habilitar el grupo para administrar su propio entorno virtualizado. Agregue una instancia de MED-V para cada requisito organizativo independiente.

-   Consideraciones legales: los problemas de privacidad o de seguridad nacionales y las leyes de FIDUCIARY pueden requerir la separación de determinados datos o impedir que otros datos crucen las fronteras nacionales. Si es necesario, agregue instancias de MED-V adicionales para satisfacer esta necesidad.

Después de determinar el número de instancias de MED-V necesarias para su infraestructura, así como el razonamiento de cada una, proporcione un nombre para cada instancia.

 

 





