---
title: Planificación de seguridad de cliente
description: Planificación de seguridad de cliente
author: dansimp
ms.assetid: 4840a60f-4c91-489c-ad0b-6671882abf9b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e0038f7cbc8592d6c7fcdfa485111da88c17791d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815931"
---
# Planificación de seguridad de cliente


El cliente de App-V proporciona varias mejoras de seguridad que no estaban presentes en versiones anteriores del producto. Estos cambios proporcionan una mayor seguridad después de la instalación y a través de una configuración posterior de la configuración del cliente. En este tema se describen algunas de estas mejoras y se identifican varias opciones de configuración importantes relacionadas con la seguridad que debe tener en cuenta durante el proceso de planeación. Es importante recordar que las aplicaciones virtuales siguen siendo ejecutables, por lo que debe asegurarse de que estos activos no sean manipulados por personas no autorizadas. Por este motivo, la caché del archivo del descriptor de software abierto (OSD) se protege según se describe más adelante en este tema y le recomendamos encarecidamente que use RTSPs, HTTPS e IPsec para proteger la publicación y la transmisión por secuencias.

## Seguridad del cliente de App-V


De forma predeterminada, durante la instalación el cliente de App-V está configurado con los permisos mínimos necesarios para permitir que un usuario realice una actualización de publicación e inicie las aplicaciones. Otras mejoras de seguridad proporcionadas en el cliente de App-V incluyen lo siguiente:

-   De forma predeterminada, la caché de archivos OSD solo puede ser actualizada por los administradores y mediante el proceso de actualización de la publicación.

-   El archivo de registro (sftlog.txt) solo es accesible para las cuentas con acceso administrativo local al cliente.

-   El archivo de registro ahora tiene un tamaño máximo.

### Asociaciones de tipo de archivo

De forma predeterminada, la instalación del cliente registra las asociaciones de tipo de archivo (FTAs) para los archivos OSD, lo que permite a los usuarios iniciar las aplicaciones directamente desde archivos OSD en lugar de los accesos directos publicados. Si un usuario con derechos de administrador local recibe un archivo OSD que contiene código malintencionado, ya sea en un correo electrónico o se descarga de un sitio web, el usuario puede abrir el archivo OSD e iniciar la aplicación incluso si el cliente se ha configurado para restringir el permiso para **agregar aplicaciones** . Puedes anular el registro de FTAs para el OSD y así reducir este riesgo. Además, puedes bloquear esta extensión en el sistema de correo electrónico y en el firewall. Para obtener más información sobre cómo configurar Outlook para bloquear extensiones, consulte <https://go.microsoft.com/fwlink/?LinkId=133278> .

**Nota de seguridad:**

A partir de la versión 4.6 de App-V, la Asociación de tipo de archivo ya no se crea para los archivos OSD durante una nueva instalación del cliente, aunque la configuración existente se mantendrá durante una actualización de la versión 4,2 o 4,5 del cliente de App-V. Si, por algún motivo, es esencial crear la Asociación de tipos de archivo, puede crear las siguientes claves de registro y establecer sus valores como se muestra a continuación:

    Create HKEY\_CLASSES\_ROOT\\.osd with a default value of SoftGrid.osd.File

    Under HKEY\_LOCAL\_MACHINE\\software\\classes\\Softgrid.osd.file, create a string value named AppUserModelID with a data value of Microsoft.AppV.Client.Tray

### Authorization

Durante la instalación, puede usar el parámetro **RequireAuthorizationIfCached** para configurar que el cliente solicite la autorización del servidor cuando intente iniciar una aplicación. Debe considerar detenidamente cómo establecer este parámetro. Si el servidor de App-V no está disponible por cualquier motivo, la aplicación usará el estado almacenado más reciente de este parámetro para controlar el acceso de los usuarios a la aplicación. Si el usuario no inició la aplicación correctamente antes de que el servidor de App-V deje de estar disponible, no podrá iniciar la aplicación hasta que pueda comunicarse con el servidor y recibir autorización. Sin embargo, si establece el parámetro para que el cliente no requiera autorización y el servidor no esté disponible, todas las aplicaciones almacenadas en caché se pueden iniciar de forma autorizada o no. Además, si el usuario tiene permiso para cambiar el modo sin conexión del cliente a través de permisos o si el usuario es un administrador local, el usuario podrá abrir todos los paquetes en caché como si la infraestructura de App-V no estuviera disponible.

### Exploración antivirus

