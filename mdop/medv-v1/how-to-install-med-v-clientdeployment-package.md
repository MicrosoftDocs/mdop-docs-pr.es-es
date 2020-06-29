---
title: Cómo instalar el cliente de MED-V
description: Cómo instalar el cliente de MED-V
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827191"
---
# <span data-ttu-id="95d62-103">Cómo instalar el cliente de MED-V</span><span class="sxs-lookup"><span data-stu-id="95d62-103">How to Install MED-V Client</span></span>


<span data-ttu-id="95d62-104">En un escenario basado en un paquete de implementación, la instalación del cliente MED-V se incluye en el paquete de implementación y se instala directamente desde el paquete.</span><span class="sxs-lookup"><span data-stu-id="95d62-104">In a deployment package-based scenario, the MED-V client installation is included in the deployment package and installed directly from the package.</span></span>

**<span data-ttu-id="95d62-105">Importante</span><span class="sxs-lookup"><span data-stu-id="95d62-105">Important</span></span>**  
<span data-ttu-id="95d62-106">Cuando use un paquete de implementación que no incluya una imagen, asegúrese de que la imagen se carga en la web o se inserta en la carpeta prestage antes de instalar el paquete de implementación.</span><span class="sxs-lookup"><span data-stu-id="95d62-106">When using a deployment package that does not include an image, ensure that the image is uploaded to the Web or pushed to the pre-stage folder prior to installing the deployment package.</span></span>



**<span data-ttu-id="95d62-107">Para instalar un paquete de implementación</span><span class="sxs-lookup"><span data-stu-id="95d62-107">To install a deployment package</span></span>**

1.  <span data-ttu-id="95d62-108">Realiza una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="95d62-108">Do one of the following:</span></span>

    -   <span data-ttu-id="95d62-109">Descargar el paquete MED-V de la Web.</span><span class="sxs-lookup"><span data-stu-id="95d62-109">Download the MED-V package from the Web.</span></span>

    -   <span data-ttu-id="95d62-110">Inserte el USB o el DVD de implementación en la unidad host.</span><span class="sxs-lookup"><span data-stu-id="95d62-110">Insert the deployment USB or DVD into the host drive.</span></span>

2.  <span data-ttu-id="95d62-111">Si MED-V no se inicia automáticamente, haga doble clic en MED-VAutoInstaller.exe.</span><span class="sxs-lookup"><span data-stu-id="95d62-111">If MED-V does not launch automatically, double-click MED-VAutoInstaller.exe.</span></span>

    <span data-ttu-id="95d62-112">Aparece un cuadro de diálogo en el que se enumeran los componentes que ya están instalados y los que se están instalando.</span><span class="sxs-lookup"><span data-stu-id="95d62-112">A dialog box appears listing the components that are already installed and those that are currently being installed.</span></span>

    **<span data-ttu-id="95d62-113">Nota</span><span class="sxs-lookup"><span data-stu-id="95d62-113">Note</span></span>**  
    <span data-ttu-id="95d62-114">Si en el equipo host hay una versión de Microsoft Virtual PC que no es compatible, aparecerá un mensaje en el que se le indicará que desinstale la versión existente y vuelva a ejecutar el instalador.</span><span class="sxs-lookup"><span data-stu-id="95d62-114">If a version of the Microsoft Virtual PC that is not supported exists on the host computer, a message will appear telling you to uninstall the existing version and run the installer again.</span></span>



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. <span data-ttu-id="95d62-115">Si es necesario, reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="95d62-115">If necessary, reboot the computer.</span></span>

   <span data-ttu-id="95d62-116">Cuando se complete la instalación, MED-V se iniciará y aparecerá un mensaje que le notificará que se ha completado la instalación.</span><span class="sxs-lookup"><span data-stu-id="95d62-116">When the installation is complete, MED-V starts and a message appears notifying you that the installation is complete.</span></span>

4. <span data-ttu-id="95d62-117">Inicie sesión en MED-V con el nombre de usuario y la contraseña siguientes:</span><span class="sxs-lookup"><span data-stu-id="95d62-117">Log in to MED-V using the following user name and password:</span></span>

   -   <span data-ttu-id="95d62-118">Escriba el nombre de dominio y el nombre de usuario seguido de la contraseña del usuario de dominio que tiene permiso para trabajar con MED-V.</span><span class="sxs-lookup"><span data-stu-id="95d62-118">Type in the domain name and user name followed by the password of the domain user who is permitted to work with MED-V.</span></span>

       <span data-ttu-id="95d62-119">Ejemplo: "domain \ _name \\user\ _name", "contraseña"</span><span class="sxs-lookup"><span data-stu-id="95d62-119">Example: "domain\_name\\user\_name", "password"</span></span>

## <span data-ttu-id="95d62-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95d62-120">Related topics</span></span>


[<span data-ttu-id="95d62-121">Cómo configurar un paquete de implementación</span><span class="sxs-lookup"><span data-stu-id="95d62-121">How to Configure a Deployment Package</span></span>](how-to-configure-a-deployment-package.md)

[<span data-ttu-id="95d62-122">Cómo cargar una imagen de MED-V en el servidor</span><span class="sxs-lookup"><span data-stu-id="95d62-122">How to Upload a MED-V Image to the Server</span></span>](how-to-upload-a-med-v-image-to-the-server.md)

[<span data-ttu-id="95d62-123">Referencia de línea de comandos de instalación de cliente</span><span class="sxs-lookup"><span data-stu-id="95d62-123">Client Installation Command Line Reference</span></span>](client-installation-command-line-reference.md)









