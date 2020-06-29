---
title: Introducción a la seguridad y la protección
description: Introducción a la seguridad y la protección
author: dansimp
ms.assetid: a43e1c53-7936-4d48-a110-0be26c8e9d97
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b08b7dcb3defa8a01a4fd8a3e7234b5ac2956c4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815660"
---
# Introducción a la seguridad y la protección


Microsoft Application Virtualization 4.5 ofrece las siguientes características de seguridad mejoradas para ayudarle a planear e implementar una estrategia de implementación más segura:

-   La virtualización de aplicaciones ahora es compatible con la seguridad de la capa de transporte (TLS) mediante los certificados X. 509 V3. Siempre que se haya suministrado un certificado de servidor a la administración de virtualización de aplicaciones planeada o al servidor de streaming, la instalación se hará segura con el protocolo de RTSPs en el puerto 322. El uso de RTSPs garantiza que la comunicación entre los servidores de virtualización de aplicaciones y los clientes de virtualización de aplicaciones se haya firmado y cifrado. Si no se asigna ningún certificado al servidor durante la instalación de Application Virtualization Server, la comunicación se establecerá en RTSP en el puerto 554.

    **Nota de seguridad:**

    Para ayudar a proporcionar una configuración segura del servidor, debe asegurarse de que los puertos RTSP estén deshabilitados incluso si tiene todos los paquetes configurados para usar RTSPs.

    Si agrega certificados de seguridad al servidor después de instalar el servidor, es posible que el servidor no detecte los certificados. Para ayudar a garantizar la detección de certificados de seguridad, reinicie el servidor después de agregar los certificados.

-   El cliente debe estar configurado para usar el mismo protocolo y puerto que el servidor, o bien no podrá comunicarse con el servidor. El cliente también debe confiar en el emisor del certificado y se suministra con varios de los proveedores principales de su almacenamiento raíz de confianza. Puede usar certificados autofirmados, pero tendrá que actualizar los clientes.

-   Al configurar los servidores IIS para usar el protocolo HTTPS para la transmisión por secuencias, necesitará configurar la capa de sockets seguros (SSL) en el servidor IIS y aprovisionar el certificado para el servidor. Los clientes también tendrán que estar configurados para confiar en la entidad emisora de certificados raíz que emitió el certificado de servidor.

-   Se ha agregado la autenticación Kerberos a Microsoft Application Virtualization como mecanismo de autenticación predeterminado. Las versiones anteriores se basaban en NTLM v2 para la autenticación. El uso de la autenticación Kerberos refuerza la seguridad de la comunicación entre el cliente y el servidor de virtualización de aplicaciones. Cuando se inicia una conexión desde el cliente, el servidor de Application Virtualization comprueba el vale de sesión con el centro de distribución de claves (KDC).

-   Gracias a la compatibilidad para usar certificados de servidor y el uso de los protocolos RTSPs o HTTPS, ahora puede admitir clientes fuera de la red corporativa. Esto puede ayudar a eliminar la necesidad de que los usuarios móviles establezcan una conexión segura a la red corporativa (VPN, RAS, etc.) antes de iniciar aplicaciones de aprovisionamiento de Application Virtualization.

Otras consideraciones de seguridad importantes que debe tener en cuenta son las siguientes:

-   Mantenga siempre los servidores totalmente actualizados y protegidos.

-   Para agregar un certificado y habilitar comunicaciones más seguras para el servidor de administración de virtualización de aplicaciones, deben cumplirse los criterios siguientes:

    -   El usuario que va a agregar el certificado debe ser un administrador en el servidor donde se encuentra el almacén de certificados.

    -   Debe iniciarse el servicio servidor.

    -   El puerto 139 en el servidor de administración debe estar abierto a la server'sIP de servicio Web.

-   Use listas de control de acceso (ACL) para asegurarse de que los paquetes de la aplicación y todos los archivos del paquete estén protegidos y no se puedan manipular. Las ACL restringen el acceso a la ubicación o carpeta donde se almacenan los paquetes, lo que permite el acceso únicamente a determinadas cuentas.

-   Asegúrese de que el canal entre el servidor de administración de virtualización de aplicaciones y la base de datos está protegido, por ejemplo, mediante IPsec.

-   Si los paquetes se almacenan en un SAN o NAS, asegúrese de que la conexión entre el dispositivo de almacenamiento central y los servidores de virtualización de la aplicación está protegida.

-   Deben protegerse todos los canales de comunicación para el cliente, incluidas las conexiones al servidor de publicación, el servidor de virtualización de aplicaciones y la ruta de acceso a los archivos OSD o ICO, mediante un protocolo como HTTPS o IPsec. 

-   Los permisos de cliente deben configurarse para ayudar a garantizar que los usuarios no puedan manipular los paquetes. Es muy importante que no otorgue a los usuarios permiso para agregar o actualizar paquetes en sistemas, como los servidores de host de sesión de escritorio remoto (host RDSession), que se comparten con varios usuarios.

-   Para que la consola de administración de servidores funcione correctamente, es necesario permitir la autenticación Kerberos en entornos de dominio o de bosque.

-   Esta versión del software no admite el hospedaje de un servidor RTSP basado en Kerberos y un servidor IIS basado en NTLM de Microsoft en el mismo equipo. Para hospedar un servidor RTSP y un servidor IIS en el mismo equipo, quite el SPN del servidor IIS y use la autenticación NTLM.

## Temas relacionados


[Planificación de la implementación del sistema de virtualización de aplicaciones](planning-for-application-virtualization-system-deployment.md)

 

 





