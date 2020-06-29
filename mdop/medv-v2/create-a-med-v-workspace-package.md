---
title: Crear un paquete de área de trabajo de MED-V
description: Crear un paquete de área de trabajo de MED-V
author: dansimp
ms.assetid: 3f75fe73-41ac-4389-ae21-5efb2d437f4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e20cf4cc9394c4a5e90178fff4fc36ed83c12d60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823261"
---
# <span data-ttu-id="97c00-103">Crear un paquete de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="97c00-103">Create a MED-V Workspace Package</span></span>


<span data-ttu-id="97c00-104">Un área de trabajo de MED-V es el entorno de escritorio de Windows XP en el que los usuarios finales interactúan con la máquina virtual proporcionada por MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-104">A MED-V workspace is the Windows XP desktop environment where end users interact with the virtual machine provided by MED-V.</span></span> <span data-ttu-id="97c00-105">El administrador crea y personaliza el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-105">The administrator creates and customizes the MED-V workspace.</span></span> <span data-ttu-id="97c00-106">El área de trabajo consta de una imagen y la Directiva de grupo que define las reglas y la funcionalidad del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-106">The workspace consists of an image and the Group Policy that defines the rules and functionality of the MED-V workspace.</span></span>

<span data-ttu-id="97c00-107">Puede crear varias áreas de trabajo de MED-V, cada una personalizada con su propia configuración, configuración y reglas.</span><span class="sxs-lookup"><span data-stu-id="97c00-107">You can create multiple MED-V workspaces, each customized with its own configuration, settings, and rules.</span></span> <span data-ttu-id="97c00-108">Un usuario, grupo o varios usuarios o grupos pueden estar asociados a cada área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-108">A user, group, or multiple users or groups can be associated with each MED-V workspace.</span></span> <span data-ttu-id="97c00-109">La personalización hace que el área de trabajo de MED-V solo esté disponible para ese usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="97c00-109">The customization makes that MED-V workspace available only for that user or group.</span></span>

<span data-ttu-id="97c00-110">Use el **Empaquetador de área de trabajo de Med-v** para crear áreas de trabajo de Med-v.</span><span class="sxs-lookup"><span data-stu-id="97c00-110">Use the **MED-V Workspace Packager** to create MED-V workspaces.</span></span> <span data-ttu-id="97c00-111">El **paquete del área de trabajo MED-V** se divide en dos secciones principales:</span><span class="sxs-lookup"><span data-stu-id="97c00-111">The **MED-V Workspace Packager** is divided into two main sections:</span></span>

-   <span data-ttu-id="97c00-112">Panel principal que incluye tres botones que se usan para crear y administrar áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-112">A main panel that includes three buttons that you use to create and manage MED-V workspaces.</span></span> <span data-ttu-id="97c00-113">El botón **crear un paquete de área de trabajo Med-v** abre el **Asistente para crear un área de trabajo Med-v** que se usa para crear las áreas de trabajo de Med-v.</span><span class="sxs-lookup"><span data-stu-id="97c00-113">The **Create a MED-V Workspace Package** button opens the **Create MED-V Workspace Package Wizard** that you use to create your MED-V workspaces.</span></span>

-   <span data-ttu-id="97c00-114">**Centro de ayuda** , situado en la parte derecha de la ventana, que proporciona información e instrucciones para ayudarle a crear, probar y administrar sus áreas de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-114">A **Help Center** on the right-hand side of the window that provides information and guidance to help you create, test, and manage your MED-V workspaces.</span></span>

**<span data-ttu-id="97c00-115">Importante</span><span class="sxs-lookup"><span data-stu-id="97c00-115">Important</span></span>**  
<span data-ttu-id="97c00-116">Para poder usar el **Empaquetador de área de trabajo de MED-V**, primero debe asegurarse de que la Directiva de ejecución de Windows PowerShell esté establecida en no restringido.</span><span class="sxs-lookup"><span data-stu-id="97c00-116">Before you can use the **MED-V Workspace Packager**, you must first make sure that the Windows PowerShell execution policy is set to Unrestricted.</span></span>

`Set-ExecutionPolicy Unrestricted`

<span data-ttu-id="97c00-117">Además, la Directiva SAN del equipo en el que se ejecuta el **paquete de área de trabajo MED-V** debe establecerse en "conectado a todos".</span><span class="sxs-lookup"><span data-stu-id="97c00-117">In addition, the SAN policy for the computer on which the **MED-V Workspace Packager** is run must be set to “Online All”.</span></span> <span data-ttu-id="97c00-118">Para comprobar la configuración de la Directiva SAN, ejecute los siguientes comandos en un símbolo del sistema con credenciales administrativas:</span><span class="sxs-lookup"><span data-stu-id="97c00-118">To check the setting of the SAN policy, run the following commands at a command prompt with administrative credentials:</span></span>

`diskpart.exe`

`DISKPART> san`

`DISKPART> exit`

<span data-ttu-id="97c00-119">Si es necesario, cambie la Directiva SAN a "en línea todo" escribiendo los siguientes comandos en el símbolo del sistema con credenciales administrativas:</span><span class="sxs-lookup"><span data-stu-id="97c00-119">If it is necessary, change the SAN policy to "Online All" by typing the following commands at the command prompt with administrative credentials:</span></span>

`diskpart.exe`

