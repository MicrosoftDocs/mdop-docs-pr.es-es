---
title: Cómo mover los informes de MBAM 2.5
description: Cómo mover los informes de MBAM 2.5
author: dansimp
ms.assetid: c8223656-ca9d-41c8-94a3-64d07a6b99e9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdef260b4381671a1b9de66565ece0b70876200
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812391"
---
# <span data-ttu-id="70256-103">Cómo mover los informes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="70256-103">How to Move the MBAM 2.5 Reports</span></span>


<span data-ttu-id="70256-104">Use estos procedimientos para mover la característica informes de un equipo a otro, es decir, para mover la característica de informes del servidor a al servidor B.</span><span class="sxs-lookup"><span data-stu-id="70256-104">Use these procedures to move the Reports feature from one computer to another, that is, to move the Reports feature from Server A to Server B.</span></span>

<span data-ttu-id="70256-105">A continuación, se resumen los pasos para mover la característica informes:</span><span class="sxs-lookup"><span data-stu-id="70256-105">The high-level steps for moving the Reports feature are:</span></span>

1.  <span data-ttu-id="70256-106">Detenga todas las instancias del sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="70256-106">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="70256-107">Instale el software de servidor MBAM 2,5 en el servidor B y configure la característica de informes en el servidor B.</span><span class="sxs-lookup"><span data-stu-id="70256-107">Install the MBAM 2.5 Server software on Server B and configure the Reports feature on Server B.</span></span>

3.  <span data-ttu-id="70256-108">Actualice los datos de conexión de los informes en los servidores de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="70256-108">Update the reports connection data on the MBAM Administration and Monitoring servers.</span></span>

4.  <span data-ttu-id="70256-109">Reanude la instancia del sitio web de supervisión y administración de MBAM.</span><span class="sxs-lookup"><span data-stu-id="70256-109">Resume the instance of the MBAM Administration and Monitoring Website.</span></span>

<span data-ttu-id="70256-110">**Nota:**  Para ejecutar los scripts de ejemplo de Windows PowerShell en este tema, debe actualizar la Directiva de ejecución de Windows PowerShell para habilitar la ejecución de scripts.</span><span class="sxs-lookup"><span data-stu-id="70256-110">**Note** To run the example Windows PowerShell scripts in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="70256-111">Consulte [ejecución de scripts de Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) para obtener instrucciones.</span><span class="sxs-lookup"><span data-stu-id="70256-111">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

 

**<span data-ttu-id="70256-112">Detener el sitio web de administración y supervisión de MBAM</span><span class="sxs-lookup"><span data-stu-id="70256-112">Stop the MBAM Administration and Monitoring Website</span></span>**

-   <span data-ttu-id="70256-113">En el servidor que ejecuta el sitio web de administración y supervisión, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="70256-113">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="70256-114">Para automatizar este procedimiento, puede usar Windows PowerShell para escribir un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="70256-114">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**<span data-ttu-id="70256-115">Instalar el software de servidor MBAM y ejecutar el Asistente para la configuración del servidor de MBAM en el servidor B</span><span class="sxs-lookup"><span data-stu-id="70256-115">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>**

