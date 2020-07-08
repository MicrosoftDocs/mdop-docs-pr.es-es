---
title: Ficha General de propiedades de virtualización de aplicaciones
description: Ficha General de propiedades de virtualización de aplicaciones
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819690"
---
# Propiedades de virtualización de aplicaciones: Pestaña General


Use la pestaña **General** del cuadro de diálogo **propiedades de Application Virtualization** para modificar la configuración de registro y las ubicaciones de datos.

Esta pestaña contiene los siguientes elementos.

<a href="" id="log-level"></a>**Nivel de registro**  
Seleccione el nivel de la lista desplegable. El nivel predeterminado es **información**.

<a href="" id="reset-log"></a>**Restablecer registro**  
Haga clic en este botón para realizar una copia de seguridad del archivo de registro actual e iniciar inmediatamente un nuevo archivo de registro.

<a href="" id="location"></a>**Ubicación**  
Escriba o busque la ubicación en la que desea guardar el archivo de registro sftlog.txt. Las ubicaciones predeterminadas son las siguientes:

-   Para WindowsXP, Windows Server2003:*C:\\Documents and Settings\\All Users\\Application cliente de virtualización de Data\\Microsoft\\Application*

-   Para Windows Vista, Windows 7, Windows Server2008:*C:\\ProgramData\\Microsoft\\Application cliente de virtualización*

<a href="" id="system-log-level"></a>**Nivel de registro del sistema**  
Seleccione el nivel de la lista desplegable. El nivel predeterminado es **ADVERTENCIA**.

**Nota:**  La configuración del **nivel de registro del sistema** controla el nivel de los mensajes enviados al registro de eventos del sistema. Los mensajes registrados son idénticos a los mensajes que se registran en el registro de eventos del cliente, pero se almacenan en una ubicación diferente que no tiene las limitaciones de espacio del registro de eventos del cliente. Dado que el registro de eventos del sistema no tiene limitaciones de espacio, es ideal para situaciones en las que es necesario realizar registros detallados.

 

<a href="" id="global-data-directory"></a>**Directorio de datos global**  
Escriba o busque la ubicación del directorio del archivo de registro. Las ubicaciones predeterminadas son las siguientes:

-   Para WindowsXP, Windows Server2003:*C:\\Documents and Settings\\All Users\\Application cliente de virtualización de Data\\Microsoft\\Application*

-   Para Windows Vista, Windows 7, Windows Server2008:*C:\\ProgramData\\Microsoft\\Application cliente de virtualización*

<a href="" id="user-data-directory"></a>**Directorio de datos de usuario**  
Escriba o busque la ubicación del directorio donde se almacenan los datos específicos del usuario. El valor predeterminado es% APPDATA%. Esta ruta debe ser una variable de entorno válida en el equipo cliente.

## Temas relacionados


[Consola de administración de cliente: Propiedades de virtualización de aplicaciones](client-management-console-application-virtualization-properties.md)

 

 





