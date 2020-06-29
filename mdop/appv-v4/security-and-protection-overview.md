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
# <span data-ttu-id="5d560-103">Introducción a la seguridad y la protección</span><span class="sxs-lookup"><span data-stu-id="5d560-103">Security and Protection Overview</span></span>


<span data-ttu-id="5d560-104">Microsoft Application Virtualization 4.5 ofrece las siguientes características de seguridad mejoradas para ayudarle a planear e implementar una estrategia de implementación más segura:</span><span class="sxs-lookup"><span data-stu-id="5d560-104">Microsoft Application Virtualization4.5 provides the following enhanced security features to help you plan and implement a more secure deployment strategy:</span></span>

-   <span data-ttu-id="5d560-105">La virtualización de aplicaciones ahora es compatible con la seguridad de la capa de transporte (TLS) mediante los certificados X. 509 V3.</span><span class="sxs-lookup"><span data-stu-id="5d560-105">Application Virtualization now supports Transport Layer Security (TLS) using X.509 V3 certificates.</span></span> <span data-ttu-id="5d560-106">Siempre que se haya suministrado un certificado de servidor a la administración de virtualización de aplicaciones planeada o al servidor de streaming, la instalación se hará segura con el protocolo de RTSPs en el puerto 322.</span><span class="sxs-lookup"><span data-stu-id="5d560-106">Provided that a server certificate has been provisioned to the planned Application Virtualization Management or Streaming Server, the installation will default to secure, using the RTSPS protocol over port 322.</span></span> <span data-ttu-id="5d560-107">El uso de RTSPs garantiza que la comunicación entre los servidores de virtualización de aplicaciones y los clientes de virtualización de aplicaciones se haya firmado y cifrado.</span><span class="sxs-lookup"><span data-stu-id="5d560-107">Using RTSPS ensures that communication between the Application Virtualization Servers and the Application Virtualization Clients is signed and encrypted.</span></span> <span data-ttu-id="5d560-108">Si no se asigna ningún certificado al servidor durante la instalación de Application Virtualization Server, la comunicación se establecerá en RTSP en el puerto 554.</span><span class="sxs-lookup"><span data-stu-id="5d560-108">If no certificate is assigned to the server during the Application Virtualization Server installation, the communication will be set to RTSP over port 554.</span></span>

    **<span data-ttu-id="5d560-109">Nota de seguridad:</span><span class="sxs-lookup"><span data-stu-id="5d560-109">Security Note:</span></span>**

    <span data-ttu-id="5d560-110">Para ayudar a proporcionar una configuración segura del servidor, debe asegurarse de que los puertos RTSP estén deshabilitados incluso si tiene todos los paquetes configurados para usar RTSPs.</span><span class="sxs-lookup"><span data-stu-id="5d560-110">To help provide a secure setup of the server, you must make sure that RTSP ports are disabled even if you have all packages configured to use RTSPS.</span></span>

    <span data-ttu-id="5d560-111">Si agrega certificados de seguridad al servidor después de instalar el servidor, es posible que el servidor no detecte los certificados.</span><span class="sxs-lookup"><span data-stu-id="5d560-111">If you add security certificates to the server after installing the server, the server might not detect the certificates.</span></span> <span data-ttu-id="5d560-112">Para ayudar a garantizar la detección de certificados de seguridad, reinicie el servidor después de agregar los certificados.</span><span class="sxs-lookup"><span data-stu-id="5d560-112">To help ensure security certificate detection, restart the server after adding the certificates.</span></span>

-   <span data-ttu-id="5d560-113">El cliente debe estar configurado para usar el mismo protocolo y puerto que el servidor, o bien no podrá comunicarse con el servidor.</span><span class="sxs-lookup"><span data-stu-id="5d560-113">The client must be configured to use the same protocol and port as the server, or it will not be able to communicate with the server.</span></span> <span data-ttu-id="5d560-114">El cliente también debe confiar en el emisor del certificado y se suministra con varios de los proveedores principales de su almacenamiento raíz de confianza.</span><span class="sxs-lookup"><span data-stu-id="5d560-114">The client must also trust the issuer of the certificate and ships with several of the primary providers in its Trusted Root Store.</span></span> <span data-ttu-id="5d560-115">Puede usar certificados autofirmados, pero tendrá que actualizar los clientes.</span><span class="sxs-lookup"><span data-stu-id="5d560-115">You can use self-signed certificates, but you will need to update the clients.</span></span>