`DISKPART> san policy=onlineall`

`DISKPART> exit`



**<span data-ttu-id="97c00-120">Importante</span><span class="sxs-lookup"><span data-stu-id="97c00-120">Important</span></span>**  
<span data-ttu-id="97c00-121">Si el software de cifrado de disco automático está instalado en el equipo que usa para montar el disco duro virtual y crear el paquete de área de trabajo MED-V, debe deshabilitar el software antes de empezar.</span><span class="sxs-lookup"><span data-stu-id="97c00-121">If automatic disk encryption software is installed on the computer that you use to mount the virtual hard disk and build the MED-V workspace package, you must disable the software before you start.</span></span> <span data-ttu-id="97c00-122">De lo contrario, no puede usar el área de trabajo de MED-V en ningún otro equipo.</span><span class="sxs-lookup"><span data-stu-id="97c00-122">Otherwise, you cannot use the MED-V workspace on any other computer.</span></span>



<span data-ttu-id="97c00-123">La información que proporcionamos aquí puede ayudarle a crear su paquete de implementación de área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-123">The information we provide here can help you create your MED-V workspace deployment package.</span></span>

## <a href="" id="bkmk-prereq"></a><span data-ttu-id="97c00-124">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="97c00-124">Prerequisites</span></span>


<span data-ttu-id="97c00-125">Antes de empezar a crear el paquete de implementación de área de trabajo de MED-V, compruebe que tiene acceso a los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="97c00-125">Before you start to build your MED-V workspace deployment package, verify that you have access to the following items:</span></span>

-   **<span data-ttu-id="97c00-126">Una imagen de Windows XP preparada</span><span class="sxs-lookup"><span data-stu-id="97c00-126">A prepared Windows XP image</span></span>**

    <span data-ttu-id="97c00-127">Para obtener más información sobre cómo crear una imagen de Windows XP para usarla con MED-V, vea [preparar una imagen de Med-v](prepare-a-med-v-image.md).</span><span class="sxs-lookup"><span data-stu-id="97c00-127">For more information about how to create a Windows XP image for use with MED-V, see [Prepare a MED-V Image](prepare-a-med-v-image.md).</span></span>

-   **<span data-ttu-id="97c00-128">Un archivo de texto o lista que contiene información sobre el redireccionamiento de la dirección URL</span><span class="sxs-lookup"><span data-stu-id="97c00-128">A text file or list that contains URL redirection information</span></span>**

    <span data-ttu-id="97c00-129">La lista o archivo de texto de redirección de URL contiene las direcciones URL que desea que se redirijan desde el equipo host a Internet Explorer en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-129">Your URL redirection text file or list contains those URLs that you want redirected from the host computer to Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="97c00-130">Cuando use el Asistente para empaquetar para crear el área de trabajo de MED-V, importe, escriba o copie y pegue esta información de redireccionamiento como uno de los pasos del proceso de creación del paquete.</span><span class="sxs-lookup"><span data-stu-id="97c00-130">When you are using the packaging wizard to create your MED-V workspace, you import, type, or copy and paste this redirection information as one of the steps in the package creation process.</span></span>

    **<span data-ttu-id="97c00-131">Nota</span><span class="sxs-lookup"><span data-stu-id="97c00-131">Note</span></span>**  
    <span data-ttu-id="97c00-132">El redireccionamiento de direcciones URL en MED-V solo admite los protocolos HTTP y HTTPS.</span><span class="sxs-lookup"><span data-stu-id="97c00-132">URL redirection in MED-V only supports the protocols HTTP and HTTPS.</span></span> <span data-ttu-id="97c00-133">MED-V no proporciona soporte técnico para FTP ni para otros protocolos.</span><span class="sxs-lookup"><span data-stu-id="97c00-133">MED-V does not provide support for FTP or any other protocols.</span></span>



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



## <span data-ttu-id="97c00-134">Empaquetar un área de trabajo de MED-V para un idioma distinto del idioma del equipo del paquete del área de trabajo MED-V</span><span class="sxs-lookup"><span data-stu-id="97c00-134">Packaging a MED-V Workspace for a Language Other than the Language of the MED-V Workspace Packager Computer</span></span>


<span data-ttu-id="97c00-135">De forma predeterminada, el área de trabajo de MED-V admite caracteres en el idioma del equipo y en inglés.</span><span class="sxs-lookup"><span data-stu-id="97c00-135">By default, the MED-V workspace supports characters in both the language of the computer and in English.</span></span> <span data-ttu-id="97c00-136">Para crear un área de trabajo de MED-V para un idioma distinto del que está instalado en el equipo, especifique **-Loc \ [locale \]** en el script de PowerShell (. PS1) después del nombre del área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-136">To create a MED-V workspace for a language other than the one installed on the computer, specify **-loc \[locale\]** in the PowerShell script (.ps1) after the MED-V workspace name.</span></span>

