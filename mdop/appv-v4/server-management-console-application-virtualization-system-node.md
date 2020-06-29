---
title: Aplicación de consola de administración de servidores nodo del sistema de virtualización
description: Aplicación de consola de administración de servidores nodo del sistema de virtualización
author: dansimp
ms.assetid: 9450832e-335c-41e7-af24-fddb8ffc327c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 51256ee7e96a97016e73dc79c87e4d422198cfb3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815441"
---
# <span data-ttu-id="cad96-103">Consola de administración de servidor: Nodo de sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="cad96-103">Server Management Console: Application Virtualization System Node</span></span>


<span data-ttu-id="cad96-104">El nodo del sistema de virtualización de aplicaciones es el nodo de nivel superior en el panel de **ámbito** .</span><span class="sxs-lookup"><span data-stu-id="cad96-104">The Application Virtualization System node is the top-level node in the **Scope** pane.</span></span> <span data-ttu-id="cad96-105">Este nodo muestra el nombre del servidor que la consola está controlando actualmente, o bien muestra el nombre del equipo local (si está conectado por el nombre) o "local" cuando la consola está conectada al equipo local.</span><span class="sxs-lookup"><span data-stu-id="cad96-105">This node displays the name of the server the console is currently controlling, or it displays the name of the local computer (if you are connected by the name) or "local" when the console is connected to the local computer.</span></span> <span data-ttu-id="cad96-106">Desde el nodo del sistema de virtualización de aplicaciones, puede conectarse a otro equipo o conectarse al equipo actual con un conjunto diferente de credenciales.</span><span class="sxs-lookup"><span data-stu-id="cad96-106">From the Application Virtualization System node, you can connect to another computer or you can connect to the current computer with a different set of credentials.</span></span>

<span data-ttu-id="cad96-107">Puede hacer clic con el botón secundario en el nodo del sistema de virtualización de aplicaciones para mostrar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="cad96-107">You can right-click the Application Virtualization System node to display the following elements.</span></span>

<a href="" id="configure-connection"></a>**<span data-ttu-id="cad96-108">Configurar conexión</span><span class="sxs-lookup"><span data-stu-id="cad96-108">Configure Connection</span></span>**  
<span data-ttu-id="cad96-109">En este cuadro de diálogo, puede modificar las siguientes opciones de configuración:</span><span class="sxs-lookup"><span data-stu-id="cad96-109">In this dialog box, you can modify the following settings:</span></span>

- <span data-ttu-id="cad96-110">**Nombre de host del servicio Web**: le permite escribir el nombre del sistema de virtualización de aplicaciones al que desea conectarse, o bien puede escribir **localhost** para conectarse al equipo local.</span><span class="sxs-lookup"><span data-stu-id="cad96-110">**Web Service Host Name**—Enables you to enter the name of the Application Virtualization System to which you want to connect, or you can enter **localhost** to connect to the local computer.</span></span>

- <span data-ttu-id="cad96-111">**Usar conexión segura**: Seleccione si desea conectarse al servidor con una conexión segura.</span><span class="sxs-lookup"><span data-stu-id="cad96-111">**Use Secure Connection**—Select if you want to connect to the server with a secure connection.</span></span>

- <span data-ttu-id="cad96-112">**Puerto**: le permite introducir el número de puerto que desea usar para la conexión.</span><span class="sxs-lookup"><span data-stu-id="cad96-112">**Port**—Enables you to enter the port number you want to use for the connection.</span></span> <span data-ttu-id="cad96-113">80 es el número de Puerto normal predeterminado y 443 es el número de puerto seguro predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cad96-113">80 is the default regular port number, and 443 is default secure port number.</span></span>

- <span data-ttu-id="cad96-114">**Usar cuenta de Windows actual**: Seleccione esta forma para usar las credenciales de la cuenta de Windows actuales.</span><span class="sxs-lookup"><span data-stu-id="cad96-114">**Use Current Windows Account**—Select to use the current Windows account credentials.</span></span>

- <span data-ttu-id="cad96-115">**Especificar cuenta de Windows**: seleccione Cuándo desea conectarse al servidor como un usuario diferente.</span><span class="sxs-lookup"><span data-stu-id="cad96-115">**Specify Windows Account**—Select when you want to connect to the server as a different user.</span></span>

