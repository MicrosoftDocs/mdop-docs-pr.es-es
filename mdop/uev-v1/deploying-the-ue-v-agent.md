---
title: Implementación del agente de UE-V
description: Implementación del agente de UE-V
author: dansimp
ms.assetid: ec1c16c4-4be0-41ff-93bc-3e2b1afb5832
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 19f3b798ad7d3a43b0a274a25dd97b651435de51
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827181"
---
# Implementación del agente de UE-V


El agente de virtualización de la experiencia del usuario de Microsoft (UE-V) debe ejecutarse en todos los equipos que usen la configuración de Windows y la aplicación de UE-V a roaming. Un solo archivo de instalación, AgentSetup.exe, instala UE-V Agent en los sistemas operativos de 32 y 64 bits. Los parámetros de la línea de comandos de UE-V Agent son los siguientes:

**Parámetros de la línea de comandos de AgentSetup.exe**

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Parámetro de la línea de comandos</strong></th>
<th align="left"><strong>Definición</strong></th>
<th align="left"><strong>Notas</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/Help o/h o/?</p></td>
<td align="left"><p>Muestra el cuadro de diálogo de uso de AgentSetup.exe.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p>SettingsStoragePath</p></td>
<td align="left"><p>Indica la ruta de acceso UNC (Convención de nomenclatura universal) que define dónde se almacena la configuración.</p></td>
<td align="left"><p>se aceptan las variables de entorno% username% o% COMPUTERNAME%. Las secuencias de comandos pueden requerir variables de escape.</p>
<p><strong>Valor predeterminado </strong> : &lt; ninguno &gt; (inicio de usuario de Active Directory)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SettingsTemplateCatalogPath</p></td>
<td align="left"><p>Indica la ruta de acceso UNC (Convención de nomenclatura universal) que define la ubicación en la que se comprobó la configuración de nuevas plantillas de ubicación de configuración.</p></td>
<td align="left"><p>Solo es necesario para las plantillas de ubicación de configuración personalizada</p></td>
</tr>
<tr class="even">
<td align="left"><p>RegisterMSTemplates</p></td>
<td align="left"><p>Especifica si se deben registrar las plantillas predeterminadas de Microsoft durante la instalación.</p></td>
<td align="left"><p>Verdadero | Valor</p>
<p><strong>Valor predeterminado </strong> : verdadero</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncMethod</p></td>
<td align="left"><p>Especifica qué método de sincronización debe usarse.</p></td>
<td align="left"><p>OfflineFiles | Nada</p>
<p><strong>Valor predeterminado </strong> : OfflineFiles</p></td>
</tr>
<tr class="even">
<td align="left"><p>SyncTimeoutInMilliseconds</p></td>
<td align="left"><p>Especifica el número de milisegundos que el equipo espera antes de que se agote el tiempo de espera cuando recupera la configuración de usuario de la ubicación de almacenamiento de configuración.</p></td>
<td align="left"><p><strong>Valor predeterminado </strong> : 2000 milisegundos</p>
<p>(espera hasta 2 segundos)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>SyncEnabled</p></td>
<td align="left"><p>Especifica si la sincronización de UE-V está habilitada o deshabilitada.</p></td>
<td align="left"><p>Verdadero | Valor</p>
<p><strong>Valor predeterminado </strong> : verdadero</p></td>
</tr>
<tr class="even">
<td align="left"><p>MaxPackageSizeInBytes</p></td>
<td align="left"><p>Especifica el tamaño de archivo de un paquete de configuración en bytes cuando el agente de UE-V notifica que los archivos superan el umbral.</p></td>
<td align="left"><p>&lt;su&gt;</p>
<p><strong>Valor predeterminado </strong> : ninguno (no hay umbral de advertencia)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CEIPEnabled</p></td>
<td align="left"><p>Especifica la configuración de participación en el programa para la mejora de la experiencia del usuario. Si se establece en verdadero, la información del instalador se carga en el sitio del programa para la mejora de la experiencia del usuario de Microsoft. Si se establece en falso, no se carga la información.</p></td>
<td align="left"><p>Verdadero | Valor</p>
<p><strong>Valor predeterminado </strong> : falso</p>
<p><strong>En Windows 7 </strong> : verdadero</p></td>
</tr>
</tbody>
</table>

 

Durante la instalación, el parámetro de la línea de comandos SettingsStoragePath especifica la ubicación de almacenamiento de configuración para los valores de configuración. Se puede definir una ubicación de almacenamiento de configuración antes de implementar el agente de UE-V. Si no se define ninguna ubicación de almacenamiento de configuración, UE-V usa el directorio principal de usuario de Active Directory como la ubicación de almacenamiento de configuración. Cuando especifique la configuración de SettingsStoragePath durante la instalación y use el% username% como parte del valor, esta tendrá la misma experiencia de configuración de usuario en todos los equipos o sesiones en los que un usuario inicie sesión. Si especifica las variables de%username%\\%COMPUTERNAME% como parte del valor de SettingsStoragePath, se conservará la experiencia de configuración de cada equipo.

