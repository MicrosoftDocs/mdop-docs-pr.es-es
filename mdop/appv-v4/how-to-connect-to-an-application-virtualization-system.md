---
title: Cómo conectarse a un sistema de virtualización de aplicaciones
description: Cómo conectarse a un sistema de virtualización de aplicaciones
author: dansimp
ms.assetid: ac38216c-5464-4c0b-a4d3-3949ba6358ac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 30d60e187e1b7595fd0dce6641fa027a1df68f3d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817711"
---
# <span data-ttu-id="33181-103">Cómo conectarse a un sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="33181-103">How to Connect to an Application Virtualization System</span></span>


<span data-ttu-id="33181-104">Debe conectar la consola de administración de Application Virtualization Server a un sistema de virtualización de aplicaciones antes de poder usar la consola de administración para administrar aplicaciones, asociaciones de tipos de archivo, paquetes, licencias de aplicaciones, grupos de servidores, directivas y administradores de proveedores.</span><span class="sxs-lookup"><span data-stu-id="33181-104">You must connect the Application Virtualization Server Management Console to an Application Virtualization System before you can use the management console to manage applications, file type associations, packages, application licenses, server groups, provider policies and administrators.</span></span> <span data-ttu-id="33181-105">El procedimiento siguiente describe los pasos que debe seguir para conectar la consola a un sistema de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="33181-105">The following procedure outlines the steps you must follow to connect the console to an Application Virtualization System.</span></span>

**<span data-ttu-id="33181-106">Para conectarse a un sistema de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="33181-106">To connect to an Application Virtualization System</span></span>**

