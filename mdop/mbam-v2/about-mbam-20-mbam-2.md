---
title: Acerca de MBAM 2.0
description: Acerca de MBAM 2.0
author: dansimp
ms.assetid: b43a0ba9-1c83-4854-a2c5-14eea0070e36
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7bdf24d1f375dd1fa8b18ac90c2fc49d2887c6c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824320"
---
# Acerca de MBAM 2.0


Microsoft BitLockerAdministration y Monitoring (MBAM) 2.0 proporciona una interfaz administrativa simplificada para el cifrado de unidad BitLocker. BitLocker ofrece una protección mejorada contra el robo de datos o la exposición de datos para equipos que se han perdido o robado. BitLocker cifra todos los datos que se almacenan en el volumen del sistema operativo Windows y en los volúmenes de datos configurados.

## Acerca de MBAM 2.0


BitLockerAdministration y Monitoring 2.0 exigen las opciones de directiva de cifrado de BitLocker que se establecen para su empresa, supervisa la compatibilidad de los equipos cliente con esas directivas e informa del estado de cifrado de los equipos de la empresa y de los usuarios individuales. Además, MBAM le permite acceder a la información de la clave de recuperación cuando los usuarios olvidan su PIN o su contraseña, o cuando cambia su BIOS o registro de inicio.

**Nota:**  BitLocker no se trata en detalle en esta guía. Para obtener información general sobre BitLocker, consulte [Introducción al cifrado de unidad BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).

 

Es posible que los siguientes grupos estén interesados en usar MBAM para administrar BitLocker:

-   Administradores, profesionales de la seguridad de ti y responsables del cumplimiento responsables de garantizar que los datos confidenciales no se revelen sin autorización

-   Administradores responsables de la seguridad del equipo en oficinas remotas o sucursales

-   Administradores responsables de equipos cliente que ejecutan Windows

## <a href="" id="what-s-new-in-mbam-2-0"></a>Novedades de MBAM 2.0


MBAM 2.0 ofrece las siguientes características y funcionalidades nuevas.

### Integración de System Center Configuration Manager con MBAM

MBAM ahora es compatible con la integración con System Center Configuration Manager. Esta integración mueve la infraestructura de cumplimiento de MBAM al entorno nativo de Configuration Manager. Los administradores de ti que usan el administrador de configuración en su empresa ahora pueden ver el estado de cumplimiento de su empresa en la consola de administración de Microsoft y profundizar en los informes para ver los equipos individuales.

### La compatibilidad de hardware solo está disponible en la topología de integración de Configuration Manager

La integración de Configuration Manager con MBAM permite que las funciones de Configuration Manager permitan o prohíban el uso de determinados tipos de hardware con MBAM y proporcionan más flexibilidad que la compatibilidad de hardware que estaba disponible en MBAM 1,0. Los administradores de TI pueden crear sus propias colecciones para limitar el hardware y pueden implementar la línea base de configuración MBAM en esas colecciones. La MBAM compatibilidad de hardware que estaba presente en MBAM 1,0 ahora solo está disponible en la topología del administrador de configuración de MBAM y se administra desde Configuration Manager.

### Directiva flexible de protectores

Los equipos que ya están cifrados con un protector (por ejemplo, TPM + PIN o el desbloqueo automático y la contraseña) y que reciben una directiva de MBAM que requiere un subconjunto de ese cifrado (por ejemplo, TPM o desbloqueo automático) se consideran conformes. En el ejemplo anterior, PIN y la contraseña no se eliminarán automáticamente a menos que el administrador de ti defina específicamente estas características como ya no permitidas.

Los equipos que no están cifrados y que reciben una directiva de MBAM (por ejemplo, TPM o desbloqueo automático) se cifran como corresponda. Los usuarios que son administradores locales pueden usar las herramientas de BitLocker (elemento del panel de control BitLocker Drive Encryption o Manage-BDE) para agregar o modificar los protectores existentes (por ejemplo, TPM + PIN o la opción de desbloqueo automático y contraseña). Seguirán siendo compatibles a menos que las directivas de MBAM específicamente las definan.

### Posibilidad de actualizar el cliente de MBAM

El Windows Installer del cliente de MBAM 2.0 detecta la versión del cliente existente y realiza los pasos necesarios para actualizar al cliente de MBAM 2.0 desde versiones anteriores.

### Capacidad de actualizar el servidor de MBAM desde versiones anteriores

Puede actualizar la infraestructura de servidor de MBAM 2.0 de versiones anteriores de MBAM de la siguiente manera:

