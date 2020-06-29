---
title: Cómo instalar el servicio web de administración
description: Cómo instalar el servicio web de administración
author: dansimp
ms.assetid: cac296f5-8ca0-4ce7-afdb-859ae207d2f1
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4b8cc1b4821cb4041d75003cf7e6ff592e1c5039
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817280"
---
# <span data-ttu-id="3e98e-103">Cómo instalar el servicio web de administración</span><span class="sxs-lookup"><span data-stu-id="3e98e-103">How to Install the Management Web Service</span></span>


<span data-ttu-id="3e98e-104">Use el siguiente procedimiento para instalar el servicio Web de administración de virtualización de aplicaciones en un equipo de destino de la red, con una cuenta de inicio de sesión que tenga privilegios de administrador local.</span><span class="sxs-lookup"><span data-stu-id="3e98e-104">Use the following procedure to install the Application Virtualization Management Web Service on a target computer on the network, with a logon account having local administrative privileges.</span></span> <span data-ttu-id="3e98e-105">Aunque no es necesario, le recomendamos que instale este componente en su servidor Web.</span><span class="sxs-lookup"><span data-stu-id="3e98e-105">Although it is not required, we recommended that you install this component on your Web server.</span></span>

**<span data-ttu-id="3e98e-106">Para instalar el servicio Web de administración</span><span class="sxs-lookup"><span data-stu-id="3e98e-106">To install the Management Web Service</span></span>**

1.  <span data-ttu-id="3e98e-107">Compruebe que ninguna de las versiones anteriores del servicio Web de virtualización de aplicaciones están instaladas en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="3e98e-107">Verify that no previous versions of the Application Virtualization Web Service are installed on your target computer.</span></span>

2.  <span data-ttu-id="3e98e-108">Vaya a la ubicación del programa de instalación del sistema de Application Virtualization en la red, ejecute este programa desde la red o copie su directorio en el equipo de destino y, a continuación, haga doble clic en **Setup.exe**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-108">Navigate to the location of the Application Virtualization System setup program on the network, either run this program from the network or copy its directory to the target computer, and then double-click **Setup.exe**.</span></span>

3.  <span data-ttu-id="3e98e-109">Una vez que se abra el Asistente de instalación, en la página **principal** , haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-109">After the Installation Wizard opens, on the **Welcome** page, click **Next**.</span></span>

4.  <span data-ttu-id="3e98e-110">En la página **contrato de licencia** , para aceptar el contrato de licencia, seleccione Acepto **los términos y condiciones de licencia**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-110">On the **License Agreement** page, to accept the license agreement, select **I accept the license terms and conditions**, and then click **Next**.</span></span>

5.  <span data-ttu-id="3e98e-111">En la página **información de registro** , especifique el nombre de **usuario** y la información de la organización y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-111">On the **Registration Information** page, specify the **User Name** and organization information, and then click **Next**.</span></span>

6.  <span data-ttu-id="3e98e-112">En la página **tipo de configuración** , haga clic en **personalizado**y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-112">On the **Setup Type** page, click **Custom**, and then click **Next**.</span></span>

    <span data-ttu-id="3e98e-113">**Nota:**  Si este no es el primer componente que instaló en este equipo, se muestra la página **mantenimiento del programa** .</span><span class="sxs-lookup"><span data-stu-id="3e98e-113">**Note** If this is not the first component you installed on this computer, the **Program Maintenance** page is displayed.</span></span> <span data-ttu-id="3e98e-114">En la página **mantenimiento del programa** , haga clic en **modificar**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-114">On the **Program Maintenance** page, click **Modify**.</span></span>

     

7.  <span data-ttu-id="3e98e-115">En la página **instalación personalizada** , desactive todos los componentes del sistema de Application Virtualization, excepto el **servicio de administración de virt**de aplicaciones y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-115">On the **Custom Setup** page, clear all Application Virtualization System components except **App Virt Management Service**, and then click **Next**.</span></span>

    <span data-ttu-id="3e98e-116">**Nota:**  Si un componente ya está instalado en el equipo, al borrarlo en la página de **instalación personalizada** , se desinstalará automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3e98e-116">**Note** If a component is already installed on the computer, by clearing it on the **Custom Setup** page, you will automatically uninstall it.</span></span>

     

