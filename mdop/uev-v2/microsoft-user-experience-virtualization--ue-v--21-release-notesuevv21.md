---
title: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1
description: Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1
author: dansimp
ms.assetid: 79a36c77-fa0c-4651-8028-4a79763a2fd2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0677dda93f2c2dc60ec627ae0c3f4bd8c199db6c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825280"
---
# Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1


Para buscar las notas de la versión de virtualización de Microsoft User Experience (UE-V) 2,0, presione Ctrl + F.

Debe leer estas notas de la versión minuciosamente antes de instalar UE-V. Las notas de la versión contienen información necesaria para instalar correctamente la virtualización de la experiencia del usuario y contienen información adicional que no está disponible en la documentación del producto. Si hay diferencias entre estas notas de la versión y otra documentación de UE-V, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## Comentarios


Díganos lo que piensa sobre nuestra documentación de MDOP enviándonos sus comentarios y comentarios. Envíe sus comentarios sobre la documentación a [mdopdocs@microsoft.com](mailto:mdopdocs@microsoft.com?subject=UE-V%20Documentation).

## Problemas conocidos de UE-V


Esta sección contiene notas de la versión para la virtualización de la experiencia del usuario.

### Configuración de UE-V las plantillas de ubicación de Skype hacen que Skype se bloquee

Cuando un usuario genera una plantilla de ubicación de configuración válida para la aplicación de escritorio de Skype, la registra y, a continuación, inicia la aplicación de escritorio de Skype, Skype se bloquea. Un _VIOLATION de ACCESS se graba en el registro de eventos de la aplicación.

SOLUCIÓN alternativa: quite o anule el registro de la plantilla de Skype para que Skype pueda volver a trabajar.

### Los scripts existentes para instalaciones silenciosas de UE-V pueden fallar

Dos cambios realizados en el instalador de UE-V pueden hacer que los scripts de instalación silenciosa que funcionaban en versiones anteriores de UE-V fallaran al instalar UE-V 2,1. La primera es un nuevo requisito que los usuarios deben aceptar los términos de licencia y aceptar o rechazar la participación en el programa para la mejora de la experiencia del usuario (CEIP), incluso durante una instalación silenciosa. El uso del parámetro/q ya no es suficiente para indicar la aceptación de los términos de licencia y el contrato para participar en el CEIP.

En segundo lugar, el instalador fuerza el reinicio del equipo después de instalar el agente de UE-V. Esto puede provocar errores en un script de instalación si no espera reiniciar (por ejemplo, instala el agente UE-V Agent en primer lugar y, después, instala inmediatamente el generador).

SOLUCIÓN: el instalador de UE-V (. msi) tiene dos nuevos parámetros de la línea de comandos que admiten instalaciones silenciosas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parámetro</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>/ACCEPTLICENSETERMS = true</strong></p></td>
<td align="left"><p>Establezca este parámetro en <strong> true </strong> para instalar UE-V silenciosamente. Agregar este parámetro implica que el usuario acepta los términos de licencia de UE-V, que se encuentran de forma predeterminada:%ProgramFiles%\Microsoft User Experience Virtualization\Agent</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>/NORESTART</strong></p></td>
<td align="left"><p>Este parámetro impide el reinicio obligatorio una vez instalado el agente de UE-V. Un código devuelto de 3010 indica que es necesario reiniciar antes de usar UE-V.</p></td>
</tr>
</tbody>
</table>

 

### La configuración del registro no se sincroniza entre App-V y aplicaciones nativas en el mismo equipo

Cuando un equipo tiene una aplicación que se instala a través de virtualización de aplicaciones (App-V) y de forma local con un archivo de Windows Installer (. msi), la configuración basada en el registro no se sincroniza entre las tecnologías.

SOLUCIÓN alternativa: para resolver este problema, ejecute la aplicación seleccionando una de las dos tecnologías, pero no ambas.

### Resultados imprevisibles con Office 2010 y Office 2013 instalados

Cuando un usuario tiene instalado Office 2010 y Office 2013, cualquier configuración común entre las dos versiones de Office se desplazará con UE-V. Esto puede provocar que el tamaño del paquete de Office 2010 sea muy grande o que se produzcan conflictos imprevisibles con 2013, especialmente si se usa Office 365.

SOLUCIÓN alternativa: instale solo una versión de Office o limite las configuraciones que se sincronizan mediante UE-V.

### Desinstalar y volver a instalar la aplicación Windows 8 revierte la configuración al estado inicial

