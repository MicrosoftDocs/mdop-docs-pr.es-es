---
title: Notas de la versión de App-V 4.6 SP1
description: Notas de la versión de App-V 4.6 SP1
author: dansimp
ms.assetid: aeb6784a-864a-4f4e-976b-40c34dcfd8d6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7081aaf4a04d52bf288d7a76b4a488e2b200c3d6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10819840"
---
# Notas de la versión de App-V 4.6 SP1


Para buscar estas notas de la versión, presione CTRL + F.

**Importante**  Lea estas notas de la versión minuciosamente antes de instalar el sistema de administración de Microsoft Application Virtualization (App-V). Estas notas de la versión contienen información que le ayudará a instalar correctamente Application Virtualization (App-V) 4.6 SP1. Este documento contiene información que no está disponible en la documentación del producto. Si hay una diferencia entre estas notas de la versión y otra documentación de App-V, el cambio más reciente debe considerarse autoritario.

 

## Protegerse contra virus y vulnerabilidades de seguridad


Para ayudar a protegerse contra virus y vulnerabilidades de seguridad, es importante instalar las últimas actualizaciones de seguridad disponibles para cualquier nuevo software que se instale. Para obtener más información, consulte el [sitio web de seguridad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problemas conocidos con Application Virtualization 4.6 SP1


Esta sección proporciona la información más actualizada sobre problemas con Microsoft Application Virtualization (App-V) 4.6 SP1. Estos problemas no aparecen en la documentación del producto y, en algunos casos, podrían contradecir la documentación del producto existente. Cuando sea posible, estos problemas se resolverán en versiones posteriores.

### La ruta de acceso de SPRT se pierde si no termina en una barra diagonal (/)

Cuando la ruta de un elemento HREF de una plantilla de proyecto no termina con una barra diagonal ( **/** ), el href generado no incluye la ruta de acceso. Esto sucede cuando el usuario manipula manualmente el archivo **. SPRT** . Si usa el secuenciador, siempre agrega la barra diagonal ( **/** ) después de la ruta de acceso.

Solución Asegúrese de que la HREF tenga una barra diagonal hacia adelante ( **/** ).

### El nombre de la carpeta de usuario no se corresponde con el nombre del paquete

Las carpetas que contienen archivos. pkg y de usuario ya no incluyen el nombre del paquete. Anteriormente, el cliente de App-V usaba el nombre corto de la 8,3 carpeta raíz del paquete como parte del nombre de la carpeta. Esto te permite identificarlo fácilmente. Cuando usas el secuenciador App-V 4,6 SP1, los nombres cortos de la 8,3 carpeta raíz del paquete son ahora cadenas aleatorias. Esto dificulta la identificación de las carpetas que contienen los archivos **. pkg** del paquete en el equipo en el que se ejecuta el cliente de App-V.

SOLUCIÓN use uno de los siguientes métodos para identificar más fácilmente estas carpetas de paquetes:

1.  Cuando cree el paquete mediante el secuenciador, especifique un nombre de carpeta que siga la Convención de nomenclatura de 8,3 para la carpeta principal de la aplicación. Este nombre se usará como parte del nombre de la carpeta de usuario tal y como se mostraba en App-V 4,6.

2.  El archivo. SPRJ contiene ahora una etiqueta que muestra la cadena que se usa como el principio del nombre de la carpeta de usuario. Puedes usar el elemento **SHORTNAME** del elemento **PACKAGEROOTFOLDER** para determinar el nombre.

### Ejecución de App-V 4,6 SP1 en equipos con más de 64 procesadores

Cuando ejecuta App-V 4,6 SP1 en equipos que tienen más de 64 procesadores instalados, se produce un error en el cliente de App-V.

SOLUCIÓN ninguna. Esta configuración no es compatible. Debe ejecutar los equipos con App-V 4,6 SP1on que tengan menos de 64 procesadores.

### La actualización de Application Virtualization 4,6 SP1 no se ofrece en todas las configuraciones regionales que usan Microsoft Update

Cuando usa Microsoft Update, la actualización de App-V 4,6 SP1 no está disponible para las siguientes configuraciones regionales de idioma:

-   Kazajo

-   Hindi

-   Serbio-cirílico

SOLUCIÓN alternativa si usa Microsoft Windows Server Update Services (WSUS), use la versión en Inglés de la actualización o descargue la actualización desde el catálogo de Microsoft Update.

### Después de expandir el paquete primario, no se puede secuenciar un complemento con componentes en paralelo

Al expandir un paquete principal con herramientas que **Tools**  /  **expanda el paquete a un sistema local** en la consola del secuenciador de App-V y se secuencia un complemento con componentes en paralelo, se devolverá un error de instalación. Por ejemplo:

-   **HRESULT 0x80073712**

Esto se debe a que el secuenciador escribe el componente en paralelo en el registro, pero no borra el valor de la siguiente clave del registro:

HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty

SOLUCIÓN alternativa después de expandir el paquete principal en el equipo que ejecuta el secuenciador, tiene que eliminar el valor de la siguiente clave del registro:

HKEY \ _LOCAL \ _MACHINE \\COMPONENTS\\StoreDirty

Una vez que haya eliminado el valor, ordene el complemento.

### Información de copyright de notas de versión

Este documento se proporciona "tal cual". La información y las vistas expresadas en este documento, como direcciones URL y otras referencias de sitios web de Internet, pueden cambiar sin previo aviso. Usted asume el riesgo de su uso.

Algunos ejemplos que se describen en este artículo se proporcionan solo para la ilustración y son ficticios. No se pretende ni se debe deducir ninguna asociación o conexión real.

Este documento no le proporciona derechos legales sobre ninguna propiedad intelectual en ningún producto de Microsoft. Puede copiar y usar este documento para su referencia interna. Puede modificar este documento para su referencia interna.



Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server y Windows Vista son marcas comerciales del grupo de empresas de Microsoft.

El resto de marcas comerciales pertenecen a sus respectivos dueños.

 

 





