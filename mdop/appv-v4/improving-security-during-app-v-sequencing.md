---
title: Mejora de la seguridad durante la secuenciación de App-V
description: Mejora de la seguridad durante la secuenciación de App-V
author: dansimp
ms.assetid: f30206dd-5749-4a27-bbaf-61fc21b9c663
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba97c334c4ac9a928fee3d69c265c12e82e43619
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816360"
---
# Mejora de la seguridad durante la secuenciación de App-V


Empaquetar aplicaciones para la secuencia es la mayor tarea en curso en una infraestructura de App-V. Como esta tarea está en curso, debe considerar cuidadosamente la creación de directivas y procedimientos para realizar el seguimiento de las aplicaciones. En App-V 4.5, durante la secuenciación, puede capturar listas de control de acceso (ACL) en los activos de archivo de la aplicación virtualizada.

## Análisis de virus en el secuenciador


Es recomendable instalar el software de digitalización en el equipo de secuenciación y, después, analizar el equipo en busca de virus y malware. Una vez que el equipo de secuenciación se digitalice y esté libre de virus o malware, deshabilite el software de análisis, incluido todo el software de detección antivirus y de malware, en el equipo de secuenciación antes de la secuencia de cualquier aplicación. Esto acelera el proceso de secuencia y evita que se detecten los componentes de software de análisis durante la secuenciación y se incluyen en el paquete de aplicación virtual.

## Captura de ACL en archivos (NTFS)


El secuenciador captura los permisos NTFS (las ACL) de los archivos que se supervisan durante la fase de instalación de secuenciación. (Antes de la publicación de App-V 4.5, las ACL no se capturaban como parte del proceso de secuencia). Esta nueva característica permite que se ejecuten ciertas aplicaciones para los usuarios con un bajo nivel de permisos que normalmente requeriría privilegios administrativos.

Esta característica también permite que el ingeniero de secuenciación Capture la configuración de seguridad identificada por el proveedor. Si no se aplica la configuración recomendada por el proveedor, podría dejar la aplicación abierta para atacar o hacer un uso indebido por parte de los usuarios. Para obtener información sobre si debe implementar una aplicación con ACL abiertas, consulte el grupo de soporte técnico de aplicaciones o el proveedor de software.

**Importante**  Aunque el secuenciador captura las ACL de NTFS durante la supervisión de la fase de instalación de la secuenciación, no captura las ACL para el registro. Los usuarios tienen acceso total a todas las claves del registro para las aplicaciones virtuales excepto los servicios. Sin embargo, si un usuario modifica el registro de una aplicación virtual, ese cambio se almacena en una ubicación específica ( `uservol_sftfs_v1.pkg` ) y no afectará a otros usuarios.

 

Durante la fase de instalación, un ingeniero de secuenciación puede modificar los permisos predeterminados de los archivos si es necesario. Una vez completado el proceso de secuenciación, pero antes de guardar el paquete, el ingeniero de secuencias puede elegir exigir los descriptores de seguridad que se capturan durante la fase de instalación. Es recomendable exigir el cumplimiento de los descriptores de seguridad si ninguna otra solución permite que la aplicación se ejecute correctamente una vez virtualizada.

 

 