Al usar la sincronización de configuración de UE-V para una aplicación de Windows 8, si el usuario desinstala la aplicación y, a continuación, vuelve a instalar la aplicación, la configuración de la aplicación vuelve a sus valores predeterminados.Esto sucede porque la desinstalación quita la copia local (en caché) de la configuración de la aplicación, pero no quita el paquete de configuración local de UE-V.Cuando la aplicación se reinstale e inicie, UE-V reúna la configuración de la aplicación que se restableció a los valores predeterminados de la aplicación y, a continuación, cargará la configuración predeterminada en la ubicación de almacenamiento central.Otros equipos que ejecutan la aplicación, descargan la configuración predeterminada.Este comportamiento es idéntico al comportamiento de las aplicaciones de escritorio.

SOLUCIÓN alternativa: ninguno.

### UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Microsoft Office

Le recomendamos que instale la versión de 32 bits de Microsoft Office para sistemas operativos de 32 y 64 bits. Para elegir la versión de Microsoft Office que necesita, haga clic aquí. ([http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623)). UE-V admite la configuración de itinerancia entre versiones de arquitectura idénticas de Office. Por ejemplo, la configuración de Office de 32 bits se transferirá entre todas las instancias de Office de 32 bits. UE-V no admite la configuración de itinerancia entre las versiones de 32 y 64 bits de Office.

SOLUCIÓN alternativa: ninguna

### <a href="" id="msi-s-are-not-localized"></a>Los MSI no están localizados

UE-V 2,0 incluye un programa de instalación localizado para UE-V Agent y UE-v generator. Estos archivos MSI siguen estando disponibles, pero la interfaz de usuario está minimizada y la de MSI solo se muestra en inglés. A pesar de que el archivo está en inglés, el programa de instalación instala todos los idiomas admitidos durante la instalación.

SOLUCIÓN alternativa: ninguna

### Los favicons asociados a los favoritos de Internet Explorer 9 no se mueven

Los favicons asociados a los favoritos de Internet Explorer 9 no se desplazan por la virtualización de la experiencia del usuario y no aparecen cuando los favoritos aparecen por primera vez en un equipo nuevo.

SOLUCIÓN: favicons aparecerá con sus favoritos asociados una vez que el marcador se use y se almacene en la memoria caché en el explorador Internet Explorer 9.

### Las rutas de configuración de archivos se almacenan en el registro

Algunas opciones de la aplicación almacenan las rutas de los archivos de configuración y configuración como valores en el registro. Los archivos a los que se hace referencia como rutas en el registro se deben sincronizar cuando se mueven los valores de configuración entre equipos.

SOLUCIÓN alternativa: Use el redireccionamiento de carpetas o cualquier otra tecnología para asegurarse de que todos los archivos a los que se hace referencia como rutas de configuración de archivos están presentes y colocados en la misma ubicación en todos los equipos en los que la configuración es móvil.

### Las rutas de almacenamiento de configuración largas pueden provocar un error

Mantenga las rutas de almacenamiento de configuración tan cortas como sea posible. Las rutas largas pueden impedir la resolución o la sincronización. UE-V usa la ruta de acceso de almacenamiento de configuración como parte de la ruta de acceso calculada para almacenar la configuración. Esa ruta se calcula de la siguiente manera: configuración ruta de almacenamiento + "settingspackages" + paquete DIR (ID. de plantilla) + nombre de paquete (plantilla ID) +. pkgx. Si esa ruta de acceso calculada supera los 260 caracteres, almacenamiento de paquetes fallará y generará el siguiente mensaje de error en el registro de eventos operativos de UE-V:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Para comprobar los eventos de registro operativos, abra el visor de eventos y vaya a registros de aplicaciones y servicios/Microsoft/virtualización de la experiencia de usuario/inicio de sesión/operativo.

SOLUCIÓN alternativa: ninguno.

### Algunas configuraciones del sistema operativo solo se mueven entre las versiones del sistema operativo

La configuración del sistema operativo para narrador y los caracteres de moneda específicos de la configuración regional (es decir, la configuración regional y de idioma) solo se transferirán a las distintas versiones del sistema operativo de Windows. Por ejemplo, los caracteres de moneda no se mueven entre Windows 7 y Windows 8.

SOLUCIÓN alternativa: ninguna

### <a href="" id="ue-v-1-agent-generates-errors-when-running-ue-v-2-templates-"></a>UE-V 1 Agent genera errores cuando se ejecutan las plantillas de UE-V 2

