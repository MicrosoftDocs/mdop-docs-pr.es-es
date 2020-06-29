---
title: Introducción a la implementación MED-V 2.0
description: Introducción a la implementación MED-V 2.0
author: dansimp
ms.assetid: 0b8998ea-c46f-4c81-a304-f380b2ed7cf8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ec2a5f86ac7d63295bd7c550bcb0a90004987e42
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826110"
---
# Introducción a la implementación MED-V 2.0


Esta sección proporciona información general e instrucciones sobre cómo instalar e implementar virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0.

## Introducción


MED-V 2,0 se basa en un modelo de aplicación, donde los mismos métodos que usa para implementar aplicaciones se pueden usar para implementar y administrar MED-V. Una solución de MED-V implementada incluye dos componentes: el agente de host MED-V y el agente invitado. El agente de host de MED-V está instalado en el escritorio de Windows 7 y el agente invitado de MED-V se instala en Windows XP dentro del área de trabajo de MED-V. MED-V también incluye un paquete de área de trabajo MED-V que proporciona la información y las herramientas necesarias para crear y configurar áreas de trabajo de MED-V.

**Importante**  
MED-V solo admite la instalación del Empaquetador de área de trabajo MED-V, el agente de host MED-V y el área de trabajo MED-V para todos los usuarios. Para instalar MED-V para el usuario actual solo seleccionando **AllUsers = ""** , se producen errores en la instalación de los componentes y en la configuración del área de trabajo MED-V.



### Los archivos de instalación de MED-V

MED-V incluye los siguientes archivos de instalación, necesarios para ejecutar MED-V:

**El archivo de instalación del agente de host MED-V**

El archivo de instalación del agente de host se denomina MED-V\_HostAgent\_Setup.exe. Este archivo se distribuye e instala en cada equipo de usuario final relevante como parte de la implementación en toda la empresa de MED-V.

**El archivo de instalación de empaquetador del área de trabajo de MED-V**

El archivo de instalación de empaquetador del área de trabajo de MED-V se denomina MED-V\_WorkspacePackager\_Setup.exe. Use este archivo para instalar el paquete de área de trabajo MED-V en un equipo en el que tiene permisos y derechos de administrador. El administrador de escritorio usa el Empaquetador de área de trabajo de MED-V para crear y administrar áreas de trabajo de MED-V.

**Nota**  
El agente invitado MED-V se instala automáticamente durante la configuración de primera vez.



### El proceso de implementación de MED-V

A continuación se encuentra una descripción general del proceso de instalación e implementación de MED-V:

1.  Instale el paquete de área de trabajo MED-V en el equipo en el que tenga las credenciales administrativas y que usará para compilar los paquetes del área de trabajo MED-V. Para obtener más información, vea [Cómo instalar el Empaquetador de área de trabajo de MED-V](how-to-install-the-med-v-workspace-packager.md).

2.  Prepare su imagen de MED-V y cree los paquetes del área de trabajo de MED-V con el Empaquetador de área de trabajo MED-V. Para obtener más información, consulte [operaciones para MED-V](operations-for-med-v.md).

3.  Implementar los componentes de MED-V necesarios en toda la empresa. Los componentes obligatorios de MED-V son Windows Virtual PC, el agente de host MED-V y el área de trabajo MED-V.

**Importante**  
La instalación de los componentes de MED-V requiere credenciales administrativas. Si un usuario final está instalando MED-V, se le pedirá que especifique las credenciales administrativas. Como alternativa, las credenciales administrativas se pueden proporcionar en contexto si se instala mediante un sistema de distribución electrónica de software (ESD).



### Componentes de MED-V

Los componentes de MED-V que implementa en toda su empresa se componen de lo siguiente:

**Windows Virtual PC**

Funciones MED-V dentro de imágenes de Windows Virtual PC para su solución de compatibilidad. Windows Virtual PC y la actualización para Windows 7 (KB977206) son obligatorias. Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).

**El archivo de instalación del agente de host MED-V**

MED-V\_HostAgent\_Setup.exe.

**Archivos de instalación del área de trabajo MED-V**

Los archivos de instalación del área de trabajo de MED-V se crean al crear el paquete del área de trabajo de MED-V que consta de lo siguiente:

Un programa ejecutable de setup.exe que ejecuta la instalación del área de trabajo MED-V

Un &lt; instalador de MED-V \ _workspace \ _name &gt; . msi

Un &lt; archivo VHD \ _filename &gt; . medv, que es el disco duro virtual comprimido

Los archivos de opciones de configuración ( &lt; área de trabajo \ _name &gt; . reg y &lt; Workspace \ _name &gt; . PS1)

Para implementar MED-V, copie todos los archivos de instalación necesarios en el equipo host o en un recurso compartido al que pueda acceder el equipo host. Ejecute los archivos de instalación del componente para Windows Virtual PC, el agente de host MED-V y el área de trabajo MED-V. Luego, inicia el agente de host MED-V para completar la primera configuración de MED-V.

Puede realizar la instalación de forma manual. Sin embargo, le recomendamos que use un método electrónico de distribución de software para automatizar la implementación de los componentes. Para obtener más información, consulte [cómo implementar un área de trabajo de MED-V a través de un sistema electrónico de distribución de software](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md).

**Nota**  
Para obtener información sobre los argumentos de la línea de comandos disponibles para controlar las opciones de instalación, consulte [Opciones de la línea de comandos para los archivos de instalación de MED-V](command-line-options-for-med-v-installation-files.md).



## Pasos de implementación


Al implementar MED-V en toda la empresa, hay dos consideraciones principales: instalación y primera configuración.

