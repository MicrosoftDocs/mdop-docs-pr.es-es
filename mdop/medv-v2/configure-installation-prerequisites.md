---
title: Configurar los requisitos previos de instalación
description: Configurar los requisitos previos de instalación
author: dansimp
ms.assetid: ff9cf28a-3eac-4b6c-8ce9-bfc202f57947
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6cd9379804c45a2025064a6eecf363c010980369
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819310"
---
# Configurar los requisitos previos de instalación


Las siguientes instrucciones son los requisitos previos para instalar y usar Microsoft Enterprise Desktop Virtualization (MED-V) 2,0:

[Windows Virtual PC](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7)

[Actualización de Windows Virtual PC](#bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update)

[Configuración de software antivirus y de copia de seguridad](#bkmk-antivirusbackupsoftwareconfiguration)

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7"></a>Cómo instalar y configurar Windows Virtual PC


**Importante**  Si ya existe una versión de Virtual PC para Windows en el equipo host, debe desinstalarla antes de instalar Windows Virtual PC.

 

**Para instalar Windows Virtual PC**

1.  Descargue [Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=195918) desde el centro de descarga de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=195918) .

2.  Ejecute el archivo de instalación en el equipo host y siga los pasos del asistente.

**Importante**  Windows Virtual PC incluye el paquete de componentes de integración, que proporciona características que mejoran la interacción entre el entorno virtual y el equipo físico. Por ejemplo, permite que el ratón se mueva entre el host y los equipos invitados. MED-V requiere la instalación del paquete de componentes de integración.

 

## <a href="" id="bkmk-howtoinstallandconfiguremicrosoftvirtualpc7update"></a>Cómo instalar y configurar la actualización de Virtual PC de Windows


La actualización de Microsoft Update asociada con el artículo KB977206 habilita el modo de Windows XP para los equipos sin tecnología de virtualización asistida por hardware (HAV). Le recomendamos que instale esta actualización porque es posible que algunas características de integración no funcionen correctamente si el paquete de componentes de integración en el sistema operativo invitado no coincide con la versión de Windows Virtual PC que está instalada en el equipo host.

**Importante**  No tiene que instalar esta actualización cuando está instalando MED-V en equipos host que ejecutan Windows 7 con Service Pack 1.

 

**Sugerencia**  Además de la actualización que se muestra aquí, le recomendamos que revise todas las actualizaciones disponibles de Virtual PC de Windows y que aplique las actualizaciones apropiadas o necesarias para su entorno.

 

**Para instalar la actualización de Windows Virtual PC**

1.  Descargue la actualización de Windows Virtual PC requerida desde el centro de descarga de Microsoft.

    [actualización de 32](https://go.microsoft.com/fwlink/?LinkId=195919) bits ( https://go.microsoft.com/fwlink/?LinkId=195919) .

    [actualización de 64](https://go.microsoft.com/fwlink/?LinkId=195920) bits ( https://go.microsoft.com/fwlink/?LinkId=195920) .

2.  Ejecute el archivo de instalación en el equipo host en modo elevado y siga los pasos que se indican en el asistente.

    Para obtener más información sobre el paquete de revisiones para Windows Virtual PC, consulte el [artículo 977206](https://go.microsoft.com/fwlink/?LinkId=195921) ( https://go.microsoft.com/fwlink/?LinkId=195921) .

## <a href="" id="bkmk-antivirusbackupsoftwareconfiguration"></a>Cómo configurar el software antivirus y de copia de seguridad


Para evitar que la actividad antivirus afecte el rendimiento del escritorio virtual, le recomendamos, donde puede excluir los siguientes tipos de archivo de máquina virtual de cualquier proceso de copia de seguridad o antivirus que se ejecute en el equipo host:

-   \*. VMC

-   \*. VUD

-   \*. VSV

-   \*. EXPIRA

## Temas relacionados


[Configurar los requisitos previos de entorno](configure-environment-prerequisites.md)

[Arquitectura de alto nivel](high-level-architecturemedv2.md)

[Configuraciones admitidas de MED-V 2.0](med-v-20-supported-configurations.md)

 

 





