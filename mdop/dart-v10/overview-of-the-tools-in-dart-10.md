---
title: Introducción a las herramientas de DaRT 10
description: Introducción a las herramientas de DaRT 10
author: dansimp
ms.assetid: 752467dd-b646-4335-82ce-9090d4651f65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8bef2b92e998bebffae526d4288c76be081fe0a9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822991"
---
# Introducción a las herramientas de DaRT 10


Desde la ventana conjunto de herramientas de diagnóstico **y recuperación** de Microsoft Diagnostics and Recovery Toolset (DART) 10, puede iniciar cualquiera de las herramientas individuales que incluye al crear la imagen de recuperación de DART 10. Para obtener información sobre cómo obtener acceso a la ventana **conjunto de herramientas de diagnóstico y recuperación** , consulte [Cómo recuperar equipos locales con la imagen de recuperación de DART](how-to-recover-local-computers-by-using-the-dart-recovery-image-dart-10.md).

Si está disponible, puede usar el Asistente para **soluciones** en la ventana **conjunto de herramientas de diagnóstico y recuperación** para seleccionar la herramienta que se adapte mejor a su problema particular, en función de una breve entrevista que proporciona el asistente.

## Explorar las herramientas de DaRT


A continuación, se ofrece una descripción de las herramientas de DaRT 10.

### Administración de equipos

**Administración de equipos** es un conjunto de herramientas administrativas de Windows que le ayudan a solucionar problemas de equipos. Puede usar las herramientas de **Administración de equipos** de DART para ver la información del sistema y los registros de eventos, administrar discos, Mostrar Autoruns y administrar servicios y drivers. La consola de **Administración de equipos** está personalizada para ayudarle a diagnosticar y reparar problemas que podrían impedir el inicio del sistema operativo Windows.

**Nota:**  No se admite la recuperación de discos dinámicos con DaRT.

 

### Analizador de bloqueo

Use el **Asistente** de análisis de bloqueo para determinar rápidamente la causa de un error en el equipo analizando el archivo de volcado de memoria en el sistema operativo Windows que está reparando. **Crash Analyzer** examina el archivo de volcado de memoria del controlador que causó el error de un equipo. Después, puede deshabilitar el controlador de dispositivo con el problema mediante el nodo **servicios y controladores** de la herramienta **Administración de equipos** .

El **Asistente del analizador de bloqueo** requiere las herramientas de depuración para Windows y los archivos de símbolos para el sistema operativo que está reparando. Puede incluir ambos requisitos al crear la imagen de recuperación de DaRT. Si no se incluyen en la imagen de recuperación y no tiene acceso a ellos en el equipo que está reparando, puede copiar el archivo de volcado de memoria en otro equipo y usar la versión independiente del **analizador de bloqueo** para diagnosticar el problema.

Ejecutar **Crash Analyzer** es una buena idea incluso si tiene previsto rehacer la imagen del equipo. La imagen podría tener un controlador defectuoso que está causando problemas en su entorno. Al ejecutar el **analizador de bloqueo**, puede identificar los problemas y mejorar la estabilidad de la imagen.

Para obtener más información acerca del **analizador de bloqueo**, consulte [diagnosticar errores del sistema con el analizador de bloqueos](diagnosing-system-failures-with-crash-analyzer-dart-10.md).

### Disk Commander

**Disk Commander** le permite recuperar y reparar particiones o volúmenes de disco mediante uno de los siguientes procesos de recuperación:

-   Restaurar el registro de inicio maestro (MBR)

-   Recuperar uno o más volúmenes perdidos

-   Restaurar tablas de particiones de copia de seguridad de **Disk Commander**

-   Guardar tablas de particiones en backup de **Disk Commander**

**ADVERTENCIA**  Le recomendamos que haga una copia de seguridad de un disco antes de usar **Disk Commander** para repararlo. Con **Disk Commander**, puede dañar los volúmenes y hacerlos inaccesibles. Además, los cambios en un volumen pueden afectar a otros volúmenes porque los volúmenes de un disco comparten una tabla de particiones.

 

**Nota:**  No se admite la recuperación de discos dinámicos con DaRT.

 

### Borrado de disco

Puede usar el **borrado de disco** para eliminar todos los datos de un disco o un volumen, incluso los datos que quedan después de cambiar el formato de una unidad de disco duro. El **borrado de disco** le permite seleccionar de una sobrescritura de paso único o de una sobrescritura de cuatro pases, que cumple con los estándares actuales del Departamento de defensa de los Estados Unidos.

