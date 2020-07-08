---
title: Planificación de seguridad del servidor
description: Planificación de seguridad del servidor
author: dansimp
ms.assetid: c7cd8227-b359-41e7-a8ae-d0d5718a76a2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9bea1bd8287a15385200bbfb425ed8e00fbcdb02
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815901"
---
# Planificación de seguridad del servidor


Para mejorar la seguridad de un entorno, debe consultar la exposición a cualquier amenaza potencial en el entorno. Proporcionar seguridad para una infraestructura de App-V requiere el uso de las características de seguridad de App-V específicas, así como de las prácticas de seguridad y características de la infraestructura subyacente. La protección de la infraestructura subyacente de servicios como servicios de Internet Information Server (IIS), servicios de dominio de Active Directory y SQL Server mejorará la seguridad general del sistema de App-V.

La configuración predeterminada de la instalación del servidor proporciona los niveles más altos de seguridad. Sin embargo, algunos de los componentes se basan en la infraestructura subyacente que no está configurada como parte de la instalación. El seguimiento de los pasos posteriores a la instalación mejorará la seguridad de la infraestructura de App-V.

El directorio de contenido contiene todos los paquetes que deben transmitirse a los clientes. Estos recursos deben ser tan seguros como sea posible para eliminar muchas amenazas de seguridad posibles. La siguiente lista ofrece instrucciones adicionales:

-   Publicación basada en UNC y/o streaming: los permisos de este elemento deben ser los más restrictivos en el entorno. Use permisos NTFS para implementar las listas de control de acceso (ACL) más restrictivas para el directorio de contenido (users = Read, Administrators = Read and write).

-   IIS usado para publicar o transmitir por secuencias: configurar IIS para admitir solo la autenticación integrada de Windows. Quitar el acceso anónimo al servidor IIS y restringir el acceso al directorio con permisos NTFS.

-   RTSP/RTSPs para transmitir paquetes de aplicaciones: configure la Directiva de proveedor de App-V para requerir la autenticación, exigir permisos de acceso y habilitar solo los grupos necesarios para que tengan acceso a la Directiva de proveedor. Configure las aplicaciones con los permisos adecuados en la base de datos.

Mantenga al mínimo el número de usuarios con privilegios administrativos para reducir posibles amenazas a los datos del almacén de datos y evitar la publicación de aplicaciones malintencionadas en la infraestructura.

## Seguridad de la virtualización de aplicaciones


App-V usa varios métodos de comunicación entre los distintos componentes de la infraestructura. Al planear la infraestructura de App-V, la protección de las comunicaciones entre los servidores puede reducir los riesgos de seguridad que ya podrían existir en la red existente.

### Almacén de datos

El servidor de administración de virtualización de aplicaciones y el servicio de administración de virtualización de aplicaciones se comunican con el almacén de datos mediante una conexión SQL a través del puerto TCP 1433. El servidor de administración usa el almacén de datos para recuperar los datos de la aplicación y de configuración, y escribe la información de uso en la base de datos. El servicio de administración se comunica con el almacén de datos en nombre de un administrador que está configurando la infraestructura de App-V. Debido a que el almacén de datos contiene información importante, es importante minimizar las amenazas a estos datos.

Se recomienda que las comunicaciones entre el servidor de administración de App-V, el servicio de administración y el almacén de datos estén protegidos con la seguridad del Protocolo de Internet (IPsec). En concreto, cree directivas que protejan el canal de comunicación entre el almacén de datos (SQL) y el servidor de administración y el almacén de datos y el servicio de administración. También puede implementar el aislamiento de servidor y dominio con IPsec, lo que garantiza que todos los componentes de la infraestructura de App-V se comuniquen solo con canales seguros. Para obtener información sobre cómo implementar IPsec, consulte la siguiente documentación:

-   Para Windows Server2003, consulte <https://go.microsoft.com/fwlink/?LinkId=133226> ( https://go.microsoft.com/fwlink/?LinkId=133226) .

-   Para Windows Server2008, consulte <https://go.microsoft.com/fwlink/?LinkId=133227> ( https://go.microsoft.com/fwlink/?LinkId=133227) .

### Directorio de contenido

La instalación de App-V Management Server configura una ubicación para el directorio de contenido. Este directorio es la ubicación de almacenamiento de los paquetes de aplicaciones virtualizadas. Esta ubicación puede ser local para el servidor o puede colocarse en un recurso compartido de red remoto. Por lo tanto, implemente IPsec para ayudar a proteger la comunicación con una ubicación remota del directorio de contenido.

También puede usar un directorio virtual en un servidor IIS para transmitir paquetes a los clientes. Si el directorio virtual que se crea para el contenido se encuentra en un origen remoto, use IPsec para ayudar a proteger la comunicación entre el servidor IIS y la ubicación de almacenamiento remoto.

El directorio de contenido contiene todos los paquetes que se transmiten a los clientes. Estos recursos deben ser tan seguros como sea posible para eliminar muchas amenazas de seguridad posibles.

### Protocolos de seguridad

