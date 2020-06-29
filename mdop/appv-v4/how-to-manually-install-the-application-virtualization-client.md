---
title: Cómo instalar manualmente el cliente de virtualización de aplicaciones
description: Cómo instalar manualmente el cliente de virtualización de aplicaciones
author: dansimp
ms.assetid: bb67f70b-d525-4317-b254-e4f084c717ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 0cb41b5e51bd33c377b17c088e97cb54f1a57685
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817081"
---
# Cómo instalar manualmente el cliente de virtualización de aplicaciones

Existen dos tipos de componentes de cliente de virtualización de aplicaciones: el cliente de escritorio de virtualización de aplicaciones, que está diseñado para la instalación en equipos de escritorio, y el cliente de virtualización de aplicaciones para servicios de escritorio remoto (anteriormente servicios de Terminal Server), que puede instalar en servidores de host de sesión de escritorio remoto. Aunque los dos programas de instalación del cliente son diferentes, puede usar el siguiente procedimiento para instalar manualmente el cliente de escritorio de Application Virtualization en un solo equipo de escritorio o el cliente de virtualización de aplicaciones para servicios de escritorio remoto en un solo servidor host de sesión de escritorio remoto. En un entorno de producción, lo más probable es que instale el cliente de escritorio de Application Virtualization en varios equipos de escritorio con un proceso de instalación automatizado. Para obtener información sobre cómo instalar varios clientes con un proceso de instalación con secuencias de comandos, consulte [Cómo instalar el cliente mediante la línea de comandos](how-to-install-the-client-by-using-the-command-line-new.md).

**Nota**  
1. Si va a instalar el cliente de virtualización de aplicaciones para el software de servicios de escritorio remoto en un servidor host de sesión de escritorio remoto, aconseje a los usuarios que tengan una sesión de cliente de RDP o ICA abierta con el servidor host de sesión de escritorio remoto que deben guardar su trabajo y cerrar sus sesiones. En una sesión de escritorio remoto, puede instalar el cliente de forma manual. Para obtener más información sobre cómo actualizar el cliente, vea [Cómo actualizar el cliente de virtualización de aplicaciones](how-to-upgrade-the-application-virtualization-client.md).

2. Si tiene alguna configuración en el equipo del usuario que dependa de la ruta de instalación del cliente, tenga en cuenta que el cliente de virtualización de aplicaciones (App-V) 4,5 usa una carpeta de instalación distinta de las versiones anteriores. De forma predeterminada, una nueva instalación del cliente de Application Virtualization (App-V) 4,5 se instalará en la carpeta \\Archivos de Programa\\microsoft de la aplicación de virtualización de Office. Si ya está instalada una versión anterior del cliente, la instalación del cliente de App-V realizará una actualización en la carpeta de instalación existente.

**Nota**  
Para App-V versión 4,6 y posteriores, cuando el cliente de App-V está instalado, SFTLDR.DLL se instala en el directorio Windows\\system32. Si el cliente de App-V está instalado en un sistema de 64 bits, SFTLDR\_WOW64.DLL se instala en el directorio Windows\\SysWOW64.

**Para instalar manualmente el cliente de escritorio de virtualización de aplicaciones**

1. Una vez que haya obtenido el archivo de instalación correcto y lo haya guardado en el equipo, asegúrese de que ha iniciado sesión con una cuenta que tiene derechos de administrador en el equipo y haga doble clic en él para expandir el archivo.

2. Elija la carpeta en la que desea guardar los archivos y, a continuación, abra la carpeta después de que se hayan copiado los archivos en él.

3. Revise las notas de la versión si corresponde.

4. Busque el archivo de setup.exe y haga doble clic en setup.exe para iniciar la instalación.

