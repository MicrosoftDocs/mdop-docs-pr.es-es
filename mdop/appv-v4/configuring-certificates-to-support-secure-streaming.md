---
title: Configuración de certificados para admitir streaming seguro
description: Configuración de certificados para admitir streaming seguro
author: dansimp
ms.assetid: 88dc76d8-7745-4729-92a1-af089c921244
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9376634a1b9843f46dba4cd452e672cc9e535226
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821891"
---
# Configuración de certificados para admitir streaming seguro


De forma predeterminada, el servicio App-V se ejecuta en la cuenta servicio de red. Sin embargo, puede crear una cuenta de servicio en servicios de dominio de Active Directory y reemplazar la cuenta de servicio de red con la cuenta de dominio de Active Directory.

El contexto de seguridad en el que se ejecuta el servicio es importante para configurar las comunicaciones seguras mejoradas. Este contexto de seguridad debe tener permisos de lectura para la clave privada del certificado. Cuando se genera una *solicitud de firma de certificado* (CSR) PKCS \ #10 para el servidor de App-V, se llama al proveedor de *servicios criptográficos* de Windows y se genera una clave privada. La clave privada está protegida con permisos otorgados únicamente a las cuentas del sistema y del administrador.

Debe modificar las listas de control de acceso (ACL) en la clave privada para permitir que el servidor de administración o streaming de App-V acceda a la clave privada necesaria para una comunicación segura de TLS correcta.

## Obtener e instalar un certificado


Los escenarios para obtener e instalar un certificado para App-V son los siguientes:

-   Infraestructura de clave pública (PKI) interna.

-   Certificado de terceros que emite la entidad de certificación (CA).

    **Nota:**  Si necesita obtener un certificado de una entidad emisora de certificados de terceros, siga la documentación disponible en el sitio web de dicha entidad.

     

Si se ha implementado una infraestructura PKI, consulte a los administradores de PKI para adquirir un certificado que cumpla con los requisitos que se describen en este tema. Si la infraestructura de PKI no está disponible, use una entidad de certificación de terceros para obtener un certificado válido.

Para obtener instrucciones paso a paso para obtener e instalar un certificado, consulte <https://go.microsoft.com/fwlink/?LinkId=151969> .

## Temas relacionados


Configurar certificados para admitir la transmisión por secuencias segura [Cómo modificar los permisos de clave privada para admitir el servidor de administración o el servidor de transmisión](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





