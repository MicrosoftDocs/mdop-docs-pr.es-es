---
title: Configuración del centro de configuración de la compañía para UE-V 2. x
description: Configuración del centro de configuración de la compañía para UE-V 2. x
author: dansimp
ms.assetid: 48fadb0a-c0dc-4287-9474-f94ce1417003
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0226b3c156a6d6ca39b0214de8acf0c5990db349
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823291"
---
# Configuración del centro de configuración de la compañía para UE-V 2. x


La virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1 SP1 incluye una nueva aplicación, el centro de configuración de la compañía, que ayuda a los usuarios a administrar la configuración para sincronizar. El centro de configuración de la empresa se instala mediante el agente de UE-V. Los usuarios acceden al centro de configuración de la compañía en el panel de control, en el menú **Inicio** o en la pantalla de **Inicio** , y a través del icono del área de notificación de UE-V. Centro de configuración de la empresa muestra qué configuración se sincroniza y permite a los usuarios ver el estado de sincronización de UE-V. Los usuarios pueden usar el centro de configuración de la compañía para seleccionar las aplicaciones o características de Windows que sincronizan su configuración entre equipos. También puede hacer clic en el botón **sincronizar ahora** para sincronizar toda la configuración inmediatamente. El administrador también puede incluir un vínculo para obtener soporte técnico en el centro de configuración de la empresa.

## Acerca del centro de configuración de la empresa


La aplicación de escritorio Centro de configuración de la compañía proporciona a los usuarios información sobre la sincronización de configuración de UE-V. El centro de configuración de la empresa es accesible de varias maneras diferentes:

-   Icono del área de notificación: con la configuración de directiva de grupo del icono de la **bandeja** o la configuración de Windows PowerShell habilitada, el icono UE-V aparece en el área de notificación. Haga clic en el icono UE-V para abrir el centro de configuración de la compañía.

    **Nota:**  El icono del área de notificación se puede deshabilitar con las siguientes opciones:

    -   Configuración de directiva de Grupo: `Policy Tray Icon`

    -   Cmdlet de Windows PowerShell: `TrayIconEnabled`

    -   Elemento de configuración del paquete de configuración de UE-V para SystemCenter2012 ConfigurationManager: `Tray icon enabled`

     

-   Aplicación panel de control: en el panel de control, vaya a **apariencia y personalización**y, después, haga clic en **centro de configuración**de la empresa.

-   Notificación de primer uso: a menos que se deshabilite, el agente de UE-V avisa al usuario de que la configuración se ha sincronizado ahora cuando el agente de UE-V se ejecuta por primera vez en un equipo. Haga clic en el cuadro de diálogo notificación para abrir el centro de configuración de la compañía.

-   La pantalla **Inicio** o el menú **Inicio** incluyen un vínculo al centro de configuración de la empresa. Una búsqueda de centro de configuración de la compañía encuentra la aplicación.

## Configurar el vínculo de soporte técnico en el centro de configuración de la compañía


El centro de configuración de la compañía puede incluir un hipervínculo en el que los usuarios pueden hacer clic para obtener soporte técnico con problemas de sincronización de configuración de UE-V. Este vínculo puede abrir cualquier protocolo de dirección URL válido, como http://para una página web o mailto://para un correo electrónico. El vínculo de soporte técnico se puede configurar mediante la Directiva de grupo, Windows PowerShell o el paquete de configuración System Center 2012 Configuration Manager UE-V.

**Cómo configurar el vínculo de soporte técnico del centro de configuración de empresa**

1.  Abra su herramienta de administración preferida:

    -   **Directiva de grupo** : Si aún no lo ha hecho, descargue la plantilla ADMX para UE-V 2 de [las plantillas administrativas de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=393941).

    -   **Windows PowerShell** : en un equipo con el agente UE-V instalado, Abra **Windows PowerShell**. Para obtener más información sobre la administración de UE-V mediante Windows PowerShell, consulte [Administering UE-v 2. x with Windows PowerShell and WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md).

    -   **Paquete de configuración de System Center 2012 para la virtualización de la experiencia del usuario de Microsoft (UE-v)** : importe el paquete de configuración de UE-v y siga la documentación del paquete de configuración para crear elementos de configuración. Para obtener más información sobre el paquete de configuración de UE-V, consulte [configuración de UE-v 2. x con System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md).

2.  Edite la configuración de las siguientes directivas:

    -   **Texto del vínculo contactar con ti** : esta opción especifica el texto del hipervínculo de la dirección URL del contacto en el centro de configuración de la empresa. Si habilita esta configuración, el centro de configuración de empresa muestra el texto especificado en el vínculo a la dirección URL de contacto.

        -   Configuración de directiva de Grupo: `Contact IT Link Text`

        -   Cmdlet de Windows PowerShell: `ContactITDescription`

        -   Elemento de configuración del paquete de configuración: `IT contact descriptive text`

    -   **Ponerse en contacto con el URL de ti** : esta opción especifica la dirección URL para el vínculo contactar con él en el centro de configuración de la empresa en un protocolo de dirección URL válido, como http://para una página web o mailto://para un correo electrónico.

        -   Configuración de directiva de Grupo: `Contact IT URL`

        -   Cmdlet de Windows PowerShell: `ContactITUrl`

        -   Elemento de configuración del paquete de configuración: `IT contact URL`

3.  Implementar la configuración en los equipos de los usuarios mediante la herramienta de administración.






 

 





