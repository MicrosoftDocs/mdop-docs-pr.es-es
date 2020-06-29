---
title: Aplicación de consola de administración de servidores nodo del sistema de virtualización
description: Aplicación de consola de administración de servidores nodo del sistema de virtualización
author: dansimp
ms.assetid: 9450832e-335c-41e7-af24-fddb8ffc327c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51256ee7e96a97016e73dc79c87e4d422198cfb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815441"
---
# Consola de administración de servidor: Nodo de sistema de virtualización de aplicaciones


El nodo del sistema de virtualización de aplicaciones es el nodo de nivel superior en el panel de **ámbito** . Este nodo muestra el nombre del servidor que la consola está controlando actualmente, o bien muestra el nombre del equipo local (si está conectado por el nombre) o "local" cuando la consola está conectada al equipo local. Desde el nodo del sistema de virtualización de aplicaciones, puede conectarse a otro equipo o conectarse al equipo actual con un conjunto diferente de credenciales.

Puede hacer clic con el botón secundario en el nodo del sistema de virtualización de aplicaciones para mostrar los siguientes elementos.

<a href="" id="configure-connection"></a>**Configurar conexión**  
En este cuadro de diálogo, puede modificar las siguientes opciones de configuración:

- **Nombre de host del servicio Web**: le permite escribir el nombre del sistema de virtualización de aplicaciones al que desea conectarse, o bien puede escribir **localhost** para conectarse al equipo local.

- **Usar conexión segura**: Seleccione si desea conectarse al servidor con una conexión segura.

- **Puerto**: le permite introducir el número de puerto que desea usar para la conexión. 80 es el número de Puerto normal predeterminado y 443 es el número de puerto seguro predeterminado.

- **Usar cuenta de Windows actual**: Seleccione esta forma para usar las credenciales de la cuenta de Windows actuales.

- **Especificar cuenta de Windows**: seleccione Cuándo desea conectarse al servidor como un usuario diferente.

- **Nombre**: permite especificar el nombre del nuevo usuario mediante el formato *DOMAIN\\username* o el <em> username@domain </em> .

- **Contraseña**: le permite escribir la contraseña que corresponde al nuevo usuario.

<a href="" id="system-options"></a>**Opciones del sistema**  
En las siguientes pestañas de este cuadro de diálogo, puede modificar la configuración asociada:

-   **Ficha General**: permite especificar la ruta de **contenido predeterminada** donde se almacenan los archivos OSD y de icono.

-   **Ficha base de datos**: permite especificar el tamaño máximo de la **base de datos** y el **historial de uso**.

<a href="" id="view"></a>**Ver**  
Cambia la apariencia de la consola de administración de Application Virtualization Server. Para obtener más información sobre cómo cambiar la apariencia de la consola, consulte los archivos de ayuda de Microsoft Management Console.

<a href="" id="new-window-from-here"></a>**Nueva ventana desde aquí**  
Abre una nueva ventana de administración de consola.

<a href="" id="export-list"></a>**Exportar lista**  
Crea un archivo de texto delimitado por tabulaciones que incluye el contenido del panel **resultados** . Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.

<a href="" id="help"></a>**Ayuda**  
Inicia el archivo de ayuda de la consola de administración.

## Temas relacionados


[Referencia de la consola de administración de servidor de virtualización de aplicaciones](application-virtualization-server-management-console-reference.md)

 

 





