---
title: Cómo hacer copia de seguridad y restaurar un servidor de MED-V
description: Cómo hacer copia de seguridad y restaurar un servidor de MED-V
author: dansimp
ms.assetid: 8d05e3a4-279b-4ce6-a319-8a09e7a30c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d51cfe3727896ed68a1fd67441174a294a1073cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823090"
---
# Cómo hacer copia de seguridad y restaurar un servidor de MED-V


Se puede realizar una copia de seguridad de los archivos XML que se encuentran en el servidor y restaurarlos en caso de pérdida de datos en el servidor.

**Para hacer una copia de seguridad de un servidor de MED-V**

-   Haga una copia de seguridad de los archivos siguientes, que se encuentran en * &lt; INSTALLDIR &gt; \\Servers\\ConfigurationServer*:

    **Nota:**  Si se ha cambiado la configuración predeterminada, es posible que los archivos se hayan almacenado en una ubicación diferente.

     

    -   ClientPolicy.xml

    -   ClientSettings.xml

    -   ConfigurationFiles.xml

    -   OrganizationPolicy.xml

    -   WorkspaceKeys.xml

    **Nota:**  También se puede realizar una copia de seguridad del archivo de ServerSettings.xml. Sin embargo, si se ha cambiado una configuración específica (por ejemplo, en el servidor original, el directorio VM MED-V se encuentra en "*C:\\Vms*" y dicho directorio no existe en el nuevo servidor), puede provocar un error.

     

**Para restaurar un servidor de MED-V**

1.  Instalar un nuevo servidor de MED-V.

2.  Copie los archivos de copia de seguridad en el siguiente directorio:

    *&lt;InstallDir &gt; \\Servers\\ConfigurationServer*

3.  Reinicie el servicio MED-V.

 

 





