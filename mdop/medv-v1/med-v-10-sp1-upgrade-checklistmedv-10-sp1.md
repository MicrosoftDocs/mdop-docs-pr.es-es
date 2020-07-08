---
title: Lista de comprobación de actualización MED-V 1.0 SP1
description: Lista de comprobación de actualización MED-V 1.0 SP1
author: dansimp
ms.assetid: 1a462b37-8c7a-4826-9175-0b1b701d345b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9c418eff8dfb6146204d7d9212d42e49db000fb1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827270"
---
# Lista de comprobación de actualización MED-V 1.0 SP1


Para actualizar Microsoft Enterprise Desktop Virtualization (MED-V) 1.0 a MED-V 1.0 Service Pack1 (SP1), el cliente debe estar actualizado. De forma opcional, el servidor puede actualizarse.

## Actualización de servidor


**Para actualizar el servidor MED-V 1.0 a MED-V 1.0 SP1**

1.  Haga una copia de seguridad de los siguientes archivos que se encuentran en el directorio * &lt; INSTALLDIR &gt; /Servers/ConfigurationServer* :

    -   OrganizationalPolicy.XML

    -   ClientPolicy.XML

    -   WorkspaceKeys.XML

2.  Haga una copia de seguridad del archivo * &lt; INSTALLDIR &gt; /servers/ServerSettings.xml* .

3.  Desinstale el servidor MED-V 1.0.

4.  Instale el servidor MED-V 1.0 SP1.

5.  Restaure los archivos de copia de seguridad en los directorios apropiados.

6.  Reinicie el servicio de servidor de MED-V.

**Nota:**  Si la configuración del servidor se ha cambiado de la predeterminada, es posible que los archivos se hayan almacenado en una ubicación diferente.

 

## Actualización de cliente


Para actualizar el cliente MED-V 1.0 a MED-V 1.0 SP1, instale el archivo. MSP en un cliente MED-V 1.0. El cliente y MED-V se actualizan automáticamente.

 

 





