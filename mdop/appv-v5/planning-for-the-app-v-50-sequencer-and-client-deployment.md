---
title: Planificación de la implementación del cliente y del secuenciador de App-V 5.0
description: Planificación de la implementación del cliente y del secuenciador de App-V 5.0
author: dansimp
ms.assetid: 57a604ad-90e1-4d32-86bb-eafff59aa43a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 8c6f7c4d717acad014f079e51a7013a57766d9ca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813463"
---
# Planificación de la implementación del cliente y del secuenciador de App-V 5.0


Antes de empezar a usar Microsoft Application Virtualization (App-V) 5,0, debe instalar el secuenciador de aplicaciones-V 5,0, el cliente de App-V 5,0 y, opcionalmente, el almacén de contenido compartido de App-V 5,0. En las siguientes secciones se trata la planificación de estas instalaciones.

## Planeación de la implementación de App-V 5,0 Sequencer


App-V 5,0 usa un proceso denominado secuenciación para crear aplicaciones virtualizadas y paquetes de aplicaciones. La secuenciación requiere el uso de un equipo que ejecuta el secuenciador de 5,0 de App-V.

**Nota:**  Para obtener información sobre la nueva funcionalidad de App-V 5,0 Sequencer, vea los **cambios en la sección Sequencer de las** novedades [de app-v 5,0](whats-new-in-app-v-50.md).

 

El equipo que ejecuta el secuenciador de App-V 5,0 debe cumplir con los requisitos mínimos del sistema. Para obtener una lista de estos requisitos, consulte [configuraciones admitidas de App-V 5,0](app-v-50-supported-configurations.md).

Idealmente, debe instalar el secuenciador en un equipo que funcione como una máquina virtual. Esto le permite revertir más fácilmente el equipo que ejecuta el secuenciador a un estado "limpio" antes de la secuencia de otra aplicación. Al instalar el secuenciador con una máquina virtual, debe realizar los siguientes pasos:

1.  Instale todos los requisitos previos del secuenciador asociado.

2.  Instale el secuenciador.

3.  Tomar una "instantánea" del entorno.

**Importante**  El equipo de seguridad de la empresa debe revisar y aprobar el plan de proceso de secuencia. Por razones de seguridad, debe mantener las operaciones del secuenciador en un laboratorio independiente del entorno de producción. La disposición de separación puede ser tan simple o completa según sea necesario, en función de los requisitos de la empresa. Los equipos de secuencias deben poder conectarse a la red corporativa para copiar paquetes finalizados en los servidores de producción. Sin embargo, dado que los equipos de secuencias suelen funcionar sin protección antivirus, no deben estar protegidos en la red corporativa. Por ejemplo, es posible que pueda funcionar detrás de un firewall o en un segmento de red aislado. Es posible que también pueda usar máquinas virtuales que estén configuradas para compartir una red virtual aislada. Siga las políticas de seguridad corporativas para resolver estas preocupaciones de manera segura.

 

[Cómo instalar el secuenciador](how-to-install-the-sequencer-beta-gb18030.md)

## Planeación de la implementación de cliente de App-V 5,0


Para ejecutar paquetes virtualizados en equipos de destino, debe instalar el cliente de App-V 5,0 en los equipos de destino. El cliente de App-V 5,0 es el componente que ejecuta una aplicación virtualizada en un equipo de destino. El cliente permite que los usuarios interactúen con iconos y tipos de archivo específicos para iniciar aplicaciones virtualizadas. El cliente también ayuda a obtener contenido de la aplicación desde el servidor de administración y almacena en caché el contenido antes de que el cliente inicie la aplicación. Existen dos tipos de cliente: el cliente para servicios de escritorio remoto, que se usa en los sistemas de servidor de host de sesión de escritorio remoto (host de sesión de escritorio remoto) y en el cliente de App-V 5,0, que se usa para todos los demás equipos.

El cliente de App-V 5,0 debe configurarse con la línea de comandos del instalador o mediante un script de PowerShell una vez completada la instalación.

La configuración debe definirse con cuidado a fin de acelerar la implementación del software de cliente de App-V 5,0. Esto es especialmente importante cuando hay equipos en diferentes oficinas donde los clientes deben configurarse para usar ubicaciones de origen diferentes.

