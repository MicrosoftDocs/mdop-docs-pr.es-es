---
title: Preparación del entorno de UE-V
description: Preparación del entorno de UE-V
author: dansimp
ms.assetid: c93d3b33-e032-451a-9e1b-8534e1625396
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8f806f3c326bad5204a7f1ee69e11b61177e3cce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824650"
---
# Preparación del entorno de UE-V


Virtualización de la experiencia del usuario de Microsoft (UE-V) roaming la configuración entre equipos mediante la ubicación de almacenamiento de configuración. La ubicación de almacenamiento de configuración es un recurso compartido de archivos y debe configurarse durante la implementación del agente de UE-V. Debe definirse como una ubicación de almacenamiento de configuración o como un directorio de inicio de Active Directory. Además, el administrador debe configurar un servidor de tiempo para que admita la sincronización coherente. Para preparar su entorno para UE-V, debe tener en cuenta lo siguiente:

-   [Almacenamiento de configuración de UE-V](#bkmk-uevsettingsstorage):

    -   [Definir una ubicación de almacenamiento de configuración](#bkmk-definingsettingsstoragelocation)

    -   [Usar el directorio principal de Active Directory con UE-V](#bkmk-usingactivedirectoryhomedirectory)

-   [Sincronizar relojes de equipo para la sincronización de configuración de UE-V](#bkmk-synchronizecomputerclocks)

-   [Planificación de rendimiento y capacidad](#bkmk-performancecapacityplanning)

Para obtener más información sobre los requisitos del sistema operativo y del equipo, consulte [configuraciones admitidas para UE-V 1,0](supported-configurations-for-ue-v-10.md).

## <a href="" id="bkmk-uevsettingsstorage"></a>Almacenamiento de configuración de UE-V


Puede definir el almacenamiento de configuración de la experiencia de usuario de virtualización en una de dos configuraciones: una ubicación de almacenamiento de configuración o un directorio de inicio de Active Directory.

### <a href="" id="bkmk-definingsettingsstoragelocation"></a>Definir una ubicación de almacenamiento de configuración

La ubicación de almacenamiento de configuración de UE-V es un recurso compartido de red estándar al que pueden acceder los usuarios de UE-V. Antes de definir la ubicación de almacenamiento de configuración, debe crear un directorio raíz. Los usuarios que van a almacenar la configuración en el recurso compartido deben tener permisos de lectura y escritura en la ubicación de almacenamiento. UE-V Agent creará carpetas específicas del usuario en este directorio raíz. La ubicación de almacenamiento de configuración se define mediante la opción de configuración **SettingsStoragePath** . Esta opción se puede configurar de las siguientes maneras:

-   Durante la instalación de UE-V Agent a través de un parámetro de la línea de comandos o en un script de proceso por lotes.

-   Usar una directiva de grupo.

-   Después de la instalación, mediante PowerShell o WMI.

La ruta de acceso debe estar en una ruta de acceso UNC (Convención de nomenclatura universal) del servidor y el recurso compartido. Por ejemplo, **\\\\server\\settingsshare\\**. Esta opción de configuración admite el uso de variables para habilitar escenarios de itinerancia específicos.

Puede usar la `%username%` variable con la ruta de acceso UNC del servidor y el recurso compartido. Esto proporcionará la misma experiencia de configuración en todos los equipos o sesiones en los que un usuario inicie sesión. Considere esta configuración para los siguientes escenarios:

1.  Los usuarios de la empresa tienen varios equipos físicos, configurados de forma similar, y la configuración de cada usuario debe ser la misma en todos los equipos.

2.  Los usuarios de la empresa usan grupos de infraestructura de escritorio virtual (VDI) en los que la configuración debe conservarse en todas las sesiones de VDI de cada usuario.

3.  Los usuarios de la empresa tienen un equipo físico y, además, usan una VDI. La experiencia de configuración de cada usuario debe ser la misma independientemente de si usa el equipo físico o la sesión de VDI.

4.  Varios usuarios usan varios equipos de la empresa. La experiencia de configuración de cada usuario debe ser la misma en todos los equipos.

Puede usar las variables **%username%\\%COMPUTERNAME%** con la ruta de acceso UNC del servidor y el recurso compartido. Esto conservará la experiencia de configuración de cada equipo. Considere esta configuración para los siguientes escenarios:

1.  Los usuarios de la empresa tienen varios equipos físicos y usted desea preservar la experiencia de configuración de cada uno de ellos.

2.  Varios usuarios usan los equipos de la empresa. La experiencia de configuración se debe conservar para cada equipo en el que el usuario inicie sesión.

El agente UE-V crea dinámicamente la ruta de acceso de almacenamiento de configuración específica del usuario según una configuración de UE-V `SettingsStoragePath` y las variables definidas.

El agente UE-V crea dinámicamente una carpeta de sistema oculta con nombre `SettingsPackages` dentro de cada ubicación de almacenamiento específica del usuario. UE-V Agent Lee y escribe la configuración en esta ubicación según se haya definido en las plantillas de ubicación de configuración de UE-V registradas.

Si la ubicación de almacenamiento de configuración es la misma para un conjunto de equipos administrados de un usuario, la configuración de UE-V aplicable se determina mediante una regla "última escritura gana". El agente que se ejecuta en un equipo Lee y escribe en la ubicación de configuración independientemente de los agentes que se ejecutan en otros equipos. Los últimos valores de configuración escritos son los valores que se aplican cuando el siguiente agente Lee de la ubicación de almacenamiento de configuración. Para obtener más información, consulte [implementar la ubicación de almacenamiento de configuración de UE-V 1,0](deploying-the-settings-storage-location-for-ue-v-10.md).

### <a href="" id="bkmk-usingactivedirectoryhomedirectory"></a>Usar el directorio principal de Active Directory con UE-V

Si no se configura ninguna ubicación de almacenamiento de configuración para UE-V cuando se implementa el agente, el directorio principal de Active Directory (AD) del usuario se usa para almacenar paquetes de ubicación de configuración. UE-V Agent crea dinámicamente la carpeta de almacenamiento de configuración debajo de la raíz del directorio particular de AD de cada usuario. El agente solo usa el directorio principal de Active Directory si no se define una ubicación de almacenamiento de configuración (SettingsStoragePath).

## <a href="" id="bkmk-synchronizecomputerclocks"></a>Sincronizar relojes de equipo para la sincronización de configuración de UE-V


Los equipos que ejecutan el agente de UE-V para sincronizar la configuración deben usar un servidor de hora. Las marcas de tiempo se usan para determinar si es necesario sincronizar la configuración desde la ubicación de almacenamiento de configuración. Si el reloj del equipo no es exacto, es posible que la configuración anterior sobrescriba la configuración más reciente o que la nueva configuración no se guarde en la ubicación de almacenamiento de configuración. El uso de un servidor de hora permite a UE-V mantener una experiencia de configuración coherente.

## <a href="" id="bkmk-performancecapacityplanning"></a>Planificación de rendimiento y capacidad


Los requisitos de capacidad para UE-V pueden determinarse mediante el uso de la capacidad de disco estándar y la supervisión de estado de la red. UE-V usa un recurso compartido de bloque de mensajes de servidor (SMB) para el almacenamiento de paquetes de configuración. El tamaño de los paquetes de configuración varía según la información de configuración de una aplicación específica. Aunque la mayoría de los paquetes de configuración son pequeños, la sincronización de archivos potencialmente grandes, como las imágenes de escritorio, puede dar lugar a un bajo nivel de rendimiento, especialmente en redes más lentas. Para minimizar los problemas con la latencia de red, debe crear ubicaciones de almacenamiento de configuración en las mismas redes locales donde residen los equipos de los usuarios.

De forma predeterminada, la sincronización de UE-V agotará el tiempo de espera después de 2 segundos si la red es lenta o el paquete de configuración es grande. Puede configurar el tiempo de espera con la Directiva de grupo. Para obtener más información sobre cómo establecer el tiempo de espera, consulte [configurar UE-V con objetos de directiva de grupo](configuring-ue-v-with-group-policy-objects.md).

## Temas relacionados


[Virtualización de la experiencia del usuario de Microsoft (UE-V) 1.0](index.md)

[Planificación de UE-V 1.0](planning-for-ue-v-10.md)

[Configuraciones admitidas para UE-V 1.0](supported-configurations-for-ue-v-10.md)

 

 





