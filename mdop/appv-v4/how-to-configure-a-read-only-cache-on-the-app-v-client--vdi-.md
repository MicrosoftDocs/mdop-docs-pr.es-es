---
title: Cómo configurar una memoria caché de solo lectura en el cliente App-V (VDI)
description: Cómo configurar una memoria caché de solo lectura en el cliente App-V (VDI)
author: dansimp
ms.assetid: 7a41e017-9e23-4a6a-a659-04d23f008b83
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 114f9dfbf55a3f62b6bc8bec6b37a659ffbfaf56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817941"
---
# Cómo configurar una memoria caché de solo lectura en el cliente App-V (VDI)


En Microsoft Application Virtualization (App-V) 4,6 el cliente admite el uso de una caché de solo lectura compartida. La caché de solo lectura compartida permite al cliente usar el espacio de disco de forma eficaz en un sistema de infraestructura de escritorio virtual (VDI), donde los usuarios ejecutan aplicaciones en máquinas virtuales (VM) hospedadas en un entorno de servidor del centro de datos y compartir almacenamiento de red en una red de área de almacenamiento (SAN). Los procedimientos siguientes proporcionan una descripción general del proceso necesario para implementar el cliente de App-V en cualquiera de las arquitecturas VDI principales, conocidas como "VM agrupada" o "VM estática". Se supone que está familiarizado con la planificación, la implementación y el funcionamiento del sistema App-V y sus componentes, así como el funcionamiento y la administración del servidor VDI. Para obtener más información sobre App-V, consulte [Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939)

**Nota:**  Los detalles descritos en estos procedimientos están pensados únicamente como ejemplos. Puede usar diferentes métodos para completar el proceso general.

 

## Implementar el cliente de App-V en un escenario de VDI


Puede implementar el cliente de App-V en un escenario de VDI usando una caché de solo lectura compartida que se ha rellenado con todas las aplicaciones necesarias para todos los usuarios. Después, configure la imagen VM maestra de VDI para que todos los clientes de App-V usen el mismo archivo de caché. A los usuarios se les concede acceso a aplicaciones específicas mediante el proceso de publicación de App-V. Puesto que la memoria caché ya está cargada previamente con todas las aplicaciones, no se produce ninguna transmisión por secuencias cuando un usuario inicia una aplicación. Sin embargo, los paquetes que se usan para rellenar previamente la memoria caché deben colocarse en un servidor de App-V que admita la transmisión por secuencias RTSP (Protocolo de transmisión en tiempo real) y que conceda permisos de acceso a los clientes de App-V. Si publica las aplicaciones con un servidor de administración de App-V, puede usarla para proporcionar esta función de transmisión por secuencias.

El proceso de implementación consta de cuatro tareas principales:

-   Crear y rellenar el archivo de caché compartida Master

-   Copiar el archivo de caché compartido en el almacenamiento del servidor VDI

-   Configuración del software cliente de App-V en la imagen maestra de VDI

-   Administrar el ciclo de implementación de actualizaciones para el archivo de caché compartido después de la implementación inicial

Estas tareas requieren un planeamiento cuidadoso. Le recomendamos que prepare y documente un proceso metódico reproducible para que su organización siga. Esto es especialmente importante para la preparación inicial y la implementación del archivo de caché compartido maestro, y para la administración continuada de actualizaciones de la aplicación, cada una de las cuales requiere una actualización de la caché compartida maestra. Use los procedimientos siguientes para completar estas tareas principales.

**Nota:**  Aunque puede publicar las aplicaciones con varios métodos diferentes, los procedimientos siguientes se basan en el uso de un servidor de administración de App-V para publicar.

 

**Para configurar la caché de solo lectura para la implementación inicial en un escenario de VDI agrupada de VM o de VM estática**

1. Configure y configure un servidor de administración de App-V en una VM en el servidor VDI para proporcionar la autenticación de usuarios y la compatibilidad de publicación.

2. Rellene la carpeta de contenido de este servidor de administración con todos los paquetes de aplicaciones necesarios para todos los usuarios.

3. Configure un equipo de ensayo que tenga instalado el cliente de App-V. Inicie sesión en el equipo de ensayo con una cuenta que tenga acceso a todas las aplicaciones, de modo que el conjunto completo de aplicaciones se publique en el equipo y, a continuación, transmita las aplicaciones a la memoria caché para que se carguen por completo.

   **Importante**  
   El equipo de almacenamiento provisional debe usar el mismo tipo de sistema operativo y la misma arquitectura de sistema que usan las máquinas virtuales en las que se ejecutará el cliente de App-V.

     

4. Reinicie el equipo de ensayo en modo seguro para asegurarse de que los drivers no se hayan iniciado, lo cual bloqueará el archivo de la caché.

   **Nota**  
   Como alternativa, puede detener y deshabilitar el servicio de virtualización de aplicaciones y, a continuación, reiniciar el equipo. Una vez que se haya copiado el archivo, recuerde habilitar e iniciar el servicio.

     