8.  <span data-ttu-id="3e98e-117">En la página **servidor de base de datos** , haga clic en **conectarse a la base de datos disponible**y, a continuación, en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-117">On the **Database Server** page, click **Connect to available database**, and then click **Next**.</span></span>

    <span data-ttu-id="3e98e-118">**Nota:**  En un entorno de producción, Microsoft da por supuesto que se conectará a una base de datos existente.</span><span class="sxs-lookup"><span data-stu-id="3e98e-118">**Note** In a production environment, Microsoft assumes that you will connect to an existing database.</span></span> <span data-ttu-id="3e98e-119">Si desea instalar una base de datos, vea [Cómo instalar una base de datos](how-to-install-a-database.md).</span><span class="sxs-lookup"><span data-stu-id="3e98e-119">If you want to install a database, see [How to Install a Database](how-to-install-a-database.md).</span></span> <span data-ttu-id="3e98e-120">Después de instalar la base de datos, continúe con el paso 13.</span><span class="sxs-lookup"><span data-stu-id="3e98e-120">After installing the database, continue with step 13.</span></span>

     

9.  <span data-ttu-id="3e98e-121">En la página **tipo de servidor de base de datos** , seleccione un tipo de base de datos de la lista y haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-121">On the **Database Server Type** page, select a database type from the list, and then click **Next**.</span></span>

10. <span data-ttu-id="3e98e-122">En la página **Ubicación del servidor de base** de datos, seleccione un servidor de base de datos de la lista de servidores disponibles o agregue un servidor activando la casilla de verificación **usar el siguiente nombre de host** y escribiendo información en los cuadros nombre del **servidor** y **número de Puerto** y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-122">On the **Database Server Location** page, select a database server from the list of available servers or add a server by selecting the **Use the following host name** check box and entering information in the **Server Name** and **Port Number** boxes, and then click **Next**.</span></span>

11. <span data-ttu-id="3e98e-123">En la página **Seleccionar base de datos** , seleccione la base de datos que desee y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-123">On the **Select Database** page, select the database you want, and then click **Next**.</span></span>

12. <span data-ttu-id="3e98e-124">En la página **configuración de usuario de base** de datos, escriba las credenciales que usará el servicio Web de administración para obtener acceso al almacén de datos y, a continuación, haga clic en **siguiente**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-124">On the **Database User Configuration** page, enter the credentials that the Management Web Service will use to access the data store, and then click **Next**.</span></span>

13. <span data-ttu-id="3e98e-125">En la página **listo para modificar el programa** , haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-125">On the **Ready to Modify the Program** page, click **Install**.</span></span>

    <span data-ttu-id="3e98e-126">**Nota:**  Si este es el primer componente que instala, se muestra la página **preparado para instalar el programa** .</span><span class="sxs-lookup"><span data-stu-id="3e98e-126">**Note** If this is the first component you install, the **Ready to Install the Program** page is displayed.</span></span> <span data-ttu-id="3e98e-127">En la página, haga clic en **instalar**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-127">On the page, click **Install**.</span></span>

     

14. <span data-ttu-id="3e98e-128">En la página **Asistente para la instalación completada** , haga clic en **Finalizar**.</span><span class="sxs-lookup"><span data-stu-id="3e98e-128">On the **Installation Wizard Completed** page, click **Finish**.</span></span>

## <span data-ttu-id="3e98e-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3e98e-129">Related topics</span></span>


[<span data-ttu-id="3e98e-130">Cómo instalar los servidores y componentes del sistema</span><span class="sxs-lookup"><span data-stu-id="3e98e-130">How to Install the Servers and System Components</span></span>](how-to-install-the-servers-and-system-components.md)

 

 





