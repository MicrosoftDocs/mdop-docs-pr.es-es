---
title: Cómo configurar una memoria caché de solo lectura en el cliente App-V (RDS)
description: Cómo configurar una memoria caché de solo lectura en el cliente App-V (RDS)
author: dansimp
ms.assetid: b6607fe2-6f92-4567-99f1-d8e3c8a591e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a44844ae9ffc3497151be7713f6a43fda0ccd8fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817950"
---
# Cómo configurar una memoria caché de solo lectura en el cliente App-V (RDS)


**Importante**  Debe estar ejecutando App-V 4,6, SP1 para poder usar este procedimiento.

 

Puede implementar el cliente de App-V mediante una memoria caché compartida que se rellena con todas las aplicaciones necesarias para todos los usuarios. A continuación, configure los clientes de servicios de escritorio remoto (RDS) de App-V para que usen el mismo archivo de caché. A los usuarios se les concede acceso a aplicaciones específicas mediante el proceso de publicación de App-V. Puesto que la memoria caché ya está cargada previamente con todas las aplicaciones, no se produce ninguna transmisión por secuencias cuando un usuario inicia una aplicación. Sin embargo, los paquetes que se usan para rellenar previamente la memoria caché deben colocarse en un servidor de App-V que admita la transmisión por secuencias RTSP (Protocolo de transmisión en tiempo real) y que conceda permisos de acceso a los clientes de App-V. Si publica las aplicaciones con un servidor de administración de App-V, puede usarla para proporcionar esta función de transmisión por secuencias.

**Nota:**  Los detalles descritos en estos procedimientos están pensados únicamente como ejemplos. Puede usar diferentes métodos para completar el proceso general.

 

## Implementar el cliente de App-V en un escenario de RDS


El proceso de implementación consta de cuatro tareas principales:

-   Crear y rellenar el archivo de caché compartida Master

-   Copiar el archivo de caché compartido en el almacenamiento del servidor

-   Configuración del software de cliente de App-V

-   Administrar el ciclo de implementación de actualizaciones para el archivo de caché compartido después de la implementación inicial

Estas tareas requieren un planeamiento cuidadoso. Le recomendamos que prepare y documente un proceso metódico reproducible para que su organización siga. Esto es especialmente importante para la preparación y la implementación del archivo de caché compartido maestro y para la administración continuada de las actualizaciones de la aplicación, cada una de las cuales requiere una actualización de la caché compartida maestra. Use los procedimientos siguientes para completar estas tareas principales.

**Nota:**  Aunque puede publicar las aplicaciones con varios métodos diferentes, los procedimientos siguientes se basan en el uso de un servidor de administración de App-V para publicación.

 

**Para configurar la caché de solo lectura para la implementación inicial**

1. Configure y configure un servidor de administración de App-V para proporcionar compatibilidad de autenticación y publicación de usuarios.

2. Rellene la carpeta de contenido de este servidor de administración con todos los paquetes de aplicaciones necesarios para todos los usuarios.

3. Configure un equipo de ensayo que tenga instalado el cliente de App-V. Inicie sesión en el equipo de ensayo con una cuenta que tenga acceso a todas las aplicaciones, de modo que el conjunto completo de aplicaciones se publique en el equipo y, a continuación, transmita las aplicaciones a la memoria caché para que se carguen por completo.

   **Importante**  
   El equipo de almacenamiento provisional debe usar el mismo tipo de sistema operativo y la misma arquitectura de sistema que usan las máquinas virtuales en las que se ejecutará el cliente de App-V.

     

4. Reinicie el equipo de ensayo en modo seguro para asegurarse de que los drivers no se han iniciado, ya que esto bloquearía el archivo de caché.

   **Nota**  
   O bien, puede detener y deshabilitar el servicio de virtualización de aplicaciones y, a continuación, reiniciar el equipo. Una vez que se haya copiado el archivo, recuerde habilitar e iniciar el servicio.

     

5. Copie el archivo de la caché Sftfs. FSD a una SAN en la que todos los servidores RDS puedan tener acceso a él, por ejemplo, en una carpeta compartida. Establezca los permisos de acceso de la carpeta en solo lectura para el grupo todos y en control total para los administradores que administrarán las actualizaciones de archivos de caché. La ubicación del archivo de la caché se puede obtener en el registro del AppFS\\FileName.

   **Importante**  
   Debe colocar el archivo FSD en una ubicación que tenga la capacidad de respuesta y la confiabilidad iguales al rendimiento del almacenamiento conectado localmente, por ejemplo, un SAN.

     

6. Instale el cliente de aplicación-V RDS en cada servidor RDS y, a continuación, configúrelo para usar la caché de solo lectura agregando los siguientes valores de clave del registro a la clave AppFS en el cliente. La clave AppFS se encuentra en HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS en los equipos de 32 bits y en HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS para equipos de 64 bits.

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
   <td align="left"><p>Ruta de FSD</p></td>
   <td align="left"><p>Especifica la ruta de acceso al archivo de la caché compartida, por ejemplo, \RDSServername\Sharefolder\SFTFS. FSD (obligatorio).</p></td>
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
   <td align="left"><p>Ruta de acceso del archivo de registro de errores (. ETL)</p></td>
   <td align="left"><p>Entrada usada para especificar la ruta de acceso del registro de errores. Práctica. Use una ruta local, como C:\Logs\Sftfs.etl).</p></td>
   </tr>
   </tbody>
   </table>

     

