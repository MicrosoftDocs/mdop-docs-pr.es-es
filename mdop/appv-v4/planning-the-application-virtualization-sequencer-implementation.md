---
title: Planificación de la implementación del secuenciador de virtualización de aplicaciones
description: Planificación de la implementación del secuenciador de virtualización de aplicaciones
author: dansimp
ms.assetid: 052f32fe-ad13-4921-a8ce-4a657eb2b2bf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ac62991e290dcd2da1c42f025a19365bda239fb8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10815891"
---
# Planificación de la implementación del secuenciador de virtualización de aplicaciones


Secuenciación, el proceso que usa la virtualización de aplicaciones para crear aplicaciones virtuales y paquetes de aplicaciones, requiere el uso de un equipo con el software Application Virtualization Sequencer instalado.

Durante el proceso de secuenciación, el secuenciador se coloca en el modo de monitor y la aplicación que se va a secuenciar se instala en el equipo de secuencias. A continuación, se inicia la aplicación de secuencia y las funciones más importantes y más usadas se ejecutan para que el proceso de supervisión pueda configurar el bloque de características principal, que contiene el contenido mínimo de un paquete de aplicación que es necesario para que se ejecute una aplicación. Cuando se completan estos pasos, se detiene el modo de supervisión y la aplicación de secuencia se guarda y se prueba para comprobar que la operación es correcta.

Cuando decida qué aplicaciones elegir para la secuenciación, recuerde que determinadas aplicaciones no se pueden secuenciar. Estas incluyen determinadas partes del sistema operativo Windows, como Internet Explorer, controladores de dispositivos y aplicaciones que inician servicios en el momento del inicio.

Para obtener información paso a paso sobre cómo instalar el secuenciador, vea [Cómo instalar Application Virtualization Sequencer](how-to-install-the-application-virtualization-sequencer.md).

**Importante**  El equipo de seguridad de la empresa debe revisar y aprobar todo el plan de proceso de secuencia. Normalmente, las operaciones de secuenciar se mantendrían separadas del entorno de producción en un laboratorio. Esto puede ser tan simple o exhaustivo como sea necesario, en función de los requisitos de la empresa. Los equipos de secuencias necesitarán conectividad con la red corporativa para copiar paquetes finalizados en los servidores de producción. Sin embargo, dado que por lo general funcionan sin protección antivirus, no deben estar en la red corporativa desprotegida, por ejemplo, es posible que pueda trabajar detrás de un firewall o en un segmento de red aislado. El uso de equipos virtuales configurados para compartir una red virtual aislada también puede ser un enfoque aceptable. Siga las políticas de seguridad corporativas para resolver esta situación de manera segura.

 

Los pasos clave para planear el proceso de secuenciación son los siguientes:

-   Considere el número de aplicaciones que espera procesar cada mes, el tamaño de esas aplicaciones y agregue un límite para las futuras actualizaciones. Los paquetes pueden tener hasta 4 GB de tamaño, comprimidos o sin comprimir.

-   Prepare y documente un proceso metódico y repetible para que su organización siga la secuencia de cada aplicación. Esto debe incluir el uso de una lista de comprobación para cada ejecución, así como un proceso de control de versiones. El uso de un registro de seguimiento para cada aplicación de secuencia también es muy útil a la hora de investigar posibles problemas técnicos con un paquete.

-   Para las aplicaciones en secuencia, use equipos de alto rendimiento optimizados para procesar el rendimiento, con al menos 4 GB de RAM y una CPU rápida (3 GHz o más rápido). Los discos duros rápidos y el uso de volúmenes de disco independientes también pueden mejorar el rendimiento. Las máquinas virtuales son ideales para la secuenciación porque se pueden restablecer fácilmente, o bien puede usar un equipo físico con una imagen limpia en una partición local para permitir una nueva creación de imágenes después de completar cada operación de secuencia de paquetes.

    **Importante**  No se admite la ejecución del secuenciador de App-V en el modo seguro.

     

-   Compruebe que comprende el entorno operativo de la aplicación secuenciada, incluidos los elementos de integración como Microsoft Office o Java Runtime Environment, porque con frecuencia determinará si se tiene que instalar algo en el equipo de secuenciación antes de realizar la secuenciación de la aplicación.

-   Asegúrese de que cada nueva operación de secuenciación siempre comienza con una imagen base limpia. Asegúrese de que el equipo de secuenciación se ha restablecido, ya sea mediante la restauración de la imagen guardada en un equipo físico o mediante el reinicio de una máquina virtual después de descartar todos los cambios. La imagen base debe tener las últimas actualizaciones aplicadas desde Windows Update antes de guardarlas.

-   Desactive cualquier cosa en el equipo de secuencias que pueda interferir con el proceso de supervisión de la instalación, tales escáneres antivirus y Windows Update, debido a que es esencial disponer de una plataforma estable durante el proceso de secuenciación. Dado que este paso produce riesgos de seguridad considerables, asegúrese de que se tomen las precauciones correctas para proteger el equipo y la red, así como el paquete de aplicación secuenciado. Le recomendamos que realice un examen antivirus de paquetes de aplicaciones antes de hacerlo.

-   Incluya un proceso detallado para probar cada aplicación después de la secuencia. La prueba de la aplicación secuenciada determinará si funciona correctamente y es una parte esencial del proceso antes de implementar la aplicación virtualizada para los usuarios finales. Como paso final de las pruebas antes de la implementación a escala amplia a los usuarios finales, también debe planear una implementación piloto en un grupo de pruebas.

-   Cuando pruebe aplicaciones de secuencia, elija equipos del mismo tipo y ejecute los mismos sistemas operativos que se usan en el entorno de producción de la empresa. Siempre que estén configurados correctamente, se pueden usar máquinas virtuales o máquinas físicas.

## Temas relacionados


[Requisitos de hardware y software del secuenciador de virtualización de aplicaciones](application-virtualization-sequencer-hardware-and-software-requirements.md)

[Cómo instalar el secuenciador de virtualización de aplicaciones](how-to-install-the-application-virtualization-sequencer.md)

[Cómo actualizar el cliente secuenciador de virtualización de aplicaciones](how-to-upgrade-the-application-virtualization-sequencer.md)

[Introducción a la seguridad y la protección](security-and-protection-overview.md)

 

 





