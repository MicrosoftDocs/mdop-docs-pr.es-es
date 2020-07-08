---
title: Acerca de los aceleradores de paquetes de App-V (App-V 4.6 SP1)
description: Acerca de los aceleradores de paquetes de App-V (App-V 4.6 SP1)
author: manikadhiman
ms.assetid: fc2d2375-8f17-4a6d-b374-771cb947cb8c
ms.reviewer: ''
manager: dansimp
ms.author: v-madhi
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cb7b8e6fa9482838283257843caf4b291c03bf2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820091"
---
# Acerca de los aceleradores de paquetes de App-V (App-V 4.6 SP1)


Puede usar los aceleradores de paquetes de App-V para secuenciar aplicaciones grandes y complejas automáticamente. Además, cuando aplica un acelerador de paquetes de App-V, no siempre es necesario instalar manualmente una aplicación para crear el paquete de aplicación virtual.

**Nota:**  En algunos casos, se le solicitará que instale una aplicación de forma local en el equipo que ejecuta el secuenciador de App-V antes de que pueda usar el acelerador de paquetes. Si necesita instalar una aplicación, debe instalar la aplicación en la ubicación predeterminada de la aplicación. El secuenciador de App-V no supervisa esta instalación. Cuando se crea el acelerador de paquetes de App-V, el autor del acelerador de paquetes determina si se necesita instalar una aplicación de forma local.

 

El secuenciador de App-V extrae los archivos necesarios del acelerador de paquetes de App-V y los medios de instalación asociados para crear un paquete virtual sin tener que supervisar la instalación de la aplicación.

**Importante**  Renuncia de responsabilidad: Microsoft Application Virtualization Sequencer no le otorga derechos de licencia a la aplicación de software que está usando para crear un acelerador de paquetes. Debe cumplir todos los términos de licencia de usuario final para dicha aplicación. Es responsabilidad suya asegurarse de que los términos de licencia de la aplicación de software le permitan crear un acelerador de paquetes con Application Virtualization Sequencer.

 

Los aceleradores de paquetes y las plantillas de proyecto de App-V difieren entre sí. Los aceleradores de paquetes son específicos de la aplicación. Las plantillas de proyecto permiten a los usuarios guardar las opciones de configuración más comunes específicas de una organización y aplicarlas a varias aplicaciones. También puede crear plantillas de proyecto en el símbolo del sistema, mientras que, en cambio, debe usar la consola del secuenciador de App-V para crear aceleradores de paquetes. Además, no se admite la creación de un paquete mediante un acelerador de paquetes ni la aplicación de una plantilla de proyecto.

## Compartir aceleradores de paquetes de App-V


En esta sección se proporciona información de procedimientos recomendados sobre cómo compartir aceleradores de paquetes. Si planea compartir aceleradores de paquetes, la información, como los nombres de los equipos, la información de la cuenta de usuario y la información sobre las aplicaciones asociadas, puede estar incluida en los aceleradores de paquetes. en la siguiente lista se describen los métodos que debe tener en cuenta al crear aceleradores de paquetes:

-   **Nombre de usuario**. Cuando inicia sesión en el equipo que ejecuta el secuenciador de App-V, debe usar una cuenta de usuario genérica, como la cuenta de **Administrador** integrada para administrar el equipo o el dominio. No debe usar una cuenta basada en un nombre de usuario existente.

-   **Nombre del equipo**. Especifique un nombre general, no Identificativo, para el equipo que ejecuta el secuenciador.

-   **Dirección URL del servidor**. En la consola SPRJ, en la pestaña **implementación** , use la configuración predeterminada para la información de configuración de la dirección URL del servidor.

-   **Las aplicaciones**. Si no desea compartir la lista de aplicaciones que se instalaron en el equipo que ejecuta el secuenciador cuando creó el acelerador de paquetes, debe eliminar el archivo de **appv\_manifest.xml** . Este archivo se encuentra en el directorio raíz del paquete de la aplicación virtual.

También debe revisar cualquier configuración o archivos de configuración asociados con el paquete de aplicación virtual para asegurarse de que las aplicaciones no contienen información personal.

## Proteger los aceleradores de paquetes de App-V


Guarda siempre los aceleradores de paquetes de App-V y cualquier medio de instalación asociado en una ubicación segura de la red para proteger los aceleradores de paquetes de App-V y los archivos de instalación para que no se manipulen o dañen. Dado que los aceleradores de paquetes también pueden contener contraseña e información específica del usuario, debe guardar los aceleradores de paquetes de App-V en una ubicación segura y debe firmar digitalmente el acelerador de paquetes después de crearlo para que se pueda comprobar el editor cuando se aplique el acelerador de paquetes. Para obtener más información sobre las firmas digitales, consulte [directrices de la aplicación de las prácticas de firma digital para la seguridad de criterios comunes](https://go.microsoft.com/fwlink/?LinkId=204705) ( https://go.microsoft.com/fwlink/?LinkId=204705) .

## Temas relacionados


[Cómo crear aceleradores de paquetes de App-V (App-V 4.6 SP1)](how-to-create-app-v-package-accelerators--app-v-46-sp1-.md)

[Cómo aplicar un acelerador de paquetes para crear un paquete de aplicaciones virtual (App-V 4,6 SP1)](how-to-apply-a-package-accelerator-to-create-a-virtual-application-package---app-v-46-sp1-.md)

 

 





