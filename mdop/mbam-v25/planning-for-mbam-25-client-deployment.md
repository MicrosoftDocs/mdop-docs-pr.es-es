---
title: Planificación para la implementación de clientes de MBAM 2.5
description: Planificación para la implementación de clientes de MBAM 2.5
author: dansimp
ms.assetid: 23c89976-af24-4753-9412-ce0ea42d1964
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ff03b58da0985b2f57308c99a9bc15f4a0554623
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825991"
---
# Planificación para la implementación de clientes de MBAM 2.5


Según el momento en que implemente el software de cliente de supervisión y administración de Microsoft BitLocker (MBAM), puede habilitar el cifrado de unidad BitLocker en un equipo de su organización antes de que el usuario final reciba el equipo o posteriormente. Tanto para la MBAM independiente como para las topologías de integración de System Center Configuration Manager, tiene que establecer la configuración de la Directiva de grupo para MBAM.

Si está usando la topología independiente MBAM, le recomendamos que use un sistema de implementación de software empresarial para implementar el software de cliente de MBAM en equipos de usuario final.

Si implementa MBAM con la topología de integración de Configuration Manager, puede usar Configuration Manager para implementar el software de cliente de MBAM en equipos de usuario final. En el administrador de configuración, la instalación de MBAM crea una colección de equipos que MBAM puede administrar. Esta colección incluye estaciones de trabajo y dispositivos que no tienen un módulo de plataforma segura (TPM), pero que ejecutan Windows 8, Windows 8,1 o Windows 10.

**Nota:**  Windows to go no es compatible con la instalación de la topología de integración de Configuration Manager al usar el administrador de configuración 2007.

 

## Implementar el cliente MBAM para habilitar el cifrado de unidad BitLocker después de la distribución de equipos a usuarios finales


Después de configurar la Directiva de grupo, puede usar un producto del sistema de implementación de software empresarial como Microsoft System Center Configuration Manager o servicios de dominio de Active Directory (AD DS) para implementar los archivos de Windows Installer de la instalación del cliente de MBAM en los equipos de destino. Para implementar el cliente MBAM, puede usar los archivos de 32 o 64 bits de MbamClientSetup.exe o MBAMClient.msi, que se proporcionan con el software de cliente de MBAM.

**Nota:**  A partir de MBAM 2,5 SP1, ya no se incluye un MSI aparte con el producto MBAM. Sin embargo, puede extraer el MSI del archivo ejecutable (. exe) que se incluye con el producto.

 

Al implementar el cliente de MBAM después de distribuir los equipos a los equipos cliente, se pide a los usuarios finales que cifren su equipo. Esta acción permite que MBAM recopile los datos, lo que incluye el PIN y la contraseña (si lo exige la Directiva) y, a continuación, iniciar el proceso de cifrado.

**Nota:**  En este enfoque, se pide a los usuarios finales que tengan equipos con un chip de TPM activar e inicializar el chip de TPM si el chip no se ha activado previamente.

 

## Usar el cliente MBAM para habilitar el cifrado de unidad BitLocker antes de la distribución de equipos a usuarios finales


En las organizaciones donde los equipos se reciban y configuren de forma centralizada y donde los equipos tengan un chip TPM compatible, puede usar el cliente de MBAM para administrar el cifrado de unidad BitLocker en cada equipo antes de que se escriban datos de usuario. La ventaja de este proceso es que cada equipo es compatible. Este método no depende de la acción del usuario final porque el administrador ya cifró el equipo. Una de las suposiciones clave para este escenario es que la Directiva de la organización instala una imagen de Windows corporativa antes de que el equipo se entregue al usuario final.

Si su organización desea usar el chip TPM para cifrar los equipos, el administrador agrega el protector TPM para cifrar el volumen del sistema operativo del equipo. Si su organización desea usar el chip TPM y un protector con PIN, el administrador cifra el volumen del sistema operativo con el protector TPM y, a continuación, los usuarios finales seleccionan un PIN cuando inician sesión por primera vez. Si su organización decide usar solo el protector del PIN, el administrador no tiene que cifrar el volumen en primer lugar. Cuando los usuarios finales inicien sesión, la administración y la supervisión de Microsoft BitLocker les pedirá que proporcionen un PIN, o un PIN y una contraseña para usarlos en posteriores reinicios del equipo.

**Nota:**  La opción de protector TPM requiere que el administrador acepte el indicador de BIOS para activar e inicializar TPM antes de que el equipo se entregue al usuario final.

 

## Compatibilidad con el cliente de MBAM para unidades de disco duro cifradas


MBAM es compatible con BitLocker en unidades de disco duro cifradas que cumplen los requisitos de especificación de TCG para Opal y las normas IEEE 1667. Cuando BitLocker está habilitado en estos dispositivos, generará claves y realizará funciones de administración en la unidad cifrada. Para obtener más información, consulta [unidad de disco duro cifrada](https://technet.microsoft.com/library/hh831627.aspx) .


## Temas relacionados


[Planificación de implementación de MBAM 2.5](planning-to-deploy-mbam-25.md)

[Implementación de cliente de MBAM 2.5](deploying-the-mbam-25-client.md)

 

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




