---
title: Procedimientos recomendados de MED-V 2.0
description: Procedimientos recomendados de MED-V 2.0
author: dansimp
ms.assetid: 47ba2dd1-6c6e-4d6e-8e18-b42291f8e02a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7b664d33b403b821ce6bc9c045d937380ab4f91b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826111"
---
# Procedimientos recomendados de MED-V 2.0


Al planear, implementar y administrar MED-V en su empresa, es posible que las recomendaciones de procedimientos recomendados sean útiles.

### Configurar la configuración de primera vez para ejecutarse de forma desatendida

Aunque puede especificar la configuración que prefiera, una práctica recomendada de MED-V es crear el archivo Sysprep. inf para que la primera configuración se pueda ejecutar en modo **desatendido** . Esto requiere que proporcione toda la información de configuración necesaria a medida que continúa con el Asistente para **Administración de instalación** . Para obtener más información sobre cómo configurar la imagen de MED-V, vea [configurar una imagen de Windows Virtual PC para Med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).

### Deshabilitar puntos de restauración en la máquina virtual

Antes de crear el paquete de área de trabajo MED-V, le recomendamos que deshabilite los puntos de restauración en la máquina virtual para evitar que el disco de diferenciación crezca sin límites. Para obtener más información, consulte [Cómo desactivar y activar Restaurar sistema en Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .

### Configurar la imagen de MED-V para usar perfiles locales

Le recomendamos que aplique solo las directivas que tengan sentido en un entorno de compatibilidad de aplicaciones para Windows XP. Por ejemplo, las directivas de personalización de escritorio no tienen que aplicarse por lo general y deben deshabilitarse. Para obtener más información sobre cómo permitir solo perfiles locales, consulte [configuración de directiva de grupo para perfiles de usuarios móviles](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .

### Configurar una actualización de rendimiento de directiva de grupo

De forma predeterminada, la Directiva de grupo se descarga en un equipo de un byte cada vez. Esto provoca retrasos cuando se une MED-V al dominio. Para aumentar el rendimiento de la Directiva de grupo, le recomendamos que establezca el valor de la siguiente clave del registro en el registro:

Subclave del registro: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon

Entrada: BufferPolicyReads

Tipo: DWORD

Valor: 1

### Distribuir avisos legales mediante la Directiva de grupo en lugar de hacerlo en la imagen MED-V

Si desea que los usuarios finales vean un contrato de nivel de servicio (SLA) antes de que tengan acceso a MED-V, le recomendamos que aplique el SLA mediante la Directiva de grupo más adelante para que se muestre el SLA al usuario final después de que finalice la primera configuración.

**PRECAUCIÓN**  Aunque un procedimiento recomendado es ejecutar la configuración por primera vez en modo **desatendido** , si decide establecer la directiva local o la entrada del registro para incluir un SLA en la imagen (disco duro virtual), también debe especificar que la primera configuración se ejecute en modo **atendido** o que la primera vez que se produzcan errores.

 

### Compactar el disco duro virtual

Le recomendamos que compacte el disco duro virtual para recuperar espacio en disco vacío y reduzca el tamaño del disco duro virtual. Para obtener más información sobre cómo compactar el disco duro virtual, vea [compactar el disco duro virtual de MED-V](compacting-the-med-v-virtual-hard-disk.md).

### Configurar la máquina virtual para que se reinicie en pantalla azul

Le recomendamos que configure la máquina virtual de área de trabajo de MED-V para que se reinicie automáticamente cuando detecte un bloqueo de pantalla azul. Para configurar esta opción en el invitado, establezca el valor AutoReboot en la clave HKEY \ _LOCAL \ _MACHINE \\SYSTEM\\CurrentControlSet\\Control\\CrashControl en "1".

También puede configurar esta opción si hace clic en **Inicio**, haga clic en **Panel de control**y, a continuación, haga clic en **sistema**. A continuación, en el área **Inicio y recuperación** de la pestaña **avanzadas** , haga clic en **configuración**. Seleccione la casilla **reinicio automático** y haga clic en **Aceptar**.

### Hacer una copia de seguridad de la imagen de MED-V antes de sellarla

Le recomendamos que cree una copia de seguridad de la imagen de MED-V antes de sellarla. Para obtener más información sobre cómo sellar la imagen de MED-V, vea [configurar una imagen de Windows Virtual PC para Med-v](configuring-a-windows-virtual-pc-image-for-med-v.md).

### Instalar Windows Virtual PC al instalar desde un archivo por lotes

Al instalar los componentes de MED-V mediante un archivo por lotes, especifique que Windows Virtual PC y la revisión de Windows Virtual PC se instalen después del agente de host MED-V y los archivos de paquete del área de trabajo MED-V. Esto garantiza que Windows Update no cause ninguna interferencia con el proceso de instalación al requerir un reinicio.

### Instalar el área de trabajo de MED-V desde una carpeta local

Debido a problemas que se pueden producir al instalar MED-V desde una ubicación de red, le recomendamos que copie los archivos de configuración del área de trabajo de MED-V localmente y, a continuación, ejecute setup.exe.

### <a href="" id="manage-printer-redirection-in-one-manner-only-"></a>Administrar la redirección de la impresora solo de una manera

Si una impresora se instala manualmente en la máquina virtual invitado MED-V, y la misma impresora se instala posteriormente en el equipo host, el resultado es que se instala dos veces en el invitado. Para evitar esta situación, le recomendamos que el procedimiento recomendado es MED-V para administrar el redireccionamiento de impresoras solo de una manera: deshabilite el redireccionamiento e instale las impresoras manualmente en el invitado, o bien habilite el redireccionamiento y no instale las impresoras de forma manual en el invitado.

### <a href="" id="configure-settings-for-med-v-guest-patching-"></a>Establecer la configuración de la revisión de invitados de MED-V

Puede controlar cuándo y durante cuánto tiempo despierta la máquina virtual de MED-V para recibir actualizaciones automáticas definiendo los valores de configuración pertinentes en el registro. Un procedimiento recomendado de MED-V es configurar el intervalo de activación para que coincida con el momento en el que se han programado las actualizaciones regulares para las máquinas virtuales de MED-V. Además, le recomendamos que configure estas opciones de forma que se asemeje al comportamiento del equipo host.

Para obtener más información sobre cómo configurar las opciones para la revisión de invitados de MED-V, consulte [administrar actualizaciones automáticas para áreas de trabajo de Med-v](managing-automatic-updates-for-med-v-workspaces.md).

### Configurar software antivirus y de copia de seguridad

Para evitar que la actividad antivirus afecte al rendimiento del escritorio virtual, le recomendamos que, cuando pueda, excluya los siguientes tipos de archivo de máquina virtual de cualquier proceso de copia de seguridad o antivirus que se ejecute en el equipo host MED-V:

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. EXPIRA

## Temas relacionados


[Seguridad y protección de MED-V](security-and-protection-for-med-v.md)

 

 





