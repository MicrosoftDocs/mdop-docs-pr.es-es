---
title: Cómo configurar el sistema de App-V para la actualización de paquetes
description: Cómo configurar el sistema de App-V para la actualización de paquetes
author: dansimp
ms.assetid: de133898-f887-46c1-9bc9-fbb03feac66a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5e5056f923c61aff39d9bd6e1d26f071177f7c12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817850"
---
# Cómo configurar el sistema de App-V para la actualización de paquetes


Al implementar una nueva versión de un paquete de aplicación existente que se ha actualizado en el secuenciador de App-V, puede implementarla para que los clientes de App-V transmitan automáticamente la nueva versión a la memoria caché local. En función de la solución de transmisión por secuencias que use, existen diferentes procedimientos para configurar la actualización del paquete. En las siguientes secciones se describen los escenarios más comunes para publicar y transmitir por secuencias, e incluir los procedimientos necesarios para configurar la actualización de paquete para cada escenario.

## Usar un servidor de administración para la publicación y la transmisión por secuencias


En este escenario, se usa un único servidor de administración de aplicaciones-V para publicar y transmitir paquetes y aplicaciones, y se requiere el protocolo RTSP (S). Cuando se importa el paquete original al servidor de administración de App-V, el administrador copia la carpeta del paquete que contiene los archivos creados por el secuenciador en la carpeta de contenido, por ejemplo, para \\\\server\\CONTENT\\packagename. El administrador también edita la entrada HREF en el archivo OSD para que apunte al archivo SFT de la carpeta Package y, a continuación, importa el paquete al servidor.

Cuando el servidor de administración autentica a un usuario, el servidor publica las aplicaciones del usuario enviando el archivo de applist.xml al cliente. A continuación, el cliente recupera los archivos y los iconos OSD para las aplicaciones desde el servidor de administración. Cuando el usuario hace doble clic en el icono de una aplicación, el contenido de la aplicación se transmite a la memoria caché del cliente de la ruta de acceso que se especifica en el archivo OSD, y se inicia la aplicación.

### Para actualizar el paquete

Para agregar una nueva versión de una aplicación que se ha actualizado en el secuenciador de App-V, el administrador debe copiar el nuevo archivo SFT y otros archivos modificados en la misma carpeta que la versión original de la aplicación. El administrador usará **Agregar versión** en la consola de administración de servidores para agregar la nueva versión del paquete.

La siguiente vez que el usuario inicia la aplicación, el servidor transmite automáticamente la nueva versión al cliente. Este método específico de actualización de un paquete fue conocido anteriormente como una actualización activa.

## Usar un servidor de administración para publicar y un servidor de transmisión por secuencias


En este escenario, el servidor de administración de App-V se usa para publicar los paquetes, y el servidor de transmisión se usa para transmitir paquetes y aplicaciones. El protocolo RTSP (S) es necesario. Cuando se importa el paquete original al servidor de administración, el administrador copia la carpeta del paquete que contiene los archivos creados por el secuenciador a la carpeta de contenido, por ejemplo, a \\\\server\\CONTENT\\packagename. El administrador edita la entrada HREF en el archivo OSD para indicar el archivo SFT en el servidor de streaming y, a continuación, importa el paquete al servidor de administración.

Para configurar el servidor de transmisión, el administrador copia la carpeta del paquete del servidor de administración a la carpeta de contenido en el servidor de transmisión. Esta carpeta debe tener el mismo nombre y ruta de acceso relativa en la carpeta de contenido del servidor de streaming, como en el servidor de administración, por ejemplo, \\\\streamingserver\\CONTENT\\packagename.

Si la configuración raíz de origen de la aplicación del cliente (ASR) está configurada para apuntar al servidor de transmisión, el cliente usa esta configuración en lugar del nombre del servidor en la entrada HREF del archivo OSD. Los campos ISR y OSR del cliente se pueden configurar opcionalmente para que señalen al servidor de administración o al servidor de transmisión, en función de la arquitectura del sistema específico que se use.

Cuando el servidor de administración autentica a un usuario, el servidor publica las aplicaciones del usuario enviando el archivo de applist.xml al cliente. El cliente recupera los iconos y archivos OSD de las aplicaciones desde el servidor de transmisión o el servidor de administración, en función de la configuración de los campos OSR y ISR.

Cuando el usuario hace doble clic en el icono de una aplicación, el cliente utiliza la ruta de acceso al archivo de contenido del paquete (SFT) que se encuentra en el elemento HREF del archivo OSD. Si se usa la ASR, el cliente reemplaza el nombre del servidor (y el puerto y el protocolo, si se usan) en el elemento HREF con la ruta de acceso al servidor de transmisión que se especifica en la ASR. A continuación, la aplicación se transmite desde el servidor de transmisión a la caché del cliente y se inicia.

