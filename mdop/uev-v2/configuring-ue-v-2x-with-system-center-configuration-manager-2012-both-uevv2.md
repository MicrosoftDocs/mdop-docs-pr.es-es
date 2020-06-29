---
title: Configuración de UE-V 2. x con System Center Configuration Manager 2012
description: Configuración de UE-V 2. x con System Center Configuration Manager 2012
author: dansimp
ms.assetid: 9a4e2a74-7646-4a77-b58f-2b4456487295
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: 2ff9ccc1a17db31471549ece37461558768c3a2b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824410"
---
# Configuración de UE-V 2. x con System Center Configuration Manager 2012


Después de instalar la virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 o 2,1 SP1 y las características requeridas, UE-V debe estar configurado. El paquete de configuración de UE-V proporciona a los administradores una manera de usar la característica de configuración de cumplimiento de System Center Configuration Manager 2012 SP1 o posterior para aplicar configuraciones coherentes en los sitios donde se instalan UE-V y Configuration Manager.

## Características compatibles con el paquete de configuración de UE-V


El paquete de configuración de UE-V incluye herramientas para realizar las siguientes tareas:

-   Crear o actualizar las líneas de distribución de plantillas de la ubicación de configuración de UE-V.

    -   Definir plantillas de UE-V para que se registren o no

    -   Actualizar los elementos de configuración de la plantilla UE-V y las líneas de base como plantillas se agregan o actualizan

    -   Distribuir y registrar plantillas de UE-V mediante el uso de correcciones de elementos de configuración estándar

-   Cree o actualice un elemento de configuración de directiva de UE-V Agent para establecer o borrar esta configuración.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Tamaño máximo del paquete</p></td>
    <td align="left"><p>Habilitar o deshabilitar la sincronización de aplicaciones de Windows</p></td>
    <td align="left"><p>Esperar sincronización al iniciar la aplicación</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Configuración de retraso de importación</p></td>
    <td align="left"><p>Sincronizar aplicaciones de Windows no enumeradas</p></td>
    <td align="left"><p>Esperar sincronización al iniciar sesión</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Notificación de importación de configuración</p></td>
    <td align="left"><p>Dirección URL de contacto de ti</p></td>
    <td align="left"><p>Esperar el tiempo de espera de la sincronización</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Configuración ruta de almacenamiento</p></td>
    <td align="left"><p>Texto descriptivo de contacto de ti</p></td>
    <td align="left"><p>Ruta del catálogo de plantillas de configuración</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Habilitación de la sincronización</p></td>
    <td align="left"><p>Icono de bandeja habilitado</p></td>
    <td align="left"><p>Iniciar o detener el servicio del agente de UE-V</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Método de sincronización</p></td>
    <td align="left"><p>Notificación de primer uso</p></td>
    <td align="left"><p>Definir qué aplicaciones de Windows van a ser la configuración de itinerancia</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Tiempo de espera de sincronización</p></td>
    <td align="left"><p></p></td>
    <td align="left"><p></p></td>
    </tr>
    </tbody>
    </table>

     

-   Comprobar el cumplimiento mediante la confirmación de que se está ejecutando UE-V.

## Generar un elemento de configuración de directiva de UE-V Agent


Todas las directivas y la configuración de los agentes UE-V se distribuyen a través de un solo elemento de configuración que se genera con la herramienta UevAgentPolicyGenerator.exe. Esta herramienta lee la configuración deseada de un archivo de configuración XML y crea un CI que contiene la configuración de detección y corrección necesaria para que el equipo cumpla con las normas.

El archivo CAB del elemento de configuración de la Directiva UE-V Agent se crea con la herramienta de línea de comandos UevTemplateBaselineGenerator.exe, que tiene estos parámetros:

-   Código de sitio del sitio &lt;&gt;

-   &lt;Nombre &gt; de nombre opcional: el valor predeterminado es "UE-V Agent Policy" si no está presente

-   &lt;La descripción &gt; de PolicyDescription es opcional: Si no está presente, se proporciona una descripción

-   CabFilePath &lt; ruta de acceso completa del elemento de configuración. Archivo CAB&gt;