Puede usar RTSPs o HTTPS para mejorar las comunicaciones seguras. RTSPs es el protocolo que usan los servidores de App-V y HTTPS es el protocolo que usan los servidores IIS. Estos protocolos se usan al publicar aplicaciones desde el servidor en el cliente de escritorio de virtualización de aplicaciones. Después de determinar el protocolo que desea, agregue un servidor de publicación que use ese protocolo.

### <a href="" id="configuring-app-v-servers-for-rtsps-"></a>Configuración de servidores de App-V para RTSPs

La instalación o configuración de un servidor de administración de App-V o de un servidor de streaming para usar la seguridad mejorada (por ejemplo, TLS) requiere que se aprovisione un certificado X. 509 V3 en el servidor de App-V. Al prepararse para instalar o configurar la seguridad de un servidor, debe cumplir con algunos requisitos específicos. Los requisitos técnicos para implementar y configurar certificados para un servidor de administración de aplicaciones-V o de streaming más seguro incluyen lo siguiente:

-   El certificado debe ser válido. En caso contrario, el cliente finaliza la conexión.

-   El certificado debe contener el uso de clave mejorada (EKU) correcto: autenticación de servidor (OID 1.3.6.1.5.5.7.3.1). En caso contrario, el cliente finaliza la conexión.

-   El nombre de dominio completo (FQDN) del certificado debe coincidir con el servidor en el que está instalado. Por ejemplo, si el cliente llama `RTSPS://Myserver.mycompany.com/content/MyApp.sft` , pero el certificado **emitido para** el campo contiene `Myserver1.mycompany.com` , el cliente no se conectará al servidor y la sesión finalizará, aunque `Myserver.mycompany.com` y se `Myserver1.mycompany.com` resuelva a la misma dirección IP.

    **Nota:**  Si usa App-V en un clúster con equilibrio de carga de red, el certificado debe estar configurado con *Nombres alternativos de asunto* (San) para admitir rtsps. Para obtener información acerca de la configuración de la entidad emisora de certificados (CA) y la creación de certificados con redes SAN, consulte <https://go.microsoft.com/fwlink/?LinkId=133228> ( https://go.microsoft.com/fwlink/?LinkId=133228) .

     

-   La CA que emite el certificado al servidor de App-V debe ser de confianza para el cliente que se conecta al servidor. En caso contrario, el cliente finaliza la conexión.

-   Debe cambiar los permisos de la *clave privada del certificado* para habilitar el acceso mediante el servicio Server App-V. De forma predeterminada, el servidor de administración de App-V y los servicios del servidor de streaming se ejecutan bajo la cuenta servicio de red. Cuando se genera un #10 PKCS \ en el servidor, se crea una clave privada. Solo los grupos sistema local y administradores tienen acceso a esta clave. Estas ACL predeterminadas evitan que el servidor de App-V acepte conexiones seguras.

    **Nota:**  Para obtener información sobre la configuración de una infraestructura de clave pública (PKI), consulte <https://go.microsoft.com/fwlink/?LinkId=133229> ( https://go.microsoft.com/fwlink/?LinkId=133229) .

     

### Configurar servidores IIS con HTTPS

Es posible que App-V use servidores IIS en ciertas configuraciones de infraestructura. Para obtener más información sobre cómo configurar los servidores IIS, consulte <https://go.microsoft.com/fwlink/?LinkId=133230> ( https://go.microsoft.com/fwlink/?LinkId=133230) .

**Nota:**  Si está usando IIS para publicar los archivos ICO y OSD, configure un tipo MIME para OSD = TXT; de lo contrario, IIS no podrá ofrecer los archivos ICO y OSD a los clientes.

 

### Seguridad de nivel de aplicación

Puede configurar los servidores para transmitir aplicaciones específicas al escritorio de un usuario. Sin embargo, el permiso de acceso realmente se concede en el nivel de paquete, no en el nivel de aplicación. Aunque una aplicación específica podría no publicarse en el escritorio del usuario, si el usuario tiene permiso para agregar aplicaciones o si es un administrador en el equipo cliente, el usuario puede crear y usar un acceso directo en el cliente para ejecutar todas las aplicaciones de un paquete.

## Configuración de administración de App-V para entorno distribuido


Al diseñar la infraestructura de su organización específica, puede instalar el servicio Web de administración de App-V en un equipo que no sea el equipo en el que instala el servidor de administración de App-V. Algunas de las razones comunes para separar estos componentes de App-V son las siguientes:

-   Rendimiento

-   Confiabilidad

-   Disponibilidad

-   Escalabilidad

Para que la infraestructura funcione correctamente, separar la consola de administración de App-V, el servidor de administración y el servicio Web de administración requieren una configuración adicional. Para obtener información detallada sobre cómo configurar el servidor, consulte [Cómo configurar el servidor para que sea de confianza para la delegación](how-to-configure-the-server-to-be-trusted-for-delegation.md).

## Temas relacionados


[Planificación de seguridad y protección](planning-for-security-and-protection.md)

 

 





