---
title: Cómo administrar los roles de administrador de MBAM
description: Cómo administrar los roles de administrador de MBAM
author: dansimp
ms.assetid: c0f25a42-dbff-418d-a776-4fe23ee07d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d00b8ebf66d2b066afae33e67298691285ce9fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812967"
---
# Cómo administrar los roles de administrador de MBAM


Una vez completada la configuración administración y supervisión de Microsoft BitLocker (MBAM) para todas las características del servidor, se debe conceder acceso a los usuarios administrativos a estas características de servidor. Como práctica recomendada, los administradores que administrarán o usarán características de servidor de MBAM se deben asignar a grupos de seguridad de Active Directory y, a continuación, esos grupos deben agregarse al grupo local administrativo de MBAM adecuado.

**Para administrar MBAM pertenencias a roles de administrador**

1.  Asignar usuarios administrativos a grupos de seguridad en servicios de ActiveDirectoryDomain.

2.  Agregue los grupos de seguridad servicios de ActiveDirectoryDomain a los roles de MBAM grupos locales administrativos en el servidor administración y supervisión de Microsoft BitLocker para las características respectivas. Los roles de usuario son los siguientes:

    -   **MBAM los administradores del sistema** tienen acceso a todas las características de supervisión y administración de Microsoft BitLocker en el sitio web de administración de MBAM.

    -   **Los usuarios de hardware de MBAM** tienen acceso a las características de compatibilidad de hardware en el sitio web de administración de MBAM.

    -   **MBAM los usuarios del Departamento de soporte** tienen acceso a las opciones administrar TPM y recuperación de unidades en el sitio web de administración de MBAM, pero deben rellenar todos los campos cuando usen ambas opciones.

    -   **Los usuarios de informes de MBAM** tienen acceso a los informes de cumplimiento y cumplimiento en el sitio web de administración de MBAM.

    -   **MBAM uso avanzado de los departamentos de soporte técnico** tienen acceso a las opciones administrar TPM y recuperación de unidades en el sitio web de administración de MBAM. No es necesario que estos usuarios rellenen todos los campos cuando usan una de las dos opciones.

    Para obtener más información acerca de los roles de administración y supervisión de Microsoft BitLocker, consulte [roles de planeación de MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

## Temas relacionados


[Administración de funciones de MBAM 1.0](administering-mbam-10-features.md)

 

 