5. Copie el archivo de la caché Sftfs. FSD en la red SAN del servidor VDI, donde todas las VM pueden tener acceso a ella, como en una carpeta compartida. Establezca los permisos de acceso de la carpeta en solo lectura para el grupo todos y en control total para los administradores que administrarán las actualizaciones de archivos de caché. La ubicación del archivo de la caché se puede obtener en el registro del AppFS\\FileName.

   **Importante**  
   Debe colocar el archivo FSD en una ubicación con la capacidad de respuesta y la confiabilidad equivalente al rendimiento de almacenamiento conectado localmente, por ejemplo, un SAN.

     

6. Instale el cliente de escritorio de App-V en la imagen de VM maestra de VDI y, a continuación, configúrelo para usar la caché de solo lectura agregando los siguientes valores de clave de registro a la clave AppFS en el cliente. La clave AppFS se encuentra en HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS.

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tecla</th>
   <th align="left">Tipo</th>
   <th align="left">Valor</th>
   <th align="left">Propósito</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>FileName</p></td>
   <td align="left"><p>Cadena</p></td>
   <td align="left"><p>Ruta de acceso a FSD</p></td>
   <td align="left"><p>Especifica la ruta de acceso al archivo de caché compartido, por ejemplo, \VDIServername\Sharefolder\SFTFS. FSD (obligatorio).</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReadOnlyFSD</p></td>
   <td align="left"><p>DWORD</p></td>
   <td align="left"><p>uno</p></td>
   <td align="left"><p>Configura el cliente para que funcione en modo de solo lectura. Esto garantiza que el cliente no intentará transmitir las actualizaciones a la caché del paquete. (Necesario)</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ErrorLogLocation</p></td>
   <td align="left"><p>Cadena</p></td>
   <td align="left"><p>Ruta de acceso al archivo de registro de errores (. ETL)</p></td>
   <td align="left"><p>Entrada usada para especificar la ruta de acceso al registro de errores. Práctica. Use una ruta local, como C:\Logs\Sftfs.etl).</p></td>
   </tr>
   </tbody>
   </table>

     

7. Configure el cliente de imagen de VM maestro para usar el servidor de publicación y para usar la actualización de publicación al iniciar sesión. A medida que los usuarios inician sesión en el sistema VDI y su VM se crea a partir de la imagen de VM maestra, se produce un ciclo de actualización de publicación y se publican todas las aplicaciones para las que su cuenta está autorizada. Estas aplicaciones se ejecutan desde la memoria caché compartida.

**Para configurar el cliente para la actualización de paquetes en un escenario de VM agrupada**

1.  Complete la actualización y las pruebas del paquete de la aplicación.

2.  Actualice el paquete en el servidor de App-V. A continuación, publique y transmita la nueva versión de las aplicaciones al cliente en el equipo de ensayo para que se carguen por completo en la caché.

3.  Reinicie el equipo de ensayo en modo seguro para asegurarse de que los drivers no se han iniciado.

    **Nota:**  Como alternativa, puede detener y deshabilitar el servicio de virtualización de aplicaciones en Services. msc y, a continuación, reiniciar el equipo. Una vez que se haya copiado el archivo, recuerde habilitar e iniciar el servicio.

     

4.  Copie el archivo de la caché Sftfs. FSD en la red SAN del servidor VDI, donde todas las VM pueden tener acceso a ella, como en una carpeta compartida. Puede usar un nombre de archivo diferente, por ejemplo, SFTFS \ _V2. FSD, para distinguir la nueva versión.

5.  Para configurar el cliente de escritorio de App-V en la imagen de VM maestra de VDI para usar el archivo de caché compartido actualizado, cambie el valor de nombre de archivo de la clave de registro AppFS para que apunte a la ubicación del archivo actualizado, por ejemplo, \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD. Cuando los usuarios cierran sesión e inician sesión de nuevo, se crea una nueva máquina virtual para ellos con la imagen principal actualizada. Toda la configuración de usuario se conservará y se aplicará a la nueva máquina virtual. Entonces tienen acceso a las aplicaciones actualizadas.

**Para configurar el cliente para la actualización de paquetes en un escenario de VM estática**

1.  Complete la actualización y las pruebas del paquete de la aplicación.

2.  Actualice el paquete en el servidor de App-V. Después, publique y transmita la nueva versión de las aplicaciones al cliente en el equipo de ensayo para que las aplicaciones se carguen por completo en la memoria caché.

3.  Reinicie el equipo de ensayo en modo seguro para asegurarse de que los drivers no se han iniciado.

    **Nota:**  Como alternativa, puede detener y deshabilitar el servicio de virtualización de aplicaciones en Services. msc y, a continuación, reiniciar el equipo. Una vez que se haya copiado el archivo, recuerde habilitar e iniciar el servicio.

     

