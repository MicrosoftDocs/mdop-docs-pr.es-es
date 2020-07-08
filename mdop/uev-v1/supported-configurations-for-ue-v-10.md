---
title: Configuraciones admitidas para UE-V 1.0
description: Configuraciones admitidas para UE-V 1.0
author: dansimp
ms.assetid: d90ab83e-741f-48eb-b1d8-a64cb9259f7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a84514317de8a4cfd9df9c94a9a130933b00874a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825551"
---
# Configuraciones admitidas para UE-V 1.0


La virtualización de la experiencia del usuario de Microsoft (UE-V) admite las siguientes configuraciones descritas.

**Nota:**  Microsoft proporciona soporte técnico para el Service Pack actual y, en algunos casos, el Service Pack anterior. Para encontrar las escalas de tiempo de soporte técnico para su producto, consulte los [Service Pack compatibles del ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31975). Para obtener más información sobre la Directiva de ciclo de vida del soporte técnico de Microsoft, consulte [preguntas más frecuentes sobre la Directiva de soporte ciclo de vida](https://go.microsoft.com/fwlink/p/?LinkId=31976)

 

## Configuraciones admitidas para el agente de UE-V y el generador de UE-V


En la tabla siguiente se enumeran los sistemas operativos que admiten el generador de virtualización de la experiencia del usuario y el agente de virtualización de la experiencia del usuario.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Sistema operativo</strong></th>
<th align="left"><strong>Edición</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>Arquitectura del sistema</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>Ultimate, Enterprise o Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bits</p></td>
<td align="left"><p>.NET Framework 3,5 SP1</p>
<p>.NET Framework 4 (generador)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, Enterprise, Data Center o Web Server</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>.NET Framework 3,5 SP1</p>
<p>.NET Framework 4 (generador)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8</p></td>
<td align="left"><p>Enterprise o Professional Edition</p></td>
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>32 o 64 bits</p></td>
<td align="left"><p>.NET Framework 4 o .NET Framework 3,5 SP1 (agente)</p>
<p>.NET Framework 4 (generador)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>.NET Framework 4 o .NET Framework 3,5 SP1 (agente)</p>
<p>.NET Framework 4 (generador)</p></td>
</tr>
</tbody>
</table>

 

No hay requisitos especiales de RAM que sean específicos de UE-V.

La instalación del agente de UE-V requiere derechos administrativos y necesitará reiniciar el equipo antes de que se pueda ejecutar el agente de UE-V.

**Importante**  La característica sincronizar la configuración de Windows 8 debe estar deshabilitada para permitir que UE-V funcione correctamente. La sincronización de la configuración con Windows 8 y UE-V provocará un comportamiento de sincronización impredecible.

 

### <a href="" id="requirements-for-the-offline-files-feature-"></a>Requisitos para la característica de archivos sin conexión

UE-V Agent puede sincronizar la configuración de usuario en equipos que no están siempre conectados a la red de la empresa, como un equipo portátil o equipos que se encuentran en oficinas remotas, así como equipos que siempre están conectados a la red de la empresa, como servidores de Windows que hospedan sesiones de Virtual Desktop Interface (VDI).

La configuración predeterminada de UE-V usa la característica de archivos sin conexión de Windows para sincronizar la configuración. Archivos sin conexión garantiza que la configuración del usuario estará disponible incluso cuando el equipo deje la red empresarial. Los cambios que se realicen en la configuración se sincronizan automáticamente con la ubicación de almacenamiento de configuración cuando se restablece la conexión a la red de la empresa. Los archivos sin conexión también garantizan que la configuración del usuario está disponible para los equipos que se encuentran en una oficina remota con una conexión lenta o limitada.

Para sincronizar la configuración de equipos que, ocasionalmente, dejan la red empresarial, la característica archivos sin conexión debe estar habilitada e iniciarse antes de que empiece la implementación de UE-V Agent. La característica archivos sin conexión está habilitada de forma predeterminada en Windows7. La característica está deshabilitada de forma predeterminada en Windows Server2008R2, Windows Server 2012 y Windows 8. Si la característica archivos sin conexión no está habilitada, se producirá un error en la sincronización de configuración de UE-V.

-   **Windows 7**

    La característica archivos sin conexión está habilitada de forma predeterminada en Windows 7. Si es necesario, los archivos sin conexión se pueden habilitar con el comando siguiente en un símbolo del sistema con privilegios elevados:

    ``` syntax
    sc config CscService start=auto
    ```

-   **Windows 8**

    La característica archivos sin conexión está deshabilitada de forma predeterminada en la versión de Windows 8. Los archivos sin conexión se pueden habilitar en Windows 8 con el comando siguiente en un símbolo del sistema con privilegios elevados:

    ``` syntax
    sc config CscService start=auto
    ```

-   **Windows Server 2008 R2 y Windows Server 2012**

    La característica archivos sin conexión no se instala de forma predeterminada en Windows Server 2008 R2 ni en Windows Server 2012. Para habilitar la característica de archivos sin conexión, debe instalarse el paquete de experiencia de escritorio. Este es un componente de servidor opcional que incluye la característica archivos sin conexión. Una vez instalado, inicie la característica archivos sin conexión con los siguientes comandos en un símbolo del sistema con privilegios elevados:

    ``` syntax
    sc config csc start= system
    ```

    ``` syntax
    sc config cscservice start= auto
    ```

El equipo debe reiniciarse antes de que se inicie la configuración.

### Sincronización de equipos con conexiones disponibles siempre

Cuando usa UE-V en equipos que siempre están conectados a la red de la empresa, como un equipo de Windows Server que hospeda sesiones de VDI, los archivos sin conexión deberían estar deshabilitados.

Cuando UE-V Agent está configurado para sincronizar la configuración sin usar archivos sin conexión, el servidor de almacenamiento de configuración se trata como un recurso compartido de red estándar. La configuración se sincroniza cuando la red está disponible. En esta configuración, UE-V Agent se puede configurar para que dé una notificación si se retrasa la importación de la configuración de la aplicación.

Si no se va a usar la característica de archivos sin conexión, debe deshabilitar el comportamiento predeterminado de UE-V antes o durante la implementación de UE-V Agent. Para deshabilitar los archivos sin conexión de UE-V, realice una de las siguientes acciones:

-   Antes de implementar el agente de UE-V, marque la casilla "no usar archivos sin conexión" en la configuración de directiva de grupo de UE-V.

-   Durante la instalación de UE-V, establezca el parámetro AgentSetup.exe `SyncMethod = None` en el símbolo del sistema o en un archivo de proceso por lotes. Para obtener más información sobre cómo implementar el agente, consulte [implementación de UE-V Agent](deploying-the-ue-v-agent.md).

Si deshabilita la configuración de archivos sin conexión de UE-V y no especifica el parámetro **SyncMethod** en el momento de la instalación, se producirá un error en la instalación del agente de UE-v. También puede deshabilitar los archivos sin conexión con PowerShell o WMI. Para obtener más información sobre WMI y los comandos de PowerShell, vea [administrar el agente y los paquetes de 1,0 UE-V con PowerShell y WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).

El equipo debe reiniciarse antes de que se inicie la configuración.

### Requisitos previos para la característica de PowerShell de UE-V

La característica de PowerShell UE-V del agente requiere que la versión 3,5 SP1 de .NET Framework esté habilitada y PowerShell versión 2,0 o superior.

### Requisitos previos para la compatibilidad con el generador de UE-V

Instale el generador de UE-V en el equipo que se usa para crear plantillas de ubicación de configuración personalizadas. Este equipo debería tener esas aplicaciones instaladas cuya configuración será móvil. Debe ser miembro del grupo administradores en el equipo que ejecuta el software de generación de UE-V. Además, el generador de UE-V debe instalarse en un equipo que use un sistema de archivos NTFS. El software de generación de UE-V requiere .NET Framework versión 4. Para obtener más información, vea [planificación de la implementación de plantillas personalizadas para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

## Temas relacionados


[Planificación de UE-V 1.0](planning-for-ue-v-10.md)

[Preparación del entorno de UE-V](preparing-your-environment-for-ue-v.md)

[Implementación de UE-V 1.0](deploying-ue-v-10.md)

Configuraciones admitidas para la virtualización de la experiencia del usuario [implementación de la ubicación de almacenamiento de configuración de UE-V 1,0](deploying-the-settings-storage-location-for-ue-v-10.md)

[Instalación del generador de UE-V](installing-the-ue-v-generator.md)

[Implementación del agente de UE-V](deploying-the-ue-v-agent.md)

 

 





