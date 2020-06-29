---
title: Cómo administrar los roles de administrador de MBAM
description: Cómo administrar los roles de administrador de MBAM
author: dansimp
ms.assetid: 813ac0c4-3cf9-47af-b4cb-9395fd915e5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14e9128904b448b20e0596a2630627b7ca8e711d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825120"
---
# Cómo administrar los roles de administrador de MBAM


Una vez completada la configuración administración y supervisión de Microsoft BitLocker (MBAM) para todas las características del servidor, los usuarios administrativos tendrán que tener permiso de acceso. Como práctica recomendada, los administradores que administrarán o usarán las características de servidor de supervisión y administración de Microsoft BitLocker deben asignarse a grupos de seguridad de servicios de dominio y, después, esos grupos deben agregarse al grupo local administrativo de MBAM correspondiente.

**Para administrar MBAM pertenencias a roles de administrador**

1.  Asignar usuarios administrativos a grupos de seguridad en servicios de dominio de ActiveDirectory.

2.  Agregue grupos de seguridad de ActiveDirectory a los roles de los grupos locales administrativos de MBAM en el servidor de MBAM para las características respectivas.

    -   **MBAM los administradores del sistema** tienen acceso a todas las características de MBAM en el sitio web de administración y supervisión de MBAM.

    -   **Los usuarios del Departamento de soporte técnico de MBAM** tienen acceso a las opciones administrar TPM y recuperación de unidades en el sitio web de administración y supervisión de MBAM, pero deben rellenar todos los campos cuando usen ambas opciones.

    -   **Los usuarios de informes de MBAM** tienen acceso a los informes de cumplimiento y cumplimiento en el sitio web de administración y supervisión de MBAM.

    -   **Los usuarios avanzados de MBAM** tienen acceso a las opciones administrar TPM y recuperación de unidades en el sitio web de administración y supervisión de MBAM, pero no necesitan rellenar todos los campos cuando usan ambas opciones.

    Para obtener más información acerca de los roles de administración y supervisión de Microsoft BitLocker, consulte [roles de planeación de MBAM 2,0](planning-for-mbam-20-administrator-roles-mbam-2.md).

## Temas relacionados


[Administración de funciones de MBAM 2.0](administering-mbam-20-features-mbam-2.md)

 

 