4.  Copie el archivo de la caché Sftfs. FSD en la red SAN del servidor VDI, donde todas las VM pueden tener acceso a ella, como en una carpeta compartida. Puede usar un nombre de archivo diferente, por ejemplo, SFTFS \ _V2. FSD, para distinguir la nueva versión.

5.  Para configurar el cliente de escritorio de App-V en la imagen de VM maestra de VDI para usar el archivo de caché compartido actualizado, cambie el valor de nombre de archivo de la clave de registro AppFS para que apunte a la ubicación del archivo actualizado, por ejemplo, \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD. Esto garantiza que los nuevos usuarios reciban la nueva versión.

6.  Cree un script que edite el valor del nombre de archivo de la clave AppFS para establecerlo en la ubicación de la caché actualizada, por ejemplo, \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD. Configure este script para que se ejecute cuando el usuario cierre sesión o inicie sesión para que se ejecute antes de que se inicien los controladores del cliente de App-V, por ejemplo, con la configuración de directiva de grupo. Cuando los usuarios cierran la sesión e inician sesión de nuevo, su VM actual se actualiza y usarán la copia actualizada de la memoria caché. A continuación, tienen acceso a las aplicaciones actualizadas.

## Cómo usar vínculos simbólicos al actualizar la caché


En lugar de modificar el valor nombre de archivo de la clave AppFS cada vez que se implementa un nuevo archivo de caché que contiene paquetes nuevos o actualizados, puede usar un vínculo simbólico en los siguientes sistemas operativos: Windows Vista, Windows 7 y Windows Server 2008. Para obtener más información sobre los vínculos simbólicos, consulte [vínculos simbólicos](https://go.microsoft.com/fwlink/?LinkId=157626) ( https://go.microsoft.com/fwlink/?LinkId=157626) . Por el contrario, Windows XP no admite el uso de vínculos simbólicos y, en su lugar, debe usar puntos de Unión. Para obtener más información acerca de las uniones, consulte el [artículo 205524](https://go.microsoft.com/fwlink/?LinkId=182553) en Microsoft Knowledge base ( https://go.microsoft.com/fwlink/?LinkId=182553) y también la herramienta Unión de la versión [v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) ( https://go.microsoft.com/fwlink/?LinkId=182554) .

**Para configurar un vínculo simbólico para que haga referencia a la caché**

1.  Durante la fase de implementación inicial, abra una ventana del símbolo del sistema como administrador local en el sistema operativo host del servidor VDI.

2.  Cree un vínculo simbólico mediante el comando MKLINK y, a continuación, configúrelo para que apunte al archivo Sftfs. FSD.

    **     mklink symlinkname \\\\vdihostserver\\sharefolder\\sftfs.fsd**

3.  En la imagen de VM maestra de VDI, abra una ventana del símbolo del sistema con la opción **Ejecutar como administrador** y otorgue permisos de vínculos remotos para que la máquina virtual pueda acceder al vínculo simbólico en el sistema operativo host de VDI. De forma predeterminada, los permisos de vínculos remotos están deshabilitados.

    **fsutil Behavior Set SymlinkEvaluation R2R: 1**

    **Nota:**  En el servidor de almacenamiento, los permisos de vínculo apropiados deben estar habilitados. Según la ubicación del vínculo y el archivo Sftfs. FSD, los permisos son **L2L: 1** o **L2R: 1** o **R2L: 1** o **R2R: 1**.

     

4.  Al configurar el cliente de escritorio de App-V en la imagen de VM maestra de VDI, establezca el valor de nombre de archivo de la clave AppFS igual a la ruta de acceso UNC del archivo FSD que usa el vínculo simbólico; por ejemplo, establézcalo en \\\\VDIHostserver\\Symlinkname. Cuando el cliente de App-V accede por primera vez a la caché, el vínculo simbólico pasa al cliente un identificador para el archivo de la caché. El cliente continúa usando ese identificador siempre que se esté ejecutando el cliente. El valor del vínculo simbólico puede actualizarse de forma segura incluso si los clientes existentes tienen la caché compartida antigua abierta.

5.  Cuando tenga que actualizar un paquete o agregar un nuevo paquete a la caché, siga los pasos 1 a 5 del procedimiento de actualización para el escenario de la VM estática o de la VM agrupada. A continuación, elimine el vínculo simbólico y vuelva a crearlo para que apunte a la nueva versión del archivo de caché compartido. Cuando se reinicia la VM, el cliente recibe un identificador de la copia actualizada de la caché porque la VM usa la ruta de acceso que contiene el vínculo simbólico actualizado. A continuación, los usuarios tienen acceso a las aplicaciones nuevas y actualizadas.

## Temas relacionados


[Cómo instalar el servidor de administración de virtualización de aplicaciones](how-to-install-application-virtualization-management-server.md)

[Cómo instalar manualmente el cliente de virtualización de aplicaciones](how-to-manually-install-the-application-virtualization-client.md)

[Cómo instalar el cliente mediante el uso de la línea de comandos](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





