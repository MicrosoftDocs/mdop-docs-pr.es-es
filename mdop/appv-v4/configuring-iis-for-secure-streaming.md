---
title: Configuración de IIS para streaming seguro
description: Configuración de IIS para streaming seguro
author: dansimp
ms.assetid: 9a80a703-4642-4bec-b7af-dc7cb6b76925
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 724fd247d98c265421cea13f4b91c97049a2b4d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821881"
---
# Configuración de IIS para streaming seguro


Con el lanzamiento de Microsoft Application Virtualization (App-V) versión 4,5, puede usar HTTP y HTTPS como protocolos para transmitir paquetes de aplicaciones a los clientes de App-V. Esta opción permite a las organizaciones aprovechar la escalabilidad adicional que suele ofrecer IIS. Al usar IIS como servidor de transmisión, puede ayudar a proteger las comunicaciones entre el cliente y el servidor mediante HTTPS en lugar de HTTP.

**Nota:**  Si desea transmitir aplicaciones desde un servidor de archivos, debe mejorar la seguridad de las comunicaciones con los paquetes de la aplicación. Esto se puede lograr con IPsec. Para obtener más información, consulte los siguientes temas en la biblioteca de TechNet:

-   Para Windows Server2003, <https://go.microsoft.com/fwlink/?LinkId=133226>

-   Para Windows Server 2008, <https://go.microsoft.com/fwlink/?LinkId=133227>

 

## Tipos MIME


Al usar IIS para transmitir en secuencias aplicaciones virtuales con HTTP o HTTPS, para admitir App-V, se deben agregar los siguientes tipos MIME al servidor IIS:

-   . OSD = TXT

-   . SFT = Binary

Use los siguientes artículos de KB como instrucciones para agregar tipos MIME:

IIS 6,0: <https://go.microsoft.com/fwlink/?LinkId=151973>

IIS 7,0: <https://go.microsoft.com/fwlink/?LinkId=151977>

## Autenticación Kerberos


Cuando usa HTTP o HTTPS y la autenticación Kerberos para transmitir archivos ICO, OSD o SFT, está mejorando la seguridad de su entorno. Sin embargo, para que IIS admita la autenticación Kerberos, debe configurar un nombre principal de servicio (SPN) adecuado. La `setspn.exe` herramienta está disponible para Windows Server2003 en las herramientas de soporte técnico del CD de instalación y está integrada en Windows Server2008.

Para crear un SPN, ejecute `setspn.exe` desde un símbolo del sistema al iniciar sesión como miembro de administradores de dominio, por ejemplo, `setspn.exe –A HTTP/FQDN of Server ServerName` .

## Temas relacionados


[Configuración del servidor de administración o streaming para la postinstalación de comunicaciones seguras](configuring-management-or-streaming-server-for-secure-communications-post-installation.md)

 

 





