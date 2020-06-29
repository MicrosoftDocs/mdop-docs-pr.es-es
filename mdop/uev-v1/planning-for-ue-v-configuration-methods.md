---
title: Planificación de métodos de configuración de UE-V
description: Planificación de métodos de configuración de UE-V
author: dansimp
ms.assetid: 57bce7ab-1be5-434b-9ee5-c96026bbe010
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4894644d72392ae984d0de290bf634e137d5b85e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827091"
---
# Planificación de métodos de configuración de UE-V


Las configuraciones de virtualización de la experiencia del usuario de Microsoft (UE-V) determinan cómo se sincronizan las opciones de configuración en toda la empresa. En este tema se describe cómo se crean las configuraciones de UE-V para ayudarle a formular un plan de configuración que se adapte mejor a sus requisitos empresariales.

## Métodos de configuración para UE-V


Puede configurar UE-V antes, durante o después de la instalación del agente, según el método de configuración que use.

**Directiva de Grupo:** la infraestructura de directiva de grupo existente se puede usar para configurar UE-v antes o después de la implementación del agente de UE-v. La plantilla de la UE-V ADMX habilita la administración centralizada de las opciones de configuración comunes del agente de UE-V e incluye la configuración para configurar la sincronización de UE-V. Los entornos de red que usan la Directiva de grupo pueden preconfigurar UE-V en previsión de la implementación del agente.

[Configurar UE-V con objetos de directiva de grupo](configuring-ue-v-with-group-policy-objects.md)

[Instalación de las plantillas ADMX de directiva de grupo de UE-V](installing-the-ue-v-group-policy-admx-templates.md)

**Instalación de la línea de comandos o del script por lotes:** los parámetros que se usan con la implementación de UE-v Agent permiten configurar muchos parámetros de UE-v. Los sistemas electrónicos de distribución de software, como System Center Configuration Manager, usan estos parámetros para configurar sus clientes al implementar e instalar el software de agente de UE-V. Para obtener una lista de parámetros de instalación y secuencias de comandos de instalación de ejemplo, consulte [Deploying The UE-V Agent](deploying-the-ue-v-agent.md).

**PowerShell y WMI:** los comandos de script que usan POWERSHELL o WMI se pueden usar para modificar las configuraciones después de instalar el agente de UE-V. Para obtener una lista de los comandos de PowerShell y WMI, vea [administrar el agente y los paquetes de 1,0 UE-V con PowerShell y WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).

**Editar la configuración del registro:** La configuración de UE-V se almacena en el registro y puede modificarse con cualquier herramienta que pueda modificar la configuración del registro, como regedit.

**Nota:**  La modificación del registro puede dar lugar a la pérdida de datos o a que el equipo deje de responder. Le recomendamos que use otros métodos de configuración.

 

### Configuración de UE-V

A continuación se muestran algunos ejemplos de parámetros de configuración de UE-V:

-   **Establecer la ruta de almacenamiento:** especifica la ubicación del recurso compartido de archivos que almacena la configuración de UE-V.

-   **Ruta del catálogo de plantillas de configuración:** especifica la ruta de acceso UNC (Convención de nomenclatura universal) que define la ubicación en la que se comprobó la nueva plantilla de ubicación de configuración.

-   **Registrar plantillas de Microsoft:** especifica si se deben registrar las plantillas predeterminadas de Microsoft durante la instalación.

-   **Método de sincronización:** especifica si la característica archivos sin conexión de Windows se usa para la compatibilidad sin conexión.

-   **Tiempo de espera de sincronización:** especifica el número de milisegundos que el equipo espera antes de que se agote el tiempo de espera al recuperar la configuración de usuario de la ubicación de almacenamiento de configuración.

-   **Sincronización habilitada:** especifica si la sincronización de configuración de UE-V está habilitada o deshabilitada.

-   **Tamaño máximo de paquete:** especifica el tamaño de archivo del paquete de configuración en bytes en los que UE-V Agent notifica una advertencia.

## Temas relacionados


[Planificación de UE-V 1.0](planning-for-ue-v-10.md)

[Planificación para la configuración de UE-V](planning-for-ue-v-configuration.md)

 

 





