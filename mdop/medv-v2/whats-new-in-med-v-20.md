---
title: Novedades de MED-V 2.0
description: Novedades de MED-V 2.0
author: dansimp
ms.assetid: 53b10bff-2b6f-463b-bdc2-5edc56526792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 78dba25fec7ae2bb41da00902b59dcd15030f2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823701"
---
# Novedades de MED-V 2.0


Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 ha evolucionado la compatibilidad de la compatibilidad de aplicaciones para Windows 7 y ha quitado la funcionalidad que no es necesaria para este escenario. Por ejemplo, se han quitado características como el cifrado del área de trabajo de MED-V, el servidor MED-V centralizado y la transferencia de recorte de área de trabajo de MED-V.

## Cambios en la funcionalidad estándar


En esta sección se describen las áreas clave donde ha cambiado la funcionalidad de MED-V 2,0.

### Creación de áreas de trabajo de MED-V

El disco duro virtual que se usa para el área de trabajo de MED-V ahora se crea en Windows Virtual PC. Entre los métodos que se usan para crear el área de trabajo MED-V se incluyen la instalación de Windows XP SP3, la actualización del sistema operativo y la preparación para su administración a través de la infraestructura de administración de software.

Se han eliminado las funciones de administración sin conexión y transferencia de recorte, además de la funcionalidad propietaria de cifrado y compresión del área de trabajo de MED-V. Al crear un área de trabajo de MED-V, un administrador debe preparar y configurar las aplicaciones y herramientas de administración apropiadas en la imagen en lugar de usar la herramienta de preparación de máquina virtual que se proporciona en MED-V 1,0.

Ahora es necesario ejecutar Sysprep en la imagen de MED-V y validarlo durante el empaquetado del área de trabajo de MED-V. El Empaquetador de área de trabajo MED-V proporciona una interfaz gráfica de usuario (GUI) que guía al administrador por el proceso de empaquetado. Se quitó la consola de MED-V 1,0 junto con la funcionalidad de administración de imágenes, la administración de perfiles del área de trabajo de MED-V y el requisito de ensayar y cifrar áreas de trabajo de MED-V.

### Implementación del área de trabajo MED-V

Para implementar un área de trabajo de MED-V, un administrador puede aprovechar sus herramientas electrónicas de distribución de software. El método de extracción de cliente disponible en MED-V 1,0 se quitó y el área de trabajo de MED-V se ha entregado usando métodos fuera de MED-V. Los administradores pueden tratar áreas de trabajo de MED-V como cualquier otro paquete de aplicación y pueden programar implementaciones e instalaciones de MED-V con sus procesos y herramientas existentes. Las instalaciones de MED-V se pueden implementar silenciosamente y se pueden administrar fácilmente dentro de una infraestructura de distribución de software existente.

### Administración de áreas de trabajo de MED-V

El área de trabajo de MED-V en MED-V 2,0 se basa en un disco duro virtual de Windows Virtual PC. MED-V ha ampliado las capacidades que proporciona Windows Virtual PC al mejorar la experiencia sin necesidad de cifrado o herramientas especiales para obtener acceso al área de trabajo de MED-V.

Después de implementar MED-V en una estación de trabajo, el área de trabajo de MED-V se puede abrir en el modo de pantalla completa con Windows Virtual PC. Esta nueva funcionalidad ha quitado el requisito de las directivas que establecieron una preferencia para los modos de pantalla completa o transparente y también ha eliminado la necesidad de forzar la pantalla completa para el diagnóstico y la solución de problemas.

Las aplicaciones de publicación para el área de trabajo de MED-V ya no se realizan con perfiles y al escribir manualmente la ruta de acceso a las aplicaciones. En su lugar, se produce de forma automática a medida que se instalan aplicaciones en el invitado. Se quita el repositorio de imágenes central que incluía las versiones de las imágenes que se entregaron a través de transferencia de recorte. En su lugar, MED-V permite a los administradores administrar el área de trabajo de MED-V como lo haría en un equipo físico, lo que permite que las aplicaciones y las actualizaciones se distribuyan sin la complejidad de una infraestructura de MED-V dedicada.

## Cambios en las características de MED-V


Varias áreas clave de MED-V 2,0 reflejan mejoras o adiciones a las siguientes características.

