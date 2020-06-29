---
title: Guía para el rendimiento de virtualización de aplicaciones 5.0
description: Guía para el rendimiento de virtualización de aplicaciones 5.0
author: dansimp
ms.assetid: 6b3a3255-b957-4b9b-8bfc-a93fe8438a81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b0f5ef07935fc34adce772e7b2fff85a12b01dc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813535"
---
# Guía para el rendimiento de virtualización de aplicaciones 5.0


Aprenda a configurar App-V 5,0 para obtener un rendimiento óptimo, optimizar paquetes de aplicaciones virtuales y ofrecer una mejor experiencia de usuario con RDS y VDI.

La implementación de varios métodos puede ayudarte a mejorar la experiencia del usuario final. Sin embargo, es posible que su entorno no admita todos los métodos.

Debe leer y comprender la siguiente información antes de leer este documento.

-   [Guía del administrador de Microsoft Application Virtualization 5,0](microsoft-application-virtualization-50-administrators-guide.md)

-   [Publicación de aplicaciones de aplicación-V 5 SP2 e interacción del cliente](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [Guía de secuenciación de Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/?LinkId=269953)

**Nota**  
Algunos términos que se usan en este documento pueden tener diferentes significados según el origen y el contexto externos. Para más información sobre los términos que se usan en este documento seguidos de un asterisco **\\** *, revise la sección terminología de la [Guía de rendimiento de virtualización](#bkmk-terms1) de la aplicación en este documento.



Por último, este documento le proporcionará la información para configurar el equipo que ejecuta el cliente de App-V 5,0 y el entorno para un rendimiento óptimo. Optimice los paquetes de aplicaciones virtuales para el rendimiento con el secuenciador y aprenda a usar la virtualización de la experiencia del usuario (UE-V) u otras tecnologías de administración del entorno de usuario para ofrecer una experiencia de usuario óptima con App-V 5,0 en servicios de escritorio remoto (RDS) y en la infraestructura de escritorio virtual no persistente (VDI).

Para ayudarle a determinar qué información es relevante para su entorno, debe revisar la breve descripción general de cada sección y la lista de comprobación de aplicabilidad.

## <a href="" id="---------app-v-5-0-in-stateful--non-persistent-deployments"></a> App-V 5,0 en estado \ * implementaciones no persistentes


Esta sección proporciona información sobre un enfoque que ayuda a garantizar que el usuario tendrá acceso a todas las aplicaciones virtuales en segundos después de iniciar sesión. Esto se logra aplicando la actualización de la publicación App-V 5,0 de ejecución de larga duración. Como verá la base del enfoque, la actualización de publicación más rápida es una que no tiene que hacer nada realmente. Se deben cumplir una serie de condiciones y los pasos seguidos para proporcionar una experiencia óptima para el usuario.

Use la información de la siguiente sección para obtener más información:

[Escenarios de uso](#bkmk-us) : al revisar los dos escenarios, tenga en cuenta que este es el enfoque. En función de sus requisitos de uso, puede optar por aplicar estos pasos a un subconjunto de usuarios o paquetes de aplicaciones virtuales.

-   Optimizado para el rendimiento: para ofrecer la experiencia óptima, puede esperar que la imagen base incluya parte del paquete de aplicaciones virtual de App-V. Se tratan estos y otros requisitos.

-   Optimizado para el almacenamiento: Si le preocupa el impacto en el almacenamiento, el cumplimiento de este escenario le ayudará a resolver esos problemas.

[Preparación del entorno](#bkmk-pe)

-   Pasos para preparar la imagen base: ya sea en un entorno VDI o RDSH no persistente, solo se deben completar unos pocos pasos en la imagen base para habilitar este enfoque.

-   Use UE-V 2,0 como solución de administración de perfiles de usuario (UPM) para el enfoque de App-V: la piedra angular de este enfoque es la capacidad de una solución UEM de conservar el contenido de pocas pocas ubicaciones del registro y los archivos. Estas ubicaciones constituyen la integración de usuarios \ *. Asegúrese de revisar los requisitos específicos para la solución de UPM.

[Tutorial de experiencia del usuario](#bkmk-uewt)

-   Tutorial: esta es una guía paso a paso de las operaciones de App-V y UE-V, así como las expectativas de los usuarios.

-   Resultado: describe los resultados esperados.

[Impacto en el ciclo de vida del paquete](#bkmk-plc)

[Mejorar la experiencia de VDI mediante la optimización y el ajuste del rendimiento](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a>Lista de comprobación de aplicabilidad

Entorno de implementación

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>VDI o RDSH no persistente.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Virtualización de la experiencia del usuario (UE-V), otras soluciones de UPM o discos de Perfil de usuario (UPD).</p></td>
</tr>
</tbody>
</table>



Configuración esperada

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Virtualización de la experiencia del usuario (UE-V) con la plantilla de estado de usuario de App-V habilitada o el software de administración de perfiles de usuario (UPM). El software UPM que no es UE-V debe poder activar el inicio de sesión o el inicio y cierre de sesión de la aplicación.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>El almacén de contenido compartido de App-V (SCS) está configurado o se puede configurar.</p></td>
</tr>
</tbody>
</table>



Administración de ti

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Es posible que el administrador necesite actualizar la imagen base de la VM regularmente para garantizar un rendimiento óptimo o que el administrador necesite administrar varias imágenes para grupos de usuarios diferentes.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a>Escenario de uso

Mientras revisa los dos escenarios, tenga en cuenta que estos enfoques se aproximan a los extremos. En función de sus requisitos de uso, puede elegir aplicar estos pasos a un subconjunto de usuarios, paquetes de aplicaciones virtuales o ambos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Optimizado para el rendimiento</th>
<th align="left">Optimizado para el almacenamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Para ofrecer la mejor experiencia de usuario, este enfoque aprovecha las capacidades de una solución de UPM y requiere una mayor preparación de la imagen y puede suponer un overhead adicional de administración de imágenes.</p>
<p>A continuación se describen varias mejoras de rendimiento en implementaciones no persistentes con estado. Para obtener más información, consulte el <strong> apartado pasos de secuenciación para optimizar los paquetes para el rendimiento de publicación </strong> y la referencia a la guía de <strong> secuenciación de 5,0 de App-V </strong> en la <strong> sección Vea también de este documento </strong> .</p></td>
<td align="left"><p>Las expectativas generales del escenario anterior aún se aplican aquí. Sin embargo, tenga en cuenta que las imágenes de VMs generalmente se almacenan en arreglos de discos muy costosos; se ha realizado una ligera alteración del enfoque. No configure previamente paquetes de aplicaciones virtuales dirigidos al usuario en la imagen base.</p>
<p>El impacto de esta modificación se detalla en la sección tutorial sobre la experiencia del usuario de este documento.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a>Preparación del entorno

En la tabla siguiente se muestran los pasos necesarios para preparar la imagen base y la versión de UE-V u otra solución UPM para el enfoque.

**Preparar la imagen base**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Optimizado para el rendimiento</th>
<th align="left">Optimizado para el almacenamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p>Instale el paquete de Hotfix 4 para la versión de cliente de Application Virtualization 5,0 SP2 del cliente.</p></li>
<li><p>Instale UE-V y descargue la plantilla de configuración de App-V de la galería de plantillas de UE-V, consulte los siguientes pasos.</p></li>
<li><p>Configurar el modo para el almacén de contenido compartido (SCS). Para obtener más información, vea <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> Cómo instalar el cliente de App-V 5,0 para el modo de almacén de contenido compartido </a> .</p></li>
<li><p>Configure la configuración de preservar integraciones del usuario en el registro DWORD.</p></li>
<li><p>Configurar previamente todos los paquetes de destino global y de usuario, por ejemplo, <strong> Add-AppvClientPackage </strong> .</p></li>
<li><p>Configure previamente todos los grupos de conexión de usuario y de destino global, por ejemplo, <strong> Add-AppvClientConnectionGroup </strong> .</p></li>
<li><p>Publicar previamente todos los paquetes de destino global.</p>
<p></p>
<p>También</p>
<ul>
<li><p>Realizar una publicación o actualización global.</p></li>
<li><p>Realizar una publicación o actualización de usuario.</p></li>
<li><p>Cancelar la publicación de todos los paquetes dirigidos al usuario.</p></li>
<li><p>Elimine las siguientes entradas de usuario de sistema de archivos virtual (VFS).</p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Instale el paquete de Hotfix 4 para la versión de cliente de Application Virtualization 5,0 SP2 del cliente.</p></li>
<li><p>Instale UE-V y descargue la plantilla de configuración de App-V de la galería de plantillas de UE-V, consulte los siguientes pasos.</p></li>
<li><p>Configurar el modo para el almacén de contenido compartido (SCS). Para obtener más información, vea <a href="how-to-install-the-app-v-50-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.0 Client for Shared Content Store Mode](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)"> Cómo instalar el cliente de App-V 5,0 para el modo de almacén de contenido compartido </a> .</p></li>
<li><p>Configure la configuración de preservar integraciones del usuario en el registro DWORD.</p></li>
<li><p>Preconfigurar todos los paquetes de destino global, por ejemplo, <strong> Add-AppvClientPackage </strong> .</p></li>
<li><p>Configure previamente todos los grupos de conexión de destino global, por ejemplo, <strong> Add-AppvClientConnectionGroup </strong> .</p></li>
<li><p>Publicar previamente todos los paquetes de destino global.</p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



**Configuraciones** -para configuraciones de cliente de App-V críticas y un poco más de contexto y procedimientos, revise la siguiente información:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Opción de configuración</th>
<th align="left">¿Qué hace?</th>
<th align="left">¿Cómo debo usarlo?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Modo de almacén de contenido compartido (SCS)</p>
<ul>
<li><p>Configurable en PowerShell con <strong> set-AppvClientConfiguration </strong> – <strong> SharedContentStoreMode </strong> , o bien</p></li>
<li><p>Durante la instalación del cliente de App-V 5,0.</p></li>
</ul></td>
<td align="left"><p>Al ejecutar el almacén de contenido compartido solo se mantienen los datos de publicación en el disco duro; los demás recursos virtuales de la aplicación se mantienen en la memoria (RAM).</p>
<p>Esto ayuda a conservar el almacenamiento local y a minimizar la e/s de disco por segundo (IOPS).</p></td>
<td align="left"><p>Esta opción se recomienda cuando hay disponibles conexiones de baja latencia entre el extremo del cliente de App-V y el servidor de contenido de SCS, SAN.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PreserveUserIntegrationsOnLogin</p>
<ul>
<li><p>Configure en el registro en <strong> software de HKEY_LOCAL_MACHINE </strong>  \  <strong> integración del cliente de </strong>  \  <strong> Microsoft </strong>  \  <strong> AppV </strong>  \  <strong> </strong>  \  <strong> </strong> .</p></li>
<li><p>Cree el valor DWORD <strong> PreserveUserIntegrationsOnLogin </strong> con el valor <strong> 1 </strong> .</p></li>
<li><p>Reinicie el servicio de cliente de App-V o reinicie el equipo que ejecuta el cliente de App-V.</p></li>
</ul></td>
<td align="left"><p>Si no ha preconfigurado ( <strong> Add-AppvClientPackage </strong> ) un paquete específico y esta configuración no está configurada, el cliente de App-V se desintegrará * las integraciones de usuarios persistentes y, a continuación, se volverá a integrar *.</p>
<p>Para cada paquete que cumpla las condiciones anteriores, lo más eficaz es que el trabajo se realizará durante la publicación o actualización.</p></td>
<td align="left"><p>Si no tiene previsto configurar previamente todos los paquetes de usuario disponibles en la imagen base, use esta configuración.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxConcurrentPublishingRefresh</p>
<ul>
<li><p>Configure en el registro en <strong> HKEY_LOCAL_MACHINE </strong> &lt; &gt; software eficaz publicación de </strong>  \  <strong> </strong>  \  <strong> </strong> &lt; cliente strong de Microsoft AppV &gt; </strong>  \  <strong> </strong> .</p></li>
<li><p>Cree el valor DWORD <strong> MaxConcurrentPublishingrefresh </strong> con el número máximo deseado de actualizaciones de publicación simultáneas.</p></li>
<li><p>No es necesario reiniciar el servicio de cliente de App-V ni el equipo.</p></li>
</ul></td>
<td align="left"><p>Esta configuración determina el número de usuarios que pueden realizar una actualización/sincronización de publicación al mismo tiempo. El valor predeterminado es sin límite.</p></td>
<td align="left"><p>Limitar el número de actualizaciones de publicación simultáneas evita un uso excesivo de la CPU que podría afectar al rendimiento del equipo. Este límite se recomienda en un entorno de RDS, en el que varios usuarios pueden iniciar sesión en el mismo equipo al mismo tiempo y realizar una sincronización de actualización de publicación.</p>
<p>Si se alcanza el umbral de actualización de publicaciones simultáneas, el tiempo necesario para publicar nuevas aplicaciones y ponerlas a disposición de los usuarios finales después de iniciar sesión podría tardar un período de tiempo indeterminado.</p></td>
</tr>
</tbody>
</table>



### Configurar la solución de UE-V para el enfoque de App-V

Se recomienda usar la virtualización de la experiencia del usuario de Microsoft (UE-V) para capturar y centralizar la configuración de la aplicación y del sistema operativo Windows de un usuario específico. Esta configuración se aplicará a los diferentes equipos a los que el usuario tiene acceso, como equipos de escritorio, equipos portátiles y sesiones de infraestructura de escritorio virtual (VDI). UE-V está optimizado para los escenarios de RDS y VDI.

Para obtener más información, vea [Introducción a la virtualización de la experiencia del usuario 2,0](https://technet.microsoft.com/library/dn458936.aspx)

En esencia, todo lo que se necesita es instalar el cliente UE-V y descargar la siguiente plantilla de configuración de App-V de Microsoft de la [Galería de plantillas de Microsoft User Experience Virtualization (UE-V)](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33). Registrar la plantilla. Para obtener más información sobre las plantillas de UE-V, vea [el recurso específico de UE-v para adquirir y registrar la plantilla](https://technet.microsoft.com/library/dn458936.aspx).

**Nota**  
Si no se realiza un paso de configuración adicional, la virtualización del entorno de usuario de Microsoft (UE-V) no podrá sincronizar los accesos directos del menú Inicio (archivos. lnk) en el equipo de destino. El tipo de archivo. lnk se excluye de forma predeterminada.

UE-V solo admitirá la eliminación del tipo de archivo. lnk de la lista de exclusión en los escenarios de RDS y VDI, donde cada dispositivo de usuario tendrá el mismo conjunto de aplicaciones instaladas en la misma ubicación y todos los archivos. lnk serán válidos para todos los dispositivos de los usuarios. Por ejemplo, UE-V no admitirá actualmente los dos escenarios siguientes, porque el resultado neto será que el acceso directo será válido en uno, pero no en todos los dispositivos.

-   Si un usuario tiene una aplicación instalada en un dispositivo con archivos. lnk habilitado y la misma aplicación nativa instalada en otro dispositivo en una raíz de instalación diferente con archivos. lnk habilitados.

-   Si un usuario tiene una aplicación instalada en un dispositivo, pero no otra con los archivos. lnk habilitados.



**Importante**  
En este tema se describe cómo cambiar el registro de Windows mediante el editor del registro. Si cambia incorrectamente el registro de Windows, puede causar serios problemas que le obliguen a reinstalar Windows. Debe hacer una copia de seguridad de los archivos de registro (System. dat y User. dat) antes de cambiar el registro. Microsoft no puede garantizar que los problemas que puedan surgir al cambiar el registro se puedan resolver. Cambie el registro bajo su propia responsabilidad.



Con el editor del registro de Microsoft (regedit.exe), vaya a **HKEY \ _LOCAL \ _MACHINE**  \\  **software**  \\  **Microsoft**  \\  **UEV**  \\  **Agent**  \\  **Configuration**  \\  **ExcludedFileTypes** y quite **. lnk** de los tipos de archivos excluidos.

**Configurar otra solución de administración de perfiles de usuario (UPM) para el enfoque de App-V**

La expectativa en un entorno con estado es que se implementa una solución de UPM y puede admitir la persistencia de datos de usuario entre sesiones y entre inicios de sesión.

Los requisitos para la solución de UPM son los siguientes.

Para habilitar una experiencia de inicio de sesión optimizada, por ejemplo, el enfoque de App-V 5,0 para el usuario, la solución debe ser capaz de:

-   Conservar las siguientes integraciones de usuarios como parte del perfil de usuario/persona.

-   Activación de una sincronización de perfiles de usuario en el inicio de sesión (o inicio de la aplicación), que puede garantizar la aplicación de todas las integraciones del usuario antes de que se inicie la publicación o actualización, o bien,

-   Adjuntar y separar un disco de Perfil de usuario (UPD) o una tecnología similar que contiene las integraciones del usuario.

-   Captura de cambios en las ubicaciones, que constituyen las integraciones del usuario antes de cerrar sesión.

Con App-V 5,0 al agregar un servidor de publicación (**Add-AppvPublishingServer**) puede configurar la sincronización para, por ejemplo, la actualización durante el inicio de sesión y/o después de un intervalo de actualización determinado. En ambos casos se crea una tarea programada.

En versiones anteriores de App-V 5,0, las tareas programadas se configuraban con un VBScript que iniciaba el usuario y la actualización global. Con el paquete de revisiones 4 para Application Virtualization 5,0 SP2, la actualización de usuario al iniciar sesión es iniciada por **SyncAppvPublishingServer.exe**. Este cambio se presentó para proporcionar soluciones de UPM para un proceso de desencadenamiento. Este proceso retrasará la/Refresh de publicación para permitir que la solución de UPM aplique las integraciones de usuario. Se cerrará cuando se complete la publicación/actualización.

**Integraciones de usuarios**

Registro: HKEY \ _CURRENT \ _USER

-   Ruta de acceso-Software\\Classes

    Excluir: configuración local, ActivatableClasses, AppX \ *

-   Ruta de acceso-Software\\Microsoft\\AppV

-   Ruta de acceso: rutas Software\\Microsoft\\Windows\\CurrentVersion\\App

**Ubicaciones de archivos**

-   Raíz: "variable de entorno" APPDATA

    Ruta: Microsoft\\AppV\\Client\\Catalog

-   Raíz: "variable de entorno" APPDATA

    Ruta: Microsoft\\AppV\\Client\\Integration

-   Raíz: "variable de entorno" APPDATA

    Ruta: Microsoft\\Windows\\Start Menu\\Programs

-   (Para conservar todos los accesos directos del escritorio, virtuales y no virtuales)

    Raíz: "KnownFolder" {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} FileMask-\ *. lnk

**Virtualización de la experiencia del usuario de Microsoft (UE-V)**

Además, le recomendamos que use la virtualización de la experiencia del usuario de Microsoft (UE-V) para capturar y centralizar la configuración de la aplicación y del sistema operativo Windows para un usuario específico. Esta configuración se aplicará a los diferentes equipos a los que el usuario tiene acceso, como equipos de escritorio, equipos portátiles y sesiones de infraestructura de escritorio virtual (VDI).

Para obtener más información, vea [Introducción a la virtualización de la experiencia del usuario 1,0](https://technet.microsoft.com/library/jj680015.aspx) y [compartir plantillas de ubicación de configuración con la galería de plantillas de UE-V](https://technet.microsoft.com/library/jj679972.aspx).

### <a href="" id="bkmk-uewt"></a>Tutorial de experiencia del usuario

Este es un tutorial paso a paso de las operaciones de App-V y UPM y las expectativas que los usuarios deben esperar.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Optimizado para el rendimiento</th>
<th align="left">Optimizado para el almacenamiento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Después de implementar este enfoque en el entorno VDI/RDSH, en el primer inicio de sesión,</p>
<ul>
<li><p>Tarea Se inicia la publicación o actualización de un usuario. (Expectativa) Si es la primera vez que un usuario ha publicado aplicaciones virtuales (por ejemplo, no persistentes), esta tendrá la duración normal de una publicación o actualización.</p></li>
<li><p>Tarea Después de la publicación/actualización, la solución UPM captura las integraciones de usuario. (Expectativa) En función de cómo esté configurada la solución UPM, esto puede suceder como parte del proceso de cierre de sesión. Esto provocará una sobrecarga similar a la de mantener el estado del usuario.</p></li>
</ul>
<p>En inicios de sesión posteriores:</p>
<ul>
<li><p>Tarea El UPM de soluciones aplica las integraciones del usuario al sistema antes de la publicación/actualización.</p>
<p>(Expectativa) Habrá accesos directos en el escritorio o en el menú Inicio, que funcionan inmediatamente. Cuando se completa la publicación/actualización (es decir, cambian los derechos de paquete), algunos pueden desaparecer.</p></li>
<li><p>Tarea La publicación/actualización procesará las operaciones de no publicación y publicación de los cambios en los derechos de paquete de usuario. (Expectativa) Si no hay cambios de derecho, publishing1 se completará en segundos. De lo contrario, la publicación o actualización aumentará en relación con el número y la complejidad * de las aplicaciones virtuales.</p></li>
<li><p>Tarea La solución UPM capturará las integraciones del usuario de nuevo al cerrar sesión. (Expectativa) Igual que el anterior.</p></li>
</ul>
<p>¹ la operación de publicación ( <strong> publicar-AppVClientPackage </strong> ) agrega entradas al catálogo de usuarios, asigna derechos al usuario, identifica el almacén local y termina completando los pasos de integración.</p></td>
<td align="left"><p>Después de implementar este enfoque en el entorno VDI/RDSH, en el primer inicio de sesión,</p>
<ul>
<li><p>Tarea Se inicia la publicación o actualización de un usuario. (Expectativa)</p>
<ul>
<li><p>Si es la primera vez que un usuario ha publicado aplicaciones virtuales (por ejemplo, no persistentes), esta tendrá la duración normal de una publicación o actualización.</p></li>
<li><p>El primero y los inicios de sesión subsiguientes se verán afectados por la preconfiguración de paquetes (Agregar/actualizar).</p>
<p></p></li>
</ul></li>
<li><p>Tarea Después de la publicación/actualización, la solución UPM captura las integraciones de usuario. (Expectativa) En función de cómo esté configurada la solución UPM, esto puede suceder como parte del proceso de cierre de sesión. Esto provocará una sobrecarga similar a la de mantener el estado del usuario</p></li>
</ul>
<p>En inicios de sesión posteriores:</p>
<ul>
<li><p>Tarea El UPM de soluciones aplica las integraciones del usuario al sistema antes de la publicación/actualización.</p></li>
<li><p>Tarea Agregar/actualizar debe configurar previamente todas las aplicaciones de destino del usuario. (Expectativa)</p>
<ul>
<li><p>Esto puede aumentar significativamente el tiempo de disponibilidad de las aplicaciones (en el orden de 10 segundos).</p></li>
<li><p>Esto incrementará el tiempo de actualización de la publicación en relación con el número y la complejidad * de las aplicaciones virtuales.</p>
<p></p></li>
</ul></li>
<li><p>Tarea La publicación/actualización procesará las operaciones de no publicación y publicación de los cambios en los derechos de paquete de usuario.</p></li>
</ul></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Consecuencia</th>
<th align="left">Consecuencia</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p>Como las integraciones de usuarios se conservan por completo, no habrá ningún trabajo, por ejemplo, integración de la publicación/actualización para completarse. Todas las aplicaciones virtuales estarán disponibles en un plazo de segundos a partir de un inicio de sesión.</p></li>
<li><p>La publicación/actualización procesará los cambios que se realicen a los usuarios titulados aplicaciones virtuales que afecten a la experiencia.</p></li>
</ul></td>
<td align="left"><p>Como la adición/actualización debe volver a configurar todas las aplicaciones virtuales en la VM, se extenderá el tiempo de actualización de publicación en cada inicio de sesión.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a>Impacto en el ciclo de vida del paquete

La actualización de un paquete es un aspecto crucial del ciclo de vida del paquete. Para ayudar a garantizar que los usuarios tengan acceso a los paquetes de aplicaciones virtuales actualizadas (publicadas) o degradadas (no publicadas) apropiados, se recomienda que actualice la imagen base para reflejar estos cambios. Para comprender por qué revisar la siguiente sección:

App-V 5,0 SP2 introdujo el concepto de Estados pendientes. En el pasado,

-   Si un administrador cambió los derechos o creó una nueva versión de un paquete (actualizado) y durante una publicación o actualización, el paquete se encontraba en uso, la operación de no publicar o publicar, respectivamente, fallaría.

-   Ahora, si un paquete está en uso, la operación quedará pendiente. Las operaciones de no publicación y de pendiente de publicación se procesarán al reiniciar el servicio o si se emite otro comando de publicación o no publicación. En el último caso, si la aplicación virtual se está usando de otra forma, la aplicación virtual permanecerá en estado pendiente. Para paquetes publicados globalmente, a menudo es necesario reiniciar (o reiniciar el servicio).

En un entorno no persistente, es improbable que se procesen estas operaciones pendientes. Las operaciones pendientes, por ejemplo las tareas se capturan en **HKEY \ _CURRENT \ _USER**  \\  **software**  \\  **Microsoft**  \\  **AppV**  \\  **Client**  \\  **PendingTasks**. Aunque esta ubicación es persistida por la solución UPM, si no se aplica al entorno antes del inicio de sesión, no se procesará.

### <a href="" id="bkmk-evdi"></a>Mejorar la experiencia de VDI mediante el ajuste de optimización del rendimiento

La siguiente sección contiene listas con información sobre las descargas y la documentación de Microsoft que pueden ser útiles al optimizar su entorno para mejorar el rendimiento.

**Blog y scripts de .NET NGEN (muy recomendable)**

Acerca de la tecnología NGEN

-   [Cómo acelerar la optimización de NGEN](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [Script](https://aka.ms/DrainNGenQueue)

**Roles de servidor y servidor de Windows**

Directrices de ajuste del rendimiento del servidor para

-   [Microsoft Windows Server 2012 R2](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [Microsoft Windows Server 2012](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [Microsoft Windows Server 2008 R2](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**Roles de servidor**

-   [Host de virtualización de escritorio remoto](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [Host de sesión de escritorio remoto](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [Relevancia de IIS: administración de App-V, publicación, servicios Web de informes](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [Relevancia de servidor de archivos (SMB): si se usa para el almacenamiento de contenido de App-V y la entrega en el modo SCS](https://technet.microsoft.com/library/jj134210.aspx)

**Guía de rendimiento del cliente de Windows (sistema operativo invitado)**

-   [Microsoft Windows 7](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [Script de optimización: (proporcionado por el soporte técnico de Microsoft)](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [Microsoft Windows 8](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [Script de optimización: (proporcionado por el soporte técnico de Microsoft)](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## Pasos de secuenciación para optimizar los paquetes de rendimiento de publicación


App-V 5,0 y App-V 5,0 SP2 proporcionan un valor significativo en sus versiones respectivas. Varias características facilitan nuevos escenarios o han habilitado nuevos escenarios de implementación de clientes. Las siguientes características pueden influir en el rendimiento de las operaciones de publicación e inicio.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paso</th>
<th align="left">Consideración</th>
<th align="left">Ventajas</th>
<th align="left">Compensaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>No hay ningún bloque de características 1 (FB1, también conocido como principal FB).</p></td>
<td align="left"><p>Sin FB1 significa que la aplicación se iniciará inmediatamente y la falla de transmisión (la aplicación requiere archivo, DLL y debe desplazarse por la red) durante el inicio. Si hay limitaciones de red, FB1:</p>
<ul>
<li><p>Reduzca el número de errores de secuencia y el ancho de banda de red que se usa cuando se inicia una aplicación por primera vez.</p></li>
<li><p>Retrasar el inicio hasta que se haya transmitido todo el FB1.</p></li>
</ul></td>
<td align="left"><p>La falla de la transmisión disminuye el tiempo de lanzamiento.</p></td>
<td align="left"><p>Es necesario reordenar los paquetes de aplicaciones virtuales con FB1 configurado.</p></td>
</tr>
</tbody>
</table>



### Quitar FB1

Quitar FB1 no requiere el instalador de la aplicación original. Una vez completados los pasos siguientes, se recomienda revertir el equipo que ejecuta el secuenciador a una instantánea limpia.

**Interfaz de usuario del secuenciador** : cree un nuevo paquete de aplicación virtual.

1.  Complete los pasos de secuenciación para personalizar el &gt; flujo.

2.  En la fase de transmisión por secuencias, no seleccione **optimizar el paquete para su implementación en una red lenta o no confiable**.

3.  Si lo deseas, pasa a **so de destino**.

**Modificar un paquete de aplicación virtual existente**

1.  Complete los pasos de secuenciación hasta transmitir.

2.  No seleccione **optimizar el paquete para su implementación a través de una red lenta o no confiable**.

3.  Mover a **crear paquete**.

**PowerShell** : actualizar un paquete de aplicaciones virtual existente.

1.  Abra una sesión de PowerShell con privilegios elevados.

2.  Importación-módulo **appvsequencer**.

3.  **Update-AppvSequencerPackage**  -  **AppvPackageFilePath**

    "C:\\Packages\\MyPackage.appv"-instalador

    "C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath

    "C:\\UpgradedPackages"

    **Nota**  
    Este cmdlet requiere un archivo ejecutable (. exe) o un archivo por lotes (. bat). Debe proporcionar un archivo ejecutable vacío (no hace nada) ni un archivo por lotes.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paso</th>
<th align="left">Razones</th>
<th align="left">Ventajas</th>
<th align="left">Compensaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>No hay ninguna instalación SXS en la publicación (ensamblados SxS anteriores a la instalación)</p></td>
<td align="left"><p>No es necesario reordenar los paquetes de aplicaciones virtuales. Los ensamblados SxS pueden permanecer en el paquete de la aplicación virtual.</p></td>
<td align="left"><p>Las dependencias de ensamblado SxS no se instalarán en el momento de la publicación.</p></td>
<td align="left"><p>Las dependencias de ensamblado SxS deben estar preinstaladas.</p></td>
</tr>
</tbody>
</table>



### Crear un nuevo paquete de aplicación virtual en el secuenciador

Si durante la supervisión del secuenciador se instala un ensamblado SxS (como un Runtime VC + +) como parte de la instalación de una aplicación, el ensamblado SxS se detectará automáticamente e incluirá en el paquete. El administrador recibirá una notificación y tendrá la opción de excluir el ensamblado SxS.

**Lado del cliente**:

Al publicar un paquete de aplicaciones virtual, el cliente de App-V 5,0 SP2 detectará si una dependencia SxS requerida ya está instalada. Si la dependencia no está disponible en el equipo y se incluye en el paquete, un Windows Installer tradicional (.** MSI**) la instalación del ensamblado SxS se iniciará. Como se ha documentado anteriormente, simplemente instale la dependencia en el equipo que ejecuta el cliente para asegurarse de que la instalación de Windows Installer (. msi) no se produzca.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paso</th>
<th align="left">Razones</th>
<th align="left">Ventajas</th>
<th align="left">Compensaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Usar selectivamente los archivos de configuración dinámica</p></td>
<td align="left"><p>El cliente de App-V 5,0 debe analizar y procesar estos archivos de configuración dinámica.</p>
<p>Sea consciente del tamaño y la complejidad (ejecución de script, VREG inclusiones y exclusiones) del archivo.</p>
<p>Es posible que varios paquetes de aplicaciones virtuales ya tengan archivos de configuración dinámica específicos del usuario o del equipo.</p></td>
<td align="left"><p>Los tiempos de publicación mejorarán si estos archivos se usan de forma selectiva o no.</p></td>
<td align="left"><p>Es necesario volver a configurar los paquetes de aplicaciones virtuales individualmente o a través de la consola de administración de servidores de App-V para quitar los archivos de configuración dinámica asociados.</p></td>
</tr>
</tbody>
</table>



### Deshabilitar una configuración dinámica con PowerShell

-   Para los paquetes ya publicados, puede usar `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` sin

    Parámetro **-DynamicDeploymentConfiguration**

-   Del mismo modo, al agregar paquetes nuevos con `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` , no use el

    Parámetro **-DynamicDeploymentConfiguration** .

Para obtener documentación sobre cómo aplicar una configuración dinámica, consulte:

-   [Cómo aplicar el archivo de configuración de usuario mediante el uso de PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell.md)

-   [Cómo aplicar el archivo de configuración de implementación mediante el uso de PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paso</th>
<th align="left">Razones</th>
<th align="left">Ventajas</th>
<th align="left">Compensaciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Cuenta para la ejecución de scripts sincrónicos durante el ciclo de vida del paquete.</p></td>
<td align="left"><p>Si el material promocional de script está incrustado en el paquete, agregar (PowerShell) puede ser considerablemente más lento.</p>
<p>La ejecución de scripts durante el inicio de aplicaciones virtuales (StartVirtualEnvironment, StartProcess) o agregar + publicar afectará al rendimiento percibido durante una o más de estas operaciones de ciclo de vida.</p></td>
<td align="left"><p>El uso de scripts asincrónicos (sin bloqueo) asegurará que las operaciones de ciclo de vida se completen de forma eficaz.</p></td>
<td align="left"><p>Este paso requiere conocimientos prácticos de todos los paquetes de aplicaciones virtuales con el material de script incrustado, que tienen archivos de configuración dinámica asociados y que hacen referencia a los scripts y ejecutan sincrónicamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Quitar fuentes virtuales extrañas del paquete.</p></td>
<td align="left"><p>La mayoría de las aplicaciones investigadas por el equipo de producto de App-V contenían un pequeño número de fuentes, generalmente menos de 20.</p></td>
<td align="left"><p>Las fuentes virtuales afectan al rendimiento de la actualización de publicaciones.</p></td>
<td align="left"><p>Las fuentes deseadas deberán habilitarse o instalarse de forma nativa. Para obtener instrucciones, consulte instalar o desinstalar fuentes.</p></td>
</tr>
</tbody>
</table>



### Determinar qué fuentes virtuales existen en el paquete

-   Haga una copia del paquete.

-   Cambiar el nombre del paquete \ _copy. appv a Package\_copy.zip

-   Abra AppxManifest.xml y busque lo siguiente:

    &lt;appv: extensión Category = "AppV. fonts"&gt;

    &lt;appv: fuentes&gt;

    &lt;appv: Font path = "\ [{Fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /Appv: Font&gt;

    **Nota**  
    Si hay fuentes marcadas como **DelayLoad**, estas no tendrán impacto en el primer inicio.



~~~
&lt;/appv:Fonts&gt;
~~~

### Excluir fuentes virtuales del paquete

Use el archivo de configuración dinámica que se adapte mejor al ámbito de usuario: configuración de implementación para todos los usuarios en el equipo, configuración de usuario para usuarios o usuarios específicos.

-   Deshabilite las fuentes con la implementación o la configuración de usuario.

Fuentes

--&gt;

&lt;Fonts Enabled = "false"/&gt;

&lt;!--

## <a href="" id="bkmk-terms1"></a> Terminología de la guía de rendimiento de App-V 5,0


Los siguientes términos se usan al describir conceptos y acciones relacionados con la optimización del rendimiento de App-V 5,0.

-   **Complejidad** : se refiere a una o varias características del paquete que pueden influir en el rendimiento durante la preconfiguración (**Add-AppvClientPackage**) o la integración (**Publish-AppvClientPackage**). Algunas características de ejemplo son: tamaño del manifiesto, número de fuentes virtuales, número de archivos.

-   **Desintegración** : elimina las integraciones de usuario.

-   **Volver a integrar** : aplica las integraciones de usuario.

-   **No persistente, agrupado** : crea un equipo que ejecuta un entorno virtual cada vez que inicia sesión.

-   **Persistentes, personales** : un equipo que ejecuta un entorno virtual que sigue siendo el mismo para cada inicio de sesión.

-   **Estado** : para este documento, implica que las integraciones de usuarios persisten entre sesiones y una tecnología de administración de entorno de usuario se usa conjuntamente con RDSH no persistente o VDI.

-   **Sin estado** : representa un escenario en el que no se conserva el estado del usuario entre sesiones.

-   **Trigger** : (o desencadenadores de acción nativa). UPM usa estos tipos de desencadenadores para iniciar operaciones de supervisión o sincronización.

-   **Experiencia de usuario** : en el contexto de App-V 5,0, la experiencia del usuario, cuantitativa, es la suma de las siguientes partes:

    -   Desde el punto en que los usuarios inician un inicio de sesión cuando pueden manipular el escritorio.

    -   Desde el punto en el que se puede interaccionar el escritorio hasta el punto en el que comienza una actualización de publicación (en las condiciones de PowerShell, sincronizar) al usar la infraestructura de servidor completo de App-V 5,0. En las instancias independientes, es cuando se inician los comandos **Add-AppVClientPackage** y **Publish-AppVClientPackage PowerShell** .

    -   Desde el principio hasta la finalización de la actualización de la publicación. En las instancias independientes, esta es la primera vez que se publica la aplicación virtual.

    -   Desde el punto en que la aplicación virtual está disponible para iniciar desde un acceso directo. Como alternativa, se trata del punto en el que se registra la Asociación de tipo de archivo y se iniciará una aplicación virtual especificada.

-   **Administración de perfiles de usuario** : el enfoque controlado y estructurado para administrar los componentes de usuario asociados con el entorno. Por ejemplo, perfiles de usuario, preferencias y administración de directivas, control de aplicaciones e implementación de aplicaciones. Puede usar las secuencias de comandos o las soluciones de terceros para configurar el entorno según sea necesario.






## Temas relacionados


[Guía del administrador de Microsoft Application Virtualization 5,0](microsoft-application-virtualization-50-administrators-guide.md)