-   ConfigurationFile &lt; ruta de acceso completa del archivo XML de configuración del agente&gt;

**Nota:**  Puede que sea necesario cambiar la Directiva de ejecución de PowerShell para permitir que estas secuencias de comandos se ejecuten en su entorno. Realice estos pasos en la consola de Configuration Manager:

1.  Seleccionar ** &gt; &gt; propiedades de configuración de cliente de administración**

2.  En la pestaña **agente de usuario** , establezca la Directiva de ejecución de **PowerShell** para **omitir**

<a href="" id="create"></a>**Crear el primer elemento de configuración de directiva de UE-V**

1.  Copie el archivo de configuración de configuración predeterminado del directorio de instalación de UE-V config Pack en una ubicación visible para la consola de administración de ConfigMgr:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\AgentConfiguration.xml c:\<target path>
    ```

    El archivo de configuración predeterminado contiene cinco secciones:

    <a href="" id="computer-policy"></a>**Directiva de equipo**  
    Todas las configuraciones de nivel de equipo UE-V. El atributo DesiredState se puede

    -   **Establecer** que el valor se asigne en el registro

    -   **Borrar** para quitar la configuración

    -   **No administrados** para dejar el elemento de configuración en su estado actual

    No quitar líneas de esta sección. En su lugar, establezca el DesiredState en ' Unmanaged ' si no desea que Configuration Manager modifique los valores actuales o predeterminados.

    <a href="" id="currentcomputeruserpolicy"></a>**CurrentComputerUserPolicy**  
    Toda la configuración del nivel de usuario de UE-V. Estas entradas invalidan la configuración del equipo de un usuario. El atributo DesiredState se puede

    -   **Establecer** que el valor se asigne en el registro

    -   **Borrar** para quitar la configuración

    -   **No administrados** para dejar el elemento de configuración en su estado actual

    No quitar líneas de esta sección. En su lugar, establezca el DesiredState en ' Unmanaged ' si no desea que Configuration Manager modifique los valores actuales o predeterminados.

    <a href="" id="services"></a>**Servicios**  
    Las entradas de esta sección controlan la operación del servicio. El archivo de configuración predeterminado contiene una sola entrada para el UevAgentService. El atributo DesiredState se puede establecer en **Running** o **Stopped**.

    <a href="" id="windows8appscomputerpolicy"></a>**Windows8AppsComputerPolicy**  
    Toda la configuración de sincronización de aplicaciones de Windows en el nivel de equipo. A cada PackageFamilyName enumerado en esta sección se le puede asignar una DesiredState de

    -   **Habilitado** para que la configuración sea móvil

    -   **Deshabilitado** para evitar la configuración de itinerancia

    -   **Desactivado** para que se elimine la entrada del control UE-V

    Se pueden agregar líneas adicionales a esta sección basándose en la lista de aplicaciones de Windows instaladas que se pueden ver con el cmdlet de PowerShell GetAppxPackage.

    <a href="" id="windows8appscurrentcomputeruserpolicy"></a>**Windows8AppsCurrentComputerUserPolicy**  
    Es idéntico a la Windows8AppsComputerPolicy con una configuración que suplanta la configuración del equipo para un usuario individual.

2.  Edite el archivo de configuración cambiando los campos estado y valor que desee.

3.  Ejecute este comando en un equipo que ejecute la consola de administración de ConfigMgr:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevAgentPolicyGenerator.exe –Site ABC –CabFilePath "C:\MyCabFiles\UevPolicyItem.cab" –ConfigurationFile "c:\AgentConfiguration.xml"
    ```

4.  Importar el archivo CAB con la consola de ConfigMgr o la importación de PowerShell CMConfigurationItem

**Actualizar un elemento de configuración de directiva de UE-V**

1.  Edite el archivo de configuración cambiando los campos estado y valor que desee.