1.  <span data-ttu-id="70256-116">Instale el software del servidor de MBAM en el servidor B. Para obtener instrucciones, consulte [Installing the MBAM 2,5 Server Software](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="70256-116">Install the MBAM Server software on Server B. For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="70256-117">En el servidor B, inicie el Asistente para la configuración del servidor de MBAM, haga clic en **Agregar nuevas características**y, a continuación, seleccione solo la característica **informes** .</span><span class="sxs-lookup"><span data-stu-id="70256-117">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Reports** feature.</span></span>

    <span data-ttu-id="70256-118">Como alternativa, puede usar el cmdlet **enable-MbamReport** de Windows PowerShell para configurar los informes.</span><span class="sxs-lookup"><span data-stu-id="70256-118">Alternatively, you can use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span>

    <span data-ttu-id="70256-119">Para obtener instrucciones sobre cómo configurar los informes, consulte [Cómo configurar los informes de MBAM 2,5](how-to-configure-the-mbam-25-reports.md).</span><span class="sxs-lookup"><span data-stu-id="70256-119">For instructions on how to configure the Reports, see [How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md).</span></span>

**<span data-ttu-id="70256-120">Actualizar los datos de conexión de los informes en el servidor de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="70256-120">Update the reports connection data on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="70256-121">En el servidor que ejecuta la característica informes, use la consola del administrador de Internet Information Services (IIS) para actualizar la dirección URL de los informes.</span><span class="sxs-lookup"><span data-stu-id="70256-121">On the server that is running the Reports feature, use the Internet Information Services (IIS) Manager console to update the Reports URL.</span></span>

2.  <span data-ttu-id="70256-122">Expanda **Administración y supervisión de Microsoft BitLocker**y, a continuación, seleccione el nodo del **Departamento de soporte técnico** .</span><span class="sxs-lookup"><span data-stu-id="70256-122">Expand **Microsoft BitLocker Administration and Monitoring**, and then select the **HelpDesk** node.</span></span>

3.  <span data-ttu-id="70256-123">En la sección **Administración** de la **vista características**, seleccione **Editor de configuración**.</span><span class="sxs-lookup"><span data-stu-id="70256-123">In the **Management** section of the **Features View**, select **Configuration Editor**.</span></span>

4.  <span data-ttu-id="70256-124">En el campo **section** , seleccione **appSettings**.</span><span class="sxs-lookup"><span data-stu-id="70256-124">In the **Section** field, select **appSettings**.</span></span>

5.  <span data-ttu-id="70256-125">Seleccione la fila de la **colección** y, a continuación, haga clic en el botón "puntos suspensivos" **(...)** en el extremo derecho del panel para abrir el editor de la **colección**.</span><span class="sxs-lookup"><span data-stu-id="70256-125">Select the **Collection** row, and then click the "ellipses" button **(…)** at the far right of the pane to open the **Collection Editor**.</span></span>

6.  <span data-ttu-id="70256-126">En el **Editor de colecciones**, seleccione la fila que contiene **Microsoft. Mbam. Reports. URL**y actualice el valor de **Microsoft. Mbam. Reports. URL** para reflejar el nombre del servidor para el servidor B.</span><span class="sxs-lookup"><span data-stu-id="70256-126">In the **Collection Editor**, select the row that contains **Microsoft.Mbam.Reports.Url**, and update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B.</span></span>

    <span data-ttu-id="70256-127">Si ha configurado previamente la característica informes en una instancia con nombre de SQL Server Reporting Services, agregue o actualice el nombre de la instancia a la dirección URL, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="70256-127">If you previously configured the Reports feature on a named instance of SQL Server Reporting Services, add or update the name of the instance to the URL, for example:</span></span>

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  <span data-ttu-id="70256-128">Para automatizar este procedimiento, puede usar Windows PowerShell para ejecutar un comando en el servidor de administración y supervisión que es similar al siguiente ejemplo de código.</span><span class="sxs-lookup"><span data-stu-id="70256-128">To automate this procedure, you can use Windows PowerShell to run a command on the Administration and Monitoring Server that is similar to the following code example.</span></span>

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    <span data-ttu-id="70256-129">Con las descripciones de la tabla siguiente, reemplace los valores del ejemplo de código por valores que coincidan con su entorno.</span><span class="sxs-lookup"><span data-stu-id="70256-129">Using the descriptions in the following table, replace the values in the code example with values that match your environment.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="70256-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="70256-130">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="70256-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="70256-131">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="70256-132">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="70256-132">$SERVERNAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="70256-133">Nombre del servidor al que se movieron los informes.</span><span class="sxs-lookup"><span data-stu-id="70256-133">Name of the server to which the Reports were moved.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="70256-134">$SRSINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="70256-134">$SRSINSTANCENAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="70256-135">Nombre de la instancia de SQL Server Reporting Services a la que se movieron los informes.</span><span class="sxs-lookup"><span data-stu-id="70256-135">Name of the instance of SQL Server Reporting Services to which the Reports were moved.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="70256-136">Reanudar la instancia del sitio web de administración y supervisión</span><span class="sxs-lookup"><span data-stu-id="70256-136">Resume the instance of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="70256-137">En el servidor que ejecuta el sitio web de administración y supervisión, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de administración y supervisión.</span><span class="sxs-lookup"><span data-stu-id="70256-137">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="70256-138">Para automatizar este procedimiento, puede usar Windows PowerShell para ejecutar un comando similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="70256-138">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    <span data-ttu-id="70256-139">**Nota:**  Para ejecutar este comando, debe agregar el módulo IIS para Windows PowerShell a la instancia actual de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="70256-139">**Note** To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

     



## <span data-ttu-id="70256-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="70256-140">Related topics</span></span>


[<span data-ttu-id="70256-141">Cómo configurar los informes de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="70256-141">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="70256-142">Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="70256-142">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="70256-143">Movimiento de funciones de MBAM 2.5 a otro servidor</span><span class="sxs-lookup"><span data-stu-id="70256-143">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 
## <span data-ttu-id="70256-144">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="70256-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="70256-145">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="70256-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="70256-146">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="70256-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





