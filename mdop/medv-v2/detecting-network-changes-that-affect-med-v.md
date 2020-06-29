---
title: Detección de cambios de red que afectan a MED-V
description: Detección de cambios de red que afectan a MED-V
author: dansimp
ms.assetid: fd29b95a-cda2-464d-b86d-50b6bd64b4ca
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b5f43c30dee9ef8e06a7ae226849a4f21e83257c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823371"
---
# Detección de cambios de red que afectan a MED-V


La solución de virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0 le permite configurar su entorno para detectar determinados cambios de red que se pueden producir después de implementar áreas de trabajo de MED-V y que pueden afectar a MED-V.

La característica incluye un componente que se ejecuta en el sistema operativo invitado al que se le notifican los cambios de configuración de red en el equipo host. Permite a una aplicación de Microsoft ESD o de otro tipo que se está ejecutando en el invitado el mismo punto de conexión de red al que se resuelve el sistema ESD o la aplicación.

**Nota:**  Esta característica solo está disponible si la máquina virtual está configurada para el modo de traducción de direcciones de red (NAT). Si la máquina virtual está configurada para el modo de puente, no se genera ninguna indicación de cambio.

 

Esta sección proporciona información e instrucciones para ayudarle a supervisar los cambios en la red que pueden afectar a MED-V.

## Detectar cambios de red para MED-V


Después de haber implementado las áreas de trabajo de MED-V, puede supervisar los cambios en determinadas configuraciones de red preformando las siguientes tareas:

1. Cree un archivo de Managed Object Format (MOF) que buscará los cambios de configuración de red que desea supervisar. El código siguiente muestra un ejemplo del archivo MOF que puede crear.

   ``` syntax
   #pragma namespace ("\\\\.\\root\\ccm\\NetworkConfig")

   class CCM_IPConfig
   {
       [NotNull: ToInstance ToSubClass] uint32 AddressFamily; // AF_INET, AF_INET6
       [Key, NotNull: ToInstance ToSubClass] string IPAddress; // IPv4 or IPv6 address
       [NotNull: ToInstance ToSubClass] string SubnetMask; // IPv4 subnet mask
   };

   class CCM_NetworkAdapter
   {
       [Key, NotNull: ToInstance ToSubClass] string Name;
       [NotNull: ToInstance ToSubClass] uint32 DHCPEnabled = 0; 
       [NotNull: ToInstance ToSubClass] uint32 Quarantined = 0; // To check if it is quarantined.
       CCM_IPConfig IPConfigInfo[];
   };

   [singleton]
   class CCM_NetworkAdapters
   {
       [NotNull: ToInstance ToSubClass] String ProviderName; // MED-V or other provider
       CCM_NetworkAdapter AdaptersInfo[];
   };
   ```

2. Compile el archivo MOF.

3. Instale el archivo MOF en el invitado.

Una vez que haya instalado el archivo MOF, puede crear una suscripción de eventos que se suscriba a eventos de creación, modificación o eliminación de instrumental de administración de Windows (WMI) para la clase **CCM \ _NetworkAdapters** . Esto detecta los siguientes cambios en el host:

¿Hay algún cambio en la configuración de la red, como los cambios en la dirección IP o el adaptador de red?

¿Está la red disponible o no disponible?

¿Se cambió la configuración de red del modo puente al modo NAT?

¿Se cambió la configuración de red del modo NAT al modo puente?

Un componente MED-V del host supervisa la red para realizar estos cambios y, a continuación, indica al invitado el cambio. Un componente en el invitado crea una instancia de WMI para supervisar el área de trabajo de MED-V para estos cambios.

La suscripción de eventos que ha creado proporciona una notificación a través del sistema WMI cuando se producen uno o varios de estos cambios de red (creación, modificación o eliminación).

## Temas relacionados


[Áreas de trabajo de monitor MED-V](monitor-med-v-workspaces.md)

[Administrar la configuración del área de trabajo de MED-V](manage-med-v-workspace-settings.md)

 

 





