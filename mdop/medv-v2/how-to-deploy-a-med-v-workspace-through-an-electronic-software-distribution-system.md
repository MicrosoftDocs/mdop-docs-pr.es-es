---
title: Cómo implementar un área de trabajo de MED-V a través de un sistema de distribución electrónica de Software
description: Cómo implementar un área de trabajo de MED-V a través de un sistema de distribución electrónica de Software
author: dansimp
ms.assetid: b5134c35-e1de-470c-93f8-ead6218d9dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56d21b0c2f010f63c04056d9fadd7763531bd9d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812991"
---
# Cómo implementar un área de trabajo de MED-V a través de un sistema de distribución electrónica de Software


Un sistema electrónico de distribución de software está diseñado para mover el software de forma eficaz a muchos equipos distintos a través de conexiones de red lentas o rápidas. La siguiente sección proporciona información e instrucciones para ayudarle a implementar el área de trabajo de MED-V en toda su empresa mediante un sistema de distribución de software.

**Nota**  
Sea cual sea la solución de distribución de software que use, debe estar familiarizado con los requisitos de su solución en particular. Si está usando System Center Configuration Manager 2007 R2 o una versión posterior, consulte la [biblioteca de documentación de Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=66999) en la biblioteca técnica de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=66999) .



**Importante**  
Si está usando System Center Configuration Manager 2007 SP2 y las áreas de trabajo de MED-V están configuradas para funcionar en modo **NAT** , las máquinas virtuales se clasifican como clientes basados en Internet y no pueden encontrar los puntos de distribución más cercanos para descargar contenido.

El [hotfix para mejorar la funcionalidad de las VM administradas por Med-v](https://go.microsoft.com/fwlink/?LinkId=201088) ( https://go.microsoft.com/fwlink/?LinkId=201088) agrega nueva funcionalidad a las máquinas virtuales administradas por Med-v y que están configuradas para funcionar en modo **NAT** . La nueva funcionalidad permite que las máquinas virtuales tengan acceso a los puntos de distribución más cercanos. Por lo tanto, el administrador puede administrar la máquina virtual y el equipo host de la misma manera. Este Hotfix debe instalarse primero en el servidor del sitio y, después, en el cliente.

La actualización está disponible públicamente. Sin embargo, es posible que se le pida que acepte un contrato de servicios de Microsoft. Siga las indicaciones en las páginas web sucesivas para recuperar este Hotfix.



También puede implementar los componentes de MED-V juntos mediante un archivo de proceso por lotes, pero para ello es necesario reiniciar después de la instalación de Windows Virtual PC. Para evitar este requisito, puede especificar un solo reinicio una vez que se hayan instalado todos los componentes. El reinicio único también inicia de forma automática MED-V porque la instalación del área de trabajo MED-V coloca una entrada en el RUNKEY.

**Para implementar un área de trabajo de MED-V mediante un sistema de distribución de software**

1.  Definir un grupo de equipos y usuarios en el sistema electrónico de distribución de software como el conjunto de destino de equipos o usuarios.

2.  Cree paquetes para cada archivo de instalación de Microsoft que deba distribuirse. A continuación se indican los archivos necesarios y el orden en el que se deben instalar:

    1.  **Windows Virtual PC** : Si no está instalado (es necesario reiniciar el equipo). Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).

    2.  **Adiciones y actualizaciones de Windows Virtual PC** : Si aún no están instaladas. Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).

    3.  **Archivo de instalación del agente de host Med-v** : instala el agente de host (MED-v \ _HostAgent \ _setup archivo de instalación). Para obtener más información, vea [Cómo instalar manualmente el agente de host MED-V](how-to-manually-install-the-med-v-host-agent.md).

        **Advertencia**  
        Cierre Internet Explorer antes de instalar el agente de host MED-V; de lo contrario, los conflictos pueden producirse posteriormente con el redireccionamiento de URL. También puede hacerlo especificando un reinicio del equipo durante una distribución.



    4.  **Instalador de área de trabajo de Med-v, VHD y ejecutable de configuración** : creados en el **Empaquetador de área de trabajo de Med-v**. Para obtener más información, vea [crear un paquete de área de trabajo de MED-V](create-a-med-v-workspace-package.md).

        **Importante**  
        El archivo de disco duro virtual comprimido (. medv) y el programa de instalación ejecutable (setup.exe) deben estar en la misma carpeta que el instalador del área de trabajo de MED-V. Después, instale el instalador de área de trabajo MED-V ejecutando setup.exe.



~~~
    **Tip**  
    Because problems can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



