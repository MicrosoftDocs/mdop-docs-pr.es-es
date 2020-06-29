---
title: Diseñar la infraestructura de servidor MED-V
description: Diseñar la infraestructura de servidor MED-V
author: dansimp
ms.assetid: 2781040f-880e-4e16-945d-a38c0adb4151
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4ba4c38328c5484b7daa292f9fc33a4e59824327
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824181"
---
# Diseñar la infraestructura de servidor MED-V


En este tema, diseñará la infraestructura de servidor para cada instancia de MED-V. Esto incluye determinar si la instancia de SQL Server existirá en el servidor MED-V o en un servidor remoto, así como el tamaño de la base de datos de SQL Server. También determinará la ubicación de la consola de administración.

## Diseñar y colocar el servidor para cada instancia de MED-V


El servidor MED-V implementa las directivas y almacena los datos de estado y del historial de sus clientes.

### Factor de forma

MED-V recomienda usar un servidor de CPU de doble núcleo de 2,8 GHz con 2 GB de RAM. Esta recomendación se basa en la hipótesis de que el servidor MED-V se ejecutará en un equipo dedicado y que SQL Server y la consola de administración de MED-V se ejecutarán en máquinas independientes.

Dada esta carga de trabajo, el servidor MED-V debe estar relativamente cargado. En ausencia de instrucciones arquitectónicas específicas en el factor de forma de servidor, diseñe el servidor con la recomendación MED-V, con memoria que coincida con el factor de forma estándar de la organización. El servidor MED-V se puede ejecutar en una máquina virtual (VM) en Windows Server2008 Hyper-V. Si se va a usar una VM, asegúrese de que tiene acceso a los recursos de CPU y de memoria equivalentes a los especificados para un equipo físico.

La capacidad de disco que requiere MED-V Server debe ser suficiente para almacenar los archivos de configuración del área de trabajo de MED-V. Un área de trabajo de MED-V solo puede usar una VM y una directiva para uno o más usuarios. Por lo tanto, el número de áreas de trabajo de MED-V que deben almacenarse depende del grado en que se requieran las distintas directivas para los distintos usuarios de la misma VM, así como del número de VMs que se usarán. Los archivos XML del área de trabajo de MED-V son de 30KB tamaño para un área de trabajo de MED-V típica. Para determinar la capacidad de disco requerida, multiplique 30 KB por el número de áreas de trabajo de MED-V que almacenará el servidor de MED-V.

Las conexiones de red más importantes del servidor MED-V son los vínculos a sus clientes, por lo tanto, coloque el servidor en una ubicación de red que proporcione la mayor cantidad de ancho de banda disponible y los vínculos más eficaces a sus clientes.

### Tolerancia a errores

Solo puede haber un servidor MED-V activo en una instancia de MED-V y MED-V no incluye capacidades estándar para colocar el servidor en un clúster de Microsoft Cluster Server (MSCS) para proporcionar tolerancia a errores. Un servidor de copia de seguridad pasivo se puede configurar manualmente.

Para decidir si un servidor de copia de seguridad pasivo debe configurarse manualmente para la instancia de MED-V, determine si los usuarios podrán usar las imágenes de MED-V en el modo sin conexión. Para obtener información sobre el modo sin conexión, consulte [Cómo configurar un usuario o grupo de dominio](how-to-configure-a-domain-user-or-groupmedvv2.md). Si los usuarios no pueden trabajar sin conexión, no podrán continuar trabajando en el caso de un error de servidor MED-V, incluso si ya se ha iniciado el área de trabajo de MED-V en el cliente. Si se permite el trabajo sin conexión, para cada área de trabajo de MED-V, determine cuánto tiempo el cliente puede trabajar sin conexión antes de que se autentique. Esta es la cantidad máxima de tiempo que el servidor puede no estar disponible.

## Diseñar y colocar la base de datos de SQL Server


El servidor MED-V usa la base de datos de SQL Server para almacenar los eventos y el estado de los clientes. Puede instalar la base de datos de SQL Server en el mismo equipo que el servidor MED-V o puede colocarla en un servidor independiente que ejecute SQL Server, que opcionalmente puede ser remoto. Puede compartir la base de datos con otras instancias de MED-V, en cuyo caso los eventos y las alertas de esas instancias se almacenarán en la misma base de datos, y los informes incluirán eventos de todas las instancias. Puede instalar la base de datos en una instancia de SQL Server existente, y las bases de datos de otros servidores de MED-V pueden residir en la misma instancia.

Si coloca el servidor de base de datos en una ubicación remota desde el servidor MED-V, en los vínculos de redes que no tienen suficiente ancho de banda disponible, los informes pueden tardar en cargarse en la consola y es posible que no se muestren los datos más recientes de los clientes. Consulte las expectativas de nivel de servicio de la organización que determinó en [defina el ámbito del proyecto](define-the-project-scope.md) y use esta información para decidir dónde ubicar la base de datos de SQL Server.

### Factor de forma

