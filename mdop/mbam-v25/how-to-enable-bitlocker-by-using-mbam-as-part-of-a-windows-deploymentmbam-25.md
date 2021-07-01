---
title: Cómo habilitar BitLocker utilizando MBAM como parte de una implementación de Windows
description: Cómo habilitar BitLocker utilizando MBAM como parte de una implementación de Windows
author: dansimp
ms.assetid: 7609ad7a-bb06-47be-b186-0a2db787c8a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: cd4086ca6bb2ea8d253ea3b743f4efe7efbbb6c1
ms.sourcegitcommit: 325c4b77f9a9df0f3de268457fed06184623bb94
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "11626187"
---
# <a name="how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deployment"></a>Cómo habilitar BitLocker utilizando MBAM como parte de una implementación de Windows

> [!IMPORTANT]
> Estas instrucciones no pertenecen a Configuration Manager BitLocker Management. El `Invoke-MbamClientDeployment.ps1` script de PowerShell no se admite para su uso con administración de BitLocker en Configuration Manager. Esto incluye el custodiado de claves de recuperación de BitLocker durante una secuencia de tareas de Configuration Manager. Además, a partir de Configuration Manager Current Branch 2103, Configuration Manager BitLocker Management ya no usa el sitio de servicios de recuperación de claves MBAM para custodiar claves. Si se intenta usar el script de PowerShell con `Invoke-MbamClientDeployment.ps1` Configuration Manager Current Branch 2103 o versiones posteriores, se pueden producir problemas graves con el sitio de Configuration Manager. Entre los problemas conocidos se incluye la creación de una gran cantidad de directivas dirigidas a todos los dispositivos que pueden provocar tormentas de directivas. Esto provocará una degradación grave del rendimiento en Configuration Manager principalmente en SQL y con puntos de administración.

En este tema se explica cómo habilitar BitLocker en el equipo de un usuario final mediante MBAM como parte del proceso Windows de creación de imágenes e implementación. Si ves una pantalla negra al reiniciar (una vez que finaliza la fase de instalación) que indica que la unidad no se puede desbloquear, consulta Versiones anteriores de Windows no se inician después del paso "Configurar Windows y Configuration Manager" si se usa BitLocker de preaprovisionamiento con Windows 10, versión [1511](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo).

**Requisitos previos:**

