---
title: Cómo implementar al cliente MBAM como parte de una implementación de Windows
description: Cómo implementar al cliente MBAM como parte de una implementación de Windows
author: dansimp
ms.assetid: 8704bf33-535d-41da-b9b2-45b60754367e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a63311bcc93d84472ceff5c80c9222fefd5445c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824911"
---
# Cómo implementar al cliente MBAM como parte de una implementación de Windows


El cliente de administración y supervisión de Microsoft BitLocker permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa. El cliente de BitLocker se puede integrar en una organización al habilitar el cifrado y la administración de BitLocker en equipos cliente durante el proceso de creación de imágenes de equipos y de Windows.

**Nota**  
Para consultar los requisitos del sistema del cliente de MBAM, consulte [configuraciones compatibles con MBAM 1,0](mbam-10-supported-configurations.md).



El cifrado de equipos cliente con BitLocker durante la fase de creación de imágenes inicial de una implementación de Windows puede reducir la sobrecarga administrativa de la implementación de MBAM. Este enfoque también garantiza que todos los equipos que se implementan ya tengan BitLocker ejecutándose y que estén configurados correctamente.

**Advertencia**  
En este tema se describe cómo cambiar el registro de Windows mediante el editor del registro. Si cambia incorrectamente el registro de Windows, puede causar serios problemas que le obliguen a reinstalar Windows. Debe hacer una copia de seguridad de los archivos de registro (System. dat y User. dat) antes de cambiar el registro. Microsoft no puede garantizar que los problemas que puedan surgir al cambiar el registro se puedan resolver. Cambie el registro bajo su propia responsabilidad.



**Para cifrar un equipo como parte de la implementación de Windows**

1.  Si su organización planea usar el protector módulo de plataforma segura (TPM) o las opciones de protector de TPM + PIN en BitLocker, debe activar el chip TPM antes de la implementación inicial de MBAM. Al activar el chip de TPM, se evita el reinicio más adelante en el proceso y se asegura de que los chips de TPM se hayan configurado correctamente de acuerdo con los requisitos de la organización. Debe activar el chip TPM manualmente en el BIOS del equipo. Para obtener más información sobre cómo configurar el chip de TPM, consulte la documentación del fabricante.

2.  Instale el agente de cliente de MBAM.

3.  Le recomendamos que se una al equipo a un dominio...

    -   Si el equipo no se ha unido a un dominio, la contraseña de recuperación no se almacena en el servicio de recuperación de claves de MBAM. De forma predeterminada, MBAM no permite que se produzca el cifrado, a menos que se pueda almacenar la clave de recuperación.

    -   Si un equipo se inicia en el modo de recuperación antes de que se almacene la clave de recuperación en el servidor de MBAM, el equipo tiene que recrear la imagen. No hay ningún método de recuperación disponible.

4.  Abra un símbolo del sistema como administrador, detenga el servicio MBAM y, a continuación, configure el servicio como **manual** o a **petición**. A continuación, ejecute los siguientes comandos:

    **net stop mbamagent**

    **SC config mbamagent Start = Demand**

5.  Establezca la configuración del registro para que el agente de MBAM ignore la Directiva de grupo y ejecute el TPM para el **cifrado solo del sistema operativo** para ello, ejecute **regedit**y, a continuación, importe la plantilla de clave del registro de c:\\Archivos de Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

6.  En regedit, vaya a HKLM\\SOFTWARE\\Microsoft\\MBAM y configure las opciones que se indican en la tabla siguiente.

    Entrada del registro

    Opciones de configuración

    DeploymentTime

    0 = DESHABILITADO

    1 = usar la configuración de directiva de tiempo de implementación (valor predeterminado)

    UseKeyRecoveryService

    0 = no usar custodia de claves (en este caso, no se necesitan las dos siguientes entradas de registro).

    1 = usar custodia de clave en el sistema de recuperación de claves (predeterminado)

    Recomendado: el equipo debe poder comunicarse con el servicio de recuperación de claves. Compruebe que el equipo puede comunicarse con el servicio antes de continuar.

    KeyRecoveryOptions

    0 = cargar solo la clave de recuperación

    1 = cargar la clave de recuperación y el paquete de recuperación de claves (predeterminado)

    KeyRecoveryServiceEndPoint

    Establezca este valor en la dirección URL del servidor Web de recuperación de claves.

    Ejemplo: http:// &lt; nombre de equipo &gt; /MBAMRecoveryAndHardwareService/CoreService.SVC.



~~~
**Note**  
MBAM policy or registry values can be set here to override the previously set values.
~~~



7. El agente de MBAM reinicia el sistema durante la implementación de cliente de MBAM. Cuando esté listo para este reinicio, ejecute el comando siguiente en un símbolo del sistema como administrador:

   **net start mbamagent**

8. Cuando se reinicien los equipos y el BIOS le solicite que acepte un cambio de TPM, acepte el cambio.

9. Durante el proceso de creación de imágenes del sistema operativo de cliente Windows, cuando esté listo para iniciar el cifrado, reinicie el servicio agente de MBAM. Después, para establecer Inicio en **automático**, abra un símbolo del sistema como administrador y ejecute los siguientes comandos:

   **SC config mbamagent Start = Auto**

   **net start mbamagent**

10. Quite los valores de omisión del registro. Para ello, ejecute regedit, vaya a la entrada del registro HKLM\\SOFTWARE\\Microsoft, haga clic con el botón secundario en el nodo **MBAM** y, a continuación, haga clic en **eliminar**.

## Temas relacionados


[Implementación de cliente de MBAM 1.0](deploying-the-mbam-10-client.md)