Los archivos de Windows Installer (. msi) específicos de la arquitectura se proporcionan para la instalación del agente de UE-V, además del instalador combinado de 32 y 64 bits. Los archivos de instalación de AgentSetupx86.msi o AgentSetupx64.msi son más pequeños que el AgentSetup.exe archivo y pueden simplificar las implementaciones del agente. Los parámetros de la línea de comandos para el instalador de AgentSetup.exe son compatibles con la instalación de Windows Installer (. msi).

**Nota:**  Durante la instalación o desinstalación del agente UE-V, puede usar el archivo AgentSetup.exe o el &lt; &gt; archivo AgentSetup. msi, pero no ambos. El mismo archivo debe usarse para desinstalar el agente de UE-V, ya que se usó para instalar el agente de UE-V.

 

Asegúrese de usar el formato de variable correcto al instalar el agente de UE-V. En la tabla siguiente se proporcionan ejemplos de opciones de implementación para usar el AgentSetup.exe o los archivos de instalación de Windows Installer (. msi).

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Tipo de implementación</strong></th>
<th align="left"><strong>Descripción de la implementación</strong></th>
<th align="left"><strong>Ejemplo</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Símbolo del sistema</p></td>
<td align="left"><p>Cuando instale UE-V Agent desde un símbolo del sistema, use el formato de variable% ^ username%. Si se necesitan comillas porque hay espacios en la ruta de almacenamiento de configuración, use un archivo de script por lotes para la implementación.</p>
<p></p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%^username%</code></p></td>
</tr>
<tr class="even">
<td align="left"><p>Script por lotes</p></td>
<td align="left"><p>Cuando instale UE-V Agent desde un archivo de script por lotes, use el formato de variable%% username%%. Si usas este método de instalación, debes escapar la variable con los%% caracteres. Sin este carácter, el script expande la variable de nombre de usuario en el momento de la instalación, en lugar de hacerlo en tiempo de ejecución, lo que hace que UE-V use una sola ubicación de almacenamiento de configuración para todos los usuarios.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=&quot;\server\settingsshare%%username%%&quot;</code></p>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>PowerShell</p></td>
<td align="left"><p>Cuando instale UE-V Agent desde un símbolo del sistema de PowerShell o un script de PowerShell, use el formato de variable% username%.</p></td>
<td align="left"><p><code>&amp; AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p>
<p><code>&amp; msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l<em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare%username%</code></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p>Distribución electrónica de software, como la implementación de la implementación de software de Configuration Manager)</p></td>
<td align="left"><p>Al instalar el agente de UE-V con Configuration Manager, use el formato de variable ^% username ^%.</p></td>
<td align="left"><p><code>AgentSetup.exe /quiet /norestart /log &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p>
<p></p>
<p><code>msiexec.exe /i &quot;&lt;path to msi file&gt;&quot; /quiet /norestart /l</em>v &quot;%temp%\UE-VAgentInstaller.log&quot; SettingsStoragePath=\server\settingsshare^%username^%</code></p></td>
</tr>
</tbody>
</table>

 

**Nota:**  La instalación del agente de U-EV requiere derechos de administrador y el equipo necesitará un reinicio antes de que se pueda ejecutar el agente de UE-V.

 

## Métodos de implementación del agente de UE-V desde un recurso compartido de red


Puede usar los siguientes métodos para implementar el agente de UE-V:

-   Una solución de distribución electrónica de software (ESD) que puede instalar un archivo de Windows Installer (. msi).

-   Un script de instalación que hace referencia al archivo de Windows Installer (. msi) que se almacena centralmente en un recurso compartido.

-   Ejecutar manualmente el programa de instalación en el equipo.

Para implementar el agente UE-V desde un recurso compartido de red, siga estos pasos:

**Para instalar y configurar el agente UE-V desde un recurso compartido de red**

1.  Fase el archivo de instalación de UE-V Agent (AgentSetup.exe) en un recurso compartido de red al que los usuarios tienen permiso de "lectura".

2.  Implementar una secuencia de comandos en equipos de usuario que instala UE-V Agent. El script debe especificar la ubicación de almacenamiento de configuración.

**Actualizar el agente de UE-V**

Las actualizaciones para el software del agente UE-V se proporcionarán a través de Microsoft Update. Durante una actualización de UE-V Agent, se puede actualizar el grupo predeterminado de plantillas de ubicación de configuración para las aplicaciones comunes de Microsoft y la configuración de Windows. Las actualizaciones de los agentes de UE-V se pueden implementar mediante la infraestructura de distribución de software empresarial (ESD).

## Temas relacionados


[Implementación de UE-V 1.0](deploying-ue-v-10.md)

[Configuraciones admitidas para UE-V 1.0](supported-configurations-for-ue-v-10.md)

[Implementación de la ubicación de almacenamiento de configuración de UE-V 1.0](deploying-the-settings-storage-location-for-ue-v-10.md)

[Instalación del generador de UE-V](installing-the-ue-v-generator.md)

Implementar el agente de virtualización de la experiencia del usuario
 

 





