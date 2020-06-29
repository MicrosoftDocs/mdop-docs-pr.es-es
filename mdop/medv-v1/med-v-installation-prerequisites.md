---
title: Requisitos previos de instalación de MED-V
description: Requisitos previos de instalación de MED-V
author: dansimp
ms.assetid: cf3c0906-23eb-4c4a-8951-a65741720f95
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2b432b8c2b06e171eb339aab6c7b15efb20d5919
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824970"
---
# Requisitos previos de instalación de MED-V


A continuación se enumeran los requisitos previos para instalar MED-V:

[Requisitos de Active Directory](#bkmk-activedirectoryrequirements)

[Base de datos de informes](#bkmk-howtoinstallthereportdatabase)

[Configuración de software antivirus y de copia de seguridad](#bkmk-antivirusbackupsoftwareconfiguration)

[Microsoft Virtual PC 2007 SP1](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1)

## <a href="" id="bkmk-activedirectoryrequirements"></a>Requisitos de Active Directory


Al configurar el servidor de MED-V, si los usuarios no forman parte del mismo dominio al que pertenece el servidor, debe establecerse una confianza entre los dominios.

## <a href="" id="bkmk-howtoinstallthereportdatabase"></a>Cómo instalar la base de datos de informes


La base de datos de informes es necesaria para almacenar todos los registros del área de trabajo de MED-V. La base de datos de registro se usa para generar informes de MED-V. Para obtener información sobre los informes, vea [informes de MED-V](med-v-reporting.md).

SQL Server se puede instalar en el mismo servidor que el servidor de MED-V o en un servidor remoto. Si va a instalar en un servidor remoto, consulte [instalar SQL Server en un servidor remoto](#bkmk-installingsqlserveronaremoteserver).

### <a href="" id="bkmk-installingsqlserveronaremoteserver"></a>Instalar SQL Server en un servidor remoto

**Para instalar SQL Server en un servidor remoto**

1.  Configure lo siguiente en el servidor remoto:

    -   Nombre de instancia: instancia predeterminada

    -   Modo de autenticación: modo mixto

    -   Usuario: el usuario predeterminado creado es "SA"

    -   Contraseña: contraseña deseada

    -   Configuración de intercalación: predeterminada

    -   Error en la configuración del informe de uso: predeterminado

2.  Instale los siguientes archivos en el servidor MED-V:

    -   Para instalar los requisitos previos para la colección de objetos del módulo de administración para Microsoft SQL Server2008, descargue el [cliente nativo de Microsoft SQL Server2008](https://go.microsoft.com/fwlink/?LinkId=164039) desde el centro de descarga de Microsoft.

    -   Para instalar los requisitos previos para la colección de objetos del módulo de administración para Microsoft SQL Server2005, descargue el [cliente nativo de Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=164038) desde el centro de descarga de Microsoft.

    -   Para instalar los archivos dll necesarios para Microsoft SQL Server2008, descargue la [recopilación de objetos de administración de Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=164041) desde el centro de descarga de Microsoft.

    -   Para instalar los archivos dll necesarios para Microsoft SQL Server2005, descargue los [objetos de administración de Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=164040) desde el centro de descarga de Microsoft.

    -   Para instalar los paquetes de instalación independientes que proporcionan valor adicional para SQL Server2008, descargue el [paquete de características de Microsoft SQL Server2008](https://go.microsoft.com/fwlink/?LinkId=163960) desde el centro de descarga de Microsoft.

    -   Para instalar los paquetes de instalación independientes que proporcionan valor adicional para SQL Server2005, descargue el [Feature Pack para Microsoft SQL Server2005]( https://go.microsoft.com/fwlink/?LinkId=163961) desde el centro de descarga de Microsoft.

    Para obtener más información sobre estos archivos, consulte [Microsoft SQL Server2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=163960) en el centro de descarga de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163960) o [Feature Pack para Microsoft SQL Server2005](https://go.microsoft.com/fwlink/?LinkId=163961) en el centro de descarga de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=163961) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>Configuración de software antivirus y de copia de seguridad


Para evitar que la actividad antivirus afecte al rendimiento del escritorio virtual, se recomienda siempre que sea posible excluir los siguientes tipos de archivo de máquina virtual de cualquier procesamiento de copia de seguridad o antivirus que se ejecute en el host:

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. CKM

-   \*. EVHD

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc2007sp1"></a>Cómo instalar y configurar Microsoft Virtual PC2007 SP1


**Importante**  Si Virtual PC para Windows existe en el equipo host, desinstálelo antes de instalar virtual PC2007 SP1.

 

**Para instalar Microsoft Virtual PC2007 SP1**

1.  Descargue Virtual PC2007 SP1 desde el centro de descarga de Microsoft [Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=142994).

2.  Ejecute el archivo de instalación en el equipo host y siga el asistente.

3.  Instale la actualización de virtual PC2007 SP1 en el equipo host en modo elevado.

    Para obtener más información, consulte [la descripción del paquete de revisiones para Virtual PC 2007 SP1](https://go.microsoft.com/fwlink/?LinkId=150575).

    **Nota:**  La actualización de virtual PC2007 SP1 es necesaria para ejecutar virtual PC2007 SP1.

     

## Temas relacionados


[Configuraciones admitidas](supported-configurationsmedv-orientation.md)

 

 





