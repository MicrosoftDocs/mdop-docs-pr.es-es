---
title: Cómo instalar el cliente de App-V mediante el uso de Setup.exe
description: Cómo instalar el cliente de App-V mediante el uso de Setup.exe
author: dansimp
ms.assetid: 106a5d97-b5f6-4a16-bf52-a84f4d558c74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60f79a2d2f74848ab121ba13cdf8c215088d54db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817340"
---
# <span data-ttu-id="95314-103">Cómo instalar el cliente de App-V mediante el uso de Setup.exe</span><span class="sxs-lookup"><span data-stu-id="95314-103">How to Install the App-V Client by Using Setup.exe</span></span>


<span data-ttu-id="95314-104">En este tema se describe cómo instalar el cliente de App-V con el programa setup.exe.</span><span class="sxs-lookup"><span data-stu-id="95314-104">This topic describes how to install the App-V client by using the setup.exe program.</span></span> <span data-ttu-id="95314-105">Al instalar el cliente de App-V con el programa setup.exe, el instalador determina qué software necesario necesita y lo instala automáticamente antes de instalar el cliente.</span><span class="sxs-lookup"><span data-stu-id="95314-105">When you install the App-V client using the setup.exe program, the installer determines which prerequisite software is needed and installs it automatically before it installs the client.</span></span>

**<span data-ttu-id="95314-106">Para instalar el cliente de virtualización de aplicaciones con Setup.exe</span><span class="sxs-lookup"><span data-stu-id="95314-106">To install the Application Virtualization Client by Using Setup.exe</span></span>**

1.  <span data-ttu-id="95314-107">Asegúrese de que ha iniciado sesión con una cuenta que tiene derechos de administrador en el equipo.</span><span class="sxs-lookup"><span data-stu-id="95314-107">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="95314-108">Abra una ventana del símbolo del sistema y, a continuación, cambie el directorio a la carpeta que contiene los archivos de instalación.</span><span class="sxs-lookup"><span data-stu-id="95314-108">Open a Command Prompt window, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="95314-109">Al instalar la versión 4.6 o una versión posterior del cliente de App-V, debe usar el instalador correcto para el sistema operativo del equipo, 32 bits o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="95314-109">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="95314-110">La instalación no se realizará y aparecerá un mensaje de error si usa el instalador equivocado.</span><span class="sxs-lookup"><span data-stu-id="95314-110">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="95314-111">Escriba la cadena de comando de instalación en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="95314-111">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="95314-112">Como alternativa, puede crear un archivo de comandos y ejecutarlo desde el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="95314-112">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="95314-113">También puede usar un lenguaje de scripts, como VBScript o Windows PowerShell, para ejecutar el comando.</span><span class="sxs-lookup"><span data-stu-id="95314-113">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="95314-114">En el siguiente ejemplo de línea de comandos se muestra cómo se puede usar setup.exe con un número de parámetros opcionales.</span><span class="sxs-lookup"><span data-stu-id="95314-114">The following command-line example shows how setup.exe can be used with a number of optional parameters.</span></span> <span data-ttu-id="95314-115">Para obtener más información sobre estos parámetros, consulte [parámetros de la línea de comandos del instalador del cliente de virtualización de aplicaciones](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="95314-115">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="95314-116">"setup.exe"/s/v "/QN SWICACHESIZE = \ \" 10240 \ \ "SWIPUBSVRDISPLAY = \ \" Production System\\ "SWIPUBSVRTYPE = \ \" HTTP/secure\\ "SWIPUBSVRHOST = \ \" PRODSYS\\ "SWIPUBSVRPORT = \ \" 443 \ \ "SWIPUBSVRPATH = \ \"/AppVirt/appsntype.xml \ \ "SWIPUBSVRREFRESH = \ \" on\\ "SWIGLOBALDATA = \ \" D:\\AppVirt\\Global\\ "SWIUSERDATA = \ \" ^% LOCALAPPDATA ^%\\Windows\\Application virtualización Client\\ "SWIFSDRIVE = \ \" Q\\ ""</span><span class="sxs-lookup"><span data-stu-id="95314-116">"setup.exe" /s /v"/qn SWICACHESIZE=\\"10240\\" SWIPUBSVRDISPLAY=\\"Production System\\" SWIPUBSVRTYPE=\\"HTTP /secure\\" SWIPUBSVRHOST=\\"PRODSYS\\" SWIPUBSVRPORT=\\"443\\" SWIPUBSVRPATH=\\"/AppVirt/appsntype.xml\\" SWIPUBSVRREFRESH=\\"on\\" SWIGLOBALDATA=\\"D:\\AppVirt\\Global\\" SWIUSERDATA=\\"^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\" SWIFSDRIVE=\\"Q\\""</span></span>**

    **<span data-ttu-id="95314-117">Importante</span><span class="sxs-lookup"><span data-stu-id="95314-117">Important</span></span>**  
    -   <span data-ttu-id="95314-118">Las comillas que aparecen en la sección "**/v**" se deben tratar como caracteres especiales e introducirse con un " **\\** " anterior.</span><span class="sxs-lookup"><span data-stu-id="95314-118">The quotation marks that appear in the "**/v**" section must be treated as special characters and entered with a preceding "**\\**".</span></span> <span data-ttu-id="95314-119">Las comillas solo son necesarias cuando el valor contiene un espacio. sin embargo, por coherencia, todas las instancias del ejemplo anterior se muestran con comillas.</span><span class="sxs-lookup"><span data-stu-id="95314-119">The quotation marks are required only when the value contains a space; however, for consistency, all the instances in the preceding example are shown as having quotation marks.</span></span>

    -   <span data-ttu-id="95314-120">Los caracteres "" **%** en "**% HomeDrive%**" deben ir precedidos del **^** carácter de escape "".</span><span class="sxs-lookup"><span data-stu-id="95314-120">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="95314-121">En caso contrario, el shell de comandos de Windows establece el valor en el del usuario que realiza la instalación.</span><span class="sxs-lookup"><span data-stu-id="95314-121">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="95314-122">Los modificadores de **InstallShield** **/s** y **/QN** son necesarios para que esto sea una instalación silenciosa.</span><span class="sxs-lookup"><span data-stu-id="95314-122">The **InstallShield** switches **/s** and **/qn** are needed to make this a silent install.</span></span> <span data-ttu-id="95314-123">El modificador **/QN** debe ir a continuación del modificador **/v** , separado por un carácter de comillas sin espacios intermedios.</span><span class="sxs-lookup"><span data-stu-id="95314-123">The **/qn** switch must follow the **/v** switch, separated by only a quote character with no intervening spaces.</span></span>

    -   <span data-ttu-id="95314-124">La carpeta especificada en el valor **SWIGLOBALDATA** debe existir previamente.</span><span class="sxs-lookup"><span data-stu-id="95314-124">The folder specified in the **SWIGLOBALDATA** value must already exist.</span></span>

     

5.  <span data-ttu-id="95314-125">Una vez completada la instalación, le recomendamos que ejecute una búsqueda de Microsoft Update para asegurarse de que están instaladas las actualizaciones más recientes.</span><span class="sxs-lookup"><span data-stu-id="95314-125">When the installation is complete, we recommend that you run a Microsoft Update scan to ensure the latest updates are installed.</span></span>

## <span data-ttu-id="95314-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95314-126">Related topics</span></span>


[<span data-ttu-id="95314-127">Cómo instalar el cliente mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="95314-127">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





