---
title: Cómo instalar el cliente mediante el uso de la línea de comandos
description: Cómo instalar el cliente mediante el uso de la línea de comandos
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817321"
---
# Cómo instalar el cliente mediante el uso de la línea de comandos


En los temas de esta sección se incluyen procedimientos para instalar el cliente de escritorio de Application Virtualization (App-V) o el cliente de App-V para servicios de escritorio remoto (anteriormente servicios de Terminal Server) con setup.exe o setup.msi. Los derechos administrativos son necesarios para ejecutar el programa de instalación.

Puede usar parámetros opcionales de la línea de comandos para aplicar valores de configuración específicos al cliente de App-V durante la instalación. Para obtener más información sobre el uso de parámetros, consulte [parámetros de la línea de comandos del instalador de cliente de virtualización de aplicaciones](application-virtualization-client-installer-command-line-parameters.md). Si ha aplicado la configuración del registro a un equipo antes de implementar un cliente, por ejemplo, mediante la Directiva de grupo, se conservan estas opciones de configuración y se aplican los parámetros adicionales de la línea de comandos. Los valores del parámetro de la línea de comandos reemplazarán cualquier valor existente para la misma configuración.

**Nota:**  Al instalar el cliente de App-V para usarlo con una caché de solo lectura, por ejemplo, con una implementación de servidor VDI, debe establecer el parámetro *AUTOLOADTARGET* en None para evitar que el cliente intente actualizar aplicaciones cuando la caché es de solo lectura.

 

Para obtener más información sobre la configuración de estos valores de parámetro después de la instalación, consulte [Cómo configurar la configuración del registro del cliente de App-v con la línea de comandos](https://go.microsoft.com/fwlink/?LinkId=169355) ( https://go.microsoft.com/fwlink/?LinkId=169355) en la guía de operaciones de Application Virtualization (App-v).

**Nota:**  Si una opción de configuración en el equipo del usuario depende de la ruta de instalación del cliente, tenga en cuenta que el cliente de Application Virtualization (App-V) 4.5 copia sus archivos de instalación en una carpeta diferente de la de versiones anteriores. De forma predeterminada, una nueva instalación del cliente de App-V 4.5 copiará sus archivos de instalación en la carpeta \\Archivos de Programa\\microsoft Application Virtualization Client. Si ya está instalada una versión anterior del cliente, la ejecución del instalador del cliente de App-V 4,5 realizará una actualización del cliente existente mediante la carpeta de instalación existente.

 

\ [Valor del token de plantilla \]

**Nota:**  Para la versión 4.6 de App-V y versiones posteriores, cuando el cliente de App-V está instalado, SFTLDR.DLL se copia en el directorio Windows\\system32. Si el cliente de App-V está instalado en un sistema de 64 bits, SFTLDR\_WOW64.DLL se copia en el directorio Windows\\SysWOW64.

 

\ [Valor del token de plantilla \]

## En esta sección


En los temas siguientes, se describe cómo instalar el cliente de escritorio de Application Virtualization (App-V) o el cliente de App-V para servicios de escritorio remoto (anteriormente servicios de Terminal Server) usando setup.exe o setup.msi.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[Cómo instalar el cliente de App-V mediante el uso de Setup.exe](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
Proporciona un procedimiento paso a paso para instalar el cliente de App-V con el programa setup.exe.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[Cómo instalar el cliente de App-V mediante el uso de Setup.msi](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
Proporciona procedimientos paso a paso para instalar cualquier software necesario y también el cliente de App-V mediante el programa de setup.msi.

## Temas relacionados


[Parámetros de línea de comandos de instalador de cliente de virtualización de aplicaciones](application-virtualization-client-installer-command-line-parameters.md)

[Cómo instalar manualmente el cliente de virtualización de aplicaciones](how-to-manually-install-the-application-virtualization-client.md)

[Cómo publicar una aplicación virtual en el cliente](how-to-publish-a-virtual-application-on-the-client.md)

[Cómo desinstalar el cliente de App-V](how-to-uninstall-the-app-v-client.md)

 

 





