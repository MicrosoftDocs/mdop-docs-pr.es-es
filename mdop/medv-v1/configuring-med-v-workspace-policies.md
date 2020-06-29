---
title: Configuración de directivas de área de trabajo de MED-V
description: Configuración de directivas de área de trabajo de MED-V
author: dansimp
ms.assetid: 0eaed981-cbf3-4b16-a4b7-4705c5705dc7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84bdae38b1c801e2c2be2a3dd1d12dd2ca7d932d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824860"
---
# Configuración de directivas de área de trabajo de MED-V


Una directiva de área de trabajo de MED-V es un grupo de parámetros configurables que definen cómo los entornos virtualizados y las aplicaciones se ejecutan en el equipo host. En los temas de esta sección se describen todas las opciones configurables en la Directiva de área de trabajo de MED-V, así como la influencia de esta configuración en el área de trabajo de MED-V.

Están disponibles los siguientes tipos de áreas de trabajo de MED-V:

-   **Persistente**: en un área de trabajo de Med-v persistente, todos los cambios y adiciones que el usuario realiza en el área de trabajo de Med-v se guardan en el área de trabajo de Med-v entre sesiones. Además, un área de trabajo de MED-V persistente se usa generalmente en un entorno de dominio.

-   Revertido: en un área de trabajo **revertida de**Med-v, al finalizar cada sesión (es decir, cuando se detiene el área de trabajo de Med-v), el área de trabajo de Med-v vuelve a su estado original durante la implementación. Los cambios o adiciones que el usuario ha realizado se guardan en el área de trabajo de MED-V entre sesiones. No se puede usar un área de trabajo de MED-V revertida en un entorno de dominio.

Es importante que decida el tipo de área de trabajo de MED-V que está creando antes de implementar el área de trabajo de MED-V, porque no se recomienda volver a configurar el tipo de área de trabajo de MED-V después de implementar una directiva para los usuarios.

**Nota:**  Al configurar una directiva, aparece un símbolo de advertencia junto a los campos obligatorios que no se han rellenado. Si no se rellena un campo obligatorio, el símbolo también aparece en la ficha.

 

## En esta sección


<a href="" id="how-to-apply-general-settings-to-a-med-v-workspace"></a>[Cómo aplicar la configuración general a un área de trabajo de MED-V](how-to-apply-general-settings-to-a-med-v-workspace.md)  
Describe la configuración general de un área de trabajo de MED-V y cómo aplicarla a una directiva.

<a href="" id="how-to-apply-virtual-machine-settings-to-a-med-v-workspace"></a>[Cómo aplicar la configuración de máquina virtual en un área de trabajo de MED-V](how-to-apply-virtual-machine-settings-to-a-med-v-workspace.md)  
Describe la configuración de la máquina virtual para un área de trabajo de MED-V y cómo aplicarla a una directiva.

<a href="" id="how-to-configure-a-domain-user-or-group"></a>[Cómo configurar un usuario de dominio o un grupo](how-to-configure-a-domain-user-or-groupmedvv2.md)  
Describe cómo configurar usuarios y grupos de dominio.

<a href="" id="how-to-configure-published-applications"></a>[Cómo configurar las aplicaciones publicadas](how-to-configure-published-applicationsmedvv2.md)  
Describe las aplicaciones y menús publicados, y cómo aplicarlos a una directiva.

<a href="" id="how-to-configure-web-settings-for-a-med-v-workspace"></a>[Cómo configurar la configuración de web para un área de trabajo de MED-V](how-to-configure-web-settings-for-a-med-v-workspace.md)  
Describe la configuración Web disponible para un área de trabajo de MED-V y cómo aplicarla a una directiva.

<a href="" id="how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace"></a>[Cómo configurar la configuración de máquina virtual para un área de trabajo de MED-V](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspace.md)  
Describe la configuración de la máquina virtual para un área de trabajo de MED-V y cómo aplicarla a una directiva.

<a href="" id="how-to-apply-network-settings-to-a-med-v-workspace"></a>[Cómo aplicar la configuración de red en un área de trabajo de MED-V](how-to-apply-network-settings-to-a-med-v-workspace.md)  
Describe la configuración de red de un área de trabajo de MED-V y cómo aplicarla a una directiva.

<a href="" id="how-to-apply-performance-settings-to-a-med-v-workspace"></a>[Cómo aplicar la configuración de rendimiento a un área de trabajo de MED-V](how-to-apply-performance-settings-to-a-med-v-workspace.md)  
Describe la configuración de rendimiento de un área de trabajo de MED-V y cómo aplicarla a una directiva.

<a href="" id="how-to-import-and-export-a-policy"></a>[Cómo importar y exportar una directiva](how-to-import-and-export-a-policy.md)  
Describe cómo importar y exportar una directiva.

 

 





