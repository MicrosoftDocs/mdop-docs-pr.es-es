---
title: Notas de la versión de App-V 4.6
description: Notas de la versión de App-V 4.6
author: dansimp
ms.assetid: a3eba129-edac-48bf-a933-3bf43a9873e5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9eee3c309a927a72155dec707d8dd95f43e90fb9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822370"
---
# Notas de la versión de App-V 4.6


Para buscar estas notas de la versión, presione CTRL + F.

**Importante**  Lea estas notas de la versión minuciosamente antes de instalar el sistema de administración de Microsoft Application Virtualization (App-V). Estas notas de la versión contienen información que necesita para instalar correctamente Application Virtualization (App-V) 4.6. Este documento contiene información que no está disponible en la documentación del producto. Si hay una discrepancia entre estas notas de la versión y otra documentación de App-V, el cambio más reciente debe considerarse autoritario.

 

## Protegerse contra virus y vulnerabilidades de seguridad


Para ayudar a protegerse contra virus y vulnerabilidades de seguridad, es importante instalar las últimas actualizaciones de seguridad disponibles para cualquier nuevo software que se instale. Para obtener más información, consulte el [sitio web de seguridad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problemas conocidos con la virtualización de aplicaciones 4.6


Esta sección proporciona la información más actualizada sobre problemas con Microsoft Application Virtualization (App-V) 4.6. Estos problemas no aparecen en la documentación del producto y, en algunos casos, podrían contradecir la documentación del producto existente. Siempre que sea posible, estos problemas se resolverán en versiones posteriores.

### Error de carga o instalación que ejecuta un archivo de Windows Installer generado por el secuenciador de App-V 4.5

La ejecución de un archivo de Windows Installer generado por el secuenciador de App-V 4.5 genera un error de carga o instalación al intentar ejecutarlo en un cliente de App-V 4,6. Verá el siguiente mensaje: "este paquete requiere Microsoft Application Virtualization Client 4.5 o posterior". Use la siguiente solución alternativa.

WORKAROUNDOpen el paquete antiguo con el secuenciador de App-V 4,5 SP1 o el secuenciador de App-V 4,6 y genera un nuevo archivo. msi para el paquete.

**Nota:**  Como alternativa, en el símbolo del sistema, el secuenciador de App-V puede generar el nuevo archivo. msi con los parámetros */Open* y */MSI* , por ejemplo, `SFTSequencer /Open:”package.sprj” /MSI` . Para obtener más información, vea [Cómo actualizar una aplicación virtual mediante la línea de comandos](how-to-upgrade-a-virtual-application-by-using-the-command-line.md).

 

### Información de copyright de notas de versión

Este documento se proporciona "tal cual". La información y las vistas expresadas en este documento, incluidas las direcciones URL y otras referencias a sitios web de Internet, pueden cambiar sin previo aviso. Usted asume el riesgo de su uso.

Algunos ejemplos que se describen en este artículo se proporcionan solo para la ilustración y son ficticios.No se pretende ni se debe deducir ninguna asociación o conexión real.

Este documento no le proporciona derechos legales sobre ninguna propiedad intelectual en ningún producto de Microsoft. Puede copiar y usar este documento para su referencia interna. Puede modificar este documento para su referencia interna.



Microsoft, Active Directory, ActiveSync, ActiveX, Excel, SQL Server, Windows, Windows PowerShell, Windows Server y Windows Vista son marcas comerciales del grupo de empresas de Microsoft.

El resto de marcas comerciales pertenecen a sus respectivos dueños.

 

 





