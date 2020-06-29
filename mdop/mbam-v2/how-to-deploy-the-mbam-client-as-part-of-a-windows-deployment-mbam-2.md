---
title: Cómo implementar al cliente MBAM como parte de una implementación de Windows
description: Cómo implementar al cliente MBAM como parte de una implementación de Windows
author: dansimp
ms.assetid: 67387de7-8b02-4412-9850-3b8d8e5c18af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d75e5748167d2d4866f98e9d3611584067ecd418
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824621"
---
# Cómo implementar al cliente MBAM como parte de una implementación de Windows


El cliente de administración y supervisión de Microsoft BitLocker permite a los administradores exigir y supervisar el cifrado de unidad BitLocker en equipos de la empresa. Si los equipos tienen un chip de módulo de plataforma segura (TPM), el cliente de BitLocker se puede integrar en una organización habilitando la administración de BitLocker y el cifrado en los equipos cliente como parte del proceso de implementación de imágenes y ventanas.

**Nota**  
Para revisar los requisitos del sistema cliente de administración y supervisión de Microsoft BitLocker, consulte [configuraciones admitidas de MBAM 2,0](mbam-20-supported-configurations-mbam-2.md).



El cifrado de equipos cliente con BitLocker durante la fase inicial de creación de la imagen de una implementación de Windows puede reducir el overhead administrativo necesario para implementar MBAM en una organización. También garantiza que todos los equipos que se implementan ya tengan BitLocker ejecutándose y que estén configurados correctamente.

**Nota**  
En el procedimiento de este tema se describe cómo modificar el registro de Windows. El uso incorrecto del editor del registro puede causar serios problemas que le obliguen a reinstalar Windows. Microsoft no puede garantizar la solución de los problemas resultantes del uso incorrecto del editor del registro. Use el editor del registro bajo su propia responsabilidad.



**Para cifrar un equipo como parte de la implementación de Windows**

1.  Si su organización planea usar el protector módulo de plataforma segura (TPM) o las opciones de protector de TPM + PIN en BitLocker, debe activar el chip TPM antes de la implementación inicial de MBAM. Al activar el chip de TPM, se evita el reinicio más adelante en el proceso y se asegura de que los chips de TPM se hayan configurado correctamente de acuerdo con los requisitos de la organización. Debe activar el chip TPM manualmente en el BIOS del equipo.

    **Nota**  
    Algunos proveedores proporcionan herramientas para activar y activar el chip TPM en el BIOS desde el sistema operativo. Para obtener más información sobre cómo configurar el chip de TPM, consulte la documentación del fabricante.



2.  Instale el agente del cliente de administración y supervisión de Microsoft BitLocker.

3.  Unir el equipo a un dominio (recomendado).

    -   Si el equipo no se une al dominio, la contraseña de recuperación no se almacena en el servicio de recuperación de claves de MBAM. De forma predeterminada, MBAM no permite que se produzca el cifrado, a menos que se pueda almacenar la clave de recuperación.

    -   Si un equipo se inicia en el modo de recuperación antes de que se almacene la clave de recuperación en el servidor de MBAM, el equipo tiene que recrear la imagen. No hay ningún método de recuperación disponible.

4.  Ejecute el símbolo del sistema como administrador, detenga el servicio MBAM y, a continuación, establezca el servicio en **manual** o a **petición**y, a continuación, empiece a escribir los comandos siguientes:

    **net stop mbamagent**

    **SC config mbamagent Start = Demand**

5.  Establezca la configuración del registro para que el agente de MBAM ignore la Directiva de grupo y ejecute el TPM para el **cifrado solo del sistema operativo** ejecutando **regedit**y, a continuación, importando la plantilla de clave del registro de c:\\Archivos de Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

6.  En regedit, vaya a HKLM\\SOFTWARE\\Microsoft\\MBAM y configure las opciones que se indican en la tabla siguiente.

    Entrada del registro

    Opciones de configuración

    DeploymentTime

    0 = DESHABILITADO

    1 = usar la configuración de directiva de tiempo de implementación (valor predeterminado)

    UseKeyRecoveryService

    0 = no usar custodia de claves (en este caso, no se necesitan las dos siguientes entradas de registro)

    1 = usar custodia de clave en el sistema de recuperación de claves (predeterminado)

    Recomendado: el equipo debe poder comunicarse con el servicio de recuperación de claves. Compruebe que el equipo puede comunicarse con el servicio antes de continuar.

    KeyRecoveryOptions

    0 = solo carga la clave de recuperación

    1 = carga de clave de recuperación y paquete de recuperación de claves (predeterminado)

    KeyRecoveryServiceEndPoint

    Establezca este valor en la dirección URL del servidor Web de recuperación de claves, por ejemplo, http:// &lt; nombre de equipo &gt; /MBAMRecoveryAndHardwareService/CoreService.SVC.



~~~
**Note**  
MBAM policy or registry values can be set here to override previously set values.
~~~



7. El agente de MBAM reinicia el sistema durante la implementación de cliente de MBAM. Cuando esté listo para este reinicio, ejecute el comando siguiente en un símbolo del sistema como administrador:

   **net start mbamagent**

8. Cuando se reinicien los equipos y el BIOS le solicite que acepte un cambio de TPM, acepte el cambio.

9. Durante el proceso de creación de imágenes del sistema operativo de cliente Windows, cuando esté listo para iniciar el cifrado, reinicie el servicio agente de MBAM y establezca iniciar en **automático** ejecutando un símbolo del sistema como administrador y escribiendo los siguientes comandos:

   **SC config mbamagent Start = Auto**

   **net start mbamagent**

10. Para quitar los valores de omisión del registro, ejecute regedit y vaya a la entrada del registro HKLM\\SOFTWARE\\Microsoft. Para eliminar el nodo **MBAM** , haga clic con el botón secundario en el nodo y haga clic en **eliminar**.

## Temas relacionados


[Implementación de cliente de MBAM 2.0](deploying-the-mbam-20-client-mbam-2.md)