### Para actualizar el paquete

Para agregar una nueva versión de una aplicación que se ha actualizado en el secuenciador de App-V, el administrador debe copiar la nueva versión del archivo SFT y cualquier otro archivo modificado en la misma carpeta que la versión original de la aplicación en el servidor de transmisión.

Por coherencia, le recomendamos que copie también los nuevos archivos en la carpeta del servidor de administración. En particular, si usa los campos OSR o ISR del cliente, copie el archivo y los iconos del OSD actualizados en el servidor especificado en los campos OSR y ISR.

Una vez que el servidor de transmisión detecta la nueva versión, la próxima vez que el usuario inicie la aplicación, el servidor transmitirá automáticamente la nueva versión al cliente.

## Usar un servidor de administración para publicar y un servidor IIS para la transmisión por secuencias


En este escenario, el servidor de administración de App-V se usa para publicar los paquetes, y el servidor IIS se usa para transmitir paquetes y aplicaciones. Cuando se importa el paquete original al servidor de administración, el administrador copia la carpeta del paquete que contiene los archivos creados por el secuenciador a la carpeta de contenido, por ejemplo, a \\\\server\\CONTENT\\packagename. El administrador edita la entrada HREF en el archivo OSD, de modo que apunte al archivo SFT en el servidor IIS y, a continuación, importa el paquete al servidor de administración.

Para configurar el servidor IIS para la transmisión por secuencias, el administrador copia la carpeta del paquete desde el servidor de administración a la carpeta de contenido en el servidor IIS. Esta carpeta debe tener el mismo nombre y ruta de acceso relativa bajo la carpeta de contenido web del servidor IIS que en el servidor de administración; por ejemplo, se puede acceder a la dirección URL en el servidor IIS mediante http://IISserver/CONTENT/packagename o https://IISserver/CONTENT/packagename .

Si la configuración raíz de origen de la aplicación del cliente (ASR) está configurada para apuntar al servidor IIS, el cliente usa la ASR en lugar del nombre del servidor en la entrada HREF del archivo OSD. De manera opcional, puede configurar los campos ISR y OSR en el cliente para que señalen al servidor de administración o al servidor IIS, en función de la arquitectura de sistema específica que use.

Cuando el servidor de administración autentica al usuario, el servidor publica las aplicaciones del usuario enviando el archivo de applist.xml al cliente. El cliente recupera los iconos y archivos OSD de las aplicaciones desde el servidor IIS o el servidor de administración, según la configuración de los campos ISR y OSR.

Cuando el usuario hace doble clic en el icono de una aplicación, el cliente utiliza la ruta de acceso al archivo de contenido del paquete (SFT) que se encuentra en el elemento HREF del archivo OSD. Si se usa la ASR, el cliente reemplaza el nombre del servidor (y el puerto y el protocolo, si se usan) en el elemento HREF con la ruta de acceso al servidor IIS que se especifica en la ASR. A continuación, la aplicación se transmite desde el servidor IIS a la caché del cliente mediante el protocolo HTTP (S) y se inicia.

### Para actualizar el paquete

El procedimiento para actualizar el paquete es el siguiente:

-   Copie la nueva versión del archivo OSD a la carpeta de la versión original en la carpeta de contenido del servidor de administración, por ejemplo, \\\\server\\CONTENT\\packagename, y reemplace el archivo OSD existente. Por coherencia, copie también los demás archivos modificados. Si se usan los campos OSR o ISR del cliente, también puede copiar el archivo OSD actualizado y los iconos en el servidor especificado en los campos OSR y ISR.

-   Copie la nueva versión del archivo SFT a la carpeta Package debajo de la carpeta de contenido web en el servidor IIS. por ejemplo, se puede acceder a la dirección URL en el servidor IIS mediante http://IISserver/CONTENT/packagename o https://IISserver/CONTENT/packagename .

En la próxima actualización de publicación, el cliente se actualiza con la nueva versión del archivo OSD. Este archivo señala ahora a la nueva versión del archivo SFT; por lo tanto, cuando el usuario vuelve a hacer doble clic en el icono de una aplicación, se inicia la nueva versión.

## Usar un servidor de administración para publicar y un recurso compartido de archivos para la transmisión por secuencias


