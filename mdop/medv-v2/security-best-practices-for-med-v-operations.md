---
title: Procedimientos recomendados de seguridad para las operaciones de MED-V
description: Procedimientos recomendados de seguridad para las operaciones de MED-V
author: dansimp
ms.assetid: 231e2b9a-8b49-42fe-93b5-2ef12fe17bac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4353a15c756dba8cf44f530c2077546e3f9288cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825400"
---
# <span data-ttu-id="cbeec-103">Procedimientos recomendados de seguridad para las operaciones de MED-V</span><span class="sxs-lookup"><span data-stu-id="cbeec-103">Security Best Practices for MED-V Operations</span></span>


<span data-ttu-id="cbeec-104">Como administrador autorizado, usted es responsable de proteger la información de los usuarios y de mantener la seguridad de su organización durante y después de la implementación de áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="cbeec-104">As an authorized administrator, you are responsible to protect the information of the users and maintain security of your organization during and after the deployment of MED-V workspaces.</span></span> <span data-ttu-id="cbeec-105">En particular, tenga en cuenta los siguientes problemas:</span><span class="sxs-lookup"><span data-stu-id="cbeec-105">In particular, consider the following issues.</span></span>

<span data-ttu-id="cbeec-106">**Personalizar Internet Explorer en el área de trabajo de MED-V**.</span><span class="sxs-lookup"><span data-stu-id="cbeec-106">**Customizing Internet Explorer in the MED-V workspace**.</span></span> <span data-ttu-id="cbeec-107">Las versiones anteriores del sistema operativo Windows y de Internet Explorer no son tan seguras como las versiones actuales.</span><span class="sxs-lookup"><span data-stu-id="cbeec-107">Earlier versions of the Windows operating system and of Internet Explorer are not as secure as current versions.</span></span> <span data-ttu-id="cbeec-108">Por lo tanto, Internet Explorer en el área de trabajo de MED-V está configurado para evitar la navegación y otras actividades que pueden suponer riesgos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="cbeec-108">Therefore, Internet Explorer in the MED-V workspace is configured to prevent browsing and other activities that can pose security risks.</span></span> <span data-ttu-id="cbeec-109">Además, la configuración de la zona de seguridad de Internet para Internet Explorer en el área de trabajo de MED-V se establece en el nivel más alto.</span><span class="sxs-lookup"><span data-stu-id="cbeec-109">In addition, the Internet security zone setting for Internet Explorer in the MED-V workspace is set to the highest level.</span></span> <span data-ttu-id="cbeec-110">De forma predeterminada, estas dos configuraciones se establecen en el paquete del área de trabajo de MED-V al crear el paquete del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="cbeec-110">By default, both of these configurations are set in the MED-V Workspace Packager when you create your MED-V workspace package.</span></span>

<span data-ttu-id="cbeec-111">Al usar el kit de administración de Internet Explorer (IEAK) o cambiar los valores predeterminados en el Empaquetador de área de trabajo de MED-V, puede personalizar Internet Explorer en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="cbeec-111">By using Internet Explorer Administration Kit (IEAK) or by changing the defaults in the MED-V Workspace Packager, you can customize Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="cbeec-112">Sin embargo, tenga en cuenta que si Personaliza Internet Explorer en el área de trabajo de MED-V de modo que sea menos seguro, puede exponer su organización a los riesgos de seguridad presentes en las versiones anteriores de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="cbeec-112">However, realize that if you customize Internet Explorer in the MED-V workspace in such a way as to make it less secure, you can expose your organization to those security risks that are present in older versions of Internet Explorer.</span></span>

<span data-ttu-id="cbeec-113">Desde una perspectiva de seguridad, los procedimientos recomendados para administrar Internet Explorer en el área de trabajo de MED-V son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="cbeec-113">From a security perspective, best practices for managing Internet Explorer in the MED-V workspace are as follows:</span></span>

-   <span data-ttu-id="cbeec-114">Al crear el paquete de área de trabajo de MED-V, deje los valores predeterminados para que Internet Explorer en el área de trabajo de MED-V se configure para evitar la navegación y otras actividades que pueden suponer riesgos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="cbeec-114">When creating your MED-V workspace package, leave the defaults set so that Internet Explorer in the MED-V workspace is configured to prevent browsing and other activities that can pose security risks.</span></span>

-   <span data-ttu-id="cbeec-115">Al crear el paquete de área de trabajo de MED-V, deje los valores predeterminados de forma que la configuración de seguridad de la zona de seguridad de Internet se mantenga en el nivel más alto.</span><span class="sxs-lookup"><span data-stu-id="cbeec-115">When creating your MED-V workspace package, leave the defaults set so that the security setting for the Internet security zone remains at the highest level.</span></span>

-   <span data-ttu-id="cbeec-116">Configure el proxy de empresa o el asesor de contenido de Internet Explorer para bloquear dominios que estén fuera de la intranet de la empresa.</span><span class="sxs-lookup"><span data-stu-id="cbeec-116">Configure your enterprise proxy or Internet Explorer Content Advisor to block domains that are outside your company’s intranet.</span></span>

**<span data-ttu-id="cbeec-117">Configurar un área de trabajo de MED-V para todos los usuarios de un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="cbeec-117">Configuring a MED-V workspace for all users on a shared computer.</span></span>** <span data-ttu-id="cbeec-118">Al configurar un área de trabajo de MED-V para que todos los usuarios puedan obtener acceso a ella en un equipo compartido, tenga en cuenta que la máquina virtual invitada (VHD) se coloca en una ubicación que concede acceso de lectura y escritura a todos los usuarios de ese sistema.</span><span class="sxs-lookup"><span data-stu-id="cbeec-118">When configuring a MED-V workspace so that it can be accessed by all users on a shared computer, realize that the guest virtual machine (VHD) is put in a location that gives Read and Write access to all users on that system.</span></span>

