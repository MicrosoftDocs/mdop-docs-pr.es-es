---
title: Cómo comprobar el redireccionamiento de la dirección URL
description: Cómo comprobar el redireccionamiento de la dirección URL
author: dansimp
ms.assetid: 38d80088-da1d-4098-b27e-76f9e78f81dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d964cf9d0114d3085d7e8952eebc82486b7b76cc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824450"
---
# Cómo comprobar el redireccionamiento de la dirección URL


Después de que finalice la prueba de la primera configuración, puede comprobar que la funcionalidad de redireccionamiento de la dirección URL funciona según lo esperado realizando las siguientes tareas.

**Importante**  El agente de host MED-V debe estar ejecutándose para que el redireccionamiento de direcciones URL funcione correctamente.

<a href="" id="bkmk-urlredir"></a>**Para probar el redireccionamiento de URL**

1.  Abra un explorador Internet Explorer en el equipo host y escriba una dirección URL que especificó para el redireccionamiento.

2.  Compruebe que la página web está abierta en Internet Explorer en la máquina virtual invitada.

3.  Repita este proceso para cada dirección URL que quiera probar.

**Para comprobar que se puede Agregar o quitar una dirección URL**

1.  Agregue o quite una dirección URL del área de trabajo de MED-V.

    Para obtener información sobre cómo agregar y quitar direcciones URL para el redireccionamiento en un área de trabajo de MED-V, consulte [Manage Med-v URL Redirection](manage-med-v-url-redirection.md).

2.  Si ha agregado una dirección URL a la lista de redireccionamiento, repita los pasos de [para probar el redireccionamiento de URL](#bkmk-urlredir) para comprobar que la nueva dirección URL redirige de la forma prevista.

3.  Si ha quitado una dirección URL de la lista de redirección, compruebe que se ha quitado siguiendo estos pasos:

    1.  Abra un explorador Internet Explorer en el equipo host y escriba la dirección URL que quitó de la lista de redireccionamiento.

    2.  Compruebe que la página web se abre en Internet Explorer en el equipo host en lugar de en la máquina virtual invitada.

        **Nota:**  Pueden pasar varios segundos hasta que tengan lugar los cambios en el redireccionamiento de la dirección URL.

**Nota:**  Si encuentra algún problema al comprobar la configuración de redireccionamiento de la dirección URL, consulte [solución de problemas de operaciones](operations-troubleshooting-medv2.md).

Después de completar la comprobación de la redirección de URL en el área de trabajo de MED-V, puede probar otras configuraciones para comprobar que funcionan según lo previsto.

Una vez que haya completado la prueba de su paquete de área de trabajo MED-V y haya comprobado que funciona como se espera, puede implementar el área de trabajo de MED-V en su empresa.

## Temas relacionados

[Cómo probar la publicación de aplicaciones](how-to-test-application-publishing.md)

[Cómo comprobar la configuración de instalación de primera vez](how-to-verify-first-time-setup-settings.md)

[Implementación del paquete del área de trabajo de MED-V](deploying-the-med-v-workspace-package.md)

 

 