**ADVERTENCIA**  Después de borrar un disco o un volumen, no puede recuperar los datos. Compruebe el tamaño y la etiqueta de un volumen antes de borrarlo.

 

### Internet

La herramienta **Explorador** le permite examinar el sistema de archivos del equipo y los recursos compartidos de red para que pueda quitar los datos importantes que el usuario haya almacenado en la unidad local antes de intentar reparar o rehacer la imagen del equipo. Y como puede asignar Letras de unidad a recursos compartidos de red, puede copiar y mover fácilmente los archivos del equipo a la red para guardarlos o de la red al equipo para restaurarlos.

### Restauración de archivos

La **restauración de archivos** le permite intentar restaurar los archivos que se han eliminado por error o que son demasiado grandes para la papelera de reciclaje. La **restauración de archivos** no se limita a los volúmenes de disco normales, pero puede buscar y restaurar archivos en volúmenes perdidos o en volúmenes cifrados con BitLocker.

**Nota:**  No se admite la recuperación de discos dinámicos con DaRT.

 

### Búsqueda de archivos

Antes de volver a crear imágenes en un equipo, es importante recuperar los archivos del disco duro local, especialmente cuando es posible que el usuario no haya realizado una copia de seguridad ni guardado los archivos en otra ubicación.

La herramienta de **búsqueda** abre una ventana de **búsqueda de archivos** que puede usar para buscar documentos cuando no conoce la ruta de acceso del archivo o para buscar tipos generales de archivos en todos los discos duros locales. Puede buscar patrones de nombres de archivo específicos en rutas de archivo específicas. También puede limitar los resultados a un intervalo de fechas o a un intervalo de tamaño.

### Desinstalación de Hotfix

El **Asistente para desinstalación de revisiones** le permite quitar revisiones o Service Packs del sistema operativo Windows en el equipo que está reparando. Use esta herramienta cuando se sospeche que un hotfix o un Service Pack impide que el sistema operativo se inicie.

Le recomendamos que desinstale solo una revisión a la vez, aunque la herramienta le permita desinstalar más de una.

**Importante**  Es posible que los programas que se instalaron o actualizaron después de instalar una revisión no funcionen correctamente después de desinstalar una revisión.

 

### Locksmith

El **Asistente para locksmith** le permite establecer o cambiar la contraseña de cualquier cuenta local en el sistema operativo Windows que esté analizando o reparando. No es necesario que conozcas la contraseña actual. Sin embargo, la contraseña que establezca debe cumplir con todos los requisitos definidos por un objeto de directiva de grupo local. Esto incluye la longitud y la complejidad de la contraseña.

Puede usar **locksmith** cuando se desconoce la contraseña de una cuenta local, como la cuenta de administrador local. No puede usar **locksmith** para establecer contraseñas para cuentas de dominio.

### Editor del registro

Puede usar el **Editor del registro** para obtener acceso y cambiar el registro del sistema operativo Windows que está analizando o reparando. Esto incluye agregar, quitar y modificar claves y valores, e importar archivos de registro (. reg).

**ADVERTENCIA**  Pueden surgir problemas graves si cambia incorrectamente el registro con el **Editor del registro**. Estos problemas pueden requerir que haya que volver a instalar el sistema operativo. Antes de realizar cambios en el registro, debe hacer una copia de seguridad de los datos valiosos del equipo. Cambie el registro bajo su propia responsabilidad.

 

### Examen de SFC

La herramienta de **análisis SFC** inicia el **Asistente para la reparación de archivos de sistema** y le permite reparar archivos de sistema que impiden que se inicie el sistema operativo Windows instalado. El **Asistente de reparación de archivos del sistema** puede reparar automáticamente los archivos del sistema dañados o que no se encuentran, o bien puede preguntarle antes de realizar cualquier reparación.

### Asistente para soluciones

El **Asistente para soluciones** presenta una serie de preguntas y, a continuación, recomienda la mejor herramienta para la situación, en función de las respuestas. Este asistente le ayuda a determinar qué herramienta usar cuando no está familiarizado con las herramientas de DaRT.

### Configuración de TCP/IP

Cuando arranca un equipo problemático en DaRT, se configura para obtener automáticamente su configuración TCP/IP (dirección IP y servidor DNS) del Protocolo de configuración dinámica de host (DHCP). Si DHCP no está disponible, puede configurar manualmente TCP/IP con la herramienta de **configuración de TCP/IP** . En primer lugar, seleccione un adaptador de red y, a continuación, configure la dirección IP y el servidor DNS para ese adaptador.

## Temas relacionados


[Tareas iniciales con DaRT 10](getting-started-with-dart-10.md)

 

 





