---
title: Cómo instalar la actualización de lenguaje MBAM en servidores distribuidos
description: Cómo instalar la actualización de lenguaje MBAM en servidores distribuidos
author: dansimp
ms.assetid: 5ddc64c6-0417-4a04-843e-b5e18d9f1a52
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6758463c6fc038c4d6ea86c0d49804f29bb543d3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825700"
---
# Cómo instalar la actualización de lenguaje MBAM en servidores distribuidos


Administración y supervisión de Microsoft BitLocker (MBAM) incluye cuatro roles de servidor que se pueden ejecutar en uno o más equipos. Sin embargo, solo dos características de servidor de MBAM requieren que la actualización admita la instalación de la versión de idioma de MBAM 1,0 y la plantilla de directiva de MBAM. En las configuraciones con las características de servidor de MBAM instaladas en varios equipos, solo es necesario actualizar las siguientes características de servidor:

-   Los informes de auditoría y cumplimiento de MBAM

-   El servidor de supervisión y administración de MBAM

**Importante**  Las características del servidor de MBAM deben actualizarse en este orden: informes de cumplimiento y auditoría en primer lugar, y luego el servidor de administración y supervisión. Las plantillas de directiva de grupo MBAM se pueden actualizar en cualquier momento, sin preocuparse por la secuencia.

 

**Para instalar la actualización de idioma MBAM en la característica de servidor de informes y cumplimiento normativo de MBAM**

1.  En el equipo que ejecuta la función MBAM Compliance and Audit Report, busque y ejecute el Asistente para la configuración de actualización de idioma de MBAM (MBAMsetup.exe).

2.  Complete el Asistente para los informes de comprobación y cumplimiento y, a continuación, cierre el asistente.

**Para instalar la actualización de idioma MBAM en la característica servidor de administración y supervisión de MBAM**

1.  En el equipo que ejecuta la característica de administración y supervisión de MBAM, abra la consola de administración de Internet Information Services (IIS), vaya a **sitios**y, a continuación, apague el sitio web de supervisión y administración de Microsoft BitLocker.

2.  Elija editar los enlaces para el sitio web de MBAM y, a continuación, modifique los enlaces del sitio. Por ejemplo, cambie el puerto de 443 a 9443.

3.  Busque y ejecute el Asistente para la configuración de la actualización de idioma de MBAM (MBAMsetup.exe). Complete el Asistente para la característica servidor de administración y supervisión y, a continuación, cierre el asistente.

4.  Después de actualizar la base de datos del servidor, abra la consola de administración de IIS y revise los enlaces del sitio web de supervisión y administración de Microsoft BitLocker.

5.  Elimine el enlace anterior y asegúrese de que el enlace restante tenga el nombre de host, el certificado y el número de puerto correctos para la configuración de empresa de MBAM.

6.  Reinicie el sitio web de MBAM.

7.  Pruebe la funcionalidad del sitio web MBAM:

    -   Abra la interfaz Web de MBAM y asegúrese de que puede obtener una clave de recuperación para un cliente.

    -   Exigir el cifrado de un equipo cliente nuevo o manualmente descifrado.

        **Nota:**  El cliente de MBAM se abrirá solo si puede comunicarse con la base de datos de recuperación y hardware.

         

## Temas relacionados


[Implementación de la actualización de versión de idioma de MBAM 1.0](deploying-the-mbam-10-language-release-update.md)

 

 





