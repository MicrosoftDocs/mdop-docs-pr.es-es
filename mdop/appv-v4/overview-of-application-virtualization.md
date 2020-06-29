---
title: Introducción a la virtualización de aplicaciones
description: Introducción a la virtualización de aplicaciones
author: dansimp
ms.assetid: 80545ef4-cf4c-420c-88d6-48e9f226051f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2f3719a817137edfd76b1b972e966c685581c58e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816061"
---
# Introducción a la virtualización de aplicaciones


Microsoft Application Virtualization (App-V) puede hacer que las aplicaciones estén disponibles para los equipos de los usuarios finales sin tener que instalar las aplicaciones directamente en esos equipos. Esto es posible gracias a un proceso conocido como *la secuenciación de la aplicación*, que permite que cada aplicación se ejecute en su propio entorno virtual independiente en el equipo cliente. Las aplicaciones secuenciadas están aisladas entre sí. Esto elimina los conflictos de la aplicación, pero las aplicaciones todavía pueden interactuar con el equipo cliente.

El cliente de App-V es la característica que permite que el usuario final interactúe con las aplicaciones después de que se hayan publicado en el equipo. El cliente administra el entorno virtual en el que se ejecutan las aplicaciones virtualizadas en cada equipo. Una vez instalado el cliente en un equipo, las aplicaciones deben estar disponibles para el equipo a través de un proceso conocido como *publicación*, que permite al usuario final ejecutar las aplicaciones virtuales. El proceso de publicación copia los iconos de la aplicación virtual y los accesos directos en el equipo (por lo general, en el escritorio de Windows o en el menú **Inicio** ) y también copia la definición del paquete y la información de la Asociación de tipos de archivo en el equipo. La publicación también hace que el contenido del paquete de la aplicación esté disponible para el equipo del usuario final.

El contenido del paquete de la aplicación virtual se puede copiar en uno o varios servidores de virtualización de aplicaciones para que pueda transmitirse a los clientes a petición y almacenarse en la memoria caché local. Los servidores de archivos y los servidores web también se pueden usar como servidores de transmisión por secuencias o el contenido se puede copiar directamente en el equipo del usuario final; por ejemplo, si usa un sistema de distribución de software electrónico, como Microsoft Endpoint Configuration Manager. En una implementación de varios servidores, mantener el contenido del paquete y mantenerlo actualizado en todos los servidores de transmisión requiere una solución completa de administración de paquetes. Según el tamaño de su organización, es posible que tenga muchas aplicaciones virtuales disponibles para los usuarios finales de todo el mundo. Administrar los paquetes para asegurarse de que las aplicaciones adecuadas estén disponibles para todos los usuarios donde y cuando necesiten tener acceso a ellos es por lo tanto un requisito importante.

## Características del sistema de Microsoft Application Virtualization


En la siguiente tabla se describen las características principales del sistema de administración de virtualización de aplicaciones de Microsoft.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Característica</th>
<th align="left">Función</th>
<th align="left">Información adicional</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Servidor de Microsoft Application Virtualization Management</p></td>
<td align="left"><p>Responsable de transmitir por secuencias el contenido del paquete y de publicar los accesos directos y las asociaciones de los tipos de archivo en el cliente de virtualización de aplicaciones.</p></td>
<td align="left"><p>El servidor de administración de virtualización de aplicaciones admite actualizaciones activas, administración de licencias y una base de datos que se pueden usar para los informes.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Carpeta de contenido </strong></p></td>
<td align="left"><p>Indica la ubicación de los paquetes de virtualización de aplicaciones para la transmisión por secuencias.</p></td>
<td align="left"><p>Esta carpeta puede encontrarse en un recurso compartido en el servidor de administración de virtualización de aplicaciones o fuera de él.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Consola de administración de Microsoft Application Virtualization</p></td>
<td align="left"><p>Esta consola es una herramienta de administración de complementos de 3,0 MMC que se usa para la administración de Microsoft Application Virtualization Server.</p></td>
<td align="left"><p>Esta herramienta se puede instalar en el servidor de Microsoft Application Virtualization o en una estación de trabajo independiente que tenga Microsoft Management Console (MMC) 3.0 y Microsoft. NETFramework 2,0 instalado.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servicio Web de administración de Microsoft Application Virtualization</p></td>
<td align="left"><p>Responsable de comunicar las solicitudes de lectura y escritura al almacén de datos de la virtualización de aplicaciones.</p></td>
<td align="left"><p>El servicio Web de administración se puede instalar en el servidor de Microsoft Application Virtualization Management o en un equipo independiente que tenga instalado Microsoft Internet Information Services (IIS).</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Almacén de datos de Microsoft Application Virtualization</p></td>
<td align="left"><p>La base de datos de App-V SQL Server responsable de almacenar toda la información relacionada con la infraestructura de virtualización de la aplicación.</p></td>
<td align="left"><p>Esta información incluye todos los registros de aplicaciones, asignaciones de aplicaciones y los grupos responsables de administrar el entorno de virtualización de aplicaciones.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Servidor de streaming de Microsoft Application Virtualization</p></td>
<td align="left"><p>Responsable de hospedar los paquetes de Application Virtualization para la transmisión por secuencias a los clientes de una sucursal, donde el vínculo al servidor de Application Virtualization Management se considera una conexión de redes de área extensa (WAN).</p></td>
<td align="left"><p>Este servidor solo contiene funcionalidad de transmisión por secuencias y no proporciona ni la consola de administración de virtualización de aplicaciones ni el servicio Web de administración de virtualización de aplicaciones.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Microsoft Application Virtualization Sequencer</p></td>
<td align="left"><p>El secuenciador se usa para supervisar y capturar la instalación de aplicaciones para crear paquetes de aplicaciones virtuales.</p></td>
<td align="left"><p>La salida consta de los iconos de la aplicación, un archivo. OSD que contiene información sobre la definición del paquete, un archivo de manifiesto del paquete y el archivo. SFT que contiene los archivos de contenido del programa de aplicación.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Cliente de Microsoft Application Virtualization</p></td>
<td align="left"><p>El cliente de escritorio de Application Virtualization y el cliente de virtualización de aplicaciones para servicios de escritorio remoto proporcionan y administran el entorno virtual de las aplicaciones virtualizadas.</p></td>
<td align="left"><p>El cliente de Microsoft Application Virtualization administra la transmisión de paquetes en la memoria caché, la actualización de publicaciones, el transporte y toda la interacción con los servidores de virtualización de aplicaciones.</p></td>
</tr>
</tbody>
</table>

 

 

 