<span data-ttu-id="97c00-137">Para crear un paquete de área de trabajo de MED-V en un idioma que no sea el predeterminado del equipo del paquete del área de trabajo MED-V, genere un script en el idioma predeterminado ejecutando el Empaquetador de área de trabajo MED-V y, a continuación, modifique la secuencia de comandos de salida según sea necesario para su configuración regional.</span><span class="sxs-lookup"><span data-stu-id="97c00-137">To create a MED-V workspace package in a language other than the default language of the MED-V Workspace Packager computer, generate a script in the default language by running the MED-V Workspace Packager and then modifying the output script as required for your locale.</span></span> <span data-ttu-id="97c00-138">El script se encuentra en el directorio de salida del área de trabajo de MED-V que se especificó durante el embalaje.</span><span class="sxs-lookup"><span data-stu-id="97c00-138">The script is located in the MED-V workspace output directory that was specified during packaging.</span></span> <span data-ttu-id="97c00-139">Los nombres de la configuración regional están en el. WXL archivos en el siguiente directorio:</span><span class="sxs-lookup"><span data-stu-id="97c00-139">The names of the locale settings are on the .WXL files in the following directory:</span></span>

<span data-ttu-id="97c00-140">C:\\Archivos de escritorio de Programa\\microsoft Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale</span><span class="sxs-lookup"><span data-stu-id="97c00-140">C:\\Program Files\\Microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale</span></span>

## <span data-ttu-id="97c00-141">Crear un paquete de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="97c00-141">Creating a MED-V Workspace Package</span></span>


<span data-ttu-id="97c00-142">Para crear un paquete de área de trabajo de MED-V, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="97c00-142">To create a MED-V workspace package, follow these steps:</span></span>

****

1.  <span data-ttu-id="97c00-143">Para abrir el **Empaquetador de área de trabajo de MED-V**, haga clic en **Inicio**, haga clic en **todos los programas**, en **Microsoft Enterprise Desktop Virtualization**y, a continuación, haga clic en **Empaquetador de área de trabajo de MED-V**.</span><span class="sxs-lookup"><span data-stu-id="97c00-143">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2.  <span data-ttu-id="97c00-144">En el panel principal de **empaquetador del área de trabajo de Med-v** , haga clic en **crear un paquete de área de trabajo Med-v**.</span><span class="sxs-lookup"><span data-stu-id="97c00-144">On the **MED-V Workspace Packager** main panel, click **Create a MED-V Workspace Package**.</span></span>

    <span data-ttu-id="97c00-145">Aparecerá el **Asistente para crear paquete de área de trabajo** Med-v.</span><span class="sxs-lookup"><span data-stu-id="97c00-145">The MED-V **Create MED-V Workspace Package Wizard** appears.</span></span> <span data-ttu-id="97c00-146">El asistente consta de las siguientes páginas:</span><span class="sxs-lookup"><span data-stu-id="97c00-146">The wizard consists of the following pages:</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="97c00-147">Información de paquete</span><span class="sxs-lookup"><span data-stu-id="97c00-147">Package Information</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="97c00-148">Especifique un nombre para el área de trabajo de MED-V y seleccione una carpeta en la que se guarden los archivos de paquete del área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-148">Specify a name for the MED-V workspace and select a folder where the MED-V workspace package files are saved.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="97c00-149">Seleccionar imagen de Windows XP</span><span class="sxs-lookup"><span data-stu-id="97c00-149">Select Windows XP Image</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="97c00-150">Especifique su imagen de Virtual PC de Windows XP preparada.</span><span class="sxs-lookup"><span data-stu-id="97c00-150">Specify your prepared Windows XP Virtual PC image.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="97c00-151">Configuración de primera vez</span><span class="sxs-lookup"><span data-stu-id="97c00-151">First Time Setup</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="97c00-152">Especificar el proceso de configuración que MED-V seguirá durante la configuración de la primera vez.</span><span class="sxs-lookup"><span data-stu-id="97c00-152">Specify the setup process that MED-V follows during first time setup.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="97c00-153">Mensajes MED-V</span><span class="sxs-lookup"><span data-stu-id="97c00-153">MED-V Messages</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="97c00-154">Especifique los mensajes y la dirección URL opcional de la información de ayuda que el usuario final verá durante la configuración primera vez.</span><span class="sxs-lookup"><span data-stu-id="97c00-154">Specify the messages and optional URL for Help information that the end user sees during first time setup.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="97c00-155">Asignar nombres a equipos</span><span class="sxs-lookup"><span data-stu-id="97c00-155">Naming Computers</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="97c00-156">Especifique cómo se denomina la máquina virtual de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-156">Specify how the MED-V virtual machine is named.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="97c00-157">Copiar configuración del host</span><span class="sxs-lookup"><span data-stu-id="97c00-157">Copy Settings from Host</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="97c00-158">Especifique cómo se definen los valores para el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-158">Specify how the settings for the MED-V workspace are defined.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="97c00-159">Inicio y redes</span><span class="sxs-lookup"><span data-stu-id="97c00-159">Startup and Networking</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="97c00-160">Especifique la configuración para iniciar el área de trabajo de MED-V, las redes y las credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="97c00-160">Specify the settings for starting the MED-V workspace, networking, and user credentials.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong><span data-ttu-id="97c00-161">Redireccionamiento web</span><span class="sxs-lookup"><span data-stu-id="97c00-161">Web Redirection</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="97c00-162">Especifique un archivo de texto o una lista de las direcciones URL que desea redirigir a Internet Explorer en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-162">Specify a text file or a list of the URLs you want redirected to Internet Explorer in the MED-V workspace.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong><span data-ttu-id="97c00-163">Resumen</span><span class="sxs-lookup"><span data-stu-id="97c00-163">Summary</span></span></strong></p></td>
    <td align="left"><p><span data-ttu-id="97c00-164">Compruebe la configuración del área de trabajo de MED-V y empiece a crear su paquete de implementación de área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-164">Verify your MED-V workspace settings and start to build your MED-V workspace deployment package.</span></span></p></td>
    </tr>
    </tbody>
    </table>



