---
title: Planificación de compatibilidad de aplicaciones del sistema operativo
description: Planificación de compatibilidad de aplicaciones del sistema operativo
author: dansimp
ms.assetid: cdb0a7f0-9da4-4562-8277-12972eb0fea8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5b10da2c870e5ddc32098136225515cdd0523809
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825470"
---
# Planificación de compatibilidad de aplicaciones del sistema operativo


Este tema ayuda a determinar cómo resolver problemas de compatibilidad con el sistema operativo de la aplicación y explica cómo Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 funciona como una solución para su organización.

En este tema se describen los requisitos empresariales para MED-V y se compara MED-V con el modo Windows XP y Microsoft Application Virtualization (App-V):

-   [Requisitos empresariales para MED-V](#bkmk-whenmedv)

-   [Ventajas del modo MED-V frente a Windows XP](#bkmk-medvvsxp)

-   [Beneficios de MED-V frente a App-V](#bkmk-medvvsappv)

## <a href="" id="bkmk-whenmedv"></a>Requisitos empresariales para MED-V


Cuando el Departamento de TI de su empresa está determinando si quiere actualizar a Windows 7, debe prestar atención a las aplicaciones de línea de negocio y a las aplicaciones de línea de negocio basadas en web para asegurarse de que se pueden ejecutar en el nuevo sistema operativo. A menudo, estas aplicaciones y direcciones URL se crearon para trabajar específicamente con una versión anterior de Windows o Internet Explorer, y pueden surgir problemas al intentar usarlos en el nuevo sistema operativo. Microsoft ofrece muchos métodos diferentes para administrar los diversos problemas de compatibilidad que se pueden producir al actualizar, como el kit de herramientas de compatibilidad de aplicaciones (ACT) y el Asistente para la compatibilidad de programas de Windows 7. Pero incluso después de que se hayan probado la compatibilidad y las correcciones de todas las aplicaciones, algunas aplicaciones siguen sin funcionar correctamente en Windows 7 o son demasiado costosas de resolver.

Con MED-V, puede ejecutar estas aplicaciones heredadas a través de un entorno de Windows Virtual PC que ejecuta Windows XP. Dado que ya no tiene que probar y validar estas aplicaciones problemáticas en el nuevo sistema operativo antes de la actualización, la migración a Windows 7 es mucho más suave y rápida.

### Lista de comprobación de MED-V

Considere MED-V si alguno de los escenarios siguientes se aplica a su caso:

-   Usted es una gran organización (por ejemplo, 500 usuarios y más), un contrato empresarial con Microsoft y un plan para actualizar a Windows 7.

-   Ha probado las aplicaciones de línea de negocio y ha encontrado algunos que no son compatibles con Windows 7.

-   Ha resuelto los problemas de compatibilidad de algunas de estas aplicaciones con problemas actualizando la aplicación o mediante una corrección proporcionada por Microsoft, como el kit de herramientas de compatibilidad de aplicaciones (ACT), pero quedan problemas de compatibilidad para algunas aplicaciones.

-   Ha considerado que App-V es una opción para ofrecer las aplicaciones incompatibles y ha concluido que incluso después de implementar App-V, sigue teniendo problemas de compatibilidad de sistema operativo de la aplicación que debe abordar.

-   Se ha considerado el modo de Windows XP como una solución y se ha determinado que no es una opción eficaz porque:

    -   Quiere poder implementar imágenes virtuales que contengan las aplicaciones problemáticas para todos los usuarios finales al mismo tiempo, en lugar de individualmente, y hacer que las imágenes virtuales se unan automáticamente al dominio.

    -   Ha decidido que es mucho más rentable administrar estas aplicaciones heredadas (que se entregan virtualmente) y controlar la configuración de Windows Virtual PC desde una ubicación centralizada en lugar de hacerlo en el escritorio de cada usuario final.

    -   Quiere poder actualizar y dar soporte a las máquinas virtuales en escala en lugar de por equipo de escritorio.

    -   Quiere poder redirigir las direcciones URL que se ejecutan mejor en una versión anterior de Internet Explorer a las máquinas virtuales y administrar fácilmente el redireccionamiento de direcciones URL más adelante.

-   Ha determinado que sería más económico y útil actualizar a Windows 7 lo antes posible y ha decidido posponer la resolución de los problemas de compatibilidad de aplicaciones restantes hasta una fecha posterior, sabiendo que tiene una solución disponible en MED-V.

## <a href="" id="bkmk-medvvsxp"></a> Ventajas del modo MED-V frente a Windows XP


Windows Virtual PC para Windows 7 le permite ejecutar diferentes versiones de un sistema operativo al mismo tiempo en un solo dispositivo y se incluye en Windows 7 Professional Edition y versiones posteriores.

La funcionalidad del modo Windows XP aprovecha Windows Virtual PC al proporcionar una imagen de Windows XP preconfigurada que le permite crear un entorno virtual de Windows XP. En este entorno virtual, puede instalar manualmente aplicaciones que no son compatibles con Windows 7 y que se ejecutan sin problemas desde su escritorio a través de Virtual PC de Windows.

**Con el modo Windows XP, puede hacer lo siguiente:**

-   Ejecute aplicaciones que sean compatibles con Windows XP dentro de una máquina virtual que se ejecute en Windows Virtual PC.

-   Publique estas aplicaciones en el menú de escritorio o de programa del anfitrión.

Cuando desee entregar estas máquinas virtuales a gran escala como parte de una migración empresarial a Windows 7, debe poder implementar rápidamente las máquinas virtuales, aprovisionarlas y personalizarlas eficazmente, controlar su configuración y respaldarlas fácilmente.

MED-V se basa en el modo de Windows XP para proporcionar compatibilidad de aplicaciones en toda la empresa. Mientras que el modo de Windows XP está limitado a proporcionar funcionalidad de aplicación virtual a personas y pequeñas empresas, MED-V permite implementaciones a gran escala de imágenes preconfiguradas de Windows XP en toda la red corporativa. Le ofrece una solución de administración lista para empresas para la configuración, la implementación y el mantenimiento de estas áreas de trabajo virtuales de MED-V. MED-V también ofrece enterpriseadministrators un conjunto de directivas para controlar el uso de la imagen. Esto incluye qué usuarios tendrán acceso a qué aplicaciones específicas dentro de estas imágenes.

**Con MED-V, puede hacer lo siguiente:**

-   Actualice a su nuevo sistema operativo sin tener que probar y resolver todas las aplicaciones y direcciones URL incompatibles.

-   Implementar imágenes virtuales de Windows XP que se unen automáticamente y se personalizan por usuario.

-   Aprovisionar aplicaciones e información de redireccionamiento de URL a los usuarios.

-   Controlar la configuración de Windows Virtual PC.

-   Mantenga y soporte técnico de puntos de conexión a través de la supervisión y la solución de problemas.

-   Asegurarse de que se revisan los equipos invitados, incluso si se encuentran en estado suspendido.

-   Automatizar la creación de máquina virtual por usuario y la inicialización de Sysprep.

-   Diagnosticar fácilmente problemas en los equipos de host e invitado.

-   Administre sin problemas los equipos invitados que se conectan a través del modo NAT de Virtual PC de Windows.

## <a href="" id="bkmk-medvvsappv"></a>Beneficios de MED-V frente a App-V


MED-V y App-V son dos tecnologías muy diferentes que pueden colaborar fácilmente para resolver problemas de compatibilidad con el sistema operativo de la aplicación. Al usar App-V, se crea un paquete individualizado para cada aplicación, cada uno de los cuales se mantiene separado de los demás. Cada aplicación virtual se puede entregar inmediatamente al usuario final, que es muy útil para una estrategia de implementación de Windows 7.

MED-V no controla las aplicaciones individualmente. En su lugar, crea una instancia adicional de Windows XP en el mismo escritorio que ejecuta Windows 7. Puede instalar tantas aplicaciones como sea necesario en esta imagen virtual y administrar la imagen como lo haría con cualquier otro escritorio de su organización.

Además, puede usar MED-V junto con App-V para que las aplicaciones virtuales que se ordenen a través de App-V se instalen, publiquen y administren con MED-V.

## Temas relacionados


[Definir y planificar la implementación de MED-V](define-and-plan-your-med-v-deployment.md)

 

 





