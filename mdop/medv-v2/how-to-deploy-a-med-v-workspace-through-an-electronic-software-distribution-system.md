---
title: Cómo implementar un área de trabajo de MED-V a través de un sistema de distribución electrónica de Software
description: Cómo implementar un área de trabajo de MED-V a través de un sistema de distribución electrónica de Software
author: dansimp
ms.assetid: b5134c35-e1de-470c-93f8-ead6218d9dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 56d21b0c2f010f63c04056d9fadd7763531bd9d5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812991"
---
# <span data-ttu-id="8fa9f-103">Cómo implementar un área de trabajo de MED-V a través de un sistema de distribución electrónica de Software</span><span class="sxs-lookup"><span data-stu-id="8fa9f-103">How to Deploy a MED-V Workspace Through an Electronic Software Distribution System</span></span>


<span data-ttu-id="8fa9f-104">Un sistema electrónico de distribución de software está diseñado para mover el software de forma eficaz a muchos equipos distintos a través de conexiones de red lentas o rápidas.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-104">An electronic software distribution system is designed to efficiently move software to many different computers over slow or fast network connections.</span></span> <span data-ttu-id="8fa9f-105">La siguiente sección proporciona información e instrucciones para ayudarle a implementar el área de trabajo de MED-V en toda su empresa mediante un sistema de distribución de software.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-105">The following section provides information and instructions to help you deploy your MED-V workspace throughout your enterprise by using a software distribution system.</span></span>

**<span data-ttu-id="8fa9f-106">Nota</span><span class="sxs-lookup"><span data-stu-id="8fa9f-106">Note</span></span>**  
<span data-ttu-id="8fa9f-107">Sea cual sea la solución de distribución de software que use, debe estar familiarizado con los requisitos de su solución en particular.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-107">Whichever software distribution solution that you use, you must be familiar with the requirements of your particular solution.</span></span> <span data-ttu-id="8fa9f-108">Si está usando System Center Configuration Manager 2007 R2 o una versión posterior, consulte la [biblioteca de documentación de Configuration Manager](https://go.microsoft.com/fwlink/?LinkId=66999) en la biblioteca técnica de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=66999) .</span><span class="sxs-lookup"><span data-stu-id="8fa9f-108">If you are using System Center Configuration Manager 2007 R2 or a later version, see the [Configuration Manager Documentation Library](https://go.microsoft.com/fwlink/?LinkId=66999) in the Microsoft Technical Library (https://go.microsoft.com/fwlink/?LinkId=66999).</span></span>



**<span data-ttu-id="8fa9f-109">Importante</span><span class="sxs-lookup"><span data-stu-id="8fa9f-109">Important</span></span>**  
<span data-ttu-id="8fa9f-110">Si está usando System Center Configuration Manager 2007 SP2 y las áreas de trabajo de MED-V están configuradas para funcionar en modo **NAT** , las máquinas virtuales se clasifican como clientes basados en Internet y no pueden encontrar los puntos de distribución más cercanos para descargar contenido.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-110">If you are using System Center Configuration Manager 2007 SP2 and your MED-V workspaces are configured to operate in **NAT** mode, the virtual machines are classified as Internet-based clients and cannot find the closest distribution points from which to download content.</span></span>

