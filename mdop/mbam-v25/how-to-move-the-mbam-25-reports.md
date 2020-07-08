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
# Cómo mover los informes de MBAM 2.5


Use estos procedimientos para mover la característica informes de un equipo a otro, es decir, para mover la característica de informes del servidor a al servidor B.

A continuación, se resumen los pasos para mover la característica informes:

1.  Detenga todas las instancias del sitio web de supervisión y administración de MBAM.

2.  Instale el software de servidor MBAM 2,5 en el servidor B y configure la característica de informes en el servidor B.

3.  Actualice los datos de conexión de los informes en los servidores de supervisión y administración de MBAM.

4.  Reanude la instancia del sitio web de supervisión y administración de MBAM.

**Nota:**  Para ejecutar los scripts de ejemplo de Windows PowerShell en este tema, debe actualizar la Directiva de ejecución de Windows PowerShell para habilitar la ejecución de scripts. Consulte [ejecución de scripts de Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) para obtener instrucciones.

 

**Detener el sitio web de administración y supervisión de MBAM**

-   En el servidor que ejecuta el sitio web de administración y supervisión, use la consola del administrador de Internet Information Services (IIS) para detener el sitio web de administración y supervisión.

    Para automatizar este procedimiento, puede usar Windows PowerShell para escribir un comando similar al siguiente:

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**Instalar el software de servidor MBAM y ejecutar el Asistente para la configuración del servidor de MBAM en el servidor B**

1.  Instale el software del servidor de MBAM en el servidor B. Para obtener instrucciones, consulte [Installing the MBAM 2,5 Server Software](installing-the-mbam-25-server-software.md).

2.  En el servidor B, inicie el Asistente para la configuración del servidor de MBAM, haga clic en **Agregar nuevas características**y, a continuación, seleccione solo la característica **informes** .

    Como alternativa, puede usar el cmdlet **enable-MbamReport** de Windows PowerShell para configurar los informes.

    Para obtener instrucciones sobre cómo configurar los informes, consulte [Cómo configurar los informes de MBAM 2,5](how-to-configure-the-mbam-25-reports.md).

**Actualizar los datos de conexión de los informes en el servidor de administración y supervisión**

1.  En el servidor que ejecuta la característica informes, use la consola del administrador de Internet Information Services (IIS) para actualizar la dirección URL de los informes.

2.  Expanda **Administración y supervisión de Microsoft BitLocker**y, a continuación, seleccione el nodo del **Departamento de soporte técnico** .

3.  En la sección **Administración** de la **vista características**, seleccione **Editor de configuración**.

4.  En el campo **section** , seleccione **appSettings**.

5.  Seleccione la fila de la **colección** y, a continuación, haga clic en el botón "puntos suspensivos" **(...)** en el extremo derecho del panel para abrir el editor de la **colección**.

6.  En el **Editor de colecciones**, seleccione la fila que contiene **Microsoft. Mbam. Reports. URL**y actualice el valor de **Microsoft. Mbam. Reports. URL** para reflejar el nombre del servidor para el servidor B.

    Si ha configurado previamente la característica informes en una instancia con nombre de SQL Server Reporting Services, agregue o actualice el nombre de la instancia a la dirección URL, por ejemplo:

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  Para automatizar este procedimiento, puede usar Windows PowerShell para ejecutar un comando en el servidor de administración y supervisión que es similar al siguiente ejemplo de código.

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    Con las descripciones de la tabla siguiente, reemplace los valores del ejemplo de código por valores que coincidan con su entorno.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Parámetro</th>
    <th align="left">Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>$SERVERNAME $</p></td>
    <td align="left"><p>Nombre del servidor al que se movieron los informes.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$SRSINSTANCENAME $</p></td>
    <td align="left"><p>Nombre de la instancia de SQL Server Reporting Services a la que se movieron los informes.</p></td>
    </tr>
    </tbody>
    </table>

     

**Reanudar la instancia del sitio web de administración y supervisión**

1.  En el servidor que ejecuta el sitio web de administración y supervisión, use la consola del administrador de Internet Information Services (IIS) para iniciar el sitio web de administración y supervisión.

2.  Para automatizar este procedimiento, puede usar Windows PowerShell para ejecutar un comando similar al siguiente:

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    **Nota:**  Para ejecutar este comando, debe agregar el módulo IIS para Windows PowerShell a la instancia actual de Windows PowerShell.

     



## Temas relacionados


[Cómo configurar los informes de MBAM 2.5](how-to-configure-the-mbam-25-reports.md)

[Configuración de las funciones de servidor de MBAM 2.5 mediante Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[Movimiento de funciones de MBAM 2.5 a otro servidor](moving-mbam-25-features-to-another-server.md)

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





