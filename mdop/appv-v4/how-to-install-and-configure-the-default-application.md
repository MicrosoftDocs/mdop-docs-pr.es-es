---
title: Cómo instalar y configurar la aplicación predeterminada
description: Cómo instalar y configurar la aplicación predeterminada
author: dansimp
ms.assetid: 5c5d5ad1-af40-4f83-8234-39e972f2c29a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1083de7a8ebf94bce0b41c0d3c3edf350a9aff38
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817370"
---
# Cómo instalar y configurar la aplicación predeterminada


La aplicación predeterminada se proporciona como parte de la instalación y se copia automáticamente en el servidor de administración de Microsoft Application Virtualization (App-V) durante la instalación. Se usa para comprobar que el servidor de administración se ha instalado y configurado correctamente, pero debe publicarse en el cliente de Microsoft Application Virtualization (App-V) para que el usuario pueda obtener acceso a él.

Use los procedimientos siguientes para publicar la aplicación predeterminada y para transmitirla.

**Para publicar la aplicación predeterminada**

1.  Inicie sesión en el servidor de administración de App-V con una cuenta que sea miembro del grupo de administradores de App-V especificado durante la instalación.

2.  En el servidor de administración de App-V, haga clic en **Inicio**, haga clic en **herramientas administrativas**y, a continuación, en **consola de administración de virtualización de aplicaciones**.

3.  En la consola de administración de App-V, haga clic en **acciones**y, a continuación, haga clic en **conectar con el sistema de virtualización de aplicaciones**.

4.  En la página **Configurar conexión** , desactive la casilla **Usar conexión segura** .

5.  En el cuadro **nombre de host de servicio Web** , escriba el nombre de dominio completo (FQDN) del servidor de administración de App-V y, a continuación, haga clic en **Aceptar**.

    **Nota:**  También puede usar **localhost** para el nombre de host de servicio Web si está instalado en el servidor de administración.

     

6.  En la consola de administración de App-V, haga clic con el botón secundario en el nodo de **servidor** y haga clic en **Opciones del sistema**.

7.  En la pestaña **General** , en el cuadro **ruta de contenido predeterminada** , escriba la ruta de acceso UNC (Convención de nomenclatura universal) a la carpeta de contenido que creó en el servidor durante la instalación; por ejemplo, \ \ \ \ &lt; nombre de servidor &gt; \\Content y, a continuación, haga clic en **Aceptar**.

    **Importante**  Use el FQDN para el nombre del servidor para que el cliente pueda resolver el nombre correctamente.

     

8.  En la consola de administración de App-V, en el panel de navegación, expanda el nodo **servidor** y, a continuación, haga clic en **aplicaciones**.

9.  En el panel de temas, haga clic en **aplicación predeterminada**y, a continuación, en el panel **acciones** , haga clic en **propiedades**.

10. En el cuadro de diálogo **propiedades** , junto al cuadro Ruta de la **OSD** , haga clic en **examinar**.

11. En el cuadro de diálogo **abrir** , escriba la ruta de acceso UNC a la carpeta de contenido que creó en el servidor durante la instalación; por ejemplo, \ \ \ \ &lt; nombre de servidor &gt; \\Content y presione Entrar. Debe usar el nombre de servidor real y no puede usar el **localhost** aquí.

    **Importante**  Asegúrese de que los valores de los cuadros **ruta de acceso** de la OSD e ruta de acceso al **icono** estén en formato UNC (por ejemplo, \ \ \ \ &lt; nombre de servidor &gt; \\Content\\DefaultApp.ico) y seleccione la carpeta de contenido que ha creado al instalar el servidor. No use **localhost** o una ruta de acceso de archivo que contenga una letra de unidad, como C:\\Archivos de Files\\.. \\.. Objetos.

     

12. Seleccione el archivo DefaultApp. OSD y haga clic en **abrir**.

13. Repita los pasos anteriores para configurar la ruta de acceso del icono.

14. Haga clic en la pestaña **permisos de acceso** y confirme que el grupo de usuarios de App-V tiene permisos de acceso a la aplicación.

15. Haga clic en la pestaña **métodos abreviados** y luego en **publicar en el escritorio del usuario**. Haga clic en **Aceptar**.

16. Abra el explorador de Windows y busque el directorio de contenido.

17. Haga doble clic en el archivo DefaultApp. OSD y ábralo con el Bloc de notas.

18. Busque la línea que contiene la etiqueta **href** y cámbiela por el código siguiente:

         `CODEBASEHREF=”RTSP://<FQDN of your server>:554/DefaultApp.sft”`

    O bien, si usa RTSPs:

         `CODEBASEHREF=”RTSPS://<FQDN of your server>:322/DefaultApp.sft”`

19. Cierre el archivo DefaultApp. OSD y guarde los cambios.

**Para transmitir la aplicación predeterminada**

1.  En el equipo que tiene instalado el cliente de App-V, inicie sesión como un usuario que sea miembro del grupo de usuarios de Application Virtualization especificado durante la instalación del servidor.

2.  En el escritorio, aparece el método abreviado de **aplicaciones predeterminado aplicación de virtualización** . Haga doble clic en el acceso directo para iniciar la aplicación.

3.  Una barra de estado, que aparece sobre el área de notificación de Windows, informa que la aplicación se está iniciando. Si el inicio de la aplicación se realiza correctamente, se muestra la pantalla de título de la aplicación predeterminada. Haga clic en **Aceptar** para cerrar el cuadro de diálogo. Ya ha confirmado que el sistema de App-V se está ejecutando correctamente.

## Temas relacionados


[Cómo configurar servidores para implementación basada en servidor](how-to-configure-servers-for-server-based-deployment.md)

 

 





