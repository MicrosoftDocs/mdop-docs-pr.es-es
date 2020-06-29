---
title: Opciones de línea de comandos para archivos de instalación de MED-V
description: Opciones de línea de comandos para archivos de instalación de MED-V
author: dansimp
ms.assetid: 7b8cd3e4-1d09-44a0-b690-f85b0d0a6b02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 39582a592a59a4d0e81ef406edc6a984497275c7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826470"
---
# Opciones de línea de comandos para archivos de instalación de MED-V


Al instalar o desinstalar Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, tiene la opción de ejecutar los archivos de instalación en el símbolo del sistema. En esta sección se describen las diferentes opciones que puede especificar al instalar o desinstalar MED-V en el símbolo del sistema.

### Argumentos de la línea de comandos

Puede usar los siguientes argumentos de la línea de comandos junto con sus respectivos archivos de instalación de MED-V.

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
<th align="left">Archivo de instalación</th>
<th align="left">Argumento</th>
<th align="left">Valores aceptados</th>
<th align="left">Tipo</th>
<th align="left">Descripción</th>
<th align="left">Predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Agente de host</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;Ruta de instalación&gt;</p></td>
<td align="left"><p>Instalación</p></td>
<td align="left"><p>Cambiar directorio instalado</p></td>
<td align="left"><p>La instalación va a programar la virtualización de escritorio de Programa\microsoft Enterprise.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Empaquetador de área de trabajo MED-V</p></td>
<td align="left"><p>MEDVDIR</p></td>
<td align="left"><p>&lt;Ruta de instalación&gt;</p></td>
<td align="left"><p>Instalación</p></td>
<td align="left"><p>Cambiar directorio instalado</p></td>
<td align="left"><p>La instalación va a programar la virtualización de escritorio de Programa\microsoft Enterprise.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Área de trabajo MED-V</p></td>
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;Ruta de instalación&gt;</p></td>
<td align="left"><p>Instalación</p></td>
<td align="left"><p>Cambiar directorio instalado</p></td>
<td align="left"><p>La instalación va a ProgramData\Microsoft\Medv\Workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Área de trabajo MED-V</p></td>
<td align="left"><p>SOBRESCRIBIR VHD</p></td>
<td align="left"><p>0 o 1</p></td>
<td align="left"><p>Instalación</p></td>
<td align="left"><p>Error de instalación si hay VHD (0) o sobrescribe el VHD existente (1).</p></td>
<td align="left"><p>La sobrescritura no se produce y se produce un error en la instalación si ya existe un disco duro virtual (VHD).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Área de trabajo MED-V</p></td>
<td align="left"><p>SUPPRESSMEDVLAUNCH</p></td>
<td align="left"><p>0 o 1</p></td>
<td align="left"><p>Instalación</p></td>
<td align="left"><p>Iniciar (0) o no comenzar (1) MED-V después de instalar el área de trabajo de MED-V.</p></td>
<td align="left"><p>Si el área de trabajo de MED-V se instaló con la interfaz de usuario (IU), una casilla en la <strong> </strong> Página finalizar controla si debe iniciar MED-V.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Área de trabajo MED-V</p></td>
<td align="left"><p>DELETEDIFFDISKS</p></td>
<td align="left"><p>0 o 1</p></td>
<td align="left"><p>Desinstalación</p></td>
<td align="left"><p>Mantener (0) o eliminar (1) VHD creados por MED-V</p></td>
<td align="left"><p>No se eliminan los VHD.</p></td>
</tr>
</tbody>
</table>

 

### Ejemplos de argumentos de la línea de comandos

En el ejemplo siguiente se instala el área de trabajo MED-V creada por el Empaquetador de área de trabajo MED-V. El archivo de instalación crea un archivo de registro en el directorio Temp y ejecuta el archivo de instalación en modo silencioso, pero no inicia el agente de host MED-V al finalizar. El archivo de instalación sobrescribe cualquier VHD que haya detrás de una instalación anterior que tenga el mismo nombre.

``` syntax
setup.exe /l* %temp%\medv-workspace-install.log /qn SUPPRESSMEDVLAUNCH=1 OVERWRITEVHD=1
```

En el siguiente ejemplo se desinstala el área de trabajo de MED-V que se instaló previamente. El archivo de instalación crea un archivo de registro en el directorio Temp y ejecuta el archivo de instalación en modo silencioso. El archivo de instalación elimina cualquier archivo de disco duro virtual restante del sistema de archivos.

``` syntax
%ProgramData%\Microsoft\Medv\Workspace\uninstall.exe /l* %temp%\medv-workspace-uninstall.log /qn DELETEDIFFDISKS=1
```

## Temas relacionados


[Implementar los componentes MED-V](deploy-the-med-v-components.md)

[Referencia técnica de MED-V](technical-reference-for-med-v.md)

 

 