3.  <span data-ttu-id="97c00-165">En la página **información del paquete** , escriba un nombre para el área de trabajo de Med-v y seleccione una carpeta en la que se guarden los archivos de paquete del área de trabajo de Med-v.</span><span class="sxs-lookup"><span data-stu-id="97c00-165">On the **Package Information** page, enter a name for the MED-V workspace and select a folder where the MED-V workspace package files are saved.</span></span>

    **<span data-ttu-id="97c00-166">Advertencia</span><span class="sxs-lookup"><span data-stu-id="97c00-166">Warning</span></span>**  
    <span data-ttu-id="97c00-167">Debe nombrar el área de trabajo de MED-V y especificar una carpeta para continuar.</span><span class="sxs-lookup"><span data-stu-id="97c00-167">You must name the MED-V workspace and specify a folder to continue.</span></span>



~~~
After you have finished, click **Next**.
~~~

4. <span data-ttu-id="97c00-168">En la página **seleccionar imagen de Windows XP** , especifique la ubicación de su imagen de Virtual PC de Windows XP de MED-V preparada (archivo. vhd).</span><span class="sxs-lookup"><span data-stu-id="97c00-168">On the **Select Windows XP Image** page, specify the location of your prepared MED-V Windows XP Virtual PC image (.vhd file).</span></span>

   **<span data-ttu-id="97c00-169">Advertencia</span><span class="sxs-lookup"><span data-stu-id="97c00-169">Warning</span></span>**  
   <span data-ttu-id="97c00-170">Debe especificar una imagen de VHD de Windows XP para continuar.</span><span class="sxs-lookup"><span data-stu-id="97c00-170">You must specify a Windows XP VHD image to continue.</span></span>



~~~
After you have finished, click **Next**.
~~~

5. <span data-ttu-id="97c00-171">En la página **primera configuración** , seleccione si quiere que la configuración se ejecute por primera vez durante la versión atendida o desatendido y si desea que el área de trabajo de MED-V se use por separado o que todos los usuarios finales usen un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="97c00-171">On the **First Time Setup** page, select whether you want first time setup to run while attended or unattended and whether you want the MED-V workspace used separately or used by all end users on a shared computer.</span></span>

   <span data-ttu-id="97c00-172">Si selecciona la **instalación desatendida, sin ninguna notificación**, no se informa al usuario final antes de ejecutar la configuración por primera vez y la máquina virtual no se muestra al usuario final durante la configuración de la primera vez.</span><span class="sxs-lookup"><span data-stu-id="97c00-172">If you select **Unattended setup, without any notification**, the end user is not informed before first time setup is run and the virtual machine is not shown to the end user during first time setup.</span></span> <span data-ttu-id="97c00-173">Además, la página de **mensajes de MED-V** del asistente se oculta porque no se necesitan mensajes si la primera vez se ejecuta el programa de instalación en modo desatendido.</span><span class="sxs-lookup"><span data-stu-id="97c00-173">In addition, the **MED-V Messages** page of the wizard is hidden because no messages are required if first time setup runs in a completely unattended mode.</span></span>

   <span data-ttu-id="97c00-174">Si selecciona la **configuración desatendida, pero notificar a los usuarios finales antes de que empiece la configuración por primera vez**, se informa al usuario final antes de ejecutar la instalación por primera vez.</span><span class="sxs-lookup"><span data-stu-id="97c00-174">If you select **Unattended setup, but notify end users before first time setup begins**, the end user is informed before first time setup is run.</span></span> <span data-ttu-id="97c00-175">Sin embargo, la máquina virtual no se muestra al usuario final durante la configuración de la primera vez.</span><span class="sxs-lookup"><span data-stu-id="97c00-175">However, the virtual machine is not shown to the end user during first time setup.</span></span>

   <span data-ttu-id="97c00-176">Seleccione **configuración atendida** si el usuario final debe especificar la información durante la configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="97c00-176">Select **Attended setup** if the end user must enter information during first time setup.</span></span>

   <span data-ttu-id="97c00-177">El comportamiento predeterminado es la **configuración desatendida, pero notifica a los usuarios finales antes de que empiece la configuración por primera vez**.</span><span class="sxs-lookup"><span data-stu-id="97c00-177">The default behavior is **Unattended setup, but notify end users before first time setup begins**.</span></span>

   **<span data-ttu-id="97c00-178">Actúe</span><span class="sxs-lookup"><span data-stu-id="97c00-178">Caution</span></span>**  
   <span data-ttu-id="97c00-179">Si creó el archivo Sysprep. inf para que la instalación mínima requiera que se complete la entrada del usuario, debe seleccionar la **configuración atendida** o los problemas pueden producirse durante la configuración de la primera vez.</span><span class="sxs-lookup"><span data-stu-id="97c00-179">If you created the Sysprep.inf file so that Mini-Setup requires user input to complete, you must select **Attended setup** or problems might occur during first time setup.</span></span>



