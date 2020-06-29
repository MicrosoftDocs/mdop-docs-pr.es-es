---
title: Cómo administrar exenciones de cifrado de BitLocker de equipo
description: Cómo administrar exenciones de cifrado de BitLocker de equipo
author: dansimp
ms.assetid: d4400a0d-b36b-4cf5-a294-1f53ec47f9ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51b93061468508900eaee7fce8a7827e2db61d19
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825680"
---
# Cómo administrar exenciones de cifrado de BitLocker de equipo


La administración y supervisión de Microsoft BitLocker (MBAM) se puede usar para excluir determinados equipos de la protección de BitLocker. Por ejemplo, una organización puede decidir controlar la exención de BitLocker entre equipos.

Para eximir a un equipo del cifrado de BitLocker, debe agregar el equipo a un grupo de seguridad en ActiveDirectoryDomainServices para omitir las reglas de protección de BitLocker basadas en equipos.

**Nota:**  Si el equipo ya está protegido por BitLocker, la Directiva de exención de equipos no surte efecto.

 

**Para excluir un equipo del cifrado de BitLocker**

1.  Agregue la cuenta de equipo que desea que esté exenta a un grupo de seguridad en ActiveDirectoryDomainServices. Esto le permite omitir cualquier regla de protección de BitLocker basada en el equipo.

2.  Cree un objeto de directiva de grupo con la plantilla de directiva de grupo MBAM, a continuación, asocie el objeto de directiva de grupo con el grupo de Active Directory que creó en el paso anterior. Para obtener más información acerca de la creación de los objetos de directiva de grupo necesarios, consulte [implementar objetos de directiva de grupo de MBAM 1,0](deploying-mbam-10-group-policy-objects.md).

3.  Cuando se inicia un equipo excluido, el cliente de MBAM comprueba la configuración de la Directiva de exención de equipos y suspende la protección en función de si el equipo forma parte del grupo de seguridad de exención de BitLocker.

## Temas relacionados


[Administración de funciones de MBAM 1.0](administering-mbam-10-features.md)

 

 





