---
title: Configuración de certificados para admitir el servidor de administración de App-V o el servidor de streaming
description: Configuración de certificados para admitir el servidor de administración de App-V o el servidor de streaming
author: dansimp
ms.assetid: 2f24e550-585e-4b7e-b486-22a3f181f543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e537244b24d7303af550b3ced8286ba2680009e7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821900"
---
# Configuración de certificados para admitir el servidor de administración de App-V o el servidor de streaming


Después de completar el proceso de aprovisionamiento de certificados y cambiar los permisos de clave privada para admitir la instalación de App-V, puede iniciar la configuración del servidor de administración o del servidor de streaming. Durante la configuración, si se aprovisiona un certificado antes de ejecutar el programa de instalación, el asistente muestra el certificado en la pantalla **modo de seguridad de conexión** y, de forma predeterminada, la casilla **usar seguridad mejorada** está activada.

**Nota:**  Seleccione el certificado que se configuró para App-V si hay más de un certificado aprovisionado para este servidor.

 

**Importante**  Al actualizar de la versión 4,2 a la 4,5, la configuración tiene una opción para **usar seguridad mejorada**. sin embargo, si selecciona esta opción, no se deshabilitará la transmisión por RTSP. Debe usar la consola de administración para deshabilitar RTSP después de la instalación.

 

Seleccione el puerto TCP que usará el servicio para las comunicaciones de cliente. El puerto predeterminado es TCP 322; sin embargo, puede cambiar el puerto a un puerto personalizado para su entorno.

Los pasos restantes del asistente son los mismos que si estuviera implementando un servidor de administración o streaming de App-V sin usar la característica de **seguridad mejorada** .

## Configuración de certificados para entornos NLB


Para admitir grandes empresas, a menudo el servidor de administración se coloca en un clúster de equilibrio de carga en la red (NLB) para admitir el gran número de conexiones. Esto requiere al menos dos servidores de administración que parecen ser un único servidor de administración. Cuando su entorno usa un clúster NLB con varios servidores de administración, necesita una configuración avanzada del certificado que se usa para el clúster NLB.

El certificado de App-V se envía a una entidad de certificación (CA) que está configurada en un equipo con Windows Server2003. El SAN le permite conectarse a un nombre de host de clúster NLB de servidor de administración específico mediante un nombre de sistema de nombres de dominio (DNS) que puede diferir de los nombres reales de los equipos, porque puede haber hasta 32 servidores que componen el clúster NLB.

Esta configuración solo es necesaria cuando se usa un clúster NLB. Cuando el cliente se conecte al servidor, se conectará usando el nombre de dominio completo (FQDN) del clúster NLB y no el FQDN de un servidor individual. Si no agrega la propiedad SAN con el FQDN de los nodos del servidor en el clúster, se rechazan todas las conexiones de cliente porque el nombre común del certificado no coincide con el nombre del servidor.

Para obtener información más detallada sobre la configuración de certificados con el atributo SAN, consulte <https://go.microsoft.com/fwlink/?LinkId=133228> .

## Temas relacionados


[Configuración de certificados para admitir streaming seguro](configuring-certificates-to-support-secure-streaming.md)

[Cómo modificar los permisos de la clave privada al servidor de administración de soporte técnico o servidor de streaming](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





