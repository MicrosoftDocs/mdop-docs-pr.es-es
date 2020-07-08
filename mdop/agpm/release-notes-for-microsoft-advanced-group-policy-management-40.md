---
title: Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0
description: Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0
author: dansimp
ms.assetid: 44c19e61-c8e8-48aa-a2c2-20396d14d5bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c4a279893d4da4121e422af99e7c1708a0126b4e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820391"
---
# Notas de la versión de Administración avanzada de directivas de grupo de Microsoft 4.0


Octubre de 2009

## Acerca de administración avanzada de directivas de grupo 4,0 de Microsoft


Administración avanzada de directivas de grupo (AGPM) de Microsoft 4,0 extiende las capacidades de la consola de administración de directivas de grupo (GPMC). AGPM proporciona control de cambios completo y administración mejorada de objetos de directiva de grupo (GPO).

Los siguientes documentos pueden ayudarle a empezar a usar AGPM 4,0.

-   Para obtener información general sobre las capacidades de AGPM, vea [información general sobre la administración avanzada de directivas de grupo](https://go.microsoft.com/fwlink/?LinkID=162671) ( https://go.microsoft.com/fwlink/?LinkID=162671) .

-   Para obtener información sobre cómo AGPM 4,0 difiere de AGPM 3,0, consulte [novedades de agpm 4,0](https://go.microsoft.com/fwlink/?LinkId=160058) ( https://go.microsoft.com/fwlink/?LinkId=160058) .

-   Para obtener instrucciones sobre cómo determinar si AGPM 4,0, AGPM 3,0 o AGPM 2,5 es adecuada para su entorno, consulte [elegir la versión de AGPM que se instalará](https://go.microsoft.com/fwlink/?LinkId=145981) ( https://go.microsoft.com/fwlink/?LinkId=145981) .

-   Para obtener instrucciones básicas sobre cómo instalar AGPM y un escenario de ejemplo para el uso de AGPM, consulte [la guía paso a paso para la administración avanzada de directivas de grupo de Microsoft 4,0](https://go.microsoft.com/fwlink/?LinkID=153505) ( https://go.microsoft.com/fwlink/?LinkID=153505) . Esta guía está diseñada principalmente para ayudar a evaluadores y usuarios de primera vez.

-   Para obtener información sobre cómo actualizar una versión anterior de AGPM o instrucciones detalladas sobre cómo planear la implementación de AGPM en su organización, consulte la [Guía de planeación de administración avanzada de directivas de grupo de Microsoft 4,0](https://go.microsoft.com/fwlink/?LinkID=156883) ( https://go.microsoft.com/fwlink/?LinkID=156883) .

-   Para obtener información sobre cómo usar AGPM para realizar tareas específicas, consulte la ayuda de 4,0 administración de directivas de grupo avanzada, que también está disponible en TechNet como la [Guía de operaciones de AGPM 4,0](https://go.microsoft.com/fwlink/?LinkId=159872) ( https://go.microsoft.com/fwlink/?LinkId=159872) .

## Más información


Para obtener más información acerca de AGPM, consulte lo siguiente:

-   [Administración avanzada de directivas de grupo de TechNet](https://go.microsoft.com/fwlink/?LinkID=146846) (https://go.microsoft.com/fwlink/?LinkID=146846)

-   [TechCenter de Microsoft Desktop Optimization Pack](https://go.microsoft.com/fwlink/?LinkId=159870) (https://www.microsoft.com/technet/mdop)

-   [TechCenter de directiva de grupo](https://go.microsoft.com/fwlink/?LinkId=145531) (https://www.microsoft.com/gp)

## Comentarios


Puede publicar comentarios o preguntas sobre AGPM en el [Foro de directivas de grupo](https://go.microsoft.com/fwlink/?LinkId=145532) ( https://go.microsoft.com/fwlink/?LinkId=145532) .

## Problemas conocidos con AGPM 4,0


### El comando importar desde producción no importa la configuración a un GPO que está desprotegido

Si edita un GPO en el entorno de producción, debe importar el GPO desde la producción para actualizar el GPO en el archivo sin conexión. El comando **Importar desde producción** le permite realizar una copia de seguridad de producción final antes de finalizar la edición para que pueda volver a la copia de seguridad de producción si es necesario.

Si el GPO se ha desprotegido al ejecutar el comando **Importar desde producción** , los cambios de producción no se incorporan en la versión desprotegida del GPO. Sin embargo, la versión importada del GPO se agrega al historial del GPO aunque esa versión no esté disponible para su edición. Cuando se protege el GPO, esa versión reemplaza la versión importada en el archivo, pero ambas están disponibles en el historial del GPO.

**Solución alternativa:** Asegúrese de que el GPO está protegido antes de importarlo de la producción. Si el GPO no se protegió antes de importarlo, puede usar el comando **Deshacer desprotección** para descartar los cambios y volver a la versión del objeto de directiva de grupo importado desde producción.

### Los GPO desprotegidos no se pueden editar durante varios minutos en un entorno que usa una topología de Active Directory de sitio múltiple

AGPM usa un modelo cliente/servidor. El servidor AGPM y el cliente AGPM determinan su propio controlador de dominio más cercano para las operaciones de la Directiva de grupo. Cuando se desprotege un GPO mediante un cliente de AGPM, en realidad es el servidor de AGPM que comprueba el GPO del archivo sin conexión en una carpeta temporal de la carpeta SYSVOL.

Si el servidor AGPM y el cliente de AGPM se encuentran en sitios diferentes, es posible que el GPO temporal desprotegido no esté presente en el controlador de dominio del sitio local durante varios minutos o hasta 30 minutos debido a la latencia de replicación de SYSVOL. En esta situación, no puede editar el GPO desprotegido mediante la GPMC en un cliente de AGPM hasta que se haya replicado SYSVOL del GPO desprotegido.

**Solución alternativa:** Como práctica recomendada, debe colocar los clientes de AGPM en el mismo sitio que el servidor de AGPM al que se conectan para que no tenga que esperar a que se produzca la replicación de SYSVOL para poder editar un GPO desprotegido.

### AGPM no puede leer el límite de la copia de seguridad si su cuenta no tiene permisos para el archivo

En un cliente de AGPM, si inicia sesión con una cuenta a la que no se le han delegado permisos en el archivo de AGPM, inicie la consola de administración de directivas de grupo (GPMC) y, a continuación, haga clic en **Cambiar control**, recibirá el siguiente error.

``` syntax
Failed to read backup purge limit for this domain. 

The following error occurred: 
You do not have sufficient permissions to perform this operation. 
Microsoft.Agpm.AccessDeniedException (80070005)
```

**Solución alternativa:** Póngase en contacto con un administrador de AGPM (control total) y solicite que deleguen el acceso a AGPM para su cuenta. Si es administrador de AGPM, inicie sesión con una cuenta a la que se haya asignado el rol de administrador de AGPM para que pueda delegar el acceso para la cuenta adicional. Para obtener más información, vea "delegar el acceso a nivel de dominio para el archivo" en la ayuda de AGPM.

## Información de copyright de notas de versión


La información de este documento, incluidas las direcciones URL y otras referencias a sitios web de Internet, está sujeta a cambios sin previo aviso y se proporciona solo a modo informativo. El usuario asume todo riesgo de uso o resultados del uso de este documento, y Microsoft Corporation no otorga garantías expresas ni implícitas. Las compañías, las organizaciones, los productos, las personas y los acontecimientos de ejemplo aquí descritos son ficticios. No se pretende indicar ni debe deducirse ninguna asociación con empresas, organizaciones, productos, personas o eventos reales. El cumplimiento de todas las leyes de propiedad intelectual vigentes es responsabilidad del usuario. Sin limitación de los derechos de propiedad intelectual, ninguna parte de este documento puede ser reproducida, almacenada o introducida en un sistema de recuperación, o transmitida de ninguna forma ni por ningún medio (electrónico, mecánico, Fotocopiado, grabación o de cualquier otro modo), ni con ningún propósito, sin la autorización expresa y por escrito de Microsoft Corporation.

Microsoft puede tener patentes, solicitudes de patentes, marcas comerciales, derechos de propiedad intelectual u otros derechos de propiedad intelectual sobre los contenidos de este documento. A excepción de lo estipulado expresamente en un contrato de licencia por escrito de Microsoft, el suministro de este documento no le otorga ninguna licencia para estas patentes, marcas comerciales, derechos de propiedad intelectual u otros derechos de propiedad intelectual.



Microsoft, MS-DOS, Windows, WindowsServer y Windows Vista son marcas comerciales registradas o marcas comerciales de MicrosoftCorporation en los Estados Unidos y/o en otros países.

Los nombres de las compañías y productos reales mencionados en el presente pueden ser marcas comerciales de sus respectivos propietarios.

 

 





