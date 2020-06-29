---
title: Planeación de la implementación del servidor de App-V 5.1
description: Planeación de la implementación del servidor de App-V 5.1
author: dansimp
ms.assetid: eedd97c9-bee0-4749-9d1e-ab9528fba398
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 31e3a116eb511356b061e6ccb18c7e25c060a66e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813438"
---
# Planeación de la implementación del servidor de App-V 5.1


La infraestructura de servidor de Microsoft Application Virtualization (App-V) 5,1 consta de un conjunto de características especializadas que se pueden instalar en uno o varios equipos servidor, en función de los requisitos de la empresa.

## Planeamiento de la implementación de App-V 5,1 Server


El servidor de App-V 5,1 consta de las siguientes características:

-   Servidor de administración: proporciona funcionalidad de administración general para la infraestructura de App-V 5,1.

-   Base de datos de administración: facilita las preimplementaciones de base de datos para la administración de App-V 5,1.

-   Publishing Server: proporciona funcionalidad de hospedaje y transmisión por secuencias para aplicaciones virtuales.

-   Servidor de informes: proporciona App-V 5,1 Reporting Services.

-   Base de datos de informes: facilita las preimplementaciones de base de datos para informes de App-V 5,1.

En la siguiente lista se muestran los métodos recomendados para instalar la infraestructura de servidor de App-V 5,1:

-   Instale el servidor de App-V 5,1. Para obtener más información, vea [cómo implementar el servidor de App-V 5,1](how-to-deploy-the-app-v-51-server.md).

-   Instale las características de base de datos, informes y administración en equipos diferentes. Para obtener más información, vea [Cómo instalar las bases de datos de administración e informes en equipos independientes de la administración y](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services51.md)Reporting Services.

-   Usar la distribución electrónica de software (ESD). Para obtener más información, vea [cómo implementar paquetes de App-V 5,1 con distribución electrónica de software](how-to-deploy-app-v-51-packages-using-electronic-software-distribution.md).

-   Instalar todas las características de servidor en un solo equipo.

## <a href="" id="---------app-v-5-1-server-interaction"></a> Interacción entre App-V 5,1 Server


Esta sección contiene información sobre cómo los diversos roles de servidor de App-V 5,1 interactúan entre sí.

El servidor de administración de App-V 5,1 contiene el repositorio de paquetes y sus configuraciones asignadas. En el caso de los servidores de publicación registrados en el servidor de administración, los metadatos asociados se proporcionan a los servidores de publicación para usarlos cuando se reciben solicitudes de actualización de los equipos que ejecutan el cliente de App-V 5,1. Los servidores de publicación de App-V 5,1 administrados por un solo servidor de administración pueden prestar servicio a distintos clientes y pueden tener nombres de sitios web y enlaces de puertos diferentes. Además, todos los servidores de publicación administrados por el mismo servidor de administración son réplicas entre sí.

**Nota:**  El servidor de administración no realiza ningún equilibrio de carga. Los metadatos asociados simplemente se pasan al servidor de publicación para usarlos al procesar las solicitudes de los clientes.

 

## Protocolos relacionados con el servidor y características externas


A continuación se muestra información sobre los protocolos relacionados con el servidor usados por los servidores de App-V 5,1. La tabla también incluye el mecanismo de informes para cada tipo de servidor.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tipo de servidor</th>
<th align="left">Protocolos</th>
<th align="left">Características externas necesarias</th>
<th align="left">Generación de informes</th>
<th align="left"></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor IIS</p></td>
<td align="left"><p>HTTP</p>
<p>HTTPS</p></td>
<td align="left"><p>Esta combinación de protocolo de servidor requiere un mecanismo para sincronizar el contenido entre el servidor de administración y el servidor de transmisión. Al usar HTTP o HTTPS, use un servidor IIS y un firewall para proteger al servidor de la exposición a Internet.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left"><p>Archivo</p></td>
<td align="left"><p>SMB</p></td>
<td align="left"><p>Esta combinación de protocolo de servidor requiere compatibilidad para sincronizar el contenido entre el servidor de administración y el servidor de transmisión. Use un equipo cliente con capacidad de uso compartido de archivos o transmisión.</p></td>
<td align="left"><p>Interna</p></td>
<td align="left"></td>
</tr>
</tbody>
</table>

 






## Temas relacionados


[Planificación de la implementación de App-V](planning-to-deploy-app-v51.md)

[Implementación del servidor de App-V 5.1](deploying-the-app-v-51-server.md)

 

 