~~~
You can also specify how a MED-V workspace is used on computers that are shared by multiple end users. You can decide that you want to create a unique MED-V workspace for each end user or that you want the MED-V workspace made available to all end users who share the computer. The default is that the MED-V workspace is unique for each end user.

**Important**  
We recommend that you disable the fast user switching feature in Windows if you configure the MED-V workspace to be accessed by all users on a shared computer. Problems can occur if an end user logs on by using the fast user switching feature in Windows when another user is still logged on.



**Tip**  
When you create a name mask for the MED-V workspace on the **Naming Computers** page, make sure that each virtual machine on a shared computer has a unique computer name.



You can also specify whether the MED-V workspace is added to the Administrators group or administrator credentials are managed outside MED-V. By default, the MED-V workspace is not automatically added to the Administrators group.

After you have finished, click **Next**.
~~~

6. <span data-ttu-id="97c00-180">En la página **mensajes de MED-V** , especifique los siguientes mensajes que el usuario final verá durante la configuración de primera vez:</span><span class="sxs-lookup"><span data-stu-id="97c00-180">On the **MED-V Messages** page, specify the following messages that the end user sees during first time setup:</span></span>

   -   <span data-ttu-id="97c00-181">Mensaje que el usuario final ve cuando comienza la configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="97c00-181">The message that the end user sees when first time setup starts.</span></span>

   -   <span data-ttu-id="97c00-182">Mensaje que verá el usuario final si se produce un error al configurar por primera vez o se produce un error.</span><span class="sxs-lookup"><span data-stu-id="97c00-182">The message that the end user sees if first time setup fails or an error occurs.</span></span>

   **<span data-ttu-id="97c00-183">Nota</span><span class="sxs-lookup"><span data-stu-id="97c00-183">Note</span></span>**  
   <span data-ttu-id="97c00-184">La página de **mensajes de MED-V** del asistente está oculta si seleccionó la **instalación desatendida, sin ninguna notificación** en la primera página de **configuración** .</span><span class="sxs-lookup"><span data-stu-id="97c00-184">The **MED-V Messages** page of the wizard is hidden if you selected **Unattended setup, without any notification** on the **First Time Setup** page.</span></span>



~~~
You can also specify an optional URL location for help information that is provided to the end user when first time setup is running.

For example, the URL can point to an internal IT webpage with answers to questions such as "How long will this take and how will I know when it has completed?" or "What do you do if you get an error message?"

**Note**  
If you specify a URL, a link is shown during first time setup that points the end user to this help information. If you do not specify a URL, no link is provided.



After you have finished, click **Next**.
~~~

7. <span data-ttu-id="97c00-185">En la página de **nombres de equipos** , puede especificar si los nombres de los equipos son administrados por MED-V o por una herramienta de administración del sistema, como Sysprep.</span><span class="sxs-lookup"><span data-stu-id="97c00-185">On the **Naming Computers** page, you can specify whether computer naming is managed by MED-V or by a system management tool, such as Sysprep.</span></span> <span data-ttu-id="97c00-186">La opción predeterminada es que la asignación de nombres de equipos sea administrada por una herramienta de administración del sistema.</span><span class="sxs-lookup"><span data-stu-id="97c00-186">The default is that computer naming is managed by a system management tool.</span></span>

   <span data-ttu-id="97c00-187">Si especifica que MED-V administra la asignación de nombres de equipos, seleccione una Convención de nomenclatura de equipos predefinida (máscara) en la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="97c00-187">If you specify that computer naming is managed by MED-V, select a predefined computer naming convention (mask) from the drop-down list.</span></span> <span data-ttu-id="97c00-188">Aparece una vista previa del nombre de un equipo de muestra que se basa en el equipo que está usando para crear el paquete de área de trabajo MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-188">A preview of a sample computer name appears that is based on the computer that you are using to build the MED-V workspace package.</span></span>

   <span data-ttu-id="97c00-189">Si selecciona una de las convenciones de nomenclatura personalizadas, los campos que puede especificar se limitan a los siguientes caracteres:</span><span class="sxs-lookup"><span data-stu-id="97c00-189">If you select one of the custom naming conventions, the fields you can specify are limited to the following characters:</span></span>

   -   <span data-ttu-id="97c00-190">Los campos prefijo y sufijo se limitan a los caracteres a-Z, a-z, 0-9 y los caracteres especiales.</span><span class="sxs-lookup"><span data-stu-id="97c00-190">The prefix and suffix fields are limited to the characters A-Z, a-z, 0-9, and the special characters !</span></span> <span data-ttu-id="97c00-191">@ \ # $% ^ & ()-\ _ ' {}.</span><span class="sxs-lookup"><span data-stu-id="97c00-191">@ \# $ % ^ & ( ) - \_ ' { } .</span></span> <span data-ttu-id="97c00-192">y ~.</span><span class="sxs-lookup"><span data-stu-id="97c00-192">and ~.</span></span>

   -   <span data-ttu-id="97c00-193">Los campos hostname y username se limitan a los dígitos del 0 al 9.</span><span class="sxs-lookup"><span data-stu-id="97c00-193">The hostname and username fields are limited to the digits 0 through 9.</span></span>

   **<span data-ttu-id="97c00-194">Importante</span><span class="sxs-lookup"><span data-stu-id="97c00-194">Important</span></span>**  
   <span data-ttu-id="97c00-195">Los nombres de equipo deben ser únicos y estar limitados a un máximo de 15 caracteres.</span><span class="sxs-lookup"><span data-stu-id="97c00-195">Computer names must be unique and are limited to a maximum of 15 characters.</span></span> <span data-ttu-id="97c00-196">Cuando decida el método de asignación de nombres de equipos, considere la posibilidad de que los usuarios finales tengan varios equipos o que compartan un equipo, y evite usar máscaras de nombre de equipo que puedan causar colisiones en la red.</span><span class="sxs-lookup"><span data-stu-id="97c00-196">When you decide on your computer naming method, consider end users who have multiple computers or that share a computer, and avoid using computer name masks that could cause a collision on the network.</span></span>



