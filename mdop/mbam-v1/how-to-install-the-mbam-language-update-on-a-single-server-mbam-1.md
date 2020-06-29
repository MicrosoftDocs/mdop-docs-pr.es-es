---
title: Cómo instalar la actualización de lenguaje MBAM en un único servidor
description: Cómo instalar la actualización de lenguaje MBAM en un único servidor
author: dansimp
ms.assetid: e6fe59a3-a3e1-455c-a059-1f23ee083cf6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 94814158335430aba433c180cdba83d0cf15b760
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824751"
---
# Cómo instalar la actualización de lenguaje MBAM en un único servidor


Administración y supervisión de Microsoft BitLocker (MBAM) incluye cuatro roles de servidor que se pueden ejecutar en uno o más equipos. Sin embargo, solo dos características de servidor de MBAM requieren que la actualización admita la instalación de la versión de idioma de MBAM 1,0 y la plantilla de directiva de MBAM. Para actualizar las tres características MBAM necesarias para instalarlas en un equipo, siga los pasos que se describen en este tema.

**Para instalar la actualización de idioma MBAM en un solo servidor**

1.  Abra la consola de administración de Internet Information Services (IIS), vaya a **sitios**y, a continuación, apague el sitio web de supervisión y administración de Microsoft BitLocker.

2.  Edite los enlaces para el sitio web MBAM y, a continuación, modifique temporalmente los enlaces del sitio. Por ejemplo, cambie el puerto de 443 a 9443.

3.  Busque y ejecute el Asistente de instalación de MBAM (MBAMsetup.exe) y seleccione las tres características siguientes:

    1.  Informes de cumplimiento y cumplimiento

    2.  Servidor de administración y supervisión

    3.  Plantillas de directiva de grupo

    **Importante**  Las características del servidor de MBAM deben actualizarse en el siguiente orden: informes de auditoría y cumplimiento en primer lugar, a continuación, el servidor de administración y supervisión. Las plantillas de directiva de grupo se pueden actualizar en cualquier momento sin preocuparse por la secuencia.

     

4.  Después de actualizar la base de datos del servidor, abra la consola de administración de IIS y revise los enlaces del sitio web de supervisión y administración de Microsoft BitLocker.

5.  Elimine uno de los enlaces y asegúrese de que el enlace restante tenga el nombre de host, el certificado y el número de puerto correctos para la configuración de empresa de MBAM.

6.  Reinicie el sitio web de MBAM.

7.  Pruebe la funcionalidad del sitio web de MBAM:

    -   Abra la interfaz Web de MBAM y asegúrese de que puede obtener una clave de recuperación para un cliente.

    -   Exigir el cifrado de un equipo cliente nuevo o manualmente descifrado.

        **Nota:**  El cliente de MBAM se abrirá solo si puede comunicarse con la base de datos de recuperación y hardware.

         

## Temas relacionados


[Implementación de la actualización de versión de idioma de MBAM 1.0](deploying-the-mbam-10-language-release-update.md)

 

 





