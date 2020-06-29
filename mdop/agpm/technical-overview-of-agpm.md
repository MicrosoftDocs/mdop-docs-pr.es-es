---
title: Introducción técnica de AGPM
description: Introducción técnica de AGPM
author: dansimp
ms.assetid: 36bc0ab5-f752-474c-8559-721ea95169c2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cc635f46c2aabb0c9fa1f472a258a3e65a07b55
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818300"
---
# <span data-ttu-id="a0bc3-103">Introducción técnica de AGPM</span><span class="sxs-lookup"><span data-stu-id="a0bc3-103">Technical Overview of AGPM</span></span>


<span data-ttu-id="a0bc3-104">Administración avanzada de directivas de grupo (AGPM) de Microsoft es una aplicación cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-104">Microsoft Advanced Group Policy Management (AGPM) is a client/server application.</span></span> <span data-ttu-id="a0bc3-105">El servidor AGPM almacena objetos de directiva de grupo (GPO) sin conexión en el archivo que AGPM crea en el sistema de archivos del servidor.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-105">The AGPM Server stores Group Policy Objects (GPOs) offline in the archive that AGPM creates on the server's file system.</span></span> <span data-ttu-id="a0bc3-106">Los administradores de directivas de grupo usan el complemento de AGPM para la consola de administración de directivas de grupo (GPMC) para trabajar con los GPO en el servidor que hospeda el archivo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-106">Group Policy administrators use the AGPM snap-in for the Group Policy Management Console (GPMC) to work with GPOs on the server that hosts the archive.</span></span> <span data-ttu-id="a0bc3-107">Comprender las partes de AGPM y los elementos relacionados, cómo almacenan los GPO en el sistema de archivos y cómo los permisos que controlan las acciones disponibles para cada rol de usuario pueden mejorar la efectividad de los administradores de directivas de grupo con AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-107">Understanding the parts of AGPM and related items, how they store GPOs in the file system, and how permissions control the actions available to each user role can improve Group Policy administrators' effectiveness with AGPM.</span></span>

## <span data-ttu-id="a0bc3-108">Terminología</span><span class="sxs-lookup"><span data-stu-id="a0bc3-108">Terminology</span></span>


<span data-ttu-id="a0bc3-109">A continuación se explican las condiciones básicas de AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-109">The following explains the basic AGPM terms.</span></span>

-   <span data-ttu-id="a0bc3-110">**Cliente de AGPM:** Un equipo que ejecuta el complemento de AGPM para la consola de administración de directivas de grupo (GPMC) y desde el que los administradores de directivas de grupo administran los GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-110">**AGPM Client:** A computer that runs the AGPM snap-in for the Group Policy Management Console (GPMC) and from which Group Policy administrators manage GPOs.</span></span>

-   <span data-ttu-id="a0bc3-111">**Complemento de AGPM:** El componente de software de AGPM instalado en clientes de AGPM para que puedan administrar GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-111">**AGPM snap-in:** The software component of AGPM installed on AGPM Clients so that they can manage GPOs.</span></span>

-   <span data-ttu-id="a0bc3-112">**Servidor de AGPM:** Un servidor que ejecuta el servicio AGPM y administra un archivo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-112">**AGPM Server:** A server that runs the AGPM Service and manages an archive.</span></span> <span data-ttu-id="a0bc3-113">Cada servidor de AGPM puede administrar un solo archivo, pero un servidor de AGPM puede administrar los datos de archivo de varios dominios en un archivo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-113">Each AGPM Server can manage only one archive, but one AGPM Server can manage archive data for multiple domains in one archive.</span></span> <span data-ttu-id="a0bc3-114">Un archivo se puede hospedar en un equipo que no sea un servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-114">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="a0bc3-115">**Servicio AGPM:** El componente de software de AGPM que se ejecuta en un servidor de AGPM como servicio.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-115">**AGPM Service:** The software component of AGPM that runs on an AGPM Server as a service.</span></span> <span data-ttu-id="a0bc3-116">El servicio administra los GPO en el archivo y en el entorno de producción de ese bosque.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-116">The service manages GPOs in the archive and in the production environment in that forest.</span></span>

