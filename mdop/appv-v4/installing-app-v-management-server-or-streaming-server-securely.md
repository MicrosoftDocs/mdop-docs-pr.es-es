---
title: Instalación de servidor de administración de App-V o servidor de streaming de forma segura
description: Instalación de servidor de administración de App-V o servidor de streaming de forma segura
author: dansimp
ms.assetid: d2a51a81-a80f-427c-a727-611e1eb74f02
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0150f4dc7f489731c4a818fed9780ebb25dbd24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816330"
---
# Instalación de servidor de administración de App-V o servidor de streaming de forma segura


Los temas de esta sección proporcionan información para instalar una versión de seguridad mejorada del servidor de administración de App-v o del servidor de streaming de App-V.

**Nota:**  La instalación o configuración de un servidor de administración o streaming de App-V para usar seguridad mejorada (por ejemplo, la seguridad de la capa de transporte o TLS) requiere que se haya aprovisionado un certificado X. 509 V3 en el servidor de App-V.

 

Cuando se prepare para instalar o configurar un servidor de administración o streaming seguro, tenga en cuenta los siguientes requisitos técnicos:

-   El certificado debe ser válido. Si el certificado no es válido, el cliente finaliza la conexión.

-   El certificado debe contener el *uso de clave mejorada* (EKU) correcto: autenticación de servidor (OID 1.3.6.1.5.5.7.3.1). Si el certificado no contiene este EKU, el cliente finaliza la conexión.

-   El nombre de dominio completo (FQDN) del certificado debe coincidir con el servidor en el que está instalado. Por ejemplo, si el cliente está llamando `RTSPS://Myserver.mycompany.com/content/MyApp.sft` y se establece el valor de certificado **emitido para** `Server1.mycompany.com` , el cliente no se conectará al servidor y la sesión finalizará. El error se notifica al usuario.

    **Nota:**  Si está usando App-V en un clúster de equilibrio de carga de red, debe configurar el certificado con nombres alternativos de asunto (San) para admitir RTSPs. Para obtener información sobre la configuración de la entidad emisora de certificados (CA) y la creación de certificados con redes SAN, consulte <https://go.microsoft.com/fwlink/?LinkId=133228> .

     

-   El cliente y el servidor necesitan confiar en la entidad emisora raíz (la CA que emite el certificado al servidor de App-V debe confiar en el cliente que se conecta al servidor). En caso contrario, el cliente finaliza la conexión.

-   La clave privada del certificado debe tener permisos cambiados para permitir que la cuenta de servicio de App-V pueda acceder al certificado. De forma predeterminada, App-V usa la cuenta servicio de red y, de forma predeterminada, la cuenta servicio de red no tiene permiso para obtener acceso a la clave privada, lo que evitará conexiones seguras.

## En esta sección


<a href="" id="configuring-certificates-to-support-secure-streaming"></a>[Configuración de certificados para admitir streaming seguro](configuring-certificates-to-support-secure-streaming.md)  
Proporciona información sobre cómo obtener, configurar e instalar certificados para admitir la transmisión por secuencias segura.

<a href="" id="how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server"></a>[Cómo modificar los permisos de la clave privada al servidor de administración de soporte técnico o servidor de streaming](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)  
Proporciona procedimientos que puede usar para modificar claves en Windows Server2003 y Windows Server2008.

<a href="" id="configuring-certificates-to-support-app-v-management-server-or-streaming-server"></a>[Configuración de certificados para admitir el servidor de administración de App-V o el servidor de streaming](configuring-certificates-to-support-app-v-management-server-or-streaming-server.md)  
Proporciona información sobre cómo configurar certificados para los servidores de administración o streaming de App-V, incluida información sobre la configuración de certificados para entornos de equilibrio de carga de red.

 

 





