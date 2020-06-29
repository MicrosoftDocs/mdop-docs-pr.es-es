---
title: Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos
description: Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos
author: dansimp
ms.assetid: 3e3d873f-13d2-402f-97b4-f62d0c399171
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c424f39c8209ca641f6073838ebcb8726acc9e25
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817900"
---
# <span data-ttu-id="96e1b-103">Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="96e1b-103">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>


<span data-ttu-id="96e1b-104">Una vez que el cliente de Application Virtualization (App-V) se ha implementado y configurado durante la instalación mediante la línea de comandos, podría ser necesario cambiar una o más opciones de configuración del cliente.</span><span class="sxs-lookup"><span data-stu-id="96e1b-104">After the Application Virtualization (App-V) Client has been deployed and configured during the installation by using the command line, it might be necessary to change one or more client configuration settings.</span></span> <span data-ttu-id="96e1b-105">Esto se consigue modificando las claves del registro apropiadas, con uno de los siguientes métodos:</span><span class="sxs-lookup"><span data-stu-id="96e1b-105">This is accomplished by editing the appropriate registry keys, using one of the following methods:</span></span>

-   <span data-ttu-id="96e1b-106">Usar el editor del registro directamente</span><span class="sxs-lookup"><span data-stu-id="96e1b-106">Using the Registry Editor directly</span></span>

-   <span data-ttu-id="96e1b-107">Uso de un archivo. reg</span><span class="sxs-lookup"><span data-stu-id="96e1b-107">Using a .reg file</span></span>

-   <span data-ttu-id="96e1b-108">Usar un lenguaje de scripts como VBScript o Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="96e1b-108">Using a scripting language such as VBScript or Windows PowerShell</span></span>

<span data-ttu-id="96e1b-109">También hay una plantilla ADM que puede usar.</span><span class="sxs-lookup"><span data-stu-id="96e1b-109">There is also an ADM template that you can use.</span></span> <span data-ttu-id="96e1b-110">Para obtener más información sobre la plantilla ADM, consulte <https://go.microsoft.com/fwlink/?LinkId=121835> .</span><span class="sxs-lookup"><span data-stu-id="96e1b-110">For more information about the ADM template, see <https://go.microsoft.com/fwlink/?LinkId=121835>.</span></span>

<span data-ttu-id="96e1b-111">**PRECAUCIÓN**  Tenga cuidado cuando edite el registro porque los errores pueden dejar el equipo en un estado inutilizable.</span><span class="sxs-lookup"><span data-stu-id="96e1b-111">**Caution** Use care when you edit the registry because errors can leave the computer in an unusable state.</span></span> <span data-ttu-id="96e1b-112">Asegúrese de seguir las prácticas empresariales estándar que se relacionan con las modificaciones del registro.</span><span class="sxs-lookup"><span data-stu-id="96e1b-112">Be sure to follow your standard business practices that relate to registry edits.</span></span> <span data-ttu-id="96e1b-113">Pruebe minuciosamente todos los cambios propuestos en un entorno de prueba antes de implementarlos en los equipos de producción.</span><span class="sxs-lookup"><span data-stu-id="96e1b-113">Thoroughly test all proposed changes in a test environment before you deploy them to production computers.</span></span>

 

## <span data-ttu-id="96e1b-114">En esta sección</span><span class="sxs-lookup"><span data-stu-id="96e1b-114">In This Section</span></span>


<span data-ttu-id="96e1b-115">**Importante**  En un equipo de 64 bits, las claves y los valores que se describen en las siguientes secciones estarán bajo HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span><span class="sxs-lookup"><span data-stu-id="96e1b-115">**Important** On a 64-bit computer, the keys and values described in the following sections will be under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client.</span></span>

 

<a href="" id="how-to-reset-the-filesystem-cache"></a>[<span data-ttu-id="96e1b-116">Cómo restablecer la caché de sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="96e1b-116">How to Reset the FileSystem Cache</span></span>](how-to-reset-the-filesystem-cache.md)  
<span data-ttu-id="96e1b-117">Proporciona la información necesaria para restablecer la caché del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="96e1b-117">Provides the information that is required to reset the FileSystem cache.</span></span>

<a href="" id="how-to-change-the-size-of-the-filesystem-cache"></a>[<span data-ttu-id="96e1b-118">Cómo cambiar el tamaño de la caché de sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="96e1b-118">How to Change the Size of the FileSystem Cache</span></span>](how-to-change-the-size-of-the-filesystem-cache.md)  
<span data-ttu-id="96e1b-119">Explica cómo se puede cambiar el tamaño de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="96e1b-119">Explains how you can change the size of the cache.</span></span>

