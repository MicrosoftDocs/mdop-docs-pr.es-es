---
title: Planificación de las aplicaciones a sincronizar con UE-V 1.0
description: Planificación de las aplicaciones a sincronizar con UE-V 1.0
author: dansimp
ms.assetid: c718274f-87b4-47f3-8ef7-5e1bd5557a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f2b04942588d0f6efad03d5e0249534cd325c09
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812415"
---
# Planificación de las aplicaciones a sincronizar con UE-V 1.0


La virtualización de la experiencia del usuario de Microsoft (UE-V) usa plantillas de ubicación de configuración (archivos XML) que definen la configuración que captura y aplica UE-V. UE-V incluye un conjunto de plantillas de ubicación de configuración predefinidas y también permite a los administradores crear plantillas de ubicación de configuración personalizada para aplicaciones de terceros o de línea de negocio que se usan en la empresa.

Como administrador, cuando considere qué aplicaciones incluir en su solución de UE-V, considere qué opciones puede personalizar un usuario y cómo y dónde se almacenará la aplicación. No todas las aplicaciones tienen opciones de configuración que se pueden personalizar o que los usuarios personalizan rutinariamente. Además, no todas las configuraciones de aplicaciones pueden moverse de forma segura en varios equipos o entornos. Sincronizar la configuración que cumpla los siguientes criterios:

-   Configuración que se almacena en ubicaciones accesibles para el usuario. Por ejemplo, no sincronice la configuración almacenada en la sección de de system32 o exterior HKCU del registro.

-   Configuración que no es específica del equipo en particular. Por ejemplo, excluya la configuración de red o de hardware.

-   Configuración que se puede sincronizar entre equipos sin riesgo de datos dañados. Por ejemplo, no use la configuración almacenada en un archivo de base de datos.

## Plantillas de ubicación de configuración incluidas en UE-V


**Plantillas de ubicación de configuración de aplicación de UE-V**

El software de instalación de UE-V Agent instala el agente y registra un grupo predeterminado de plantillas de ubicación de configuración para las aplicaciones comunes de Microsoft. Estas plantillas de ubicación de configuración capturan valores de configuración para las siguientes aplicaciones:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Categoría de aplicación</strong></th>
<th align="left"><strong>Descripción</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aplicaciones de Microsoft Office 2010</p></td>
<td align="left"><p>Microsoft Word 2010</p>
<p>Microsoft Excel 2010</p>
<p>Microsoft Outlook 2010</p>
<p>Microsoft Access 2010</p>
<p>Microsoft Project 2010</p>
<p>Microsoft PowerPoint 2010</p>
<p>Microsoft Publisher 2010</p>
<p>Microsoft Visio 2010</p>
<p>Microsoft SharePoint Workspace 2010</p>
<p>Microsoft InfoPath 2010</p>
<p>Microsoft Lync 2010</p>
<p>Microsoft OneNote 2010</p></td>
</tr>
<tr class="even">
<td align="left"><p>Opciones del explorador (Internet Explorer 8, Internet Explorer 9 e Internet Explorer 10)</p></td>
<td align="left"><p>Favoritos, Página principal, pestañas y barras de herramientas.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Accesorios de Windows</p></td>
<td align="left"><p>Calculadora, Bloc de notas, WordPad.</p></td>
</tr>
</tbody>
</table>

 

La configuración de la aplicación se aplica a la aplicación cuando se inicia la aplicación. Se guardan cuando se cierra la aplicación.

**Plantillas de ubicación de configuración de UE-V Windows**

La virtualización de la experiencia del usuario incluye plantillas de ubicación de configuración que capturan valores de configuración para la siguiente configuración de Windows:

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Configuración de Windows</th>
<th align="left">Descripción</th>
<th align="left">Aplicar en</th>
<th align="left">Estado predeterminado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Fondo de escritorio</p></td>
<td align="left"><p>Actualmente está activo el fondo de escritorio.</p></td>
<td align="left"><p>Iniciar sesión, desbloquear, conexión remota.</p></td>
<td align="left"><p>Habilitado</p></td>
</tr>
<tr class="even">
<td align="left"><p>Accesibilidad</p></td>
<td align="left"><p>Accesibilidad y configuración de entrada, lupa, narrador y teclado en pantalla.</p></td>
<td align="left"><p>Iniciar sesión, desbloquear, conexión remota.</p></td>
<td align="left"><p>Deshabilitado</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuración del escritorio</p></td>
<td align="left"><p>Configuración del menú Inicio y de la barra de tareas, opciones de carpeta, iconos predeterminados del escritorio, relojes adicionales y configuración de región e idioma.</p></td>
<td align="left"><p>Solo inicio de sesión.</p></td>
<td align="left"><p>Deshabilitado</p></td>
</tr>
</tbody>
</table>

 

