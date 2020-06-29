---
title: Configuración de App-V para administración segura
description: Configuración de App-V para administración segura
author: dansimp
ms.assetid: 4543fa81-c8cc-4b10-83b7-060778eb1349
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: de70c1df734bbf1168fd7dacf9410d3451a8a3c2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821901"
---
# Configuración de App-V para administración segura


En un entorno donde sea importante proteger las operaciones administrativas, App-V permite la comunicación segura entre el servicio de administración web de App-V y la consola de administración de App-V. Dado que el servicio de administración es una aplicación basada en Web, requiere la protección de la aplicación de servidor de administración de App-V en el servidor Web que hospeda el servicio de administración. Tal y como se muestra en la siguiente ilustración, este proceso incluye el uso de HTTPS para la comunicación y la configuración del servidor IIS para permitir únicamente la autenticación integrada de Windows.

![configuración de red del servicio Web de App-v](images/appvmgmtwebservice.gif)

El servicio de administración web de App-V se instala como una aplicación basada en Web en IIS. Para que el servicio de administración web admita conexiones seguras (SSL) entre la consola de administración de App-V y el servicio de administración web, tendrá que configurar el servidor IIS donde está instalado el servicio de administración web y configurar la consola de administración de App-V.

## En esta sección


<a href="" id="configuring-certificates-to-support-the-app-v-web-management-service"></a>[Configuración de certificados para admitir el servicio de administración web de App-V](configuring-certificates-to-support-the-app-v-web-management-service.md)  
Proporciona información útil sobre la configuración de certificados para admitir conexiones SSL, para ayudar a proteger la comunicación del servicio de administración web de App-V.

<a href="" id="how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment"></a>[Cómo instalar y configurar la consola de administración de App-V para un entorno más seguro](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)  
Proporciona un procedimiento paso a paso para conectarse a un servicio de administración web de App-V mediante una conexión segura.

 

 





