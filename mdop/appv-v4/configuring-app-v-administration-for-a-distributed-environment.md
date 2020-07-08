---
title: Configuración de administración de App-V para entorno distribuido
description: Configuración de administración de App-V para entorno distribuido
author: dansimp
ms.assetid: 53971fa9-8319-435c-be74-c37feb9af1da
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c1a638d6afde9270859c8aa98fc9f421c39cfc72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821911"
---
# Configuración de administración de App-V para entorno distribuido


Al diseñar la infraestructura de su organización específica, puede instalar el servicio Web de administración de App-V en un equipo que no sea el equipo en el que instala el servidor de administración de App-V. Algunas de las razones comunes para separar estos componentes de App-V son las siguientes:

-   Rendimiento

-   Confiabilidad

-   Disponibilidad

-   Escalabilidad

Separar el servidor de administración y el servicio Web de administración requiere configuración adicional para que la infraestructura funcione correctamente. Cuando separe estas dos características pero no complete los procedimientos que se describen en este tema, la consola de administración se conectará al servicio Web de administración, pero no podrá autenticar correctamente con el almacén de datos. La consola de administración no se cargará correctamente y el administrador no podrá completar ninguna tarea administrativa.

Este comportamiento se produce porque el servicio Web de administración no puede usar las credenciales que se le han pasado desde la consola de administración para acceder al almacén de datos. La solución es configurar el servidor de servicio Web de administración para que sea "de confianza para la delegación".

## Configuración de servicios de dominio de Active Directory


También es necesario configurar correctamente los servicios de dominio de Active Directory para que funcionen en un entorno distribuido. Esta sección incluye la información que necesita para configurar los servicios de dominio de Active Directory.

### Cuando el servicio SQL usa una cuenta de sistema local

Para configurar el entorno en el que el servicio SQL usa la cuenta del sistema local, cambie las propiedades de la cuenta del equipo del servicio Web de administración para que sea de confianza para la delegación. Para obtener procedimientos detallados sobre cómo hacer esto, consulte [Cómo configurar el servidor para que sea de confianza para la delegación](how-to-configure-the-server-to-be-trusted-for-delegation.md)

### Cuando el servicio SQL usa una cuenta basada en el dominio

Para configurar el entorno en el que los servidores SQL usan cuentas de servicio basadas en el dominio, debe considerar si se aplican diversos factores, entre los que se incluyen los siguientes:

-   Agrupación de SQL Server

-   Replicación

-   Tareas automatizadas

-   Servidores vinculados

Para obtener información sobre cómo configurar los servicios de dominio de Active Directory cuando el servicio SQL usa una cuenta basada en el dominio, consulte <https://go.microsoft.com/fwlink/?LinkId=151968> .

 

 