### Creación de áreas de trabajo de MED-V

Las áreas de trabajo de MED-V deben crearse con Windows Virtual PC. Es necesario migrar las imágenes existentes de Virtual PC 2007. La herramienta de preparación de la máquina virtual no está incluida en MED-V 2,0 y los administradores deben configurar, actualizar y optimizar sus imágenes según el archivo de ayuda de MED-V 2,0. La ejecución de Sysprep en la imagen de MED-V es un paso obligatorio y debe realizarse antes de empaquetar.

### Paquete de área de trabajo MED-V

Windows PowerShell es la base del paquete de área de trabajo MED-V. Esta funcionalidad reemplaza algunas de las funciones y funciones de la consola anteriores administradas por las funciones centralizadas de MED-V. El empaquetador del área de trabajo MED-V simplemente empaqueta el disco duro virtual con la configuración y la imagen apropiadas para que los administradores puedan implementarlos fácilmente. Las características avanzadas se proporcionan mediante Windows PowerShell.

### Distribución del área de trabajo MED-V

La infraestructura de servidor dedicada ya no es necesaria para MED-V 2,0 y el método de extracción de cliente para implementar áreas de trabajo de MED-V se ha eliminado. Las áreas de trabajo de MED-V ahora se implementan con su infraestructura electrónica de distribución de software y se pueden almacenar en recursos compartidos comunes que se usan para otros paquetes de instalación.

### Configuración de primera vez

El proceso de configuración por primera vez se integra ahora con la Convención de creación de imágenes estándar de Sysprep. El área de configuración del área de trabajo de MED-V Workspace puede aplicar dinámicamente la configuración especificada en el paquete de área de trabajo de MED-V a la imagen a medida que comienza la instalación mínima. Se ha quitado la herramienta de scripting en la consola y el primer proceso de configuración se basa ahora en las opciones que el administrador ha configurado en el paquete de área de trabajo MED-V.

### Publicación de aplicaciones

Los administradores pueden instalar aplicaciones en la imagen de MED-V, ya sea antes de empaquetarla, después de implementar el área de trabajo de MED-V o mediante una combinación de ambos. MED-V ya no examina la Directiva del área de trabajo de MED-V para publicar aplicaciones, sino que se refiere a lo que realmente se instala en el invitado. A medida que se instalan aplicaciones en el invitado, se detectan y se publican automáticamente en el menú de **Inicio** de host y están listas para ser iniciados por el usuario final.

### Redireccionamiento de URL

MED-V 2,0 ofrece redireccionamiento de direcciones web de host a invitado, basado en las directivas configuradas y administradas por el administrador. Después de redirigir una dirección URL al explorador invitado, la experiencia predeterminada es intentar limitar el usuario a ese sitio redirigido. Esto minimiza las actividades de navegación que un usuario puede realizar y que no están previsto por el administrador. Se quitó el redireccionamiento del explorador de invitado a host.

### Solución de problemas

MED-V ahora aprovecha los procesos estándar basados en host para la solución de problemas. Dado que el área de trabajo de MED-V ya no está cifrada, se puede abrir en el modo de pantalla completa dentro de la consola de Windows Virtual PC, donde se puede ver y trabajar como estación de trabajo estándar. Además, los registros ya no se cifran de forma local y se registran centralmente. MED-V ahora hace un uso extensivo de los registros de eventos locales, y el nivel de registro de la salida, desde información informativa a niveles de depuración, puede configurarse fácilmente. Por último, se proporciona un kit de herramientas de solución de problemas para que los administradores y el personal del Departamento de soporte puedan tener una vista gráfica y agregada de todas las opciones de solución de problemas, y pueden seleccionar sin esfuerzo las actividades que más se adapten a sus necesidades.

MED-V ya no se ejecuta como servicio del sistema. En su lugar, se ejecuta como procesos de propiedad del usuario y solo se ejecuta cuando un usuario ha iniciado sesión.La funcionalidad que anteriormente proporcionaba el servicio propiedad del sistema se proporciona ahora en los procesos de usuario.

## Temas relacionados


[Implementación de MED-V](deployment-of-med-v.md)

[Operaciones de MED-V](operations-for-med-v.md)

 

 