-   <span data-ttu-id="a0bc3-117">**Archivo:** En AGPM, almacén central que contiene los GPO controlados que administra el servidor de AGPM asociado, además del historial de cada uno de esos GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-117">**Archive:** In AGPM, a central store that contains the controlled GPOs that the associated AGPM Server manages, in addition to the history for each of those GPOs.</span></span> <span data-ttu-id="a0bc3-118">Esto incluye todas las versiones controladas anteriores de cada GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-118">This includes all previous controlled versions of each GPO.</span></span> <span data-ttu-id="a0bc3-119">Un archivo se compone de un archivo de índice de archivo y datos de archivo asociados que pueden incluir datos de los GPO de varios dominios.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-119">An archive consists of an archive index file and associated archive data that may include data for GPOs in multiple domains.</span></span> <span data-ttu-id="a0bc3-120">Un archivo se puede hospedar en un equipo que no sea un servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-120">An archive can be hosted on a computer other than an AGPM Server.</span></span>

-   <span data-ttu-id="a0bc3-121">**GPO controlado:** Un GPO administrado por AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-121">**Controlled GPO:** A GPO that is being managed by AGPM.</span></span> <span data-ttu-id="a0bc3-122">AGPM administra el historial y los permisos de los GPO controlados, que se almacenan en el archivo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-122">AGPM manages the history and permissions of controlled GPOs, which it stores in the archive.</span></span>

-   <span data-ttu-id="a0bc3-123">**Objeto de directiva de grupo** no superpuesto: Un GPO en el entorno de producción para un dominio y no administrado por AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-123">**Uncontrolled GPO:** A GPO in the production environment for a domain and not managed by AGPM.</span></span>

## <span data-ttu-id="a0bc3-124">Lo que AGPM instala, crea y afecta</span><span class="sxs-lookup"><span data-stu-id="a0bc3-124">What AGPM installs, creates, and affects</span></span>


<span data-ttu-id="a0bc3-125">En un servidor de AGPM, el programa de configuración de AGPM instala el servicio AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-125">On an AGPM Server, the AGPM Setup program installs the AGPM Service.</span></span> <span data-ttu-id="a0bc3-126">AGPM no modifica el servicio de directorio® de Active Directory ni el esquema.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-126">AGPM does not alter the Active Directory® directory service or the schema.</span></span> <span data-ttu-id="a0bc3-127">De forma predeterminada, los archivos de programa del servidor AGPM se instalan en%ProgramFiles%\\Microsoft\\AGPM\\Server.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-127">By default, the AGPM Server program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Server.</span></span> <span data-ttu-id="a0bc3-128">Puede instalar el servicio AGPM en un controlador de dominio si es necesario; sin embargo, le recomendamos que instale el servicio AGPM en un servidor miembro.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-128">You can install the AGPM Service on a domain controller if you have to; however, we recommend that you install the AGPM Service on a member server.</span></span>

<span data-ttu-id="a0bc3-129">En un cliente de AGPM, el programa de configuración de AGPM instala el complemento de AGPM y agrega una carpeta de **control de cambios** a cada dominio que aparece en la GPMC.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-129">On an AGPM Client, the AGPM Setup program installs the AGPM snap-in, adding a **Change Control** folder to each domain that appears in the GPMC.</span></span> <span data-ttu-id="a0bc3-130">De forma predeterminada, los archivos de programa cliente AGPM se instalan en%ProgramFiles%\\Microsoft\\AGPM\\Client.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-130">By default, the AGPM Client program files are installed in %ProgramFiles%\\Microsoft\\AGPM\\Client.</span></span>