2.  Ejecute el comando del paso 3 en [crear el primer elemento de configuración de directiva de UE-V](#create). Si cambió el nombre con el parámetro PolicyName, asegúrese de que escribe el mismo nombre.

3.  Reimporte el archivo CAB. Se actualizará la versión de ConfigMgr.

## Generar una línea base de plantilla de UE-V
Las plantillas de UE-V se distribuyen con una línea base que contiene varios elementos de configuración. Cada elemento de configuración contiene los scripts de detección y corrección necesarios para instalar una plantilla de UE-V. La plantilla real UE-V se incrusta en el script de corrección para la distribución mediante la funcionalidad de elemento de configuración estándar.

La línea base de la plantilla UE-V se crea con la herramienta de línea de comandos UevTemplateBaselineGenerator.exe, que tiene estos parámetros:

-   Código de sitio del sitio &lt;&gt;

-   &lt;Nombre &gt; de BaselineName (opcional: el valor predeterminado es "UE-V template Distributing Baseline" si no está presente)

-   &lt;Descripción &gt; de BaselineDescription (opcional: se proporciona una descripción si no está presente)

-   &lt;Carpeta de plantillas de TemplateFolder UE-V&gt;

-   Registrar &lt; lista de archivos de plantilla separada por comas&gt;

-   Eliminar la &lt; lista de plantillas separadas por comas&gt;

-   CabFilePath &lt; ruta de acceso completa al archivo CAB de línea base que se va a generar&gt;

El resultado es un archivo CAB de línea base que está listo para importarlo a Configuration Manager. Si, en una fecha futura, actualiza o agrega una plantilla, puede volver a ejecutar el comando con el mismo nombre de línea base. Importar el archivo CAB genera actualizaciones de versión de CI en las plantillas modificadas.

### <a href="" id="create2"></a>Crear la primera línea base de la plantilla UE-V

1.  Cree un conjunto "maestro" de plantillas de UE-V en una ubicación de carpeta estable visible para el equipo que ejecuta la consola de administración de ConfigMgr. A medida que se agregan o se actualizan las plantillas, esta carpeta es el lugar donde se extraen para su distribución. La lista inicial de plantillas se puede copiar desde un equipo con UE-V instalado. La ubicación predeterminada de la plantilla es C:\\Archivos de Programa\\microsoft User Experience Virtualization\\Templates.

2.  Cree un archivo de text.bat donde pueda agregar el comando generador de plantillas. Esto es opcional, pero hará que la regeneración sea más sencilla si guarda los parámetros de comando.

3.  Agregue el comando y los parámetros al archivo. bat que generará la línea base. En el ejemplo siguiente se crea una línea base que distribuye el Bloc de notas y la calculadora:

    ``` syntax
    C:\Program Files (x86)\Microsoft User Experience Virtualization\ConfigPack\UevTemplateBaselineGenerator.exe –Site "ABC" –TemplateFolder "C:\ProductionUevTemplates" –Register "MicrosoftNotepad.xml, MicrosoftCalculator.xml" –CabFilePath "C:\MyCabFiles\UevTemplateBaseline.cab"
    ```

4.  Ejecute el archivo. bat para crear UevTemplateBaseline.cab listo para importarlo a Configuration Manager.

### Actualizar una línea base de la plantilla UE-V

El generador de plantillas usa la versión de la plantilla para determinar si se debe actualizar una plantilla. Si hace que una plantilla cambie y actualiza la versión, el generador de línea base compara la plantilla de la carpeta maestra con la plantilla contenida en el CI en el servidor de ConfigMgr. Si se encuentra una diferencia, la línea base generada y las versiones modificada de CI se actualizan.

Para distribuir una nueva plantilla del Bloc de notas, debe seguir estos pasos:

1.  Actualice la plantilla y la versión de la plantilla que se encuentran en el &lt; &gt; elemento de versión de la plantilla.

2.  Copie la plantilla en el directorio de plantillas maestras.

3.  Ejecute el comando en el archivo. bat que creó en el paso 3 en [crear la primera línea base de la plantilla UE-V](#create2).

4.  Importe el archivo CAB generado en ConfigMgr con la consola o importación de PowerShell-CMBaseline.

## Obtener el paquete de configuración de UE-V


El paquete de configuración de UE-V para Configuration Manager 2012 SP1 o versiones posteriores puede descargarse [aquí](https://go.microsoft.com/fwlink/?LinkId=317263).






## Temas relacionados


[Administrar configuraciones para UE-V 2.x](manage-configurations-for-ue-v-2x-new-uevv2.md)

 

 





