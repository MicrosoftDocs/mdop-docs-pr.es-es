---
title: Referencia de esquema de plantilla de aplicación para UE-V 2. x
description: Referencia de esquema de plantilla de aplicación para UE-V 2. x
author: dansimp
ms.assetid: be8735a5-6a3e-4b1f-ba14-2a3bc3e5a8b6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 03ff6eabae68f07c23d5977f901e6a90e292c6ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10827410"
---
# Referencia de esquema de plantilla de aplicación para UE-V 2. x


Virtualización de la experiencia del usuario de Microsoft (UE-V) 2,0, 2,1 y 2,1 SP1 use las plantillas de ubicación de configuración XML para definir la configuración de la aplicación de escritorio y la configuración de Windows que se capturan y aplican en UE-V. UE-V incluye un conjunto de plantillas de ubicación de configuración predeterminada. También puede crear plantillas de ubicación de configuración personalizadas con el generador de UE-V.

Un usuario avanzado puede personalizar el archivo XML para una plantilla de ubicación de configuración. En este tema se detalla la estructura XML de las plantillas de ubicación de configuración de UE-V 2,1 (SP1) y 2,0 y se proporcionan instrucciones para editar estos archivos.

## Referencia de esquema de plantilla de aplicación de UE-V 2,1 y 2,1 SP1


En esta sección se detalla la estructura XML de la plantilla de ubicación de configuración de UE-V 2,1 y 2,1 SP1 y se proporcionan instrucciones para editar este archivo.

### En esta sección

