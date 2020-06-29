---
title: Cómo modificar los permisos de la clave privada al servidor de administración de soporte técnico o servidor de streaming
description: Cómo modificar los permisos de la clave privada al servidor de administración de soporte técnico o servidor de streaming
author: dansimp
ms.assetid: 1ebe86fa-0fbc-4512-aebc-0a5da991cd43
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e35c2df518f22ba81a070d2c40ad3862f376a6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817030"
---
# Cómo modificar los permisos de la clave privada al servidor de administración de soporte técnico o servidor de streaming


Para admitir una instalación de App-V más segura, puede usar los procedimientos siguientes para modificar las claves privadas en Windows Server2003 o en Windows Server2008. Para modificar los permisos de la clave privada, puede usar la herramienta kit de recursos de Windows Server2003 `WinHttpCertCfg.exe` .

Para Windows Server2003, el procedimiento requiere que un certificado que cumpla los requisitos previos enumerados en este documento esté instalado en el equipo o los equipos en los que instalará el servidor de streaming o administración de App-V. Encontrará más información sobre el uso de la `WinHttpCertCfg.exe` herramienta en <https://go.microsoft.com/fwlink/?LinkId=151981> .

En Windows Server2008, el proceso de cambiar las ACL en la clave privada es mucho más simple. La interfaz de usuario del certificado se puede usar para administrar los permisos de clave privada.

**Nota:**  El contexto de seguridad predeterminado es servicio de red. sin embargo, en su lugar se puede usar una cuenta de dominio.

 

**Para administrar las claves privadas en Windows Server2003**

1.  En el equipo que se convertirá en el servidor de administración o streaming de App-V, escriba el siguiente comando en un símbolo del sistema para mostrar los permisos actuales asignados a un certificado específico:

    `winhttpcertcfg -l -c LOCAL_MACHINE\My -s Name_of_cert`

2.  Si es necesario, modifique los permisos del certificado para proporcionar acceso de lectura al contexto de seguridad que se usará para el servicio de administración o transmisión por secuencias:

    `winhttpcertcfg -g -c LOCAL_MACHINE\My -s Name_of_cert -a NetworkService`

3.  Compruebe que el contexto de seguridad se haya agregado correctamente mediante una lista de los permisos en el certificado:

    `winhttpcertcfg –l –c LOCAL_MACHINE\My –s Name_of_cert`

**Para administrar las claves privadas en Windows Server2008**

1.  Cree una consola de administración de Microsoft (MMC) con el complemento *certificados* que se dirige al almacén de certificados de la *máquina local* .

2.  Expanda la consola MMC y seleccione **administrar claves privadas**.

3.  En la pestaña **seguridad** , agregue la cuenta **servicio de red** con acceso de **lectura** .

## Temas relacionados


[Configuración de certificados para admitir el servidor de administración de App-V o el servidor de streaming](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)

[Configuración de certificados para admitir streaming seguro](configuring-certificates-to-support-secure-streaming.md)

 

 





