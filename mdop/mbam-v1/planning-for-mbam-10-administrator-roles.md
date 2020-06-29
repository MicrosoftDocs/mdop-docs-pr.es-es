---
title: Planificación de roles de administrador de MBAM 1.0
description: Planificación de roles de administrador de MBAM 1.0
author: dansimp
ms.assetid: 95be0eb4-25e9-43ca-a8e7-27373d35544d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 104d650824330ea990881c520a7811511f496dd1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825890"
---
# Planificación de roles de administrador de MBAM 1.0


En este tema se incluyen y describen los roles de administrador que están disponibles en administración y supervisión de Microsoft BitLocker (MBAM), así como las ubicaciones de servidor donde se crean los grupos locales.

## Roles de administrador de MBAM


<a href="" id="---------------mbam-system-administrators"></a> **Administradores del sistema MBAM**  
Los administradores de este rol tienen acceso a todas las características de MBAM. El grupo local para este rol está instalado en el servidor de supervisión y administración.

<a href="" id="---------------mbam-hardware-users"></a> **Usuarios de hardware de MBAM**  
Los administradores de este rol tienen acceso a las características de capacidad de hardware de MBAM. El grupo local para este rol está instalado en el servidor de supervisión y administración.

<a href="" id="---------------mbam-helpdesk-users"></a> **Usuarios de MBAM Helpdesk**  
Los administradores de este rol tienen acceso a las características del Departamento de soporte técnico de MBAM. El grupo local para este rol está instalado en el servidor de supervisión y administración.

<a href="" id="---------------mbam--report-users"></a> **Usuarios de informes de MBAM**  
Los administradores de este rol tienen acceso a la característica informes de cumplimiento y auditoría de MBAM. El grupo local para este rol está instalado en el servidor de administración y supervisión, la base de datos de cumplimiento y la auditoría, y en el servidor que hospeda los informes de cumplimiento y cumplimiento.

<a href="" id="---------------mbam--advanced-helpdesk-users"></a> **MBAM los usuarios avanzados del servicio de asistencia**  
Los administradores de este rol han aumentado el acceso a las características del Departamento de soporte técnico de MBAM. El grupo local para este rol está instalado en el servidor de supervisión y administración. Si un usuario es miembro de MBAM y usuarios del Departamento de soporte técnico avanzado, los permisos de los usuarios avanzados de soporte técnico de MBAM se sobrescribirán a los permisos de usuario de MBAM Helpdesk.

**Importante**  Para ver los informes, un usuario administrativo debe ser miembro del grupo de seguridad de **usuarios de informes de MBAM** en el servidor de administración y supervisión, la base de datos de cumplimiento y auditoría, y en el servidor que hospeda la característica de cumplimiento e informes. Como práctica recomendada, cree un grupo de seguridad en Active Directory con derechos en el grupo de seguridad local de **usuarios de MBAM** en el servidor de administración y supervisión, y en el servidor que hospeda el cumplimiento y los informes.

 

## Temas relacionados


[Preparación del entorno para MBAM 1.0](preparing-your-environment-for-mbam-10.md)

 

 





