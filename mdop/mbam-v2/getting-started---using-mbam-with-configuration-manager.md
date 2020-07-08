---
title: 'Tareas iniciales: Uso de MBAM con Administrador de configuración'
description: 'Tareas iniciales: Uso de MBAM con Administrador de configuración'
author: dansimp
ms.assetid: b0a1d3cc-0b01-4b69-a2cd-fd09fb3beda4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 654de38918102a41395efe37dc593ce8f49113e4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825170"
---
# Tareas iniciales: Uso de MBAM con Administrador de configuración


Al instalar Microsoft BitLocker Administration and Monitoring (MBAM), puede elegir una topología que integre MBAM con Configuration Manager 2007 o SystemCenter2012 ConfigurationManager. Para obtener una lista de las versiones compatibles de Configuration Manager que admite MBAM, consulte [planificación para implementar MBAM con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md). En la topología integrada, las características de compatibilidad de hardware e informes se quitan de MBAM y se obtiene acceso a ellas desde Configuration Manager.

**Importante**  Windows to go no se admite al instalar la topología integrada de MBAM con Configuration Manager 2007.

 

## Uso de MBAM con Administrador de configuración


La integración de MBAM se basa en un nuevo paquete de configuración que instala los tres elementos siguientes en Configuration Manager 2007 o SystemCenter2012 ConfigurationManager, que se describen en detalle en las secciones siguientes:

Datos de configuración que se componen de elementos de configuración y una línea base de configuración

Colección

Informes

### Datos de configuración

Los datos de configuración instalan una línea base de configuración, denominada "protección de BitLocker", que contiene dos elementos de configuración: "protección de unidades del sistema operativo de BitLocker" y "protección de las unidades de datos fijas de BitLocker". La línea base de configuración se implementa en la colección, que también se crea cuando se instala MBAM. Los dos elementos de configuración proporcionan la base para evaluar el estado de cumplimiento de los equipos cliente. Esta información es capturada, almacenada y evaluada en Configuration Manager. Los elementos de configuración se basan en los requisitos de cumplimiento para las unidades de sistema operativo (OSDs) y las unidades de datos fijas (FDDs). La información necesaria para los equipos implementados se recopila para que se pueda evaluar la conformidad de esos tipos de unidades. De forma predeterminada, la línea base de configuración evalúa el estado de cumplimiento cada 12 horas y envía los datos de cumplimiento a Configuration Manager.

### Colección

MBAM crea una colección que se denomina MBAM equipos compatibles. La línea base de configuración está destinada a los equipos cliente de esta colección. Esta es una colección dinámica que, de forma predeterminada, se ejecuta cada 12 horas y evalúa la pertenencia. La pertenencia se basa en tres criterios:

-   Es una versión compatible del sistema operativo Windows. Actualmente, MBAM solo es compatible con Windows 7 Enterprise y Windows 7 Ultimate, Windows 8 Enterprise y Windows to Go, cuando Windows to Go se ejecuta en Windows 8 Enterprise.

-   Es un equipo físico. No se admiten máquinas virtuales.

-   El módulo de plataforma segura (TPM) está disponible. Para Windows 7 se requiere una versión compatible de TPM 1,2 o posterior. Windows 8 y Windows to go no requieren TPM.

La colección se evalúa en todos los equipos y crea el subconjunto de equipos compatibles que proporciona la base para la evaluación de cumplimiento y los informes para la integración de MBAM.

### Informes

Existen cuatro informes que puede usar para ver el cumplimiento. Estos son:

-   **Panel de cumplimiento de BitLocker Enterprise** : proporciona a los administradores de ti tres vistas distintas de la información en un único informe: distribución de estado de cumplimiento, no conforme (distribución de errores) y distribución de estado de cumplimiento según el tipo de unidad. Las opciones de desglose del informe permiten a los administradores de TI hacer clic en los datos y ver una lista de los equipos que coincidan con el estado que seleccione.

-   **Detalles de cumplimiento de BitLocker Enterprise** : permite a los administradores de ti ver información sobre el estado de compatibilidad con el cifrado de BitLocker de la empresa e incluye el estado de cumplimiento de cada equipo. Las opciones de desglose del informe permiten a los administradores de TI hacer clic en los datos y ver una lista de los equipos que coincidan con el estado que seleccione.