Si una plantilla de ubicación de configuración de UE-V 2 se distribuye a un equipo instalado con un agente de UE-V 1, algunos ajustes no se sincronizan entre los equipos y el agente informa de errores en el registro de eventos.

SOLUCIÓN: al migrar de UE-V 1 a UE-V 2 y es probable que tenga equipos en los que se ejecuta la versión anterior del agente, cree un catálogo independiente de UE-V 2,0 para admitir el agente y las plantillas de UE-V 2,0.

## Revisiones y artículos de Knowledge base para UE-V 2,1


Esta sección contiene revisiones y artículos de KB para UE-V 2,1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Artículo de KB</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>3018608</p></td>
<td align="left"><p>UE-V 2,1-TemplateConsole.exe se bloquea cuando faltan las clases WMI de UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3018608/EN-US" data-raw-source="[support.microsoft.com/kb/3018608/EN-US](https://support.microsoft.com/kb/3018608/EN-US)">support.microsoft.com/kb/3018608/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2903501</p></td>
<td align="left"><p>UE-V: User Experience Virtualization (UE-V) compatibilidad con perfiles de usuario</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2903501/EN-US" data-raw-source="[support.microsoft.com/kb/2903501/EN-US](https://support.microsoft.com/kb/2903501/EN-US)">support.microsoft.com/kb/2903501/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2770042</p></td>
<td align="left"><p>Configuración del registro de UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2770042/EN-US" data-raw-source="[support.microsoft.com/kb/2770042/EN-US](https://support.microsoft.com/kb/2770042/EN-US)">support.microsoft.com/kb/2770042/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2847017</p></td>
<td align="left"><p>Configuración de UE-V replicada por Internet Explorer</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2847017/EN-US" data-raw-source="[support.microsoft.com/kb/2847017/EN-US](https://support.microsoft.com/kb/2847017/EN-US)">support.microsoft.com/kb/2847017/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769631</p></td>
<td align="left"><p>Cómo reparar una instalación de UE-V dañada</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769631/EN-US" data-raw-source="[support.microsoft.com/kb/2769631/EN-US](https://support.microsoft.com/kb/2769631/EN-US)">support.microsoft.com/kb/2769631/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2850989</p></td>
<td align="left"><p>No se admite la migración de perfiles MAPI con Microsoft UE-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850989/EN-US" data-raw-source="[support.microsoft.com/kb/2850989/EN-US](https://support.microsoft.com/kb/2850989/EN-US)">support.microsoft.com/kb/2850989/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769586</p></td>
<td align="left"><p>UE-V roaming las carpetas vacías y las claves de registro</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769586/EN-US" data-raw-source="[support.microsoft.com/kb/2769586/EN-US](https://support.microsoft.com/kb/2769586/EN-US)">support.microsoft.com/kb/2769586/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2782997</p></td>
<td align="left"><p>Cómo habilitar el registro de depuración en la virtualización de la experiencia del usuario de Microsoft (UE-V)</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2782997/EN-US" data-raw-source="[support.microsoft.com/kb/2782997/EN-US](https://support.microsoft.com/kb/2782997/EN-US)">support.microsoft.com/kb/2782997/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2769570</p></td>
<td align="left"><p>UE-V no actualiza el tema en sesiones de RDS o VDI</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2769570/EN-US" data-raw-source="[support.microsoft.com/kb/2769570/EN-US](https://support.microsoft.com/kb/2769570/EN-US)">support.microsoft.com/kb/2769570/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2850582</p></td>
<td align="left"><p>Cómo usar la virtualización de la experiencia del usuario de Microsoft con aplicaciones de App-V</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2850582/EN-US" data-raw-source="[support.microsoft.com/kb/2850582/EN-US](https://support.microsoft.com/kb/2850582/EN-US)">support.microsoft.com/kb/2850582/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>3041879</p></td>
<td align="left"><p>Versiones de archivo actuales para la virtualización de la experiencia del usuario de Microsoft</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3041879/EN-US" data-raw-source="[support.microsoft.com/kb/3041879/EN-US](https://support.microsoft.com/kb/3041879/EN-US)">support.microsoft.com/kb/3041879/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2843592</p></td>
<td align="left"><p>Información sobre la virtualización de la experiencia del usuario y alta disponibilidad</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2843592/EN-US" data-raw-source="[support.microsoft.com/kb/2843592/EN-US](https://support.microsoft.com/kb/2843592/EN-US)">support.microsoft.com/kb/2843592/EN-US</a></p></td>
</tr>
</tbody>
</table>

 






 

 