En este escenario, el servidor de administración de App-V se usa para publicar los paquetes, y el servidor de archivos se usa para transmitir paquetes y aplicaciones. Cuando se importa el paquete original al servidor de administración, el administrador copia la carpeta del paquete que contiene los archivos creados por el secuenciador a la carpeta de contenido, por ejemplo, a \\\\server\\CONTENT\\packagename. El administrador modifica la entrada HREF en el archivo OSD para que señale al archivo SFT en el servidor de archivos e importa el paquete al servidor de administración.

Para configurar el servidor de archivos para la transmisión por secuencias, el administrador copia la carpeta del paquete desde el servidor de administración a la carpeta de contenido en el servidor de archivos. Esta carpeta debe tener el mismo nombre y ruta de acceso relativa bajo la carpeta de contenido del servidor de archivos que en el servidor de administración, por ejemplo \\\\fileserver\\CONTENT\\packagename.

Si la configuración raíz de origen de la aplicación del cliente (ASR) está configurada para apuntar al servidor de archivos mediante una ruta de acceso UNC, por ejemplo \\\\fileserver\\content, el cliente usa esta configuración en lugar del nombre del servidor en la entrada HREF del archivo OSD. El administrador puede configurar, de forma opcional, los campos ISR y OSR en el cliente para que señalen al servidor de administración o al servidor de archivos, en función de la arquitectura de sistema específica que se use.

Cuando el servidor de administración autentica al usuario, el servidor publica las aplicaciones del usuario enviando el archivo de applist.xml al cliente. El cliente recupera los iconos y archivos OSD de las aplicaciones desde el servidor de archivos o el servidor de administración, en función de la configuración de los campos ISR y OSR.

Cuando el usuario hace doble clic en el icono de una aplicación, el cliente utiliza la ruta de acceso al archivo de contenido del paquete (SFT) que se encuentra en el elemento HREF del archivo OSD. Si se usa la ASR, el cliente reemplaza el nombre del servidor (y el puerto y el protocolo, si se usan) en el elemento HREF con la ruta de acceso al servidor de archivos especificado en la ASR. A continuación, la aplicación se transmite desde el servidor de archivos a la caché del cliente y se inicia.

### Para actualizar el paquete

El procedimiento para actualizar el paquete es el siguiente:

-   Copie la nueva versión del archivo OSD a la carpeta de la versión original en la carpeta de contenido del servidor de administración, por ejemplo, \\\\server\\CONTENT\\packagename, reemplazando el archivo OSD existente. Cualquier otro archivo modificado debe copiarse también por coherencia. Si se usan los campos OSR o ISR del cliente, también puede copiar el archivo OSD actualizado y los iconos en el servidor especificado en los campos OSR y ISR.

-   Copie la nueva versión del archivo SFT a la carpeta Package en la carpeta de contenido en el servidor de archivos, por ejemplo \\\\fileserver\\CONTENT\\packagename. Copie el archivo SFT de V2 a la carpeta del recurso compartido de contenido en el servidor de archivos, por ejemplo, \\\\fileserver\\CONTENT\\packagename\\V1.

En la próxima actualización de publicación, el cliente se actualiza con la nueva versión del archivo OSD. Este archivo apunta a la nueva versión del archivo SFT, de modo que cuando el usuario vuelve a hacer doble clic en el icono de una aplicación, se inicia la nueva versión.

## Actualizar el paquete con el modo de transmisión por secuencias de MSI


Cuando se genera un archivo de Windows Installer (MSI) durante la secuenciación de un paquete, el secuenciador crea una. Archivo MSI que contiene toda la información de publicación necesaria. El administrador debe copiar el. MSI al cliente y el archivo. SFT archivo que contiene el contenido del paquete a un recurso compartido de red accesible por el equipo cliente.

Para publicar la aplicación en el cliente, ejecute el siguiente comando en el equipo cliente:

   **Msiexec.exe/i \\\\PathToMsi\\packagename.msi MODE = STREAMing OVERRIDEURL = \\\\\\\\server\\share\\package.SFT**

Los. MSI publica las aplicaciones en el cliente y, a continuación, transmite el archivo. SFT a la caché del cliente.

### Para actualizar el paquete

Para agregar una nueva versión, un administrador debe implementar un nuevo. MSI al cliente y un nuevo archivo. SFT al recurso compartido de red. Después, el administrador debe ejecutar el mismo comando usado para implementar el paquete, pero usar el nuevo. MSI y el nuevo archivo. SFT, por ejemplo:

   **Msiexec.exe/i \\\\PathToMsi\\packagename\_2.msi MODE = STREAMing OVERRIDEURL = \\\\\\\\server\\share\\package\_2.SFT**

 

 





