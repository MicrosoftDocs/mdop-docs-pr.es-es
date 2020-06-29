---
title: Cómo configurar un paquete de implementación
description: Cómo configurar un paquete de implementación
author: dansimp
ms.assetid: 748272a1-6af2-476e-a3f1-87435b8e94b1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: aba5e91a4da92f9e51a5ccc70502658ae724d76f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825950"
---
# Cómo configurar un paquete de implementación


El Asistente de empaquetado le guiará a través de la creación de un paquete mediante la creación de una carpeta en el equipo local y la transferencia de todos los archivos de instalación necesarios a la única carpeta. El contenido de la carpeta se puede mover a varias unidades de medios extraíbles para su distribución.

**Nota**  
Un solo paquete no puede contener archivos de instalación para sistemas x86 y x64.



## Cómo crear un paquete de implementación


**Para crear un paquete de implementación**

1. Verifica en el módulo **imágenes** que hayas creado al menos una imagen empaquetada local.

2. En el menú **herramientas** , seleccione **Asistente para empaquetar**.

3. En la Página principal del **Asistente para empaquetar** , haga clic en **siguiente**.

4. En la página de **imagen del área de trabajo** , seleccione la casilla **incluir imagen en el paquete** para incluir una imagen en el paquete.

   El campo **imagen** está habilitado.

   **Nota**  
   No se requiere una imagen en un paquete de MED-V; el paquete puede crearse sin una imagen. En tal caso, la imagen debe cargarse en el servidor para poder descargarla posteriormente a través de la red al cliente o insertarla en una carpeta previa a la etapa de la imagen.



5. Haga clic en la lista de **imágenes** para ver todas las imágenes disponibles. Seleccione la imagen que se va a copiar en el paquete. Haga clic en **Actualizar** para actualizar la lista de imágenes disponibles.

6. Haz clic en **Siguiente**.

7. En la página Configuración de la **instalación de Med-v** , seleccione el archivo de instalación Med-v siguiendo uno de estos procedimientos:

   -   En el campo **archivo de instalación MED-V** , escriba la ruta de acceso completa al directorio donde se encuentra el archivo de instalación.

   -   Haga clic en **...** para ir al directorio donde se encuentra el archivo de instalación.

   **Nota**  
   Este campo es obligatorio y el asistente no continuará sin un nombre de archivo válido.



8. En el campo **dirección del servidor** , escriba el nombre del servidor o la dirección IP.

9. En el campo **Puerto de servidor** , escriba el puerto del servidor.

10. Seleccione el **servidor al que se accede con https** para requerir una conexión HTTPS para conectarse al servidor.

11. Realiza una de las siguientes acciones:

    -   Haga clic en **configuración de instalación predeterminada**y, a continuación, haga clic en **siguiente** para continuar y dejar la configuración predeterminada.

    -   Haga clic en **configuración de instalación personalizada**y, a continuación, en **siguiente** para personalizar la configuración de instalación.

        1.  En la página **Configuración personalizada de la instalación de MED-V** , en el campo **carpeta de instalación** , escriba la ruta de acceso de la carpeta donde se instalarán los archivos Med-v en el equipo host.

            **Nota**  
            Se recomienda usar variables en la ruta de acceso en lugar de constantes, que pueden variar de un equipo a un equipo.

            Por ejemplo, usa *%ProgramFiles%\\MED-V* en lugar de *c:\\MED-V*.



    ~~~
    2.  In the **Virtual machines images folder** field, type the path of the folder where the virtual images files will be installed on the host computer.

        **Note**  
        If you are using image pre-staging, this is the image pre-stage folder where the image is located.



    3.  In the **Minimal required RAM** field, enter the RAM required to install a MED-V package. If the user installing the MED-V package does not have the minimal required RAM, the installation will fail.

    4.  Select the **Install the MED-V management application** check box to include the MED-V management console application in the installation.

    5.  Select the **Create a shortcut to MED-V on the desktop** check box to create a shortcut to MED-V on the host's desktop.

    6.  Select the **Start automatically on computer startup** check box to start MED-V automatically on startup.

    7.  Click **Next**.
    ~~~

12. En la página **instalaciones adicionales** , seleccione la casilla **incluir instalación de software de virtualización** para incluir la instalación de Virtual PC en el paquete.

    El campo del **archivo de instalación** está habilitado. Escriba la ruta de acceso completa del archivo de instalación del software de virtualización o haga clic en **...** para ir al directorio.

13. Active la casilla **incluir instalación de Virtual PC QFE** para incluir la instalación de la actualización de Virtual PC en el paquete.

    El campo del **archivo de instalación** está habilitado. Escriba la ruta de acceso completa del archivo de instalación de la actualización de Virtual PC, o bien haga clic en **...** para ir al directorio.

14. Active la casilla **incluir instalación de Microsoft .NET framework 2,0** para incluir la instalación de Microsoft .net Framework 2,0 en el paquete.

    El campo del **archivo de instalación** está habilitado. Escriba la ruta de acceso completa del archivo de instalación de Microsoft .NET Framework 2,0 o haga clic en **...** para ir al directorio.

15. Haz clic en **Siguiente**.

16. En la página **Finalizar** , seleccione la ubicación en la que se debe guardar el paquete siguiendo uno de estos procedimientos:

    -   En el campo **destino del paquete** , escriba la ruta de acceso completa del directorio en el que se debe guardar el paquete.

    -   Haga clic en **...** para ir al directorio donde se deben guardar los archivos de instalación.

    **Nota**  
    Crear el paquete puede consumir más espacio que el tamaño real del paquete. Por lo tanto, se recomienda crear el paquete en el disco duro. Después de crear el paquete, se puede copiar en el USB.



17. En el campo **nombre del paquete** , escriba un nombre para el paquete.

18. Haga clic en **Finalizar** para crear el paquete.

    Se crea el paquete. Esto puede demorar unos minutos.

    Una vez creado el paquete, aparecerá un mensaje para notificarle que se ha completado correctamente.

**Nota**  
Si ha guardado todos los archivos de forma local y no directamente en los medios extraíbles, asegúrese de copiar solo el contenido de la carpeta y no la carpeta en los medios extraíbles.



**Nota**  
El medio extraíble debe ser lo suficientemente grande para que el contenido del paquete consuma solamente tres cuartos de la memoria del medio extraíble, como máximo.



**Nota**  
Al crear el paquete, es posible que sea necesario tener un tamaño doble del tamaño real del paquete cuando se complete la compilación.



## Temas relacionados


[Creación de una imagen de MED-V](creating-a-med-v-image.md)









