---
title: Solución de problemas de implementación
description: Solución de problemas de implementación
author: dansimp
ms.assetid: 9ee980f2-4e77-4020-9f0e-8c2ffdc390ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe9677175c9538bc070d2adea17a96351397d9a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822900"
---
# Solución de problemas de implementación


Este tema incluye información para ayudarle a solucionar problemas de implementación en Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Solución de problemas en la implementación de MED-V


El siguiente problema puede ocurrir al implementar MED-V. La solución ayuda a solucionar este problema.

**Se producen problemas Si instala MED-V solo para usuarios actuales.** MED-V solo admite la instalación del Empaquetador de área de trabajo MED-V, el agente de host MED-V y el área de trabajo MED-V para todos los usuarios. La instalación del usuario actual solo provoca errores en la instalación de los componentes y en la configuración del área de trabajo MED-V.

**Solución**

Nunca use la opción **AllUsers = ""** al instalar los componentes de MED-V.

**MED-V requiere el uso exclusivo de la pila de virtualización.** Solo se puede ejecutar una pila de virtualización a la vez en un equipo. Windows Virtual PC debe usar la pila virtual y MED-V depende de Windows Virtual PC. Por lo tanto, si intenta implementar o usar MED-V cuando se ejecutan otras aplicaciones que usan la pila virtual, MED-V no se puede ejecutar o se puede instalar correctamente.

**Solución**

Cierre todas las aplicaciones que se estén ejecutando que usen la pila de virtualización antes de instalar o ejecutar MED-V.

**Los accesos directos permanecen después de la desinstalación.** De forma predeterminada, al desinstalar MED-V, se quitan los accesos directos del menú **Inicio** del usuario final. Sin embargo, en determinadas situaciones, como para los usuarios finales que ejecutan perfiles móviles, los accesos directos a las aplicaciones publicadas de MED-V se conservan en el menú **Inicio** del usuario final.

**Solución**

Para eliminar manualmente los métodos abreviados del menú **Inicio** , haga clic con el botón secundario en los métodos abreviados y, a continuación, haga clic en **quitar**.

**Deshabilite la configuración de directiva de grupo de mensajes de inicio de sesión en el área de trabajo MED-V.** Si el mensaje de inicio de sesión de Windows XP está habilitado en el área de trabajo de MED-V, el usuario final debe iniciar sesión cada vez que quiera abrir una aplicación virtual de MED-V. Esto crea una experiencia de usuario deficiente.

**Solución**

Deshabilite la siguiente configuración de directiva de grupo en la máquina virtual de MED-V:

**Inicio de sesión interactivo: texto del mensaje para los usuarios que intentan iniciar sesión**

**Inicio de sesión interactivo: título del mensaje para los usuarios que intentan iniciar una sesión**

## Temas relacionados


[Solución de problemas de operaciones](operations-troubleshooting-medv2.md)

 

 





