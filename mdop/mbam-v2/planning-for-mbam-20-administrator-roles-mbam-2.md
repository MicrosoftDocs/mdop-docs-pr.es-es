---
title: Planificación de roles de administrador de MBAM 2.0
description: Planificación de roles de administrador de MBAM 2.0
author: dansimp
ms.assetid: 6f813297-6479-42d3-a21b-896d54466b5b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a89a04c0ef074407dc3cd081d351d44023e65e70
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824891"
---
# Planificación de roles de administrador de MBAM 2.0


En este tema se enumeran y describen los roles de administrador disponibles en administración y supervisión de BitLocker de Microsoft (MBAM), así como las ubicaciones de servidor donde se crean los grupos locales.

## Roles de administrador de MBAM


<a href="" id="---------------mbam-system-administrators"></a> **Administradores del sistema MBAM**  
Los administradores de este rol tienen acceso a todas las características de supervisión y administración de Microsoft BitLocker. El grupo local para este rol está instalado en el servidor de supervisión y administración.

<a href="" id="---------------mbam-helpdesk-users"></a> **Usuarios de MBAM Helpdesk**  
Los administradores de este rol tienen acceso a las características de soporte técnico de MBAM. El grupo local para este rol está instalado en el servidor de supervisión y administración.

<a href="" id="---------------mbam-report-users"></a> **Usuarios de informes de MBAM**  
Los administradores de este rol tienen acceso a los informes de cumplimiento y cumplimiento de la MBAM. El grupo local para este rol está instalado en el servidor de administración y supervisión, la base de datos de cumplimiento y la auditoría, y en el servidor que hospeda los informes de cumplimiento y cumplimiento.

<a href="" id="---------------mbam-advanced-helpdesk-users"></a> **MBAM los usuarios avanzados del servicio de asistencia**  
Los administradores de este rol han aumentado el acceso a las características de soporte técnico de MBAM. El grupo local para este rol está instalado en el servidor de supervisión y administración. Si un usuario es miembro de MBAM y usuarios del Departamento de soporte técnico avanzado, los permisos de usuario del servicio de asistencia al MBAM avanzado sobrescribirán los permisos de usuario de MBAM Helpdesk.

**Importante**  Para ver los informes, un usuario administrativo debe ser miembro del grupo de seguridad de **usuarios de informes de MBAM** en el servidor de administración y supervisión, la base de datos de cumplimiento y auditoría, y en el servidor que hospeda la característica informes de cumplimiento y auditoría. Como práctica recomendada, cree un grupo de seguridad en los servicios de dominio de Active Directory con derechos en el grupo de seguridad local de **los usuarios de MBAM** en el servidor de supervisión y administración y en el servidor que hospeda los informes de cumplimiento y cumplimiento.

 

## Temas relacionados


[Preparación del entorno para MBAM 2.0](preparing-your-environment-for-mbam-20-mbam-2.md)

 

 





