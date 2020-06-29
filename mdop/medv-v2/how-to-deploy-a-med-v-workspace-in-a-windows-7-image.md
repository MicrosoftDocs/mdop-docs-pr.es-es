---
title: Cómo implementar un área de trabajo de MED-V en una imagen de Windows 7
description: Cómo implementar un área de trabajo de MED-V en una imagen de Windows 7
author: dansimp
ms.assetid: a83aba4e-8681-4906-9872-f431c0bb15f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 49dd796d6f6af425b9000b595a0d828c3cb0035a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827281"
---
# Cómo implementar un área de trabajo de MED-V en una imagen de Windows 7


Puede instalar todos los componentes de MED-V en una imagen de Windows 7 que distribuya por toda la empresa, como lo haría en cualquier nueva instalación de Windows 7. Después, el usuario final finaliza la instalación del área de trabajo MED-V haciendo clic en el acceso directo del menú **Inicio** que configuró para iniciar Med-v. La configuración comienza por la primera vez que el usuario final sigue las instrucciones para completar la configuración.

La siguiente sección proporciona información e instrucciones para ayudarle a implementar el área de trabajo de MED-V en toda su empresa con una imagen de Windows 7.

**Para implementar un área de trabajo de MED-V en una imagen de Windows 7**

1.  Crear una imagen estándar de Windows 7. Para obtener más información, consulte [creación de una imagen estándar de Windows 7: guía paso a paso](https://go.microsoft.com/fwlink/?LinkId=204843) ( https://go.microsoft.com/fwlink/?LinkId=204843) .

2.  En la imagen de Windows 7, instale Windows Virtual PC y las actualizaciones de Windows Virtual PC. Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).

3.  Instale el agente de host MED-V usando el archivo de instalación MED-V \ _HostAgent \ _Setup. Para obtener más información, vea [Cómo instalar manualmente el agente de host MED-V](how-to-manually-install-the-med-v-host-agent.md).

    **ADVERTENCIA**  Internet Explorer debe cerrarse antes de instalar el agente de host MED-V; de lo contrario, los conflictos pueden producirse posteriormente con el redireccionamiento de URL. También puede hacerlo especificando un reinicio del equipo durante una distribución.

     

4.  Copie los archivos de paquete del área de trabajo de MED-V en la imagen de Windows 7. Los archivos de paquete del área de trabajo de MED-V son el instalador del área de trabajo de MED-V, el archivo. medv y el archivo setup.exe que ha creado con el **Empaquetador de área de trabajo de Med-v**.

    **Importante**  El archivo. medv y setup.exe debe estar en la misma carpeta que el instalador del área de trabajo de MED-V. A continuación, instale el área de trabajo de MED-V ejecutando setup.exe.

     

5.  Configure un acceso directo en el menú **Inicio** para abrir la instalación del paquete de área de trabajo de MED-V.

    Cree un acceso directo al menú **Inicio** para el setup.exe archivo que permita al usuario final iniciar una instalación de MED-V según sea necesario.

6.  Con el proceso de implementación de imágenes estándar de su empresa, distribuya la imagen de Windows 7 a los equipos de su empresa que necesiten MED-V.

Cuando el usuario final tiene que acceder a una aplicación publicada en el área de trabajo de MED-V, puede hacer clic en el acceso directo del menú **Inicio** para instalar el área de trabajo de Med-v. Esto se inicia automáticamente la primera configuración y completa la configuración de MED-V. Una vez completada la configuración, el usuario final puede acceder a las aplicaciones de MED-V en el menú **Inicio** .

## Temas relacionados


[Introducción a la implementación MED-V 2.0](med-v-20-deployment-overview.md)

[Cómo implementar un área de trabajo de MED-V a través de un sistema de distribución electrónica de Software](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

 

 





