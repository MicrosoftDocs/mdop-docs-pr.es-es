---
title: Cómo crear o editar los archivos mof
description: Cómo crear o editar los archivos mof
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825321"
---
# Cómo crear o editar los archivos mof


Antes de instalar administración y supervisión de Microsoft BitLocker (MBAM) con Configuration Manager, debe editar el archivo Configuration. mof. También necesita editar o crear el archivo SMS \ _def. mof, en función de la versión de Configuration Manager que esté usando.

## Editar el archivo Configuration.mof


Para permitir que los equipos cliente informen detalles de compatibilidad con BitLocker a través de los informes de MBAM Configuration Manager, tiene que editar el archivo Configuration. mof para Microsoft System Center Configuration Manager 2007 y SystemCenter2012 ConfigurationManager.

[Editar el archivo Configuration.mof](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a>Crear o editar el archivo SMS \ _def. mof


Para permitir que los equipos cliente informen de los detalles de cumplimiento de BitLocker en los informes de MBAM Configuration Manager, tiene que crear o editar el archivo SMS \ _def. mof. En el administrador de configuración 2007, el archivo ya existe, por lo que tendrá que editar, pero no sobrescribir, el archivo existente. Si está usando SystemCenter2012 ConfigurationManager, debe crear el archivo.

[Crear o editar el archivo SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md)

## Temas relacionados


[Implementación de MBAM con Administrador de configuración](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





