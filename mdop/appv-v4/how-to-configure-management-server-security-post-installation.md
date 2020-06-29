---
title: Cómo configurar la postinstalación de seguridad del servidor de administración
description: Cómo configurar la postinstalación de seguridad del servidor de administración
author: dansimp
ms.assetid: 71979fa6-3d0b-4a8b-994e-cb728d013090
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 521e72ead78055a7d3261664ccb75d454c22e622
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817940"
---
# Cómo configurar la postinstalación de seguridad del servidor de administración


Use la consola de administración de App-V para agregar el certificado y configurar el servidor de administración de App-V para mejorar la seguridad. Puede usar el siguiente procedimiento para configurar la seguridad después de la instalación.

**Para configurar la seguridad del servidor de administración después de la instalación**

1.  Abra la consola de administración de App-V y conéctese al **servicio de administración** con privilegios de administrador de App-v.

2.  Expanda el servidor, expanda **grupos de servidores**y, a continuación, seleccione el grupo de servidores adecuado con el que se registró el servidor de administración.

3.  Haga clic con el botón secundario en el objeto servidor de administración y seleccione **propiedades**.

4.  En la pestaña **puertos** , haga clic en **certificado de servidor** y complete el Asistente para seleccionar el certificado que se aprovisionó correctamente.

    **Nota:**  Si no se muestran certificados en el asistente, significa que no se ha aprovisionado un certificado o que el certificado cumple los requisitos de App-V.

     

5.  Haga clic en **siguiente** para continuar con la página **Asistente para certificados** .

6.  Seleccione el certificado correcto en la pantalla **certificados disponibles** .

7.  Haz clic en **Finalizar**.

8.  Después de completar el asistente, desactive **RTSP** como puerto de escucha disponible. Esto evita que se realicen conexiones a través de un canal de comunicación no seguro.

9.  Haga clic en **aplicar**y reinicie el servicio **servidor de aplicaciones virtual de Microsoft** . Use el complemento MMC del servicio para realizar esta tarea.

## Temas relacionados


[Cómo configurar la postinstalación de seguridad del servidor de streaming](how-to-configure-streaming-server-security-post-installation.md)

[Solución de problemas de permisos de certificado](troubleshooting-certificate-permission-issues.md)

 

 





