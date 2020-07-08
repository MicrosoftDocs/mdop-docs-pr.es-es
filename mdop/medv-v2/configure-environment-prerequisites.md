---
title: Configurar los requisitos previos de entorno
description: Configurar los requisitos previos de entorno
author: dansimp
ms.assetid: 7379e8e5-1cb2-4b8e-8acc-5c04e26f8c91
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8d6fc3b81f6dafbe709dd904b9fba6124d2f6b6a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826450"
---
# Configurar los requisitos previos de entorno


Antes de que pueda implementar y ejecutar Microsoft Enterprise Desktop Virtualization (MED-V) 2,0, debe asegurarse de que su entorno cumple los siguientes requisitos mínimos.

**Windows 7**

El agente de hospedaje de MED-V y el Empaquetador de área de trabajo MED-V solo se admiten en Windows 7 o posterior.

**Windows XP SP3**

El agente invitado MED-V solo se admite en Windows XP SP3.

**.NET Framework 3,5 SP1**

Los agentes de host y de hospedaje MED-V y el Empaquetador de área de trabajo MED-V requieren Microsoft .NET Framework 3,5 SP1.

**Importante**  También debe instalar la actualización [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) , que resuelve varios problemas de compatibilidad de aplicaciones conocidos.

 

**Nota:**  Debe instalar manualmente .NET Framework 3,5 SP1 y la actualización KB959209 en la imagen de Windows Virtual PC que preparará para usar con MED-V. Sin embargo, de forma predeterminada, Microsoft .NET Framework 3,5 SP1 y la actualización se incluyen al instalar Windows 7 en el equipo host.

 

**Una infraestructura de Active Directory**

La Directiva de grupo proporciona la administración centralizada y la configuración de los sistemas operativos, las aplicaciones y la configuración de los usuarios en un entorno de Active Directory.

## Temas relacionados


[Configurar los requisitos previos de instalación](configure-installation-prerequisites.md)

[Arquitectura de alto nivel](high-level-architecturemedv2.md)

[Configuraciones admitidas de MED-V 2.0](med-v-20-supported-configurations.md)

 

 





