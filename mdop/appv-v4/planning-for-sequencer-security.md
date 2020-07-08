---
title: Planificación de seguridad del secuenciador
description: Planificación de seguridad del secuenciador
author: dansimp
ms.assetid: 8043cb02-476d-4c28-a850-903a8ac5b2d3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: bf1e85e24d93d373add38b5efe51ceb40faae24e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815911"
---
# Planificación de seguridad del secuenciador


Incorpore procedimientos de implementación recomendados lo antes posible al configurar virtualización de aplicaciones (App-V) para que la implementación del secuenciador sea funcional y más segura. Si ya ha configurado el secuenciador, use las siguientes pautas de procedimientos recomendados para revisar las decisiones de diseño y analizarlas desde una perspectiva de seguridad.

**Importante**  
El secuenciador de App-V recopila e implementa toda la información de la aplicación registrada en el equipo que ejecuta el secuenciador. Debe asegurarse de que todos los usuarios que tengan acceso al equipo en el que se ejecuta el secuenciador tengan credenciales administrativas. Los usuarios con credenciales de cuenta de usuario no deben tener acceso para controlar el contenido y los archivos de paquete. Si está realizando la secuencia en un equipo que ejecuta servicios de escritorio remoto (anteriormente servicios de Terminal Server), asegúrese de que se trata de un equipo dedicado a la secuenciación y de que los usuarios con credenciales de cuenta de usuario no están conectados a él durante la secuenciación.



## Procedimientos recomendados de seguridad del secuenciador


Considere los escenarios siguientes y los procedimientos recomendados asociados al implementar y usar el secuenciador de Application Virtualization (App-V):

-   **Análisis de virus en el equipo en el que se ejecuta el secuenciador**: se recomienda explorar el equipo que ejecuta el secuenciador en busca de virus y, a continuación, deshabilitar todo el software de detección antivirus y malware en el equipo que ejecuta el secuenciador durante el proceso de secuenciación. Esto acelerará el proceso de secuencia y evitará que los componentes de software antivirus y antimalware interfieran con el proceso de secuencia. Después, instale el paquete secuenciado en un equipo que no ejecute el secuenciador y, después de una instalación correcta, explore el equipo en busca de virus. Si se encuentran virus, debe ponerse en contacto con el fabricante del software para informarle de los archivos de origen infectados y solicitar un origen de instalación actualizado sin virus. De manera opcional, el secuenciador puede analizarse después de la fase de instalación y, si se encuentra un virus, debe ponerse en contacto con el fabricante del software según se menciona anteriormente.

    **Nota**  
    Si se detecta un virus en una aplicación, la aplicación no se debe implementar en los equipos de destino.



-   **Captura de listas de control de acceso (ACL) en archivos NTFS**: el secuenciador de App-V captura los permisos del sistema de archivos NTFS para los archivos que se supervisan durante la instalación del producto. Esta capacidad le permite replicar con mayor precisión el comportamiento previsto de la aplicación, como si estuviera instalado en forma local y no virtualizada. En algunos escenarios, una aplicación puede almacenar información a la que los usuarios no estaban destinados a obtener acceso a los archivos de la aplicación. Por ejemplo, una aplicación podría almacenar información de credenciales en un archivo dentro de la aplicación. Si las ACL no se aplican en el paquete, un usuario podría ver y, a continuación, usar esta información fuera de la aplicación.

    **Nota**  
    No se deben secuenciar las aplicaciones que almacenan información específica de seguridad no cifrada, como contraseñas, etc.



~~~
During the installation phase, you can modify the default permissions of the files if necessary. After completion of the sequencing process, but before saving the package, you can choose whether to enforce security descriptors that were captured during the installation of the application. By default, App-V will enforce the security descriptors specified during the installation of the application. If you turn off security descriptor enforcement, you should test the application to ensure the removal of associated Access Control Lists (ACL) will not cause the application to perform unexpectedly.
~~~

-   El **secuenciador no captura las ACL del registro**: aunque el secuenciador captura las ACL del sistema de archivos NTFS durante la fase de instalación de la secuenciación, no captura las ACL para el registro. Los usuarios tendrán acceso total a todas las claves del registro para las aplicaciones virtuales excepto los servicios. Sin embargo, si un usuario modifica el registro de una aplicación virtual, el cambio se almacenará en una tienda específica (**uservol \ _sftfs \ _v1. pkg**) y no afectará a otros usuarios.

-   **Servicios de aplicaciones**: App-V proporciona soporte técnico para los servicios de aplicación que forman parte de una aplicación virtualizada. Sin embargo, en el entorno virtual, el contexto de seguridad que se ejecutará como está limitado. Los únicos contextos de seguridad admitidos en un entorno virtual son sistema local, servicio local y servicio de red. Durante la secuenciación, si se especifica un contexto de seguridad para un servicio de aplicación distinto de los tres compatibles, se aplicará el contexto de seguridad del sistema local en el entorno virtual. Si el servicio de aplicaciones está configurado para usar servicio local o servicio de red, se le atenderá en el entorno virtual. La configuración de la cuenta de servicio se puede realizar durante el proceso de secuenciación con estos tres contextos de seguridad.

-   **Información de seguridad persistente**: al secuenciar aplicaciones, puede instalar la aplicación como un usuario o puede desarrollar un método automatizado para instalar la aplicación mientras se está supervisando. Todo lo que no se excluye del paquete se capturará como parte de ese paquete, de modo que la aplicación tendrá los activos necesarios para ejecutarse en un entorno virtualizado. Algunas aplicaciones almacenan información confidencial de seguridad (como contraseñas) durante la instalación; Si no está protegido, es posible que otros usuarios puedan acceder a esta información de seguridad con acceso al paquete. Durante la instalación, si una instalación de aplicación le pide una contraseña u otra información confidencial de seguridad, consulte la documentación para asegurarse de que no persiste (se elimina después de la instalación) o, si se ha conservado, que está protegida (cifrada).

-   **Proteger paquetes de aplicaciones virtuales**: siempre guarda paquetes de aplicaciones virtuales en una ubicación segura de la red para impedir que el paquete se manipule o se dañe.

## Temas relacionados


[Planificación de seguridad y protección](planning-for-security-and-protection.md)