### Instalación

1.  **Windows Virtual PC** : durante la instalación, MED-V busca Windows Virtual PC y su actualización obligatoria para Windows 7 (KB977206). Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).

    Puede instalar estas como parte de las instalaciones de Windows 7 antes de instalar MED-V, o bien puede instalarlas como parte de la distribución de MED-V. Sin embargo, MED-V no incluye ningún mecanismo para su implementación; se deben implementar mediante un sistema de distribución de software electrónico (ESD) o como parte de la imagen de Windows 7.

    **Importante**  
    Al instalar los componentes de MED-V mediante un archivo por lotes, se recomienda especificar que Windows Virtual PC y la revisión de Windows Virtual PC se instalen después del agente de host MED-V y los archivos de paquete del área de trabajo MED-V. Esto significa que Windows Update no causará ninguna interferencia con el proceso de instalación al requerir un reinicio.



~~~
**Note**  
After you install Windows Virtual PC, the computer must be restarted.
~~~



2. **Agente de host Med-v** : instala el agente de host Med-v en el equipo con Windows 7 donde se ejecutará Med-v. Debe instalarse antes de instalar el área de trabajo de MED-V y comprobar que Windows Virtual PC está instalado.

3. **Área de trabajo de Med-v** : para crear los archivos necesarios en esta instalación, use el Empaquetador de área de trabajo Med-v: los archivos setup.exe,. medv y. msi. Para instalar el área de trabajo de MED-V, ejecute setup.exe; Esto desencadena los otros archivos según sea necesario. La instalación coloca una entrada en el registro debajo de la clave de ejecución de la máquina local para iniciar el agente de host MED-V, que siempre ejecuta MED-V cuando se inicia Windows.

   **Importante**  
   La instalación del área de trabajo de MED-V puede ser ejecutada de forma interactiva por el usuario final o silenciosamente a través de un sistema electrónico de distribución de software. La instalación del área de trabajo de MED-V requiere credenciales administrativas, por lo que los usuarios finales deben ser administradores de sus equipos para instalar el área de trabajo de MED-V. Como alternativa, un sistema electrónico de distribución de software normalmente se ejecuta en el contexto del sistema y tiene los permisos necesarios.



~~~
**Tip**  
Because of problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



### Configuración de primera vez

Después de instalar MED-V y los componentes necesarios, debe configurarse MED-V. La configuración de MED-V se conoce como configuración de primera vez. Al usar el **Empaquetador de área de trabajo de MED-V**, puede configurar la configuración de primera hora para que se ejecute en modo silencioso o de forma interactiva. La primera configuración de MED-V requiere que los usuarios finales escriban su contraseña para autenticar en el área de trabajo de MED-V, pero en caso contrario puede ser casi invisible para el usuario. Las notificaciones se muestran en el área de notificación, como cuando se completa la configuración por primera vez y las aplicaciones están listas. A continuación se indican las acciones que se producen durante la configuración de MED-V por primera vez:

1.  El disco duro virtual debe estar configurado. La instalación mínima se ejecuta y expande la imagen de Windows XP. Normalmente, esto se produce en una ventana oculta, pero MED-V se puede configurar para que se muestre durante esta configuración.

2.  Después de que finalice la instalación mínima, puede ejecutar los comandos que necesita para la configuración adicional, como instalar el software ESD u otras aplicaciones, o configurar la imagen. Puede llamarlos en el archivo Sysprep. inf, pero no son necesarios. Para obtener más información, vea [configuración de una imagen de Windows Virtual PC para MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).

3.  Ftscompletion.exe se ejecuta como el último paso de la configuración. Este proceso completa la configuración de MED-V, agrega el usuario al grupo RDP para permitir que tengan acceso al área de trabajo de MED-V, copia los registros, indica MED-V que el área de trabajo de MED-V está listo y después reinicia el área de trabajo de MED-V. Este proceso también puede Agregar al usuario como administrador del área de trabajo de MED-V si se configuró cuando se creó el área de trabajo de MED-V. Normalmente, Ftscompletion.exe se llama a través del archivo Sysprep, INF, pero también puede ejecutarse a través de otro método, como un script. Sin embargo, Ftscompletion.exe debe ser la última acción que se realice cuando la estación de trabajo esté configurada. Para obtener más información, vea [configuración de una imagen de Windows Virtual PC para MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md).

4.  Una vez reiniciado el área de trabajo de MED-V Ftscompletion.exe, el usuario final inicia sesión. Si no guardaban su contraseña durante la configuración de la primera vez, se le pedirá. El área de trabajo de MED-V se inicia y se configura para el usuario. La configuración incluye la aplicación de directiva de grupo.

    Le recomendamos que aplique solo las directivas que tengan sentido en un entorno de compatibilidad de aplicaciones para Windows XP. Por ejemplo, normalmente no es necesario aplicar las directivas de personalización de escritorio y deben deshabilitarse. Para obtener más información sobre cómo permitir solo perfiles locales, consulte [configuración de directiva de grupo para perfiles de usuarios móviles](https://go.microsoft.com/fwlink/?LinkId=205072) ( https://go.microsoft.com/fwlink/?LinkId=205072) .

Una vez completada la configuración, se notifica al usuario final que las aplicaciones publicadas están listas. Después, pueden acceder a las aplicaciones instaladas en el área de trabajo de MED-V desde el menú **Inicio** .

## Temas relacionados


[Preparar el entorno de implementación para MED-V](prepare-the-deployment-environment-for-med-v.md)

[Implementación de MED-V](deployment-of-med-v.md)









