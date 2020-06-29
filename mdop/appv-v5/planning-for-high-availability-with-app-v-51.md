---
title: Planificación para alta disponibilidad con App-V 5.1
description: Planificación para alta disponibilidad con App-V 5.1
author: dansimp
ms.assetid: 1f190a0e-10ee-4fbe-a602-7e807e943033
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5c8e0e684051859a4caa2c4ef983c040295bc6d4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813479"
---
# Planificación para alta disponibilidad con App-V 5.1


La configuración del sistema de Microsoft Application Virtualization (App-V) 5,1 puede aprovechar las ventajas de las opciones que mantienen un alto nivel de servicio disponible.

Use la información de las siguientes secciones como ayuda para comprender las opciones para implementar App-V 5,1 en una configuración de alta disponibilidad.

-   [Compatibilidad con clústeres de Microsoft SQL Server](#bkmk-sqlcluster)

-   [Compatibilidad con el equilibrio de carga de red de IIS](#bkmk-iisloadbal)

-   [Compatibilidad con servidores de archivos agrupados en el modo de ejecución (SCS)](#bkmk-clusterscsmode)

-   [Compatibilidad con el reflejo de Microsoft SQL Server](#bkmk-sqlmirroring)

-   [Compatibilidad con Microsoft SQL Server siempre activada](#bkmk-sqlalwayson)

## <a href="" id="bkmk-sqlcluster"></a>Compatibilidad con clústeres de Microsoft SQL Server


Puede ejecutar la base de datos de administración de App-V y la base de datos de informes en equipos que ejecutan clústeres de Microsoft SQL Server. Sin embargo, debe instalar las bases de datos con scripts.

Para obtener instrucciones, vea [cómo implementar las bases de datos de App-V con scripts SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts51.md).

## <a href="" id="bkmk-iisloadbal"></a>Compatibilidad con el equilibrio de carga de red de IIS


Puede usar el equilibrio de carga de red de Internet Information Services (IIS) para configurar un entorno de alta disponibilidad para equipos que ejecuten los servicios de administración de App-V 5. x, publicación y creación de informes implementados mediante IIS.

Revise lo siguiente para obtener más información sobre la configuración de IIS y el equilibrio de carga de red en equipos que ejecutan sistemas operativos de Windows Server:

-   Proporciona información sobre cómo configurar servicios de Internet Information Server (IIS) 7,0.

    [Obtención de alta disponibilidad y escalabilidad: arr y NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)

-   Configuración de Microsoft Windows Server

    [Equilibrio de carga de red](https://go.microsoft.com/fwlink/?LinkId=316370) ( https://go.microsoft.com/fwlink/?LinkId=316370) .

    Esta información también se aplica a los clústeres de equilibrio de carga de red (NLB) de IIS en Windows Server2008, Windows Server2008R2 o Windows Server2012.

    **Nota:**  La funcionalidad de equilibrio de carga de red de IIS en Windows Server2012 es generalmente la misma que en Windows Server2008R2. Sin embargo, algunos detalles de las tareas se modifican en Windows Server2012. Para obtener información sobre las nuevas formas de realizar tareas, consulte [navegación y tareas de administración comunes en Windows server 2012 R2 Preview y Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) ( https://go.microsoft.com/fwlink/?LinkId=316371) .

     

## <a href="" id="bkmk-clusterscsmode"></a>Compatibilidad con servidores de archivos agrupados en el modo de ejecución (SCS)


La ejecución de App-V 5,1 en el modo compartir almacén de contenido (SCS) con servidores de archivos agrupados es compatible.

Puede usar los siguientes pasos para habilitar esta configuración:

-   Configure App-V 5,1 para que se ejecute en el modo de SCS de cliente. Para obtener más información sobre la configuración de App-V 5,1 SCS, consulte [Cómo instalar el cliente de App-v 5,1 para el modo de almacenamiento de contenido compartido](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md).

-   Configure el clúster de servidores de archivos configurado tanto en el modo de escalado horizontal de Microsoft Server2012 como en el modo pre **2012** con una San virtual.

Puede usar los siguientes pasos para validar la configuración:

1.  Agregue un paquete en el servidor de publicación. Para obtener más información sobre cómo agregar un paquete, consulte [Cómo agregar o actualizar paquetes mediante la consola de administración](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md).

2.  Realice una actualización de publicación en el equipo que ejecuta el cliente de App-V 5,1 y abra una aplicación.

3.  Cambiar de nodo de clúster la actualización de publicación en Mid y la transmisión por secuencias para asegurar que la conmutación por error funcione correctamente.

Revise lo siguiente para obtener más información sobre cómo configurar los clústeres de conmutación por error de Windows Server:

-   [Lista de comprobación: crear un servidor de archivos agrupado](https://go.microsoft.com/fwlink/?LinkId=316372) ( https://go.microsoft.com/fwlink/?LinkId=316372) .

-   [Usar volúmenes compartidos de clúster en un clúster de conmutación por error de Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316373) ( https://go.microsoft.com/fwlink/?LinkId=316373) .

## <a href="" id="bkmk-sqlmirroring"></a>Compatibilidad con el reflejo de Microsoft SQL Server


Con el reflejo de Microsoft SQL Server, donde la base de datos del servidor de administración de App-V 5,1 se refleja con dos instancias de SQL Server, se admiten las bases de datos de servidor de administración de App-V 5,1.

Revise lo siguiente para obtener más información sobre cómo configurar el reflejo de Microsoft SQL Server:

-   [Cómo: preparar una base de datos de reflejo para la creación de reflejos (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)

-   [Establecer una sesión de creación de reflejo de base de datos con la autenticación de Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)

Puede usar los siguientes pasos para validar la configuración:

1.  Inicie una sesión de creación de reflejos de Microsoft SQL Server.

2.  Seleccione **conmutación por error** para designar una nueva instancia maestra de Microsoft SQL Server.

3.  Compruebe que el servidor de administración de App-V 5,1 siga funcionando según lo esperado después de la conmutación por error.

La cadena de conexión en el servidor de administración se puede modificar para que incluya **failover Partner = &lt; server2 &gt; **. Esto solo es útil cuando el principal en el reflejo conmuta por error al secundario y el equipo que ejecuta el cliente de App-V 5,1 está haciendo una conexión nueva (por ejemplo, después de reiniciar).

Siga estos pasos para modificar la cadena de conexión para que incluya **failover Partner &lt; = &gt; server2**:

**Importante**  En este tema se describe cómo cambiar el registro de Windows mediante el editor del registro. Si cambia incorrectamente el registro de Windows, puede causar serios problemas que le obliguen a reinstalar Windows. Debe hacer una copia de seguridad de los archivos de registro (System. dat y User. dat) antes de cambiar el registro. Microsoft no puede garantizar que los problemas que puedan surgir al cambiar el registro se puedan resolver. Cambie el registro bajo su propia responsabilidad.

 

1.  Inicie sesión en el servidor de administración y Abra **regedit**.

2.  Vaya a **HKEY \ _LOCAL \ _MACHINE**  \\  **software**  \\  **Microsoft**  \\  **AppV**  \\  **Server**  \\  **ManagementService**.

3.  Modifique el valor de **Administración \ _SQL \ _CONNECTION \ _STRING** valor con el **asociado de conmutación por error = &lt; servidor2 &gt; **.

4.  Reinicie el servicio de administración mediante la consola de IIS.

    **Nota:**  El reflejo de la base de datos está en la lista de características del motor de base de datos obsoletas para Microsoft SQL Server2012 a causa de la característica **AlwaysOn** disponible en Microsoft sql server 2012.

     

Para obtener más información, haga clic en cualquiera de los siguientes vínculos:

-   [Cómo: preparar una base de datos de reflejo para la creación de reflejos (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) ( https://go.microsoft.com/fwlink/?LinkId=394235) .

-   [Cómo: configurar una sesión de creación de reflejo de base de datos (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) ( https://go.microsoft.com/fwlink/?LinkId=394236) .

-   [Establecer una sesión de creación de reflejo de base de datos con la autenticación de Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) ( https://go.microsoft.com/fwlink/?LinkId=394237) .

-   [Características del motor de base de datos obsoletas en SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) ( https://go.microsoft.com/fwlink/?LinkId=394238) .

## <a href="" id="bkmk-sqlalwayson"></a>Compatibilidad con Microsoft SQL Server siempre en la configuración


La base de datos de App-V 5,1 Management Server admite implementaciones en equipos que ejecutan Microsoft SQL Server con la configuración **Always on** .






## Temas relacionados


[Planificación de la implementación de App-V](planning-to-deploy-app-v51.md)

 

 