<span data-ttu-id="a0bc3-131">En la tabla 1 se describen los elementos que AGPM instala o crea y las partes del sistema operativo que afectan a la operación AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-131">Table 1 describes both the items that AGPM installs or creates and the parts of the operating system that affect AGPM operation.</span></span>

**<span data-ttu-id="a0bc3-132">Tabla 1: elementos instalados, creados o afectados por AGPM</span><span class="sxs-lookup"><span data-stu-id="a0bc3-132">Table 1: Items installed, created, or affected by AGPM</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a0bc3-133">Elemento</span><span class="sxs-lookup"><span data-stu-id="a0bc3-133">Item</span></span></th>
<th align="left"><span data-ttu-id="a0bc3-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0bc3-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0bc3-135">Servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="a0bc3-135">AGPM Service</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-136">El servicio AGPM se ejecuta en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-136">The AGPM Service runs on the AGPM Server.</span></span> <span data-ttu-id="a0bc3-137">El servicio administra el archivo, que contiene los GPO desconectados y los GPO controlados en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-137">The service manages the archive, which contains offline GPOs, and controlled GPOs in the production environment.</span></span> <span data-ttu-id="a0bc3-138">La configuración predeterminada del servicio AGPM es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="a0bc3-138">The default configuration of the AGPM Service is as follows:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="a0bc3-139">Nombre del servicio: </strong> servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="a0bc3-139">Service name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="a0bc3-140">Nombre para mostrar: </strong> servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="a0bc3-140">Display name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="a0bc3-141">Ruta de acceso al ejecutable: </strong> % ProgramFiles% \Microsoft\AGPM\Server\Agpm.exe</span><span class="sxs-lookup"><span data-stu-id="a0bc3-141">Path to executable:</strong> %ProgramFiles%\Microsoft\AGPM\Server\Agpm.exe</span></span></p></li>
<li><p><strong><span data-ttu-id="a0bc3-142">Inicio: </strong> automático</span><span class="sxs-lookup"><span data-stu-id="a0bc3-142">Startup:</strong> Automatic</span></span></p></li>
<li><p><strong><span data-ttu-id="a0bc3-143">Iniciar sesión como: </strong> cuenta de servicio AGPM especificada durante la instalación del servidor de AGPM, que se puede cambiar usando <strong> programas y características </strong> en el <strong> Panel de control </strong> .</span><span class="sxs-lookup"><span data-stu-id="a0bc3-143">Log on as:</strong> AGPM Service Account specified during installation of AGPM Server, which can be changed using <strong>Programs and Features</strong> in the <strong>Control Panel</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a0bc3-144">Archivo de AGPM</span><span class="sxs-lookup"><span data-stu-id="a0bc3-144">AGPM archive</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-145">De forma predeterminada, AGPM crea el archivo en%ProgramData%\Microsoft\AGPM en el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-145">By default, AGPM creates the archive in %ProgramData%\Microsoft\AGPM on the AGPM Server.</span></span> <span data-ttu-id="a0bc3-146">El archivo proporciona almacenamiento para objetos de directiva de grupo desconectados y puede almacenar varias versiones de cada uno de ellos.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-146">The archive provides storage for offline GPOs, and it can store multiple versions of each GPO.</span></span> <span data-ttu-id="a0bc3-147">Los cambios que AGPM realiza a los GPO en el archivo no afectan al entorno de producción hasta que un administrador o aprobador de AGPM implemente el GPO en el entorno de producción y vincule el GPO a una unidad organizativa (OU).</span><span class="sxs-lookup"><span data-stu-id="a0bc3-147">Changes that AGPM makes to GPOs in the archive do not affect the production environment until an AGPM Administrator or Approver deploys the GPO to the production environment and links the GPO to an organizational unit (OU).</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0bc3-148">Firewall de Windows</span><span class="sxs-lookup"><span data-stu-id="a0bc3-148">Windows Firewall</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-149">Durante la instalación, AGPM habilita una regla de Firewall de Windows entrante que permite que el cliente de AGPM se comunique con el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-149">During installation, AGPM enables an inbound Windows Firewall rule that allows the AGPM Client to communicate with the AGPM Server.</span></span> <span data-ttu-id="a0bc3-150">La regla predeterminada de Firewall de Windows es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="a0bc3-150">The default Windows Firewall rule is the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="a0bc3-151">Nombre: </strong> servicio AGPM</span><span class="sxs-lookup"><span data-stu-id="a0bc3-151">Name:</strong> AGPM Service</span></span></p></li>
<li><p><strong><span data-ttu-id="a0bc3-152">Acción: </strong> permitir la conexión</span><span class="sxs-lookup"><span data-stu-id="a0bc3-152">Action:</strong> Allow the connection</span></span></p></li>
<li><p><strong><span data-ttu-id="a0bc3-153">Programas: </strong> todos los programas que cumplen las condiciones especificadas</span><span class="sxs-lookup"><span data-stu-id="a0bc3-153">Programs:</strong> All programs that meet the specified conditions</span></span></p></li>
<li><p><strong><span data-ttu-id="a0bc3-154">Tipo de protocolo: </strong> TCP</span><span class="sxs-lookup"><span data-stu-id="a0bc3-154">Protocol type:</strong> TCP</span></span></p></li>
<li><p><strong><span data-ttu-id="a0bc3-155">Puerto local: </strong> 4600</span><span class="sxs-lookup"><span data-stu-id="a0bc3-155">Local port:</strong> 4600</span></span></p></li>
<li><p><strong><span data-ttu-id="a0bc3-156">Puerto remoto: </strong> todos los puertos</span><span class="sxs-lookup"><span data-stu-id="a0bc3-156">Remote port:</strong> All ports</span></span></p></li>
<li><p><strong><span data-ttu-id="a0bc3-157">Dirección IP local: </strong> cualquiera</span><span class="sxs-lookup"><span data-stu-id="a0bc3-157">Local IP address:</strong> Any</span></span></p></li>
<li><p><strong><span data-ttu-id="a0bc3-158">Dirección IP remota: </strong> cualquiera</span><span class="sxs-lookup"><span data-stu-id="a0bc3-158">Remote IP address:</strong> Any</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="a0bc3-159">Servidor de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="a0bc3-159">E-mail server</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-160">AGPM usa el Protocolo simple de transferencia de correo (SMTP) para enviar solicitudes de correo electrónico a las direcciones configuradas en la <strong> pestaña delegación de dominios </strong> . Por ejemplo, cuando un editor solicita que se cree un nuevo GPO, AGPM notifica a cada dirección de correo electrónico especificada en la <strong> pestaña delegación de dominios </strong> .</span><span class="sxs-lookup"><span data-stu-id="a0bc3-160">AGPM uses Simple Mail Transfer Protocol (SMTP) to send e-mail requests to the addresses configured on the <strong>Domain Delegation</strong> tab. For example, when an Editor requests that a new GPO be created, AGPM notifies each e-mail address specified on the <strong>Domain Delegation</strong> tab.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="a0bc3-161">Complemento AGPM</span><span class="sxs-lookup"><span data-stu-id="a0bc3-161">AGPM snap-in</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-162">El complemento de AGPM para la GPMC se ejecuta en los clientes de AGPM y lo usan los administradores de la Directiva de grupo para administrar GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-162">The AGPM snap-in for the GPMC runs on AGPM Clients and is used by Group Policy administrators to manage GPOs.</span></span> <span data-ttu-id="a0bc3-163">El complemento aparece en la GPMC como una <strong> </strong> carpeta de control de cambios en cada dominio.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-163">The snap-in appears in the GPMC as a <strong>Change Control</strong> folder in each domain.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <span data-ttu-id="a0bc3-164">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="a0bc3-164">Additional references</span></span>

