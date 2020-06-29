---
title: Cómo implementar los componentes de MED-V a través de un sistema de distribución electrónica de Software
description: Cómo implementar los componentes de MED-V a través de un sistema de distribución electrónica de Software
author: dansimp
ms.assetid: 8a800bdf-6fa4-47b4-b417-df053289d4e8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d772702c770340796fe770273146bd0308617a69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824851"
---
# <span data-ttu-id="b1649-103">Cómo implementar los componentes de MED-V a través de un sistema de distribución electrónica de Software</span><span class="sxs-lookup"><span data-stu-id="b1649-103">How to Deploy the MED-V Components Through an Electronic Software Distribution System</span></span>


<span data-ttu-id="b1649-104">Un sistema electrónico de distribución de software puede ayudarte a mover el software de forma eficaz a muchos equipos a través de conexiones de red lentas o rápidas.</span><span class="sxs-lookup"><span data-stu-id="b1649-104">An electronic software distribution system can help you efficiently move software to many computers over slow or fast network connections.</span></span> <span data-ttu-id="b1649-105">La siguiente sección proporciona información e instrucciones para ayudarle a implementar los componentes de virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0 en toda la empresa mediante un sistema de distribución de software.</span><span class="sxs-lookup"><span data-stu-id="b1649-105">The following section provides information and instructions to help you deploy the Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 components throughout your enterprise by using a software distribution system.</span></span>

