---
title: Preparación del entorno para MBAM 2.0
description: Preparación del entorno para MBAM 2.0
author: dansimp
ms.assetid: 5fb01da9-620e-4992-9e54-2ed3fb69e6af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f1be989112d456064db302952d50159d00b5597a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825610"
---
# Preparación del entorno para MBAM 2.0


Antes de empezar la configuración de administración y supervisión de Microsoft BitLocker (MBAM), debe asegurarse de que cumple los requisitos previos para instalar el producto. Cuando sepa Cuáles son los requisitos previos, puede implementar el producto de forma eficaz y habilitar sus características para que sea más eficaz la compatibilidad de los objetivos empresariales de su organización.

Si implementa la administración y administración de Microsoft BitLocker con Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager, consulte [planificación para implementar MBAM con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

## Revisar los requisitos previos de implementación de MBAM 2,0


El cliente MBAM y cada una de las características de servidor de MBAM tienen requisitos previos específicos que deben cumplirse para poder instalarse correctamente.

Para garantizar una instalación correcta de los clientes de MBAM y las características de MBAM Server, asegúrese de que los equipos especificados para la instalación de características de servidor o cliente de MBAM MBAM se hayan preparado correctamente para la configuración de MBAM.

**Nota:**  El programa de instalación de MBAM verifica que se cumplan todos los requisitos previos antes de que se inicie la instalación. Si no se cumplen todos los requisitos previos, se producirá un error en la instalación.

 

[Requisitos previos de implementación de MBAM 2.0](mbam-20-deployment-prerequisites-mbam-2.md)

## Plan for MBAM 2,0 requisitos de la Directiva de grupo


Antes de que MBAM pueda administrar clientes en la empresa, debe definir una directiva de grupo para los requisitos de cifrado de su entorno.

**Importante**  MBAM no funcionará con directivas para el cifrado de unidad BitLocker independiente. Es necesario definir la configuración de la Directiva de grupo para MBAM, o el cifrado y la aplicación de BitLocker producirán errores.

 

[Planificación de los requisitos de directiva de grupo de MBAM 2.0](planning-for-mbam-20-group-policy-requirements-mbam-2.md)

## Planear los roles de administrador de MBAM 2,0


Los roles de administrador de MBAM se administran por grupos locales creados por el programa de instalación de MBAM al instalar el servidor de administración y administración de BitLocker, la característica informes de cumplimiento y de auditoría, y la base de datos de estado de cumplimiento y auditoría.

La pertenencia a los roles de administración y supervisión de Microsoft BitLocker puede administrarse mejor creando grupos de seguridad en ActiveDirectoryDomainServices, agregando las cuentas de administrador adecuadas a esos grupos y, a continuación, agregando esos grupos de seguridad a los grupos locales administración y supervisión de BitLocker. Para obtener más información, consulte [Cómo administrar los roles de administrador de MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).

## Otros recursos para la planeación de MBAM


[Planificación para MBAM 2.0](planning-for-mbam-20-mbam-2.md)

[Configuraciones admitidas de MBAM 2.0](mbam-20-supported-configurations-mbam-2.md)

 

 





