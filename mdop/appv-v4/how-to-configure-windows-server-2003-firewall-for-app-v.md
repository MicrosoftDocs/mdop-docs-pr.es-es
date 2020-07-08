---
title: Cómo configurar el Firewall de Windows Server 2003 para App-V
description: Cómo configurar el Firewall de Windows Server 2003 para App-V
author: dansimp
ms.assetid: 2c0e80f8-41e9-4164-ac83-b23b132b489a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af75479504b454851ee2efc7ca2638d2daf45053
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817730"
---
# Cómo configurar el Firewall de Windows Server 2003 para App-V


Use el siguiente procedimiento para configurar el Firewall de WindowsServer 2003 para App-V.

**Para configurar Firewall de WindowsServer 2003 para App-V**

1.  En el **Panel de control**, abra el Firewall de **Windows**.

    **Nota:**  Si el servidor no se ha configurado para ejecutar el servicio de Firewall antes de este paso, se le pedirá que inicie el servicio de Firewall.

     

2.  Si los archivos ICO y OSD se publican a través de SMB, asegúrese de que el **uso compartido de impresoras y archivos** está habilitado en la pestaña **excepciones** .

    **Nota:**  Si los archivos ICO y OSD se publican a través de HTTP/HTTPS en el servidor de administración, es posible que tenga que agregar una excepción para HTTP o HTTPS. Si el servidor IIS que hospeda los archivos ICO y OSD está alojado en un equipo independiente del servidor de administración, debe agregar la excepción a ese equipo. Para maximizar el rendimiento, le recomendamos que aloje los archivos ICO y OSD en un servidor independiente del servidor de administración.

     

3.  Agregue una excepción de programa para `sghwdsptr.exe` , que es el ejecutable del servicio servidor de administración. La ruta de acceso predeterminada para este archivo ejecutable es `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .

    **Nota:**  Si el servidor de administración usa RTSP para la comunicación, también debe agregar una excepción de programa para `sghwsvr.exe` .

    El servidor de streaming de App-V requiere una excepción `sglwdsptr.exe` de programa para la comunicación de rtsps. El servidor de streaming de App-V que usa RTSP para la comunicación también necesita una excepción de programa para `sglwsvr.exe` .

     

4.  Asegúrese de que se ha configurado el ámbito adecuado para cada excepción. Para reducir el riesgo, quite cualquier equipo y limite estrictamente las direcciones IP a las que responderá el servidor.

## Temas relacionados


[Cómo configurar el Firewall de Windows Server 2008 para App-V](how-to-configure-windows-server-2008-firewall-for-app-v.md)

 

 