~~~
**Caution**  
The computer name settings that you specify on this page override those specified in the Sysprep.inf answer file.



After you have finished, click **Next**.
~~~

8. <span data-ttu-id="97c00-197">En la página **copiar configuración de host** , puede seleccionar la configuración siguiente para especificar cómo se configura el área de trabajo de MED-V:</span><span class="sxs-lookup"><span data-stu-id="97c00-197">On the **Copy Settings from Host** page, you can select the following settings to specify how the MED-V workspace is configured:</span></span>

   **<span data-ttu-id="97c00-198">Actúe</span><span class="sxs-lookup"><span data-stu-id="97c00-198">Caution</span></span>**  
   <span data-ttu-id="97c00-199">La configuración que especifique en esta página que se copia del equipo host al área de trabajo MED-V reemplaza a las especificadas en el archivo de respuesta Sysprep. inf.</span><span class="sxs-lookup"><span data-stu-id="97c00-199">The settings that you specify on this page that are copied from the host computer to the MED-V workspace override those specified in the Sysprep.inf answer file.</span></span>



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Copy regional settings</strong></p></td>
<td align="left"><p>Select this check box to copy the regional settings from the host computer to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[RegionalSettings]
Language
SystemLocale
UserLocale
UserLocale_DefaultUser
InputLocale
InputLocale_DefaultUser
</code></pre></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy user settings</strong></p></td>
<td align="left"><p>Select this check box to copy certain user settings, such as user name and company name, from the host to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[UserData]
OrgName
FullName</code></pre>
<div class="alert">
<strong>Note</strong>  
<p>Personal settings, such as Internet browsing history, are not copied over to the MED-V workspace.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain name</strong></p></td>
<td align="left"><p>Select this check box to let the guest join the same domain as the host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><div class="alert">
<strong>Important</strong>  
<p>The MED-V guest must be configured to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain organizational unit</strong></p></td>
<td align="left"><p>Select this check box to copy the domain organizational unit from the host computer to the MED-V workspace. This check box is only enabled if you select to copy the domain name from the host computer.</p></td>
</tr>
</tbody>
</table>



After you have finished, click **Next**.
~~~

