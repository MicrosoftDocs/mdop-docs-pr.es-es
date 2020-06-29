---
title: Arquitectura de alto nivel
description: Arquitectura de alto nivel
author: dansimp
ms.assetid: a78e12ad-5aa6-40e0-ae8b-51acaf005712
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 00df29c751653645ab4bee9762af57576a40092a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826201"
---
# Arquitectura de alto nivel


La solución MED-V consta de los siguientes elementos:

-   **Máquina virtual definida por el administrador**: encapsula un entorno de escritorio completo, incluido un sistema operativo, aplicaciones y herramientas de seguridad y administración opcionales.

-   **Repositorio de imágenes**: almacena todas las imágenes virtuales en un servidor IIS estándar y habilita la administración de versiones de imágenes virtuales, la recuperación de imágenes autenticadas por el cliente y la descarga eficaz (de una nueva imagen o actualizaciones) a través de la tecnología de transferencia de recorte.

-   **Servidor de administración**: asocia imágenes virtuales del repositorio de imágenes junto con directivas de uso del administrador a usuarios o grupos de Active Directory®. El servidor de administración también agrega eventos de clientes y los almacena en una base de datos externa (Microsoft SQL Server®) para fines de supervisión e informes.

-   **Consola de administración**: permite a los administradores controlar el servidor de administración y el repositorio de imágenes.

-   **Cliente de usuario final**

    1.  Ciclo de vida de la imagen virtual: autenticación, recuperación de imágenes, aplicación de políticas de uso.

    2.  Administración de sesiones de máquina virtual: inicia, detiene, bloquea la máquina virtual.

    3.  Experiencia de escritorio sencilla: las aplicaciones instaladas en la máquina virtual se encuentran disponibles de forma transparente a través del menú Inicio de escritorio estándar y se integran con otras aplicaciones en el escritorio del usuario.

Toda la comunicación entre el cliente y los servidores (servidor de administración y repositorio de imágenes) se realiza en la parte superior de un canal HTTP o HTTPS estándar.

![](images/506f54d0-38fa-446a-8070-17ae26da5355.gif)

 

 





