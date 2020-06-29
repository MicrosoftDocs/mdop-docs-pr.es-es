---
title: Configurar el firewall para los servidores de App-V
description: Configurar el firewall para los servidores de App-V
author: dansimp
ms.assetid: f779c450-6c6f-46a8-ac66-5e82e0689d55
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 92db727eb060546ab71f2c647f2d89b662be5c64
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821820"
---
# Configurar el firewall para los servidores de App-V


Después de instalar el servidor de administración de Microsoft Application Virtualization (App-V) o el servidor de streaming y configurarlo para usar el protocolo RTSP o RTSPs, debe crear excepciones de Firewall para los programas de App-V.

## Configurar excepciones de Firewall para el servidor de administración de virtualización de aplicaciones


Cree una excepción de Firewall para **sghwdsptr.exe** y **sghwsvr.exe**. Estos programas se encuentran en la carpeta C:\\Archivos de Programa\\microsoft System Center App virt Management Server\\App virt Management Server\\bin en un sistema operativo de 32 bits. Si está usando una versión de sistema operativo de 64 bits, la carpeta se encuentra en C:\\Archivos de programa (x86) \\Microsoft System Center App virt Management Server\\App virt Management Server\\bin.

## Configurar excepciones de Firewall para el servidor de streaming de Application Virtualization


Cree una excepción de Firewall para **sglwdsptr.exe** y **sglwsvr.exe**. Estos programas se encuentran en la carpeta C:\\Archivos de Programa\\microsoft System Center App virt streaming Server\\App virt streaming Server\\bin en un sistema operativo de 32 bits. Si está usando una versión de sistema operativo de 64 bits, la carpeta se encuentra en C:\\Archivos de programa (x86) \\Microsoft System Center App virt streaming Server\\App virt streaming Server\\bin.

## Temas relacionados


[Cómo configurar servidores para implementación basada en servidor](how-to-configure-servers-for-server-based-deployment.md)

[Cómo instalar y configurar la aplicación predeterminada](how-to-install-and-configure-the-default-application.md)

 

 