-   <span data-ttu-id="5d560-116">Al configurar los servidores IIS para usar el protocolo HTTPS para la transmisión por secuencias, necesitará configurar la capa de sockets seguros (SSL) en el servidor IIS y aprovisionar el certificado para el servidor.</span><span class="sxs-lookup"><span data-stu-id="5d560-116">When configuring IIS servers to use the HTTPS protocol for streaming, you will need to set up Secure Sockets Layer (SSL) on the IIS server and provision the certificate for the server.</span></span> <span data-ttu-id="5d560-117">Los clientes también tendrán que estar configurados para confiar en la entidad emisora de certificados raíz que emitió el certificado de servidor.</span><span class="sxs-lookup"><span data-stu-id="5d560-117">The clients will also need to be configured to trust the root certification authority that issued the server certificate.</span></span>

-   <span data-ttu-id="5d560-118">Se ha agregado la autenticación Kerberos a Microsoft Application Virtualization como mecanismo de autenticación predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5d560-118">Kerberos authentication has been added to Microsoft Application Virtualization as the default authentication mechanism.</span></span> <span data-ttu-id="5d560-119">Las versiones anteriores se basaban en NTLM v2 para la autenticación.</span><span class="sxs-lookup"><span data-stu-id="5d560-119">Earlier versions relied upon NTLM V2 for authentication.</span></span> <span data-ttu-id="5d560-120">El uso de la autenticación Kerberos refuerza la seguridad de la comunicación entre el cliente y el servidor de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="5d560-120">Using Kerberos Authentication strengthens the security of the communication between the client and the Application Virtualization server.</span></span> <span data-ttu-id="5d560-121">Cuando se inicia una conexión desde el cliente, el servidor de Application Virtualization comprueba el vale de sesión con el centro de distribución de claves (KDC).</span><span class="sxs-lookup"><span data-stu-id="5d560-121">When a connection has been initiated from the client, the Application Virtualization Server verifies the session ticket with the Key Distribution Center (KDC).</span></span>

-   <span data-ttu-id="5d560-122">Gracias a la compatibilidad para usar certificados de servidor y el uso de los protocolos RTSPs o HTTPS, ahora puede admitir clientes fuera de la red corporativa.</span><span class="sxs-lookup"><span data-stu-id="5d560-122">Because of the support for using server certificates and using the RTSPS or HTTPS protocols, you can now support clients outside of the corporate network.</span></span> <span data-ttu-id="5d560-123">Esto puede ayudar a eliminar la necesidad de que los usuarios móviles establezcan una conexión segura a la red corporativa (VPN, RAS, etc.) antes de iniciar aplicaciones de aprovisionamiento de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="5d560-123">This can help eliminate the need for mobile users to set up a secure connection to the corporate network (VPN, RAS, and so on) prior to launching Application Virtualization provisioned applications.</span></span>

<span data-ttu-id="5d560-124">Otras consideraciones de seguridad importantes que debe tener en cuenta son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="5d560-124">Other important security considerations to consider include the following:</span></span>

-   <span data-ttu-id="5d560-125">Mantenga siempre los servidores totalmente actualizados y protegidos.</span><span class="sxs-lookup"><span data-stu-id="5d560-125">Always keep servers fully updated and protected.</span></span>

-   <span data-ttu-id="5d560-126">Para agregar un certificado y habilitar comunicaciones más seguras para el servidor de administración de virtualización de aplicaciones, deben cumplirse los criterios siguientes:</span><span class="sxs-lookup"><span data-stu-id="5d560-126">To add a certificate to enable more secure communications to the Application Virtualization Management Server, the following criteria must be met:</span></span>

    -   <span data-ttu-id="5d560-127">El usuario que va a agregar el certificado debe ser un administrador en el servidor donde se encuentra el almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="5d560-127">The user who will be adding the certificate must be an administrator on the server where the certificate store is located.</span></span>

    -   <span data-ttu-id="5d560-128">Debe iniciarse el servicio servidor.</span><span class="sxs-lookup"><span data-stu-id="5d560-128">The server service must be started.</span></span>

    -   <span data-ttu-id="5d560-129">El puerto 139 en el servidor de administración debe estar abierto a la server'sIP de servicio Web.</span><span class="sxs-lookup"><span data-stu-id="5d560-129">Port 139 on the Management Server must be open to the Web Service server’sIP.</span></span>

