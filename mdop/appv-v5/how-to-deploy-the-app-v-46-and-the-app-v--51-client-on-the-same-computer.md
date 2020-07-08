---
title: Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,1 en el mismo equipo
description: Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,1 en el mismo equipo
ms.assetid: 498d50c7-f13d-4fbb-8ea1-b959ade26fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 354db96223e623a7cd0416cb49ad67eb4d8f7162
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814174"
---
# Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,1 en el mismo equipo

**Nota:** App-V 4,6 ha salido del soporte técnico estándar.

Use la siguiente información para instalar el cliente de Microsoft Application Virtualization (App-V) 5,1 (preferiblemente, con los Service Packs y las revisiones más recientes) y el cliente de App-V 4.6 SP2 o App-V 4.6 S3 en el mismo equipo. Para conocer las versiones compatibles, los requisitos y otra información de planificación, consulte [planificación de la migración desde una versión anterior de App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).

**Para implementar el cliente de App-V 5,1 y el cliente de App-V 4,6 en el mismo equipo**

1.  Instale la siguiente versión del cliente de App-V en el equipo que ejecuta App-V 4,6.

    -   [Microsoft Application Virtualization 4,6 Service Pack 3](https://www.microsoft.com/download/details.aspx?id=41187)

2.  Instale el cliente de App-V 5,1 en el equipo que ejecuta la versión de App-V 4,6 SP3 del cliente. Para obtener los mejores resultados, le recomendamos que instale todas las actualizaciones disponibles para el cliente de App-V 5,1.

3.  Convertir o reordenar los paquetes gradualmente.

    -   Para convertir los paquetes, use el convertidor de paquetes de App-V 5,1 y convierta los paquetes necesarios al formato de archivo de App-V 5,1 (**. appv**).

    -   Para reordenar los paquetes, considere la posibilidad de usar la última versión del secuenciador para obtener los mejores resultados.

    Para obtener más información sobre la publicación de paquetes, consulte [Cómo publicar un paquete mediante la consola de administración](how-to-publish-a-package-by-using-the-management-console-51.md).

4.  Implemente paquetes en los equipos cliente.

5.  Convertir los puntos de extensión según sea necesario. Para obtener más información, consulta los siguientes recursos:

    -   [Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.1 convertido para todos los usuarios de un equipo específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

    -   [Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.1 para un usuario específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

    -   [Cómo convertir un paquete creado en una versión anterior de App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

6.  Pruebe que los paquetes de App-V 5,1 se hayan realizado correctamente y, a continuación, quite los paquetes 4,6. Para comprobar el estado de usuario de los equipos cliente, le recomendamos que use la [Virtualización](https://technet.microsoft.com/library/dn458947.aspx) de la experiencia del usuario u otra herramienta de administración del entorno del usuario.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Planificación para migrar desde una versión anterior de App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md)

[Implementación del secuenciador y del cliente de App-V 5.1](deploying-the-app-v-51-sequencer-and-client.md)

 

 





