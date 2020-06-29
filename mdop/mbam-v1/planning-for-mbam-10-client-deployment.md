---
title: Planificación para la implementación de clientes de MBAM 1.0
description: Planificación para la implementación de clientes de MBAM 1.0
author: dansimp
ms.assetid: 3af2e7f3-134b-4ab9-9847-b07474ca6ac3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d58d6420febd2da9ee9cd4074fc8b5870285b0b4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825880"
---
# Planificación para la implementación de clientes de MBAM 1.0


Según el momento en que implemente el cliente de administración y supervisión de Microsoft BitLocker (MBAM), puede habilitar el cifrado de BitLocker en un equipo de su organización, ya sea antes de que el usuario final reciba el equipo o posteriormente. Para habilitar el cifrado de BitLocker después de que el usuario final reciba el equipo, configure la Directiva de grupo. Para habilitar el cifrado de BitLocker antes de que el usuario final reciba el equipo, implemente el software de cliente de MBAM mediante un sistema de implementación de software empresarial.

Puede usar uno de los métodos o ambos en su organización. Si usa ambos métodos, puede mejorar la compatibilidad, la elaboración de informes y la compatibilidad de recuperación de claves.

**Nota:**  Para consultar los requisitos del sistema del cliente de MBAM, consulte [configuraciones compatibles con MBAM 1,0](mbam-10-supported-configurations.md).

 

## Implementar el cliente MBAM para habilitar el cifrado de BitLocker después de la distribución de equipos a los usuarios finales


Después de configurar la Directiva de grupo, puede usar un producto de sistema de implementación de software empresarial, como Microsoft System Center Configuration Manager 2012 o servicios de dominio de Active Directory, para implementar los archivos de Windows Installer de la instalación de cliente MBAM en los equipos de destino. Los dos archivos de Windows Installer de la instalación de cliente de MBAM son MBAMClient-64bit.msi y MBAMClient-32bit.msi, que se proporcionan con el software MBAM. Para obtener más información sobre cómo implementar MBAM objetos de directiva de grupo, consulte [implementar objetos de directiva de grupo de MBAM 1,0](deploying-mbam-10-group-policy-objects.md).

Al implementar el cliente MBAM, después de distribuir los equipos a los usuarios finales, se pide a los usuarios finales que cifren sus equipos. Esto le permite a MBAM recopilar los datos, incluir el PIN y la contraseña y, a continuación, comenzar el proceso de cifrado.

**Nota:**  En este enfoque, a los usuarios se les pide activar e inicializar el chip módulo de plataforma segura (TPM), si aún no se ha activado.

 

## Usar el cliente MBAM para habilitar el cifrado de BitLocker antes de la distribución de equipos a usuarios finales


En las organizaciones donde los equipos se reciben y configuran de forma centralizada, puede instalar el cliente de MBAM para administrar el cifrado de BitLocker en cada equipo antes de que se escriban datos de usuario en él. La ventaja de este proceso es que cada equipo será compatible con el cifrado de BitLocker. Este método no depende de la acción del usuario porque el administrador ya cifró el equipo. Una de las suposiciones clave para este escenario es que la Directiva de la organización instala una imagen de Windows corporativa antes de que el equipo se entregue al usuario.

Si su organización quiere usar (TPM) para cifrar equipos, el administrador debe cifrar el volumen del sistema operativo del equipo con el protector TPM. Si su organización desea usar el chip de TPM y un protector de PIN, el administrador debe cifrar el volumen del sistema con el protector TPM y, a continuación, los usuarios seleccionan un PIN la primera vez que inician sesión. Si su organización decide usar solo el protector del PIN, el administrador no tiene que cifrar el volumen en primer lugar. Cuando los usuarios inician sesión en sus equipos, MBAM les pide que proporcionen un PIN o un PIN y una contraseña que usarán cuando reinicien su equipo más tarde.

**Nota:**  La opción de protector del TPM requiere que el administrador acepte el indicador BIOS para activar e inicializar TPM antes de entregar el equipo al usuario.

 

## Temas relacionados


[Planificar la implementación de MBAM 1.0](planning-to-deploy-mbam-10.md)

[Implementación de cliente de MBAM 1.0](deploying-the-mbam-10-client.md)

 

 