-   **Cumplimiento de equipos con BitLocker** : permite a los administradores de ti ver un equipo individual y determinar por qué se ha notificado con un estado determinado de conforme o no compatible. El informe también muestra el estado de cifrado de las unidades de sistema operativo (OSD) y las unidades de datos fijas (FDDs).

-   **Resumen de cumplimiento de BitLocker Enterprise** : permite a los administradores de ti ver el estado de la conformidad de la empresa con la Directiva de MBAM. El estado de cada equipo es evaluado y el informe muestra un resumen de la compatibilidad de todos los equipos de la empresa con la Directiva. Las opciones de desglose del informe permiten a los administradores de TI hacer clic en los datos y ver una lista de los equipos que coincidan con el estado que seleccione.

## Arquitectura de alto nivel de MBAM con Configuration Manager


En la siguiente imagen se muestra la arquitectura de MBAM con la topología de Configuration Manager. Esta configuración admite hasta 200.000 clientes MBAM en un entorno de producción.

![arquitectura Mbam con Configuration Manager](images/mbam2-cmserver.gif)

A continuación se ofrece una descripción de los servidores, las bases de datos y las características de esta arquitectura. Las características del servidor y las bases de datos de la imagen de arquitectura aparecen debajo del equipo o servidor en el que se recomienda instalarlas.

-   **Servidor de base de datos** : la base de datos de **recuperación**, la base de datos de **Auditoría**y los **informes de auditoría** se instalan en un servidor Windows y en una instancia de SQLServer compatible. La base de datos de recuperación almacena los datos de recuperación que se recopilan de MBAM equipos cliente. La base de datos de auditoría almacena los datos de actividad que se recopilan de los equipos cliente que han tenido acceso a datos de recuperación. Los informes de auditoría proporcionan datos sobre el estado de cumplimiento de los equipos cliente de su empresa.

-   **Servidor de sitio primario de Configuration Manager** : el servidor de Configuration Manager contiene la instalación del servidor de MBAM con la topología de integración de System Center Configuration Manager, que debe instalarse en un servidor de sitio primario de Configuration Manager. El servidor de Configuration Manager recopila la información de inventario de hardware de los equipos cliente y se usa para notificar la compatibilidad de BitLocker de equipos cliente. Al ejecutar la instalación del servidor de instalación de MBAM, se instalan una colección y los datos de configuración en el servidor de sitio primario de Configuration Manager.

-   **Servidor de administración y supervisión** : el **servidor de supervisión y administración** está instalado en un servidor de Windows y consta del sitio web de administración y supervisión y los servicios Web de supervisión. El sitio web de administración y supervisión se usa para auditar actividades y para obtener acceso a datos de recuperación (por ejemplo, claves de recuperación de BitLocker). El **portal de autoservicio** también está instalado en el servidor de administración y supervisión. El portal permite a los usuarios finales de equipos cliente iniciar sesión de forma independiente en un sitio web para obtener una clave de recuperación si pierden o olvidan su contraseña de BitLocker. Los informes de auditoría también se instalan en el servidor de administración y supervisión.

-   **Estación de trabajo de administración** : la **plantilla de directiva** consta de objetos de directiva de grupo que definen la configuración de implementación de MBAM para el cifrado de unidad BitLocker. Puede instalar la plantilla de directiva en cualquier servidor o estación de trabajo, pero normalmente se instala en una estación de trabajo de administración que es un servidor de Windows o un equipo cliente de Windows compatible. La estación de trabajo no tiene que ser un equipo dedicado.

-   Equipo cliente de **Configuration Manager** y **cliente de MBAM**

    -   El **cliente de MBAM** realiza las siguientes tareas:

        -   Usa objetos de directiva de grupo para exigir el cifrado de BitLocker de los equipos cliente de la empresa.

        -   Recopila la clave de recuperación de los tres tipos de unidades de datos de BitLocker: unidades de sistema operativo, unidades de datos fijas y unidades de datos extraíbles (USB).

        -   Recopila información de recuperación e información del equipo de los equipos cliente.

    -   **Cliente de Configuration Manager** : el cliente de Configuration Manager permite a Configuration Manager recopilar datos de compatibilidad de hardware sobre los equipos cliente y permite que Configuration Manager informe de la información de cumplimiento.

## Temas relacionados


[Uso de MBAM con Administrador de configuración](using-mbam-with-configuration-manager.md)

 

 





