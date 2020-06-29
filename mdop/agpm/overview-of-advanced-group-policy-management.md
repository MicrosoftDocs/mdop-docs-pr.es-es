---
title: Introducción a Administración avanzada de directivas de grupo
description: Introducción a Administración avanzada de directivas de grupo
author: dansimp
ms.assetid: 028de9dd-848b-42bc-a982-65ba5c433772
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38396de6bd8bdace72d3add1bba09769ae26de32
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822481"
---
# Introducción a Administración avanzada de directivas de grupo


Puede usar la administración de directivas de grupo (AGPM) avanzada para ampliar las capacidades de la consola de administración de directivas de grupo (GPMC) y proporcionar control de cambios completo y administración mejorada para objetos de directiva de grupo (GPO).

## Desarrollo de objetos de directiva de grupo con control de cambios


Con AGPM, puede almacenar una copia de cada GPO en un archivo central, de modo que los administradores de la Directiva de grupo puedan verlo y modificarlo sin conexión sin afectar inmediatamente a la versión implementada del GPO. Además, AGPM almacena una copia de cada versión de cada GPO controlado en el archivo para que pueda volver a una versión anterior si es necesario.

Los términos "proteger" y "desprotección" se usan casi de la misma manera que en una biblioteca (o en aplicaciones que proporcionan control de cambios, control de versiones o control de código fuente para el desarrollo de programación). Para usar un libro que está en una biblioteca, debe desprotegerlo de la biblioteca. Nadie más puede usarla mientras la hayas desprotegido. Cuando haya terminado con el libro, vuelva a registrarlo en la biblioteca para que otros usuarios puedan usarlo.

Al desarrollar GPO con AGPM:

1.  Cree un GPO controlado nuevo o controle un GPO previamente no controlado.

2.  Desproteja el GPO para que usted y solo usted pueda modificarlo.

3.  Edite el GPO.

4.  Proteja el GPO editado, para que otros usuarios puedan modificarlo, o para que se pueda implementar.

5.  Revise los cambios.

6.  Implemente el GPO en el entorno de producción.

## Delegación basada en roles


AGPM proporciona una delegación completa, fácil de usar y basada en roles. Los permisos de nivel de dominio permiten a los administradores de AGPM proporcionar acceso a dominios individuales sin proporcionar acceso a otros dominios. La delegación basada en GPO permite a los administradores de AGPM permitir el acceso solo a determinados GPO.

En AGPM, hay roles definidos específicamente: administrador de AGPM (control total), aprobador, editor y revisor. El rol de administrador de AGPM incluye los permisos para todos los demás roles. De forma predeterminada, solo los aprobadores tienen la capacidad de implementar GPO en el entorno de producción, lo que protege el entorno de errores accidentales de los editores menos experimentados. También de forma predeterminada, todos los roles incluyen el rol de revisor y, por lo tanto, la posibilidad de ver la configuración de GPO en los informes. Sin embargo, AGPM proporciona a un administrador de AGPM la flexibilidad para personalizar el acceso a los GPO según las necesidades de su organización.

## Delegación en un entorno de administrador de varias directivas de grupo


En un entorno en el que varias personas realicen cambios en los GPO, un administrador de AGPM delegará permisos a editores, aprobadores y revisores, ya sea como grupos o como individuos. Para obtener un proceso de desarrollo de GPO típico para un editor y un aprobador, vea [lista de comprobación: crear, editar e implementar un GPO](checklist-create-edit-and-deploy-a-gpo.md).

### Referencias adicionales

-   [Lista de comprobación: Crear, editar e implementar un GPO](checklist-create-edit-and-deploy-a-gpo.md)

-   [Realización de tareas del administrador AGPM](performing-agpm-administrator-tasks.md)

-   [Realización de tareas de editor](performing-editor-tasks.md)

-   [Realización de tareas del Aprobador](performing-approver-tasks.md)

-   [Realización de tareas de revisor](performing-reviewer-tasks.md)

-   [Solución de problemas de Administración avanzada de directivas de grupo](troubleshooting-advanced-group-policy-management.md)

-   [Interfaz de usuario: Administración avanzada de directivas de grupo](user-interface-advanced-group-policy-management.md)

 

 