**<span data-ttu-id="cbeec-119">Configuración de una cuenta de proxy para unirse a un dominio.</span><span class="sxs-lookup"><span data-stu-id="cbeec-119">Configuring a proxy account for domain joining.</span></span>** <span data-ttu-id="cbeec-120">Al configurar una cuenta de proxy para unir máquinas virtuales al dominio, debe saber que un usuario final puede obtener las credenciales de la cuenta de proxy.</span><span class="sxs-lookup"><span data-stu-id="cbeec-120">When configuring a proxy account for joining virtual machines to the domain, you must know that it is possible for an end user to obtain the proxy account credentials.</span></span> <span data-ttu-id="cbeec-121">Por lo tanto, deben tomarse precauciones, como limitar los derechos de usuario de la cuenta, para evitar que un usuario final pueda usar las credenciales para causar daños.</span><span class="sxs-lookup"><span data-stu-id="cbeec-121">Thus, necessary precautions must be taken, such as limiting account user rights, to prevent an end user from using the credentials for causing harm.</span></span>

**<span data-ttu-id="cbeec-122">Configuración de Sysprep.</span><span class="sxs-lookup"><span data-stu-id="cbeec-122">Sysprep Configuration.</span></span>** <span data-ttu-id="cbeec-123">Aunque el archivo Sysprep. inf está cifrado de forma predeterminada, su contenido puede ser descifrado y leído por cualquier usuario final determinado que pueda iniciar sesión correctamente en la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cbeec-123">Although the Sysprep.inf file is encrypted by default, its contents can be decrypted and read by any determined end user who can successfully log on to the virtual machine.</span></span> <span data-ttu-id="cbeec-124">Esto provoca problemas de seguridad porque el archivo Sysprep. inf puede contener credenciales además de una clave de producto de Windows.</span><span class="sxs-lookup"><span data-stu-id="cbeec-124">This raises security concerns because the Sysprep.inf file can contain credentials in addition to a Windows product key.</span></span>

<span data-ttu-id="cbeec-125">Puede reducir este riesgo configurando una cuenta limitada para unir máquinas virtuales al dominio y especificando las credenciales para esa cuenta cuando configure Sysprep.</span><span class="sxs-lookup"><span data-stu-id="cbeec-125">You can lessen this risk by setting up a limited account for joining virtual machines to the domain and specifying the credentials for that account when configuring Sysprep.</span></span> <span data-ttu-id="cbeec-126">Como alternativa, también puede configurar Sysprep y la primera instalación para que se ejecute en modo **atendido** y para que los usuarios finales proporcionen sus credenciales para unirse a la máquina virtual en el dominio.</span><span class="sxs-lookup"><span data-stu-id="cbeec-126">Alternately, you can also configure Sysprep and first time setup to run in **Attended** mode and require end users to provide their credentials for joining the virtual machine to the domain.</span></span>

<span data-ttu-id="cbeec-127">Una práctica recomendada de MED-V es especificar que FtsCompletion.exe se ejecuta en una cuenta que proporciona al usuario final derechos para conectarse al invitado a través del cliente de conexión de escritorio remoto (RDC).</span><span class="sxs-lookup"><span data-stu-id="cbeec-127">A MED-V best practice is to specify that FtsCompletion.exe is run under an account that gives the end user rights to connect to the guest through the Remote Desktop Connection (RDC) Client.</span></span>

**<span data-ttu-id="cbeec-128">Autenticación de usuario final.</span><span class="sxs-lookup"><span data-stu-id="cbeec-128">End-user authentication.</span></span>** <span data-ttu-id="cbeec-129">Habilitar el almacenamiento en caché de las credenciales del usuario final proporciona la mejor experiencia de usuario de MED-V, pero crea la posibilidad de que alguien pueda obtener acceso a las credenciales del usuario final.</span><span class="sxs-lookup"><span data-stu-id="cbeec-129">Enabling the caching of end-user credentials provides the best user experience of MED-V, but creates the potential that someone could gain access to the end user’s credentials.</span></span> <span data-ttu-id="cbeec-130">La única forma de reducir este riesgo es especificando en el **paquete del área de trabajo MED-V** que las credenciales de usuario final no se almacenan.</span><span class="sxs-lookup"><span data-stu-id="cbeec-130">The only way to lessen this risk is by specifying on the **MED-V Workspace Packager** that end-user credentials are not stored.</span></span> <span data-ttu-id="cbeec-131">Para obtener más información sobre la autenticación de usuarios finales, consulte [autenticación de usuarios finales de MED-V](authentication-of-med-v-end-users.md).</span><span class="sxs-lookup"><span data-stu-id="cbeec-131">For more information about authentication of end users, see [Authentication of MED-V End Users](authentication-of-med-v-end-users.md).</span></span>

## <span data-ttu-id="cbeec-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cbeec-132">Related topics</span></span>


[<span data-ttu-id="cbeec-133">Solución de problemas de operaciones</span><span class="sxs-lookup"><span data-stu-id="cbeec-133">Operations Troubleshooting</span></span>](operations-troubleshooting-medv2.md)

[<span data-ttu-id="cbeec-134">Microsoft Enterprise Desktop Virtualization 2,0</span><span class="sxs-lookup"><span data-stu-id="cbeec-134">Microsoft Enterprise Desktop Virtualization 2.0</span></span>](index.md)

 

 





