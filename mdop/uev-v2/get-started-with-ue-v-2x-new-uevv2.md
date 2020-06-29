---
title: Introducción a UE-V 2.x
description: Introducción a UE-V 2.x
author: dansimp
ms.assetid: 526ecbf0-0dee-4f0b-b017-8f8d25357b14
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 02/13/2017
ms.openlocfilehash: d3f01dd67ea9e5f6cfcf5dc3425265deff3f7df1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823290"
---
# Introducción a UE-V 2.x


Siga los pasos que se indican en esta guía para implementar rápidamente la virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0 o 2,1 en un entorno de prueba pequeño. Esto le ayuda a determinar si UE-V es la solución adecuada para administrar la configuración de usuario en varios dispositivos de su empresa.

**Nota:**  La información de esta sección se repite con más detalle en el resto de la documentación. Por lo tanto, si ya sabe que UE-V 2 es la solución adecuada y no necesita evaluarla, puede ir directamente a [preparar una implementación de UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md).

 

La instalación estándar de UE-V sincroniza la configuración predeterminada de Microsoft Windows y Office, así como la mayoría de las opciones de la aplicación de Windows. Asegúrese de que su entorno de prueba incluya dos o más equipos de usuario que compartan el acceso a la red y que va a evaluar UE-V en poco tiempo.

