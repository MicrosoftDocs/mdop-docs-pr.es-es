---
title: Uso de UE-V 2. x con aplicaciones de virtualización de aplicaciones
description: Uso de UE-V 2. x con aplicaciones de virtualización de aplicaciones
author: dansimp
ms.assetid: 4644b810-fc48-4fd0-96e4-2fc6cd64d8ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 221d21c5815b36b57a04a0299352e5fe64f657c5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827271"
---
# Uso de UE-V 2. x con aplicaciones de virtualización de aplicaciones


Virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1 SP1 son compatibles con aplicaciones de virtualización de aplicaciones (App-V) de Microsoft sin ninguna modificación necesaria para el paquete de App-V o la plantilla UE-V. Sin embargo, se requiere un paso adicional porque no puede ejecutar el generador de UE-V directamente en una aplicación de App-V virtualizada. En su lugar, debe instalar la aplicación de forma local, generar la plantilla y, a continuación, aplicar la plantilla a la aplicación virtualizada. UE-V admite los paquetes de App-V 4,5, App-V 4,6 y App-V 5,0.

## Sincronización de configuración de UE-V para aplicaciones de App-V


Los monitores de UE-V cuando una aplicación se abre por el nombre del programa y, opcionalmente, por números de versión de archivo y números de versión del producto, si la aplicación se instala de forma local o virtualmente usando App-V. Cuando se inicia la aplicación, UE-V supervisa el proceso de App-V, aplica la configuración que se almacena en la ruta de almacenamiento de configuración del usuario y, a continuación, permite que la aplicación se inicie con normalidad. UE-V supervisa las aplicaciones de App-V y traduce automáticamente las rutas de archivos y de registro relevantes en la ubicación virtualizada, en lugar de en la ubicación física fuera del entorno informático de App-V.

 **Para implementar la sincronización de configuración de una aplicación virtualizada**

1.  Ejecute el generador de UE-V para recopilar la configuración de la aplicación instalada de forma local cuya configuración desea sincronizar entre equipos. Este proceso crea una plantilla de ubicación de configuración. Si usa una plantilla integrada, como la plantilla 2010 de Microsoft Office, omita este paso. Para obtener más información sobre cómo ejecutar el generador de UE-V, consulte [deploy UE-V 2. x para aplicaciones personalizadas](deploy-ue-v-2x-for-custom-applications-new-uevv2.md#createcustomtemplates).

2.  Instale el paquete de aplicación de App-V si todavía no lo ha hecho.

3.  Publique la plantilla en la ubicación del catálogo de plantillas de configuración o instale la plantilla manualmente mediante el `Register-UEVTemplate` cmdlet de Windows PowerShell.

    **Nota:**  Si publica la plantilla recién creada en el catálogo de plantillas de configuración, el cliente no recibirá la plantilla hasta que el proveedor de sincronización actualice la configuración. Para iniciar manualmente este proceso, Abra **el programador de tareas**, expanda la biblioteca del programador de **tareas**, expanda **Microsoft**y expanda **UE-V**. En el panel resultados, haga clic con el botón secundario en **actualización automática de plantillas**y, a continuación, haga clic en **Ejecutar**.

     

4.  Inicie el paquete de App-V.






## Temas relacionados


[Administración de UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

 

 





