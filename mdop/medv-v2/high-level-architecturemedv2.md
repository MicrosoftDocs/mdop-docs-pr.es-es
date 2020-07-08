---
title: Arquitectura de alto nivel
description: Arquitectura de alto nivel
author: dansimp
ms.assetid: a00edb9f-207b-4f32-9e8f-522ea2739d2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a5db4a56b2abfb0df19b0d6d86f4bf88380c2bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827291"
---
# Arquitectura de alto nivel


Esta sección describe la arquitectura del sistema de alto nivel y el diseño de componentes de virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0.

## Arquitectura del sistema


MED-V mejora el equipo virtual de Windows para que ejecute dos sistemas operativos en un dispositivo, lo que agrega una entrega de imagen virtual, aprovisionamiento basado en directivas de grupo y administración centralizada. Con MED-V, puede configurar, implementar y administrar fácilmente las imágenes corporativas de Virtual PC en cualquier escritorio basado en Windows que ejecute Windows 7 Professional, Enterprise o Windows 7 Ultimate. La solución MED-V incluye los siguientes componentes:

<a href="" id="---------------med-v-host"></a> **Host MED-V**  
Entorno de Windows 7 que incluye un agente de host MED-V, un sistema de distribución electrónica de software (ESD), un sistema de administración de registro y un invitado MED-V. El host MED-V interactúa con el invitado MED-V para que se puedan procesar determinadas funciones de configuración e información del sistema.

<a href="" id="-------------------med-v-host-agent"></a> **Agente de host MED-V**  
El software MED-V contenido en el host MED-V que proporciona un canal para comunicarse con el invitado MED-V. También proporciona funciones como la configuración de primera vez y la publicación de aplicaciones.

**Nota:**  Después de instalar MED-V y sus componentes necesarios, se debe configurar MED-V. La configuración de MED-V se conoce como configuración de primera vez.

 

<a href="" id="esd-system"></a>**Sistema ESD**  
El método de distribución de software existente que le permite implementar e instalar los archivos de paquete del área de trabajo de MED-V que crea MED-V.

<a href="" id="registry-management-system"></a>**Sistema de administración del registro**  
El método existente de administrar la configuración y las preferencias de la Directiva de grupo.

<a href="" id="windows-virtual-pc-image"></a>**Imagen de Windows Virtual PC**  
Una máquina virtual definida por el administrador que contiene los siguientes componentes:

<a href="" id="corporate-operating-system"></a>**Sistema operativo de la empresa**  
Su sistema operativo empresarial estándar.

<a href="" id="management-and-security-tools"></a>**Herramientas de administración y seguridad**  
Sus herramientas de seguridad y administración estándar, como la protección antivirus.

<a href="" id="-----------------------med-v-guest"></a> **Invitado MED-V**  
Un entorno de Windows XP SP3, como parte de un equipo virtual de Windows que se ejecuta en Windows 7 y que contiene los siguientes componentes:

<a href="" id="---------------------------med-v-guest-agent"></a> **Agente invitado MED-V**  
El software MED-V contenido en el invitado MED-V que proporciona un canal para comunicarse con el host MED-V. También admite el agente de host MED-V con funciones como realizar la configuración por primera vez.

**Nota:**  El agente invitado MED-V se instala automáticamente durante la configuración de primera vez.

 

<a href="" id="esd-client"></a>**Cliente ESD**  
Una parte opcional de su sistema ESD que instala paquetes de software e informa del estado al sistema ESD.

## Temas relacionados


[Planificación de compatibilidad de aplicaciones del sistema operativo](planning-for-application-operating-system-compatibility.md)

[Preparar el entorno de implementación para MED-V](prepare-the-deployment-environment-for-med-v.md)

 

 





