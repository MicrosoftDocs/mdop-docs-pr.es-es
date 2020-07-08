---
title: Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,0 en el mismo equipo
description: Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,0 en el mismo equipo
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.openlocfilehash: 38e77ce6ce6c0dba7c67f6c0dfa5c9e263e07e20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814182"
---
# Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,0 en el mismo equipo

**Nota:** App-V 4,6 ha salido del soporte técnico estándar. A continuación se supone que el cliente de App-V 4,6 SP3 ya está instalado.

Use la siguiente información para instalar el cliente de App-V 5,0 (preferiblemente, con los Service Packs y las revisiones más recientes) y el cliente de App-V 4.6 SP3 en el mismo equipo. Para conocer las versiones compatibles, los requisitos y otra información de planificación, consulte [planificación de la migración desde una versión anterior de App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).

**Para implementar el cliente de App-V 5,0 y el cliente de App-V 4,6 en el mismo equipo**

1.  Instale el cliente del SP3 de App-V 5,0 en el equipo que ejecuta la versión de App-V 4,6 del cliente. Para obtener los mejores resultados, le recomendamos que instale todas las actualizaciones disponibles para el cliente del SP3 de App-V 5,0.

2.  Convertir o reordenar los paquetes gradualmente.

    -   Para convertir los paquetes, use el convertidor de paquetes de App-V 5,0 y convierta los paquetes necesarios al formato de archivo de App-V 5,0 (**. appv**).

    -   Para reordenar los paquetes, considere la posibilidad de usar la última versión del secuenciador para obtener los mejores resultados.

    Para obtener más información sobre la publicación de paquetes, consulte [Cómo publicar un paquete mediante la consola de administración](how-to-publish-a-package-by-using-the-management-console-50.md).

3.  Implemente paquetes en los equipos cliente.

4.  Convertir los puntos de extensión según sea necesario. Para obtener más información, consulta los siguientes recursos:

    -   [Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.0 convertido para todos los usuarios de un equipo específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.0 para un usuario específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [Cómo convertir un paquete creado en una versión anterior de App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  Pruebe que los paquetes de App-V 5,0 se hayan realizado correctamente y, a continuación, quite los paquetes 4,6. Para comprobar el estado de usuario de los equipos cliente, le recomendamos que use la [Virtualización](https://technet.microsoft.com/library/dn458947.aspx) de la experiencia del usuario u otra herramienta de administración del entorno del usuario.

    **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Planificación para migrar desde una versión anterior de App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)

[Implementación del secuenciador y del cliente de App-V 5.0](deploying-the-app-v-50-sequencer-and-client.md)

 

 





