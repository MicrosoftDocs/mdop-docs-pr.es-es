---
title: Introducción a Administración avanzada de directivas de grupo
description: Introducción a Administración avanzada de directivas de grupo
author: dansimp
ms.assetid: 3a8d1e58-12b9-42bd-898f-6d57514dfbb9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: feb43972c78ed12501e372800c1f5ec19609477a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822491"
---
# Introducción a Administración avanzada de directivas de grupo


Puede usar la administración de directivas de grupo (AGPM) avanzada para extender las capacidades de la consola de administración de directivas de grupo (GPMC) para proporcionar control de cambios completo y una administración mejorada para objetos de directiva de grupo (GPO).

## Desarrollo de objetos de directiva de grupo con control de cambios


Con AGPM, puede almacenar una copia de cada GPO en un archivo central para que los administradores de la Directiva de grupo puedan verlo y cambiarlo sin conexión sin afectar inmediatamente a la versión implementada del GPO. Además, AGPM almacena una copia de cada versión de cada GPO controlado en el archivo para que pueda volver a una versión anterior si es necesario.

Los términos "proteger" y "desprotección" se usan de la misma manera que en una biblioteca (o en aplicaciones que proporcionan control de cambios, control de versiones o control de código fuente para programación de programación). Para usar un libro que está en una biblioteca, debe desprotegerlo de la biblioteca. Nadie más puede usarla mientras la hayas desprotegido. Cuando haya terminado con el libro, vuelva a registrarlo en la biblioteca para que otros usuarios puedan usarlo.

Al desarrollar GPO mediante AGPM:

1.  Cree un GPO controlado nuevo o controle un GPO previamente no controlado.

2.  Desproteja el GPO, de modo que usted y solo usted pueda cambiarlo.

3.  Edite el GPO.

4.  Proteja el GPO editado, de modo que otros usuarios puedan cambiarlo, o para que pueda implementarse.

5.  Revise los cambios.

6.  Implemente el GPO en el entorno de producción.

## Delegación basada en roles


AGPM proporciona una delegación completa y fácil de usar para administrar el acceso a los GPO en el archivo. Los permisos de nivel de dominio permiten a los administradores de AGPM proporcionar acceso a dominios individuales sin proporcionar acceso a otros dominios. La delegación basada en GPO permite a los administradores de AGPM proporcionar acceso a GPO específicos sin proporcionar acceso en todo el dominio.

En AGPM, hay roles definidos específicamente: administrador de AGPM (control total), aprobador, editor y revisor. El rol de administrador de AGPM incluye los permisos para todos los demás roles. De forma predeterminada, solo los aprobadores tienen la capacidad de implementar GPO en el entorno de producción, lo que protege el entorno de errores de los editores menos experimentados. También de forma predeterminada, todos los roles incluyen el rol de revisor y, por lo tanto, la posibilidad de ver la configuración de GPO en los informes. Sin embargo, AGPM proporciona a un administrador de AGPM la flexibilidad para personalizar el acceso a los GPO según las necesidades de su organización.

## Delegación en un entorno de administrador de varias directivas de grupo


En un entorno en el que varias personas cambian los GPO, un administrador de AGPM delega los permisos a editores, aprobadores y revisores, ya sea como grupos o como individuos. Para obtener un proceso de desarrollo de GPO típico para un editor y un aprobador, vea [lista de comprobación: crear, editar e implementar un GPO](checklist-create-edit-and-deploy-a-gpo-agpm30ops.md).

### Referencias adicionales

-   [Guía de operaciones de Administración avanzada de directivas de grupo de MIcrosoft 3.0](operations-guide-for-microsoft-advanced-group-policy-management-30-agpm30ops.md)

 

 