<span data-ttu-id="8fa9f-111">El [hotfix para mejorar la funcionalidad de las VM administradas por Med-v](https://go.microsoft.com/fwlink/?LinkId=201088) ( https://go.microsoft.com/fwlink/?LinkId=201088) agrega nueva funcionalidad a las máquinas virtuales administradas por Med-v y que están configuradas para funcionar en modo **NAT** .</span><span class="sxs-lookup"><span data-stu-id="8fa9f-111">The [hotfix to improve the functionality for VMs that are managed by MED-V](https://go.microsoft.com/fwlink/?LinkId=201088) (https://go.microsoft.com/fwlink/?LinkId=201088) adds new functionality to virtual machines that are managed by MED-V and that are configured to operate in **NAT** mode.</span></span> <span data-ttu-id="8fa9f-112">La nueva funcionalidad permite que las máquinas virtuales tengan acceso a los puntos de distribución más cercanos.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-112">The new functionality lets virtual machines access the closest distribution points.</span></span> <span data-ttu-id="8fa9f-113">Por lo tanto, el administrador puede administrar la máquina virtual y el equipo host de la misma manera.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-113">Therefore, the administrator can manage the virtual machine and the host computer in the same manner.</span></span> <span data-ttu-id="8fa9f-114">Este Hotfix debe instalarse primero en el servidor del sitio y, después, en el cliente.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-114">This hotfix must be installed first on the site server and then on the client.</span></span>

<span data-ttu-id="8fa9f-115">La actualización está disponible públicamente.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-115">The update is publicly available.</span></span> <span data-ttu-id="8fa9f-116">Sin embargo, es posible que se le pida que acepte un contrato de servicios de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-116">However, you might be prompted to accept an agreement for Microsoft Services.</span></span> <span data-ttu-id="8fa9f-117">Siga las indicaciones en las páginas web sucesivas para recuperar este Hotfix.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-117">Follow the prompts on the successive webpages to retrieve this hotfix.</span></span>



<span data-ttu-id="8fa9f-118">También puede implementar los componentes de MED-V juntos mediante un archivo de proceso por lotes, pero para ello es necesario reiniciar después de la instalación de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-118">You can also deploy the MED-V components together by using a batch file, but this requires a restart after the installation of Windows Virtual PC.</span></span> <span data-ttu-id="8fa9f-119">Para evitar este requisito, puede especificar un solo reinicio una vez que se hayan instalado todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-119">To bypass this requirement, you can specify a single restart after all of the components are installed.</span></span> <span data-ttu-id="8fa9f-120">El reinicio único también inicia de forma automática MED-V porque la instalación del área de trabajo MED-V coloca una entrada en el RUNKEY.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-120">The single restart also automatically starts MED-V because the MED-V workspace installation places an entry in the RUNKEY.</span></span>

**<span data-ttu-id="8fa9f-121">Para implementar un área de trabajo de MED-V mediante un sistema de distribución de software</span><span class="sxs-lookup"><span data-stu-id="8fa9f-121">To deploy a MED-V workspace by using a software distribution system</span></span>**

1.  <span data-ttu-id="8fa9f-122">Definir un grupo de equipos y usuarios en el sistema electrónico de distribución de software como el conjunto de destino de equipos o usuarios.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-122">Define a group of computers and users in the electronic software distribution system as the target set of computers/users.</span></span>

2.  <span data-ttu-id="8fa9f-123">Cree paquetes para cada archivo de instalación de Microsoft que deba distribuirse.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-123">Create packages for each Microsoft installation file that needs to be distributed.</span></span> <span data-ttu-id="8fa9f-124">A continuación se indican los archivos necesarios y el orden en el que se deben instalar:</span><span class="sxs-lookup"><span data-stu-id="8fa9f-124">The following are the required files and the order in which they must be installed:</span></span>

    1.  <span data-ttu-id="8fa9f-125">**Windows Virtual PC** : Si no está instalado (es necesario reiniciar el equipo).</span><span class="sxs-lookup"><span data-stu-id="8fa9f-125">**Windows Virtual PC** – if not already installed (a computer restart is required).</span></span> <span data-ttu-id="8fa9f-126">Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="8fa9f-126">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    2.  <span data-ttu-id="8fa9f-127">**Adiciones y actualizaciones de Windows Virtual PC** : Si aún no están instaladas.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-127">**Windows Virtual PC Additions and Updates** – if not already installed.</span></span> <span data-ttu-id="8fa9f-128">Para obtener más información, vea [configurar los requisitos previos de instalación](configure-installation-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="8fa9f-128">For more information, see [Configure Installation Prerequisites](configure-installation-prerequisites.md).</span></span>

    3.  <span data-ttu-id="8fa9f-129">**Archivo de instalación del agente de host Med-v** : instala el agente de host (MED-v \ _HostAgent \ _setup archivo de instalación).</span><span class="sxs-lookup"><span data-stu-id="8fa9f-129">**MED-V Host Agent Installation File** – installs the Host Agent (MED-V\_HostAgent\_Setup installation file).</span></span> <span data-ttu-id="8fa9f-130">Para obtener más información, vea [Cómo instalar manualmente el agente de host MED-V](how-to-manually-install-the-med-v-host-agent.md).</span><span class="sxs-lookup"><span data-stu-id="8fa9f-130">For more information, see [How to Manually Install the MED-V Host Agent](how-to-manually-install-the-med-v-host-agent.md).</span></span>

        **<span data-ttu-id="8fa9f-131">Advertencia</span><span class="sxs-lookup"><span data-stu-id="8fa9f-131">Warning</span></span>**  
        <span data-ttu-id="8fa9f-132">Cierre Internet Explorer antes de instalar el agente de host MED-V; de lo contrario, los conflictos pueden producirse posteriormente con el redireccionamiento de URL.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-132">Close Internet Explorer before you install the MED-V Host Agent, otherwise conflicts can occur later with URL redirection.</span></span> <span data-ttu-id="8fa9f-133">También puede hacerlo especificando un reinicio del equipo durante una distribución.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-133">You can also do this by specifying a computer restart during a distribution.</span></span>



    4.  <span data-ttu-id="8fa9f-134">**Instalador de área de trabajo de Med-v, VHD y ejecutable de configuración** : creados en el **Empaquetador de área de trabajo de Med-v**.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-134">**MED-V Workspace Installer, VHD, and Setup Executable** – created in the **MED-V Workspace Packager**.</span></span> <span data-ttu-id="8fa9f-135">Para obtener más información, vea [crear un paquete de área de trabajo de MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="8fa9f-135">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

        **<span data-ttu-id="8fa9f-136">Importante</span><span class="sxs-lookup"><span data-stu-id="8fa9f-136">Important</span></span>**  
        <span data-ttu-id="8fa9f-137">El archivo de disco duro virtual comprimido (. medv) y el programa de instalación ejecutable (setup.exe) deben estar en la misma carpeta que el instalador del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-137">The compressed virtual hard disk file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.</span></span> <span data-ttu-id="8fa9f-138">Después, instale el instalador de área de trabajo MED-V ejecutando setup.exe.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-138">Then, install the MED-V workspace installer by running setup.exe.</span></span>



~~~
    **Tip**  
    Because problems can occur when you install MED-V from a network location, we recommend that you copy the MED-V workspace setup files locally and then run setup.exe.
~~~



3. <span data-ttu-id="8fa9f-139">Configure los paquetes para que se ejecuten en modo silencioso (no es necesaria la intervención del usuario).</span><span class="sxs-lookup"><span data-stu-id="8fa9f-139">Configure the packages to run in silent mode (no user interaction is required).</span></span>

   <span data-ttu-id="8fa9f-140">Si se ejecuta en modo silencioso, se elimina la solicitud de cerrar Internet Explorer si está en ejecución y se pide iniciar el agente de host MED-V.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-140">Running in silent mode eliminates the prompt to close Internet Explorer if it is running and the prompt to start the MED-V Host Agent.</span></span> <span data-ttu-id="8fa9f-141">Ambas acciones se realizan cuando se reinicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-141">Both actions are performed when the computer is restarted.</span></span>

   **<span data-ttu-id="8fa9f-142">Nota</span><span class="sxs-lookup"><span data-stu-id="8fa9f-142">Note</span></span>**  
   <span data-ttu-id="8fa9f-143">La instalación de Windows Virtual PC requiere que reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-143">Installation of Windows Virtual PC requires you to restart the computer.</span></span> <span data-ttu-id="8fa9f-144">Puede crear un único proceso de instalación e instalar todos los componentes al mismo tiempo si elimina el reinicio e ignora los requisitos previos necesarios para que MED-V se instale.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-144">You can create a single installation process and install all the components at the same time if you suppress the restart and ignore the prerequisites necessary for MED-V to install.</span></span> <span data-ttu-id="8fa9f-145">También puede hacerlo con los argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-145">You can also do this by using command-line arguments.</span></span> <span data-ttu-id="8fa9f-146">Para obtener un ejemplo de estos argumentos, consulte [cómo implementar los componentes de MED-V a través de un sistema electrónico de distribución de software](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md#bkmk-batch).</span><span class="sxs-lookup"><span data-stu-id="8fa9f-146">For an example of these arguments, see [How to Deploy the MED-V Components Through an Electronic Software Distribution System](how-to-deploy-the-med-v-components-through-an-electronic-software-distribution-system.md#bkmk-batch).</span></span> <span data-ttu-id="8fa9f-147">MED-V se inicia automáticamente cuando se reinicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-147">MED-V automatically starts when the computer is restarted.</span></span>



4. <span data-ttu-id="8fa9f-148">Instale MED-V y sus componentes antes de instalar Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-148">Install MED-V and its components before installing Windows Virtual PC.</span></span> <span data-ttu-id="8fa9f-149">Vea el archivo de proceso por lotes de ejemplo más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-149">See the example batch file later in this topic.</span></span>

   **<span data-ttu-id="8fa9f-150">Importante</span><span class="sxs-lookup"><span data-stu-id="8fa9f-150">Important</span></span>**  
   <span data-ttu-id="8fa9f-151">Seleccione la opción **omitir \ _PREREQUISITES** como se muestra en el archivo de proceso por lotes de ejemplo para que los componentes de MED-V puedan instalarse antes que los componentes de VPC requeridos.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-151">Select the **IGNORE\_PREREQUISITES** option as shown in the example batch file so that the MED-V components can be installed prior to the required VPC components.</span></span> <span data-ttu-id="8fa9f-152">Instale los componentes de MED-V en este orden para permitir el reinicio único.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-152">Install the MED-V components in this order to allow for the single restart.</span></span>



5. <span data-ttu-id="8fa9f-153">Identifique cualquier otro requisito necesario para la instalación y para el sistema de distribución de software, como plataformas de destino y el espacio libre en disco.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-153">Identify any other requirements necessary for the installation and for your software distribution system, such as target platforms and the free disk space.</span></span>

6. <span data-ttu-id="8fa9f-154">Asigne los paquetes al conjunto de equipos de destino de equipos o usuarios.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-154">Assign the packages to the target set of computers/users.</span></span>

   <span data-ttu-id="8fa9f-155">Mientras se ejecutan los equipos, el cliente del sistema de distribución de software reconoce que hay nuevos paquetes disponibles y comienza a instalar los paquetes según la definición y los requisitos.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-155">As computers are running, the software distribution system client recognizes that new packages are available and begins to install the packages per the definition and requirements.</span></span> <span data-ttu-id="8fa9f-156">Las instalaciones deben ejecutarse secuencialmente en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-156">The installations should run sequentially in silent.</span></span> <span data-ttu-id="8fa9f-157">Recomendamos que se realice como un único proceso que no requiera reiniciar hasta que se instalen todos los paquetes.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-157">We recommend that this is performed as a single process that does not require a restart until all the packages are installed.</span></span>

7. <span data-ttu-id="8fa9f-158">Una vez completadas las instalaciones, reinicie los equipos actualizados.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-158">After the installations are complete, restart the updated computers.</span></span>

   <span data-ttu-id="8fa9f-159">Según el sistema de distribución de software, puede programar un reinicio del equipo o los usuarios finales podrán reiniciar los equipos manualmente durante su trabajo normal.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-159">Depending on the software distribution system, you can schedule a restart of the computer or the end users can restart the computers manually during their regular work.</span></span> <span data-ttu-id="8fa9f-160">Después de reiniciar el equipo, MED-V se inicia automáticamente después de que un usuario final inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-160">After the computer is restarted, MED-V automatically starts after an end user logs on.</span></span> <span data-ttu-id="8fa9f-161">Cuando MED-V se inicia por primera vez, se ejecuta la configuración primera vez.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-161">When MED-V starts for the first time, it runs first time setup.</span></span>

<span data-ttu-id="8fa9f-162">La configuración comienza por primera vez y puede tardar varios minutos en completarse, según el tamaño del disco duro virtual que especificó y el número de directivas aplicadas al área de trabajo de MED-V en el inicio.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-162">First time setup starts and might take several minutes to finish, depending on the size of the virtual hard disk that you specified and the number of policies applied to the MED-V workspace on startup.</span></span> <span data-ttu-id="8fa9f-163">El usuario final puede realizar un seguimiento del progreso observando el icono de MED-V en el área de notificación.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-163">The end user can track the progress by watching the MED-V icon in the notification area.</span></span> <span data-ttu-id="8fa9f-164">Para obtener más información sobre la configuración de la primera vez, vea [información general sobre la implementación de 2,0 MED-V](med-v-20-deployment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8fa9f-164">For more information about first time setup, see [MED-V 2.0 Deployment Overview](med-v-20-deployment-overview.md).</span></span>

**<span data-ttu-id="8fa9f-165">Para instalar el área de trabajo de MED-V mediante un archivo por lotes</span><span class="sxs-lookup"><span data-stu-id="8fa9f-165">To install the MED-V workspace by using a batch file</span></span>**

1.  <span data-ttu-id="8fa9f-166">Ejecute la instalación en un símbolo del sistema con credenciales administrativas.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-166">Run the installation at a command prompt with administrative credentials.</span></span>

2.  <span data-ttu-id="8fa9f-167">Implemente cada componente en un solo directorio.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-167">Deploy each component to a single directory.</span></span> <span data-ttu-id="8fa9f-168">Si se ejecuta desde un recurso compartido de red, se necesita más tiempo para descomprimir el archivo. medv.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-168">If run from a network share, a longer time is required to decompress the .medv file.</span></span>

3.  <span data-ttu-id="8fa9f-169">Como práctica recomendada, especifique que Windows Virtual PC y la revisión de Windows Virtual PC se instalen después del agente de host MED-V y los archivos de paquete del área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-169">As a best practice, specify that Windows Virtual PC and the Windows Virtual PC hotfix are installed after the MED-V Host Agent and the MED-V workspace package files.</span></span> <span data-ttu-id="8fa9f-170">Esto significa que Windows Update no causará ninguna interferencia con el proceso de instalación al requerir un reinicio.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-170">This means that Windows Update will not cause any interference with the installation process by requiring a restart.</span></span>

4.  <span data-ttu-id="8fa9f-171">Reinicie el equipo una vez que haya finalizado el archivo por lotes.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-171">Restart the computer after the batch file is finished.</span></span>

<span data-ttu-id="8fa9f-172">Después del reinicio, se le solicitará al usuario que ejecute la configuración por primera vez y se completará la configuración de MED-V.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-172">After the restart, the user is prompted to run first time setup and complete the configuration of MED-V.</span></span>

<span data-ttu-id="8fa9f-173">En el siguiente ejemplo, con los argumentos especificados, se muestra cómo instalar componentes de MED-V de 64 bits en un único proceso:</span><span class="sxs-lookup"><span data-stu-id="8fa9f-173">The following example, with the specified arguments, shows how to install 64-bit MED-V components in a single process:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8fa9f-174">Argumento</span><span class="sxs-lookup"><span data-stu-id="8fa9f-174">Argument</span></span></th>
<th align="left"><span data-ttu-id="8fa9f-175">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fa9f-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fa9f-176">/norestart</span><span class="sxs-lookup"><span data-stu-id="8fa9f-176">/norestart</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fa9f-177">Impide que la instalación de Windows Virtual PC y la actualización de Virtual PC de Windows reinicie el equipo host.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-177">Prevents the installation of Windows Virtual PC and the Windows Virtual PC update from restarting the host computer.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8fa9f-178">/Quiet</span><span class="sxs-lookup"><span data-stu-id="8fa9f-178">/quiet</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fa9f-179">Instala los componentes de MED-V en modo silencioso sin interacción del usuario.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-179">Installs the MED-V components in quiet mode without user interaction.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fa9f-180">/QN</span><span class="sxs-lookup"><span data-stu-id="8fa9f-180">/qn</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fa9f-181">Instala los componentes de MED-V sin una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-181">Installs the MED-V components without a user interface.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8fa9f-182">IGNORE_PREREQUISITES</span><span class="sxs-lookup"><span data-stu-id="8fa9f-182">IGNORE_PREREQUISITES</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fa9f-183">Instala sin comprobar Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-183">Installs without checking for Windows Virtual PC.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="8fa9f-184">Nota</span><span class="sxs-lookup"><span data-stu-id="8fa9f-184">Note</span></span></strong><br/><p><span data-ttu-id="8fa9f-185">Especifique este argumento solo si va a instalar Windows Virtual PC como parte de esta instalación.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-185">Only specify this argument if you are installing Windows Virtual PC as part of this installation.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8fa9f-186">OVERWRITEVHD</span><span class="sxs-lookup"><span data-stu-id="8fa9f-186">OVERWRITEVHD</span></span></p></td>
<td align="left"><p><span data-ttu-id="8fa9f-187">Fuerza la instalación del área de trabajo de MED-V y evita las preguntas que pueda generar.</span><span class="sxs-lookup"><span data-stu-id="8fa9f-187">Forces the installation of the MED-V workspace and prevents any prompts that it might generate.</span></span></p></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="8fa9f-188">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8fa9f-188">Example</span></span>


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

## <span data-ttu-id="8fa9f-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8fa9f-189">Related topics</span></span>


[<span data-ttu-id="8fa9f-190">Introducción a la implementación MED-V 2.0</span><span class="sxs-lookup"><span data-stu-id="8fa9f-190">MED-V 2.0 Deployment Overview</span></span>](med-v-20-deployment-overview.md)

[<span data-ttu-id="8fa9f-191">Cómo implementar un área de trabajo de MED-V en una imagen de Windows 7</span><span class="sxs-lookup"><span data-stu-id="8fa9f-191">How to Deploy a MED-V Workspace in a Windows 7 Image</span></span>](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)