<span data-ttu-id="a0bc3-165">Para obtener más información acerca de los archivos instalados por AGPM, consulte la [Guía de planeación de AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).</span><span class="sxs-lookup"><span data-stu-id="a0bc3-165">For more information about the files installed by AGPM, see the [Planning Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160060).</span></span>

## <span data-ttu-id="a0bc3-166">Archive</span><span class="sxs-lookup"><span data-stu-id="a0bc3-166">Archive</span></span>


<span data-ttu-id="a0bc3-167">De forma predeterminada, el proceso de instalación del servidor de AGPM crea el archivo en el disco duro local del servidor de AGPM en%ProgramData%\\Microsoft\\AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-167">By default, the AGPM Server installation process creates the archive on the local hard disk of the AGPM Server at %ProgramData%\\Microsoft\\AGPM.</span></span> <span data-ttu-id="a0bc3-168">Sin embargo, puede cambiar la ruta durante la instalación e incluso crear el archivo en un servidor que no sea el servidor de AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-168">However, you can change the path during installation and even create the archive on a server other than the AGPM Server.</span></span>

<span data-ttu-id="a0bc3-169">El archivo contiene una subcarpeta por cada versión de cada objeto de directiva de grupo que contiene el archivo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-169">The archive contains a subfolder for each version of each GPO the archive contains.</span></span> <span data-ttu-id="a0bc3-170">El nombre de cada subcarpeta es un GUID que identifica una versión del GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-170">The name of each subfolder is a GUID that identifies a version of the GPO.</span></span>

