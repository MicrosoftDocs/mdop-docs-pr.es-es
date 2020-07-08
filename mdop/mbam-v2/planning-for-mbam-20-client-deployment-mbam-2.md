---
title: Planeación para la implementación de clientes de MBAM 2.0
description: Planeación para la implementación de clientes de MBAM 2.0
author: dansimp
ms.assetid: 3a92cf29-092f-4cad-bdfa-d5f6aafe554b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c3a7383188d4064247d8e493c8e6125fc24a1d2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812622"
---
# Planeación para la implementación de clientes de MBAM 2.0


Según el momento en que implemente el cliente de administración y supervisión de Microsoft BitLocker (MBAM), puede habilitar el cifrado de unidad BitLocker en un equipo de su organización, ya sea antes de que el usuario final reciba el equipo o posteriormente. Tanto para la MBAM independiente como para las topologías de Configuration Manager, debe configurar la configuración de directiva de grupo para MBAM.

Si está usando la topología independiente MBAM, le recomendamos que use un sistema de implementación de software empresarial para implementar el software de cliente de MBAM en equipos de usuario final.

Si implementa MBAM con la topología de Configuration Manager, puede usar Configuration Manager para implementar el software de cliente de MBAM en equipos de usuario final. En el administrador de configuración, la instalación de MBAM crea una colección de equipos que MBAM puede administrar. Esta colección incluye estaciones de trabajo y dispositivos que no tienen un módulo de plataforma segura (TPM), pero que ejecutan Windows 8.

**Nota:**  Windows to go no es compatible con las instalaciones integradas de Configuration Manager de MBAM si está usando Configuration Manager 2007.

 

## Implementar el cliente MBAM para habilitar el cifrado de BitLocker después de la distribución de equipos a los usuarios finales


Después de configurar la Directiva de grupo, puede usar un producto del sistema de implementación de software empresarial como Microsoft System Center Configuration Manager o servicios de dominio de Active Directory (AD DS) para implementar los archivos de Windows Installer de la instalación del cliente de MBAM en los equipos de destino. Para implementar el cliente MBAM, puede usar los archivos de 32 o 64 bits de MbamClientSetup.exe o MBAMClient.msi, que se proporcionan con el software MBAM.

Al implementar el cliente de MBAM después de distribuir los equipos a los equipos cliente, se pide a los usuarios finales que cifren su equipo. Esto permite que MBAM recopile los datos, que incluyen el PIN y la contraseña y, a continuación, comenzar el proceso de cifrado.

**Nota:**  En este enfoque, se pide a los usuarios que tengan equipos con un chip de TPM activar e inicializar el chip de TPM si el chip no se ha activado previamente.

 

## Usar el cliente MBAM para habilitar el cifrado de BitLocker antes de la distribución de equipos a usuarios finales


En las organizaciones donde los equipos se reciben y configuran de forma centralizada y donde los equipos tienen un chip TPM compatible, puede instalar el cliente MBAM para administrar el cifrado de BitLocker en cada equipo antes de que se escriban datos de usuario. La ventaja de este proceso es que cada equipo será compatible con el cifrado de BitLocker. Este método no depende de la acción del usuario porque el administrador ya cifró el equipo. Una de las suposiciones clave para este escenario es que la Directiva de la organización instala una imagen de Windows corporativa antes de que el equipo se entregue al usuario.

Si su organización desea usar el chip TPM para cifrar los equipos, el administrador agrega el protector TPM para cifrar el volumen del sistema operativo del equipo. Si su organización desea usar el chip de TPM y un protector de PIN, el administrador cifra el volumen del sistema operativo con el protector de TPM y, a continuación, los usuarios seleccionan un PIN cuando inician sesión por primera vez. Si su organización decide usar solo el protector del PIN, el administrador no tiene que cifrar el volumen en primer lugar. Cuando los usuarios inician sesión, administración y supervisión de Microsoft BitLocker les pide que proporcionen un PIN, o un PIN y una contraseña para usarlos en posteriores reinicios del equipo.

**Nota:**  La opción de protector TPM requiere que el administrador acepte el indicador de BIOS para activar e inicializar TPM antes de que el equipo se entregue al usuario.

 

## Temas relacionados


[Planificación de la implementación de MBAM 2.0](planning-to-deploy-mbam-20-mbam-2.md)

[Implementación de cliente de MBAM 2.0](deploying-the-mbam-20-client-mbam-2.md)

 

 