-   [Atributo de declaración y de codificación XML](#xml21)

-   [Espacio de nombres y elemento raíz](#namespace21)

-   [Tipos de datos](#data21)

-   [Elemento Name](#name21)

-   [Elemento ID](#id21)

-   [Elemento version](#version21)

-   [Elemento Author](#author21)

-   [Procesos y elemento de proceso](#processes21)

-   [Elemento Application](#application21)

-   [Elemento común](#common21)

-   [Elemento SettingsLocationTemplate](#settingslocationtemplate21)

-   [Apéndice: SettingsLocationTemplate. xsd](#appendix21)

### <a href="" id="xml21"></a>Atributo de declaración y de codificación XML

**Obligatorio: verdadero**

**Tipo: cadena**

La declaración XML debe especificar el atributo de versión XML 1,0 ( &lt; ? XML version = "1.0" &gt; ). Las plantillas de ubicación de configuración creadas por el generador de UE-V se guardan en la codificación UTF-8, aunque la codificación no se especifica explícitamente. Le recomendamos que incluya el atributo de codificación = "UTF-8" en este elemento como procedimiento recomendado. Todas las plantillas incluidas con el producto especifican también esta etiqueta (vea los documentos de la experiencia del usuario de%ProgramFiles%\\Microsoft Virtualization\\Templates por referencia). Por ejemplo:

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace21"></a>Espacio de nombres y elemento raíz

**Obligatorio: verdadero**

**Tipo: cadena**

UE-V usa el https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate espacio de nombres para todas las aplicaciones. SettingsLocationTemplate es el elemento raíz y contiene todos los demás elementos. SettingsLocationTemplate de referencia en todas las plantillas que usan esta etiqueta:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data21"></a>Tipos de datos

Estos son los tipos de datos para el esquema de la plantilla de aplicación UE-V.

<a href="" id="guid"></a>**GUID** GUID describe una expresión regular de identificador global único estándar con el formato "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {12} \ \}". Se usa en el elemento Filesetting\\Root\\KnownFolder para comprobar el formato de las carpetas conocidas.

<a href="" id="filenamestring"></a>**FilenameString** FilenameString se refiere al nombre de archivo de un proceso que se va a supervisar. Sus valores están restringidos por la función regex \ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /: \] +, (es decir, no pueden contener caracteres de barra invertida o asterisco o signo de interrogación; caracteres comodín, el carácter de canalización, el signo mayor que o menor que, la barra diagonal o los caracteres de dos puntos).

<a href="" id="idstring"></a>**IDString** IDString se refiere al valor de identificador de elementos de la aplicación, SettingsLocationTemplate y elementos comunes (se usa para describir conjuntos de aplicaciones que comparten una configuración común). Está restringido por el mismo Regex que FilenameString (\ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /:\]+).

<a href="" id="templateversion"></a>**TemplateVersion** TemplateVersion es un valor entero que se usa para describir la revisión de la plantilla de ubicación de configuración. Su valor puede oscilar entre 0 y 2147483647.

<a href="" id="empty"></a>**Vacío** Vacío hace referencia a un valor null. Se usa en Process\\ShellProcess para indicar que no hay ningún proceso para supervisar. Este valor no debe usarse en ninguna plantilla de aplicación.

<a href="" id="author"></a>**Autor** El tipo de datos autor es un tipo complejo que identifica al autor de una plantilla. Contiene dos elementos secundarios: **Name** y **email**. En el tipo de datos autor, el elemento nombre es obligatorio mientras que el elemento de correo electrónico es opcional. Este tipo se describe más detalladamente en el elemento SettingsLocationTemplate.

<a href="" id="range"></a>**Intervalo** Range define una clase Integer formada por dos elementos secundarios: **Minimum** y **Maximum**. Este tipo de datos se implementa en el tipo de datos ProcessVersion. Si se especifica, se deben incluir los valores mínimo y máximo.

<a href="" id="processversion"></a>**ProcessVersion** ProcessVersion define un tipo con cuatro elementos secundarios: **principal**, **secundario**, de **compilación**y de **revisión**. Este tipo de datos es utilizado por el elemento Process para rellenar sus valores ProductVersion y FileVersion. Los datos de este tipo son un valor de rango. El elemento secundario principal es obligatorio y el resto es opcional.

<a href="" id="architecture"></a>**Arquitectura** La arquitectura enumera dos valores posibles: **Win32** y **Win64**. Estos valores se usan para especificar la arquitectura de los procesos.

<a href="" id="process"></a>**Proceso** El tipo de datos proceso es un contenedor que se usa para describir los procesos que va a supervisar UE-V. Contiene seis elementos secundarios: **nombre de archivo**, **arquitectura**, **NombreProducto**, **FileDescription**, **ProductVersion**y **fileversion**. En esta tabla se detalla el tipo de datos respectivo de cada elemento:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Elemento</strong></p></td>
<td align="left"><p><strong>Tipo de datos</strong></p></td>
<td align="left"><p><strong>Mandatory</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>NombreDeArchivo</p></td>
<td align="left"><p>FilenameString</p></td>
<td align="left"><p>Verdadero</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Arquitectura</p></td>
<td align="left"><p>Arquitectura</p></td>
<td align="left"><p>Falso</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Falso</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Falso</p></td>
</tr>
<tr class="even">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>Falso</p></td>
</tr>
<tr class="odd">
<td align="left"><p>FileVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>Falso</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**Procesos** El tipo de datos processes representa un contenedor para una colección de uno o más elementos de proceso. Se admiten dos elementos secundarios en el tipo de secuencia procesos: **proceso** y **ShellProcess**. Proceso es un elemento de tipo proceso y ShellProcess es de tipo de datos vacío. Debe identificarse al menos un elemento en la secuencia.

<a href="" id="path"></a>**Ruta de acceso** La ruta de acceso la utiliza RegistrySetting y FileSetting para hacer referencia al registro y a las rutas de acceso de archivos. Este elemento admite dos atributos opcionales: **recursivo** y **DeleteIfNotFound**. Ambos valores se establecen en default = "false".

Recursivo indica que la ruta de acceso y todas las subcarpetas están incluidas para la configuración del archivo o que todas las claves del registro secundarias se incluyen para la configuración del registro. En ambos casos, todos los elementos del nivel actual se incluyen en los datos capturados. En el caso de un objeto FileSettings, todos los archivos de la carpeta especificada se incluyen en los datos capturados por UE-V, pero no se incluyen las carpetas. Para las rutas de registro, se capturan todos los valores de la ruta de acceso actual, pero no se capturan las claves de registro secundarias. En ambos casos, debe tenerse cuidado para evitar capturar grandes conjuntos de datos o un gran número de elementos.

El atributo DeleteIfNotFound quita la configuración de los datos de la ruta de almacenamiento de configuración del usuario. Esto puede ser conveniente en los casos en que la eliminación de esta configuración del paquete guardará una gran cantidad de espacio en disco en el servidor de archivos de la ruta de almacenamiento configuración.

<a href="" id="filemask"></a>**FileMask** FileMask especifica solo algunos tipos de archivo para la carpeta definida por la ruta de acceso. Por ejemplo, Path puede ser `C:\users\username\files` y FileMask podría ser `*.txt` incluir solo archivos de texto.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting representa un contenedor de valores y claves de registro, así como el comportamiento deseado asociado en la parte de UE-V Agent. En este tipo se definen cuatro elementos secundarios: **path**, **Name**, **Exclude**y una secuencia de los valores **path** y **Name**.

<a href="" id="filesetting"></a>**FileSetting** FileSetting contiene parámetros asociados con rutas de archivos y archivos. Se definen cuatro elementos secundarios: **raíz**, **ruta**, **FileMask**y **excluir**. La raíz es obligatoria y las demás son opcionales.

<a href="" id="settings"></a>**Configuración** Configuración es un contenedor de todas las opciones de configuración que se aplican a una plantilla determinada. Contiene instancias de las configuraciones Registry, File, SystemParameter y CustomAction descritas anteriormente. Además, también puede contener los siguientes elementos secundarios con comportamientos descritos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Elemento</strong></p></td>
<td align="left"><p><strong>Descripción</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Asincrónico</p></td>
<td align="left"><p>Los paquetes de configuración asincrónica se aplican sin bloquear el inicio de la aplicación para que se inicie la aplicación mientras se sigue aplicando la configuración. Esto es útil para las opciones de configuración que se pueden aplicar de forma asincrónica, como las que se aplican <code>get/set</code> a través de una API, como SystemParameterSetting.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>De forma predeterminada, UE-V solo guarda la configuración de una aplicación cuando se cierra la última instancia de una aplicación que usa la plantilla. Cuando este elemento se establece en ' false ', UE-V exporta la configuración incluso si se están ejecutando otras instancias de una aplicación. Plantillas adaptadas: aquellas que incluyen una sección de elementos comunes, que se envían con UE-V, usan este indicador para permitir que la configuración compartida se exporte siempre al cerrarse de la aplicación, evitando la configuración específica de la aplicación para que no se exporte hasta que se cierre la última instancia.</p></td>
</tr>
<tr class="even">
<td align="left"><p>AlwaysApplySettings</p></td>
<td align="left"><p>(introducido en 2,1)</p>
<p>Este parámetro fuerza la aplicación de un paquete de configuración importado aunque no existan diferencias entre el paquete y el estado actual de la aplicación. Este parámetro debe usarse solo en casos especiales, ya que puede ralentizar la importación de configuración.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name21"></a>Elemento Name

**Obligatorio: verdadero**

**Tipo: cadena**

Name especifica un nombre único para la plantilla de ubicación Settings. Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración. En general, Evite hacer referencia a la información de versión, ya que puede ser objeto del elemento ProductVersion. Por ejemplo, especifique `<Name>My Application</Name>` en lugar de `<Name>My Application 1.1</Name>` .

**Nota:**  UE-V no hace referencia a DTD externas, por lo que no es posible usar entidades con nombre en una plantilla de ubicación de configuración. Por ejemplo, no use &reg; el signo de marca comercial registrada®. En su lugar, use referencias numeradas canónicas para incluir estos tipos de caracteres especiales, por ejemplo, & \ #174 para el carácter®. Esta regla se aplica a todos los valores de cadena de este documento.

Consulte <http://www.w3.org/TR/xhtml1/dtds.html> para obtener una lista completa de las entidades de caracteres. Los documentos con codificación UTF-8 pueden incluir directamente los caracteres Unicode. Al guardar las plantillas mediante el generador de UE-V, se convierten las entidades de caracteres en representaciones Unicode automáticamente.

 

### <a href="" id="id21"></a>Elemento ID

**Obligatorio: verdadero**

**Tipo: cadena**

ID rellena un identificador único para una plantilla determinada. Esta etiqueta se convierte en el identificador principal que el agente de UE-V usa para hacer referencia a la plantilla en tiempo de ejecución (por ejemplo, consulte la salida de los cmdlets de PowerShell Get-UevTemplate y Get-UevTemplateProgram). Por Convención, esta etiqueta no debe contener espacios, lo que simplifica el scripting. Los números de versión de las aplicaciones deben especificarse en este elemento para permitir la identificación sencilla de la plantilla, como `<ID>MicrosoftCalculator6</ID>` o `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version21"></a>Elemento version

**Obligatorio: verdadero**

**Tipo: entero**

**Valor mínimo: 0**

**Valor máximo: 2147483647**

Versión identifica la versión de la plantilla de ubicación de configuración para el seguimiento administrativo de los cambios. El generador de UE-V incrementa automáticamente este número en uno cada vez que se guarda la plantilla. Observe que este campo debe ser un número entero entero; los valores fraccionarios, como, por ejemplo, `<Version>2.5</Version>` no están permitidos.

**Sugerencia:** Puede guardar las notas sobre los cambios de versión mediante etiquetas `<!-- -->` de comentario XML, por ejemplo:

```xml
  <!--
     Version History

     Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
     Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
     Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
     Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
   -->
  <Version>4</Version>
```

**Importante**  Se consulta este valor para determinar si se debe aplicar una nueva versión de una plantilla a una plantilla existente en estos casos:

-   Cuando se ejecuta la tarea de actualización automática de la plantilla programada

-   Cuando se ejecuta el cmdlet Update-UevTemplate de PowerShell

-   Cuando se llama al método Update microsoft\\uev: SettingsLocationTemplate mediante WMI

 

### <a href="" id="author21"></a>Elemento Author

**Obligatorio: falso**

**Tipo: cadena**

Autor identifica al creador de la plantilla de ubicación de configuración. Se admiten dos elementos secundarios opcionales: **nombre** y **correo electrónico**. Ambos atributos son opcionales, pero si se especifica el elemento secundario email, debe ir acompañado del elemento Name. Autor hace referencia al nombre completo del contacto para la plantilla de ubicación de configuración y el correo electrónico debe hacer referencia a una dirección de correo electrónico del autor. Le recomendamos que incluya esta información en las plantillas publicadas públicamente, por ejemplo, en la [Galería de plantillas de UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).

### <a href="" id="processes21"></a>Procesos y elemento de proceso

**Obligatorio: verdadero**

**Type: Element**

Procesos contiene al menos un `<Process>` elemento, que a su vez contiene los siguientes elementos secundarios **: nombre de archivo**, **arquitectura**, **NombreProducto**, **FileDescription**, **ProductVersion**y **fileversion**. El elemento secundario FILENAME es obligatorio y el resto es opcional. Un elemento completamente rellenado contiene etiquetas similares a este ejemplo:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### NombreDeArchivo

**Obligatorio: verdadero**

**Tipo: cadena**

Nombre de archivo se refiere al nombre de archivo real del ejecutable tal como aparece en el sistema de archivos. Este elemento especifica el criterio principal que UE-V usa para evaluar si una plantilla se aplica a un proceso o no. Este elemento debe especificarse en el XML de la plantilla de ubicación de configuración.

Los nombres de archivo válidos no deben coincidir con la expresión regular \ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /: \] +, es decir, no pueden contener caracteres de barra invertida, asterisco o signo de interrogación caracteres comodín, el carácter de barra vertical, el signo mayor que o menor que, o el signo de dos puntos (\ \? \* | &lt; &gt; /o: caracteres.).

**Sugerencia:** Para probar una cadena con este regex, use una ventana de comandos de PowerShell y sustituya el nombre de su archivo ejecutable por **YourFileName**:

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

Un valor de **true** indica que la cadena contiene caracteres ilegales. A continuación se muestran algunos ejemplos de valores ilegales:

-   \\\\server\\share\\program.exe

-   Programa \ *. exe

-   Pro? ram.exe

-   Programa &lt; 1 &gt; . exe

**Nota:**  El generador de UE-V codifica los caracteres mayor que y menor que, como &gt; y &lt; respectivamente.

 

En raras ocasiones, el valor del nombre de archivo no incluirá necesariamente la extensión. exe, pero debe especificarse como parte del valor. Por ejemplo, `<Filename>MyApplictication.exe</Filename>` debe especificarse en lugar de `<Filename>MyApplictication</Filename>` . En el segundo ejemplo no se aplica la plantilla al proceso si el nombre real del archivo ejecutable es "MyApplication.exe".

### Arquitectura

**Obligatorio: falso**

**Tipo: arquitectura (cadena)**

Arquitectura se refiere a la arquitectura de procesador para la que se compiló el ejecutable de destino. Los valores válidos son Win32 para las aplicaciones de 32 bits o Win64 para aplicaciones de 64 bits. Si está presente, esta etiqueta limita la aplicabilidad de la plantilla de ubicación de configuración a una arquitectura de aplicación determinada. Para obtener un ejemplo de esto, compare la experiencia de usuario de%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml y los archivos de MicrosoftOffice2010Win64.xml incluidos en UE-V. Esto es útil cuando las rutas relativas cambian entre diferentes versiones de un archivo ejecutable o si se han agregado o quitado parámetros de configuración al pasar de una arquitectura de procesador a otra.

Si este elemento está ausente, la plantilla de ubicación de configuración omite la arquitectura del proceso y se aplica a los procesos de 32 y 64 bits si se aplican el nombre de archivo y otros atributos.

**Nota:**  UE-V no admite procesadores ARM en esta versión.

 

### ProductName

**Obligatorio: falso**

**Tipo: cadena**

ProductName es un elemento opcional que se usa para identificar un producto con fines administrativos o de generación de informes. ProductName difiere de FILENAME en el que no hay restricciones de expresiones regulares en su valor. Esto permite comprender más fácilmente las descripciones de un proceso donde el nombre ejecutable puede no ser obvio. Por ejemplo:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**Obligatorio: falso**

**Tipo: cadena**

FileDescription es una etiqueta opcional que permite una descripción administrativa del archivo ejecutable. Este es un campo de texto sin formato y puede ser útil para distinguir varios ejecutables dentro de un paquete de software donde es necesario identificar la función del ejecutable.

Por ejemplo, en una aplicación adecuada podría ser útil proporcionar avisos sobre la función de dos ejecutables (MyApplication.exe y MyApplicationHelper.exe), tal como se muestra aquí:

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**Obligatorio: falso**

**Tipo: cadena**

ProductVersion hace referencia a las versiones principales y secundarias de los productos de un archivo, así como a un nivel de compilación y revisión. ProductVersion es un elemento opcional, pero, si se especifica, debe contener al menos el elemento secundario principal. El valor debe expresar un rango con el formato mínimo = "X" máximo = "Y" donde X e y son enteros. Los valores mínimos y máximos pueden ser idénticos.

Es posible que los elementos de versión de archivo y producto no estén especificados. De este modo, se convierte la plantilla "independiente de la versión", lo que significa que la plantilla se aplicará a todas las versiones del archivo ejecutable especificado.

**Ejemplo 1:**

Versión del producto: 1,0 especificada en el generador de UE-V genera el siguiente XML:

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**Ejemplo 2:**

Versión del archivo: 5.0.2.1000 especificada en el generador de UE-V genera el siguiente XML:

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**Ejemplo incorrecto 1: intervalo incompleto:**

Solo está presente el atributo Minimum. El valor máximo debe incluirse también en un rango.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**Ejemplo incorrecto 2: se especificó una menor sin el elemento principal:**

Solo está presente el elemento menor. También se debe incluir una mayor importancia.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### FileVersion

**Obligatorio: falso**

**Tipo: cadena**

FileVersion distingue entre la versión de lanzamiento de una aplicación publicada y los detalles internos de la compilación de un ejecutable de componente. Para la mayoría de las aplicaciones comerciales, estos números son idénticos. Cuando varían, la versión de producto de un archivo indica la identificación de la versión genérica de un archivo, mientras que la versión de archivo indica una compilación específica de un archivo (como en el caso de una revisión o una actualización). Esto identifica de forma única los archivos sin romper la lógica de detección.

Para determinar la versión del producto y la versión de archivo de un ejecutable en particular, haga clic con el botón derecho en el archivo en el explorador de Windows, seleccione Propiedades y, a continuación, haga clic en la pestaña detalles.

Incluir un elemento FileVersion para una aplicación permite una lógica de detección de ajuste más granular, pero no es necesario para la mayoría de las aplicaciones. La configuración del elemento de ProductVersion se comprueba en primer lugar y, a continuación, se comprueba la opción FileVersion. Se aplicará la configuración más restrictiva.

Los elementos secundarios y las reglas de sintaxis de la FileVersion son idénticos a los de ProductVersion.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application21"></a>Elemento Application

Aplicación es un contenedor de la configuración que se aplica a una aplicación en particular. Es una colección de los siguientes campos o tipos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Campo/tipo</strong></p></td>
<td align="left"><p><strong>Descripción</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Especifica un nombre único para la plantilla de ubicación de configuración. Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración. Para obtener más información, vea <a href="#name21" data-raw-source="[Name](#name21)"> nombre </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Rellena un identificador único para una plantilla determinada. Esta etiqueta se convierte en el identificador principal que usa el agente de UE-V para hacer referencia a la plantilla en tiempo de ejecución. Para obtener más información, consulte <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>Una descripción opcional de la plantilla.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nombre opcional que se muestra en la interfaz de usuario, adaptado por la configuración regional de un idioma.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Descripción de la plantilla opcional localizada por la configuración regional de un idioma.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Versión</p></td>
<td align="left"><p>Identifica la versión de la plantilla de ubicación de configuración para el seguimiento administrativo de los cambios. Para obtener más información, consulte <a href="#version21" data-raw-source="[Version](#version21)"> versión </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Controla si esta plantilla está habilitada junto con una cuenta de Microsoft o no. Si la sincronización de MSA está habilitada para un usuario en un equipo, esta plantilla se deshabilitará automáticamente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>De forma similar a MSA, esto controla si esta plantilla está habilitada junto con Office365. Si se usa Office 365 para sincronizar la configuración, esta plantilla se deshabilitará automáticamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (introducido en 2,1)</p></td>
<td align="left"><p>Especifica que esta plantilla solo se puede asociar con el perfil especificado dentro de este elemento y que no se puede cambiar mediante WMI o PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Procesos</p></td>
<td align="left"><p>Un contenedor para una colección de uno o varios elementos de proceso. Para obtener más información, consulte <a href="#processes21" data-raw-source="[Processes](#processes21)"> procesos </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuración</p></td>
<td align="left"><p>Un contenedor para todas las opciones de configuración que se aplican a una plantilla determinada. Contiene instancias de la configuración del registro, archivo, SystemParameter y CustomAction. Para obtener más información, vea <strong> configuración </strong> de los <a href="#data21" data-raw-source="[Data types](#data21)"> tipos de datos </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common21"></a>Elemento común

Common es similar a un elemento de la aplicación, pero siempre está asociado con dos o más elementos de la aplicación. La sección común representa el conjunto de opciones de configuración que se comparten entre las instancias de la aplicación. Es una colección de los siguientes campos o tipos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Campo/tipo</strong></p></td>
<td align="left"><p><strong>Descripción</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Especifica un nombre único para la plantilla de ubicación de configuración. Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración. Para obtener más información, vea <a href="#name21" data-raw-source="[Name](#name21)"> nombre </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Rellena un identificador único para una plantilla determinada. Esta etiqueta se convierte en el identificador principal que usa el agente de UE-V para hacer referencia a la plantilla en tiempo de ejecución. Para obtener más información, consulte <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>Una descripción opcional de la plantilla.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nombre opcional que se muestra en la interfaz de usuario, adaptado por la configuración regional de un idioma.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Descripción de la plantilla opcional localizada por la configuración regional de un idioma.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Versión</p></td>
<td align="left"><p>Identifica la versión de la plantilla de ubicación de configuración para el seguimiento administrativo de los cambios. Para obtener más información, consulte <a href="#version21" data-raw-source="[Version](#version21)"> versión </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Controla si esta plantilla está habilitada junto con una cuenta de Microsoft o no. Si la sincronización de MSA está habilitada para un usuario en un equipo, esta plantilla se deshabilitará automáticamente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>De forma similar a MSA, esto controla si esta plantilla está habilitada junto con Office365. Si se usa Office 365 para sincronizar la configuración, esta plantilla se deshabilitará automáticamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>FixedProfile (introducido en 2,1)</p></td>
<td align="left"><p>Especifica que esta plantilla solo se puede asociar con el perfil especificado dentro de este elemento y que no se puede cambiar mediante WMI o PowerShell.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuración</p></td>
<td align="left"><p>Un contenedor para todas las opciones de configuración que se aplican a una plantilla determinada. Contiene instancias de la configuración del registro, archivo, SystemParameter y CustomAction. Para obtener más información, vea <strong> configuración </strong> de los <a href="#data21" data-raw-source="[Data types](#data21)"> tipos de datos </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate21"></a>Elemento SettingsLocationTemplate

Este elemento define la configuración para una sola aplicación o un conjunto de aplicaciones.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Campo/tipo</strong></p></td>
<td align="left"><p><strong>Descripción</strong></p></td>
</tr>
<tr class="even">
<td align="left"><p>Name</p></td>
<td align="left"><p>Especifica un nombre único para la plantilla de ubicación de configuración. Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración. Para obtener más información, vea <a href="#name21" data-raw-source="[Name](#name21)"> nombre </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ID</p></td>
<td align="left"><p>Rellena un identificador único para una plantilla determinada. Esta etiqueta se convierte en el identificador principal que usa el agente de UE-V para hacer referencia a la plantilla en tiempo de ejecución. Para obtener más información, consulte <a href="#id21" data-raw-source="[ID](#id21)"> ID </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>Una descripción opcional de la plantilla.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nombre opcional que se muestra en la interfaz de usuario, adaptado por la configuración regional de un idioma.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Descripción de la plantilla opcional localizada por la configuración regional de un idioma.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix21"></a>Apéndice: SettingsLocationTemplate. xsd

Este es el archivo SettingsLocationTemplate. xsd que muestra sus elementos, elementos secundarios, atributos y parámetros:

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013A/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

    <xs:simpleType name="Guid">
        <xs:restriction base="xs:string">
            <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="FilenameString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="IDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="CompositeIDString">
        <xs:restriction base="xs:string">
            <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+([.][^\\\?\*\|&lt;&gt;/:.]+)?" />
        </xs:restriction>
    </xs:simpleType>

    <xs:simpleType name="TemplateVersion">
        <xs:restriction base="xs:integer">
            <xs:minInclusive value="0" />
            <xs:maxInclusive value="2147483647" />
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Empty">
        <xs:sequence/>
    </xs:complexType>

    <xs:complexType name="LocalizedString">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Locale" type="xs:string" use="required"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="LocalizedName">
        <xs:sequence>
            <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="LocalizedDescription">
        <xs:sequence>
            <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="ReplacedTemplates">
      <xs:sequence>
        <xs:element name="ID" type="CompositeIDString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Author">
        <xs:all>
            <xs:element name="Name" type="xs:string" minOccurs="1" />
            <xs:element name="Email" type="xs:string" minOccurs="0" />
        </xs:all>
    </xs:complexType>

    <xs:complexType name="Range">
        <xs:attribute name="Minimum" type="xs:integer" use="required"/>
        <xs:attribute name="Maximum" type="xs:integer" use="required"/>
    </xs:complexType>

    <xs:complexType name="ProcessVersion">
        <xs:sequence>
            <xs:element name="Major" type="Range" minOccurs="1" />
            <xs:element name="Minor" type="Range" minOccurs="0" />
            <xs:element name="Build" type="Range" minOccurs="0" />
            <xs:element name="Patch" type="Range" minOccurs="0" />
        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="Architecture">
        <xs:restriction base="xs:string">
            <xs:enumeration value="Win32"/>
            <xs:enumeration value="Win64"/>
        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Process">
        <xs:sequence>
            <xs:element name="Filename" type="FilenameString" minOccurs="1" />
            <xs:element name="Architecture" type="Architecture" minOccurs="0" />
            <xs:element name="ProductName" type="xs:string" minOccurs="0" />
            <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
            <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
            <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Processes">
        <xs:sequence>
            <xs:choice minOccurs="1">
                <xs:element name="Process" type="Process" />
                <xs:element name="ShellProcess" type="Empty" />
            </xs:choice>
            <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Path">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
                <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
            </xs:extension>
        </xs:simpleContent>
    </xs:complexType>

    <xs:complexType name="RegistrySetting">
        <xs:sequence>
            <xs:element name="Path" type="Path" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="FileSetting">
        <xs:sequence>

            <xs:element name="Root">
                <xs:complexType>
                    <xs:choice>
                        <xs:element name="KnownFolder" type="Guid" />
                        <xs:element name="RegistryEntry" type="xs:string" />
                        <xs:element name="EnvironmentVariable" type="xs:string" />
                    </xs:choice>
                </xs:complexType>
            </xs:element>

            <xs:element name="Path" minOccurs="0" type="Path" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

            <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="Path" type="Path" minOccurs="0" />
                        <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>

        </xs:sequence>
    </xs:complexType>

    <xs:simpleType name="CustomActionSetting">
        <xs:restriction base="xs:anyURI"/>
    </xs:simpleType>

    <xs:simpleType name="SystemParameterSetting">
        <xs:restriction base="xs:string">

            <!-- Accessibility parameters -->
            <xs:enumeration value="AccessTimeout"/>
            <xs:enumeration value="AudioDescription"/>
            <xs:enumeration value="ClientAreaAnimation"/>
            <xs:enumeration value="DisableOverlappedContent"/>
            <xs:enumeration value="FilterKeys"/>
            <xs:enumeration value="FocusBorderHeight"/>
            <xs:enumeration value="FocusBorderWidth"/>
            <xs:enumeration value="HighContrast"/>
            <xs:enumeration value="MessageDuration"/>
            <xs:enumeration value="MouseClickLock"/>
            <xs:enumeration value="MouseClickLockTime"/>
            <xs:enumeration value="MouseKeys"/>
            <xs:enumeration value="MouseSonar"/>
            <xs:enumeration value="MouseVanish"/>
            <xs:enumeration value="ScreenReader"/>
            <xs:enumeration value="ShowSounds"/>
            <xs:enumeration value="SoundSentry"/>
            <xs:enumeration value="StickyKeys"/>
            <xs:enumeration value="ToggleKeys"/>

            <!-- Input parameters -->
            <xs:enumeration value="Beep"/>
            <xs:enumeration value="BlockSendInputResets"/>
            <xs:enumeration value="DefaultInputLang"/>
            <xs:enumeration value="DoubleClickTime"/>
            <xs:enumeration value="DoubleClkHeight"/>
            <xs:enumeration value="DoubleClkWidth"/>
            <xs:enumeration value="KeyboardCues"/>
            <xs:enumeration value="KeyboardDelay"/>
            <xs:enumeration value="KeyboardPref"/>
            <xs:enumeration value="KeyboardSpeed"/>
            <xs:enumeration value="Mouse"/>
            <xs:enumeration value="MouseButtonSwap"/>
            <xs:enumeration value="MouseHoverHeight"/>
            <xs:enumeration value="MouseHoverTime"/>
            <xs:enumeration value="MouseHoverWidth"/>
            <xs:enumeration value="MouseSpeed"/>
            <xs:enumeration value="MouseTrails"/>
            <xs:enumeration value="SnapToDefButton"/>
            <xs:enumeration value="WheelScrollChars"/>
            <xs:enumeration value="WheelScrollLines"/>

            <!-- Desktop parameters (limited subset) -->
            <xs:enumeration value="DeskWallpaper"/>
            <xs:enumeration value="DesktopColor"/>

        </xs:restriction>
    </xs:simpleType>

    <xs:complexType name="Settings">
        <xs:sequence>
            <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
            <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
            <xs:element name="AlwaysApplySettings" type="xs:boolean" minOccurs="0" />
            <xs:choice minOccurs="0" maxOccurs="unbounded">
                <xs:element name="Registry" type="RegistrySetting" />
                <xs:element name="File" type="FileSetting" />
                <xs:element name="SystemParameter" type="SystemParameterSetting" />
                <xs:element name="CustomAction" type="CustomActionSetting" />
            </xs:choice>
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Common">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>

    <xs:complexType name="Application">
        <xs:sequence>
            <xs:element name="Name" type="xs:string" />
            <xs:element name="ID" type="IDString" />
            <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
            <xs:element name="Description" type="xs:string" minOccurs="0" />
            <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
            <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
            <xs:element name="Version" type="xs:integer" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
        </xs:sequence>
    </xs:complexType>


    <xs:element name="SettingsLocationTemplate">
        <xs:complexType>
            <xs:sequence>

                <xs:element name="Name" type="xs:string" />
                <xs:element name="ID" type="IDString" />
                <xs:element name="Description" type="xs:string" minOccurs="0" />
                <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
                <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

                <xs:choice>

                    <!-- Single application -->
                    <xs:sequence>
                        <xs:element name="ReplacedTemplates" type="ReplacedTemplates" minOccurs="0" />
                        <xs:element name="Version" type="TemplateVersion" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
                        <xs:element name="DeferToOffice365" type="Empty" minOccurs="0" />
                        <xs:element name="Processes" type="Processes" />
                        <xs:element name="Settings" type="Settings" />
                    </xs:sequence>

                    <!-- Suite of applications -->
                    <xs:sequence>
                        <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
                        <xs:element name="Author" type="Author" minOccurs="0" />
                        <xs:element name="FixedProfile" type="xs:string"  minOccurs="0" />
                        <xs:element name="Common" type="Common" />
                        <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
                    </xs:sequence>

                </xs:choice>

            </xs:sequence>
        </xs:complexType>
    </xs:element>
    <!-- SettingsLocationTemplate -->

</xs:schema>
```

## Referencia de esquema de la plantilla de aplicación UE-V 2,0


En esta sección se describe la estructura XML de la plantilla de ubicación de configuración de UE-V 2,0 y se proporcionan instrucciones para editar este archivo.

### En esta sección

-   [Atributo de declaración y de codificación XML](#xml)

-   [Espacio de nombres y elemento raíz](#namespace)

-   [Tipos de datos](#data)

-   [Elemento Name](#name)

-   [Elemento ID](#id)

-   [Elemento version](#version)

-   [Elemento Author](#author)

-   [Procesos y elemento de proceso](#processes)

-   [Elemento Application](#application)

-   [Elemento común](#common)

-   [Elemento SettingsLocationTemplate](#settingslocationtemplate)

-   [Apéndice: SettingsLocationTemplate. xsd](#appendix)

### <a href="" id="xml"></a>Atributo de declaración y de codificación XML

**Obligatorio: verdadero**

**Tipo: cadena**

La declaración XML debe especificar el atributo de versión XML 1,0 ( &lt; ? XML version = "1.0" &gt; ). Las plantillas de ubicación de configuración creadas por el generador de UE-V se guardan en la codificación UTF-8, aunque la codificación no se especifica explícitamente. Le recomendamos que incluya el atributo de codificación = "UTF-8" en este elemento como procedimiento recomendado. Todas las plantillas incluidas con el producto especifican también esta etiqueta (vea los documentos de la experiencia del usuario de%ProgramFiles%\\Microsoft Virtualization\\Templates por referencia). Por ejemplo:

`<?xml version="1.0" encoding="UTF-8"?>`

### <a href="" id="namespace"></a>Espacio de nombres y elemento raíz

**Obligatorio: verdadero**

**Tipo: cadena**

UE-V usa el https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate espacio de nombres para todas las aplicaciones. SettingsLocationTemplate es el elemento raíz y contiene todos los demás elementos. SettingsLocationTemplate de referencia en todas las plantillas que usan esta etiqueta:

`<SettingsLocationTemplate xmlns='https://schemas.microsoft.com/UserExperienceVirtualization/2012/SettingsLocationTemplate'>`

### <a href="" id="data"></a>Tipos de datos

Estos son los tipos de datos para el esquema de la plantilla de aplicación UE-V.

<a href="" id="guid"></a>**GUID** GUID describe una expresión regular de identificador global único estándar con el formato "\ \ {\ [a-fA-F0-9 \] {8} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {4} -\ [a-FA-F0-9 \] {12} \ \}". Se usa en el elemento Filesetting\\Root\\KnownFolder para comprobar el formato de las carpetas conocidas.

<a href="" id="filenamestring"></a>**FilenameString** FilenameString se refiere al nombre de archivo de un proceso que se va a supervisar. Sus valores están restringidos por la función regex \ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /: \] +, (es decir, no pueden contener caracteres de barra invertida o asterisco o signo de interrogación; caracteres comodín, el carácter de canalización, el signo mayor que o menor que, la barra diagonal o los caracteres de dos puntos).

<a href="" id="idstring"></a>**IDString** IDString se refiere al valor de identificador de elementos de la aplicación, SettingsLocationTemplate y elementos comunes (se usa para describir conjuntos de aplicaciones que comparten una configuración común). Está restringido por el mismo Regex que FilenameString (\ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /:\]+).

<a href="" id="templateversion"></a>**TemplateVersion** TemplateVersion es un valor entero que se usa para describir la revisión de la plantilla de ubicación de configuración. Su valor puede oscilar entre 0 y 2147483647.

<a href="" id="empty"></a>**Vacío** Vacío hace referencia a un valor null. Se usa en Process\\ShellProcess para indicar que no hay ningún proceso para supervisar. Este valor no debe usarse en ninguna plantilla de aplicación.

<a href="" id="author"></a>**Autor** El tipo de datos autor es un tipo complejo que identifica al autor de una plantilla. Contiene dos elementos secundarios: **Name** y **email**. En el tipo de datos autor, el elemento nombre es obligatorio mientras que el elemento de correo electrónico es opcional. Este tipo se describe más detalladamente en el elemento SettingsLocationTemplate.

<a href="" id="range"></a>**Intervalo** Range define una clase Integer formada por dos elementos secundarios: **Minimum** y **Maximum**. Este tipo de datos se implementa en el tipo de datos ProcessVersion. Si se especifica, se deben incluir los valores mínimo y máximo.

<a href="" id="processversion"></a>**ProcessVersion** ProcessVersion define un tipo con cuatro elementos secundarios: **principal**, **secundario**, de **compilación**y de **revisión**. Este tipo de datos es utilizado por el elemento Process para rellenar sus valores ProductVersion y FileVersion. Los datos de este tipo son un valor de rango. El elemento secundario principal es obligatorio y el resto es opcional.

<a href="" id="architecture"></a>**Arquitectura** La arquitectura enumera dos valores posibles: **Win32** y **Win64**. Estos valores se usan para especificar la arquitectura de los procesos.

<a href="" id="process"></a>**Proceso** El tipo de datos proceso es un contenedor que se usa para describir los procesos que va a supervisar UE-V. Contiene seis elementos secundarios: **nombre de archivo**, **arquitectura**, **NombreProducto**, **FileDescription**, **ProductVersion**y **fileversion**. En esta tabla se detalla el tipo de datos respectivo de cada elemento:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento</th>
<th align="left">Tipo de datos</th>
<th align="left">Mandatory</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>NombreDeArchivo</p></td>
<td align="left"><p>FilenameString</p></td>
<td align="left"><p>Verdadero</p></td>
</tr>
<tr class="even">
<td align="left"><p>Arquitectura</p></td>
<td align="left"><p>Arquitectura</p></td>
<td align="left"><p>Falso</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductName</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Falso</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileDescription</p></td>
<td align="left"><p>Cadena</p></td>
<td align="left"><p>Falso</p></td>
</tr>
<tr class="odd">
<td align="left"><p>ProductVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>Falso</p></td>
</tr>
<tr class="even">
<td align="left"><p>FileVersion</p></td>
<td align="left"><p>ProcessVersion</p></td>
<td align="left"><p>Falso</p></td>
</tr>
</tbody>
</table>

 

<a href="" id="processes"></a>**Procesos** El tipo de datos processes representa un contenedor para una colección de uno o más elementos de proceso. Se admiten dos elementos secundarios en el tipo de secuencia procesos: **proceso** y **ShellProcess**. Proceso es un elemento de tipo proceso y ShellProcess es de tipo de datos vacío. Debe identificarse al menos un elemento en la secuencia.

<a href="" id="path"></a>**Ruta de acceso** La ruta de acceso la utiliza RegistrySetting y FileSetting para hacer referencia al registro y a las rutas de acceso de archivos. Este elemento admite dos atributos opcionales: **recursivo** y **DeleteIfNotFound**. Ambos valores se establecen en default = "false".

Recursivo indica que la ruta de acceso y todas las subcarpetas están incluidas para la configuración del archivo o que todas las claves del registro secundarias se incluyen para la configuración del registro. En ambos casos, todos los elementos del nivel actual se incluyen en los datos capturados. En el caso de un objeto FileSettings, todos los archivos de la carpeta especificada se incluyen en los datos capturados por UE-V, pero no se incluyen las carpetas. Para las rutas de registro, se capturan todos los valores de la ruta de acceso actual, pero no se capturan las claves de registro secundarias. En ambos casos, debe tenerse cuidado para evitar capturar grandes conjuntos de datos o un gran número de elementos.

El atributo DeleteIfNotFound quita la configuración de los datos de la ruta de almacenamiento de configuración del usuario. Esto puede ser conveniente en los casos en que la eliminación de esta configuración del paquete guardará una gran cantidad de espacio en disco en el servidor de archivos de la ruta de almacenamiento configuración.

<a href="" id="filemask"></a>**FileMask** FileMask especifica solo algunos tipos de archivo para la carpeta definida por la ruta de acceso. Por ejemplo, Path puede ser `C:\users\username\files` y FileMask podría ser `*.txt` incluir solo archivos de texto.

<a href="" id="registrysetting"></a>**RegistrySetting** RegistrySetting representa un contenedor de valores y claves de registro, así como el comportamiento deseado asociado en la parte de UE-V Agent. En este tipo se definen cuatro elementos secundarios: **path**, **Name**, **Exclude**y una secuencia de los valores **path** y **Name**.

<a href="" id="filesetting"></a>**FileSetting** FileSetting contiene parámetros asociados con rutas de archivos y archivos. Se definen cuatro elementos secundarios: **raíz**, **ruta**, **FileMask**y **excluir**. La raíz es obligatoria y las demás son opcionales.

<a href="" id="settings"></a>**Configuración** Configuración es un contenedor de todas las opciones de configuración que se aplican a una plantilla determinada. Contiene instancias de las configuraciones Registry, File, SystemParameter y CustomAction descritas anteriormente. Además, también puede contener los siguientes elementos secundarios con comportamientos descritos:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Elemento</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Asincrónico</p></td>
<td align="left"><p>Los paquetes de configuración asincrónica se aplican sin bloquear el inicio de la aplicación para que se inicie la aplicación mientras se sigue aplicando la configuración. Esto es útil para las opciones de configuración que se pueden aplicar de forma asincrónica, como las que se aplican <code>get/set</code> a través de una API, como SystemParameterSetting.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PreventOverlappingSynchronization</p></td>
<td align="left"><p>De forma predeterminada, UE-V solo guarda la configuración de una aplicación cuando se cierra la última instancia de una aplicación que usa la plantilla. Cuando este elemento se establece en ' false ', UE-V exporta la configuración incluso si se están ejecutando otras instancias de una aplicación. Plantillas adaptadas: aquellas que incluyen una sección de elementos comunes, que se envían con UE-V, usan este indicador para permitir que la configuración compartida se exporte siempre al cerrarse de la aplicación, evitando la configuración específica de la aplicación para que no se exporte hasta que se cierre la última instancia.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="name"></a>Elemento Name

**Obligatorio: verdadero**

**Tipo: cadena**

Name especifica un nombre único para la plantilla de ubicación Settings. Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración. En general, Evite hacer referencia a la información de versión, ya que puede ser objeto del elemento ProductVersion. Por ejemplo, especifique `<Name>My Application</Name>` en lugar de `<Name>My Application 1.1</Name>` .

**Nota:**  UE-V no hace referencia a DTD externas, por lo que no es posible usar entidades con nombre en una plantilla de ubicación de configuración. Por ejemplo, no use &reg; el signo de marca comercial registrada®. En su lugar, use referencias numeradas canónicas para incluir estos tipos de caracteres especiales, por ejemplo, & \ #174 para el carácter®. Esta regla se aplica a todos los valores de cadena de este documento.

Consulte <http://www.w3.org/TR/xhtml1/dtds.html> para obtener una lista completa de las entidades de caracteres. Los documentos con codificación UTF-8 pueden incluir directamente los caracteres Unicode. Al guardar las plantillas mediante el generador de UE-V, se convierten las entidades de caracteres en representaciones Unicode automáticamente.

 

### <a href="" id="id"></a>Elemento ID

**Obligatorio: verdadero**

**Tipo: cadena**

ID rellena un identificador único para una plantilla determinada. Esta etiqueta se convierte en el identificador principal que el agente de UE-V usa para hacer referencia a la plantilla en tiempo de ejecución (por ejemplo, consulte la salida de los cmdlets de PowerShell Get-UevTemplate y Get-UevTemplateProgram). Por Convención, esta etiqueta no debe contener espacios, lo que simplifica el scripting. Los números de versión de las aplicaciones deben especificarse en este elemento para permitir la identificación sencilla de la plantilla, como `<ID>MicrosoftCalculator6</ID>` o `<ID>MicrosoftOffice2010Win64</ID>` .

### <a href="" id="version"></a>Elemento version

**Obligatorio: verdadero**

**Tipo: entero**

**Valor mínimo: 0**

**Valor máximo: 2147483647**

Versión identifica la versión de la plantilla de ubicación de configuración para el seguimiento administrativo de los cambios. El generador de UE-V incrementa automáticamente este número en uno cada vez que se guarda la plantilla. Observe que este campo debe ser un número entero entero; los valores fraccionarios, como, por ejemplo, `<Version>2.5</Version>` no están permitidos.

**Sugerencia:** Puede guardar las notas sobre los cambios de versión mediante etiquetas `<!-- -->` de comentario XML, por ejemplo:

```xml
<!--
    Version History

    Version 1 Jul 05, 2012 Initial template created by Generator - Denise@Contoso.com
    Version 2 Jul 31, 2012 Added support for app.exe v2.1.3 - Mark@Contoso.com
    Version 3 Jan 01, 2013 Added font settings support - Mark@Contoso.com
    Version 4 Jan 31, 2013 Added support for plugin settings - Tony@Contoso.com
  -->
<Version>4</Version>
```

**Importante**  Se consulta este valor para determinar si se debe aplicar una nueva versión de una plantilla a una plantilla existente en estos casos:

-   Cuando se ejecuta la tarea de actualización automática de la plantilla programada

-   Cuando se ejecuta el cmdlet Update-UevTemplate de PowerShell

-   Cuando se llama al método Update microsoft\\uev: SettingsLocationTemplate mediante WMI

 

### <a href="" id="author"></a>Elemento Author

**Obligatorio: falso**

**Tipo: cadena**

Autor identifica al creador de la plantilla de ubicación de configuración. Se admiten dos elementos secundarios opcionales: **nombre** y **correo electrónico**. Ambos atributos son opcionales, pero si se especifica el elemento secundario email, debe ir acompañado del elemento Name. Autor hace referencia al nombre completo del contacto para la plantilla de ubicación de configuración y el correo electrónico debe hacer referencia a una dirección de correo electrónico del autor. Le recomendamos que incluya esta información en las plantillas publicadas públicamente, por ejemplo, en la [Galería de plantillas de UE-V](https://gallery.technet.microsoft.com/site/search?f%5B0%5D.Type=RootCategory&f%5B0%5D.Value=UE-V).

### <a href="" id="processes"></a>Procesos y elemento de proceso

**Obligatorio: verdadero**

**Type: Element**

Procesos contiene al menos un `<Process>` elemento, que a su vez contiene los siguientes elementos secundarios **: nombre de archivo**, **arquitectura**, **NombreProducto**, **FileDescription**, **ProductVersion**y **fileversion**. El elemento secundario FILENAME es obligatorio y el resto es opcional. Un elemento completamente rellenado contiene etiquetas similares a este ejemplo:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <Architecture>Win64</Architecture>
  <ProductName> MyApplication </ProductName>
  <FileDescription>MyApplication.exe</FileDescription>
  <ProductVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="2" Maximum="2" />
    <Minor Minimum="0" Maximum="0" />
    <Build Minimum="0" Maximum="0" />
    <Patch Minimum="5" Maximum="5" />
  </FileVersion>
</Process>
```

### NombreDeArchivo

**Obligatorio: verdadero**

**Tipo: cadena**

Nombre de archivo se refiere al nombre de archivo real del ejecutable tal como aparece en el sistema de archivos. Este elemento especifica el criterio principal que UE-V usa para evaluar si una plantilla se aplica a un proceso o no. Este elemento debe especificarse en el XML de la plantilla de ubicación de configuración.

Los nombres de archivo válidos no deben coincidir con la expresión regular \ [^ \ \ \ \ \ \? \ \ \ * \ \ | &lt; &gt; /: \] +, es decir, no pueden contener caracteres de barra invertida, asterisco o signo de interrogación caracteres comodín, el carácter de barra vertical, el signo mayor que o menor que, o el signo de dos puntos (\ \? \* | &lt; &gt; /o: caracteres.).

**Sugerencia:** Para probar una cadena con este regex, use una ventana de comandos de PowerShell y sustituya el nombre de su archivo ejecutable por **YourFileName**:

`"YourFileName.exe" -match  "[\\\?\*\|<>/:]+"`

Un valor de **true** indica que la cadena contiene caracteres ilegales. A continuación se muestran algunos ejemplos de valores ilegales:

-   \\\\server\\share\\program.exe

-   Programa \ *. exe

-   Pro? ram.exe

-   Programa &lt; 1 &gt; . exe

**Nota:**  El generador de UE-V codifica los caracteres mayor que y menor que, como &gt; y &lt; respectivamente.

 

En raras ocasiones, el valor del nombre de archivo no incluirá necesariamente la extensión. exe, pero debe especificarse como parte del valor. Por ejemplo, `<Filename>MyApplictication.exe</Filename>` debe especificarse en lugar de `<Filename>MyApplictication</Filename>` . En el segundo ejemplo no se aplica la plantilla al proceso si el nombre real del archivo ejecutable es "MyApplication.exe".

### Arquitectura

**Obligatorio: falso**

**Tipo: arquitectura (cadena)**

Arquitectura se refiere a la arquitectura de procesador para la que se compiló el ejecutable de destino. Los valores válidos son Win32 para las aplicaciones de 32 bits o Win64 para aplicaciones de 64 bits. Si está presente, esta etiqueta limita la aplicabilidad de la plantilla de ubicación de configuración a una arquitectura de aplicación determinada. Para obtener un ejemplo de esto, compare la experiencia de usuario de%ProgramFiles%\\Microsoft Virtualization\\templates\\ MicrosoftOffice2010Win32.xml y los archivos de MicrosoftOffice2010Win64.xml incluidos en UE-V. Esto es útil cuando las rutas relativas cambian entre diferentes versiones de un archivo ejecutable o si se han agregado o quitado parámetros de configuración al pasar de una arquitectura de procesador a otra.

Si este elemento está ausente, la plantilla de ubicación de configuración omite la arquitectura del proceso y se aplica a los procesos de 32 y 64 bits si se aplican el nombre de archivo y otros atributos.

**Nota:**  UE-V no admite procesadores ARM en esta versión.

 

### ProductName

**Obligatorio: falso**

**Tipo: cadena**

ProductName es un elemento opcional que se usa para identificar un producto con fines administrativos o de generación de informes. ProductName difiere de FILENAME en el que no hay restricciones de expresiones regulares en su valor. Esto permite comprender más fácilmente las descripciones de un proceso donde el nombre ejecutable puede no ser obvio. Por ejemplo:

```xml
<Process>
  <Filename>MyApplication.exe</Filename>
  <ProductName>My Application 6.x by Contoso.com</ProductName>
  <ProductVersion>
    <Major Minimum="6" Maximum="6" />
  </ProductVersion>
</Process>
```

### FileDescription

**Obligatorio: falso**

**Tipo: cadena**

FileDescription es una etiqueta opcional que permite una descripción administrativa del archivo ejecutable. Este es un campo de texto sin formato y puede ser útil para distinguir varios ejecutables dentro de un paquete de software donde es necesario identificar la función del ejecutable.

Por ejemplo, en una aplicación adecuada podría ser útil proporcionar avisos sobre la función de dos ejecutables (MyApplication.exe y MyApplicationHelper.exe), tal como se muestra aquí:

```xml
<Processes>
  <Process>
    <Filename>MyApplication.exe</Filename>
    <FileDescription>My Application Main Engine</ FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
  <Process>
    <Filename>MyApplicationHelper.exe</Filename>
    <FileDescription>My Application Background Process Executable</FileDescription>
    <ProductVersion>
      <Major Minimum="6" Maximum="6" />
    </ProductVersion>
  </Process>
</Processes>
```

### ProductVersion

**Obligatorio: falso**

**Tipo: cadena**

ProductVersion hace referencia a las versiones principales y secundarias de los productos de un archivo, así como a un nivel de compilación y revisión. ProductVersion es un elemento opcional, pero, si se especifica, debe contener al menos el elemento secundario principal. El valor debe expresar un rango con el formato mínimo = "X" máximo = "Y" donde X e y son enteros. Los valores mínimos y máximos pueden ser idénticos.

Es posible que los elementos de versión de archivo y producto no estén especificados. De este modo, se convierte la plantilla "independiente de la versión", lo que significa que la plantilla se aplicará a todas las versiones del archivo ejecutable especificado.

**Ejemplo 1:**

Versión del producto: 1,0 especificada en el generador de UE-V genera el siguiente XML:

```xml
<ProductVersion>
  <Major Minimum="1" Maximum="1" />
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

**Ejemplo 2:**

Versión del archivo: 5.0.2.1000 especificada en el generador de UE-V genera el siguiente XML:

```xml
<FileVersion>
  <Major Minimum="5" Maximum="5" />
  <Minor Minimum="0" Maximum="0" />
  <Build Minimum="2" Maximum="2" />
  <Patch Minimum="1000" Maximum="1000" />
</FileVersion>
```

**Ejemplo incorrecto 1: intervalo incompleto:**

Solo está presente el atributo Minimum. El valor máximo debe incluirse también en un rango.

```xml
<ProductVersion>
  <Major Minimum="2" />
</ProductVersion>
```

**Ejemplo incorrecto 2: se especificó una menor sin el elemento principal:**

Solo está presente el elemento menor. También se debe incluir una mayor importancia.

```xml
<ProductVersion>
  <Minor Minimum="0" Maximum="0" />
</ProductVersion>
```

### FileVersion

**Obligatorio: falso**

**Tipo: cadena**

FileVersion distingue entre la versión de lanzamiento de una aplicación publicada y los detalles internos de la compilación de un ejecutable de componente. Para la mayoría de las aplicaciones comerciales, estos números son idénticos. Cuando varían, la versión de producto de un archivo indica la identificación de la versión genérica de un archivo, mientras que la versión de archivo indica una compilación específica de un archivo (como en el caso de una revisión o una actualización). Esto identifica de forma única los archivos sin romper la lógica de detección.

Para determinar la versión del producto y la versión de archivo de un ejecutable en particular, haga clic con el botón derecho en el archivo en el explorador de Windows, seleccione Propiedades y, a continuación, haga clic en la pestaña detalles.

Incluir un elemento FileVersion para una aplicación permite una lógica de detección de ajuste más granular, pero no es necesario para la mayoría de las aplicaciones. La configuración del elemento de ProductVersion se comprueba en primer lugar y, a continuación, se comprueba la opción FileVersion. Se aplicará la configuración más restrictiva.

Los elementos secundarios y las reglas de sintaxis de la FileVersion son idénticos a los de ProductVersion.

```xml
<Process>
  <Filename>MSACCESS.EXE</Filename>
  <Architecture>Win32</Architecture>
  <ProductVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </ProductVersion>
  <FileVersion>
    <Major Minimum="14" Maximum="14" />
    <Minor Minimum="0" Maximum="0" />
  </FileVersion>
</Process>
```

### <a href="" id="application"></a>Elemento Application

Aplicación es un contenedor de la configuración que se aplica a una aplicación en particular. Es una colección de los siguientes campos o tipos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo/tipo</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Especifica un nombre único para la plantilla de ubicación de configuración. Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración. Para obtener más información, vea <a href="#name" data-raw-source="[Name](#name)"> nombre </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Rellena un identificador único para una plantilla determinada. Esta etiqueta se convierte en el identificador principal que usa el agente de UE-V para hacer referencia a la plantilla en tiempo de ejecución. Para obtener más información, consulte <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>Una descripción opcional de la plantilla.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nombre opcional que se muestra en la interfaz de usuario, adaptado por la configuración regional de un idioma.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Descripción de la plantilla opcional localizada por la configuración regional de un idioma.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versión</p></td>
<td align="left"><p>Identifica la versión de la plantilla de ubicación de configuración para el seguimiento administrativo de los cambios. Para obtener más información, consulte <a href="#version" data-raw-source="[Version](#version)"> versión </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Controla si esta plantilla está habilitada junto con una cuenta de Microsoft o no. Si la sincronización de MSA está habilitada para un usuario en un equipo, esta plantilla se deshabilitará automáticamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>De forma similar a MSA, esto controla si esta plantilla está habilitada junto con Office365. Si se usa Office 365 para sincronizar la configuración, esta plantilla se deshabilitará automáticamente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Procesos</p></td>
<td align="left"><p>Un contenedor para una colección de uno o varios elementos de proceso. Para obtener más información, consulte <a href="#processes" data-raw-source="[Processes](#processes)"> procesos </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configuración</p></td>
<td align="left"><p>Un contenedor para todas las opciones de configuración que se aplican a una plantilla determinada. Contiene instancias de la configuración del registro, archivo, SystemParameter y CustomAction. Para obtener más información, vea <strong> configuración </strong> de los <a href="#data" data-raw-source="[Data types](#data)"> tipos de datos </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="common"></a>Elemento común

Common es similar a un elemento de la aplicación, pero siempre está asociado con dos o más elementos de la aplicación. La sección común representa el conjunto de opciones de configuración que se comparten entre las instancias de la aplicación. Es una colección de los siguientes campos o tipos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo/tipo</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Especifica un nombre único para la plantilla de ubicación de configuración. Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración. Para obtener más información, vea <a href="#name" data-raw-source="[Name](#name)"> nombre </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Rellena un identificador único para una plantilla determinada. Esta etiqueta se convierte en el identificador principal que usa el agente de UE-V para hacer referencia a la plantilla en tiempo de ejecución. Para obtener más información, consulte <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>Una descripción opcional de la plantilla.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nombre opcional que se muestra en la interfaz de usuario, adaptado por la configuración regional de un idioma.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Descripción de la plantilla opcional localizada por la configuración regional de un idioma.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Versión</p></td>
<td align="left"><p>Identifica la versión de la plantilla de ubicación de configuración para el seguimiento administrativo de los cambios. Para obtener más información, consulte <a href="#version" data-raw-source="[Version](#version)"> versión </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>DeferToMSAccount</p></td>
<td align="left"><p>Controla si esta plantilla está habilitada junto con una cuenta de Microsoft o no. Si la sincronización de MSA está habilitada para un usuario en un equipo, esta plantilla se deshabilitará automáticamente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>DeferToOffice365</p></td>
<td align="left"><p>De forma similar a MSA, esto controla si esta plantilla está habilitada junto con Office365. Si se usa Office 365 para sincronizar la configuración, esta plantilla se deshabilitará automáticamente.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Configuración</p></td>
<td align="left"><p>Un contenedor para todas las opciones de configuración que se aplican a una plantilla determinada. Contiene instancias de la configuración del registro, archivo, SystemParameter y CustomAction. Para obtener más información, vea <strong> configuración </strong> de los <a href="#data" data-raw-source="[Data types](#data)"> tipos de datos </a> .</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="settingslocationtemplate"></a>Elemento SettingsLocationTemplate

Este elemento define la configuración para una sola aplicación o un conjunto de aplicaciones.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Campo/tipo</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Name</p></td>
<td align="left"><p>Especifica un nombre único para la plantilla de ubicación de configuración. Se usa con fines de presentación al hacer referencia a la plantilla en WMI, PowerShell, visor de eventos y registros de depuración. Para obtener más información, vea <a href="#name" data-raw-source="[Name](#name)"> nombre </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>ID</p></td>
<td align="left"><p>Rellena un identificador único para una plantilla determinada. Esta etiqueta se convierte en el identificador principal que usa el agente de UE-V para hacer referencia a la plantilla en tiempo de ejecución. Para obtener más información, consulte <a href="#id" data-raw-source="[ID](#id)"> ID </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Descripción</p></td>
<td align="left"><p>Una descripción opcional de la plantilla.</p></td>
</tr>
<tr class="even">
<td align="left"><p>LocalizedNames</p></td>
<td align="left"><p>Nombre opcional que se muestra en la interfaz de usuario, adaptado por la configuración regional de un idioma.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>LocalizedDescriptions</p></td>
<td align="left"><p>Descripción de la plantilla opcional localizada por la configuración regional de un idioma.</p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="appendix"></a>Apéndice: SettingsLocationTemplate. xsd

Este es el archivo SettingsLocationTemplate. xsd que muestra sus elementos, elementos secundarios, atributos y parámetros:

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="UevSettingsLocationTemplate"
  targetNamespace="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  elementFormDefault="qualified"
  xmlns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:mstns="https://schemas.microsoft.com/UserExperienceVirtualization/2013/SettingsLocationTemplate"
  xmlns:xs="http://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="Guid">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="FilenameString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="IDString">
    <xs:restriction base="xs:string">
      <xs:pattern value="[^\\\?\*\|&lt;&gt;/:.]+" />
    </xs:restriction>
  </xs:simpleType>

  <xs:simpleType name="TemplateVersion">
    <xs:restriction base="xs:integer">
      <xs:minInclusive value="0" />
      <xs:maxInclusive value="2147483647" />
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Empty">
    <xs:sequence/>
  </xs:complexType>

  <xs:complexType name="LocalizedString">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Locale" type="xs:string" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="LocalizedName">
    <xs:sequence>
      <xs:element name="Name" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="LocalizedDescription">
    <xs:sequence>
      <xs:element name="Description" type="LocalizedString" minOccurs="1" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Author">
    <xs:all>
      <xs:element name="Name" type="xs:string" minOccurs="1" />
      <xs:element name="Email" type="xs:string" minOccurs="0" />
    </xs:all>
  </xs:complexType>

  <xs:complexType name="Range">
    <xs:attribute name="Minimum" type="xs:integer" use="required"/>
    <xs:attribute name="Maximum" type="xs:integer" use="required"/>
  </xs:complexType>

  <xs:complexType name="ProcessVersion">
    <xs:sequence>
      <xs:element name="Major" type="Range" minOccurs="1" />
      <xs:element name="Minor" type="Range" minOccurs="0" />
      <xs:element name="Build" type="Range" minOccurs="0" />
      <xs:element name="Patch" type="Range" minOccurs="0" />
    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="Architecture">
    <xs:restriction base="xs:string">
      <xs:enumeration value="Win32"/>
      <xs:enumeration value="Win64"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Process">
    <xs:sequence>
      <xs:element name="Filename" type="FilenameString" minOccurs="1" />
      <xs:element name="Architecture" type="Architecture" minOccurs="0" />
      <xs:element name="ProductName" type="xs:string" minOccurs="0" />
      <xs:element name="FileDescription" type="xs:string" minOccurs="0" />
      <xs:element name="ProductVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="FileVersion" type="ProcessVersion" minOccurs="0" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Processes">
    <xs:sequence>
      <xs:choice minOccurs="1">
        <xs:element name="Process" type="Process" />
        <xs:element name="ShellProcess" type="Empty" />
      </xs:choice>
      <xs:element name="Process" type="Process" minOccurs="0" maxOccurs="unbounded" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Path">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute name="Recursive" type="xs:boolean" default="false"/>
        <xs:attribute name="DeleteIfNotFound" type="xs:boolean" default="false"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="RegistrySetting">
    <xs:sequence>
      <xs:element name="Path" type="Path" />
      <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="Name" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="FileSetting">
    <xs:sequence>

      <xs:element name="Root">
        <xs:complexType>
          <xs:choice>
            <xs:element name="KnownFolder" type="Guid" />
            <xs:element name="RegistryEntry" type="xs:string" />
            <xs:element name="EnvironmentVariable" type="xs:string" />
          </xs:choice>
        </xs:complexType>
      </xs:element>

      <xs:element name="Path" minOccurs="0" type="Path" />
      <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>

      <xs:element name="Exclude" minOccurs="0" maxOccurs="unbounded">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Path" type="Path" minOccurs="0" />
            <xs:element name="FileMask" type="xs:string" minOccurs="0" maxOccurs="unbounded" />
          </xs:sequence>
        </xs:complexType>
      </xs:element>

    </xs:sequence>
  </xs:complexType>

  <xs:simpleType name="SystemParameterSetting">
    <xs:restriction base="xs:string">

      <!-- Accessibility parameters -->
      <xs:enumeration value="AccessTimeout"/>
      <xs:enumeration value="AudioDescription"/>
      <xs:enumeration value="ClientAreaAnimation"/>
      <xs:enumeration value="DisableOverlappedContent"/>
      <xs:enumeration value="FilterKeys"/>
      <xs:enumeration value="FocusBorderHeight"/>
      <xs:enumeration value="FocusBorderWidth"/>
      <xs:enumeration value="HighContrast"/>
      <xs:enumeration value="MessageDuration"/>
      <xs:enumeration value="MouseClickLock"/>
      <xs:enumeration value="MouseClickLockTime"/>
      <xs:enumeration value="MouseKeys"/>
      <xs:enumeration value="MouseSonar"/>
      <xs:enumeration value="MouseVanish"/>
      <xs:enumeration value="ScreenReader"/>
      <xs:enumeration value="ShowSounds"/>
      <xs:enumeration value="SoundSentry"/>
      <xs:enumeration value="StickyKeys"/>
      <xs:enumeration value="ToggleKeys"/>

      <!-- Input parameters -->
      <xs:enumeration value="Beep"/>
      <xs:enumeration value="BlockSendInputResets"/>
      <xs:enumeration value="DefaultInputLang"/>
      <xs:enumeration value="DoubleClickTime"/>
      <xs:enumeration value="DoubleClkHeight"/>
      <xs:enumeration value="DoubleClkWidth"/>
      <xs:enumeration value="KeyboardCues"/>
      <xs:enumeration value="KeyboardDelay"/>
      <xs:enumeration value="KeyboardPref"/>
      <xs:enumeration value="KeyboardSpeed"/>
      <xs:enumeration value="Mouse"/>
      <xs:enumeration value="MouseButtonSwap"/>
      <xs:enumeration value="MouseHoverHeight"/>
      <xs:enumeration value="MouseHoverTime"/>
      <xs:enumeration value="MouseHoverWidth"/>
      <xs:enumeration value="MouseSpeed"/>
      <xs:enumeration value="MouseTrails"/>
      <xs:enumeration value="SnapToDefButton"/>
      <xs:enumeration value="WheelScrollChars"/>
      <xs:enumeration value="WheelScrollLines"/>

      <!-- Desktop parameters (limited subset) -->
      <xs:enumeration value="DeskWallpaper"/>
      <xs:enumeration value="DesktopColor"/>

    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="Settings">
    <xs:sequence>
      <xs:element name="Asynchronous" type="xs:boolean" minOccurs="0" />
      <xs:element name="PreventOverlappingSynchronization" type="xs:boolean" minOccurs="0" />
      <xs:choice minOccurs="0" maxOccurs="unbounded">
        <xs:element name="Registry" type="RegistrySetting" />
        <xs:element name="File" type="FileSetting" />
        <xs:element name="SystemParameter" type="SystemParameterSetting" />
      </xs:choice>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Common">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="Application">
    <xs:sequence>
      <xs:element name="Name" type="xs:string" />
      <xs:element name="ID" type="IDString" />
      <xs:element name="Description" type="xs:string" minOccurs="0" />
      <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
      <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />
      <xs:element name="Version" type="xs:integer" />
      <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
      <xs:element name="Processes" type="Processes" />
      <xs:element name="Settings" type="Settings" />
    </xs:sequence>
  </xs:complexType>


  <xs:element name="SettingsLocationTemplate">
    <xs:complexType>
      <xs:sequence>

        <xs:element name="Name" type="xs:string" />
        <xs:element name="ID" type="IDString" />
        <xs:element name="Description" type="xs:string" minOccurs="0" />
        <xs:element name="LocalizedNames" type="LocalizedName" minOccurs="0" />
        <xs:element name="LocalizedDescriptions" type="LocalizedDescription" minOccurs="0" />

        <xs:choice>

          <!-- Single application -->
          <xs:sequence>
            <xs:element name="Version" type="TemplateVersion" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="DeferToMSAccount" type="Empty"  minOccurs="0" />
            <xs:element name="Processes" type="Processes" />
            <xs:element name="Settings" type="Settings" />
          </xs:sequence>

          <!-- Suite of applications -->
          <xs:sequence>
            <xs:element name="ManageSuiteOnly" type="xs:boolean" minOccurs="0" />
            <xs:element name="Author" type="Author" minOccurs="0" />
            <xs:element name="Common" type="Common" />
            <xs:element name="Application" type="Application" minOccurs="2" maxOccurs="unbounded" />
          </xs:sequence>

        </xs:choice>

      </xs:sequence>
    </xs:complexType>
  </xs:element>
  <!-- SettingsLocationTemplate -->

</xs:schema>
```






## Temas relacionados


[Trabajar con plantillas de UE-V 2. x personalizadas y el generador de UE-V 2. x](working-with-custom-ue-v-2x-templates-and-the-ue-v-2x-generator-new-uevv2.md)

[Referencia técnica de UE-V 2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