La configuración de la accesibilidad y el fondo de escritorio de Windows se aplica cuando el usuario inicia sesión, cuando el equipo está desbloqueado o cuando se trata de una conexión remota a otro equipo. El agente guarda esta configuración cuando el usuario cierra la sesión, cuando el equipo está bloqueado o cuando se desconecta una conexión remota. De forma predeterminada, la configuración de fondo de escritorio de Windows se mueve entre equipos con la misma versión del sistema operativo.

La configuración del escritorio de Windows y de accesibilidad se aplica al iniciar sesión antes de que se presente al usuario el escritorio. Para optimizar la experiencia de inicio de sesión, esta configuración no se mueve de forma predeterminada. La configuración del escritorio y la facilidad de acceso se puede habilitar mediante la Directiva de grupo, PowerShell y WMI.

UE-V no admite la itinerancia de configuración entre sistemas operativos con distintos idiomas. Por ejemplo, no es compatible con la sincronización entre el inglés y el alemán. El idioma de todos los equipos a los que UE-V roaming la configuración del usuario debe coincidir.

**Nota:**  Si cambia las plantillas de ubicación de configuración que proporciona Microsoft, es posible que la característica de virtualización de la experiencia del usuario no funcione correctamente para el grupo de configuración de Windows o la aplicación designada.

 

## <a href="" id="prevent-unintentional-user-settings-configuration-"></a>Evitar la configuración de un usuario no intencionado


La virtualización de la experiencia del usuario comprueba la información de la nueva configuración de usuario y la descarga según corresponda desde una ubicación de almacenamiento de configuración. A continuación, aplica la configuración al equipo local en los casos siguientes:

-   Cada vez que se inicia una aplicación que tiene una plantilla registrada de UE-V.

-   Cuando un usuario inicia sesión en el equipo.

-   Cuando un usuario desbloquea su equipo.

-   Cuando se establece una conexión con un equipo de escritorio remoto que tiene UE-V instalado.

Si UE-V está instalado en el equipo a y en el equipo B, y la configuración deseada para la aplicación en el equipo A, el equipo a debe abrir y cerrar la aplicación en primer lugar. Si una aplicación se abre y cierra en el equipo B, la configuración de la aplicación en el equipo a se configurará para que sea la misma que la configuración de la aplicación en el equipo B.

Este escenario también se aplica a la configuración de Windows. Si la configuración de Windows en el equipo B debe ser la misma que la configuración de Windows del equipo A, entonces el usuario debe iniciar sesión y cerrar la sesión en primer lugar.

Si la configuración de usuario deseada se aplica en el orden equivocado, se puede recuperar ejecutando una operación de restauración para la aplicación específica o configuración de Windows en el equipo en el que se sobrescribió la configuración. Para obtener más información, consulte restauración de la [aplicación y configuración de Windows sincronizada con UE-V 1,0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).

## Plantillas de ubicación de configuración personalizada de UE-V


Puede crear plantillas de ubicación de configuración personalizadas con el generador de UE-V. Después de crear y probar una plantilla de ubicación de configuración personalizada en un entorno de prueba, puede implementar las plantillas de ubicación de configuración en los equipos de la empresa. Las plantillas de ubicación de configuración personalizada deben implementarse con una infraestructura de implementación existente, como el método de distribución de software empresarial (ESD), con preferencias, o mediante la configuración de un catálogo de plantillas de configuración de UE-V. Las plantillas implementadas con ESD o una directiva de grupo se deben registrar con el WMI o PowerShell de UE-V. Para obtener más información sobre las plantillas de ubicación de configuración personalizada, consulte [planificación de la implementación de plantillas personalizadas para UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

Para obtener instrucciones sobre si debe sincronizarse una aplicación de línea de negocio, vea [lista de comprobación para evaluar las aplicaciones de línea de negocio de UE-V 1,0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).

## Temas relacionados


[Planificación de UE-V 1.0](planning-for-ue-v-10.md)

[Planificación de la implementación de la plantilla personalizada para UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Implementación de UE-V 1.0](deploying-ue-v-10.md)

 

 