**Sustitución de servidor manual local** : debe desinstalar manualmente la infraestructura de servidor de MBAM existente y, a continuación, instalar la infraestructura de servidor de MBAM 2,0. No es necesario quitar las bases de datos para realizar la actualización. En su lugar, seleccione las bases de datos existentes, que creó la versión anterior del cliente de MBAM. A continuación, la instalación de actualización de MBAM 2.0 migra las bases de datos existentes a MBAM 2,0.

**Actualización de cliente distribuido** : Si usa la topología de MBAM independiente, puede actualizar los clientes de MBAM gradualmente después de instalar la infraestructura de servidor de MBAM 2,0. El servidor de MBAM 2,0 detecta la versión del cliente existente y realiza los pasos necesarios para actualizar al cliente de 2,0.

Después de actualizar la infraestructura de servidor de MBAM 2,0, los clientes de MBAM 1,0 continúan reportando correctamente al servidor de MBAM 2,0, depósito de garantía de datos de recuperación, pero el cumplimiento se basará en las políticas de MBAM 1,0. Debe actualizar los clientes a MBAM 2,0 para que los equipos cliente notifiquen de forma precisa el cumplimiento de las directivas de MBAM 2,0. Puede actualizar los clientes al cliente de MBAM 2,0 sin desinstalar el cliente anterior y el cliente comenzará a aplicar y notificará las directivas de MBAM 2,0.

Si está usando MBAM con Configuration Manager, debe actualizar los clientes de MBAM 1,0 a MBAM 2,0.

### <a href="" id="mbam-support-for-bitlocker-s-enterprise-scenarios-on-the-windows-8-platform"></a>MBAM compatibilidad con los escenarios empresariales de BitLocker en la plataforma Windows 8

MBAM es compatible con el sistema operativo Windows 8 como plataforma de destino para la instalación del cliente de MBAM. Esta compatibilidad permite que los administradores de ti instalen el agente de MBAM, para cifrar las unidades del sistema operativo Windows 8 y para informar sobre el cumplimiento de los equipos. MBAM aprovecha el TPM y los protectores de TPM + PIN para administrar el sistema operativo Windows 8 de la misma forma que lo hace el sistema operativo Windows 7. MBAM 2.0 también agrega compatibilidad para cifrar los clientes de Windows to go.

### Adición del portal de autoservicio

Los usuarios finales pueden usar ahora el portal de autoservicio para recuperar sus claves de recuperación. El portal de autoservicio se puede implementar en un solo servidor con las otras características de MBAM o en un servidor independiente que proporciona a los administradores de ti la flexibilidad de exponer el portal de autoservidor a los usuarios, según sea necesario. Después de que el portal de autoservicio autentique a los usuarios, los usuarios solo tienen que escribir los primeros ocho dígitos de la identificación de la clave de recuperación para recibir su clave de recuperación.

MBAM también protege la clave permitiendo a los usuarios recuperar claves solo para los equipos en los que son usuarios, lo que reduce el riesgo de que otros usuarios obtengan acceso no autorizado.

### Capacidad para reanudar automáticamente la protección de BitLocker desde un estado suspendido

MBAM ya no permite que los administradores de TI mantengan BitLocker suspendido y desprotegido durante períodos prolongados. Si un administrador de ti suspende BitLocker, MBAM vuelve a habilitarlo automáticamente cuando se reinicia el equipo, lo que reduce el riesgo de que el equipo pueda ser atacado.

### Las unidades de datos fijas se pueden configurar para que se desbloqueen automáticamente sin contraseña

Una directiva de unidad de datos fija (FDD) ya puede configurarse para permitir el desbloqueo automático de la unidad sin una contraseña. A los usuarios no se les pide una contraseña antes de que se cifre la DISQUETERA, y la DISQUETERA se protegerá y se desbloqueará automáticamente con la unidad del sistema operativo.

## <a href="" id="---------mbam-2-0-release-notes"></a> Notas de la versión de MBAM 2.0


Para obtener más información y para obtener noticias de última hora que no se incluyen en la documentación, consulte las [notas de la versión de MBAM 2,0](release-notes-for-mbam-20-mbam-2.md).

## Cómo obtener MBAM 2.0


Esta tecnología es parte del paquete de optimización de escritorio de Microsoft (MDOP). Los clientes empresariales pueden obtener MDOP con Microsoft Software Assurance. Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte [¿Cómo puedo obtener MDOP?](https://go.microsoft.com/fwlink/p/?LinkId=322049)

## Temas relacionados


[Introducción a MBAM 2.0](getting-started-with-mbam-20-mbam-2.md)

 

 





