---
title: Seguridad de cliente de escritorio de App-V
description: Seguridad de cliente de escritorio de App-V
author: dansimp
ms.assetid: 216b9c16-7bb4-4f94-b9d8-810501285008
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 26add6f855780113613cf1591c41722643954477
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822320"
---
# <span data-ttu-id="80546-103">Seguridad de cliente de escritorio de App-V</span><span class="sxs-lookup"><span data-stu-id="80546-103">App-V Desktop Client Security</span></span>


<span data-ttu-id="80546-104">El cliente de escritorio de App-V ofrece muchas mejoras de seguridad que no estaban disponibles en versiones anteriores del producto.</span><span class="sxs-lookup"><span data-stu-id="80546-104">The App-V Desktop Client provides many security enhancements that were not available in previous versions of the product.</span></span> <span data-ttu-id="80546-105">Estos cambios proporcionan mayores niveles de seguridad de forma predeterminada, así como la configuración de la configuración de los clientes.</span><span class="sxs-lookup"><span data-stu-id="80546-105">These changes provide higher levels of security by default and through configuration of the client settings.</span></span>

<span data-ttu-id="80546-106">**Nota:**  Al instalar el cliente de escritorio de App-V en un equipo, el software tiene como valor predeterminado la configuración más segura.</span><span class="sxs-lookup"><span data-stu-id="80546-106">**Note** When you install the App-V Desktop Client on a computer, the software defaults to the most secure settings.</span></span> <span data-ttu-id="80546-107">Sin embargo, al actualizar, la configuración anterior del cliente continúa.</span><span class="sxs-lookup"><span data-stu-id="80546-107">However, when upgrading, the previous settings of the client persist.</span></span>

 

<span data-ttu-id="80546-108">De forma predeterminada, el cliente de escritorio de App-V solo está configurado con los permisos necesarios para permitir que un usuario no administrativo realice una actualización de publicación y aplicaciones de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="80546-108">By default, the App-V Desktop Client is configured only with the permissions required to allow a non-administrative user to perform a publishing refresh and stream applications.</span></span> <span data-ttu-id="80546-109">Entre las mejoras de seguridad adicionales proporcionadas en el cliente de escritorio de App-V se incluyen las siguientes:</span><span class="sxs-lookup"><span data-stu-id="80546-109">Additional security enhancements provided in the App-V Desktop Client include the following:</span></span>

-   <span data-ttu-id="80546-110">De forma predeterminada, solo el proceso de actualización de la publicación permite una actualización de la caché OSD.</span><span class="sxs-lookup"><span data-stu-id="80546-110">By default, an OSD cache update is allowed only by the publishing refresh process.</span></span>

-   <span data-ttu-id="80546-111">El archivo de registro ( `sftlog.txt` ) solo es accesible para las cuentas con acceso administrativo local al cliente.</span><span class="sxs-lookup"><span data-stu-id="80546-111">The log file (`sftlog.txt`) is accessible only by accounts with local administrative access to the client.</span></span>

-   <span data-ttu-id="80546-112">El archivo de registro ahora tiene un tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="80546-112">The log file now has a maximum size.</span></span>

-   <span data-ttu-id="80546-113">Los archivos de registro se administran mediante la configuración de archivo.</span><span class="sxs-lookup"><span data-stu-id="80546-113">The log files are managed through archive settings.</span></span>

-   <span data-ttu-id="80546-114">El registro de eventos del sistema se realiza ahora.</span><span class="sxs-lookup"><span data-stu-id="80546-114">System Event logging is now performed.</span></span>

## <span data-ttu-id="80546-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="80546-115">Permissions</span></span>


<span data-ttu-id="80546-116">Después de instalar el cliente de escritorio, puede configurar otras opciones de seguridad a través de MMC o en un cliente individual mediante el registro o la plantilla ADM proporcionada por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="80546-116">After you install the Desktop Client, you can configure other security settings through the MMC, or on an individual client by using the registry or the ADM Template provided by Microsoft.</span></span> <span data-ttu-id="80546-117">El cliente de escritorio de App-V tiene permisos que puede configurar para restringir el acceso de usuarios no administrativos a todas las características del cliente de escritorio.</span><span class="sxs-lookup"><span data-stu-id="80546-117">The App-V Desktop Client has permissions that you can set to restrict non-administrative users from accessing all the features of the Desktop Client.</span></span> <span data-ttu-id="80546-118">Para obtener una lista completa de los permisos, consulte el archivo de ayuda del cliente de App-V o la guía de operaciones de App-V.</span><span class="sxs-lookup"><span data-stu-id="80546-118">For a full list of permissions, please see the App-V Client Help file or App-V Operations Guide.</span></span>