5. El asistente comprueba el sistema para asegurarse de que se ha instalado todo el software necesario y, si no se encuentra alguno de los siguientes elementos, el asistente le pedirá automáticamente que lo instale:

    - Paquete redistribuible de Microsoft Visual C++ 2005 SP1 (x86)

    - Microsoft Core XML Services (MSXML) 6,0 SP1 (x86)

    - Informes de errores de aplicaciones de Microsoft

    **Nota**  
    Para App-V versión 4,6 y posteriores, el Asistente también instalará Microsoft Visual C++ 2008 SP1 Redistributable Package (x86).

    Para obtener más información sobre cómo instalar Microsoft Visual C++ 2008 SP1 Redistributable Package (x86), consulte [https://go.microsoft.com/fwlink/?LinkId=150700](https://go.microsoft.com/fwlink/?LinkId=150700) .

    Si se le solicita, haga clic en **instalar**. Se muestra el progreso de instalación y el estado cambia de **pendiente** a **instalación**. El estado de la instalación cambiará a **correcto** , ya que cada paso se completa correctamente.

6. Cuando se muestre el **Asistente para el asistente InstallShield de Microsoft Application Virtualization Desktop** , haga clic en **siguiente**.

7. Aparece la pantalla **contrato de licencia** . Lea el contrato de licencia y, si está de acuerdo, haga clic en Acepto **las condiciones del contrato de licencia** y, a continuación, haga clic en **siguiente**.

   De manera opcional, puedes hacer clic en el botón para leer la declaración de privacidad. Para acceder a la declaración de privacidad, debe estar conectado a Internet.

8. En la pantalla **tipo de configuración** , seleccione el tipo de configuración. Haga clic en **típica** para usar los valores de programa predeterminados, o haga clic en **personalizado** si desea establecer la configuración del programa durante la instalación.

9. Si elige **típica**, la siguiente pantalla muestra **preparado para instalar el programa**. Haga clic en **instalar** para iniciar la instalación.

10. Si elige **personalizado**, aparece la pantalla **carpeta de destino** .

11. En la pantalla **carpeta de destino** , haga clic en **siguiente** para aceptar la carpeta predeterminada o haga clic en **cambiar** para mostrar la pantalla cambiar la **carpeta de destino actual** . Vaya a o, en el campo **nombre de carpeta** , escriba la carpeta de destino, haga clic en **Aceptar**y, a continuación, haga clic en **siguiente**.

12. En la pantalla **Ubicación de datos de Application Virtualization** , haga clic en **siguiente** para aceptar las ubicaciones de datos predeterminadas o realice las siguientes acciones para cambiar la ubicación de almacenamiento de los datos:

    1. Haga clic en **cambiar**y, a continuación, vaya a o, en el campo **ubicación global de datos** , escriba la carpeta de destino de la ubicación de datos global y haga clic en **Aceptar**. El directorio de datos global es el lugar donde el cliente de escritorio de virtualización de aplicaciones almacena en caché los datos compartidos por todos los usuarios del equipo, como los archivos OSD y los datos de archivo SFT.

    2. Si desea cambiar la letra de unidad que se va a usar, seleccione la letra de unidad que prefiera de la lista desplegable.

    3. Escriba una nueva ruta de acceso para almacenar los datos específicos del usuario en el campo **Ubicación de datos específica del usuario** si desea cambiar la ubicación de los datos. El directorio de datos de usuario es el lugar donde el cliente de escritorio de virtualización de aplicaciones almacena información específica del usuario, como la configuración personal de aplicaciones virtualizadas.

       **Nota**  
       Esta ruta de acceso debe ser diferente para cada usuario, por lo que debe incluir una variable de entorno específica del usuario o una unidad asignada o cualquier otro elemento que se resuelva como una ruta de acceso única para cada usuario.

    4. Cuando haya terminado de realizar los cambios, haga clic en **siguiente**.

13. En la pantalla **configuración de tamaño de caché** , puede aceptar o cambiar el tamaño predeterminado de la memoria caché. Haga clic en uno de los siguientes botones de radio para elegir cómo administrar el espacio de caché:

    1. **Use el tamaño máximo de caché**. Escriba un valor numérico comprendido entre 100 y 1048576 (1 TB) en el campo **tamaño máximo (MB)** para especificar el tamaño máximo de la memoria caché.

    2. **Use el umbral de espacio libre en disco**. Escriba un valor numérico para especificar la cantidad de espacio libre en disco, en MB, que el cliente de virtualización de aplicaciones debe dejar de estar disponible en el disco. Esto permite que la caché crezca hasta que la cantidad de espacio libre en el disco alcance este límite. El valor que se muestra en **espacio libre de disco restante** indica cuánto espacio de disco está actualmente sin usar.

    **Importante**  
    Para asegurarse de que la memoria caché tiene suficiente espacio asignado para todos los paquetes que se pueden implementar, use la configuración de **umbral usar espacio libre en disco** al configurar el cliente para que la caché pueda crecer según sea necesario. Como alternativa, determine de antemano cuánto espacio en disco será necesario para la caché de App-V y, en el momento de la instalación, establezca el tamaño de la caché según corresponda. Para obtener más información sobre la característica de administración de espacios en caché, en la guía de operaciones de Microsoft Application Virtualization (App-V), vea **Cómo usar la característica de administración de espacio en caché**.

    Haz clic en **Siguiente** para continuar.

14. En las siguientes secciones de la pantalla de configuración de la **Directiva de paquete en tiempo de ejecución** , puede cambiar los parámetros que afectan a la forma en que el cliente de virtualización de aplicaciones se comporta durante el tiempo de ejecución:

    1. **Raíz de origen**de la aplicación. Especifica la ubicación de los archivos de SFT. Si se usa, reemplaza las partes protocolo, servidor y puerto de la dirección URL del código base HREF en el archivo OSD.

    2. **Autorización**de la aplicación. Cuando se activa la opción **requerir autorización del usuario, incluso cuando la caché** está activada, los usuarios deben conectarse a un servidor y validar sus credenciales al menos una vez antes de que se les permita iniciar cada aplicación virtual.

    3. **Permitir la transferencia desde un archivo**. Indica si se habilitará la transmisión desde un archivo, independientemente de cómo se use el campo **raíz de origen** de la aplicación. Si no está activado, la transmisión por secuencias de archivos está deshabilitada. Debe activarse si la **raíz de origen** de la aplicación contiene una ruta de acceso UNC con el formato \\\\server\\share.

    4. **Cargar la aplicación automáticamente**. Controla cuándo y cómo se produce la carga automática de aplicaciones en segundo plano.

       **Nota**  
       Al instalar el cliente de App-V para usarlo con una caché de solo lectura, por ejemplo, con una implementación de servidor VDI, establezca **las aplicaciones que se cargan** automáticamente en **no cargar aplicaciones automáticamente** para evitar que el cliente intente actualizar aplicaciones en la caché de solo lectura.

    Haz clic en **Siguiente** para continuar.

15. En la pantalla de **Publishing Server** , seleccione la casilla **configurar un servidor de publicación ahora** si desea definir un servidor de publicación, o haga clic en **siguiente** si desea hacerlo más tarde. Para definir un servidor de publicación, especifique la siguiente información:

    1. **Nombre para mostrar**: escriba el nombre que desea mostrar para el servidor.

    2. **Tipo**: seleccione el tipo de servidor de la lista desplegable de tipos de servidor.

    3. **Nombre de host** y **Puerto**: escriba el nombre de host y el puerto en los campos correspondientes. Al seleccionar un tipo de servidor en la lista desplegable, el campo puerto se rellenará automáticamente con los números de puertos estándar. Para cambiar un número de puerto, haga clic en el tipo de servidor en la lista y cambie el número de Puerto según sus necesidades.

    4. **Ruta**: Si ha seleccionado un **servidor HTTP estándar** o un **servidor HTTP de seguridad mejorado**, debe escribir la ruta de acceso completa del archivo XML que contiene la publicación de datos en este campo. Si selecciona **Application Virtualization Server** o servidor de **Virtualización mejorada de aplicaciones de seguridad**, este campo no está activo.

    5. **Ponerse en contacto automáticamente con este servidor para actualizar la configuración cuando un usuario inicia**sesión: Seleccione esta casilla si desea que se consulte este servidor automáticamente cuando los usuarios inicien sesión en su cuenta en el cliente de virtualización de aplicaciones.

    6. Cuando haya finalizado con los pasos de configuración, haga clic en **siguiente**.

16. En la pantalla **preparado para instalar el programa** , haga clic en **instalar**. Se muestra una pantalla que muestra el progreso de la instalación.

17. En la pantalla **Asistente de instalación completada** , haga clic en **Finalizar**.

    **Nota**  
    Si la instalación no se realiza por algún motivo, es posible que tenga que reiniciar el equipo antes de volver a intentar la instalación.

## Temas relacionados

[Cómo instalar el cliente mediante el uso de la línea de comandos](how-to-install-the-client-by-using-the-command-line-new.md)

[Introducción al escenario de distribución independiente](stand-alone-delivery-scenario-overview.md)
