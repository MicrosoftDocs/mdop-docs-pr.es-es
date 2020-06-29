---
title: Configuración de certificados para admitir el servidor de administración de App-V o el servidor de streaming
description: Configuración de certificados para admitir el servidor de administración de App-V o el servidor de streaming
author: dansimp
ms.assetid: 2f24e550-585e-4b7e-b486-22a3f181f543
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e537244b24d7303af550b3ced8286ba2680009e7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821900"
---
# <span data-ttu-id="6479c-103">Configuración de certificados para admitir el servidor de administración de App-V o el servidor de streaming</span><span class="sxs-lookup"><span data-stu-id="6479c-103">Configuring Certificates to Support App-V Management Server or Streaming Server</span></span>


<span data-ttu-id="6479c-104">Después de completar el proceso de aprovisionamiento de certificados y cambiar los permisos de clave privada para admitir la instalación de App-V, puede iniciar la configuración del servidor de administración o del servidor de streaming.</span><span class="sxs-lookup"><span data-stu-id="6479c-104">After you complete the certificate provisioning process and change the private key permissions to support the App-V installation, you can launch the setup of the Management Server or the Streaming Server.</span></span> <span data-ttu-id="6479c-105">Durante la configuración, si se aprovisiona un certificado antes de ejecutar el programa de instalación, el asistente muestra el certificado en la pantalla **modo de seguridad de conexión** y, de forma predeterminada, la casilla **usar seguridad mejorada** está activada.</span><span class="sxs-lookup"><span data-stu-id="6479c-105">During setup, if a certificate is provisioned before running the setup program, the wizard displays the certificate in the **Connection Security Mode** screen and, by default, the **Use enhanced security** check box is selected.</span></span>

<span data-ttu-id="6479c-106">**Nota:**  Seleccione el certificado que se configuró para App-V si hay más de un certificado aprovisionado para este servidor.</span><span class="sxs-lookup"><span data-stu-id="6479c-106">**Note** Select the certificate that was configured for App-V if there is more than one certificate provisioned for this server.</span></span>

 

<span data-ttu-id="6479c-107">**Importante**  Al actualizar de la versión 4,2 a la 4,5, la configuración tiene una opción para **usar seguridad mejorada**. sin embargo, si selecciona esta opción, no se deshabilitará la transmisión por RTSP.</span><span class="sxs-lookup"><span data-stu-id="6479c-107">**Important** When upgrading from version 4.2 to version 4.5, the setup has an option for **Use enhanced security**; however, selecting this option will not disable streaming over RTSP.</span></span> <span data-ttu-id="6479c-108">Debe usar la consola de administración para deshabilitar RTSP después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="6479c-108">You must use the Management Console to disable RTSP after installation.</span></span>

 

<span data-ttu-id="6479c-109">Seleccione el puerto TCP que usará el servicio para las comunicaciones de cliente.</span><span class="sxs-lookup"><span data-stu-id="6479c-109">Select the TCP port that the service will use for client communications.</span></span> <span data-ttu-id="6479c-110">El puerto predeterminado es TCP 322; sin embargo, puede cambiar el puerto a un puerto personalizado para su entorno.</span><span class="sxs-lookup"><span data-stu-id="6479c-110">The default port is TCP 322; however, you can change the port to a custom port for your environment.</span></span>

<span data-ttu-id="6479c-111">Los pasos restantes del asistente son los mismos que si estuviera implementando un servidor de administración o streaming de App-V sin usar la característica de **seguridad mejorada** .</span><span class="sxs-lookup"><span data-stu-id="6479c-111">The remaining steps of the wizard are the same as if you were deploying an App-V Management or Streaming Server without using the **Enhanced security** feature.</span></span>

## <span data-ttu-id="6479c-112">Configuración de certificados para entornos NLB</span><span class="sxs-lookup"><span data-stu-id="6479c-112">Configuring Certificates for NLB Environments</span></span>


