---
title: Página Archivos de instalación
description: Página Archivos de instalación
author: dansimp
ms.assetid: b0aad26f-b143-4f09-87a1-9f016a23cb62
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 08a2e7318271503f072298ca137a1e65e16c0178
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816341"
---
# Página Archivos de instalación


Use la página **archivos de instalación** para especificar los archivos de instalación que se usaron para crear el paquete de aplicaciones virtual especificado en la página **seleccionar paquete** de este asistente. Si ha creado un paquete de aplicaciones virtual que contiene varias aplicaciones, debe copiar todos los archivos de instalación necesarios en una sola carpeta del equipo que ejecuta Microsoft Application Virtualization Sequencer.

Esta página contiene los siguientes elementos:

<a href="" id="original-installation-files"></a>**Archivos de instalación original**  
Haga clic en **examinar** para especificar los archivos de instalación que se usaron originalmente para crear el paquete de aplicación virtual. El directorio principal que especifique debe guardarse localmente en el equipo que ejecuta el secuenciador y debe contener todos los archivos o subcarpetas necesarios para la instalación que contengan los archivos de instalación. Los archivos de instalación pueden estar contenidos en la carpeta principal o en cualquiera de las subcarpetas de la carpeta principal especificada.

<a href="" id="files-installed-on-local-system"></a>**Archivos instalados en el sistema local**  
Haga clic en **examinar** para especificar los archivos de instalación que se han instalado localmente en el equipo que ejecuta el secuenciador. Solo puede seleccionar esta opción si los archivos de instalación de la aplicación se instalaron en la ubicación predeterminada de la aplicación.

**Nota:**  La ubicación de instalación predeterminada que proporcione dependerá de las siguientes condiciones:

 

-   La raíz del paquete especificada cuando el paquete se creó originalmente.

-   La ubicación de instalación especificada en Windows Installer cuando el paquete se creó originalmente.

-   La ruta de instalación predeterminada de la aplicación.

Por ejemplo, si la raíz del paquete especificada es **Q:\\Office12** y durante la instalación, la ubicación de instalación predeterminada cambia de **c:\\Archivos de Files\\Office12** a **Q:\\Office12**, la ruta especificada durante la deshidratación debe ser **c:\\Archivos de Files\\Office 12**.

Si la raíz del paquete especificada es **Q:\\Microsoft** y durante la instalación, la ubicación de instalación predeterminada cambia de **c:\\Archivos de Files\\Office12** a **Q:\\Microsoft\\Office12**, la ruta de acceso especificada durante la deshidratación debe ser c:\\Archivos de **programa**.

Al crear un paquete con un acelerador de paquetes, cada archivo del paquete, por ejemplo **Q:\\Office12\\file.txt** se encuentra en el equipo local reemplazando la raíz del paquete **Q:\\Office12** por la ubicación predeterminada especificada cuando se creó el acelerador de paquetes, por ejemplo, **c:\\Archivos de Files\\Office12**. En el ejemplo anterior, el archivo debe estar ubicado en **c:\\Archivos de Files\\Office12\\file.txt**.

## Temas relacionados


[Crear asistente del acelerador de paquetes (AppV 4.6 SP1)](create-package-accelerator-wizard--appv-46-sp1-.md)

 

 