9. <span data-ttu-id="97c00-200">En la página **Inicio y redes** , puede cambiar el comportamiento predeterminado de las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="97c00-200">On the **Startup and Networking** page, you can change the default behavior for the following settings:</span></span>

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="97c00-201">Iniciar área de trabajo MED-V</span><span class="sxs-lookup"><span data-stu-id="97c00-201">Start MED-V workspace</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="97c00-202">Elija si desea iniciar el área de trabajo de MED-V al iniciar sesión de usuario, al utilizar por primera vez, o para que el usuario final decida cuándo se inicia el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-202">Choose whether to start the MED-V workspace at user logon, at first use, or to let the end user decide when the MED-V workspace starts.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="97c00-203">El área de trabajo de MED-V se inicia de una de estas dos maneras: cuando el usuario final inicia sesión o cuando inicia por primera vez una acción que requiere MED-V, como abrir una aplicación publicada o especificar una dirección URL que requiere redireccionamiento.</span><span class="sxs-lookup"><span data-stu-id="97c00-203">The MED-V workspace starts in one of two ways: either when the end user logs on or when they first start an action that requires MED-V, such as opening a published application or entering a URL that requires redirection.</span></span></p>
   <p><span data-ttu-id="97c00-204">Puede definir esta configuración para el usuario final o permitir que el usuario final controle el inicio de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-204">You can either define this setting for the end user or let the end user control how MED-V starts.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="97c00-205">Nota</span><span class="sxs-lookup"><span data-stu-id="97c00-205">Note</span></span></strong><br/><p><span data-ttu-id="97c00-206">Si especifica que el usuario final decide, el comportamiento predeterminado que experimentan es que el área de trabajo de MED-V se inicia cuando inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="97c00-206">If you specify that the end user decides, the default behavior they experience is that the MED-V workspace starts when they log on.</span></span> <span data-ttu-id="97c00-207">Pueden cambiar el valor predeterminado haciendo clic con el botón derecho en el icono MED-V en el área de notificación y seleccionando <strong> configuración de usuario de Med-v </strong> .</span><span class="sxs-lookup"><span data-stu-id="97c00-207">They can change the default by right-clicking the MED-V icon in the notification area and selecting <strong>MED-V User Settings</strong>.</span></span> <span data-ttu-id="97c00-208">Si define esta configuración para el usuario final, no podrá cambiar el modo en que se inicia MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-208">If you define this setting for the end user, they cannot change how MED-V starts.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="97c00-209">Redes</span><span class="sxs-lookup"><span data-stu-id="97c00-209">Networking</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="97c00-210">Seleccione <strong> compartido </strong> o <strong> con puente </strong> para su configuración de red.</span><span class="sxs-lookup"><span data-stu-id="97c00-210">Select <strong>Shared</strong> or <strong>Bridged</strong> for your networking setting.</span></span> <span data-ttu-id="97c00-211">El valor predeterminado es <strong> Shared </strong> .</span><span class="sxs-lookup"><span data-stu-id="97c00-211">The default is <strong>Shared</strong>.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong><span data-ttu-id="97c00-212">Compartido </strong> - el área de trabajo de MED-V usa la traducción de direcciones de red (NAT) para compartir el host&#39;s IP para el tráfico saliente.</span><span class="sxs-lookup"><span data-stu-id="97c00-212">Shared</strong> - The MED-V workspace uses Network Address Translation (NAT) to share the host&#39;s IP for outgoing traffic.</span></span></p>
   <p><strong><span data-ttu-id="97c00-213">Con puente </strong> - el área de trabajo de MED-V tiene su propia dirección de red, que normalmente se obtiene a través de DHCP.</span><span class="sxs-lookup"><span data-stu-id="97c00-213">Bridged</strong> - The MED-V workspace has its own network address, typically obtained through DHCP.</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong><span data-ttu-id="97c00-214">Almacenar credenciales</span><span class="sxs-lookup"><span data-stu-id="97c00-214">Store credentials</span></span></strong></p></td>
   <td align="left"><p><span data-ttu-id="97c00-215">Elija si desea almacenar las credenciales de usuario final.</span><span class="sxs-lookup"><span data-stu-id="97c00-215">Choose whether you want to store the end user credentials.</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><span data-ttu-id="97c00-216">El comportamiento predeterminado es que el almacenamiento de credenciales está deshabilitado para que el usuario final se autentique cada vez que inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="97c00-216">The default behavior is that credential storing is disabled so that the end user must be authenticated every time that they log on.</span></span></p>
   <div class="alert">
   <strong><span data-ttu-id="97c00-217">Importante</span><span class="sxs-lookup"><span data-stu-id="97c00-217">Important</span></span></strong><br/><p><span data-ttu-id="97c00-218">Aunque el almacenamiento en caché de las credenciales del usuario final proporciona la mejor experiencia del usuario, debe tener en cuenta los riesgos implicados.</span><span class="sxs-lookup"><span data-stu-id="97c00-218">Even though caching the end user’s credentials provides the best user experience, you should be aware of the risks involved.</span></span></p>
   <p><span data-ttu-id="97c00-219">La credencial de dominio del usuario final se almacena en un formato reversible en el administrador de credenciales de Windows.</span><span class="sxs-lookup"><span data-stu-id="97c00-219">The end user’s domain credential is stored in a reversible format in the Windows Credential Manager.</span></span> <span data-ttu-id="97c00-220">Como resultado, un atacante podría escribir un programa que recupere la contraseña y podría obtener acceso a las credenciales del usuario.</span><span class="sxs-lookup"><span data-stu-id="97c00-220">As a result, an attacker could write a program that retrieves the password and could gain access to the user’s credentials.</span></span> <span data-ttu-id="97c00-221">Solo puede reducir este riesgo deshabilitando el almacenamiento de credenciales de usuario final.</span><span class="sxs-lookup"><span data-stu-id="97c00-221">You can only lessen this risk by disabling the storing of end-user credentials.</span></span></p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



~~~
After you have finished, click **Next**.
~~~

10. <span data-ttu-id="97c00-222">En la página de **redireccionamiento web** , puede escribir, pegar o importar una lista de las direcciones URL que se redirigen a Internet Explorer en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-222">On the **Web Redirection** page, you can enter, paste, or import a list of the URLs that are redirected to Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="97c00-223">Para obtener más información sobre cómo configurar la información de redireccionamiento de la dirección URL, consulte [requisitos previos](#bkmk-prereq).</span><span class="sxs-lookup"><span data-stu-id="97c00-223">For more information about how to configure your URL redirection information, see [Prerequisites](#bkmk-prereq).</span></span>

   <span data-ttu-id="97c00-224">También puede especificar cómo está configurado Internet Explorer en el área de trabajo de MED-V para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="97c00-224">You can also specify how Internet Explorer in the MED-V workspace is configured for end users.</span></span> <span data-ttu-id="97c00-225">De forma predeterminada, el nivel de seguridad de la zona de Internet está establecido en alto.</span><span class="sxs-lookup"><span data-stu-id="97c00-225">By default, the Internet zone security level is set to High.</span></span> <span data-ttu-id="97c00-226">Además, se eliminan ciertas capacidades de exploración predeterminadas, como la barra de direcciones.</span><span class="sxs-lookup"><span data-stu-id="97c00-226">Also, certain default browsing capabilities, such as the address bar, are removed.</span></span> <span data-ttu-id="97c00-227">Esta configuración predeterminada de Internet Explorer en el área de trabajo de MED-V proporciona un entorno de exploración más seguro para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="97c00-227">This default configuration of Internet Explorer in the MED-V workspace provides a more secure browsing environment for end users.</span></span>

   **<span data-ttu-id="97c00-228">Actúe</span><span class="sxs-lookup"><span data-stu-id="97c00-228">Caution</span></span>**  
   <span data-ttu-id="97c00-229">Al cambiar la configuración predeterminada, puede personalizar Internet Explorer en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-229">By changing the default settings, you can customize Internet Explorer in the MED-V workspace.</span></span> <span data-ttu-id="97c00-230">Sin embargo, tenga en cuenta que si cambia la configuración predeterminada para que sea menos segura, puede exponer su organización a los riesgos de seguridad presentes en las versiones anteriores de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="97c00-230">However, realize that if you change the default settings so as to make them less secure, you can expose your organization to those security risks that are present in older versions of Internet Explorer.</span></span> <span data-ttu-id="97c00-231">Para obtener más información, vea [procedimientos recomendados de seguridad para las operaciones de MED-V](security-best-practices-for-med-v-operations.md).</span><span class="sxs-lookup"><span data-stu-id="97c00-231">For more information, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).</span></span>



