---
title: Clientes unidos a un dominio y no unidos a un dominio
description: Clientes unidos a un dominio y no unidos a un dominio
author: dansimp
ms.assetid: a935dc98-de60-45f3-ab74-2444ce082e88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4385ab3f26bb867dd649fe768e1500c9d015ffa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821631"
---
# Clientes unidos a un dominio y no unidos a un dominio


El cliente de escritorio de App-V puede configurarse para permitir la conexión a una red, independientemente de si el cliente está unido a un dominio o no.

## Clientes Unidos a un dominio


Los clientes Unidos a un dominio, pero fuera de la red interna, pueden comunicarse con la infraestructura de App-V mediante una conexión VPN. Cuando desee proporcionar a los usuarios la capacidad de abandonar la red interna pero seguir comunicándose en una infraestructura de App-V, su entorno requiere muy poca configuración. Como los usuarios ya forman parte del dominio, simplemente debe asegurarse de que se admitan las credenciales almacenadas en caché en el cliente. Esta es la configuración predeterminada y los cambios realizados en esta configuración se pueden realizar desde directivas de grupo.

Tal como se mencionó en la guía de procedimientos recomendados de seguridad de App-V, el usuario intentará enviar su vale de usuario a la infraestructura de App-V para la autenticación. Si el vale ha expirado, volverá a usar NTLM y las credenciales almacenadas en caché en el equipo. Para permitir el uso de roaming, los administradores deben asegurarse de que el servidor de publicación al que se tiene acceso internamente está disponible en el mismo nombre de forma externa para que los nombres se resuelvan correctamente.

## Clientes no Unidos a un dominio


Los clientes que no tienen un dominio Unido pero deben comunicarse en la infraestructura de App-V deben estar configurados para garantizar que la autenticación de la infraestructura de App-V se realice correctamente. El cliente de escritorio de App-V no permite solicitar el proceso de actualización de publicación, por lo que el cliente debe estar configurado para presentar las credenciales apropiadas al servidor de administración de App-V.

El servidor de publicación, que está configurado para la actualización de publicaciones desde el cliente que no está unido a un dominio, requiere que el nombre externo en el que se encuentra configurado el acceso de los clientes sea el nombre común o un nombre alternativo de asunto (SAN) en el certificado del servidor de publicación.

## Temas relacionados


[Cómo asignar las credenciales correctas para Windows Vista](how-to-assign--the-proper-credentials-for-windows-vista.md)

[Cómo asignar las credenciales correctas para Windows XP](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





