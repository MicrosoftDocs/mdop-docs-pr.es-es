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
# <span data-ttu-id="07be8-103">Arquitectura de alto nivel</span><span class="sxs-lookup"><span data-stu-id="07be8-103">High-Level Architecture</span></span>


<span data-ttu-id="07be8-104">La solución MED-V consta de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="07be8-104">The MED-V solution comprises the following elements:</span></span>

-   <span data-ttu-id="07be8-105">**Máquina virtual definida por el administrador**: encapsula un entorno de escritorio completo, incluido un sistema operativo, aplicaciones y herramientas de seguridad y administración opcionales.</span><span class="sxs-lookup"><span data-stu-id="07be8-105">**Administrator-defined virtual machine**—Encapsulates a full desktop environment, including an operating system, applications, and optional management and security tools.</span></span>

-   <span data-ttu-id="07be8-106">**Repositorio de imágenes**: almacena todas las imágenes virtuales en un servidor IIS estándar y habilita la administración de versiones de imágenes virtuales, la recuperación de imágenes autenticadas por el cliente y la descarga eficaz (de una nueva imagen o actualizaciones) a través de la tecnología de transferencia de recorte.</span><span class="sxs-lookup"><span data-stu-id="07be8-106">**Image repository**—Stores all virtual images on a standard IIS server and enables virtual images version management, client-authenticated image retrieval, and efficient download (of a new image or updates) via Trim Transfer technology.</span></span>

-   <span data-ttu-id="07be8-107">**Servidor de administración**: asocia imágenes virtuales del repositorio de imágenes junto con directivas de uso del administrador a usuarios o grupos de Active Directory®.</span><span class="sxs-lookup"><span data-stu-id="07be8-107">**Management server**—Associates virtual images from the image repository along with administrator usage policies to Active Directory® users or groups.</span></span> <span data-ttu-id="07be8-108">El servidor de administración también agrega eventos de clientes y los almacena en una base de datos externa (Microsoft SQL Server®) para fines de supervisión e informes.</span><span class="sxs-lookup"><span data-stu-id="07be8-108">The management server also aggregates clients' events and stores them in an external database (Microsoft SQL Server®) for monitoring and reporting purposes.</span></span>

-   <span data-ttu-id="07be8-109">**Consola de administración**: permite a los administradores controlar el servidor de administración y el repositorio de imágenes.</span><span class="sxs-lookup"><span data-stu-id="07be8-109">**Management console**—Enables administrators to control the management server and the image repository.</span></span>

-   **<span data-ttu-id="07be8-110">Cliente de usuario final</span><span class="sxs-lookup"><span data-stu-id="07be8-110">End-user client</span></span>**

    1.  <span data-ttu-id="07be8-111">Ciclo de vida de la imagen virtual: autenticación, recuperación de imágenes, aplicación de políticas de uso.</span><span class="sxs-lookup"><span data-stu-id="07be8-111">Virtual image life-cycle—Authentication, image retrieval, enforcement of usage policies.</span></span>

    2.  <span data-ttu-id="07be8-112">Administración de sesiones de máquina virtual: inicia, detiene, bloquea la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="07be8-112">Virtual machine session management—Start, stop, lock the virtual machine.</span></span>

    3.  <span data-ttu-id="07be8-113">Experiencia de escritorio sencilla: las aplicaciones instaladas en la máquina virtual se encuentran disponibles de forma transparente a través del menú Inicio de escritorio estándar y se integran con otras aplicaciones en el escritorio del usuario.</span><span class="sxs-lookup"><span data-stu-id="07be8-113">Single desktop experience—Applications installed in the virtual machine seamlessly available through the standard desktop Start menu and integrated with other applications on the user desktop.</span></span>

<span data-ttu-id="07be8-114">Toda la comunicación entre el cliente y los servidores (servidor de administración y repositorio de imágenes) se realiza en la parte superior de un canal HTTP o HTTPS estándar.</span><span class="sxs-lookup"><span data-stu-id="07be8-114">All communication between the client and the servers (management server and image repository) is carried on top of a standard HTTP or HTTPS channel.</span></span>

![](images/506f54d0-38fa-446a-8070-17ae26da5355.gif)

 

 





