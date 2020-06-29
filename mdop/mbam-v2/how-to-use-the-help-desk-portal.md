---
title: Cómo usar el portal del Departamento de soporte técnico
description: Cómo usar el portal del Departamento de soporte técnico
author: dansimp
ms.assetid: c27f7737-10c8-4164-9de8-57987292c89c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8813fbe9a7b6980b656ecc673ac4ed618c4cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826330"
---
# Cómo usar el portal del Departamento de soporte técnico


El sitio web de administración y supervisión de MBAM, también conocido como portal de servicio de asistencia, es una interfaz administrativa para el cifrado de unidad BitLocker que se instala como parte de la infraestructura de servidor de administración y supervisión de Microsoft BitLocker (MBAM). En las siguientes secciones se describe cómo puede usar este sitio web para revisar informes, recuperar unidades de los usuarios finales y administrar los TPMs de los usuarios finales.

## <a href="" id="bkmk-reports"></a>Informes


MBAM recopila información de equipos de Active Directory y clientes, lo que le permite ejecutar diferentes informes para supervisar el uso de BitLocker y el cumplimiento. Con la sección **informes** del sitio web de administración y supervisión, puede generar informes sobre el cumplimiento de la norma empresarial, los equipos individuales y la actividad de recuperación de claves. Para obtener una descripción de cada informe, consulte [Understanding MBAM Reports](understanding-mbam-reports-mbam-2.md).

**Para obtener acceso a los informes**

1.  Abra un explorador Web y vaya al sitio web de administración y supervisión de MBAM.

2.  Seleccione **informes** en el panel de la izquierda.

3.  En la barra de menús superior, seleccione el tipo de informe que desea generar. Para guardar los informes, haga clic en el botón **exportar** en la barra de menús informes.

Para obtener más información sobre cómo ejecutar informes de MBAM, consulte [Cómo generar informes de MBAM](how-to-generate-mbam-reports-mbam-2.md).

## <a href="" id="bkmk-drirec"></a>Recuperación de unidades


La característica **recuperación de unidades** del sitio web de supervisión y administración permite a los usuarios con roles de administrador específicos (por ejemplo, usuarios del servicio de asistencia) obtener acceso a datos de claves de recuperación que ha recopilado el cliente de MBAM. Estos datos se pueden usar para acceder a una unidad protegida con BitLocker cuando BitLocker pasa al modo de recuperación. Para obtener instrucciones sobre cómo recuperar una unidad que esté en modo de recuperación, consulte [Cómo recuperar una unidad en modo de recuperación](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).

También puede recuperar unidades que se hayan movido o que estén dañadas:

-   [Cómo recuperar una unidad que se ha movido](how-to-recover-a-moved-drive-mbam-2.md)

-   [Cómo recuperar una unidad dañada](how-to-recover-a-corrupted-drive-mbam-2.md)

Para obtener más información sobre cómo recuperar una unidad protegida con BitLocker, consulte [realizar la administración de BitLocker con MBAM](performing-bitlocker-management-with-mbam-mbam-2.md).

## <a href="" id="bkmk-manatpm"></a>Administrar TPM


La característica administrar TPM del sitio web administración y supervisión proporciona a los usuarios que tienen determinados roles de administrador (por ejemplo, "usuarios del Departamento de soporte técnico") el acceso a los datos de TPM recopilados por el cliente de MBAM. En un bloqueo de TPM, un administrador puede usar el sitio web de administración y supervisión para recuperar el archivo de contraseñas necesario para desbloquear el TPM. Para obtener instrucciones sobre cómo restablecer un TPM después de un bloqueo de TPM, consulte [cómo restablecer un bloqueo de TPM](how-to-reset-a-tpm-lockout-mbam-2.md).

## <a href="" id="bkmk-helpdesk"></a> Tareas del servicio de asistencia de MBAM


Puede usar el sitio web de administración y supervisión para muchas tareas administrativas, como la administración de hardware protegido por BitLocker, la recuperación de unidades y la ejecución de informes. De forma predeterminada, la dirección URL del sitio web de supervisión y administración es http:// &lt; *MBAMAdministrationServername* &gt; , aunque puede personalizarla durante el proceso de instalación.

**Nota:**  Para acceder a las diversas características que ofrece el sitio web de supervisión y supervisión, debe tener las funciones apropiadas asociadas a su cuenta de usuario. Para obtener más información sobre los roles de usuario, consulte [Cómo administrar los roles de administrador de MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).

 

Use los siguientes vínculos para buscar información sobre las tareas que puede realizar mediante el sitio web de administración y supervisión:

-   [Cómo restablecer un bloqueo de TPM](how-to-reset-a-tpm-lockout-mbam-2.md)

-   [Cómo recuperar una unidad en modo de recuperación](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

-   [Cómo recuperar una unidad que se ha movido](how-to-recover-a-moved-drive-mbam-2.md)

-   [Cómo recuperar una unidad dañada](how-to-recover-a-corrupted-drive-mbam-2.md)

-   [Cómo determinar el estado de cifrado de BitLocker de equipos perdidos](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

 

 