Si va a ejecutar SQL Server en el mismo servidor que MED-V y solo se usará SQL Server para almacenar los datos de ese servidor, empiece con la recomendación MED-V y agregue recursos para la carga de SQL Server. Si SQL Server va a almacenar eventos y alertas de más de una instancia de MED-V, para obtener información sobre cómo escalar el factor de forma del servidor, consulte la guía de [planeación y diseño de la infraestructura de Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) (http://go.Microsoft.com/fwlink/?LinkId=163302).

El tamaño de la base de datos dependerá del número de eventos de cliente que almacene la base de datos. Los eventos se crean mediante el funcionamiento normal del cliente, como cuando se inicia un área de trabajo de MED-V o cuando se produce un error en el área de trabajo de MED-V. El intervalo predeterminado en el que el cliente envía eventos es de 1 minuto.

Para calcular el tamaño de la base de datos, determine lo siguiente:

-   Número de clientes en la instancia de MED-V. El máximo es 5.000.

-   Tasa típica de llegada de eventos. Esta tarifa depende del comportamiento de uso del cliente, pero es de aproximadamente de 15 a 20 eventos por día por cliente.

-   Tamaño del evento. Normalmente, el tamaño es de unos 200 bytes.

-   Cantidad de almacenamiento. Número de días que se almacenarán los eventos.

Multiplique estos valores para calcular el tamaño del almacenamiento de datos requerido en bytes y, a continuación, agregue un factor de seguridad para las siguientes cuentas:

-   Errores, que podrían crear un gran número de eventos desde un cliente en un breve período de tiempo.

-   Tabla de base de datos y espacio organizativo.

Para aproximar el requisito de optimización de la infraestructura por segundo (IOPs), use los valores anteriores, multiplicando la tasa de llegada de eventos típica por el número de clientes de la instancia. Esto da como resultado el número de registros que se pueden escribir por día. Divida ese número por 86.400 para obtener el número de registros escritos por segundo. Si una operación de escritura se puede equiparar con una única operación de optimización de infraestructura (IO), este número es la IOPs de escritura obligatoria. Agregue un búfer para la actividad de informes. Esto es difícil de determinar pero depende de la cantidad de consolas que se usan con la instancia y de la frecuencia con la que se usan para generar informes.

### Tolerancia a errores

Cuando el cliente de MED-V se esté ejecutando, si el servidor no está disponible, se hará una copia de seguridad de los eventos en el cliente y los informes no estarán disponibles en la consola de administración. Consulte las expectativas de nivel de servicio de la organización determinadas en [definir el ámbito del proyecto](define-the-project-scope.md) para decidir si es necesario el diseño de una infraestructura SQL Server tolerante a errores.

MED-V no ofrece compatibilidad para ejecutar SQL Server en un clúster de MSCS. Para poder poner en espera activa y evitar la pérdida de datos en caso de que se produzca un error, puede colocar SQL Server en una configuración de trasvase de registros. Para obtener información sobre el trasvase de registros, consulte la guía de [planeación y diseño de la infraestructura de Microsoft SQL Server 2008](https://go.microsoft.com/fwlink/?LinkId=163302) ( https://go.microsoft.com/fwlink/?LinkId=163302) .

## Diseñar la consola de administración


Parte de la funcionalidad de la consola de administración MED-V es probar las máquinas virtuales antes de que se embalen para distribuirlas a clientes de MED-V. Por lo tanto, la consola de administración debe diseñarse con un factor de forma similar a la de un equipo cliente de MED-V típico.

La consola de administración se instala junto con el cliente de MED-V y usa Microsoft Virtual PC2007 SP1 con la revisión que se describe en el artículo 974918 de Microsoft Knowledge base. Debe utilizarse un sistema operativo de cliente; la consola de administración de MED-V no se puede ejecutar en el mismo sistema que el servidor MED-V.

No puede compartir una consola de administración con varias instancias de servidor MED-V. La dirección del servidor de MED-V se especifica durante la instalación del cliente de MED-V de la consola de administración. Esto se puede cambiar después de la instalación, pero en cualquier momento la consola de administración solo puede funcionar con un solo servidor de MED-V.

Puede usar varias consolas de administración con un solo servidor de MED-V. Para evitar conflictos, está disponible un mecanismo que notifica a otros usuarios de la consola cuando una consola ha realizado cambios en un área de trabajo de MED-V.

Para cada instancia de MED-V, Determine cuántas consolas de administración serán necesarias y dónde se colocarán. Seleccione un factor de forma de cliente de MED-V típico para usar en la consola de administración.

## Temas relacionados


[Configuraciones admitidas de MED-V 1.0 SP1](med-v-10-sp1-supported-configurationsmedv-10-sp1.md)

[Configuración del servidor de MED-V para el modo de clúster](configuring-med-v-server-for-cluster-mode.md)

[Cómo instalar el cliente MED-V y la consola de administración de MED-V](how-to-install-med-v-client-and-med-v-management-console.md)

[Uso de la interfaz de usuario de la consola de administración de MED-V](using-the-med-v-management-console-user-interface.md)

 

 





