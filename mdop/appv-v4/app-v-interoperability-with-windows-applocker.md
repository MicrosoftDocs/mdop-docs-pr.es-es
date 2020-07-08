---
title: Interoperabilidad de App-V con Windows AppLocker
description: Interoperabilidad de App-V con Windows AppLocker
author: dansimp
ms.assetid: 9a488034-607d-411c-b495-ff184c726f49
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 6f67bb87c0a4474acee3c4982b65c930e86c4917
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822311"
---
# Interoperabilidad de App-V con Windows AppLocker


La versión 4,5 del cliente de Microsoft Application Virtualization (App-V) es compatible con la característica AppLocker de Windows 7. La característica AppLocker permite a los administradores de ti especificar qué aplicaciones están restringidas para su ejecución en equipos. En este documento se describe cómo configurar las reglas de AppLocker para que funcionen con el entorno virtual de App-V y las aplicaciones virtualizadas.

**Nota:**  Windows AppLocker debe habilitarse primero antes de configurar las reglas de Windows AppLocker para las aplicaciones virtuales. Para obtener más información sobre cómo habilitar Windows AppLocker, [Windows AppLocker](https://go.microsoft.com/fwlink/?LinkId=156732) ( https://go.microsoft.com/fwlink/?LinkId=156732) .

 

## Configuración de reglas de Windows AppLocker para aplicaciones virtuales


Los administradores locales pueden crear reglas de Windows AppLocker que restringen la ejecución de programas ejecutables (archivos. exe), archivos de Windows Installer (archivos. msi y. msp) y scripts (archivos. PS,. bat,. cmd,. vbs y. js). El administrador realiza esta acción usando un equipo de referencia que tiene el cliente de App-V instalado y que tiene todas las aplicaciones virtuales relevantes transmitidas a la memoria caché del cliente. Después, el administrador usa la sección Windows AppLocker del complemento de Microsoft Management Console (MMC) Directiva de seguridad local en el equipo de referencia para crear las reglas.

Al examinar para buscar una ruta de acceso de directorio o un archivo específico para el que desea crear una regla, puede acceder a la unidad de App-V usando la ruta de acceso al recurso compartido oculto. Por ejemplo, puedes ir a \\\\localhost\\Q $, donde la unidad de App-V es la unidad Q. Sin embargo, para crear la regla, debe editar la ruta de acceso para quitar la referencia a \\\\localhost\\Q $ y usar Q:\\ en su lugar. Para poder acceder a los archivos de la aplicación, debe iniciar cada una de las aplicaciones en el equipo de referencia y es necesario disponer de derechos administrativos para ir a \\\\localhost\\Q $.

 

 