**<span data-ttu-id="b1649-106">Nota</span><span class="sxs-lookup"><span data-stu-id="b1649-106">Note</span></span>**  
<span data-ttu-id="b1649-107">Sea cual sea la solución de distribución de software que use, debe estar familiarizado con los requisitos de su solución en particular.</span><span class="sxs-lookup"><span data-stu-id="b1649-107">Whichever software distribution solution that you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="b1649-108">Si está usando System Center Configuration Manager 2007 R2 o una versión posterior, consulte la [biblioteca de documentación de Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=66999) en la biblioteca técnica de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=66999) .</span><span class="sxs-lookup"><span data-stu-id="b1649-108">If you are using System Center Configuration Manager 2007 R2 or a later version, see the [Configuration Manager Documentation Library](https://go.microsoft.com/fwlink/?LinkId=66999) in the Microsoft Technical Library (https://go.microsoft.com/fwlink/?LinkId=66999).</span></span>



**<span data-ttu-id="b1649-109">Importante</span><span class="sxs-lookup"><span data-stu-id="b1649-109">Important</span></span>**  
<span data-ttu-id="b1649-110">Si está usando System Center Configuration Manager 2007 SP2 y las áreas de trabajo de MED-V están configuradas para funcionar en modo **NAT** , las máquinas virtuales se clasifican como clientes basados en Internet y no pueden encontrar los puntos de distribución más cercanos para descargar contenido.</span><span class="sxs-lookup"><span data-stu-id="b1649-110">If you are using System Center Configuration Manager 2007 SP2 and your MED-V workspaces are configured to operate in **NAT** mode, the virtual machines are classified as Internet-based clients and cannot find the closest distribution points from which to download content.</span></span>

<span data-ttu-id="b1649-111">El [hotfix para mejorar la funcionalidad de las VM administradas por Med-v](https://go.microsoft.com/fwlink/?LinkId=201088) ( https://go.microsoft.com/fwlink/?LinkId=201088) agrega nueva funcionalidad a las máquinas virtuales administradas por Med-v y que están configuradas para funcionar en modo **NAT** .</span><span class="sxs-lookup"><span data-stu-id="b1649-111">The [hotfix to improve the functionality for VMs that are managed by MED-V](https://go.microsoft.com/fwlink/?LinkId=201088) (https://go.microsoft.com/fwlink/?LinkId=201088) adds new functionality to virtual machines that are managed by MED-V and that are configured to operate in **NAT** mode.</span></span> <span data-ttu-id="b1649-112">La nueva funcionalidad permite que las máquinas virtuales tengan acceso a los puntos de distribución más cercanos.</span><span class="sxs-lookup"><span data-stu-id="b1649-112">The new functionality lets virtual machines access the closest distribution points.</span></span> <span data-ttu-id="b1649-113">Por lo tanto, el administrador puede administrar la máquina virtual y el equipo host de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="b1649-113">Therefore, the administrator can manage the virtual machine and the host computer in the same manner.</span></span> <span data-ttu-id="b1649-114">Este Hotfix debe instalarse primero en el servidor del sitio y, después, en el cliente.</span><span class="sxs-lookup"><span data-stu-id="b1649-114">This hotfix must be installed first on the site server and then on the client.</span></span>

<span data-ttu-id="b1649-115">La actualización está disponible públicamente.</span><span class="sxs-lookup"><span data-stu-id="b1649-115">The update is publicly available.</span></span> <span data-ttu-id="b1649-116">Sin embargo, es posible que se le pida que acepte un contrato de servicios de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b1649-116">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="b1649-117">Siga las indicaciones en las páginas web sucesivas para recuperar este Hotfix.</span><span class="sxs-lookup"><span data-stu-id="b1649-117">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>



**<span data-ttu-id="b1649-118">Nota</span><span class="sxs-lookup"><span data-stu-id="b1649-118">Note</span></span>**  
<span data-ttu-id="b1649-119">Debe instalar el paquete de área de trabajo MED-V y crear sus áreas de trabajo de MED-V para poder implementar los componentes de MED-V a través del sistema de distribución de software.</span><span class="sxs-lookup"><span data-stu-id="b1649-119">You must install the MED-V workspace packager and build your MED-V workspaces before you can deploy the MED-V components through your software distribution system.</span></span> <span data-ttu-id="b1649-120">Para obtener más información sobre cómo preparar una imagen y crear áreas de trabajo de MED-V, consulte [operaciones para Med-v](operations-for-med-v.md).</span><span class="sxs-lookup"><span data-stu-id="b1649-120">For more information about how to prepare an image and to build your MED-V workspaces, see [Operations for MED-V](operations-for-med-v.md).</span></span>



**<span data-ttu-id="b1649-121">Para implementar los componentes de MED-V mediante un sistema de distribución de software</span><span class="sxs-lookup"><span data-stu-id="b1649-121">To deploy the MED-V components by using a software distribution system</span></span>**

1.  <span data-ttu-id="b1649-122">Definir un grupo de equipos y usuarios en el sistema electrónico de distribución de software como el conjunto de destino de equipos o usuarios.</span><span class="sxs-lookup"><span data-stu-id="b1649-122">Define a group of computers and users in the electronic software distribution system as the target set of computers/users.</span></span>

2.  <span data-ttu-id="b1649-123">Cree paquetes para cada archivo de instalación de Microsoft que deba distribuirse.</span><span class="sxs-lookup"><span data-stu-id="b1649-123">Create packages for each Microsoft installation file that needs to be distributed.</span></span> <span data-ttu-id="b1649-124">A continuación se indican los archivos necesarios y el orden en el que se deben instalar:</span><span class="sxs-lookup"><span data-stu-id="b1649-124">The following are the required files and the order in which they must be installed:</span></span>

    1.  <span data-ttu-id="b1649-125">**Windows Virtual PC** : Si no está instalado (es necesario reiniciar el equipo).</span><span class="sxs-lookup"><span data-stu-id="b1649-125">**Windows Virtual PC** – if not already installed (a computer restart is required).</span></span> <span data-ttu-id="b1649-126">Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="b1649-126">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    2.  <span data-ttu-id="b1649-127">**Adiciones y actualizaciones de Windows Virtual PC** : Si aún no están instaladas.</span><span class="sxs-lookup"><span data-stu-id="b1649-127">**Windows Virtual PC Additions and Updates** – if not already installed.</span></span> <span data-ttu-id="b1649-128">Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="b1649-128">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    3.  <span data-ttu-id="b1649-129">**Archivo de instalación del agente de host Med-v** : instala el agente de host (MED-v \ _HostAgent \ _setup archivo de instalación).</span><span class="sxs-lookup"><span data-stu-id="b1649-129">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="b1649-130">Para obtener más información, vea [Cómo instalar manualmente el agente de host MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="b1649-130">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

        **<span data-ttu-id="b1649-131">Advertencia</span><span class="sxs-lookup"><span data-stu-id="b1649-131">Warning</span></span>**  
        <span data-ttu-id="b1649-132">Cierre Internet Explorer antes de instalar el agente de host MED-V; de lo contrario, los conflictos pueden producirse posteriormente con el redireccionamiento de URL.</span><span class="sxs-lookup"><span data-stu-id="b1649-132">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="b1649-133">También puede hacerlo especificando un reinicio del equipo durante una distribución.</span><span class="sxs-lookup"><span data-stu-id="b1649-133">You can also do this by specifying a computer restart during a distribution.</span></span>   

    4.  <span data-ttu-id="b1649-134">**Instalador de área de trabajo de Med-v, VHD y ejecutable de configuración** : creados en el **Empaquetador de área de trabajo de Med-v**.</span><span class="sxs-lookup"><span data-stu-id="b1649-134">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="b1649-135">Para obtener más información, vea [crear un paquete de área de trabajo de MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="b1649-135">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        **<span data-ttu-id="b1649-136">Importante</span><span class="sxs-lookup"><span data-stu-id="b1649-136">Important</span></span>**  
        <span data-ttu-id="b1649-137">El archivo de disco duro virtual comprimido (. medv) y el programa de instalación ejecutable (setup.exe) deben estar en la misma carpeta que el instalador del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="b1649-137">The compressed virtual hard disk file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="b1649-138">Después, instale el instalador de área de trabajo MED-V ejecutando setup.exe.</span><span class="sxs-lookup"><span data-stu-id="b1649-138">Then, install the MED-V workspace installer by running setup.exe.</span></span>

        **<span data-ttu-id="b1649-139">Sugerencia</span><span class="sxs-lookup"><span data-stu-id="b1649-139">Tip</span></span>**  
        <span data-ttu-id="b1649-140">Dado que los problemas que se pueden producir al instalar MED-V desde una ubicación de red, le recomendamos que copie los archivos de configuración del área de trabajo de MED-V localmente y, a continuación, ejecute setup.exe.</span><span class="sxs-lookup"><span data-stu-id="b1649-140">Because problems that can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.</span></span>       

3.  <span data-ttu-id="b1649-141">Configure los paquetes para que se ejecuten en modo silencioso (no es necesaria la intervención del usuario).</span><span class="sxs-lookup"><span data-stu-id="b1649-141">Configure the packages to run in silent mode (no user interaction is required).</span></span>

    <span data-ttu-id="b1649-142">Si se ejecuta en modo silencioso, se elimina la solicitud de cerrar Internet Explorer si está en ejecución y se pide iniciar el agente de host MED-V.</span><span class="sxs-lookup"><span data-stu-id="b1649-142">Running in silent mode eliminates the prompt to close Internet Explorer if it is running and the prompt to start the MED-V Host Agent.</span></span> <span data-ttu-id="b1649-143">Ambas acciones se realizan cuando se reinicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="b1649-143">Both actions are performed when the computer is restarted.</span></span>

    **<span data-ttu-id="b1649-144">Nota</span><span class="sxs-lookup"><span data-stu-id="b1649-144">Note</span></span>**  
    <span data-ttu-id="b1649-145">La instalación de Windows Virtual PC requiere que reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="b1649-145">Installation of Windows Virtual PC requires you to restart the computer.</span></span> <span data-ttu-id="b1649-146">Puede crear un único proceso de instalación e instalar todos los componentes al mismo tiempo si elimina el reinicio e ignora los requisitos previos necesarios para que MED-V se instale.</span><span class="sxs-lookup"><span data-stu-id="b1649-146">You can create a single installation process and install all the components at the same time if you suppress the restart and ignore the prerequisites necessary for MED-V to install.</span></span> <span data-ttu-id="b1649-147">También puede hacerlo con los argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="b1649-147">You can also do this by using command-line arguments.</span></span> <span data-ttu-id="b1649-148">Para obtener un ejemplo de estos argumentos, consulte [para instalar los componentes de MED-V mediante un archivo por lotes](#bkmk-batch).</span><span class="sxs-lookup"><span data-stu-id="b1649-148">For an example of these arguments, see [To install the MED-V components by using a batch file](#bkmk-batch).</span></span> <span data-ttu-id="b1649-149">MED-V se inicia automáticamente cuando se reinicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="b1649-149">MED-V automatically starts when the computer is restarted.</span></span>

4.  <span data-ttu-id="b1649-150">Instale MED-V y sus componentes antes de instalar Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="b1649-150">Install MED-V and its components before installing Windows Virtual PC.</span></span> <span data-ttu-id="b1649-151">Vea el archivo de proceso por lotes de ejemplo más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="b1649-151">See the example batch file later in this topic.</span></span>

    **<span data-ttu-id="b1649-152">Importante</span><span class="sxs-lookup"><span data-stu-id="b1649-152">Important</span></span>**  
    <span data-ttu-id="b1649-153">Seleccione la opción **omitir \ _PREREQUISITES** como se muestra en el archivo de proceso por lotes de ejemplo para que los componentes de MED-V puedan instalarse antes que los componentes de VPC requeridos.</span><span class="sxs-lookup"><span data-stu-id="b1649-153">Select the **IGNORE\_PREREQUISITES** option as shown in the example batch file so that the MED-V components can be installed prior to the required VPC components.</span></span> <span data-ttu-id="b1649-154">Instale los componentes de MED-V en este orden para permitir el reinicio único.</span><span class="sxs-lookup"><span data-stu-id="b1649-154">Install the MED-V components in this order to allow for the single restart.</span></span>

5.  <span data-ttu-id="b1649-155">Identifique cualquier otro requisito necesario para la instalación y para el sistema de distribución de software, como plataformas de destino y el espacio libre en disco.</span><span class="sxs-lookup"><span data-stu-id="b1649-155">Identify any other requirements necessary for the installation and for your software distribution system, such as target platforms and the free disk space.</span></span>

6.  <span data-ttu-id="b1649-156">Asigne los paquetes al conjunto de equipos de destino de equipos o usuarios.</span><span class="sxs-lookup"><span data-stu-id="b1649-156">Assign the packages to the target set of computers/users.</span></span>

    <span data-ttu-id="b1649-157">Mientras se ejecutan los equipos, el cliente del sistema de distribución de software reconoce que hay nuevos paquetes disponibles y comienza a instalar los paquetes según la definición y los requisitos.</span><span class="sxs-lookup"><span data-stu-id="b1649-157">As computers are running, the software distribution system client recognizes that new packages are available and begins to install the packages per the definition and requirements.</span></span> <span data-ttu-id="b1649-158">Las instalaciones deben ejecutarse secuencialmente en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="b1649-158">The installations should run sequentially in silent mode.</span></span> <span data-ttu-id="b1649-159">Recomendamos que se realice como un único proceso que no requiera reiniciar hasta que se instalen todos los paquetes.</span><span class="sxs-lookup"><span data-stu-id="b1649-159">We recommend that this is performed as a single process that does not require a restart until all the packages are installed.</span></span>

7.  <span data-ttu-id="b1649-160">Una vez completadas las instalaciones, reinicie los equipos actualizados.</span><span class="sxs-lookup"><span data-stu-id="b1649-160">After the installations are complete, restart the updated computers.</span></span>

    <span data-ttu-id="b1649-161">Según el sistema de distribución de software, puede programar un reinicio del equipo o los usuarios finales podrán reiniciar los equipos manualmente durante su trabajo normal.</span><span class="sxs-lookup"><span data-stu-id="b1649-161">Depending on the software distribution system, you can schedule a restart of the computer or the end users can restart the computers manually during their regular work.</span></span> <span data-ttu-id="b1649-162">Después de reiniciar el equipo, MED-V se inicia automáticamente después de que un usuario final inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="b1649-162">After the computer is restarted, MED-V automatically starts after an end user logs on.</span></span> <span data-ttu-id="b1649-163">Cuando MED-V se inicia por primera vez, se ejecuta la configuración primera vez.</span><span class="sxs-lookup"><span data-stu-id="b1649-163">When MED-V starts for the first time, it runs first time setup.</span></span>

<span data-ttu-id="b1649-164">La configuración comienza por primera vez y puede tardar varios minutos en completarse, según el tamaño del disco duro virtual que especificó y el número de directivas aplicadas al área de trabajo de MED-V en el inicio.</span><span class="sxs-lookup"><span data-stu-id="b1649-164">First time setup starts and might take several minutes to finish, depending on the size of the virtual hard disk that you specified and the number of policies applied to the MED-V workspace on startup.</span></span> <span data-ttu-id="b1649-165">El usuario final puede realizar un seguimiento del progreso observando el icono de MED-V en el área de notificación.</span><span class="sxs-lookup"><span data-stu-id="b1649-165">The end user can track the progress by watching the MED-V icon in the notification area.</span></span> <span data-ttu-id="b1649-166">Para obtener más información sobre la configuración de la primera vez, vea [información general sobre la implementación de 2,0 MED-V](med-v-20-deployment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b1649-166">For more information about first time setup, see [MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md).</span></span>

<a href="" id="bkmk-batch"></a>**<span data-ttu-id="b1649-167">Para instalar los componentes de MED-V mediante un archivo por lotes</span><span class="sxs-lookup"><span data-stu-id="b1649-167">To install the MED-V components by using a batch file</span></span>**

1.  <span data-ttu-id="b1649-168">Ejecute la instalación en un símbolo del sistema con credenciales administrativas.</span><span class="sxs-lookup"><span data-stu-id="b1649-168">Run the installation at a command prompt with administrative credentials.</span></span>

2.  <span data-ttu-id="b1649-169">Implemente cada componente en un solo directorio.</span><span class="sxs-lookup"><span data-stu-id="b1649-169">Deploy each component to a single directory.</span></span> <span data-ttu-id="b1649-170">Si se ejecuta desde un recurso compartido de red, se necesita más tiempo para descomprimir el archivo. medv.</span><span class="sxs-lookup"><span data-stu-id="b1649-170">If run from a network share, a longer time is required to decompress the .medv file.</span></span>

3.  <span data-ttu-id="b1649-171">Como práctica recomendada, especifique que Windows Virtual PC y la revisión de Windows Virtual PC se instalen después del agente de host MED-V y los archivos de paquete del área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="b1649-171">As a best practice, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="b1649-172">Esto significa que Windows Update no causará ninguna interferencia con el proceso de instalación al requerir un reinicio.</span><span class="sxs-lookup"><span data-stu-id="b1649-172">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

4.  <span data-ttu-id="b1649-173">Reinicie el equipo una vez que haya finalizado el archivo por lotes.</span><span class="sxs-lookup"><span data-stu-id="b1649-173">Restart the computer after the batch file is finished.</span></span>

<span data-ttu-id="b1649-174">Después del reinicio, se le solicitará al usuario que ejecute la configuración por primera vez y se completará la configuración de MED-V.</span><span class="sxs-lookup"><span data-stu-id="b1649-174">After the restart, the user is prompted to run first time setup and complete the configuration of MED-V.</span></span>

<span data-ttu-id="b1649-175">En el siguiente ejemplo, con los argumentos especificados, se muestra cómo instalar componentes de MED-V de 64 bits en un único proceso:</span><span class="sxs-lookup"><span data-stu-id="b1649-175">The following example, with the specified arguments, shows how to install 64-bit MED-V components in a single process:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b1649-176">Argumento</span><span class="sxs-lookup"><span data-stu-id="b1649-176">Argument</span></span></th>
<th align="left"><span data-ttu-id="b1649-177">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1649-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1649-178">/norestart</span><span class="sxs-lookup"><span data-stu-id="b1649-178">/norestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1649-179">Impide que la instalación de Windows Virtual PC y la actualización de Virtual PC de Windows reinicie el equipo host.</span><span class="sxs-lookup"><span data-stu-id="b1649-179">Prevents the installation of Windows Virtual PC and the Windows Virtual PC update from restarting the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1649-180">/Quiet</span><span class="sxs-lookup"><span data-stu-id="b1649-180">/quiet</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1649-181">Instala los componentes de MED-V en modo silencioso sin interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="b1649-181">Installs the MED-V components in quiet mode without user interaction.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1649-182">/QN</span><span class="sxs-lookup"><span data-stu-id="b1649-182">/qn</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1649-183">Instala los componentes de MED-V sin una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b1649-183">Installs the MED-V components without a user interface.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b1649-184">IGNORE_PREREQUISITES</span><span class="sxs-lookup"><span data-stu-id="b1649-184">IGNORE_PREREQUISITES</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1649-185">Instala sin comprobar Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="b1649-185">Installs without checking for Windows Virtual PC.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="b1649-186">Nota</span><span class="sxs-lookup"><span data-stu-id="b1649-186">Note</span></span></strong><br/><p><span data-ttu-id="b1649-187">Especifique este argumento solo si va a instalar Windows Virtual PC como parte de esta instalación.</span><span class="sxs-lookup"><span data-stu-id="b1649-187">Only specify this argument if you are installing Windows Virtual PC as part of this installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b1649-188">OVERWRITEVHD</span><span class="sxs-lookup"><span data-stu-id="b1649-188">OVERWRITEVHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="b1649-189">Fuerza la instalación del área de trabajo de MED-V y evita las preguntas que pueda generar.</span><span class="sxs-lookup"><span data-stu-id="b1649-189">Forces the installation of the MED-V workspace and prevents any prompts that it might generate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="b1649-190">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1649-190">Example</span></span>


``` syntax
:: Install MED-V and the Pre-requisites

:: Install the MED-V Host Agent: install in quiet mode, ignore that Windows Virtual PC is not installed completely, and log results
start /WAIT .\MED-V_HostAgent_Setup.exe /qn IGNORE_PREREQUISITES=1 /l* %TEMP%\MEDVhost.log

:: Install the MED-V Workspace: install in quiet mode, Overwrite the VHD if it already exists, and log results
start /WAIT .\setup.exe /qn OVERWRITEVHD=1 /l* %TEMP%\MEDVworkspace.log

:: Install Windows Virtual PC: install in quiet mode and do not reboot
start /WAIT wusa.exe Windows6.1-KB958559-x64.msu /norestart /quiet

:: Install Windows Virtual PC patch to support non-HAV: install in quiet mode and do not reboot
wusa.exe Windows6.1-KB977206-x64.msu /norestart /quiet

:: After successful installation of the above components, a reboot of the host computer is required to complete installation.
```

## <span data-ttu-id="b1649-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1649-191">Related topics</span></span>


[<span data-ttu-id="b1649-192">Introducción a la implementación MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="b1649-192">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="b1649-193">Implementar los componentes MED-V</span><span class="sxs-lookup"><span data-stu-id="b1649-193">Deploy the MED-V Components</span></span>](deploy-the-med-v-components.md)