-   Debe haber un proceso Windows de implementación de imagen de Windows existente( Microsoft Deployment Toolkit (MDT), Microsoft System Center Configuration Manager o alguna otra herramienta o proceso de creación de imágenes.

-   Tpm debe estar habilitado en el BIOS y visible para el sistema operativo

-   La infraestructura de servidor MBAM debe estar en su lugar y ser accesible

-   La partición del sistema requerida por BitLocker debe crearse

-   La máquina debe estar unida al dominio durante la creación de imágenes antes de que MBAM habilita completamente BitLocker

**Para habilitar BitLocker con MBAM 2.5 SP1 como parte de una Windows implementación**

1. En MBAM 2.5 SP1, el enfoque recomendado para habilitar BitLocker durante una implementación Windows es mediante el `Invoke-MbamClientDeployment.ps1` script de PowerShell.

   -   El `Invoke-MbamClientDeployment.ps1` script crea BitLocker durante el proceso de creación de imágenes. Cuando la directiva de BitLocker lo requiere, el agente MBAM solicita inmediatamente al usuario del dominio que cree un PIN o una contraseña cuando el usuario del dominio inicie sesión por primera vez después de la creación de imágenes.

   -   Fácil de usar con MDT, System Center Configuration Manager o procesos de creación de imágenes independientes

   -   Compatible con PowerShell 2.0 o posterior

   -   Cifrar el volumen del sistema operativo con el protector de teclas tpm

   -   Totalmente compatible con el aprovisionamiento previo de BitLocker

   -   Cifrar de forma opcional los FDD

   -   Propietario del TPM de custodiaAuth Para Windows 7, MBAM debe ser el propietario del TPM para que se produzca la custodia.
   Por Windows 8.1, Windows 10 RTM y Windows 10 versión 1511, se admite la custodia de OwnerAuth de TPM.
   Por Windows 10, versión 1607 o posterior, solo Windows puede tomar posesión del TPM. En addiiton, Windows conservará la contraseña del propietario del TPM al aprovisionar el TPM. Consulta [Contraseña del propietario del TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) para obtener más información.

   -   Claves de recuperación de custodia y paquetes de claves de recuperación

   -   Estado de cifrado de informes inmediatamente

   -   Nuevos proveedores WMI

   -   Registro detallado

   -   Control de errores robusto

   Puede descargar el `Invoke-MbamClientDeployment.ps1` script desde el Centro Microsoft.com [descarga](https://www.microsoft.com/download/details.aspx?id=54439). Este es el script principal al que llamará el sistema de implementación para configurar el cifrado de unidad BitLocker y las claves de recuperación de registros con el servidor MBAM.

   **Métodos de implementación wmi para MBAM:** Los siguientes métodos WMI se han agregado en MBAM 2.5 SP1 para admitir la habilitación de BitLocker mediante el `Invoke-MbamClientDeployment.ps1` script de PowerShell.

   <a href="" id="mbam-machine-wmi-class"></a>**Clase WMI MBAM\_Machine** 
    **PrepareTpmAndEscrowOwnerAuth:** Lee el OwnerAuth del TPM y lo envía a la base de datos de recuperación mbam mediante el servicio de recuperación mbam. Si el TPM no es propiedad y el aprovisionamiento automático no está en, genera un OwnerAuth de TPM y toma posesión. Si se produce un error, se devuelve un código de error para solucionar problemas.

   **Nota** Por Windows 10, versión 1607 o posterior, solo Windows puede tomar posesión del TPM. En addiiton, Windows conservará la contraseña del propietario del TPM al aprovisionar el TPM. Consulta [Contraseña del propietario del TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) para obtener más información.

| Parámetro | Descripción |
| -------- | ----------- |
| RecoveryServiceEndPoint | Cadena que especifica el punto de conexión del servicio de recuperación MBAM. |

A continuación se muestra una lista de mensajes de error comunes:

| Valores devueltos comunes | Mensaje de error |
| -------------------- | ------------- |
|  **S_OK**<br />0 (0x0) | El método se ha realizado correctamente. |
| **MBAM_E_TPM_NOT_PRESENT**<br />2147746304 (0x80040200) | TPM no está presente en el equipo o está deshabilitado en la configuración del BIOS. |
| **MBAM_E_TPM_INCORRECT_STATE**<br />2147746305 (0x80040201) | TPM no está en el estado correcto (se permite la instalación habilitada, activada y del propietario). |
| **MBAM_E_TPM_AUTO_PROVISIONING_PENDING**<br />2147746306 (0x80040202) | MBAM no puede asumir la propiedad del TPM porque el aprovisionamiento automático está pendiente. Inténtelo de nuevo una vez completado el aprovisionamiento automático. |
| **MBAM_E_TPM_OWNERAUTH_READFAIL**<br />2147746307 (0x80040203) | MBAM no puede leer el valor de autorización del propietario del TPM. Es posible que el valor se haya quitado después de una custodia correcta. En Windows 7, MBAM no puede leer el valor si el TPM es propiedad de otros usuarios. |
| **MBAM_E_REBOOT_REQUIRED**<br />2147746308 (0x80040204) | El equipo debe reiniciarse para establecer tpm en el estado correcto. Es posible que deba reiniciar manualmente el equipo. |
| **MBAM_E_SHUTDOWN_REQUIRED**<br />2147746309 (0x80040205) | El equipo debe apagarse y volver a estar activado para establecer el TPM en el estado correcto. Es posible que deba reiniciar manualmente el equipo. |
| **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | El extremo remoto denegó el acceso. |
| **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | El extremo remoto no existe o no se pudo encontrar. |
| **WS_E_ENDPOINT_FAILURE<br />2151481357 (0x803D000F) | El extremo remoto no pudo procesar la solicitud. |
| **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | El extremo remoto no era accesible. |
| **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Se recibió un mensaje que contiene un error desde el extremo remoto. Asegúrese de que se está conectando al extremo de servicio correcto. |
| **WS_E_INVALID_ENDPOINT_URL** 2151481376 (0x803D0020) | La dirección URL de la dirección del extremo no es válida. La dirección URL debe empezar por "http" o "https". |

   **ReportStatus:** Lee el estado de cumplimiento del volumen y lo envía a la base de datos de estado de cumplimiento mbam mediante el servicio de informes de estado de MBAM. El estado incluye la fuerza del cifrado, el tipo de protector, el estado del protector y el estado de cifrado. Si se produce un error, se devuelve un código de error para solucionar problemas.

   | Parámetro | Descripción |
   | --------- | ----------- |
   | ReportingServiceEndPoint | Cadena que especifica el extremo de servicio de informes de estado MBAM. |

   A continuación se muestra una lista de mensajes de error comunes:

   | Valores devueltos comunes | Mensaje de error |
   | -------------------- | ------------- |
   | **S_OK**<br /> 0 (0x0) | El método se ha realizado correctamente |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | El extremo remoto denegó el acceso.|
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | El extremo remoto no existe o no se pudo encontrar. |
   | **WS_E_ENDPOINT_FAILURE**<br /> 2151481357 (0x803D000F) | El extremo remoto no pudo procesar la solicitud. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | El extremo remoto no era accesible. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Se recibió un mensaje que contiene un error desde el extremo remoto. Asegúrese de que se está conectando al extremo de servicio correcto. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | La dirección URL de la dirección del extremo no es válida. La dirección URL debe empezar por "http" o "https". |

   <a href="" id="mbam-volume-wmi-class"></a>**MBAM\_Volume Clase WMI** **EscrowRecoveryKey:** lee la contraseña numérica de recuperación y el paquete clave del volumen y las envía a la base de datos de recuperación de MBAM mediante el servicio de recuperación mbam. Si se produce un error, se devuelve un código de error para solucionar problemas.

   | Parámetro | Descripción |
   | --------- | ----------- |
   | RecoveryServiceEndPoint | Cadena que especifica el punto de conexión del servicio de recuperación MBAM. |

   A continuación se muestra una lista de mensajes de error comunes:

   | Valores devueltos comunes | Mensaje de error |
   | -------------------- | ------------- |
   | **S_OK**<br />0 (0x0) | El método se ha realizado correctamente |
   | **FVE_E_LOCKED_VOLUME**<br />2150694912 (0x80310000) | El volumen está bloqueado. |
   | **FVE_E_PROTECTOR_NOT_FOUND**<br />2150694963 (0x80310033) | No se encontró un protector de contraseña numérica para el volumen. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | El extremo remoto denegó el acceso. |
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | El extremo remoto no existe o no se pudo encontrar. |
   | **WS_E_ENDPOINT_FAILURE**<br />2151481357 (0x803D000F) | El extremo remoto no pudo procesar la solicitud. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | El extremo remoto no era accesible. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Se recibió un mensaje que contiene un error desde el extremo remoto. Asegúrese de que se está conectando al extremo de servicio correcto. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | La dirección URL de la dirección del extremo no es válida. La dirección URL debe empezar por "http" o "https". |
     

2. **Implementar MBAM con Microsoft Deployment Toolkit (MDT) y PowerShell**

   1.  En MDT, cree un nuevo recurso compartido de implementación o abra un recurso compartido de implementación existente.

       **Nota**  
       El `Invoke-MbamClientDeployment.ps1` script de PowerShell se puede usar con cualquier proceso o herramienta de creación de imágenes. En esta sección se muestra cómo integrarlo mediante MDT, pero los pasos son similares a integrarlo con cualquier otro proceso o herramienta.

       **Precaución**  
       Si usas el aprovisionamiento previo de BitLocker (WinPE) y quieres mantener el valor de autorización del propietario del TPM, debes agregar el script en WinPE inmediatamente antes de que la instalación se reinicie en el sistema operativo `SaveWinPETpmOwnerAuth.wsf` completo. **Si no usa este script, perderá el valor de autorización del propietario del TPM al reiniciar.**

   2.  Copiar `Invoke-MbamClientDeployment.ps1` en ** &lt; DeploymentShare &gt; \\Scripts**. Si usa el aprovisionamiento previo, copie el `SaveWinPETpmOwnerAuth.wsf` archivo en ** &lt; DeploymentShare &gt; \\Scripts**.

   3.  Agregue la aplicación cliente MBAM 2.5 SP1 al nodo Aplicaciones del recurso compartido de implementación.

       1.  En el **nodo Aplicaciones,** haga clic **en Nueva aplicación**.

       2.  Seleccione **Aplicación con archivos de origen**. Haz clic en **Siguiente**.

       3.  En **Nombre de la**aplicación , escriba "Cliente DE MBAM 2.5 SP1". Haz clic en **Siguiente**.

       4.  Vaya al directorio que contiene `MBAMClientSetup-<Version>.msi` . Haz clic en **Siguiente**.

       5.  Escriba "Cliente DE MBAM 2.5 SP1" como directorio que se creará. Haz clic en **Siguiente**.

       6.  Escriba `msiexec /i MBAMClientSetup-<Version>.msi /quiet` en la línea de comandos. Haz clic en **Siguiente**.

       7.  Acepte los valores predeterminados restantes para completar el Asistente para nueva aplicación.

   4.  En MDT, haga clic con el botón secundario en el nombre del recurso compartido de implementación y haga clic en **Propiedades**. Haga clic en **la pestaña** Reglas. Agregue las líneas siguientes:

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       Haga clic en Aceptar para cerrar la ventana.

   5.  En el nodo Secuencias de tareas, edite una secuencia de tareas existente usada para Windows implementación. Si lo desea, puede crear una nueva secuencia de tareas haciendo **** clic con el botón secundario en el nodo **Secuencias** de tareas, seleccionando Nueva secuencia de tareas y completando el asistente.

       En la **pestaña Secuencia de** tareas de la secuencia de tareas seleccionada, realice estos pasos:

       1.  En la **carpeta Preinstalar,** habilita la tarea opcional **Habilitar BitLocker (sin conexión)** si quieres que BitLocker esté habilitado en WinPE, que solo cifra el espacio usado.

       2.  Para conservar OwnerAuth de TPM al usar el aprovisionamiento previo, lo que permite que MBAM lo escrow más adelante, haga lo siguiente:

           1.  Buscar el **paso Instalar sistema operativo**

           2.  Agregar un nuevo **paso ejecutar línea de** comandos después de él

           3.  Asigne un nombre al paso **Persist TPM OwnerAuth**

           4.  Establezca la línea de comandos en Nota: para Windows 10 `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **** versión 1607 o posterior, solo Windows puede asumir la propiedad del TPM. En addiiton, Windows conservará la contraseña del propietario del TPM al aprovisionar el TPM. Consulta [Contraseña del propietario del TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) para obtener más información.

       3.  En la **carpeta Restaurar estado,** elimine la **tarea Habilitar BitLocker.**

       4.  En la **carpeta Restaurar estado** en **Tareas**personalizadas, cree una nueva **tarea Instalar** aplicación y asíñale el nombre Instalar **agente MBAM**. Haga clic **en el botón de** opción Instalar aplicación única y vaya a la aplicación cliente MBAM 2.5 SP1 creada anteriormente.

       5.  En **** la carpeta Restaurar estado en Tareas personalizadas, **** cree una nueva tarea Ejecutar script de **PowerShell** (después del paso de aplicación cliente de MBAM 2.5 SP1) con la siguiente configuración (actualice los parámetros según corresponda para su entorno):

           -   Nombre: Configurar BitLocker para MBAM

           -   Script de PowerShell: `Invoke-MbamClientDeployment.ps1`

           -   Parámetros:

               <table>
               <colgroup>
               <col width="33%" />
               <col width="33%" />
               <col width="33%" />
               </colgroup>
               <tbody>
               <tr class="odd">
               <td align="left"><p>-RecoveryServiceEndpoint</p></td>
               <td align="left"><p>Obligatorio</p></td>
               <td align="left"><p>Punto de conexión de servicio de recuperación mbam</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-StatusReportingServiceEndpoint</p></td>
               <td align="left"><p>Opcional</p></td>
               <td align="left"><p>Extremo de servicio de informes de estado MBAM</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-EncryptionMethod</p></td>
               <td align="left"><p>Opcional</p></td>
               <td align="left"><p>Método de cifrado (predeterminado: AES 128)</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-EncryptAndEscrowDataVolume</p></td>
               <td align="left"><p>Conmutador</p></td>
               <td align="left"><p>Especificar para cifrar los volúmenes de datos y las claves de recuperación del volumen de datos de custodia</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-WaitForEncryptionToComplete</p></td>
               <td align="left"><p>Conmutador</p></td>
               <td align="left"><p>Especificar para esperar a que se complete el cifrado</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-DoNotResumeSuspendedEncryption</p></td>
               <td align="left"><p>Conmutador</p></td>
               <td align="left"><p>Especificar que el script de implementación no reanudará el cifrado suspendido</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreEscrowOwnerAuthFailure</p></td>
               <td align="left"><p>Conmutador</p></td>
               <td align="left"><p>Especifique para omitir el error de custodia del propietario del TPM. Debe usarse en los escenarios en los que MBAM no puede leer la autenticación del propietario del TPM, por ejemplo, si el aprovisionamiento automático de TPM está habilitado.</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-IgnoreEscrowRecoveryKeyFailure</p></td>
               <td align="left"><p>Conmutador</p></td>
               <td align="left"><p>Especificar para omitir el error de custodia de clave de recuperación de volumen</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreReportStatusFailure</p></td>
               <td align="left"><p>Conmutador</p></td>
               <td align="left"><p>Especificar para omitir el error de informes de estado</p></td>
               </tr>
               </tbody>
               </table>

                 

**Para habilitar BitLocker con MBAM 2.5 o versiones anteriores como parte de una Windows implementación**

1.  Instale el cliente MBAM. Para obtener instrucciones, [vea How to Deploy the MBAM Client by Using a Command Line](how-to-deploy-the-mbam-client-by-using-a-command-line.md).

2.  Unir el equipo a un dominio (recomendado).

    -   Si el equipo no está unido a un dominio, la contraseña de recuperación no se almacena en el servicio de recuperación de claves MBAM. De forma predeterminada, MBAM no permite que se produzca el cifrado a menos que se pueda almacenar la clave de recuperación.

    -   Si un equipo se inicia en modo de recuperación antes de que la clave de recuperación se almacene en el servidor MBAM, no hay ningún método de recuperación disponible y el equipo debe volver a crearse.

3.  Abra un símbolo del sistema como administrador y detenga el servicio MBAM.

4.  Establezca el servicio en **Manual** o **A petición** escribiendo los siguientes comandos:

    **net stop mbamagent**

    **sc config mbamagent start= demand**

5.  Establezca los valores del Registro para que el cliente MBAM ignore la configuración de directiva de grupo y, en su lugar, establezca el cifrado para iniciar la Windows se implementa en ese equipo cliente.

    **Precaución**  
    En este paso se describe cómo modificar el Windows registro. El uso incorrecto del Editor del Registro puede provocar problemas graves que pueden requerir la reinstalación de Windows. No podemos garantizar que los problemas resultantes del uso incorrecto del Editor del Registro se puedan resolver. Use el Editor del Registro por su cuenta y riesgo.

    1.  Establezca el TPM para el cifrado de solo sistema **operativo,** ejecute Regedit.exe y, a continuación, importe la plantilla de clave del Registro desde C:\\Archivos de programa\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

    2.  En Regedit.exe, vaya a HKLM\\SOFTWARE\\Microsoft\\MBAM y configure las opciones que se enumeran en la tabla siguiente.

        **Nota**  
        Puede establecer la configuración de directiva de grupo o los valores del Registro relacionados con MBAM aquí. Esta configuración invalidará los valores establecidos anteriormente.

        Entrada del Registro Configuración

        DeploymentTime

        0 = Desactivado

        1 = Usar la configuración de directiva de tiempo de implementación (valor predeterminado): use esta configuración para habilitar el cifrado en el momento en que Windows se implementa en el equipo cliente.

        UseKeyRecoveryService

        0 = No usar custodia de claves (las dos entradas siguientes del Registro no son necesarias en este caso)

        1 = Usar custodia de clave en el sistema de recuperación de claves (predeterminado)

        Esta es la configuración recomendada, que permite a MBAM almacenar las claves de recuperación. El equipo debe poder comunicarse con el servicio de recuperación de claves MBAM. Compruebe que el equipo puede comunicarse con el servicio antes de continuar.

        KeyRecoveryOptions

        0 = Solo carga la clave de recuperación

        1 = Carga la clave de recuperación y el paquete de recuperación de claves (predeterminado)

        KeyRecoveryServiceEndPoint

        Establezca este valor en la dirección URL del servidor que ejecuta el servicio de recuperación de claves, por ejemplo, http:// nombre del equipo &lt; &gt; /MBAMRecoveryAndHardwareService/CoreService.svc.


6.  El cliente MBAM reiniciará el sistema durante la implementación del cliente MBAM. Cuando esté listo para este reinicio, ejecute el siguiente comando en un símbolo del sistema como administrador:

    **net start mbamagent**

7.  Cuando los equipos se reinicien y el BIOS le pida, acepte el cambio de TPM.

8.  Durante el proceso de creación de imágenes del sistema operativo cliente de Windows, cuando esté listo para iniciar el cifrado, abra un símbolo del sistema como administrador y escriba los siguientes comandos para establecer el inicio en **Automático** y para reiniciar el agente de cliente MBAM:

    **sc config mbamagent start= auto**

    **net start mbamagent**

9.  Para eliminar los valores del Registro de omisión, ejecute Regedit.exe y vaya a la entrada del Registro HKLM\\SOFTWARE\\Microsoft. Haga clic con el botón secundario en **el nodo MBAM** y, a continuación, haga clic **en Eliminar**.

## <a name="related-topics"></a>Temas relacionados

[Implementación de cliente de MBAM 2.5](deploying-the-mbam-25-client.md)

[Planificación para la implementación de clientes de MBAM 2.5](planning-for-mbam-25-client-deployment.md)

## <a name="got-a-suggestion-for-mbam"></a>¿Tienes una sugerencia para MBAM?
- Agregue o vote las sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, use el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