-   <span data-ttu-id="5d560-130">Use listas de control de acceso (ACL) para asegurarse de que los paquetes de la aplicación y todos los archivos del paquete estén protegidos y no se puedan manipular.</span><span class="sxs-lookup"><span data-stu-id="5d560-130">Use access control lists (ACLs) to ensure that the application packages and all package files are protected and cannot be tampered.</span></span> <span data-ttu-id="5d560-131">Las ACL restringen el acceso a la ubicación o carpeta donde se almacenan los paquetes, lo que permite el acceso únicamente a determinadas cuentas.</span><span class="sxs-lookup"><span data-stu-id="5d560-131">ACLs restrict access to the location or folder where you store the packages, allowing access only to certain accounts.</span></span>

-   <span data-ttu-id="5d560-132">Asegúrese de que el canal entre el servidor de administración de virtualización de aplicaciones y la base de datos está protegido, por ejemplo, mediante IPsec.</span><span class="sxs-lookup"><span data-stu-id="5d560-132">Make sure that the channel between the Application Virtualization Management Server and the database is secured—for example, by using IPsec.</span></span>

-   <span data-ttu-id="5d560-133">Si los paquetes se almacenan en un SAN o NAS, asegúrese de que la conexión entre el dispositivo de almacenamiento central y los servidores de virtualización de la aplicación está protegida.</span><span class="sxs-lookup"><span data-stu-id="5d560-133">If packages are stored on a SAN or NAS, ensure the connection between the central storage device and the Application Virtualization Servers is protected.</span></span>

-   <span data-ttu-id="5d560-134">Deben protegerse todos los canales de comunicación para el cliente, incluidas las conexiones al servidor de publicación, el servidor de virtualización de aplicaciones y la ruta de acceso a los archivos OSD o ICO, mediante un protocolo como HTTPS o IPsec.</span><span class="sxs-lookup"><span data-stu-id="5d560-134">All communication channels to the client should be protected—including connections to the publishing server, the Application Virtualization Server, and the path to the OSD and ICO files—by using a protocol such as HTTPS or IPsec.</span></span> 

-   <span data-ttu-id="5d560-135">Los permisos de cliente deben configurarse para ayudar a garantizar que los usuarios no puedan manipular los paquetes.</span><span class="sxs-lookup"><span data-stu-id="5d560-135">Client permissions should be configured to help ensure that packages cannot be tampered with by users.</span></span> <span data-ttu-id="5d560-136">Es muy importante que no otorgue a los usuarios permiso para agregar o actualizar paquetes en sistemas, como los servidores de host de sesión de escritorio remoto (host RDSession), que se comparten con varios usuarios.</span><span class="sxs-lookup"><span data-stu-id="5d560-136">It is especially important that you do not grant users permission to add or update packages on systems, such as Remote Desktop Session Host (RDSession Host) servers, that are shared with multiple users.</span></span>

-   <span data-ttu-id="5d560-137">Para que la consola de administración de servidores funcione correctamente, es necesario permitir la autenticación Kerberos en entornos de dominio o de bosque.</span><span class="sxs-lookup"><span data-stu-id="5d560-137">Kerberos authentication must be permitted across domain or forest environments for the Server Management Console to work correctly.</span></span>

-   <span data-ttu-id="5d560-138">Esta versión del software no admite el hospedaje de un servidor RTSP basado en Kerberos y un servidor IIS basado en NTLM de Microsoft en el mismo equipo.</span><span class="sxs-lookup"><span data-stu-id="5d560-138">This release of the software does not support hosting a Kerberos-based RTSP server and a Microsoft NTLM-only-based IIS server on the same computer.</span></span> <span data-ttu-id="5d560-139">Para hospedar un servidor RTSP y un servidor IIS en el mismo equipo, quite el SPN del servidor IIS y use la autenticación NTLM.</span><span class="sxs-lookup"><span data-stu-id="5d560-139">To host an RTSP server and an IIS server on the same computer, remove the SPN from the IIS server and use NTLM authentication.</span></span>

## <span data-ttu-id="5d560-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d560-140">Related topics</span></span>


[<span data-ttu-id="5d560-141">Planificación de la implementación del sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5d560-141">Planning for Application Virtualization System Deployment</span></span>](planning-for-application-virtualization-system-deployment.md)

 

 





