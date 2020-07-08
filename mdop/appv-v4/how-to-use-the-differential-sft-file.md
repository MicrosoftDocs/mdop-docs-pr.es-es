---
title: Cómo usar el archivo SFT diferencial
description: Cómo usar el archivo SFT diferencial
author: dansimp
ms.assetid: 607e30fd-2f0e-4e2f-b669-0b3f010aebb0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 85cc45f9665569d77fcf275db6dbc080eb919229
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816390"
---
# Cómo usar el archivo SFT diferencial


Al secuenciar una aplicación, el secuenciador de Microsoft Application Virtualization (App-V) crea archivos SFT (. SFT) para almacenar toda la información de configuración y el contenido de los archivos de la aplicación virtual. En la versión 4.5 de App-V, se ha introducido el archivo de SFT diferencial (. dsft). Después de usar el secuenciador para crear una actualización de un paquete existente, puede optar por generar este archivo para almacenar solo las diferencias entre el paquete de aplicación secuencial original y la nueva versión. Por lo tanto, es mucho más pequeño que el archivo SFT completo para la nueva versión de la aplicación y reduce el impacto de enviar actualizaciones de paquetes a través de conexiones de red con poco ancho de banda. Sin embargo, su uso solo se admite en determinadas situaciones limitadas. Esta característica estaba pensada para usarse específicamente donde se utiliza un sistema de distribución de software electrónico (ESD) para administrar un grupo de usuarios con un servidor de archivos local a través de una conexión de ancho de banda bajo y no se usan servidores de streaming de App-V.

No es necesario usar el archivo SFT diferencial si está usando la configuración Manager2007 para administrar los usuarios, ya que Configuration Manager tiene compatibilidad con implementaciones con poco ancho de banda ya integradas. Tampoco es necesario si usa la administración de Application Virtualization (App-V) o los servidores de streaming con la actualización activa porque el cliente solo recuperará las diferencias entre las versiones de paquete nuevas y anteriores.

El procedimiento siguiente muestra cómo usar el mkdiffpkg.exe que está incluido en la instalación del secuenciador para crear el archivo SFT diferencial, después de completar la actualización del paquete de aplicación virtual y para implementar el archivo SFT diferencial. Completar este procedimiento ayuda a garantizar que si el paquete se descarga de alguna manera en el equipo cliente, la próxima vez que el usuario intente ejecutar la aplicación, el cliente volverá a la URL de invalidación, que está configurada para transmitir el paquete completo V2. SFT del recurso compartido de archivos local. Esto evitará que el usuario no haya podido iniciar la aplicación. Si todo el cliente se daña o se desinstala, se recomienda que el sistema de ESD esté configurado para implementar la versión completa del paquete actualizado, V2. SFT, al cliente.

Para obtener más información sobre cómo actualizar un paquete, consulte "Cómo actualizar una aplicación virtual existente" en la guía de operaciones de App-V 4.5 en <https://go.microsoft.com/fwlink/?LinkId=133129>

**Nota:**  Como requisito previo, todos los equipos de los usuarios a los que se dirige el ESD deben tener el archivo v1. SFT cargado completamente en su caché local, y la transmisión de archivos debe estar habilitada en todos los equipos.

 

**Para usar el archivo SFT diferencial**

1.  Inicie sesión en el equipo del secuenciador con una cuenta que tenga derechos de administrador. Abra el paquete original (V1) para la actualización en el secuenciador y, a continuación, actualice el paquete a la nueva versión (V2) y guárdelo como un nuevo V2. SFT.

2.  Abra una ventana de comandos en la carpeta de instalación de App-V 4.5 Sequencer y ejecute el siguiente comando:

    `“mkdiffpkg.exe V2.sft V2.dsft”`

3.  Con el sistema ESD u otro proceso de copia de archivos, copie el archivo de contenido completo del paquete V2, V2. SFT, a un recurso compartido de archivos local al que puedan acceder los equipos del usuario en una conexión de red bien conectada.

4.  Con el sistema ESD, coloca una copia del archivo SFT diferencial, V2. dsft, en cada equipo del usuario.

5.  Para importar el archivo V2. dsft, ejecute el siguiente comando de SFTMIME en cada equipo de usuario:

    `“SFTMIME load package:<package name> /SFTPATH <path to V2.dsft>”`

6.  Ejecute el siguiente comando SFTMIME en cada equipo del usuario para configurar la dirección URL de reemplazo para que apunte al archivo V2. SFT:

    `“SFTMIME configure package:<package name> /OverrideURL FILE://<network path to V2.sft>”`

**Nota**  
-   Los archivos de SFT diferencial deben aplicarse a los clientes en el orden correcto. Por ejemplo, V2. dsft debe aplicarse a una aplicación v1 antes de que se aplique V3. dsft.

-   La función **generar paquete de Microsoft Windows Installer (MSI)** en el secuenciador no se puede usar con el archivo SFT diferencial.

 

## Temas relacionados


[Cómo crear o actualizar aplicaciones virtuales con el secuenciador de App-V](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

 

 