-   [Paso 1: confirmar los requisitos previos](#step1): Asegúrese de que su entorno puede ejecutar UE-V, incluyendo detalles sobre las configuraciones admitidas.

-   [Paso 2: implementar la ubicación de almacenamiento de configuración de UE-V 2](#step2): todas las implementaciones de UE-v requieren una ubicación para los paquetes de configuración que contienen los valores de configuración sincronizados.

-   [Paso 3: implementar el agente de UE-v 2](#step3): para sincronizar la configuración con UE-v, los dispositivos deben tener el agente UE-v instalado y en ejecución.

-   [Paso 4: probar la implementación de evaluación de UE-v 2](#step4): ejecute algunas pruebas en dos equipos que tengan instalado UE-v Agent y vea el funcionamiento de UE-v.

¡ Así está! Una vez que hayas seguido los pasos, podrás evaluar cómo UE-V puede funcionar en tu empresa.

**Evaluación adicional:** También puede realizar pasos adicionales para configurar algunas aplicaciones de línea de negocio y de terceros para sincronizar su configuración mediante UE-V, tal como se detalla en [deploy UE-v 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md).

## <a href="" id="step1"></a>Paso 1: confirmar los requisitos previos


Antes de continuar, asegúrese de que su entorno incluye los siguientes requisitos para la ejecución de UE-V.

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Sistema operativo</strong></th>
<th align="left"><strong>Edición</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>Arquitectura del sistema</strong></th>
<th align="left"><strong>Windows PowerShell</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>7</p></td>
<td align="left"><p>Ultimate, Enterprise o Professional Edition</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32 o 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 o superior</p></td>
<td align="left"><p>.NET Framework 4 o superior</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, Enterprise, Datacenter o Web Server</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 o superior</p></td>
<td align="left"><p>.NET Framework 4 o superior</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 8.1</p></td>
<td align="left"><p>Enterprise o Pro</p></td>
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>32 o 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 o superior</p></td>
<td align="left"><p>4,5 de .NET Framework</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2012 o Windows Server 2012 R2</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 o superior</p></td>
<td align="left"><p>4,5 de .NET Framework</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows 10, pre-1607 Verison</p></td>
<td align="left"><p>Enterprise o Pro</p></td>
<td align="left"><p></p></td>
<td align="left"><p>32 o 64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 o superior</p></td>
<td align="left"><p>4,5 de .NET Framework</p></td>
</tr>
<tr class="even">
<td align="left"><p>WindowsServer2016</p></td>
<td align="left"><p>Standard o Datacenter</p></td>
<td align="left"><p>Ninguno</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>Windows PowerShell 3,0 o superior</p></td>
<td align="left"><p>4,5 de .NET Framework</p></td>
</tr>
</tbody>
</table>

**Nota:** A partir de Windows 10, versión 1607, UE-V está incluida en [Windows 10 para empresas](https://www.microsoft.com/WindowsForBusiness/windows-for-enterprise) y ya no forma parte del paquete de optimización de escritorio de Microsoft

También...

-   **Licencia de MDOP:** Esta tecnología es parte del paquete de optimización de escritorio de Microsoft (MDOP). Los clientes empresariales pueden obtener MDOP con Microsoft Software Assurance. Para obtener más información sobre Microsoft Software Assurance y cómo adquirir MDOP, consulte ¿Cómo puedo obtener MDOP ( https://go.microsoft.com/fwlink/p/?LinkId=322049) .

-   **Credenciales administrativas** de cualquier equipo en el que vaya a instalarlo

## <a href="" id="step2"></a>Paso 2: implementar la ubicación de almacenamiento de configuración de UE-V 2


Tendrá que implementar una ubicación de almacenamiento de configuración, un recurso compartido de red estándar en el que se almacena la configuración de usuario en un archivo de paquete de configuración. Al crear el recurso de almacenamiento de configuración, debe limitar el acceso a los usuarios que lo necesiten. [Implementar una ubicación de almacenamiento de configuración](https://technet.microsoft.com/library/dn458891.aspx#ssl) proporciona información más detallada.

**Crear un recurso compartido de red**

1.  Cree un nuevo grupo de seguridad y agréguele a los usuarios de UE-V.

2.  Cree una nueva carpeta en el equipo centralizado que almacena los paquetes de configuración de UE-V y, a continuación, conceda a los usuarios de UE-V acceso con permisos de grupo a la carpeta. El administrador que admita UE-V debe tener permisos para esta carpeta compartida.

3.  Asigne permisos de usuarios de UE-V para crear un directorio cuando se conecten. Conceda permiso total a todos los subdirectorios de ese directorio, pero no bloquee el acceso a nada anterior.

    1.  Establezca los siguientes permisos de bloque de mensajes de servidor (SMB) de nivel de recurso compartido para la carpeta de ubicación de almacenamiento de configuración.

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong>Cuenta de usuario</strong></th>
        <th align="left"><strong>Permisos recomendados</strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Todos</p></td>
        <td align="left"><p>No hay permisos</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Grupo de seguridad de los usuarios de UE-V</p></td>
        <td align="left"><p>Control total</p></td>
        </tr>
        </tbody>
        </table>

         

    2.  Establezca los siguientes permisos del sistema de archivos NTFS en la carpeta de ubicación de almacenamiento de configuración.

        <table>
        <colgroup>
        <col width="33%" />
        <col width="33%" />
        <col width="33%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><strong>Cuenta de usuario</strong></th>
        <th align="left"><strong>Permisos recomendados</strong></th>
        <th align="left"><strong>Carpeta</strong></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Creador/propietario</p></td>
        <td align="left"><p>Control total</p></td>
        <td align="left"><p>Solo subcarpetas y archivos</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Grupo de seguridad de los usuarios de UE-V</p></td>
        <td align="left"><p>Listar carpeta/leer datos, crear carpetas/anexar datos</p></td>
        <td align="left"><p>Solo esta carpeta</p></td>
        </tr>
        </tbody>
        </table>

         

**Nota de seguridad:**

Si crea el recurso de almacenamiento de configuración en un equipo que ejecuta un sistema operativo Windows Server, configure UE-V para comprobar que el grupo de administradores local o el usuario actual es el propietario de la carpeta donde se almacenan los paquetes de configuración. Para habilitar esta seguridad adicional, especifique esta configuración en el editor del registro de Windows Server:

1.  Agregue una clave del registro **reg \ _DWORD** denominada **"RepositoryOwnerCheckEnabled"** a **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\uev\\agent\\configuration**.

2.  Establezca el valor de la clave del registro en *1*.

## <a href="" id="step3"></a>Paso 3: implementar el agente de UE-V 2


El agente UE-V sincroniza la configuración de las aplicaciones y de Windows entre los equipos y los dispositivos de los usuarios. Para fines de evaluación, instale el agente en al menos dos equipos del entorno de prueba que pertenezcan al mismo usuario.

Ejecute el archivo AgentSetup.exe desde la línea de comandos para instalar el agente de UE-V. Se instala en sistemas operativos de 32 y 64 bits.

``` syntax
AgentSetup.exe SettingsStoragePath=\\server\settingsshare\%username%
```

Debe especificar el parámetro de la línea de comandos SettingsStoragePath como el recurso compartido de red del paso 2. [Implementar un agente de UE-V](https://technet.microsoft.com/library/dn458891.aspx#agent) proporciona información más detallada.

## <a href="" id="step4"></a>Paso 4: probar la implementación de la evaluación de UE-V 2


Ahora puede ejecutar algunas pruebas en la implementación de evaluación de UE-V para ver cómo funciona UE-V.

****

1.  En el primer equipo (equipo A), realice uno o varios de estos cambios:

    1.  Abra el escritorio de Windows y mueva la barra de tareas a otra ubicación en la ventana.

    2.  Cambie las fuentes predeterminadas.

    3.  Abra Calculator y establezca el valor en **científico**.

    4.  Cambie el comportamiento de cualquier aplicación de Windows, como se detalla en [administrar las plantillas de ubicación de configuración de UE-V 2. x con Windows PowerShell y WMI](managing-ue-v-2x-settings-location-templates-using-windows-powershell-and-wmi-both-uevv2.md).

    5.  Deshabilitar la sincronización y los perfiles de itinerancia de configuración de la cuenta de Microsoft.

2.  Cierre la sesión en el equipo A. la configuración se guarda en un paquete de configuración de UE-V cuando los usuarios bloquean, cierran sesión, salen de una aplicación o cuando se ejecuta el proveedor de sincronización (cada 30 minutos de forma predeterminada).

3.  Inicie sesión en el segundo equipo (el equipo B) como el mismo usuario que el equipo A.

4.  Abra el escritorio de Windows y compruebe que la ubicación de la barra de tareas coincide con la del equipo A. Compruebe que las fuentes predeterminadas coinciden y que esa calculadora se establece en **científica**. Además, verifica el cambio que realizaste en cualquier aplicación de Windows.

Puede cambiar la configuración del equipo B a la configuración del equipo original. Cierre la sesión con el equipo B e inicie sesión en el equipo a para comprobar los cambios.

## Otros recursos para este producto


-   [Virtualización de la experiencia del usuario de Microsoft (UE-V) 2. x](index.md)

-   [Preparar una implementación de UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

-   [Administración de UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

-   [Solución de problemas de UE-V 2. x](troubleshooting-ue-v-2x-both-uevv2.md)

-   [Referencia técnica de UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)






 

 





