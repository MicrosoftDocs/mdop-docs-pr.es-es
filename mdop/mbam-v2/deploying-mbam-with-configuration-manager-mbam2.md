---
title: Implementación de MBAM con Administrador de configuración
description: Implementación de MBAM con Administrador de configuración
author: dansimp
ms.assetid: 89d03e29-457a-471d-b893-e0b74a83ec50
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c6cffc1cf51a26aeaa94fcb265199c19f0f34abe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823451"
---
# Implementación de MBAM con Administrador de configuración


Los procedimientos siguientes describen cómo implementar Microsoft BitLocker Administration and Monitoring (MBAM) con Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager por conel configuración recomendada, que se describe en [Introducción: uso de MBAM con Configuration Manager](getting-started---using-mbam-with-configuration-manager.md). La configuración recomendada es instalar las características de administración y supervisión en uno o varios servidores de supervisión y administración de Microsoft BitLocker, e instalar Microsoft System Center Configuration Manager 2007 o MicrosoftSystemCenter2012 ConfigurationManager en un servidor independiente.

Antes de iniciar la instalación, asegúrese de que cumple con los requisitos previos y los requisitos de hardware y software para instalar MBAM con Configuration Manager revisando la [planificación para implementar MBAM con Configuration Manager](planning-to-deploy-mbam-with-configuration-manager-2.md).

Si alguna vez necesita volver a instalar MBAM con la topología del administrador de configuración, tendrá que quitar los objetos de Configuration Manager en primer lugar. Lea el [artículo](https://go.microsoft.com/fwlink/?LinkId=286306) de la Knowledge base para obtener más información.

Los pasos para instalar MBAM con Configuration Manager se agrupan en las siguientes categorías. Complete los pasos de cada categoría para completar la instalación.

## Cómo crear o editar los archivos mof


Para permitir que los equipos cliente informen detalles de compatibilidad con BitLocker a través de los informes de MBAM Configuration Manager, tiene que editar el archivo **Configuration. mof** y editar o crear el archivo Sms \ _def. mof, en función de la versión de Configuration Manager que esté usando.

[Cómo crear o editar los archivos mof](how-to-create-or-edit-the-mof-files.md)

## Cómo instalar MBAM con Administrador de configuración


En esta sección se describen los pasos para instalar lo siguiente: MBAM en el servidor de Configuration Manager; las bases de datos de recuperación y auditoría en el servidor de base de datos; y las características de servidor de administración y supervisión en el servidor de administración y supervisión.

[Cómo instalar MBAM con Administrador de configuración](how-to-install-mbam-with-configuration-manager.md)

## Cómo validar la instalación de características del servidor de MBAM en el servidor de Configuration Manager


Una vez completada la instalación de administración y supervisión de Microsoft BitLocker, valide que la instalación haya configurado correctamente todas las características de MBAM necesarias para el servidor de Configuration Manager.

[Cómo validar la instalación de MBAM con Administrador de configuración](how-to-validate-the-mbam-installation-with-configuration-manager.md)

## Temas relacionados


[Uso de MBAM con Administrador de configuración](using-mbam-with-configuration-manager.md)

 

 