<span data-ttu-id="a0bc3-171">El archivo gpostate.xml registra el estado de cada GPO en el archivo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-171">The gpostate.xml file records the state of each GPO in the archive.</span></span> <span data-ttu-id="a0bc3-172">El archivo es un manifiesto que describe el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-172">The file is a manifest that describes the contents of the archive.</span></span> <span data-ttu-id="a0bc3-173">Por ejemplo, un GPO puede tener varias versiones, y cada versión está en su propia subcarpeta en el archivo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-173">For example, a GPO can have many versions, and each version is in its own subfolder in the archive.</span></span> <span data-ttu-id="a0bc3-174">El archivo gpostate.xml indica qué subcarpetas contienen diferentes versiones de un único GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-174">The gpostate.xml file indicates which subfolders contain different versions of a single GPO.</span></span> <span data-ttu-id="a0bc3-175">Además, las plantillas de GPO tienen subcarpetas en el archivo, pero gpostate.xml indica que se trata de plantillas y de objetos no controlados.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-175">Additionally, GPO templates have subfolders in the archive, but gpostate.xml indicates that these are templates and not controlled GPOs.</span></span> <span data-ttu-id="a0bc3-176">De forma similar, cuando los administradores de directivas de grupo eliminan los GPO, AGPM cambia sus Estados en gpostate.xml para indicar que se encuentran en la **papelera de reciclaje** , pero que no quita realmente las subcarpetas de los GPO del archivo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-176">Similarly, when Group Policy administrators delete GPOs, AGPM changes their states in gpostate.xml to indicate that they are in the **Recycle Bin** but does not actually remove the GPOs' subfolders from the archive.</span></span>

<span data-ttu-id="a0bc3-177">**PRECAUCIÓN**  No edite manualmente gpostate.xml o los GPO que contiene el archivo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-177">**Caution** Do not manually edit gpostate.xml or the GPOs the archive contains.</span></span> <span data-ttu-id="a0bc3-178">Esta información solo se proporciona para mejorar la comprensión del archivo de AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-178">This information is provided only to enhance understanding of the AGPM archive.</span></span> <span data-ttu-id="a0bc3-179">En su lugar, use el complemento de AGPM para cambiar los GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-179">Instead, use the AGPM snap-in to change GPOs.</span></span>

 