7. Configure cada servidor RDS de la granja para usar el servidor de publicación y para usar la actualización de publicación cuando los usuarios inicien sesión. A medida que los usuarios inician sesión en los servidores de RDS, se produce un ciclo de actualización de publicación y se publican todas las aplicaciones para las que su cuenta está autorizada. Estas aplicaciones se ejecutan desde la memoria caché compartida.

**Para configurar el cliente de RDS para la actualización de paquetes**

1.  Complete la actualización y las pruebas del paquete de la aplicación.

2.  Actualice el paquete en el servidor de App-V. A continuación, publique y transmita la nueva versión de las aplicaciones al cliente en el equipo de ensayo para que se carguen por completo en la caché.

3.  Reinicie el equipo de ensayo en modo seguro para asegurarse de que los drivers no se han iniciado.

    **Nota:**  También puede detener y, a continuación, deshabilitar el servicio de virtualización de aplicaciones en Services. msc y reiniciar el equipo. Una vez que se haya copiado el archivo, recuerde habilitar e iniciar el servicio.

     

4.  Copie el archivo de la caché Sftfs. FSD a una SAN en la que todos los servidores RDS puedan tener acceso a él, por ejemplo, en una carpeta compartida. Puede usar un nombre de archivo diferente, por ejemplo, SFTFS \ _V2. FSD, para distinguir la nueva versión.

5.  Para configurar el cliente de App-V RDS en cada servidor RDS de la granja para usar el archivo de caché compartido actualizado, cambie el valor del nombre de archivo de la clave de registro AppFS para que apunte a la ubicación del archivo actualizado, por ejemplo, \\\\RDSServername\\Sharefolder\\SFTFS\ _V2. FSD. Esto garantiza que cada servidor RDS recibirá la copia actualizada de la memoria caché cuando se reinicien los drivers de App-Vclient.

    **Importante**  Debe reiniciar los servidores de RDS para poder usar el archivo de caché compartido actualizado.

     

## Cómo usar vínculos simbólicos al actualizar la caché


En lugar de cambiar el valor del nombre de archivo de la clave AppFS cada vez que se implementa un nuevo archivo de caché que contiene paquetes nuevos o actualizados, puede usar un vínculo simbólico en los siguientes sistemas operativos: Windows Vista, Windows 7 y Windows Server 2008. Para obtener más información sobre los vínculos simbólicos, consulte [vínculos simbólicos](https://go.microsoft.com/fwlink/?LinkId=157626) ( https://go.microsoft.com/fwlink/?LinkId=157626) . Por el contrario, Windows XP no admite el uso de vínculos simbólicos y, en su lugar, debe usar puntos de Unión. Para obtener más información acerca de las uniones, consulte el [artículo 205524](https://go.microsoft.com/fwlink/?LinkId=182553) en Microsoft Knowledge base ( https://go.microsoft.com/fwlink/?LinkId=182553) y también la herramienta Unión de la versión [v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) ( https://go.microsoft.com/fwlink/?LinkId=182554) .

**Para configurar un vínculo simbólico para que haga referencia a la caché**

1.  Durante la fase de implementación inicial, abra una ventana del símbolo del sistema como administrador local en el sistema operativo host del servidor RDS.

2.  Cree un vínculo simbólico mediante el comando MKLINK y, a continuación, configúrelo para que apunte al archivo Sftfs. FSD.

    **     mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd**

3.  En la imagen de VM maestra de VDI, abra una ventana del símbolo del sistema con la opción **Ejecutar como administrador** y otorgue permisos de vínculos remotos para que la máquina virtual pueda acceder al vínculo simbólico en el sistema operativo host de VDI. De forma predeterminada, los permisos de vínculos remotos están deshabilitados.

    **fsutil Behavior Set SymlinkEvaluation R2R: 1**

    **Nota:**  En el servidor de almacenamiento, los permisos de vínculo apropiados deben estar habilitados. Según la ubicación del vínculo y el archivo Sftfs. FSD, los permisos son **L2L: 1** o **L2R: 1** o **R2L: 1** o **R2R: 1**.

     

4.  Cuando configures el cliente de usuario de App-V, establece el valor de nombre de archivo de la clave AppFS igual a la ruta de acceso UNC del archivo FSD que usa el vínculo simbólico. Por ejemplo, establezca el nombre de archivo en \\\\VDIHostserver\\Symlinkname. Cuando el cliente de App-V accede por primera vez a la caché, el vínculo simbólico pasa al cliente un identificador para el archivo de la caché. El cliente continúa usando ese identificador siempre que se esté ejecutando el cliente. El valor del vínculo simbólico puede actualizarse de forma segura incluso si los clientes existentes tienen la caché compartida antigua abierta.

5.  Cuando deba actualizar un paquete o agregar un nuevo paquete a la caché, siga los pasos 1 a 4 del procedimiento de actualización. A continuación, elimine el vínculo simbólico y vuelva a crearlo para que apunte a la nueva versión del archivo de caché compartido. Esto garantiza que cada servidor RDS recibirá la copia actualizada de la caché cuando se reinicien los drivers del cliente App-V. Cuando se reinicia el servidor RDS, el cliente de App-V recibe un identificador de la copia actualizada de la caché porque el cliente usa la ruta de acceso que contiene el vínculo simbólico actualizado. A continuación, los usuarios tienen acceso a las aplicaciones nuevas y actualizadas.

## Temas relacionados


[Cómo instalar el servidor de administración de virtualización de aplicaciones](how-to-install-application-virtualization-management-server.md)

[Cómo instalar manualmente el cliente de virtualización de aplicaciones](how-to-manually-install-the-application-virtualization-client.md)

[Cómo instalar el cliente mediante el uso de la línea de comandos](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