- <span data-ttu-id="cad96-116">**Nombre**: permite especificar el nombre del nuevo usuario mediante el formato *DOMAIN\\username* o el <em> username@domain </em> .</span><span class="sxs-lookup"><span data-stu-id="cad96-116">**Name**—Enables you to enter the name of the new user by using either the *DOMAIN\\username* or the <em>username@domain</em> format.</span></span>

- <span data-ttu-id="cad96-117">**Contraseña**: le permite escribir la contraseña que corresponde al nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="cad96-117">**Password**—Enables you to enter the password that corresponds to the new user.</span></span>

<a href="" id="system-options"></a>**<span data-ttu-id="cad96-118">Opciones del sistema</span><span class="sxs-lookup"><span data-stu-id="cad96-118">System Options</span></span>**  
<span data-ttu-id="cad96-119">En las siguientes pestañas de este cuadro de diálogo, puede modificar la configuración asociada:</span><span class="sxs-lookup"><span data-stu-id="cad96-119">On the following tabs on this dialog box, you can modify the associated settings:</span></span>

-   <span data-ttu-id="cad96-120">**Ficha General**: permite especificar la ruta de **contenido predeterminada** donde se almacenan los archivos OSD y de icono.</span><span class="sxs-lookup"><span data-stu-id="cad96-120">**General Tab**—Enables you to specify the **Default Content Path** where the OSD and icon files are stored.</span></span>

-   <span data-ttu-id="cad96-121">**Ficha base de datos**: permite especificar el tamaño máximo de la **base de datos** y el **historial de uso**.</span><span class="sxs-lookup"><span data-stu-id="cad96-121">**Database Tab**—Enables you to specify the maximum **Database Size** and the **Usage History**.</span></span>

<a href="" id="view"></a>**<span data-ttu-id="cad96-122">Ver</span><span class="sxs-lookup"><span data-stu-id="cad96-122">View</span></span>**  
<span data-ttu-id="cad96-123">Cambia la apariencia de la consola de administración de Application Virtualization Server.</span><span class="sxs-lookup"><span data-stu-id="cad96-123">Changes the appearance of the Application Virtualization Server Management Console.</span></span> <span data-ttu-id="cad96-124">Para obtener más información sobre cómo cambiar la apariencia de la consola, consulte los archivos de ayuda de Microsoft Management Console.</span><span class="sxs-lookup"><span data-stu-id="cad96-124">For more information about changing the appearance of the console, refer to the help files for the Microsoft Management Console.</span></span>

<a href="" id="new-window-from-here"></a>**<span data-ttu-id="cad96-125">Nueva ventana desde aquí</span><span class="sxs-lookup"><span data-stu-id="cad96-125">New Window from Here</span></span>**  
<span data-ttu-id="cad96-126">Abre una nueva ventana de administración de consola.</span><span class="sxs-lookup"><span data-stu-id="cad96-126">Opens a new management console window.</span></span>

<a href="" id="export-list"></a>**<span data-ttu-id="cad96-127">Exportar lista</span><span class="sxs-lookup"><span data-stu-id="cad96-127">Export List</span></span>**  
<span data-ttu-id="cad96-128">Crea un archivo de texto delimitado por tabulaciones que incluye el contenido del panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="cad96-128">Creates a tab-delimited text file that contains the contents of the **Results** pane.</span></span> <span data-ttu-id="cad96-129">Este elemento muestra un cuadro de diálogo estándar para **guardar un archivo** en el que se especifica la ubicación del archivo de texto que se está creando.</span><span class="sxs-lookup"><span data-stu-id="cad96-129">This item displays a standard **File Save** dialog box where you specify the location for the text file you are creating.</span></span>

<a href="" id="help"></a>**<span data-ttu-id="cad96-130">Ayuda</span><span class="sxs-lookup"><span data-stu-id="cad96-130">Help</span></span>**  
<span data-ttu-id="cad96-131">Inicia el archivo de ayuda de la consola de administración.</span><span class="sxs-lookup"><span data-stu-id="cad96-131">Starts the management console help file.</span></span>

## <span data-ttu-id="cad96-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cad96-132">Related topics</span></span>


[<span data-ttu-id="cad96-133">Referencia de la consola de administración de servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="cad96-133">Application Virtualization Server Management Console Reference</span></span>](application-virtualization-server-management-console-reference.md)

 

 





