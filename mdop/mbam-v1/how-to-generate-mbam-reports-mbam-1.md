---
title: Cómo generar informes MBAM.
description: Cómo generar informes MBAM.
author: dansimp
ms.assetid: cdf4ae76-040c-447c-8736-c9e57068d221
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f0b5a4e984d7a609eab7204e67f46042992f586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824530"
---
# Cómo generar informes MBAM.


Administración y supervisión de Microsoft BitLocker (MBAM) genera varios informes para supervisar el uso del cifrado de BitLocker y el cumplimiento. En este tema se describe cómo abrir el sitio web de administración de MBAM y cómo generar informes de MBAM sobre cumplimiento de normas para empresas, equipos individuales, compatibilidad de hardware y actividad de recuperación de claves. Para obtener más información sobre los informes de MBAM, vea Descripción de los [informes de MBAM](understanding-mbam-reports-mbam-1.md).

**Nota:**  Para ejecutar los informes, debe ser miembro de la función de **usuarios de informes** en los equipos en los que haya instalado las características del servidor de administración y supervisión, la base de datos de cumplimiento y la auditoría, y los informes de auditoría y cumplimiento.

 

**Para abrir el sitio web de administración de MBAM**

1.  Abra un explorador Web y vaya al sitio web de MBAM. La dirección URL predeterminada del sitio Web *es &lt; http:// &gt; NombreDeEquipo* del servidor de supervisión y administración de Microsoft BitLocker.

    **Nota:**  Si el sitio web de MBAMadministration se instaló en un puerto que no es 80, debe especificar ese número de puerto en la dirección URL. Por ejemplo, *http:// &lt; nombreEquipo &gt; : &lt; Port &gt; *. Si especificó un nombre de host para el sitio web de MBAMadministration durante la instalación, la dirección URL sería *http:// &lt; hostname &gt; *.

     

2.  En el panel de navegación, haga clic en **informes**. En el panel principal, haga clic en la pestaña de su tipo de informe: **Informe de cumplimiento**de la empresa, informe de **cumplimiento de equipos**, informe de auditoría de **hardware**o informe de **Auditoría de recuperación**.

    **Nota:**  Los datos históricos de los clientes de MBAM se conservan en la base de datos de cumplimiento. Es posible que se necesiten datos retenidos en caso de pérdida o robo de un equipo. Cuando se ejecutan informes empresariales, debe usar fechas de inicio y finalización apropiadas para el ámbito de los intervalos de tiempo para los informes de una a dos semanas, con el fin de aumentar la precisión de los datos de informes.

     

**Para generar un informe de compatibilidad empresarial**

1.  En el sitio web de MBAMadministration, haga clic en **informes** en el panel de navegación y, a continuación, haga clic en la pestaña **Informe de cumplimiento corporativo** y seleccione los filtros adecuados para el informe. Para el informe de cumplimiento de la empresa, puede configurar los siguientes filtros.

    -   **Estado de cumplimiento**. Use este filtro para especificar los tipos de estado de cumplimiento (por ejemplo, conformes o no conformes) para incluirlos en el informe.

    -   **Estado de error**. Use este filtro para especificar los tipos de estado de error, como sin error o error, para incluirlos en el informe.

2.  Haga clic en **Ver informe** para mostrar el informe especificado.

    Los resultados del informe se pueden guardar en cualquiera de los formatos de archivo disponibles, como HTML, Microsoft Word y Microsoft Excel.

    **Nota:**  El informe de cumplimiento de la empresa se genera a partir de un trabajo de SQL que se ejecuta cada seis horas. Por lo tanto, la primera vez que intente ver el informe, puede encontrarse con algunos datos que faltan.

     

3.  Para ver la información de un equipo en el informe cumplimiento de equipos, seleccione el nombre del equipo.

4.  Seleccione el signo más (+) situado junto al nombre del equipo para ver información sobre los volúmenes del equipo.

**Para generar el informe de cumplimiento de equipos**

1.  En el sitio web de MBAMadministration, seleccione el nodo de **Informe** en el panel de navegación y, a continuación, seleccione el **Informe de cumplimiento de equipos**. Use el informe de cumplimiento de equipos para buscar el **nombre de usuario** o **el nombre del equipo**.

2.  Haga clic en **Ver informe** para ver el informe del equipo.

    Los resultados se pueden guardar en cualquiera de los formatos de archivo disponibles, como HTML, Microsoft Word y Microsoft Excel.

3.  Para mostrar más información sobre un equipo en el informe cumplimiento de equipos, seleccione el nombre del equipo.

4.  Seleccione el signo más (+) situado junto al nombre del equipo para ver información sobre los volúmenes del equipo.

    **Nota:**  Un equipo cliente de MBAM se considera conforme si el equipo cumple con los requisitos de la configuración de la Directiva MBAM o el modelo de hardware del equipo se establece en incompatible. Por lo tanto, al ver información detallada sobre los volúmenes de disco asociados con el equipo, los equipos que están exentos de cifrado de BitLocker debido a la compatibilidad de hardware se pueden mostrar como compatibles aunque el estado de cifrado del volumen de la unidad se muestre como no conforme.

     

**Para generar el informe de auditoría de compatibilidad de hardware**

1.  En el sitio web de MBAMadministration, seleccione el nodo de **Informe** en el panel de navegación y, a continuación, seleccione el **Informe de auditoría de hardware**. Seleccione los filtros adecuados para su informe de auditoría de hardware. El informe de auditoría de hardware ofrece los siguientes filtros disponibles:

    -   **Usuario (dominio\\usuario)**. Especifica el nombre del usuario que realizó un cambio.

    -   **Cambiar tipo**. Especifica el tipo de cambios que está buscando.

    -   **Fecha de inicio**. Especifica la parte de la fecha de inicio del intervalo de fechas en el que desea informar.

    -   **Fecha de finalización**. Especifica la parte de la fecha de finalización del intervalo de fechas en el que desea informar.

2.  Haga clic en **Ver informe** para ver el informe.

    Los resultados se pueden guardar en varios formatos de archivo disponibles, como HTML, Microsoft Word y Microsoft Excel.

**Para generar el informe de auditoría de clave de recuperación**

1.  En el sitio web de MBAMadministration, seleccione el nodo de **Informe** en el panel de navegación y, a continuación, seleccione el **Informe de auditoría de recuperación**. Seleccione los filtros para el informe de auditoría de clave de recuperación. Los filtros disponibles para auditorías de claves de recuperación son los siguientes:

    -   **Solicitante**. Especifica el nombre de usuario del solicitante. El solicitante es la persona del Departamento de soporte que ha tenido acceso a la clave en nombre de un usuario.

    -   **Solicitante**. Especifica el nombre de usuario del solicitante. El solicitante es la persona que llamó al servicio de asistencia para obtener una clave de recuperación.

    -   **Resultado** de la solicitud Especifica los tipos de resultado de la solicitud, como: correcto o erróneo. Por ejemplo, es posible que desee ver los intentos fallidos de acceso clave.

    -   **Tipo de clave**. Especifica el tipo de clave, como por ejemplo: contraseña de clave de recuperación o hash de contraseña de TPM.

    -   **Fecha de inicio**. Especifica la fecha de inicio del intervalo de fechas.

    -   **Fecha de finalización**. Especifica la parte de la fecha de finalización del intervalo de fechas.

2.  Haga clic en **Ver informe** para mostrar el informe.

    Los resultados se pueden guardar en varios formatos de archivo disponibles, como HTML, Microsoft Word y Microsoft Excel.

## Temas relacionados


[Supervisión e informes de cumplimiento de BitLocker con MBAM 1.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





