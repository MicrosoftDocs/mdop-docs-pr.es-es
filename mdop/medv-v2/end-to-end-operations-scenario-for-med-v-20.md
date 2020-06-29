---
title: Escenario de operaciones de principio a fin de MED-V 2.0
description: Escenario de operaciones de principio a fin de MED-V 2.0
author: dansimp
ms.assetid: 1d87f5f3-9fc5-4731-8bd1-c155714f34ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90a7c2135ad27040ed87dac980b67321eb771574
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826170"
---
# Escenario de operaciones de principio a fin de MED-V 2.0


Este escenario de ejemplo de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 le ayuda a implementar y administrar MED-V mediante el uso de varios escenarios de principio a fin. Puede considerar este escenario de ejemplo como un caso práctico que ayuda a poner escenarios y procedimientos individuales en el contexto.

Esta sección proporciona información básica e instrucciones para crear, implementar y administrar áreas de trabajo de MED-V como una solución completa en su empresa.

## Escenario paso a paso de operaciones de MED-V


Los procedimientos paso a paso que se siguen en un escenario de operaciones de MED-V son los siguientes:

-   [Creación de una imagen de Windows Virtual PC para Med-v](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc) revisa cómo crear y configurar una imagen de Windows Virtual PC para Med-v. Antes de poder enviar un área de trabajo de MED-V a los usuarios, primero debe preparar un disco duro virtual (VHD) que use para crear el paquete del instalador de área de trabajo MED-V para MED-V.

-   [Creación de una imagen de Windows Virtual PC para MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installingwindowsxpontovpc) revisa cómo instalar el sistema operativo Windows XP SP3 en la imagen de Windows Virtual PC. MED-V requiere que Windows XP SP3 esté instalado en la imagen de Windows Virtual PC antes de crear el área de trabajo de MED-V.

-   [Creación de una imagen de Windows Virtual PC para MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installingnet) revisa cómo instalar manualmente .net Framework 3,5 SP1 y la actualización KB959209 en la imagen de Windows Virtual PC que preparas para usar con MED-V. MED-V requiere .NET Framework 3,5 SP1 y la actualización [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (se https://go.microsoft.com/fwlink/?LinkId=204950) ocupa de varios problemas de compatibilidad de aplicaciones conocidos.

-   [Creación de una imagen de Windows Virtual PC para MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-applypatchestovpc) revisa cómo actualizar su imagen de Windows XP con las últimas actualizaciones de software y otras revisiones necesarias o importantes para ejecutar MED-V.

-   [Creación de una imagen de Windows Virtual PC para MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installintegration) revisa cómo instalar el paquete de componentes de integración en la imagen de Windows XP. Estas proporcionan características que mejoran la interacción entre el entorno virtual y el equipo físico.

-   [Instalar aplicaciones en una imagen de Windows Virtual PC](installing-applications-on-a-windows-virtual-pc-image.md) revisa cómo puede instalar ciertos tipos de software en la imagen de Windows XP que son útiles cuando se ejecuta MED-V, como un sistema de distribución de software electrónico y software antivirus.

-   [Configuración de una imagen de Windows Virtual PC para MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md) describe cómo configurar la imagen mediante Sysprep para asegurarse de que está lista para su uso con MED-V. La imagen de MED-V preparada se usa para crear el paquete del área de trabajo de MED-V.

-   [Crear un paquete de área de trabajo Med-v](create-a-med-v-workspace-package.md) revisa cómo crear el paquete de área de trabajo Med-v que se implementa en toda la empresa. Implemente el paquete de área de trabajo MED-V para instalar el área de trabajo MED-V en equipos de usuario final. Un área de trabajo de MED-V es el entorno de escritorio de Windows XP desde el que los usuarios finales interactúan con la máquina virtual proporcionada por MED-V.

-   [Probar el paquete de área de trabajo Med-v](testing-the-med-v-workspace-package.md) describe cómo crear un entorno de prueba en el que pueda probar la funcionalidad del paquete de área de trabajo Med-v, como la configuración de configuración y la publicación de aplicaciones por primera vez. Una vez que haya completado la prueba de su paquete de área de trabajo MED-V y haya comprobado que funciona según lo previsto, puede implementarlo en toda la empresa.

-   [Implementar el paquete de área de trabajo Med-v](deploying-the-med-v-workspace-package.md) describe cómo implementar el área de trabajo de Med-v mediante un sistema de distribución de software electrónico o en una imagen de Windows 7. O, si lo prefiere, en esta sección también se muestra cómo puede implementar el área de trabajo de MED-V manualmente.

-   [Supervisar áreas de trabajo de Med-v](monitor-med-v-workspaces.md) revisa cómo supervisar la implementación de áreas de trabajo de Med-v para determinar si la configuración de la primera vez se completó correctamente. Es importante supervisar el éxito de la configuración correcta porque MED-V no se encuentra en un estado utilizable hasta que la configuración de la primera vez se haya completado correctamente. En esta sección también se muestra cómo puede configurar su entorno para detectar los cambios de red que pueden afectar a MED-V.

-   [Administrar las aplicaciones de área de trabajo de MED-V](manage-med-v-workspace-applications.md) revisa cómo instalar y quitar o publicar y anular la publicación de aplicaciones en un área de trabajo de MED-V implementada. En esta sección también se muestra cómo actualizar manualmente el software en un área de trabajo de MED-V y cómo administrar las actualizaciones automáticas. El área de trabajo de MED-V es una máquina virtual que contiene un sistema operativo independiente cuyo proceso de actualización automática de software debe administrarse exactamente igual que los equipos físicos de su empresa.

-   Administración de la dirección [URL de MED-V](manage-med-v-url-redirection.md) revisa cómo agregar y quitar la configuración de la redirección de direcciones web en el área de trabajo de Med-v implementada. Puede Agregar o quitar información de redireccionamiento de la dirección URL a través del registro o reconstruyendo el área de trabajo de MED-V. También puede usar el asistente en el Empaquetador de área de trabajo MED-V para administrar el redireccionamiento de direcciones web.

-   [Administrar la configuración del área de trabajo de Med-v](manage-med-v-workspace-settings.md) revisa cómo ver y editar las opciones de configuración de Med-v con el Empaquetador de área de trabajo Med-v. En esta sección se enumeran todas las claves del registro MED-V configurables y se incluyen el tipo, predeterminado y la descripción de cada una. Esta sección también incluye información sobre cómo administrar las impresoras en áreas de trabajo de MED-V. En MED-V 2,0, el redireccionamiento de impresoras proporciona a los usuarios una experiencia de impresión coherente entre la máquina virtual de MED-V y el equipo host.

## Temas relacionados


[Operaciones de MED-V](operations-for-med-v.md)

[Escenario de planificación de principio a fin de MED-V 2.0](end-to-end-planning-scenario-for-med-v-20.md)

[Escenario de implementación de principio a fin de MED-V 2.0](end-to-end-deployment-scenario-for-med-v-20.md)

 

 





