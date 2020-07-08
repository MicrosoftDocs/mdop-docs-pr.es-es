---
title: Cómo configurar la postinstalación de seguridad del servidor de streaming
description: Cómo configurar la postinstalación de seguridad del servidor de streaming
author: dansimp
ms.assetid: 9bde3677-d1aa-4dcc-904e-bb49a268d748
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1945b38da5dd50c0bd2fb0c741bd92012e78586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817901"
---
# Cómo configurar la postinstalación de seguridad del servidor de streaming


Configure el servidor de streaming de App-V para mejorar la seguridad a través del registro. Al igual que con el servidor de administración de App-V, se debe aprovisionar correctamente un certificado con el identificador de EKU correcto para la autenticación del servidor antes de completar el siguiente procedimiento posterior a la instalación.

**Para configurar la seguridad del servidor de streaming después de la instalación**

1.  Cree una consola MMC, agregue el complemento **certificados** y seleccione almacén de **certificados de la máquina local**.

2.  Abra los certificados **personales** para el equipo y abra el certificado suministrado para App-V.

3.  En la pestaña **detalles** , desplácese hasta la huella digital y copie el hash en el panel de detalles.

4.  Abra el editor del registro y vaya a `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server` .

5.  Edite el `X509CertHash` valor, pegue el hash de la huella digital en el campo de valor y quite todos los espacios. Haga clic en **Aceptar** para aceptar la edición.

6.  En el editor del registro, vaya a `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts` .

7.  Cree un nuevo valor de **DWORD** denominado "322" y, a continuación, escriba el valor decimal como 322 o el valor hexadecimal como 142.

8.  Reinicie el servicio de transmisión por secuencias.

## Temas relacionados


[Cómo configurar la postinstalación de seguridad del servidor de administración](how-to-configure-management-server-security-post-installation.md)

[Solución de problemas de permisos de certificado](troubleshooting-certificate-permission-issues.md)

 

 





