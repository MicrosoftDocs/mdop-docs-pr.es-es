---
title: Acerca del secuenciador de virtualización de aplicaciones
description: Acerca del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: bee193ca-58bd-40c9-b41a-310435633895
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 83709bcceabe3312fba34512b47d28a24b4dc52c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820000"
---
# Acerca del secuenciador de virtualización de aplicaciones


El secuenciador de Microsoft Application Virtualization (App-V) supervisa y registra todos los procesos de instalación y configuración de una aplicación y crea los siguientes archivos: **ICO**, **OSD**, **SFT**y **SPRJ**. Estos archivos contienen toda la información necesaria sobre una aplicación para que la aplicación pueda ejecutarse en un entorno virtual en los equipos de destino. Puede usar el secuenciador de Microsoft Application Virtualization (App-V) para crear aplicaciones virtuales. Después de la secuencia de una aplicación, se puede transmitir a los equipos de destino, o bien los equipos de destino pueden ejecutar la aplicación virtual descargando el contenido del paquete de aplicación virtual y ejecutando la aplicación de forma local.

**Importante**  Para ejecutar un paquete de aplicación virtual, el equipo de destino debe ejecutar la versión adecuada del cliente de App-V.

 

Los paquetes de aplicaciones virtuales se ejecutan en equipos de destino sin interactuar con el sistema operativo subyacente en el equipo de destino, ya que cada aplicación se ejecuta en un entorno virtual y se aísla de otras aplicaciones que se instalan o se ejecutan en el equipo de destino. Este aislamiento puede reducir los conflictos de aplicaciones y puede ayudar a reducir la cantidad requerida de pruebas previas a la implementación de aplicaciones.

## Terminología del secuenciador


<a href="" id="application-virtualization-drive"></a>Unidad de virtualización de aplicaciones  
La unidad de virtualización de aplicaciones es la unidad predeterminada (Q:\) en el equipo de destino desde el que se ejecutan las aplicaciones con secuencias.

<a href="" id="ico-file"></a>Archivo ICO  
El archivo de icono en el escritorio del cliente, que se usa para iniciar una aplicación de secuencia.

<a href="" id="installation-directory"></a>Directorio de instalación  
El directorio usado por el secuenciador para colocar los archivos de instalación durante la instalación.

<a href="" id="open-software-descriptor--osd--file"></a>Archivo descriptor de software (OSD) abierto  
Un archivo basado en XML que indica al cliente de App-V cómo recuperar la aplicación secuenciada del servidor de streaming de App-V y cómo ejecutar la aplicación secuenciada en el entorno virtual.

<a href="" id="package-root-directory"></a>Directorio raíz del paquete  
El directorio en el equipo de secuencia en el que se instalan los archivos para el paquete de aplicación de secuencia. Este directorio también existe prácticamente en el equipo al que se transmitirá una aplicación de secuencia.

<a href="" id="sequenced-application"></a>Aplicación de secuencia  
Una aplicación que ha sido supervisada por el secuenciador, dividida en bloques de características principales y secundarios, transmitida a un equipo de destino que ejecuta el cliente de App-V y ejecuta un entorno virtual.

<a href="" id="sequenced-application-package"></a>Paquete de aplicación de secuencia  
Los archivos que componen una aplicación virtual y permiten que se ejecute una aplicación virtual. Estos archivos se crean después de la secuenciación e incluyen específicamente los archivos **. OSD**, **. SFT**, **. SPRJ**y **. ico** .

<a href="" id="sequencing"></a>128  
El proceso de creación de un paquete de aplicación con el secuenciador de App-V. En este proceso, se supervisa una aplicación, se configuran los métodos abreviados y se crea un paquete de aplicación de secuencia.

<a href="" id="sequencing-computer"></a>Equipo de secuencias  
El equipo utilizado para secuenciar una aplicación.

<a href="" id="virtual-application"></a>Aplicación virtual  
Una aplicación empaquetada por el secuenciador para que se ejecute en un entorno virtual independiente. El entorno virtual contiene la información necesaria para ejecutar la aplicación en el cliente sin instalar la aplicación de forma local.

<a href="" id="primary-feature-block"></a>Bloque de características principal  
El contenido mínimo en un paquete de aplicación virtual que es necesario para que una aplicación se ejecute en un equipo de destino. El contenido del bloque de características principal se identifica durante la fase de aplicación de las secuencias y generalmente consta del contenido de las características de aplicación más usadas.

## <a href="" id="sequencing-applications-"></a>Aplicaciones de secuencias


Existen dos métodos para crear y modificar paquetes de aplicaciones virtuales en su entorno. El primer método es mediante el Asistente para **secuenciación** . El Asistente para la **secuenciación** le permite crear nuevos o modificar paquetes de aplicaciones virtuales existentes. Para obtener más información sobre cómo usar el Asistente para **secuenciación** , vea [Cómo secuenciar una nueva aplicación](how-to-sequence-a-new-application.md). El segundo método es usando la línea de comandos. La línea de comandos le permite crear o modificar paquetes de aplicaciones virtuales existentes mediante el símbolo del sistema. Para obtener más información sobre cómo usar la línea de comandos, consulte [Cómo administrar aplicaciones virtuales mediante la línea de comandos](how-to-manage-virtual-applications-using-the-command-line.md).

El Asistente para la **secuenciación** proporciona las siguientes funciones para crear paquetes de aplicaciones virtuales:

1.  **Configuración del paquete**: el Asistente para **secuenciación** solicita la información de configuración del paquete necesaria para completar el archivo descriptor de software abierto (OSD), que es un archivo necesario para iniciar un paquete de aplicación de secuencia.

2.  **Instalación de aplicaciones**: el Asistente para **secuenciación** recopila información sobre la instalación y la configuración de inicio de una aplicación. Supervisa y registra la información de instalación e inicio asociada a la aplicación para crear los archivos necesarios para un paquete de aplicaciones virtual.

3.  **Inicio**de la aplicación: el Asistente para **secuenciación** recopila información para compilar y ordenar los bloques de código necesarios para realizar el inicio inicial del paquete de la aplicación secuenciada en el equipo de destino. La compilación del bloque de código se conoce como el bloque de características principal.

## Consideraciones de seguridad del transordeno de Application Virtualization


El secuenciador de App-V ejecuta todos los servicios detectados en el momento de la secuenciación con la cuenta del sistema local y no aplica los descriptores de seguridad en las solicitudes de control de servicio. Si el servicio se instaló con una cuenta de usuario diferente o si los descriptores de seguridad están diseñados para conceder a diferentes grupos de usuarios permisos de servicio específicos, considere detenidamente si el servicio debe virtualizarse. En algunos casos, debe instalar el servicio localmente para asegurarse de que se mantiene la seguridad de los servicios previstas.

**Importante**  Siempre debes guardar paquetes de aplicaciones virtuales en un lugar seguro.

 

## Temas relacionados


[Información general sobre el secuenciador de virtualización de aplicaciones](application-virtualization-sequencer-overview.md)

 

 





