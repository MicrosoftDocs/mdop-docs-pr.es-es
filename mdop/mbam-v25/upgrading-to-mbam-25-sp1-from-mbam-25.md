---
title: Actualización a MBAM 2.5 SP1 desde MBAM 2.5
description: Actualización a MBAM 2.5 SP1 desde MBAM 2.5
author: dansimp
ms.assetid: ''
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 2/16/2018
ms.openlocfilehash: 330ded822dd9da96a1c33eabcb31d744044dc28e
ms.sourcegitcommit: ae34c5cb5e7979b472b257a4691142e493d5d6fe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/30/2020
ms.locfileid: "11091625"
---
# Actualización a MBAM 2.5 SP1 desde MBAM 2.5
En este tema se describe el proceso de actualización del servidor de administración y supervisión de Microsoft BitLocker (MBAM) 2,5 y el cliente de MBAM de 2,5 a MBAM 2,5 SP1.

### Antes de comenzar
#### Descargar el lanzamiento de servicio de mayo de 2019
[Paquete de optimización de escritorio](https://www.microsoft.com/download/details.aspx?id=58345)

#### Descargar la versión de mantenimiento del 2018 de julio
[Paquete de optimización de escritorio](https://www.microsoft.com/download/details.aspx?id=57157)


#### Comprobar el documentaion de instalación
Compruebe que tiene la documentación actual de su entorno de MBAM, incluidos los nombres de servidor, los nombres de base de datos, las cuentas de servicio y las contraseñas.

### Pasos de la actualización
#### Pasos para actualizar la base de datos MBAM (SQL Server)
1. Usar el configurador de MBAM; Quite la función Reports del servidor SQL Server o donde se hospede la base de datos de SSRS. En función de su entorno, puede ser el mismo servidor o uno independiente.
  > [!NOTE]
  > No verá una opción para quitar las bases de datos; Esto es normal.  
2. Instale 2,5 SP1 (que se encuentra en MDOP-Microsoft Desktop Optimization Pack 2015 desde el sitio del centro de servicios de licencias por volumen:  <https://www.microsoft.com/Licensing/servicecenter/default.aspx>
3. No lo configure en este momento 
4. Usar el configurador de MBAM; volver a agregar el rol informes
5. Usar el configurador de MBAM; volver a agregar el rol de base de datos SQL en SQL Server
6. Al final, se le advertirá de que las bases de DBs ya existen y que no se crearon, pero esto es de esperar
7. Este proceso actualiza las bases de datos existentes en la versión actual que se está instalando.              

#### Pasos para actualizar el servidor de MBAM (ejecutando MBAM e IIS)
1. Usar el configurador de MBAM; quitar los portales de administrador y de autoservicio del servidor IIS
2. Instalar MBAM 2,5 SP1
3. No lo configure en este momento  
4. Usar el configurador de MBAM; volver a agregar los portales de administrador y de autoservicio al servidor IIS 
5. Abra un símbolo del sistema con privilegios elevados, escriba **iisreset**y presione Entrar.
 
#### Pasos para actualizar los clientes/puntos de conexión de MBAM
1. Desinstalar el agente 2,5 de los puntos de conexión de cliente
2. Instalar el agente de 2,5 SP1 en los puntos de conexión de cliente
3. Expulsar la actualización de cliente de Resumen de mayo de 2019 a clientes que ejecutan el agente de 2,5 SP1 
4. No es necesario desinstalar el cliente existente antes de instalar el Resumen de mayo de 2019.  