También debe determinar cómo va a implementar el software de cliente. Aunque es posible implementar el cliente de forma manual en cada equipo, la mayoría de las organizaciones prefieren implementar el cliente a través de un proceso automatizado. Una organización más grande podría tener un sistema de distribución de software electrónico (ESD) operativo, que es un sistema de implementación de cliente ideal. Si no existe ningún sistema ESD, puede usar el método estándar de instalación de software de su organización. Los posibles métodos incluyen Directiva de grupo o diversas técnicas de scripting. En función de la cantidad y de ubicaciones dispares de los equipos cliente, este proceso de implementación puede ser complejo. Debe usar un enfoque estructurado para asegurarse de que todos los equipos tengan el cliente instalado con la configuración correcta.

Para obtener una lista de los requisitos mínimos de cliente, consulte [requisitos previos de App-V 5,0](app-v-50-prerequisites.md).

[Cómo implementar el cliente de App-V](how-to-deploy-the-app-v-client-gb18030.md)

## <a href="" id="bkmk-client-coexist"></a>Planeamiento de la coexistencia de aplicaciones-V del cliente


Puede implementar el cliente de App-V 5,0 en paralelo con el cliente de App-V 4,6. La coexistencia de cliente requiere que agregue o publique aplicaciones virtualizadas mediante un archivo de configuración de implementación o un archivo de configuración de usuario, porque hay ciertas opciones de configuración en estos archivos de configuración que se deben configurar para que App-V 5,0 funcione con los clientes de App-V 4.6. Cuando se actualiza un paquete mediante el cliente o el servidor, el paquete debe volver a enviar el archivo de configuración. Esto se aplica a cualquier paquete que tenga un archivo de configuración correspondiente, por lo que no es específico de la coexistencia de los clientes. Sin embargo, si no envía el archivo de configuración durante la actualización del paquete, el estado del paquete no funcionará como se espera en los escenarios de coexistencia.

Los archivos de configuración dinámica de App-V 5,0 personalizan un paquete para un usuario específico. Debe crear el archivo de configuración de usuario dinámica (. xml) o el archivo de configuración de implementación dinámica para poder usarlos. Para crear el archivo necesita una operación manual avanzada.

Cuando se usa un archivo de configuración de usuario dinámico, no se usa ninguna de la información de App-V 5,0 para la extensión en el archivo de manifiesto. Esto significa que el archivo de configuración de usuario dinámico debe incluir todo lo que sea para la extensión específica de App-V 5,0 en el archivo de manifiesto, así como los cambios que desea realizar, como, por ejemplo, las eliminaciones y actualizaciones. Para obtener más información sobre cómo crear un archivo de configuración personalizado, consulte [Cómo crear un archivo de configuración personalizado con la consola de administración de App-V 5,0](how-to-create-a-custom-configuration-file-by-using-the-app-v-50-management-console.md).

[Cómo implementar la aplicación-V 4,6 y el cliente de App-V 5,0 en el mismo equipo](how-to-deploy-the-app-v-46-and-the-app-v--50-client-on-the-same-computer.md)

## <a href="" id="bkmk-plan-for-scs"></a>Planificación del almacén de contenido compartido de App-V 5,0 (SCS)


El modo de almacenamiento compartido de contenido de App-V 5,0 permite al equipo que ejecuta el cliente de App-V 5,0 ejecutar aplicaciones virtualizadas y ninguno de los contenidos del paquete se guarda en el equipo que ejecuta el cliente de App-V 5,0. Las aplicaciones virtuales se transmiten a los equipos de destino solo cuando lo solicita el cliente.

En la siguiente lista se muestran algunas de las ventajas de usar el almacén de contenido compartido de App-V 5,0:

-   Conflictos de aplicaciones de aplicación y de multiusuario reducidos y, por lo tanto, una necesidad reducida de pruebas de regresión

-   Implementación acelerada de aplicaciones mediante la reducción del riesgo de implementación

-   Administración simplificada de perfiles

[Cómo instalar el cliente de App-V 5.0 para el modo de almacén de contenido compartido](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md)






## <a href="" id="other-resources-for-the-app-v-5-0-deployment-"></a>Otros recursos para la implementación de App-V 5,0


[Planificación de la implementación de App-V](planning-to-deploy-app-v.md)

 

 