<span data-ttu-id="a0bc3-180">Cuando AGPM crea el archivo, ofrece control total para el sistema, los administradores y la cuenta de servicio AGPM (especificada en la configuración del servidor de AGPM).</span><span class="sxs-lookup"><span data-stu-id="a0bc3-180">When AGPM creates the archive, it gives Full Control to SYSTEM, Administrators, and the AGPM Service Account (specified in the setup of AGPM Server).</span></span> <span data-ttu-id="a0bc3-181">El cambio de permisos mediante la interfaz de usuario de AGPM en el complemento de AGPM no modifica los permisos del archivo, ya que la cuenta de servicio AGPM realiza todas las operaciones en nombre del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-181">Changing permissions by using the AGPM user interface on the AGPM snap-in does not alter permissions on the archive, because the AGPM Service Account performs all operations on behalf of the logged-on user.</span></span>

### <span data-ttu-id="a0bc3-182">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="a0bc3-182">Additional references</span></span>

<span data-ttu-id="a0bc3-183">Para obtener información sobre cómo realizar una copia de seguridad del archivo, restaurarlo a partir de una copia de seguridad o mover tanto el servidor de AGPM como el archivo, consulte la sección "realizar tareas de administrador de AGPM" en la [Guía de operaciones de AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span><span class="sxs-lookup"><span data-stu-id="a0bc3-183">For information about how to back up the archive, restore the archive from a backup, or move both the AGPM Server and the archive, see the "Performing AGPM Administrator Tasks" section in the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

## <span data-ttu-id="a0bc3-184">Roles y permisos</span><span class="sxs-lookup"><span data-stu-id="a0bc3-184">Roles and permissions</span></span>


<span data-ttu-id="a0bc3-185">Roles simplificar la delegación.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-185">Roles simplify delegation.</span></span> <span data-ttu-id="a0bc3-186">En lugar de asignar permisos detallados a los administradores de directivas de grupo, los administradores de AGPM pueden asignar uno de los cuatro roles a los administradores de directiva de grupo para permitirles realizar el trabajo relacionado con ese rol:</span><span class="sxs-lookup"><span data-stu-id="a0bc3-186">Instead of assigning detailed permissions to Group Policy administrators, AGPM Administrators can assign one of four roles to Group Policy administrators to let them perform work related to that role:</span></span>

-   <span data-ttu-id="a0bc3-187">**Administrador AGPM:** Los administradores de la Directiva de grupo que tengan asignado el rol de administrador de AGPM (control total) pueden realizar cualquier tarea en AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-187">**AGPM Administrator:** Group Policy administrators assigned the AGPM Administrator (Full Control) role can perform any task in AGPM.</span></span> <span data-ttu-id="a0bc3-188">Los administradores de AGPM pueden configurar opciones para todo el dominio y delegar permisos a otros administradores de la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-188">AGPM Administrators can configure domain-wide options and delegate permissions to other Group Policy administrators.</span></span>

-   <span data-ttu-id="a0bc3-189">**Aprobador:** Los administradores de la Directiva de grupo que tengan asignada la función de aprobador pueden implementar GPO en el entorno de producción de un dominio.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-189">**Approver:** Group Policy administrators assigned the Approver role can deploy GPOs to the production environment for a domain.</span></span> <span data-ttu-id="a0bc3-190">Los aprobadores también pueden crear y eliminar objetos de directiva de grupo y aprobar o rechazar solicitudes de editores.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-190">Approvers can also create and delete GPOs and approve or reject requests from Editors.</span></span> <span data-ttu-id="a0bc3-191">Los aprobadores pueden ver la lista de GPO en un dominio, ver la configuración de la Directiva en los GPO y crear y ver informes de la configuración de la Directiva en un GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-191">Approvers can view the list of GPOs in a domain, view the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="a0bc3-192">No pueden editar la configuración de la Directiva en los GPO a menos que también tengan asignada la función editor.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-192">They cannot edit the policy settings in GPOs unless they are also assigned the Editor role.</span></span>

-   <span data-ttu-id="a0bc3-193">**Editor:** Los administradores de la Directiva de grupo que tengan asignada la función editor pueden ver la lista de GPO de un dominio, ver la configuración de la Directiva en los GPO, editar la configuración de la Directiva en los GPO y crear y ver informes de la configuración de la Directiva en un GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-193">**Editor:** Group Policy administrators assigned the Editor role can view the list of GPOs in a domain, view the policy settings in GPOs, edit the policy settings in GPOs, and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="a0bc3-194">A menos que también se les asigne el rol de aprobador, los editores no podrán crear, implementar ni eliminar objetos de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-194">Unless they are also assigned the Approver role, Editors cannot create, deploy, or delete GPOs.</span></span> <span data-ttu-id="a0bc3-195">Sin embargo, pueden solicitar que los GPO se creen, se implementen o se eliminen.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-195">However, they can request that GPOs be created, deployed, or deleted.</span></span>

-   <span data-ttu-id="a0bc3-196">**Revisor:** Los administradores de la Directiva de grupo que tienen asignada la función de revisor pueden ver la lista de los GPO de un dominio y crear y ver informes de la configuración de la Directiva en un GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-196">**Reviewer:** Group Policy administrators assigned the Reviewer role can view the list of GPOs in a domain and create and view reports of the policy settings in a GPO.</span></span> <span data-ttu-id="a0bc3-197">A menos que se les asigne la función editor, no pueden editar la configuración de directiva en un GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-197">Unless they are also assigned the Editor role, they cannot edit policy settings in a GPO.</span></span>

<span data-ttu-id="a0bc3-198">AGPM proporciona a los administradores de AGPM la flexibilidad de configurar permisos en un nivel más detallado que los roles mediante el complemento de AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-198">AGPM gives AGPM Administrators the flexibility to configure permissions at a more detailed level than roles by using the AGPM snap-in.</span></span> <span data-ttu-id="a0bc3-199">En la tabla 2 se describen estos permisos y se indican los permisos otorgados a cada rol de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-199">Table 2 describes these permissions and indicates the permissions granted to each role by default.</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="a0bc3-200">Permiso</span><span class="sxs-lookup"><span data-stu-id="a0bc3-200">Permission</span></span></th>
<th align="left"><span data-ttu-id="a0bc3-201">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0bc3-201">Description</span></span></th>
<th align="left"><span data-ttu-id="a0bc3-202">Administrador AGPM</span><span class="sxs-lookup"><span data-stu-id="a0bc3-202">AGPM Administrator</span></span></th>
<th align="left"><span data-ttu-id="a0bc3-203">Approver</span><span class="sxs-lookup"><span data-stu-id="a0bc3-203">Approver</span></span></th>
<th align="left"><span data-ttu-id="a0bc3-204">Procesador</span><span class="sxs-lookup"><span data-stu-id="a0bc3-204">Editor</span></span></th>
<th align="left"><span data-ttu-id="a0bc3-205">Revisor</span><span class="sxs-lookup"><span data-stu-id="a0bc3-205">Reviewer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0bc3-206">Control total</span><span class="sxs-lookup"><span data-stu-id="a0bc3-206">Full Control</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-207">Tener todos los permisos.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-207">Have all permissions.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-208">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-208">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0bc3-209">Crear GPO</span><span class="sxs-lookup"><span data-stu-id="a0bc3-209">Create GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-210">Crear GPO en un dominio.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-210">Create GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-211">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-211">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-212">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-212">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0bc3-213">Contenido de la lista</span><span class="sxs-lookup"><span data-stu-id="a0bc3-213">List Contents</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-214">Enumere los GPO de un dominio.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-214">List the GPOs in a domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-215">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-215">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-216">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-216">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-217">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-217">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-218">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-218">Yes</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0bc3-219">Leer configuración</span><span class="sxs-lookup"><span data-stu-id="a0bc3-219">Read Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-220">Leer la configuración de la Directiva dentro de un objeto de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-220">Read the policy settings within a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-221">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-221">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-222">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-222">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-223">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-223">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-224">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-224">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0bc3-225">Editar configuración</span><span class="sxs-lookup"><span data-stu-id="a0bc3-225">Edit Settings</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-226">Cambiar la configuración de la Directiva en un GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-226">Change the policy settings in a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-227">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-227">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-228">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-228">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0bc3-229">Eliminar GPO</span><span class="sxs-lookup"><span data-stu-id="a0bc3-229">Delete GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-230">Eliminar un GPO.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-230">Delete a GPO.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-231">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-231">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-232">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-232">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0bc3-233">Modificar la seguridad</span><span class="sxs-lookup"><span data-stu-id="a0bc3-233">Modify Security</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-234">Delegar el acceso a nivel de dominio, delegar el acceso a un único GPO y delegar el acceso al entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-234">Delegate domain-level access, delegate access to a single GPO, and delegate access to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-235">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-235">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0bc3-236">Implementar GPO</span><span class="sxs-lookup"><span data-stu-id="a0bc3-236">Deploy GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-237">Implemente un GPO desde el archivo en el entorno de producción.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-237">Deploy a GPO from the archive to the production environment.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-238">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-238">Yes</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-239">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-239">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0bc3-240">Crear plantilla</span><span class="sxs-lookup"><span data-stu-id="a0bc3-240">Create Template</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-241">Cree una plantilla de GPO en AGPM.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-241">Create a GPO template in AGPM.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-242">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-242">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-243">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-243">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0bc3-244">Modificar opciones</span><span class="sxs-lookup"><span data-stu-id="a0bc3-244">Modify Options</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-245">Configurar la notificación de correo electrónico AGPM y limitar las versiones de GPO almacenadas en el archivo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-245">Configure AGPM e-mail notification and limit the GPO versions stored in the archive.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-246">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-246">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="a0bc3-247">Exportar GPO</span><span class="sxs-lookup"><span data-stu-id="a0bc3-247">Export GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-248">Exportar un GPO a un archivo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-248">Export a GPO to a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-249">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-249">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-250">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-250">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="a0bc3-251">Importar GPO</span><span class="sxs-lookup"><span data-stu-id="a0bc3-251">Import GPO</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-252">Importar un GPO desde un archivo.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-252">Import a GPO from a file.</span></span></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-253">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-253">Yes</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="a0bc3-254">Sí</span><span class="sxs-lookup"><span data-stu-id="a0bc3-254">Yes</span></span></p></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="a0bc3-255">**Nota:** 
 **Exportar** permisos de GPO y de **GPO de importación** no están disponibles en AGPM 3,0 o 2,5.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-255">**Note**
**Export GPO** and **Import GPO** permissions are not available in AGPM 3.0 or 2.5.</span></span>

<span data-ttu-id="a0bc3-256">La capacidad de delegar el acceso a los GPO en el entorno de producción de un dominio y la capacidad de limitar el número de versiones de GPO almacenadas no están disponibles en AGPM 2,5.</span><span class="sxs-lookup"><span data-stu-id="a0bc3-256">The ability to delegate access to GPOs in the production environment for a domain and the ability to limit the number of GPO versions stored are not available in AGPM 2.5.</span></span>

 

### <span data-ttu-id="a0bc3-257">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="a0bc3-257">Additional references</span></span>

<span data-ttu-id="a0bc3-258">Para obtener información acerca de qué tareas pueden realizar los administradores de directivas de grupo asignadas a una determinada función o sobre qué permisos son necesarios para realizar una tarea específica, consulte la [Guía de operaciones de AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span><span class="sxs-lookup"><span data-stu-id="a0bc3-258">For information about what tasks can be performed by Group Policy administrators assigned a particular role or about which permissions are required to perform a specific task, see the [Operations Guide for AGPM](https://go.microsoft.com/fwlink/?LinkId=160061).</span></span>

 

 





