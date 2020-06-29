---
title: Cómo implementar el cliente de App-V
description: Cómo implementar el cliente de App-V
ms.author: dansimp
author: dansimp
ms.assetid: 9c4e67ae-ddaf-4e23-8c16-72d029a74a27
ms.reviewer: ''
manager: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/05/2018
ms.openlocfilehash: 4e246e13bf59f167eade77200afd866c6a3c41fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814119"
---
# Cómo implementar el cliente de App-V


Use el siguiente procedimiento para instalar el cliente de Microsoft Application Virtualization (App-V) 5,0 y el cliente de servicios de escritorio remoto. Debe instalar la versión del cliente que se corresponda con el sistema operativo del equipo de destino.

<a href="" id="bkmk-clt-install-prereqs"></a>**Qué hacer antes de empezar**

1. Revise e instale los requisitos previos de software:

   Instale el software necesario que corresponde a la versión de la aplicación de App-V que está instalando:

   - [Acerca de App-V 5.0 SP3](about-app-v-50-sp3.md)

   - App-V 5,0 SP1 y App-V 5,0 SP2: no hay nuevos requisitos previos en estas versiones

   - [Requisitos previos de App-V 5.0](app-v-50-prerequisites.md)

2. Revise la coexistencia del cliente y los escenarios no admitidos, como se aplica a la instalación:


   |                                               |                                                                                                                            |
   |-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
   |      Implementación de clientes de App-V coexistentes       | [Planificación de la implementación del cliente y del secuenciador de App-V 5.0](planning-for-the-app-v-50-sequencer-and-client-deployment.md) |
   | Escenarios de instalación no compatibles o limitadas |                         [Consideraciones compatibles con App-V 5.0](app-v-50-supported-configurations.md)                         |

   ---

3. Revise las ubicaciones de información del registro del cliente, registro y solución de problemas:

#### Información del registro del cliente
<ul><li>De forma predeterminada, después de instalar el cliente de App-V 5,0, la información del cliente se almacena en el registro, en la siguiente clave del registro:<p><p><code>HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\APPV\CLIENT</code></li><li>Al implementar un paquete virtualizado en un equipo que ejecuta el cliente de App-V, los datos del paquete asociado se almacenan en la siguiente ubicación:<p><p><code>C:\ProgramData\App-V</code><p><p>Sin embargo, puede volver a configurar esta ubicación con la siguiente clave del registro:<p><p><code>HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\SOFTWARE\MICROSOFT\APPV\CLIENT\STREAMING\PACKAGEINSTALLATIONROOT</code></li></ul>

