---
title: Cómo configurar el Firewall de Windows Server 2008 para App-V
description: Cómo configurar el Firewall de Windows Server 2008 para App-V
author: dansimp
ms.assetid: 57f4ed17-0651-4a3c-be1e-29d9520c6aeb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 19e4cda9ac3b908f68e4f69b9663033d8a21ae41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817720"
---
# Cómo configurar el Firewall de Windows Server 2008 para App-V


Con la introducción de Windows Server2008, los componentes de Firewall e IPsec se han fusionado en un solo servicio y se han mejorado las capacidades de este servicio. El nuevo servicio de Firewall admite la inspección de estado entrante y saliente. Además, puede configurar reglas de firewall y directivas de IPsec específicas mediante directivas de grupo. Para obtener más información sobre el Firewall de Windows en Windows Server2008, consulte <https://go.microsoft.com/fwlink/?LinkId=151980> .

El procedimiento siguiente no incluye agregar una excepción para la publicación de ICO y OSD a través de SMB o HTTP/HTTPS. Dichas excepciones se agregan automáticamente según el perfil de red y los roles instalados en el Firewall de Windows Server 2008.

**Nota:**  Si el servidor de administración está configurado para usar RTSP, repita este procedimiento para agregar el `sghwsvr.exe` programa como una excepción.

El servidor de streaming de App-V requiere la excepción del programa `sglwdsptr.exe` para la comunicación de rtsps. Un servidor de streaming de App-V que use RTSP para la comunicación también necesita una excepción de programa para `sglwsvr.exe` .

 

**Para configurar Firewall de Windows Server2008 para App-V**

1.  Abra el **firewall de Windows con** la consola de administración de seguridad avanzada mediante el panel de control o escribiendo `wf.msc` en la línea ejecutar.

2.  Cree una nueva regla de entrada y seleccione **programa**.

3.  Seleccione la ruta de acceso del programa y vaya a `sghwdsptr.exe` , que se encuentra de forma predeterminada en `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .

4.  Haz clic en **Siguiente**.

5.  En la página de **acciones** , seleccione **permitir la conexión**y, a continuación, haga clic en **siguiente**.

6.  Seleccione los **perfiles** que desea aplicar a la regla de entrada.

7.  Proporcione un nombre y una descripción para la regla y haga clic en **Finalizar**.

## Temas relacionados


[Cómo configurar el Firewall de Windows Server 2003 para App-V](how-to-configure-windows-server-2003-firewall-for-app-v.md)

 

 





