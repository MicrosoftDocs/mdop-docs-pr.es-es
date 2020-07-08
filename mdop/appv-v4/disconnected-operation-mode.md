---
title: Modo de operación desconectado
description: Modo de operación desconectado
author: dansimp
ms.assetid: 3f9849ea-ba53-4c68-85d3-87a4218f59c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6e9534b93f23b17e5258ef5e2d548eb93213f2f8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821621"
---
# Modo de operación desconectado


La configuración del modo de funcionamiento desconectado: accesible haciendo clic con el botón secundario en el nodo de **virtualización de aplicaciones** , seleccionando **propiedades**y haciendo clic en la pestaña **Conectividad** , permite que el cliente de escritorio de Application Virtualization o el cliente de servicios de escritorio remoto (anteriormente servicios de Terminal Server) ejecuten aplicaciones que se almacenan en la memoria caché del sistema de archivos cuando el cliente no

Las razones por las que no se puede conectar con el servidor son: error del servidor, interrupción de la red o desconexión de la red. Si se produce algún error, el cliente cambiará automáticamente a la operación desconectada. Una vez desconectado, si el cliente necesita más datos del servidor para continuar ejecutando una aplicación o si el tiempo de espera de la operación de desconexión se agota, el cliente intentará volver a conectarse al servidor. Si se produce un error en este intento de conexión, la aplicación se cerrará.

De forma predeterminada, la operación desconectada está habilitada y el tiempo de espera está establecido en 90 días. El valor de tiempo de espera se especifica como el número de días que desea limitar el modo de funcionamiento desconectado y puede escribir un valor de 1 a 999.

## Temas relacionados


[Cómo deshabilitar o modificar la configuración de modo de operación desconectado](how-to-disable-or-modify-disconnected-operation-mode-settings.md)

 

 





