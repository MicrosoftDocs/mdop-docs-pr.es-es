---
title: Administrar configuraciones para UE-V 2.x
description: Administrar configuraciones para UE-V 2.x
author: dansimp
ms.assetid: e2332eca-a9cd-4446-8f7c-d17058b03466
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20d5d2942dbd805a4054a9431b237c821cbb70fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827381"
---
# Administrar configuraciones para UE-V 2.x


En el curso de la virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 o 2,1 SP1, debe administrar la configuración de UE-V Agent y administrar también las ubicaciones de almacenamiento de recursos, como archivos de paquete de configuración. Es posible que tenga que realizar otras tareas, por ejemplo, configurar el centro de configuración de la empresa para definir cómo los usuarios interactúan con UE-V. En los siguientes temas se proporcionan instrucciones para administrar estos recursos de UE-V.

## Configuración de UE-V 2. x mediante objetos de directiva de grupo


Puede usar objetos de directiva de grupo para modificar la configuración que define cómo UE-V sincroniza la configuración de los equipos.

[Configuración de UE-V 2. x con objetos de directiva de grupo](configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)

## Configuración de UE-V 2. x con System Center Configuration Manager 2012


Puede usar SystemCenter2012 ConfigurationManager para administrar el agente UE-V mediante el paquete de configuración de UE-V 2.

[Configuración de UE-V 2. x con System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)

## Administración de UE-V 2. x con PowerShell y WMI


UE-V proporciona cmdlets de Windows PowerShell, que pueden ayudar a los administradores a realizar varias tareas de UE-V.

[Administración de UE-V 2. x con Windows PowerShell y WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

## Configuración del centro de configuración de la compañía para UE-V 2. x


Puede configurar el centro de configuración de la empresa que se instala mediante el agente de UE-V para definir cómo los usuarios interactúan con UE-V.

[Configuración del centro de configuración de la compañía para UE-V 2. x](configuring-the-company-settings-center-for-ue-v-2x-both-uevv2.md)

## Ejemplos de opciones de configuración de UE-V 2. x


A continuación se muestran algunos ejemplos de parámetros de configuración de UE-V:

-   **Configuración ruta de almacenamiento:** Especifica la ubicación del recurso compartido de archivos que almacena la configuración de UE-V.

-   **Ruta del catálogo de plantillas de configuración:** Especifica la ruta de acceso UNC (Convención de nomenclatura universal) que define la ubicación en la que se comprobó la configuración de nuevas plantillas de ubicación de configuración.

-   **Registrar plantillas de Microsoft:** Especifica si se deben registrar las plantillas predeterminadas de Microsoft durante la instalación.

-   **Método de sincronización:** Especifica si UE-V usa el proveedor de sincronización o "ninguno". El "SyncProvider" admite equipos que están desconectados de la red. "Ninguno" se aplica cuando el equipo siempre está conectado a la red. Para obtener más información sobre el método de sincronización, vea [métodos de sincronización de UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).

-   **Tiempo de espera de sincronización:** Especifica el número de milisegundos que el equipo espera antes de que se agote el tiempo de espera cuando recupera la configuración de usuario de la ubicación de almacenamiento de configuración.

-   **Habilitar sincronización:** Especifica si la sincronización de configuración de UE-V está habilitada o deshabilitada.

-   **Tamaño máximo de paquete:** Especifica un tamaño de umbral de archivo de configuración de paquete en bytes en el que UE-V Agent notifica una advertencia.

-   **No sincronizar la configuración de la aplicación de Windows:** Especifica que UE-V no debe sincronizar las aplicaciones de Windows.

-   **Habilitar o deshabilitar la notificación de primer uso:** Especifica si UE-V muestra un cuadro de diálogo la primera vez que se ejecuta el agente UE-V en el equipo de un usuario.

-   **Activar/desactivar el icono de la bandeja:** Especifica si UE-V muestra un icono en el área de notificación y las notificaciones asociadas a él. El icono proporciona un vínculo al centro de configuración de la empresa.

-   **Hipervínculo de contacto personalizado:** Define la ruta de acceso, el texto y la descripción del vínculo **contactar con él** en el centro de configuración de la empresa.






## Temas relacionados


[Administración de UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Implementar funciones necesarias para UE-V 2.x](deploy-required-features-for-ue-v-2x-new-uevv2.md)

[Implementar UE-V 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 





