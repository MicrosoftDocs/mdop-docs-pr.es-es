---
title: Cómo agregar o quitar la información de redireccionamiento de dirección URL en un área de trabajo de MED-V implementada
description: Cómo agregar o quitar la información de redireccionamiento de dirección URL en un área de trabajo de MED-V implementada
author: dansimp
ms.assetid: bf55848d-bf77-452e-aaa5-4dd4868ff5bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: f0892b16bfc10e6b3f28fe99c51c2c5cedb73d7f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826441"
---
# Cómo agregar o quitar la información de redireccionamiento de dirección URL en un área de trabajo de MED-V implementada


Para editar la información de redireccionamiento de la dirección URL en un área de trabajo de MED-V implementada, le recomendamos que actualice el registro del sistema mediante la Directiva de grupo. Aunque no lo recomendamos, también puede volver a crear e implementar el área de trabajo de MED-V con la información de redireccionamiento de la dirección URL actualizada.

La clave del registro suele encontrarse en:

Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

El siguiente valor de cadena múltiple debe estar presente: `RedirectUrls`

El valor datos para `RedirectUrls` es una lista de todas las direcciones URL que especificó para el redireccionamiento cuando compiló el paquete de área de trabajo Med-v con el **Empaquetador de área de trabajo Med-v**. Para obtener más información, vea [crear un paquete de área de trabajo de MED-V](create-a-med-v-workspace-package.md).

Puede Agregar y quitar información de redirección de la dirección URL realizando una de las siguientes tareas:

-   [Editar la clave de registro de redireccionamiento de URL e implementar con la Directiva de grupo](#bkmk-editreg)

-   [Editar el archivo de texto de redirección de la dirección URL y volver a crear el área de trabajo MED-V](#bkmk-edittext)

<a href="" id="bkmk-editreg"></a>**Para actualizar la información de redireccionamiento de URL mediante Directiva de grupo**

1.  Edite el valor de cadena múltiple de clave del registro que tiene el nombre `RedirectUrls` . Este valor suele encontrarse en:

    Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

    Si va a agregar direcciones URL a la clave del registro, escríbala una por línea, tal y como se necesita al crear el paquete de área de trabajo MED-V. Para obtener más información, vea [crear un paquete de área de trabajo de MED-V](create-a-med-v-workspace-package.md).

2.  Implemente la clave del registro actualizada con la Directiva de grupo. Para obtener más información acerca de cómo usar la Directiva de grupo, consulte [instalación de software de directiva de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

**Nota:**  Este método de edición de la información de redireccionamiento de URL es una práctica recomendada de MED-V.

 

<a href="" id="bkmk-edittext"></a>**Para volver a crear el área de trabajo de MED-V con un archivo de texto de dirección URL actualizado**

-   Otra forma de agregar y quitar direcciones URL de la lista de redirección es actualizar el archivo de texto de redireccionamiento de URL y, a continuación, usarlo para crear un nuevo área de trabajo de MED-V. Después, puede volver a implementar el área de trabajo de MED-V como antes, mediante el proceso de implementación estándar, como un sistema ESD.

    **Importante**  No se recomienda este método de edición de la información de redireccionamiento de direcciones URL. Además, siempre que vuelva a implementar el área de trabajo de MED-V en su empresa, la configuración debe volver a ejecutarse y todos los datos guardados en la máquina virtual se perderán.

     

## Temas relacionados


[Cómo comprobar el redireccionamiento de la dirección URL](how-to-test-url-redirection.md)

[Administración de aplicaciones implementadas en áreas de trabajo de MED-V](managing-applications-deployed-to-med-v-workspaces.md)

[Crear un paquete de área de trabajo de MED-V](create-a-med-v-workspace-package.md)

 

 