#### Archivos de registro de cliente                  
<ul><li>Para obtener información sobre el archivo de registro asociada con el cliente de App-V 5,0, busque en el siguiente registro:<p><p><code>Event logs/Applications and Services Logs/Microsoft/AppV</code></li><li>En App-V 5,0 SP3, se han consolidado algunos registros y se han movido a la siguiente ubicación:<p><p><code>Event logs/Applications and Services Logs/Microsoft/AppV/ServiceLog</code><p><p>Para obtener una lista de los registros que se han movido, consulte [acerca de App-V 5,0 SP3](about-app-v-50-sp3.md#bkmk-event-logs-moved).</li><li>Los paquetes que se encuentran almacenados en los equipos que ejecutan el cliente de App-V 5,0 se guardan en la siguiente ubicación:<p><p><code>C:\ProgramData\App-V\<<em>package id</em>>\<<em>version id</em>></code></li></ul>

#### Información para la solución de problemas de instalación del cliente
- Consulte el registro de errores en la carpeta **% temp%** . 
- Para revisar los archivos de registro, haga clic en **Inicio**, escriba **% temp%** y, a continuación, busque el **registro de appv_**. 

## Para instalar el cliente de App-V 5,0

1. Copie el archivo de instalación del cliente App-V 5,0 en el equipo en el que se instalará.<p><p>Elija entre los siguientes tipos de cliente:


   |                  Tipo de cliente                  |          Archivo para usar          |
   |-----------------------------------------------|-------------------------------|
   |        Versión estándar del cliente         |   **appv_client_setup.exe**   |
   | Versión de servicios de escritorio remoto del cliente | **appv_client_setup_rds.exe** |

   ---

2. Haga doble clic en el archivo de instalación y haga clic en **instalar**. Antes de comenzar la instalación, el instalador comprueba si el equipo tiene [requisitos previos de App-V 5,0](app-v-50-prerequisites.md).

3. Revise y acepte los términos de licencia del software, elija si desea usar Microsoft Update y si desea participar en el programa para la mejora de la experiencia del usuario de Microsoft, y haga clic en **instalar**.

4. En la página la **configuración se completó correctamente** , haga clic en **cerrar**.

   La instalación crea las siguientes entradas para el cliente App-V en los **programas**:

   -   **.exe**

   -   **.msi**

   -   **paquete de idioma**

   >[!NOTE]
   >Después de la instalación, solo se puede desinstalar el archivo. exe.


## Para instalar el cliente de App-V 5,0 con un script

1. Instale todo el software necesario necesario en los equipos de destino. Consulte [Qué hacer antes de empezar](#bkmk-clt-install-prereqs). Si instala el cliente con un archivo. msi, se producirá un error en la instalación si falta alguno de los requisitos previos.

2. Para usar un script para instalar el cliente de App-V 5,0, use los siguientes parámetros con **appv\_client\_setup.exe**.

   >[!NOTE]
   >El instalador de Windows (. msi) cliente admite el mismo conjunto de conmutadores, excepto el parámetro **/log** .

   |                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                     |
   |----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |           /INSTALLDIR            |                                                                                                                                                               Especifica el directorio de instalación. Ejemplo de uso:<p><p>**/INSTALLDIR = C:\Archivos de Files\AppV Client**                                                                                                                                                                |
   |            /CEIPOPTIN            |                                                                                                                                                          Permite la participación en el programa para la mejora de la experiencia del usuario. Ejemplo de uso:<p><p>**/CEIPOPTIN = [0 \ | 1 \]**                                                                                                                                                           |
   |             /MUOPTIN             |                                                                                                                                                                                 Habilita Microsoft Update. Ejemplo de uso:<p><p>**/MUOPTIN = [0 \ | 1 \]**                                                                                                                                                                                  |
   |     /PACKAGEINSTALLATIONROOT     |                                                                                                                                         Especifica el directorio en el que se instalarán todas las nuevas aplicaciones y actualizaciones. Ejemplo de uso: <p><p>**/PACKAGEINSTALLATIONROOT = ' paquetes C:\App-V**                                                                                                                                         |
   |        /PACKAGESOURCEROOT        |                                                                                                                                                  Invalida la ubicación de origen para descargar el contenido del paquete. Ejemplo de uso:<p><p>**/PACKAGESOURCEROOT = ' <http://packageStore> '**                                                                                                                                                  |
   |            /AUTOLOAD             |                                                                                           Especifica cómo se cargarán los nuevos paquetes por App-V 5,0 en un equipo específico. Las siguientes opciones están habilitadas: [1]; cargar automáticamente todos los paquetes [2]; o no carga automáticamente paquetes [0]. Ejemplo de uso:<p><p>**/AUTOLOAD = [0 \ | 1 \ | 2 \]**                                                                                           |
   |     /SHAREDCONTENTSTOREMODE      |                                                                                                                                           Especifica que el contenido del paquete transmitido no se guardará en el disco duro local. Ejemplo de uso: <p><p>**/SHAREDCONTENTSTOREMODE = [0 \ | 1 \]**                                                                                                                                            |
   |          /MIGRATIONMODE          |                                                                                                                     Permite que el cliente de App-V 5,0 modifique los accesos directos y los FTAs asociados a los paquetes creados con una versión anterior. Ejemplo de uso:<p><p>**/MIGRATIONMODE = [0 \ | 1 \]**                                                                                                                     |
   |      /ENABLEPACKAGESCRIPTS       |                                                                                                                                   Habilita los scripts que se definen en el archivo de manifiesto del paquete o los archivos de configuración que se deben ejecutar. Ejemplo de uso:<p><p>**/ENABLEPACKAGESCRIPTS = [0 \ | 1 \]**                                                                                                                                   |
   |    /ROAMINGREGISTRYEXCLUSIONS    |                                                                                                                                      Especifica las rutas de registro que no se transferirán a un perfil de usuario. Ejemplo de uso:<p><p>**/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients**                                                                                                                                      |
   |      /ROAMINGFILEEXCLUSIONS      |                                                                                                                                  Especifica las rutas de archivo relativas a% userprofile% que no se mueven con el perfil de un usuario. Ejemplo de uso: <p><p>**/ROAMINGFILEEXCLUSIONS ' escritorio; mis imágenes '**                                                                                                                                   |
   |   /S [1-5] PUBLISHINGSERVERNAME    |                                                                                                                                                           Muestra el nombre del servidor de publicación. Ejemplo de uso:<p><p>**/S2PUBLISHINGSERVERNAME = MyPublishingServer**                                                                                                                                                            |
   |    /S [1-5] PUBLISHINGSERVERURL    |                                                                                                                                                                Muestra la dirección URL del servidor de publicación. Ejemplo de uso:<p><p>**/S2PUBLISHINGSERVERURL = \\pubserver**                                                                                                                                                                |
   |   /S [1-5] GLOBALREFRESHENABLED    |                                                                                                                                                                    Habilita una actualización de publicación global. Ejemplo de uso:<p><p>**/S2GLOBALREFRESHENABLED = [0 \ | 1 \]**                                                                                                                                                                     |
   |   /S [1-5] GLOBALREFRESHONLOGON    |                                                                                                                                                             Inicia una actualización de publicación global cuando un usuario inicia sesión. Ejemplo de uso:<p><p>**/S2LOGONREFRESH = [0 \ | 1 \]**                                                                                                                                                              |
   |   /S [1-5] GLOBALREFRESHINTERVAL   |                                                                                                                                         Especifica el intervalo de actualización de la publicación, donde **0** indica que no se actualiza periódicamente. Ejemplo de uso: **/S2PERIODICREFRESHINTERVAL = [0-744]**                                                                                                                                         |
   | /S [1-5] GLOBALREFRESHINTERVALUNIT |                                                                                                                                                            Especifica la unidad de intervalo (horas [0], días [1]). Ejemplo de uso:<p><p>**/S2GLOBALREFRESHINTERVALUNIT = [0 \ | 1 \]**                                                                                                                                                            |
   |    /S [1-5] USERREFRESHENABLED     |                                                                                                                                                                          Habilita la actualización de publicaciones de usuario. Ejemplo de uso: **/S2USERREFRESHENABLED = [0 \ | 1 \]**                                                                                                                                                                          |
   |    /S [1-5] USERREFRESHONLOGON     |                                                                                                                                                              Inicia una actualización de publicación de usuario cuando un usuario inicia sesión. Ejemplo de uso:<p><p>**/S2LOGONREFRESH = [0 \ | 1 \]**                                                                                                                                                               |
   |    /S [1-5] USERREFRESHINTERVAL    |                                                                                                                                         Especifica el intervalo de actualización de la publicación, donde **0** indica que no se actualiza periódicamente. Ejemplo de uso: **/S2PERIODICREFRESHINTERVAL = [0-744]**                                                                                                                                         |
   |  /S [1-5] USERREFRESHINTERVALUNIT  |                                                                                                                                                             Especifica la unidad de intervalo (horas [0], días [1]). Ejemplo de uso:<p><p>**/S2USERREFRESHINTERVALUNIT = [0 \ | 1 \]**                                                                                                                                                             |
   |               Log               |                                                                                                                                                Especifica una ubicación donde se guarda la información del registro. La ubicación predeterminada es% Temp%. Ejemplo de uso:<p><p>**/log C:\logs\log.log**                                                                                                                                                |
   |                q                |                                                                                                                                                                                                Especifica una instalación desatendida.                                                                                                                                                                                                |
   |             Pair              |                                                                                                                                                                                               Repara una instalación de cliente anterior.                                                                                                                                                                                               |
   |            /NORESTART            | Impide que el equipo se reinicie después de la instalación del cliente.<p><p>El parámetro impide que el equipo del usuario final se reinicie después de que se instalen las actualizaciones y le permite programar el reinicio cuando lo desee. Por ejemplo, puede instalar App-V 5,0 SPX y, después, instalar el paquete de revisiones Y sin reiniciar el producto después de la instalación del Service Pack. Después de la instalación, debe reiniciar antes de empezar a usar App-V. |
   |            /UNINSTALL            |                                                                                                                                                                                                       Desinstala el cliente.                                                                                                                                                                                                        |
   |           /ACCEPTEULA            |                                                                                                                                              Acepta el contrato de licencia. Esto es necesario para una instalación desatendida. Ejemplo de uso:<p><p>**/ACCEPTEULA** o **/ACCEPTEULA = 1**                                                                                                                                               |
   |             /LAYOUT              |                                                                                                                               Especifica la acción de diseño asociada. También extrae los archivos de Windows Installer (. msi) y de script a una carpeta sin instalar App-V 5,0. No se espera ningún valor.                                                                                                                                |
   |            /LAYOUTDIR            |                                                                                                                                                 Especifica el directorio de diseño. Requiere un valor de cadena. Ejemplo de uso:<p><p>**/LAYOUTDIR = "cliente de virtualización C:\Application"**                                                                                                                                                  |
   |          /?,/h,/Help           |                                                                                                                                                                                      Solicita ayuda acerca de los parámetros de instalación anteriores.                                                                                                                                                                                      |

   ---

## Para instalar el cliente de App-V 5,0 con el archivo de Windows Installer (. msi)

1. Instale los requisitos previos necesarios en los equipos de destino. Consulte [Qué hacer antes de empezar](#bkmk-clt-install-prereqs). Si no se cumplen los requisitos previos, se producirá un error en la instalación.

2. Asegúrese de que los equipos de destino no tengan reinicios pendientes antes de instalar el cliente con los archivos App-V 5,0 Windows Installer (. msi). Los archivos de Windows Installer no marcan un reinicio pendiente.

3. Implemente uno de los siguientes archivos de Windows Installer en el equipo de destino. El archivo que especifique debe coincidir con la configuración del equipo de destino.


   |                       Tipo de implementación                        |      Implementar este archivo       |
   |-----------------------------------------------------------------|-----------------------------|
   | El equipo está ejecutando un sistema operativo Microsoft Windows de 32 bits |   appv_client_MSI_x86.msi   |
   | El equipo está ejecutando un sistema operativo Microsoft Windows de 64 bits |   appv_client_MSI_x64.msi   |
   | Está implementando el cliente de servicios de escritorio remoto de App-V 5,0  | appv_client_rds_MSI_x64.msi |

   ---

4. Con la información de la tabla siguiente, seleccione el paquete de idioma correspondiente **. msi** para instalar según el idioma que desee para el equipo de destino. La **xxxx** de la tabla se refiere a la configuración regional de destino del paquete de idioma.

   **Qué debe saber antes de empezar:** 

   -  Los paquetes de idioma son comunes al cliente de App-V 5,0 estándar y a la versión de servicios de escritorio remoto del cliente de App-V 5,0.

   -  Si instala el cliente de App-V 5,0 con el **archivo. exe**, el instalador solo implementará el paquete de idioma que coincida con el sistema operativo que se ejecuta en el equipo de destino.

   -  Para implementar paquetes de idioma adicionales en un equipo de destino, use el procedimiento **para instalar el cliente de App-V 5,0 con el archivo de Windows Installer (. msi)**.

   |                       Tipo de implementación                        |       Implementar este archivo       |
   |-----------------------------------------------------------------|------------------------------|
   | El equipo está ejecutando un sistema operativo Microsoft Windows de 32 bits | appv_client_LP_xxxx_ x86.msi |
   | El equipo está ejecutando un sistema operativo Microsoft Windows de 64 bits | appv_client_LP_xxxx_ x64.msi |

   ---

   **¿Tiene una sugerencia para App-V**? Agregar o votar sobre [sugerencias](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). <p><p>**¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Implementación de App-V 5.0](deploying-app-v-50.md)

[Información acerca de la configuración de cliente](about-client-configuration-settings.md)

[Cómo desinstalar el cliente de App-V 5.0](how-to-uninstall-the-app-v-50-client.md)