~~~
After you have finished, click **Next**.
~~~

11. <span data-ttu-id="97c00-232">En la página de **Resumen** , puede revisar la configuración de empaquetado de este área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="97c00-232">On the **Summary** page, you can review the packaging settings for this MED-V workspace.</span></span> <span data-ttu-id="97c00-233">Si desea cambiar la configuración, haga clic en el botón **anterior** para volver a la página correspondiente.</span><span class="sxs-lookup"><span data-stu-id="97c00-233">If you want to change any settings, click the **Previous** button to return to the relevant page.</span></span> <span data-ttu-id="97c00-234">Cuando haya terminado de revisar la configuración, haga clic en **crear**.</span><span class="sxs-lookup"><span data-stu-id="97c00-234">After you have finished reviewing the settings, click **Create**.</span></span>

   <span data-ttu-id="97c00-235">Se abrirá la página de **finalización** del **Asistente crear paquete de área de trabajo MED-V** para mostrar el progreso de la creación del paquete.</span><span class="sxs-lookup"><span data-stu-id="97c00-235">The **Completion** page of the **Create MED-V Workspace Package Wizard** opens to show the progress of the package creation.</span></span>

   **<span data-ttu-id="97c00-236">Nota</span><span class="sxs-lookup"><span data-stu-id="97c00-236">Note</span></span>**  
   <span data-ttu-id="97c00-237">El proceso de creación del paquete del área de trabajo de MED-V puede demorar varios minutos en completarse, según el tamaño del VHD especificado.</span><span class="sxs-lookup"><span data-stu-id="97c00-237">The MED-V workspace package creation process might take several minutes to complete, depending on the size of the VHD specified.</span></span>



~~~
If the MED-V workspace package is created successfully, the **Completion** page displays a list of the files that you created and their respective locations. The following is a list of the files that are created and their descriptions:

-   **setup.exe**—an installation program that you deploy and run on end-user computers to install the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.msi**—an installer file that you deploy to the end-user computers. The setup.exe file will run this file to install the MED-V workspaces.

-   **&lt;*vhd\_name*&gt;.medv**—a compressed VHD file that you deploy to the end-user computers. The setup.exe file uses it when it installs the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.reg**—the configuration settings that are installed when the setup.exe, &lt;*workspace\_name*&gt;.msi, and &lt;*vhd\_name*&gt;.medv files are deployed and setup.exe is run.

-   **&lt;*workspace\_name*&gt;.ps1**—a Windows PowerShell script that you can use to rebuild the registry file and re-build the MED-V workspace package.

    **Important**  
    Before deployment, you can edit configuration settings by updating the .ps1 file that has your preferred method of script editing, such as Windows PowerShell. After you change the .ps1 file, use that file to rebuild the MED-V workspace package that you deploy to your enterprise. For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

    However, after the MED-V workspace is deployed, you must edit configuration settings through the registry. For a list and description of the configuration settings, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).
~~~



12. <span data-ttu-id="97c00-238">Haga clic en **cerrar** para cerrar el Asistente para empaquetar y volver al **Empaquetador de área de trabajo MED-V**.</span><span class="sxs-lookup"><span data-stu-id="97c00-238">Click **Close** to close the packaging wizard and return to the **MED-V Workspace Packager**.</span></span>

<span data-ttu-id="97c00-239">El paquete de área de trabajo de MED-V ya está listo para realizar pruebas antes de la implementación.</span><span class="sxs-lookup"><span data-stu-id="97c00-239">Your MED-V workspace package is now ready for testing before deployment.</span></span>

## <span data-ttu-id="97c00-240">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="97c00-240">Related topics</span></span>


[<span data-ttu-id="97c00-241">Establecimiento de la configuración avanzada con Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="97c00-241">Configuring Advanced Settings by Using Windows PowerShell</span></span>](configuring-advanced-settings-by-using-windows-powershell.md)

[<span data-ttu-id="97c00-242">Probar el paquete de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="97c00-242">Testing the MED-V Workspace Package</span></span>](testing-the-med-v-workspace-package.md)

[<span data-ttu-id="97c00-243">Preparar una imagen de MED-V</span><span class="sxs-lookup"><span data-stu-id="97c00-243">Prepare a MED-V Image</span></span>](prepare-a-med-v-image.md)