3. Configure los paquetes para que se ejecuten en modo silencioso (no es necesaria la intervención del usuario).

   Si se ejecuta en modo silencioso, se elimina la solicitud de cerrar Internet Explorer si está en ejecución y se pide iniciar el agente de host MED-V. Ambas acciones se realizan cuando se reinicia el equipo.

   **Nota**  
   La instalación de Windows Virtual PC requiere que reinicie el equipo. Puede crear un único proceso de instalación e instalar todos los componentes al mismo tiempo si elimina el reinicio e ignora los requisitos previos necesarios para que MED-V se instale. También puede hacerlo con los argumentos de la línea de comandos. Para obtener un ejemplo de estos argumentos, consulte [cómo implementar los componentes de MED-V a través de un sistema electrónico de distribución de software](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md#bkmk-batch). MED-V se inicia automáticamente cuando se reinicia el equipo.



4. Instale MED-V y sus componentes antes de instalar Windows Virtual PC. Vea el archivo de proceso por lotes de ejemplo más adelante en este tema.

   **Importante**  
   Seleccione la opción **omitir \ _PREREQUISITES** como se muestra en el archivo de proceso por lotes de ejemplo para que los componentes de MED-V puedan instalarse antes que los componentes de VPC requeridos. Instale los componentes de MED-V en este orden para permitir el reinicio único.



5. Identifique cualquier otro requisito necesario para la instalación y para el sistema de distribución de software, como plataformas de destino y el espacio libre en disco.

6. Asigne los paquetes al conjunto de equipos de destino de equipos o usuarios.

   Mientras se ejecutan los equipos, el cliente del sistema de distribución de software reconoce que hay nuevos paquetes disponibles y comienza a instalar los paquetes según la definición y los requisitos. Las instalaciones deben ejecutarse secuencialmente en modo silencioso. Recomendamos que se realice como un único proceso que no requiera reiniciar hasta que se instalen todos los paquetes.

7. Una vez completadas las instalaciones, reinicie los equipos actualizados.

   Según el sistema de distribución de software, puede programar un reinicio del equipo o los usuarios finales podrán reiniciar los equipos manualmente durante su trabajo normal. Después de reiniciar el equipo, MED-V se inicia automáticamente después de que un usuario final inicie sesión. Cuando MED-V se inicia por primera vez, se ejecuta la configuración primera vez.

La configuración comienza por primera vez y puede tardar varios minutos en completarse, según el tamaño del disco duro virtual que especificó y el número de directivas aplicadas al área de trabajo de MED-V en el inicio. El usuario final puede realizar un seguimiento del progreso observando el icono de MED-V en el área de notificación. Para obtener más información sobre la configuración de la primera vez, vea [información general sobre la implementación de 2,0 MED-V](med-v-20-deployment-overview.md).

**Para instalar el área de trabajo de MED-V mediante un archivo por lotes**

1.  Ejecute la instalación en un símbolo del sistema con credenciales administrativas.

2.  Implemente cada componente en un solo directorio. Si se ejecuta desde un recurso compartido de red, se necesita más tiempo para descomprimir el archivo. medv.

3.  Como práctica recomendada, especifique que Windows Virtual PC y la revisión de Windows Virtual PC se instalen después del agente de host MED-V y los archivos de paquete del área de trabajo MED-V. Esto significa que Windows Update no causará ninguna interferencia con el proceso de instalación al requerir un reinicio.

4.  Reinicie el equipo una vez que haya finalizado el archivo por lotes.

Después del reinicio, se le solicitará al usuario que ejecute la configuración por primera vez y se completará la configuración de MED-V.

En el siguiente ejemplo, con los argumentos especificados, se muestra cómo instalar componentes de MED-V de 64 bits en un único proceso:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Argumento</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/norestart</p></td>
<td align="left"><p>Impide que la instalación de Windows Virtual PC y la actualización de Virtual PC de Windows reinicie el equipo host.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/Quiet</p></td>
<td align="left"><p>Instala los componentes de MED-V en modo silencioso sin interacción del usuario.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/QN</p></td>
<td align="left"><p>Instala los componentes de MED-V sin una interfaz de usuario.</p></td>
</tr>
<tr class="even">
<td align="left"><p>IGNORE_PREREQUISITES</p></td>
<td align="left"><p>Instala sin comprobar Windows Virtual PC.</p>
<div class="alert">
<strong>Nota</strong><br/><p>Especifique este argumento solo si va a instalar Windows Virtual PC como parte de esta instalación.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>OVERWRITEVHD</p></td>
<td align="left"><p>Fuerza la instalación del área de trabajo de MED-V y evita las preguntas que pueda generar.</p></td>
</tr>
</tbody>
</table>



## Ejemplo


``` syntax
:: Install MED-V and the Pre-requisites

:: Install the MED-V Host Agent: install in quiet mode, ignore that Windows Virtual PC is not installed completely, and log results
start /WAIT .\MED-V_HostAgent_Setup.exe /qn IGNORE_PREREQUISITES=1 /l* %TEMP%\MEDVhost.log

:: Install the MED-V Workspace: install in quiet mode, Overwrite the VHD if it already exists, and log results
start /WAIT .\setup.exe /qn OVERWRITEVHD=1 /l* %TEMP%\MEDVworkspace.log

:: Install Windows Virtual PC: install in quiet mode and do not reboot
start /WAIT wusa.exe Windows6.1-KB958559-x64.msu /norestart /quiet

:: Install Windows Virtual PC patch to support non-HAV: install in quiet mode and do not reboot
wusa.exe Windows6.1-KB977206-x64.msu /norestart /quiet

:: After successful installation of the above components, a reboot of the host computer is required to complete installation.
```

## Temas relacionados


[Introducción a la implementación MED-V 2.0](med-v-20-deployment-overview.md)

[Cómo implementar un área de trabajo de MED-V en una imagen de Windows 7](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)









