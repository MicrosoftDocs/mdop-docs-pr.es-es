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
ms.openlocfilehash: 4b2cbf333c705088d0a068521fb65e99551bb1f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826230"
---
# Cómo habilitar BitLocker utilizando MBAM como parte de una implementación de Windows


En este tema, se explica cómo habilitar BitLocker en el equipo de un usuario final mediante MBAM como parte del proceso de creación de imágenes e implementación de Windows. Si ve una pantalla negra en el reinicio (después de concluir la fase de instalación) indicando que la unidad no se puede desbloquear, consulte [versiones anteriores de Windows no se inicia después de "configurar el administrador de configuración y configuración de Windows" si se usa BitLocker de Windows 10, versión 1511](https://support.microsoft.com/en-us/help/4494799/earlier-windows-versions-don-t-start-after-you-use-pre-provision-bitlo).

**Requisitos previos:**

-   Un proceso de implementación de imágenes de Windows existente (Microsoft Deployment Toolkit (MDT), Microsoft System Center Configuration Manager o algún otro proceso o herramienta de imágenes) debe estar en su sitio.

-   TPM debe estar habilitado en el BIOS y visible para el sistema operativo

-   La infraestructura de servidores de MBAM debe estar vigente y accesible

-   Debe crearse la partición de sistema requerida por BitLocker

-   El equipo debe estar unido a un dominio durante la creación de imágenes antes de que MBAM completamente habilite BitLocker

**Para habilitar BitLocker con MBAM 2,5 SP1 como parte de una implementación de Windows**

1. En MBAM 2,5 SP1, el método recomendado para habilitar BitLocker durante una implementación de Windows es usar el `Invoke-MbamClientDeployment.ps1` script de PowerShell.

   -   La `Invoke-MbamClientDeployment.ps1` secuencia de comandos actúa como BitLocker durante el proceso de creación de imágenes. Cuando la Directiva de BitLocker lo requiere, el agente de MBAM solicita inmediatamente al usuario del dominio que cree un PIN o una contraseña cuando el usuario del dominio inicia sesión por primera vez después de la creación de imágenes.

   -   Fácil de usar con MDT, System Center Configuration Manager o procesos de creación de imágenes independientes

   -   Compatible con PowerShell 2,0 o versiones posteriores

   -   Cifrar volumen del sistema operativo con el protector de clave TPM

   -   Totalmente compatible con el aprovisionamiento previo de BitLocker

   -   , Opcionalmente, cifrar FDDs

   -   Depósito de OwnerAuth TPM para Windows 7, MBAM debe ser el propietario del TPM para que se produzca el depósito de garantía.
   Para Windows 8,1, Windows 10 RTM y Windows 10 versión 1511, se admite el depósito de garantía de TPM OwnerAuth.
   Para Windows 10, versión 1607 o posterior, solo Windows puede tomar posesión de TPM. En addiiton, Windows no conservará la contraseña de propietario de TPM al aprovisionar el TPM. Para obtener más información, consulta la [contraseña de propietario de TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) .

   -   Claves de recuperación de depósito de garantía y paquetes de claves de recuperación

   -   Informar inmediatamente del estado del cifrado

   -   Nuevos proveedores de WMI

   -   Registro detallado

   -   Control de errores sólido

   Puede descargar el `Invoke-MbamClientDeployment.ps1` script desde el [centro de descarga de Microsoft.com](https://www.microsoft.com/download/details.aspx?id=54439). Este es el script principal al que el sistema de implementación llamará para configurar el cifrado de unidad BitLocker y las claves de recuperación de registro con el servidor MBAM.

   **Métodos de implementación de WMI para MBAM:** Los siguientes métodos WMI se han agregado en MBAM 2,5 SP1 para permitir la habilitación de BitLocker mediante el `Invoke-MbamClientDeployment.ps1` script de PowerShell.

   <a href="" id="mbam-machine-wmi-class"></a>**MBAM \ _Machine clase WMI** 
    **PrepareTpmAndEscrowOwnerAuth:** Lee la OwnerAuth de TPM y la envía a la base de datos de recuperación de MBAM con el servicio de recuperación de MBAM. Si el TPM no pertenece y el aprovisionamiento automático no está activado, genera un OwnerAuth de TPM y toma la propiedad. Si se produce un error, se devuelve un código de error para la solución de problemas.

   **Nota:** Para Windows 10, versión 1607 o posterior, solo Windows puede tomar posesión de TPM. En addiiton, Windows no conservará la contraseña de propietario de TPM al aprovisionar el TPM. Para obtener más información, consulta la [contraseña de propietario de TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) .

| Parámetro | Descripción |
| -------- | ----------- |
| RecoveryServiceEndPoint | Cadena que especifica el extremo del servicio de recuperación de MBAM. |

A continuación se muestra una lista de mensajes de error comunes:

| Valores devueltos comunes | Mensaje de error |
| -------------------- | ------------- |
|  **S_OK**<br />0 (0X0) | El método se realizó correctamente. |
| **MBAM_E_TPM_NOT_PRESENT**<br />2147746304 (0x80040200) | El TPM no está presente en el equipo o está deshabilitado en la configuración del BIOS. |
| **MBAM_E_TPM_INCORRECT_STATE**<br />2147746305 (0x80040201) | El TPM no se encuentra en el estado correcto (habilitado, activado y permitido por el propietario). |
| **MBAM_E_TPM_AUTO_PROVISIONING_PENDING**<br />2147746306 (0x80040202) | MBAM no puede tomar posesión de TPM porque el aprovisionamiento automático está pendiente. Inténtalo de nuevo después de completar el aprovisionamiento automático. |
| **MBAM_E_TPM_OWNERAUTH_READFAIL**<br />2147746307 (0x80040203) | MBAM no puede leer el valor de autorización de propietario de TPM. Es posible que el valor se haya eliminado después de un depósito de garantía. En Windows 7, MBAM no puede leer el valor si el TPM es propiedad de otros usuarios. |
| **MBAM_E_REBOOT_REQUIRED**<br />2147746308 (0x80040204) | El equipo debe reiniciarse para establecer TPM en el estado correcto. Es posible que tenga que reiniciar manualmente el equipo. |
| **MBAM_E_SHUTDOWN_REQUIRED**<br />2147746309 (0x80040205) | El equipo debe apagarse y volver a activarse para establecer TPM en el estado correcto. Es posible que tenga que reiniciar manualmente el equipo. |
| **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | El punto de conexión remoto ha denegado el acceso. |
| **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | El extremo remoto no existe o no se pudo encontrar. |
| * * WS_E_ENDPOINT_FAILURE<br />2151481357 (0x803D000F) | El extremo remoto no pudo procesar la solicitud. |
| **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | El extremo remoto no es accesible. |
| **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Se recibió un mensaje con un error del extremo remoto. Asegúrese de que se está conectando al extremo de servicio correcto. |
| **WS_E_INVALID_ENDPOINT_URL** 2151481376 (0x803D0020) | La dirección URL de la dirección de extremo no es válida. La dirección URL debe empezar por "http" o "https". |

   **ReportStatus:** Lee el estado de cumplimiento del volumen y lo envía a la base de datos de Estados de cumplimiento de MBAM mediante el servicio de informes de estado de MBAM. El estado incluye la intensidad de cifrado, el tipo de protector, el estado del protector y el estado de cifrado. Si se produce un error, se devuelve un código de error para la solución de problemas.

   | Parámetro | Descripción |
   | --------- | ----------- |
   | ReportingServiceEndPoint | Cadena que especifica el extremo del servicio de informes de estado de MBAM. |

   A continuación se muestra una lista de mensajes de error comunes:

   | Valores devueltos comunes | Mensaje de error |
   | -------------------- | ------------- |
   | **S_OK**<br /> 0 (0X0) | El método se realizó correctamente |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | El punto de conexión remoto ha denegado el acceso.|
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | El extremo remoto no existe o no se pudo encontrar. |
   | **WS_E_ENDPOINT_FAILURE**<br /> 2151481357 (0x803D000F) | El extremo remoto no pudo procesar la solicitud. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | El extremo remoto no es accesible. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Se recibió un mensaje con un error del extremo remoto. Asegúrese de que se está conectando al extremo de servicio correcto. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | La dirección URL de la dirección de extremo no es válida. La dirección URL debe empezar por "http" o "https". |

   <a href="" id="mbam-volume-wmi-class"></a>**MBAM \ _VOLUME WMI (clase** ) **EscrowRecoveryKey:** lee la contraseña numérica de recuperación y el paquete de claves del volumen y los envía a la MBAM base de datos de recuperación mediante el servicio de recuperación de MBAM. Si se produce un error, se devuelve un código de error para la solución de problemas.

   | Parámetro | Descripción |
   | --------- | ----------- |
   | RecoveryServiceEndPoint | Cadena que especifica el extremo del servicio de recuperación de MBAM. |

   A continuación se muestra una lista de mensajes de error comunes:

   | Valores devueltos comunes | Mensaje de error |
   | -------------------- | ------------- |
   | **S_OK**<br />0 (0X0) | El método se realizó correctamente |
   | **FVE_E_LOCKED_VOLUME**<br />2150694912 (0x80310000) | El volumen está bloqueado. |
   | **FVE_E_PROTECTOR_NOT_FOUND**<br />2150694963 (0x80310033) | No se encontró un protector de contraseña numérica para el volumen. |
   | **WS_E_ENDPOINT_ACCESS_DENIED**<br />2151481349 (0x803D0005) | El punto de conexión remoto ha denegado el acceso. |
   | **WS_E_ENDPOINT_NOT_FOUND**<br />2151481357 (0x803D000D) | El extremo remoto no existe o no se pudo encontrar. |
   | **WS_E_ENDPOINT_FAILURE**<br />2151481357 (0x803D000F) | El extremo remoto no pudo procesar la solicitud. |
   | **WS_E_ENDPOINT_UNREACHABLE**<br />2151481360 (0x803D0010) | El extremo remoto no es accesible. |
   | **WS_E_ENDPOINT_FAULT_RECEIVED**<br />2151481363 (0x803D0013) | Se recibió un mensaje con un error del extremo remoto. Asegúrese de que se está conectando al extremo de servicio correcto. |
   | **WS_E_INVALID_ENDPOINT_URL**<br />2151481376 (0x803D0020) | La dirección URL de la dirección de extremo no es válida. La dirección URL debe empezar por "http" o "https". |
     

2. **Implementar MBAM con Microsoft Deployment Toolkit (MDT) y PowerShell**

   1.  En MDT, cree un nuevo recurso compartido de implementación o abra un recurso compartido de implementación existente.

       **Nota**  
       El `Invoke-MbamClientDeployment.ps1` script de PowerShell se puede usar con cualquier proceso o herramienta de imágenes. En esta sección se muestra cómo integrarlo con MDT, pero los pasos son similares a la integración con cualquier otro proceso o herramienta.

       **Actúe**  
       Si usa el preaprovisionamiento de BitLocker (WinPE) y desea mantener el valor de autorización de propietario de TPM, debe agregar el `SaveWinPETpmOwnerAuth.wsf` script en WinPE inmediatamente antes de que la instalación se reinicie en el sistema operativo completo. **Si no usa este script, perderá el valor de autorización de propietario de TPM al reiniciar.**

   2.  Copie `Invoke-MbamClientDeployment.ps1` a ** &lt; DeploymentShare &gt; \\Scripts**. Si está usando el preaprovisionamiento, copie el `SaveWinPETpmOwnerAuth.wsf` archivo en ** &lt; DeploymentShare &gt; \\Scripts**.

   3.  Agregue la aplicación cliente de MBAM 2,5 SP1 al nodo aplicaciones del recurso compartido de implementación.

       1.  En el nodo **aplicaciones** , haga clic en **nueva aplicación**.

       2.  Seleccione **aplicación con archivos de origen**. Haz clic en **Siguiente**.

       3.  En **nombre**de la aplicación, escriba "cliente de MBAM 2,5 SP1". Haz clic en **Siguiente**.

       4.  Vaya al directorio que contiene `MBAMClientSetup-<Version>.msi` . Haz clic en **Siguiente**.

       5.  Escriba "MBAM 2,5 SP1 Client" como el directorio que desea crear. Haz clic en **Siguiente**.

       6.  Escriba `msiexec /i MBAMClientSetup-<Version>.msi /quiet` en la línea de comandos. Haz clic en **Siguiente**.

       7.  Acepte los valores predeterminados restantes para completar el Asistente para nueva aplicación.

   4.  En MDT, haga clic con el botón secundario en el nombre del recurso compartido de implementación y haga clic en **propiedades**. Haga clic en la pestaña **reglas** . Agregue las siguientes líneas:

       `SkipBitLocker=YES``BDEInstall=TPM``BDEInstallSuppress=NO``BDEWaitForEncryption=YES`

       Haga clic en Aceptar para cerrar la ventana.

   5.  En el nodo secuencias de tareas, edite una secuencia de tareas existente usada para la implementación de Windows. Si lo desea, puede crear una nueva secuencia de tareas haciendo clic con el botón secundario en el nodo **secuencias** de tareas, seleccionando **nueva secuencia de tareas**y completando el asistente.

       En la pestaña **secuencia de tareas** de la secuencia de tareas seleccionada, siga estos pasos:

       1.  En la carpeta **preinstalación** , habilite la opción **Habilitar BitLocker (desconectado)** si quiere habilitar BitLocker en WinPE, que cifra solo el espacio usado.

       2.  Para conservar el TPM OwnerAuth al usar el preaprovisionamiento, permitir que MBAM para el depósito de garantía más tarde, haga lo siguiente:

           1.  Buscar el paso **instalar el sistema operativo**

           2.  Agregar un nuevo paso de **línea de comandos ejecutar** después de él

           3.  Nombre el paso **Persist TPM OwnerAuth**

           4.  Establezca la línea de comandos en `cscript.exe "%SCRIPTROOT%/SaveWinPETpmOwnerAuth.wsf"`
            **Nota:** para Windows 10, versión 1607 o posterior, solo Windows puede tomar posesión de TPM. En addiiton, Windows no conservará la contraseña de propietario de TPM al aprovisionar el TPM. Para obtener más información, consulta la [contraseña de propietario de TPM](https://docs.microsoft.com/windows/security/hardware-protection/tpm/change-the-tpm-owner-password) .

       3.  En la carpeta de **restauración de estado** , elimine la tarea **Habilitar BitLocker** .

       4.  En la carpeta **restaurar estado** de **tareas personalizadas**, cree una nueva tarea **instalar aplicación** y ASÍGNELE el nombre **instalar agente de MBAM**. Haga clic en el botón de radio **instalar una sola aplicación** y vaya a la aplicación cliente de MBAM 2,5 SP1 creada anteriormente.

       5.  En la carpeta de **restauración de estado** de **tareas personalizadas**, cree una nueva tarea **Ejecutar script de PowerShell** (después del paso de la aplicación cliente de MBAM 2,5 SP1) con la siguiente configuración (actualice los parámetros según corresponda para su entorno):

           -   Nombre: configurar BitLocker para MBAM

           -   Script de PowerShell: `Invoke-MbamClientDeployment.ps1`

           -   Los

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
               <td align="left"><p>Extremo de servicio de recuperación de MBAM</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-StatusReportingServiceEndpoint</p></td>
               <td align="left"><p>Opcional</p></td>
               <td align="left"><p>Extremo del servicio de informes de estado de MBAM</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-EncryptionMethod</p></td>
               <td align="left"><p>Opcional</p></td>
               <td align="left"><p>Método de cifrado (valor predeterminado: AES 128)</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-EncryptAndEscrowDataVolume</p></td>
               <td align="left"><p>Conmutador</p></td>
               <td align="left"><p>Especifique si desea cifrar los volúmenes de datos y las claves de recuperación del volumen de datos del depósito de garantía</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-WaitForEncryptionToComplete</p></td>
               <td align="left"><p>Conmutador</p></td>
               <td align="left"><p>Especificar que se espere a que se complete el cifrado</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-DoNotResumeSuspendedEncryption</p></td>
               <td align="left"><p>Conmutador</p></td>
               <td align="left"><p>Especificar que el script de implementación no reanude el cifrado suspendido</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreEscrowOwnerAuthFailure</p></td>
               <td align="left"><p>Conmutador</p></td>
               <td align="left"><p>Especificar ignorar el error de custodia de autenticación de propietario de TPM. Debe usarse en los escenarios en los que MBAM no puede leer la autenticación de propietario de TPM, por ejemplo, si el aprovisionamiento automático de TPM está habilitado.</p></td>
               </tr>
               <tr class="even">
               <td align="left"><p>-IgnoreEscrowRecoveryKeyFailure</p></td>
               <td align="left"><p>Conmutador</p></td>
               <td align="left"><p>Especificar ignorar el error de custodia de la clave de recuperación de volumen</p></td>
               </tr>
               <tr class="odd">
               <td align="left"><p>-IgnoreReportStatusFailure</p></td>
               <td align="left"><p>Conmutador</p></td>
               <td align="left"><p>Especificar ignorar el error de informes de estado</p></td>
               </tr>
               </tbody>
               </table>

                 

**Para habilitar BitLocker con MBAM 2,5 o versiones anteriores como parte de una implementación de Windows**

1.  Instale el cliente MBAM. Para obtener instrucciones, consulte [cómo implementar el cliente de MBAM con una línea de comandos](how-to-deploy-the-mbam-client-by-using-a-command-line.md).

2.  Unir el equipo a un dominio (recomendado).

    -   Si el equipo no se ha unido a un dominio, la contraseña de recuperación no se almacena en el servicio de recuperación de claves de MBAM. De forma predeterminada, MBAM no permite que se produzca el cifrado, a menos que se pueda almacenar la clave de recuperación.

    -   Si un equipo se inicia en modo de recuperación antes de que la clave de recuperación se almacene en el servidor de MBAM, no hay ningún método de recuperación disponible y se debe recrear la imagen del equipo.

3.  Abra un símbolo del sistema como administrador y detenga el servicio MBAM.

4.  Para establecer el servicio como **manual** o **a petición** , escriba los siguientes comandos:

    **net stop mbamagent**

    **SC config mbamagent Start = Demand**

5.  Establezca los valores del registro para que el cliente de MBAM pase por alto la configuración de directiva de grupo y, en su lugar, establezca el cifrado para que se inicie Windows en ese equipo cliente.

    **PRECAUCIÓN**  En este paso se describe cómo modificar el registro de Windows. El uso incorrecto del editor del registro puede causar serios problemas que le obliguen a reinstalar Windows. No podemos garantizar que se puedan resolver los problemas resultantes del uso incorrecto del editor del registro. Use el editor del registro bajo su propia responsabilidad.

    1.  Configure el TPM para el **cifrado solo para el sistema operativo**, ejecute Regedit.exe y, a continuación, importe la plantilla de clave de registro desde C:\\Archivos de Files\\Microsoft\\MDOP MBAM\\MBAMDeploymentKeyTemplate.reg.

    2.  En Regedit.exe, vaya a HKLM\\SOFTWARE\\Microsoft\\MBAM y configure las opciones que se indican en la tabla siguiente.

        **Nota:**  Aquí puede establecer la configuración de directiva de grupo o valores del registro relacionados con MBAM. Esta configuración anulará los valores establecidos previamente.

        Configuración de la entrada del registro

        DeploymentTime

        0 = deshabilitado

        1 = usar la configuración de directiva de tiempo de implementación (valor predeterminado): Use esta configuración para habilitar el cifrado en el momento en que Windows se implemente en el equipo cliente.

        UseKeyRecoveryService

        0 = no usar custodia de claves (en este caso, no se necesitan las dos siguientes entradas de registro)

        1 = usar custodia de clave en el sistema de recuperación de claves (predeterminado)

        Esta es la configuración recomendada, que permite a MBAM almacenar las claves de recuperación. El equipo debe poder comunicarse con el servicio de recuperación de claves de MBAM. Compruebe que el equipo puede comunicarse con el servicio antes de continuar.

        KeyRecoveryOptions

        0 = solo carga la clave de recuperación

        1 = carga de clave de recuperación y paquete de recuperación de claves (predeterminado)

        KeyRecoveryServiceEndPoint

        Establezca este valor en la dirección URL del servidor que ejecuta el servicio de recuperación de claves, por ejemplo, http:// &lt; nombre de equipo &gt; /MBAMRecoveryAndHardwareService/CoreService.SVC.


6.  El cliente de MBAM reiniciará el sistema durante la implementación de cliente de MBAM. Cuando esté listo para este reinicio, ejecute el siguiente comando en un símbolo del sistema como administrador:

    **net start mbamagent**

7.  Cuando se reinicien los equipos y el BIOS le solicite, acepte el cambio de TPM.

8.  Durante el proceso de creación de imágenes del sistema operativo de cliente de Windows, cuando esté listo para iniciar el cifrado, abra un símbolo del sistema como administrador y escriba los siguientes comandos para establecer el inicio en **automático** y para reiniciar el agente de cliente de MBAM:

    **SC config mbamagent Start = Auto**

    **net start mbamagent**

9.  Para eliminar los valores de omisión del registro, ejecute Regedit.exe y vaya a la entrada del registro HKLM\\SOFTWARE\\Microsoft. Haga clic con el botón derecho en el nodo **MBAM** y luego haga clic en **eliminar**.

## Temas relacionados

[Implementación de cliente de MBAM 2.5](deploying-the-mbam-25-client.md)

[Planificación para la implementación de clientes de MBAM 2.5](planning-for-mbam-25-client-deployment.md)

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
