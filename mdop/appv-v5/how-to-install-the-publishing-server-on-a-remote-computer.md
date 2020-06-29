---
title: Cómo instalar el servidor de publicación en un equipo remoto
description: Cómo instalar el servidor de publicación en un equipo remoto
author: dansimp
ms.assetid: 37970706-54ff-4799-9485-b9b49fd50f37
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9d711fa51ade856b3ac5880ba60a19315c358734
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813998"
---
# Cómo instalar el servidor de publicación en un equipo remoto


Use el siguiente procedimiento para instalar el servidor de publicación en un equipo independiente. Antes de llevar a cabo el siguiente procedimiento, asegúrese de que la base de datos y el servidor de administración están disponibles.

**Para instalar el servidor de publicación en un equipo independiente**

1. Copie los archivos de instalación de App-V 5,0 Server en el equipo en el que desea instalarlo. Para iniciar la instalación de servidor de App-V 5,0, haga clic con el botón secundario del ratón y ejecute **appv\_server\_setup.exe** como administrador. Haz clic en **Instalar**.

2. En la página **Introducción** , revise y acepte los términos de licencia y haga clic en **siguiente**.

3. En la página **usar Microsoft Update para ayudar a mantener la seguridad de su equipo y la Página actualizada** , para habilitar las actualizaciones de Microsoft, seleccione **usar Microsoft Update al buscar actualizaciones (recomendado).** Para deshabilitar las actualizaciones de Microsoft, seleccione **no quiero usar Microsoft Update**. Haz clic en **Siguiente**.

4. En la página **selección de características** , seleccione la casilla **Publishing Server** y haga clic en **siguiente**.

5. En la página **Ubicación de instalación** , acepte la ubicación predeterminada y haga clic en **siguiente**.

6. En la página **configurar Publishing Server** , especifique los siguientes elementos:

   -   La dirección URL del servicio de administración a la que se conectará el servidor de publicación. Por ejemplo, **http://ManagementServerName:12345** .

   -   Especifique el nombre del sitio web que desea usar para el servicio de publicación. Acepte el valor predeterminado si no tiene un nombre personalizado.

   -   Para el **enlace de Puerto**, especifique un número de puerto único que usará App-V 5,0, por ejemplo, **54321**.

7. En la página **preparado para instalar** , haga clic en **instalar**.

8. Una vez completada la instalación, el servidor de publicación debe registrarse en el servidor de administración. En la consola de administración de App-V 5,0, realice los siguientes pasos para registrar el servidor:

   1.  Abra la consola de servidor de administración de App-V 5,0.

   2.  En el panel izquierdo, seleccione **Servers**y, a continuación, **Register New Server**.

   3.  Escriba el nombre de este servidor y una descripción (si es necesario) y haga clic en **Agregar**.

9. Para comprobar si el servidor de publicación se está ejecutando correctamente, debe importar un paquete al servidor de administración, encontrarlo en un grupo de AD y publicar el paquete. Con un explorador de Internet, abra la siguiente dirección URL: <strong> http://publishingserver:pubport </strong> . Si el servidor se ejecuta correctamente, se mostrará información similar a la siguiente:

   ```xml
   <Publishing Protocol="1.0">
     <Packages>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" VersionId="5d03c08f-51dc-4026-8cf9-15ebe3d65a72" PackageUrl="\\server\share\file.appv" />
     </Packages>
     <NoGroup>
       <Package PackageId="28115343-06e2-44dc-a327-3a0b9b868bda" />
     </NoGroup>
   </Publishing>
   ```

   **¿Tiene una sugerencia para App-V**? Agregue o vote por sugerencias [aquí](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization). **¿Tiene un problema de App-V?** Use el [Foro de TechNet de App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Temas relacionados


[Implementación de App-V 5.0](deploying-app-v-50.md)

 

 





