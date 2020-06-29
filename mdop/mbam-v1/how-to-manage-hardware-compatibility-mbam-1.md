---
title: Cómo administrar la compatibilidad de hardware
description: Cómo administrar la compatibilidad de hardware
author: dansimp
ms.assetid: c74b96b9-8161-49bc-b5bb-4838734e7df5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf9e2c5b2b33ea93d9834a81700bd2be8a9b9757
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812983"
---
# Cómo administrar la compatibilidad de hardware


Administración y supervisión de Microsoft BitLocker (MBAM) puede recopilar información sobre el fabricante y el modelo de equipos cliente después de implementar la Directiva de grupo permitir comprobación de la compatibilidad del hardware. Si configura esta Directiva, el agente de MBAM notifica la marca del equipo y la información del modelo al servidor de MBAM cuando se implementa el cliente MBAM en un equipo cliente.

La característica compatibilidad de hardware es útil cuando la organización tiene equipos o hardware de equipos antiguos que no son compatibles con los chips del módulo de plataforma segura (TPM). En estos casos, puede usar la característica compatibilidad de hardware para asegurarse de que el cifrado de BitLocker solo se aplica a los modelos de equipo que lo admiten. Si todos los equipos de su organización van a admitir BitLocker, no tiene que usar la característica de compatibilidad de hardware.

**Nota:**  De forma predeterminada, la característica de compatibilidad de hardware de MBAM no está habilitada. Para habilitarlo, seleccione la característica **compatibilidad de hardware** en la característica servidor de **Administración y supervisión** durante la instalación. Para obtener más información sobre cómo configurar y configurar la compatibilidad de hardware, consulte [implementación de la infraestructura de servidor de MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).

 

La característica compatibilidad de hardware funciona de la siguiente manera.

****

1.  El agente de cliente de MBAM descubre información básica del equipo, como el fabricante, el modelo, el creador de BIOS, la versión de BIOS, el creador de TPM y la versión de TPM y, a continuación, pasa esta información al servidor de MBAM.

2.  El servidor de MBAM genera una lista de las funciones y los modelos de equipos cliente que permiten diferenciar entre los que pueden o no son compatibles con BitLocker

3.  Los agentes de cliente de MBAM que se implementan en la empresa actualizan automáticamente esta lista con todos los nuevos equipos y los modelos que se detectan con un estado de **desconocido**. Un administrador puede usar el sitio web de administración de MBAM para cambiar las entradas de la lista y especificar una marca y un modelo de equipo determinado como **compatible** o **incompatible**.

4.  Antes de que el agente de cliente de MBAM empiece a cifrar una unidad, el agente verifica primero la compatibilidad de cifrado de BitLocker del hardware en el que se está ejecutando.

    -   Si el hardware está marcado como compatible, el proceso de cifrado de BitLocker se inicia. MBAM también volverá a comprobar el estado de compatibilidad de hardware del equipo una vez al día.

    -   Si el hardware se marca como incompatible, el agente registra un evento y pasa un estado de "hardware exento" como parte de los informes de cumplimiento normativo. El agente verifica cada siete días para ver si el estado ha cambiado a "compatible".

    -   Si el hardware está marcado como desconocido, el proceso de cifrado de BitLocker no se iniciará. El agente de cliente de MBAM volverá a comprobar el estado de compatibilidad de hardware del equipo una vez al día.

**ADVERTENCIA**  Si el agente de cliente de MBAM intenta cifrar un equipo que no es compatible con el cifrado de unidad BitLocker, existe la posibilidad de que se dañe el equipo. Asegúrese de que la característica compatibilidad de hardware esté correctamente configurada cuando su organización tenga hardware antiguo que no sea compatible con BitLocker.

 

**Para administrar la compatibilidad de hardware**

1.  Abra un explorador Web y navegue al sitio web de supervisión y administración de Microsoft BitLocker. Seleccione **hardware** en la barra de menús de la izquierda.

2.  En el panel derecho, haga clic en **búsqueda avanzada**y, a continuación, en filtrar para mostrar una lista de todos los modelos de equipos que tienen el estado de **capacidad** de **desconocido**. Se muestra una lista de modelos de equipo que coinciden con los criterios de búsqueda. Los administradores pueden agregar, editar o quitar nuevos tipos de equipos de esta página.

3.  Revise cada configuración de hardware desconocida para determinar si la configuración debe establecerse en **compatible** o **incompatible**.

4.  Seleccione una o más filas y, a continuación, haga clic en **establecer compatible** o **establecer como incompatible** para establecer la compatibilidad de BitLocker, según corresponda, para los modelos de equipos seleccionados. Si se establece en **compatible**, BitLocker intenta forzar la Directiva de cifrado de unidad en los equipos que coinciden con el modelo admitido. Si se establece en **incompatible**, BitLocker no aplicará la Directiva de cifrado de unidad en esos equipos.

    **Nota:**  Después de configurar un modelo de equipo como compatible, el cliente de MBAM puede tardar más de veinticuatro horas en iniciar el cifrado de BitLocker en los equipos que coincidan con ese modelo de hardware.

     

5.  Los administradores deben supervisar regularmente la lista de compatibilidad de hardware para revisar los nuevos modelos detectados por el agente de MBAM y, después, actualizar su configuración de compatibilidad a **compatible** o **incompatible** , según corresponda.

## Temas relacionados


[Administración de funciones de MBAM 1.0](administering-mbam-10-features.md)

 

 