<span data-ttu-id="80546-119">**Importante**  Considere detenidamente las consecuencias de cambiar los derechos de acceso, especialmente en los sistemas compartidos por varios usuarios, como los servidores de terminal.</span><span class="sxs-lookup"><span data-stu-id="80546-119">**Important** Carefully consider the consequences of changing access rights, especially on systems that are shared by multiple users, such as Terminal Servers.</span></span>

 

<span data-ttu-id="80546-120">**Nota:**  Si los usuarios del entorno tienen privilegios de administrador local para sus equipos, los permisos se pasan por alto.</span><span class="sxs-lookup"><span data-stu-id="80546-120">**Note** If users in the environment have local administrator privileges for their computers, the permissions are ignored.</span></span>

 

### <span data-ttu-id="80546-121">Plantilla ADM</span><span class="sxs-lookup"><span data-stu-id="80546-121">ADM Template</span></span>

<span data-ttu-id="80546-122">Microsoft Application Virtualization (App-V) presenta una plantilla ADM que puede usar para establecer la configuración de cliente más común mediante directivas de grupo.</span><span class="sxs-lookup"><span data-stu-id="80546-122">Microsoft Application Virtualization (App-V) introduces an ADM Template that you can use to configure the most common client settings through Group Policies.</span></span> <span data-ttu-id="80546-123">Esta plantilla permite a los administradores implementar y cambiar muchas de las opciones de configuración del cliente a través de un modelo de administración centralizado.</span><span class="sxs-lookup"><span data-stu-id="80546-123">This template enables administrators to implement and change many of the client settings through a centralized administration model.</span></span> <span data-ttu-id="80546-124">Algunos de los valores disponibles en la plantilla ADM son configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="80546-124">Some of the settings available in the ADM Template are security settings.</span></span>

<span data-ttu-id="80546-125">**Importante**  Cuando use la plantilla ADM, recuerde que la configuración es la configuración de preferencias de directiva de grupo y no directivas de grupo completamente administradas.</span><span class="sxs-lookup"><span data-stu-id="80546-125">**Important** When using the ADM Template, remember that the settings are Group Policy preference settings and not fully managed Group Policies.</span></span>

 

<span data-ttu-id="80546-126">Para obtener una descripción completa de la plantilla ADM, la configuración específica y la orientación para implementar correctamente clientes en su entorno, consulte las notas del producto de la plantilla ADM de App-V en [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063) .</span><span class="sxs-lookup"><span data-stu-id="80546-126">For a full description of the ADM Template, the specific settings, and guidance to successfully deploy clients in your environment, see the App-V ADM Template white paper at [https://go.microsoft.com/fwlink/LinkId=122063](https://go.microsoft.com/fwlink/?LinkId=122063).</span></span>

## <span data-ttu-id="80546-127">Quitar asociaciones de tipo de archivo OSD</span><span class="sxs-lookup"><span data-stu-id="80546-127">Removing OSD File Type Associations</span></span>


<span data-ttu-id="80546-128">Si su organización no requiere que los usuarios abran las aplicaciones directamente desde un archivo OSD, puede mejorar la seguridad si quita las asociaciones de tipos de archivo en el cliente.</span><span class="sxs-lookup"><span data-stu-id="80546-128">If your organization does not require users to open applications directly from an OSD file, you can enhance security by removing the file type associations on the client.</span></span> <span data-ttu-id="80546-129">Quite las `HKEY_CURRENT_USERS` teclas para OSD y `Softgird.osd.file` con el editor del registro.</span><span class="sxs-lookup"><span data-stu-id="80546-129">Remove the `HKEY_CURRENT_USERS` keys for OSD and `Softgird.osd.file` by using the registry editor.</span></span> <span data-ttu-id="80546-130">Puede poner este proceso en un script de inicio de sesión o en un script posterior a la instalación para automatizar estos cambios.</span><span class="sxs-lookup"><span data-stu-id="80546-130">You can put this process into a logon script or into a post-installation script to automate these changes.</span></span>

 

 





