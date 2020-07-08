---
title: Cómo validar la instalación de MBAM con Administrador de configuración
description: Cómo validar la instalación de MBAM con Administrador de configuración
author: dansimp
ms.assetid: 8e268539-91c3-4e8a-baae-faf3605da818
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 500c6f6ee5138b5677bf1fa20e2627a56981df1f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822640"
---
# Cómo validar la instalación de MBAM con Administrador de configuración


Después de instalar administración y supervisión de Microsoft BitLocker (MBAM) con Configuration Manager, valide que la instalación haya configurado correctamente todas las características necesarias para MBAM completando los siguientes pasos.

**Para validar la instalación de características del servidor de MBAM con Configuration Manager**

1.  En el servidor donde se implementa System Center Configuration Manager, abra el **Panel de control**. Seleccione el programa que se usa para desinstalar o cambiar un programa. Compruebe que **Administración y supervisión de Microsoft BitLocker** aparece en la lista de programas y características.

    **Nota:**  Para validar la instalación, debe usar una cuenta de dominio que tenga credenciales administrativas de equipo local en cada servidor.

     

2.  Use la consola del administrador de configuración para confirmar que se muestra una nueva colección denominada "MBAMs compatibles".

    Para ver la colección con Configuration Manager 2007: haga clic en **Site Database** ( &lt; **nombresitio** &gt;  -  &lt; **ServerName** &gt; , &lt; **siteName** &gt; ), **Administración de equipos**.

    Para ver la colección con SystemCenter2012 ConfigurationManager: haga clic en el área de trabajo de **activos fijos y cumplimiento** , **colecciones de dispositivos**.

3.  Use la consola del administrador de configuración para comprobar que los siguientes informes aparecen en la carpeta **MBAM** :

    -   Cumplimiento de BitLocker Computer

    -   Panel de cumplimiento de BitLocker Enterprise

    -   Detalles de la compatibilidad con BitLocker Enterprise

    -   Resumen de cumplimiento de BitLocker Enterprise

    Para ver los informes con Configuration Manager 2007: haga clic en **informes**, **Reporting Services**, \ \ \ \ &lt; **nombreDeServidor** &gt; , **carpetas de informes**

    Para ver los informes con SystemCenter2012 ConfigurationManager: haga clic en el área **de trabajo** **supervisión** , informes, **informes**.

4.  Use la consola del administrador de configuración para confirmar que aparece la línea base de configuración "protección de BitLocker".

    Para ver las líneas de base de configuración con el administrador de configuración 2007: haga clic en **Administración de configuración deseada**, **líneas base de configuración**.

    Para ver las líneas de base de configuración con SystemCenter2012 ConfigurationManager: haga clic en el área de trabajo **activos y cumplimiento** , **configuración de cumplimiento**, **líneas de base de configuración**.

5.  Use la consola del administrador de configuración para confirmar que se muestran los siguientes elementos de configuración nuevos:

    -   Protección de las unidades de datos fijas de BitLocker

    -   Protección de unidades del sistema operativo BitLocker

    Para ver los elementos de configuración con Configuration Manager 2007: haga clic en administración de la **configuración deseada**, **elementos de configuración**.

    Para ver los elementos de configuración con SystemCenter2012 ConfigurationManager: haga clic en el área de trabajo **activos y cumplimiento** , **configuración de cumplimiento**, **elementos de configuración**.

## Temas relacionados


[Implementación de MBAM con Administrador de configuración](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





