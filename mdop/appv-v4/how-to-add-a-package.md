---
title: Cómo agregar un paquete
description: Cómo agregar un paquete
author: dansimp
ms.assetid: 5407fdbe-e658-44f6-a9b8-a566b81dedce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c580d7d131017c52e278adda0208ffcb2e86ccf2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821400"
---
# Cómo agregar un paquete


Puede Agregar un paquete desde la consola de administración de Application Virtualization Server de las siguientes maneras:

-   Importar una aplicación, que crea el paquete automáticamente en el proceso.

-   Agregar un paquete de forma manual.

Se recomienda importar aplicaciones en lugar de agregarlas manualmente. Para obtener más información sobre cómo importar aplicaciones, vea [Cómo importar una aplicación](how-to-import-an-applicationserver.md).

**Para agregar un paquete de forma manual**

1.  En la consola de administración de Application Virtualization Server, haga clic con el botón derecho en el nodo **paquetes** en el panel izquierdo y elija **nuevo paquete**.

2.  En el cuadro de diálogo **nuevo paquete** , escriba un nombre en el campo **nombre del paquete** .

3.  Busque o escriba un nombre de ruta en el campo **ruta de acceso completa del archivo de paquete** . Debe ser un archivo de SFT.

    **Nota:**  Si busca el archivo SFT, reemplace la ruta de acceso local (como C:\\Archivos de Files\\User\ _Apps \\Virtual\ _App \ _Server \\content) con el nombre de host estático o la dirección IP del servidor. El uso de la variable *% SFT \ _SOFTGRIDSERVER%* requiere la configuración del equipo por cliente.

    En los cuadros de diálogo que hacen referencia a servidores de aplicaciones virtuales, debe usar una ubicación de red, como el nombre de host estático del servidor o la dirección IP a la que los usuarios pueden tener acceso. El archivo descriptor de software abierto (OSD) de la aplicación puede reemplazar la variable de marcador de posición *% SFT \ _SOFTGRIDSERER%* por la dirección IP o el nombre de host estático del servidor. Si deja la variable de marcador de posición, debe establecer esta variable en cada equipo cliente que tenga acceso a ese servidor. Establezca una variable de usuario o de sistema en cada equipo para SFT \ _SOFTGRIDSERVER. El valor de la variable debe ser el nombre de host estático o la dirección IP del servidor. Si establece una variable, salga de la sesión del cliente, cierre la sesión y vuelva a usar Microsoft Windows y, a continuación, reinicie la sesión en cada equipo en el que se haya realizado una sesión y que haya establecido la variable.

     

4.  Haz clic en **Siguiente**.

5.  El cuadro de diálogo **Resumen** muestra la ubicación del archivo y le pide que copie el archivo en la ubicación si todavía no lo ha hecho. Haga clic en **Finalizar** una vez que haya verificado la información.

    **Nota:**  Si está administrando aplicaciones en un servidor remoto, en el siguiente cuadro de diálogo, escriba solo la ruta de acceso del archivo relativa a la raíz de contenido del servidor.

     

## Temas relacionados


[Cómo importar una aplicación](how-to-import-an-applicationserver.md)

[Cómo administrar paquetes en la consola de administración de servidor](how-to-manage-packages-in-the-server-management-console.md)

 

 





