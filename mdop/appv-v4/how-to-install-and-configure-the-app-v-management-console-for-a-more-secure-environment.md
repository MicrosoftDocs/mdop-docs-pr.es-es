---
title: Cómo instalar y configurar la consola de administración de App-V para un entorno más seguro
description: Cómo instalar y configurar la consola de administración de App-V para un entorno más seguro
author: dansimp
ms.assetid: 9d89ef09-cdbf-48fc-99da-b24fc987ef8f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9887787d1e203410b5517439d897260305d7526e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817371"
---
# Cómo instalar y configurar la consola de administración de App-V para un entorno más seguro


La instalación predeterminada de la consola de administración de App-V incluye compatibilidad con las comunicaciones seguras. Cada consola de administración se configura en función de la conexión cuando la consola se inicia por primera vez o cuando se conecta a un servicio de administración web de App-V adicional. La configuración predeterminada usa SSL sobre el puerto TCP 443. Puede cambiar el número de puerto si el número de puerto se modificó en el servidor. Puede usar el siguiente procedimiento para conectarse a un servicio de administración web de App-V mediante una conexión segura.

**Cómo conectarse a un servicio de administración de App-V mediante una conexión SSL**

1.  Inicie la consola de administración de Application Virtualization.

2.  Haga clic en **Configurar conexión** en el panel acciones de la consola.

3.  Escriba el **nombre de host del servicio Web**y asegúrese de que la selección de **Usar conexión segura** está seleccionada.

    **Importante**  El nombre proporcionado en el nombre de host de servicio Web debe coincidir con el nombre común del certificado o la conexión fallará.

     

4.  Seleccione las credenciales de inicio de sesión apropiadas y haga clic en **Aceptar**.

## Temas relacionados


[Configuración de certificados para admitir el servicio de administración web de App-V](configuring-certificates-to-support-the-app-v-web-management-service.md)

 

 