1. <span data-ttu-id="33181-107">Haga clic con el botón derecho en el nodo del sistema de virtualización de aplicaciones en el panel de **ámbito** y seleccione **conectar con el sistema de virtualización de aplicaciones** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="33181-107">Right-click the Application Virtualization System node in the **Scope** pane, and select **Connect to Application Virtualization System** from the pop-up menu.</span></span>

   **<span data-ttu-id="33181-108">Nota</span><span class="sxs-lookup"><span data-stu-id="33181-108">Note</span></span>**  
   <span data-ttu-id="33181-109">Hay tres componentes para la administración de servidores de virtualización de aplicaciones: la consola de administración de virtualización de aplicaciones, el servicio Web de administración y el almacén de SQL.</span><span class="sxs-lookup"><span data-stu-id="33181-109">There are three components to Application Virtualization server management: the Application Virtualization Management Console, the Management Web Service, and the SQL Datastore.</span></span> <span data-ttu-id="33181-110">Si estos componentes se distribuyen en diferentes equipos físicos, debe configurar la seguridad correctamente para que los componentes se comuniquen a través del sistema.</span><span class="sxs-lookup"><span data-stu-id="33181-110">If these components are distributed across different physical machines, you must configure security properly for the components to communicate across the system.</span></span> <span data-ttu-id="33181-111">Para obtener más información, consulte los siguientes manuales y artículos:</span><span class="sxs-lookup"><span data-stu-id="33181-111">For more information, see the following manuals and articles:</span></span>

   <span data-ttu-id="33181-112">[Cómo configurar el servidor para que sea de confianza para la delegación](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)</span><span class="sxs-lookup"><span data-stu-id="33181-112">[How to Configure the Server to be Trusted for Delegation](https://go.microsoft.com/fwlink/?LinkID=166682) (https://go.microsoft.com/fwlink/?LinkID=166682)</span></span>

   <span data-ttu-id="33181-113">[Guía de planeación e implementación del sistema de virtualización de aplicaciones](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)</span><span class="sxs-lookup"><span data-stu-id="33181-113">[Planning and Deployment Guide for the Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=122063) (https://go.microsoft.com/fwlink/?LinkID=122063)</span></span>

   <span data-ttu-id="33181-114">[Guía de operaciones del sistema de virtualización de aplicaciones](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)</span><span class="sxs-lookup"><span data-stu-id="33181-114">[Operations Guide for the Application Virtualization System](https://go.microsoft.com/fwlink/?LinkID=133129) (https://go.microsoft.com/fwlink/?LinkID=133129)</span></span>

   <span data-ttu-id="33181-115">[Artículo 930472](https://go.microsoft.com/fwlink/?LinkId=114647) de Microsoft Knowledge base (https://go.microsoft.com/fwlink/?LinkId=114647)</span><span class="sxs-lookup"><span data-stu-id="33181-115">[Article 930472](https://go.microsoft.com/fwlink/?LinkId=114647) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114647)</span></span>

   <span data-ttu-id="33181-116">[Artículo 930565](https://go.microsoft.com/fwlink/?LinkId=114648) de Microsoft Knowledge base (https://go.microsoft.com/fwlink/?LinkId=114648)</span><span class="sxs-lookup"><span data-stu-id="33181-116">[Article 930565](https://go.microsoft.com/fwlink/?LinkId=114648) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=114648)</span></span>

     

2. <span data-ttu-id="33181-117">Complete los campos en el cuadro de diálogo **conectar con el sistema de virtualización de aplicaciones** :</span><span class="sxs-lookup"><span data-stu-id="33181-117">Complete the fields in the **Connect to Application Virtualization System** dialog box:</span></span>

   1. <span data-ttu-id="33181-118">**Nombre de host del servicio Web**: escriba el nombre del sistema de virtualización de aplicaciones al que desea conectarse o escriba **localhost** para conectarse al servidor local.</span><span class="sxs-lookup"><span data-stu-id="33181-118">**Web Service Host Name**—Enter the name of the Application Virtualization System to which you want to connect, or enter **localhost** to connect to the local server.</span></span>

   2. <span data-ttu-id="33181-119">**Usar conexión segura**: Seleccione esta casilla si desea conectarse al servidor con una conexión segura.</span><span class="sxs-lookup"><span data-stu-id="33181-119">**Use Secure Connection**—Select this check box if you want to connect to the server with a secure connection.</span></span>

   3. <span data-ttu-id="33181-120">**Puerto**: Introduzca el número de puerto que desea usar para la conexión.</span><span class="sxs-lookup"><span data-stu-id="33181-120">**Port**—Enter the port number you want to use for the connection.</span></span> <span data-ttu-id="33181-121">**80** es el número de Puerto normal predeterminado y **443** es el número de puerto seguro.</span><span class="sxs-lookup"><span data-stu-id="33181-121">**80** is the default regular port number, and **443** is the secure-port number.</span></span>

   4. <span data-ttu-id="33181-122">**Usar cuenta de Windows actual**: Seleccione este botón de radio para usar las credenciales de cuenta de Windows actuales.</span><span class="sxs-lookup"><span data-stu-id="33181-122">**Use Current Windows Account**—Select this radio button to use the current Windows account credentials.</span></span>

   5. <span data-ttu-id="33181-123">**Especificar cuenta de Windows**: Seleccione este botón de radio cuando desee conectar con el servidor como otro usuario.</span><span class="sxs-lookup"><span data-stu-id="33181-123">**Specify Windows Account**—Select this radio button when you want to connect to the server as a different user.</span></span>

   6. <span data-ttu-id="33181-124">**Nombre**: escriba el nombre del nuevo usuario con el formato *DOMAIN\\username* o el <em> username@domain </em> .</span><span class="sxs-lookup"><span data-stu-id="33181-124">**Name**—Enter the name of the new user by using either the *DOMAIN\\username* or the <em>username@domain</em> format.</span></span>

   7. <span data-ttu-id="33181-125">**Contraseña**: escriba la contraseña que corresponde al nuevo usuario.</span><span class="sxs-lookup"><span data-stu-id="33181-125">**Password**—Enter the password that corresponds to the new user.</span></span>

3. <span data-ttu-id="33181-126">Haz clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="33181-126">Click **OK**.</span></span>

## <span data-ttu-id="33181-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33181-127">Related topics</span></span>


[<span data-ttu-id="33181-128">Cómo realizar tareas administrativas en la consola de administración de servidor de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="33181-128">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)

 

 





