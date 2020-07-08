---
title: Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V
description: Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V
author: dansimp
ms.assetid: fd5a62e9-0577-44d2-ae17-61c0aef78ce8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cc8f9579d800aa0e5da0d67e0cd71bcae5e912a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826921"
---
# Cómo publicar y anular la publicación de una aplicación en el área de trabajo de MED-V


Aunque una aplicación se instala en un área de trabajo de MED-V, también es posible que tenga que publicar la aplicación antes de que esté disponible para el usuario final. De forma predeterminada, la mayoría de las aplicaciones se publican en el momento en que se instalan y se habilitan los accesos directos.

En algunos casos, es posible que desee instalar aplicaciones en el área de trabajo de MED-V sin que estén disponibles para el usuario final, por ejemplo, software de detección de virus. De forma similar, hay ocasiones en las que desea publicar una aplicación instalada en el área de trabajo de MED-V que antes no estaba disponible para el usuario final. Por ejemplo, es posible que tenga que publicar una aplicación instalada si la instalación no ha creado automáticamente un acceso directo en el menú **Inicio** .

**Importante**  Si publica una aplicación que no admite rutas de acceso UNC, le recomendamos que asigne la aplicación a una unidad.

 

Puede publicar o anular la publicación de aplicaciones en un área de trabajo de MED-V implementada realizando una de las siguientes tareas:

**Para publicar o anular la publicación de una aplicación instalada**

1.  Para publicar una aplicación en un área de trabajo de MED-V implementada, copie un acceso directo para esa aplicación en la siguiente carpeta de la máquina virtual:

    Menú Users\\Start de C:\\Documents and Settings\\All

    Si es necesario, use una directiva de grupo o un sistema ESD para implementar una secuencia de comandos que copie el acceso directo de esa aplicación a la carpeta del menú todos los Users\\Start.

2.  Para anular la publicación de una aplicación en un área de trabajo de MED-V implementada, elimine el acceso directo de la aplicación en la siguiente carpeta de la máquina virtual:

    Menú Users\\Start de C:\\Documents and Settings\\All

    Si es necesario, use una directiva de grupo o un sistema ESD para implementar una secuencia de comandos que elimine el acceso directo de la aplicación en la carpeta del menú todos los Users\\Start.

    **Nota:**  Con frecuencia, el acceso directo se elimina automáticamente del menú **Inicio** del equipo host al desinstalar la aplicación. Sin embargo, en algunos casos, como para un área de trabajo de MED-V que está configurada para todos los usuarios de un equipo compartido, es posible que tenga que eliminar manualmente el acceso directo en el menú **Inicio** después de desinstalar la aplicación. El usuario final puede hacerlo haciendo clic con el botón secundario del ratón en el acceso directo y seleccionando **eliminar**.

     

Para comprobar que la aplicación se ha publicado o no se ha publicado, compruebe en el área de trabajo de MED-V si el método abreviado correspondiente está disponible o no.

**Nota:**  Las aplicaciones que se incluyen en Windows XP SP3 y que se encuentran en la carpeta del menú Inicio de la máquina virtual no se publican automáticamente en el host. Se controlan mediante la configuración del registro que bloquea la publicación automática. Para obtener más información, vea [lista de exclusión de aplicaciones de Virtual PC de Windows](windows-virtual-pc-application-exclude-list.md).

 

**Para publicar elementos del panel de control**

1.  Cree un acceso directo en la máquina virtual en la que el destino sea el nombre del elemento, como C:\\WINDOWS\\system32\\appwiz.cpl.

    El acceso directo debe crearse o moverse a la carpeta "%ALLUSERSPROFILE%\\Start Menu\\" o a una de sus subcarpetas.

    El elemento se publicará en el equipo host, en la ubicación correspondiente, en la carpeta del menú Inicio del host.

2.  Inicie el acceso directo para el elemento en el host.

**PRECAUCIÓN**  Cuando cree el acceso directo, no especifique% SystemRoot% \\control.exe. Esta aplicación no se publicará porque está incluida en la configuración del registro que bloquea la publicación automática.

 

**Cómo controla MED-V la publicación automática de aplicaciones**

1.  Durante la publicación de la aplicación, MED-V copia los accesos directos de la máquina virtual invitada en el equipo host al intentar coincidir con la jerarquía de carpetas que existe en el invitado. Al hacerlo, MED-V copia los accesos directos del invitado en el host siguiendo estos pasos:

    1.  MED-V intenta localizar una carpeta en Start Menu\\Programs en el equipo host que tiene el mismo nombre que la carpeta del invitado donde se encuentra el acceso directo.

    2.  Si no hay ninguna carpeta coincidente, MED-V intenta encontrar una carpeta en la carpeta del menú Inicio del host que tiene el mismo nombre que la carpeta del invitado donde se encuentra el acceso directo.

    3.  Si no hay ninguna carpeta coincidente, MED-V copia el acceso directo a la carpeta predeterminada del host, la carpeta Start Menu\\Programs.

2.  Ejemplo de proceso de publicación de aplicaciones:

    1.  Si un acceso directo de la aplicación se publica en la carpeta Start Menu\\Programs\\AppShortcuts en el invitado, MED-V busca en el equipo anfitrión una carpeta Start Menu\\Programs\\ AppShortcuts y, si la encuentra, copia el acceso directo a esa carpeta.

    2.  Si no se encuentra la carpeta, MED-V busca en el equipo anfitrión una carpeta Start Menu\\AppShortcuts y, si la encuentra, copia el acceso directo a esa carpeta.

    3.  Si no se encuentra la carpeta, MED-V copia el acceso directo a la carpeta Inicio de Menu\\Programs.

**Nota:**  Ya debe existir una carpeta en la carpeta del menú Inicio del equipo host para MED-V para copiar el acceso directo allí. MED-V no crea la carpeta si aún no existe.

 

## Temas relacionados


[Instalar y quitar una aplicación en el área de trabajo de MED-V](installing-and-removing-an-application-on-the-med-v-workspace.md)

[Administrar las actualizaciones de Software para áreas de trabajo de MED-V](managing-software-updates-for-med-v-workspaces.md)

[Lista de exclusión de aplicación de Windows Virtual PC](windows-virtual-pc-application-exclude-list.md)

 

 