<a href="" id="how-to-use-the-cache-space-management-feature"></a>[<span data-ttu-id="96e1b-120">Cómo usar la función de administración de espacio de caché</span><span class="sxs-lookup"><span data-stu-id="96e1b-120">How to Use the Cache Space Management Feature</span></span>](how-to-use-the-cache-space-management-feature.md)  
<span data-ttu-id="96e1b-121">Describe cómo configurar la característica de administración de espacio en caché.</span><span class="sxs-lookup"><span data-stu-id="96e1b-121">Describes how you can configure the cache space management feature.</span></span>

<a href="" id="how-to-configure-the-client-log-file"></a>[<span data-ttu-id="96e1b-122">Cómo configurar el archivo de registro del cliente</span><span class="sxs-lookup"><span data-stu-id="96e1b-122">How to Configure the Client Log File</span></span>](how-to-configure-the-client-log-file.md)  
<span data-ttu-id="96e1b-123">Describe los diversos valores de las claves del registro que controlan el archivo de registro del cliente y cómo se pueden cambiar.</span><span class="sxs-lookup"><span data-stu-id="96e1b-123">Describes the various registry key values that control the client log file and how you can change them.</span></span>

<a href="" id="how-to-configure-user-permissions"></a>[<span data-ttu-id="96e1b-124">Cómo configurar los permisos de usuario</span><span class="sxs-lookup"><span data-stu-id="96e1b-124">How to Configure User Permissions</span></span>](how-to-configure-user-permissions.md)  
<span data-ttu-id="96e1b-125">Identifica la clave del registro que controla los permisos de usuario y proporciona ejemplos de cómo puede cambiar algunos permisos.</span><span class="sxs-lookup"><span data-stu-id="96e1b-125">Identifies the registry key that controls the user permissions and gives examples of how you can change some permissions.</span></span>

<a href="" id="how-to-configure-the-client-for-application-package-retrieval"></a>[<span data-ttu-id="96e1b-126">Cómo configurar al cliente para la recuperación del paquete de aplicación</span><span class="sxs-lookup"><span data-stu-id="96e1b-126">How to Configure the Client for Application Package Retrieval</span></span>](how-to-configure-the-client-for-application-package-retrieval.md)  
<span data-ttu-id="96e1b-127">Explica cómo configurar el cliente para recuperar asociaciones de tipo de archivo, iconos y contenido del paquete de diferentes orígenes, y ofrece varios ejemplos de formato de ruta de acceso correcto.</span><span class="sxs-lookup"><span data-stu-id="96e1b-127">Explains how to configure the client to retrieve package content, icons, and file type associations from different sources, and provides several examples of the correct path format.</span></span>

<a href="" id="how-to-configure-the-client-for-disconnected-operation-mode"></a>[<span data-ttu-id="96e1b-128">Cómo configurar al cliente para el modo de operación desconectado</span><span class="sxs-lookup"><span data-stu-id="96e1b-128">How to Configure the Client for Disconnected Operation Mode</span></span>](how-to-configure-the-client-for-disconnected-operation-mode.md)  
<span data-ttu-id="96e1b-129">Proporciona información sobre cómo configurar las diversas opciones asociadas al modo de operaciones sin conexión.</span><span class="sxs-lookup"><span data-stu-id="96e1b-129">Provides information about how to configure the various settings associated with disconnected operations mode.</span></span>

<a href="" id="how-to-configure-shortcut-and-file-type-association-behavior"></a>[<span data-ttu-id="96e1b-130">Cómo configurar el acceso directo y el comportamiento de las asociaciones de tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="96e1b-130">How to Configure Shortcut and File Type Association Behavior</span></span>](how-to-configure-shortcut-and-file-type-association-behavior-46-only.md)  
<span data-ttu-id="96e1b-131">Describe los valores de la clave del registro que controlan los accesos directos y las asociaciones de tipos de archivo en el cliente de App-V y proporciona detalles sobre cómo configurarlos.</span><span class="sxs-lookup"><span data-stu-id="96e1b-131">Describes the registry key values that control shortcuts and file type associations in the App-V client, and provides details on how to configure them.</span></span>

## <span data-ttu-id="96e1b-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="96e1b-132">Related topics</span></span>


[<span data-ttu-id="96e1b-133">Cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="96e1b-133">Application Virtualization Client</span></span>](application-virtualization-client.md)

 

 





