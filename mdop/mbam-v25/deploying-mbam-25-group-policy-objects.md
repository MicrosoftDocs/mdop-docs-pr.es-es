---
title: Implementación de objetos de directiva de grupo de MBAM 2.5
description: Implementación de objetos de directiva de grupo de MBAM 2.5
author: dansimp
ms.assetid: 4b835054-6846-463d-af58-8ac4639a1188
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9624b94e9d4808a35e1199290f4cd90a8122f767
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824390"
---
# Implementación de objetos de directiva de grupo de MBAM 2.5


Para implementar MBAM, tiene que establecer la configuración de directiva de grupo que define MBAM configuración de implementación para el cifrado de unidad BitLocker. Para completar esta tarea, debe copiar las plantillas de directiva de grupo MBAM en un servidor o estación de trabajo capaces de ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM) y, a continuación, editar la configuración.

**Importante**  No cambie la configuración de directiva de grupo en el nodo **cifrado de unidad BitLocker** o MBAM no funcionará correctamente. Al establecer la configuración de directiva de grupo en el nodo de **MBAM de MDOP (administración de BitLocker)** , MBAM configura automáticamente la configuración de **cifrado de unidad BitLocker** para usted.

 

## Copia de plantillas de directiva de grupo de MBAM 2.5


Antes de instalar el cliente de MBAM, debe copiar los objetos de directiva de grupo (GPO) específicos de MBAM en la estación de trabajo de administración. Estos GPO definen la configuración de implementación de MBAM para el cifrado de unidad BitLocker. Puede copiar las plantillas de directiva de grupo en cualquier servidor o estación de trabajo que sea un servidor de Windows o un equipo cliente de Windows compatible y que pueda ejecutar la consola de administración de directivas de grupo (GPMC) o la administración avanzada de directivas de grupo (AGPM).

[Copia de plantillas de directiva de grupo de MBAM 2.5](copying-the-mbam-25-group-policy-templates.md)

## Editar la configuración de GPO de MBAM 2,0


Después de crear los GPO necesarios, debe implementar la configuración de la Directiva de grupo MBAM en los equipos cliente de su organización. Para ver y crear GPO, debe tener instalada la consola de administración de directivas de grupo (GPMC) o la administración de directivas de grupo (AGPM) avanzada.

[Edición de configuración de directiva de grupo de MBAM 2.5](editing-the-mbam-25-group-policy-settings.md)

## Mostrar u ocultar el panel de control de MBAM en el panel de control de Windows


Puesto que MBAM ofrece un panel de control personalizado de MBAM que puede reemplazar el panel de control predeterminado de BitLocker de Windows, también puede elegir mostrar u ocultar el panel de control predeterminado de BitLocker a los usuarios finales mediante la configuración de directiva de grupo.

[Ocultación del elemento de Cifrado de unidad BitLocker predeterminado en el Panel de Control](hiding-the-default-bitlocker-drive-encryption-item-in-control-panel-mbam-25.md)

## Otros recursos para implementar objetos de directiva de grupo de MBAM 2,0


[Implementación de MBAM 2.5](deploying-mbam-25.md)

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

 

 