El software antivirus que se ejecuta en un equipo cliente de App-V puede detectar y denunciar un archivo infectado en el entorno virtual. Sin embargo, no puede desinfectar el archivo. Si se detecta un virus en el entorno virtual, el software antivirus realizará la operación de cuarentena o reparación configurada en la memoria caché, no en el paquete en sí. Configure el software antivirus con una excepción para el archivo sftfs. FSD. Este archivo es el archivo de caché que almacena paquetes en el cliente de App-V.

**Nota de seguridad:**

Si se detecta un virus en una aplicación o un paquete implementado en el entorno de producción, reemplace la aplicación o el paquete con una versión libre de virus.

## Comunicación entre el cliente y el servidor


Las actualizaciones de publicación y la transmisión por secuencias de paquetes también son áreas donde las consideraciones de seguridad relacionadas con la comunicación entre clientes y servidores son importantes.

### Actualización de publicaciones

Cuando el cliente se comunica con el servidor para realizar una actualización de publicación, usa las credenciales del usuario que ha iniciado sesión para solicitar información sobre los paquetes de la aplicación. Debe proteger la comunicación que se produce entre el cliente de App-V y el servidor de administración de App-V para asegurarse de que no se pueda manipular ninguna información de publicación en tránsito. Esto se realiza mediante la opción seguridad mejorada, que usará RTSPs/HTTPS. La comunicación entre el cliente y la ubicación en la que se almacenan los archivos ICO y OSD debe usar IPsec para recursos compartidos SMB/CIFS y HTTPS para un servidor IIS.

**Nota:**  Si está usando IIS para publicar los archivos ICO y OSD, configure un tipo MIME para OSD = TXT; de lo contrario, IIS no podrá ofrecer los archivos ICO y OSD a los clientes.

 

### Streaming de paquetes

Cuando un usuario inicia una aplicación por primera vez, o si se han establecido parámetros de carga automática en el cliente, el paquete de la aplicación se transmite desde un servidor a la caché del cliente. Este proceso es compatible con los protocolos RTSP/RTSPs, HTTP/HTTPS y SMB/CIFS. Los archivos OSD controlan qué protocolos se usan, a menos que la configuración **ApplicationSourceRoot** o **OverrideURL** se haya configurado en los clientes. Debe configurar la comunicación para que se produzca a través de RTSPs, HTTPS o IPsec para SMB/CIFS, a fin de lograr mayores niveles de seguridad. Para obtener más información sobre cómo elegir qué método de comunicación usar, consulte la guía de planeación e implementación de App-V en <https://go.microsoft.com/fwlink/?LinkId=122063> .

**Nota:**  Si está usando IIS para publicar paquetes (archivos SFT), configure un tipo MIME para SFT = Binary; de lo contrario, IIS no podrá ofrecer los archivos SFT a los clientes.

 

### Perfiles de itinerancia y redirección de carpetas

El sistema App-V almacena los cambios específicos de usuario en los paquetes en el archivo usrvol \ _sftfs \ _v1. pkg. Este archivo se encuentra en la carpeta datos de programa del perfil de un usuario. Puesto que el perfil o una carpeta de datos de la aplicación redirigida se transfiere entre el cliente y el servidor, use IPsec para proteger la comunicación.

## Consideraciones para clientes con conexión a Internet


Para los clientes orientados a Internet, es importante tener en cuenta si el cliente está unido a un dominio o si no está unido a un dominio.

### Cliente unido a un dominio

De forma predeterminada, los clientes de App-V usan vales de Kerberos emitidos por los servicios de dominio de Active Directory para la autenticación y autorización en la intranet. Estos vales de Kerberos son válidos durante 10 horas de forma predeterminada. El cliente usará este vale para acceder al servidor de App-V, siempre y cuando el vale sea válido, incluso si el equipo no puede conectarse al controlador de dominio para actualizar el vale. Si el vale Kerberos expira, el cliente de App-V volverá a la autenticación NTLM y usará las credenciales almacenadas en la caché del usuario.

### Cliente que no está unido a un dominio

Si un usuario está basado en el hogar y el equipo no está unido al dominio de la compañía, App-V aún puede admitir la entrega de aplicaciones. Para autenticar y autorizar a un usuario a realizar una actualización de publicación e iniciar aplicaciones, configure la cuenta de usuario en el equipo cliente para almacenar el nombre de usuario y la contraseña que tienen acceso al entorno de App-V y para proporcionar los permisos adecuados a las aplicaciones.

## Temas relacionados


[Planificación de seguridad y protección](planning-for-security-and-protection.md)

 

 