<span data-ttu-id="6479c-113">Para admitir grandes empresas, a menudo el servidor de administración se coloca en un clúster de equilibrio de carga en la red (NLB) para admitir el gran número de conexiones.</span><span class="sxs-lookup"><span data-stu-id="6479c-113">To support large enterprises, often the Management Server is placed into a Network Load Balancing (NLB) cluster to support the large number of connections.</span></span> <span data-ttu-id="6479c-114">Esto requiere al menos dos servidores de administración que parecen ser un único servidor de administración.</span><span class="sxs-lookup"><span data-stu-id="6479c-114">This requires at least two Management Servers that appear to be a single Management Server.</span></span> <span data-ttu-id="6479c-115">Cuando su entorno usa un clúster NLB con varios servidores de administración, necesita una configuración avanzada del certificado que se usa para el clúster NLB.</span><span class="sxs-lookup"><span data-stu-id="6479c-115">When your environment uses an NLB cluster with several Management Servers, you need an advanced configuration of the certificate used for the NLB cluster.</span></span>

<span data-ttu-id="6479c-116">El certificado de App-V se envía a una entidad de certificación (CA) que está configurada en un equipo con Windows Server2003.</span><span class="sxs-lookup"><span data-stu-id="6479c-116">The App-V certificate is submitted to a certification authority (CA) that is configured on a computer running Windows Server2003.</span></span> <span data-ttu-id="6479c-117">El SAN le permite conectarse a un nombre de host de clúster NLB de servidor de administración específico mediante un nombre de sistema de nombres de dominio (DNS) que puede diferir de los nombres reales de los equipos, porque puede haber hasta 32 servidores que componen el clúster NLB.</span><span class="sxs-lookup"><span data-stu-id="6479c-117">The SAN lets you connect to a specific Management Server NLB cluster host name by using a Domain Name System (DNS) name that might differ from the actual computer names, because there can be up to 32 servers that comprise the NLB cluster.</span></span>

<span data-ttu-id="6479c-118">Esta configuración solo es necesaria cuando se usa un clúster NLB.</span><span class="sxs-lookup"><span data-stu-id="6479c-118">This configuration is necessary only when using an NLB cluster.</span></span> <span data-ttu-id="6479c-119">Cuando el cliente se conecte al servidor, se conectará usando el nombre de dominio completo (FQDN) del clúster NLB y no el FQDN de un servidor individual.</span><span class="sxs-lookup"><span data-stu-id="6479c-119">When the client connects to the server, it will connect using the fully qualified domain name (FQDN) of the NLB cluster and not the FQDN of an individual server.</span></span> <span data-ttu-id="6479c-120">Si no agrega la propiedad SAN con el FQDN de los nodos del servidor en el clúster, se rechazan todas las conexiones de cliente porque el nombre común del certificado no coincide con el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="6479c-120">If you do not add the SAN property with the FQDN of the server nodes in the cluster, all client connections are refused because the common name of the certificate won’t match the server name.</span></span>

<span data-ttu-id="6479c-121">Para obtener información más detallada sobre la configuración de certificados con el atributo SAN, consulte <https://go.microsoft.com/fwlink/?LinkId=133228> .</span><span class="sxs-lookup"><span data-stu-id="6479c-121">For more detailed information about configuring certificates with the SAN attribute, see <https://go.microsoft.com/fwlink/?LinkId=133228>.</span></span>

## <span data-ttu-id="6479c-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6479c-122">Related topics</span></span>


[<span data-ttu-id="6479c-123">Configuración de certificados para admitir streaming seguro</span><span class="sxs-lookup"><span data-stu-id="6479c-123">Configuring Certificates to Support Secure Streaming</span></span>](configuring-certificates-to-support-secure-streaming.md)

[<span data-ttu-id="6479c-124">Cómo modificar los permisos de la clave privada al servidor de administración de soporte técnico o servidor de streaming</span><span class="sxs-lookup"><span data-stu-id="6479c-124">How to Modify Private Key Permissions to Support Management Server or Streaming Server</span></span>](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





