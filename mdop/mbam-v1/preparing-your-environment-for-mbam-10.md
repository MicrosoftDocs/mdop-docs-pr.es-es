---
title: Preparación del entorno para MBAM 1.0
description: Preparación del entorno para MBAM 1.0
author: dansimp
ms.assetid: 915f7c3c-70ad-4a90-a434-73e7fba97ecb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9a2de4e825d5c89aeabcf57d78dc856bacb03e11
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823191"
---
# Preparación del entorno para MBAM 1.0


Antes de empezar la configuración de administración y supervisión de Microsoft BitLocker (MBAM), asegúrese de cumplir los requisitos previos necesarios para instalar el producto. Si conoce los requisitos previos previamente, puede implementar el producto de forma eficaz y habilitar sus características, que pueden admitir los objetivos empresariales de su organización de forma más eficaz.

## Revisar los requisitos previos de implementación de MBAM 1,0


El cliente MBAM y cada una de las características de servidor de MBAM tienen requisitos previos específicos que deben cumplirse para poder instalarse correctamente.

Para garantizar una instalación correcta de los clientes de MBAM y las características de MBAM Server, debe asegurarse de que la instalación de las características de los equipos especificados para MBAM cliente o MBAM Server se haya preparado correctamente para la configuración de MBAM.

**Nota:**  El programa de instalación de MBAM verifica si se cumplen todos los requisitos previos antes de que se inicie la instalación. Si no se cumplen, se producirá un error en la instalación.

 

[Requisitos previos de implementación de MBAM 1.0](mbam-10-deployment-prerequisites.md)

## Plan for MBAM 1,0 requisitos de la Directiva de grupo


Antes de que MBAM pueda administrar clientes en la empresa, debe definir la Directiva de grupo para los requisitos de cifrado de su entorno.

**Importante**  MBAM no funcionará con directivas para el cifrado de unidad BitLocker independiente. La Directiva de grupo debe definirse para MBAM; de lo contrario, se producirá un error en el cifrado y la aplicación de BitLocker.

 

[Planificación de los requisitos de directiva de grupo de MBAM 1.0](planning-for-mbam-10-group-policy-requirements.md)

## Planear los roles de administrador de MBAM 1,0


Los roles de administrador de MBAM se administran por grupos locales creados por el programa de instalación de MBAM al instalar lo siguiente: servidor de administración y administración de BitLocker, la característica informes de cumplimiento y de auditoría, y la base de datos de estado de cumplimiento y auditoría.

La pertenencia de roles de MBAM se puede administrar más eficazmente si crea grupos de seguridad en ActiveDirectoryDomainServices, agrega las cuentas de administrador apropiadas a esos grupos y, a continuación, agrega esos grupos de seguridad a los grupos locales de MBAM. Para obtener más información, consulte [Cómo administrar los roles de administrador de MBAM](how-to-manage-mbam-administrator-roles-mbam-1.md).

[Planificación de roles de administrador de MBAM 1.0](planning-for-mbam-10-administrator-roles.md)

## Otros recursos para la planeación de MBAM


[Planificación para MBAM 1.0](planning-for-mbam-10.md)

 

 





