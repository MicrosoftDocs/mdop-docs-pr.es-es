---
title: Implementación de Microsoft Office 2016 mediante el uso de App-V
description: Implementación de Microsoft Office 2016 mediante el uso de App-V
author: dansimp
ms.assetid: cc675cde-cb8d-4b7c-a700-6104b78f1d89
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 07/25/2017
ms.openlocfilehash: dfedab98e0bdf0a0d5f5e407d9bedadbbf56ad69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814622"
---
# Implementación de Microsoft Office 2016 mediante el uso de App-V


Use la información de este artículo para usar Microsoft Application Virtualization 5,0, o versiones posteriores, para ofrecer Microsoft Office 2016 como una aplicación virtualizada a los equipos de su organización. Para obtener información sobre cómo usar App-V para ofrecer Office 2013, consulte [implementar Microsoft office 2013 mediante App-v](deploying-microsoft-office-2013-by-using-app-v.md). Para obtener información sobre cómo usar App-V para ofrecer Office 2010, consulte [implementar Microsoft office 2010 mediante App-v](deploying-microsoft-office-2010-by-using-app-v.md).

Este tema contiene las siguientes secciones:

-   [Qué debe saber antes de empezar](#bkmk-before-you-start)

-   [Crear un paquete de Office 2016 para App-V con la herramienta de implementación de Office](#bkmk-create-office-pkg)

-   [Publicar el paquete de Office para App-V 5,0](#bkmk-pub-pkg-office)

-   [Personalizar y administrar paquetes de App-V de Office](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a>Qué debe saber antes de empezar


Antes de implementar Office 2016 mediante App-V, revise la siguiente información de planeación.

### <a href="" id="bkmk-supp-vers-coexist"></a>Versiones de Office compatibles y coexistencia de Office

Use la siguiente tabla para obtener información acerca de las versiones compatibles de Office y acerca de la ejecución de versiones coexistentes de Office.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Información para revisar</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Supported versions of Microsoft Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)">Versiones compatibles de Microsoft Office</a></p></td>
<td align="left"><ul>
<li><p>Versiones compatibles de Office</p></li>
<li><p>Tipos de implementación admitidos (por ejemplo, escritorio, infraestructura de escritorio virtual personal (VDI), VDI agrupada)</p></li>
<li><p>Opciones de licencia de Office</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with coexisting versions of Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)">Planificación para usar App-V con versiones coexistentes de Office</a></p></td>
<td align="left"><p>Consideraciones para instalar diferentes versiones de Office en el mismo equipo</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a>Requisitos de empaquetado, publicación e implementación

Antes de implementar Office con App-V, revise los siguientes requisitos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Requisitos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Empaquetado</p></td>
<td align="left">
<ul>
<li><p>Todas las aplicaciones de Office que desee implementar para los usuarios deben tener un único paquete.</p></li>
<li><p>En App-V 5,0 y versiones posteriores, debe usar la herramienta de implementación de Office para crear paquetes. No puede usar el secuenciador.</p></li>
<li><p>Si va a implementar Microsoft Visio 2016 y Microsoft Project 2016 junto con Office, debe incluirlos en el mismo paquete que Office. Para obtener más información, consulte <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2016 and Project 2016 with Office](#bkmk-deploy-visio-project)"> implementar Visio 2016 y Project 2016 con Office </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Publicación</p></td>
<td align="left"><ul>
<li><p>Solo puede publicar un paquete de Office en cada equipo cliente.</p></li>
<li><p>Debe publicar el paquete de Office globalmente. No puede publicar para el usuario.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Implementar cualquiera de los siguientes productos en un equipo compartido, por ejemplo, con servicios de escritorio remoto:</p>
<ul>
<li><p>Aplicaciones de Microsoft 365 para empresas</p></li>
<li><p>Visio Pro para Office 365</p></li>
<li><p>Project Pro para Office 365</p></li>
</ul></td>
<td align="left"><p>Debe habilitar la <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> activación en equipos compartidos </a> .</p>
</td>
</tr>
</tbody>
</table>



### Excluir aplicaciones de Office de un paquete

En la siguiente tabla se describen los métodos recomendados para excluir aplicaciones específicas de Office de un paquete.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Use la <strong> </strong> configuración ExcludeApp al crear el paquete con la herramienta de implementación de Office.</p></td>
<td align="left"><ul>
<li><p>Permite excluir determinadas aplicaciones de Office del paquete cuando la herramienta de implementación de Office crea el paquete. Por ejemplo, puede usar esta opción para crear un paquete que solo contenga Microsoft Word.</p></li>
<li><p>Para obtener más información, consulta <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> elemento ExcludeApp </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Modificar el archivo de DeploymentConfig.xml</p></td>
<td align="left"><ul>
<li><p>Modifique el archivo DeploymentConfig.xml después de que se haya creado el paquete. Este archivo contiene la configuración de paquete predeterminada para todos los usuarios de un equipo que ejecuta el cliente de App-V.</p></li>
<li><p>Para obtener más información, consulte <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2016 applications](#bkmk-disable-office-apps)"> deshabilitar aplicaciones de Office 2016 </a> .</p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a>Crear un paquete de Office 2016 para App-V con la herramienta de implementación de Office


Complete los pasos siguientes para crear un paquete de Office 2016 para App-V 5,0 o posterior.

>**Important** &nbsp; Importante &nbsp; En App-V 5,0 y versiones posteriores, debe usar la herramienta de implementación de Office para crear un paquete. No puede usar el secuenciador para crear paquetes.

### Revisar los requisitos previos para usar la herramienta de implementación de Office

El equipo en el que está instalando la herramienta de implementación de Office debe tener:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Como requisito previo</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Requisitos previos de software</p></td>
<td align="left"><p>.NET Framework 4</p></td>
</tr>
<tr class="even">
<td align="left"><p>Sistemas operativos compatibles</p></td>
<td align="left"><ul>
<li><p>versión de 64 bits de Windows 10</p></li>
<li><p>versión de 64 bits de Windows 8 o 8,1</p></li>
<li><p>versión de 64 bits de Windows 7</p></li>
</ul></td>
</tr>
</tbody>
</table>


>**Nota:**  En este tema, el término "paquete de aplicación de Office 2016" se refiere a licencias de suscripción.


### Crear paquetes de Office 2016 App-V con la herramienta de implementación de Office

Para crear paquetes de Office 2016 App-V, use la herramienta de implementación de Office. En las siguientes instrucciones se explica cómo crear un paquete de App-V de Office 2016 con licencias de suscripciones.

Crear paquetes de aplicación de Office 2016 en equipos Windows de 64 bits. Una vez creado, el paquete de Office 2016 App-V se ejecutará en equipos Windows 7, Windows 8,1 y Windows 10 de 32 bits y 64

### Descargar la herramienta de implementación de Office

Los paquetes de Office 2016 App-V se crean con la herramienta de implementación de Office, que genera un paquete de App-V de Office 2016. El paquete no se puede crear ni modificar mediante el secuenciador de App-V. Para comenzar la creación del paquete:

1.  Descargue la [herramienta de implementación de Office 2016 para hacer clic y ejecutar](https://www.microsoft.com/download/details.aspx?id=49117).

> **Importante** Debe usar la herramienta de implementación de Office 2016 para crear paquetes de App-V de Office 2016.
> 2. Ejecute el archivo. exe y extraiga sus características en la ubicación deseada. Para facilitar este proceso, puede crear una carpeta de red compartida donde se guardarán las características.

    Example: \\\\Server\\Office2016

3. Compruebe que exista un setup.exe y un archivo configuration.xml y que se encuentren en la ubicación que especificó.

### Descargar aplicaciones de Office 2016

Después de descargar la herramienta de implementación de Office, puede usarla para obtener las aplicaciones de Office 2016 más recientes. Después de obtener las aplicaciones de Office, cree el paquete de Office 2016 App-V.

El archivo XML incluido en la herramienta de implementación de Office especifica los detalles del producto, como los idiomas y las aplicaciones de Office incluidos.

1. **Personalizar el archivo de configuración XML de ejemplo:** Use el archivo de configuración XML de ejemplo que haya descargado con la herramienta de implementación de Office para personalizar las aplicaciones de Office:

   1. Abra el archivo XML de muestra en el Bloc de notas o su editor de texto preferido.

   2. Con el archivo de configuration.xml de ejemplo abierto y listo para editar, puede especificar productos, idiomas y la ruta de acceso en la que guarda las aplicaciones de Office 2016. A continuación se encuentra un ejemplo básico del archivo de configuration.xml:

      ```xml
      <Configuration>
         <Add SourcePath= "\\Server\Office2016” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      >**Nota:**  La configuración de XML es un archivo XML de ejemplo. El archivo incluye líneas con comentarios. Puede "Quitar comentarios" estas líneas para personalizar la configuración adicional con el archivo. Para "Quitar comentarios" de estas líneas, quite el "<! --"desde el principio de la línea y"--> "desde el final de la línea.

      El archivo de configuración XML anterior especifica que Office 2016 ProPlus 32-bit Edition, incluido Visio ProPlus, se descargará en inglés al \\\\server\\Office 2016, que es la ubicación donde se guardarán las aplicaciones de Office. Tenga en cuenta que el identificador de producto de las aplicaciones no afectará al final de la licencia de Office. Los paquetes de Office 2016 App-V con varias licencias se pueden crear a partir de las mismas aplicaciones mediante la especificación de licencias en una fase posterior. La tabla siguiente resume los atributos personalizables y los elementos del archivo XML:

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left">Entrada</th>
      <th align="left">Descripción</th>
      <th align="left">Ejemplo</th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p>Elemento Add</p></td>
      <td align="left"><p>Especifica los productos e idiomas que se van a incluir en el paquete.</p></td>
      <td align="left"><p>N/D</p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>OfficeClientEdition (atributo del elemento "Add")</p></td>
      <td align="left"><p>Especifica la edición de Office 2016 producto que se va a usar: 32 bits o 64 bits. Se produce un error en la operación si <strong> OfficeClientEdition </strong> no se establece en un valor válido.</p></td>
      <td align="left"><p><strong>OfficeClientEdition </strong> = &quot; 32&quot;</p>
      <p><strong>OfficeClientEdition </strong> = &quot; 64&quot;</p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p>Elemento Product</p></td>
      <td align="left"><p>Especifica la aplicación. El proyecto 2016 y Visio 2016 deben especificarse aquí como un producto agregado que se incluirá en las aplicaciones.

      Para obtener más información acerca de los identificadores de producto, consulte <a href="https://support.microsoft.com/kb/2842297" data-raw-source="[Product IDs that are supported by the Office Deployment Tool for Click-to-Run](https://support.microsoft.com/kb/2842297)"> identificadores de producto admitidos por la herramienta de implementación de Office para hacer clic y ejecutar</a>
      </p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      </td>
      </tr>
      <tr class="even">
      <td align="left"><p>Elemento de lenguaje</p></td>
      <td align="left"><p>Especifica el idioma admitido en las aplicaciones.</p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p>Version (atributo del elemento Add)</p></td>
      <td align="left"><p>Opcional. Especifica la compilación que se usará para el paquete.</p>
      <p>De forma predeterminada, es la compilación anunciada más reciente (según se define en v32.CAB en el origen de Office).</p></td>
      <td align="left"><p><code>16.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>SourcePath (atributo del elemento "Add")</p></td>
      <td align="left"><p>Especifica la ubicación en la que se guardarán las aplicaciones.</p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2016”</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>Canal (atributo del elemento "Add")</p></td>
      <td align="left"><p>Opcional. Especifica el canal de actualización del producto que desea descargar o instalar. </p><p>Para obtener más información sobre los canales de actualización, vea información general sobre los canales de actualización de las aplicaciones de Microsoft 365 para empresas.</p></td>
      <td align="left"><p><code>Channel=&quot;Deferred&quot;</code></p></td>
      </tr>
      </tbody>
      </table>

      Después de editar el archivo configuration.xml para especificar el producto, los idiomas y la ubicación en que se guardarán las aplicaciones de Office 2016, por ejemplo, puede guardar el archivo de configuración como Customconfig.xml.

2. **Descargue las aplicaciones en la ubicación especificada:** Use un símbolo del sistema con privilegios elevados y un sistema operativo de 64 bits para descargar las aplicaciones de Office 2016 que se convertirán más adelante en un paquete de App-V. A continuación se muestra un comando de ejemplo con una descripción de los detalles:

   ``` syntax
   \\server\Office2016\setup.exe /download \\server\Office2016\Customconfig.xml
   ```

   En el ejemplo:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>\server\Office2016</strong></p></td>
   <td align="left"><p>es la ubicación del recurso compartido de red que contiene la herramienta de implementación de Office y el archivo de Configuration.xml personalizado Customconfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Setup.exe</strong></p></td>
   <td align="left"><p>es la herramienta de implementación de Office.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>/Download</strong></p></td>
   <td align="left"><p>Descarga las aplicaciones de Office 2016 que especifique en el archivo customConfig.xml. Estos bits pueden convertirse más tarde en un paquete de App-V de Office 2016 con licencias por volumen.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>\server\Office2016\Customconfig.xml</strong></p></td>
   <td align="left"><p>pasa el archivo de configuración XML necesario para completar el proceso de descarga, en este ejemplo, customconfig.xml. Después de usar el comando de descarga, las aplicaciones de Office deberían encontrarse en la ubicación especificada en el archivo XML de configuración, en este ejemplo \Server\Office2016.</p></td>
   </tr>
   </tbody>
   </table>



### Convertir las aplicaciones de Office en un paquete de App-V

Después de descargar las aplicaciones de Office 2016 mediante la herramienta de implementación de Office, use la herramienta de implementación de Office para convertirlas en un paquete de App-V de Office 2016. Complete los pasos que correspondan al modelo de licencias.

**Resumen de lo que debe hacer:**

-   Crear los paquetes de App-V de Office 2016 en equipos Windows de 64 bits. Sin embargo, el paquete se ejecutará 32 en equipos con Windows 7, Windows 8 o 8,1 de 64 bits.

-   Cree un paquete de Office App-V para el paquete de licencias de suscripciones con la herramienta de implementación de Office y, a continuación, modifique el CustomConfig.xml archivo de configuración.

    En la siguiente tabla se resumen los valores que debe introducir en el archivo CustomConfig.xml del modelo de licencias que está usando. Los pasos que se indican en las secciones siguientes de la tabla especificarán las entradas exactas que tiene que hacer.

>**Nota:** &nbsp; &nbsp; Puede usar la herramienta de implementación de Office para crear paquetes de App-V para las aplicaciones de Microsoft 365 para empresas. No se admite la creación de paquetes para las versiones con licencia por volumen de Office Professional Plus o Office Standard.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Id. del producto</th>
<th align="left">Licencias de suscripciones</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Office 2016</strong></p></td>
<td align="left"><p>O365ProPlusRetail</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Office 2016 con Visio 2016</strong></p></td>
<td align="left"><p>O365ProPlusRetail</p>
<p>VisioProRetail</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Office 2016 con Visio 2016 y Project 2016</strong></p></td>
<td align="left"><p>O365ProPlusRetail</p>
<p>VisioProRetail</p>
<p>ProjectProRetail</p></td>
</tr>
</tbody>
</table>



**Cómo convertir las aplicaciones de Office en un paquete de App-V**

1. En el Bloc de notas, vuelva a abrir el archivo CustomConfig.xml y realice los cambios siguientes en el archivo:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Parámetro</th>
   <th align="left">Qué cambiar el valor a</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>RutaOrigen</p></td>
   <td align="left"><p>Apunte a las aplicaciones de Office descargadas anteriormente.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ProductID</p></td>
   <td align="left"><p>Especifique la licencia de la suscripción, como se muestra en el siguiente ejemplo:</p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2016&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p>En este ejemplo, se han realizado los cambios siguientes para crear un paquete con licencias de suscripciones:</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>RutaOrigen</strong></p></td>
   <td align="left"><p>es la ruta de acceso, que se cambió para que apunte a las aplicaciones de Office que se descargaron anteriormente.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Id. del producto</strong></p></td>
   <td align="left"><p>para Office se cambió a <code>O365ProPlusRetail</code> .</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Id. del producto</strong></p></td>
   <td align="left"><p>para Visio se cambió a <code>VisioProRetail</code> .</p></td>
   </tr>
   </tbody>
   </table>
   <p></p>
   <tr class="odd">
   <td align="left"><p>ExcludeApp (opcional)</p></td>
   <td align="left"><p>Le permite especificar programas de Office que no desea incluir en el paquete de App-V que crea la herramienta de implementación de Office. Por ejemplo, puede excluir Access e InfoPath.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>PACKAGEGUID (opcional)</p></td>
   <td align="left"><p>De forma predeterminada, todos los paquetes de App-V creados por la herramienta de implementación de Office comparten el mismo identificador de paquete de App-V. Puede usar PACKAGEGUID para especificar un identificador de paquete diferente para cada paquete, que le permite publicar varios paquetes de App-V, creados mediante la herramienta de implementación de Office, y administrarlos mediante el servidor de App-V.</p>
   <p>Un ejemplo de Cuándo usar este parámetro es crear paquetes diferentes para diferentes usuarios. Por ejemplo, puede crear un paquete con solo Office 2016 para algunos usuarios y crear otro paquete con Office 2016 y Visio 2016 para otro conjunto de usuarios.</p>
&gt;<strong>Nota </strong> aunque use identificadores de paquete únicos, aún puede implementar un solo paquete de App-V en un solo dispositivo.
   </td>
   </tr>
   </tbody>
   </table>



2. Use el comando/Packager para convertir las aplicaciones de Office en un paquete de App-V de Office 2016.

   Por ejemplo:

   ``` syntax
   \\server\Office2016\setup.exe /packager \\server\Office2016\Customconfig.xml  \\server\share\Office2016AppV
   ```

   En el ejemplo:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>\server\Office2016</strong></p></td>
   <td align="left"><p>es la ubicación del recurso compartido de red que contiene la herramienta de implementación de Office y el archivo de Configuration.xml personalizado Customconfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Setup.exe</strong></p></td>
   <td align="left"><p>es la herramienta de implementación de Office.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>/packager</strong></p></td>
   <td align="left"><p>crea el paquete de Office 2016 App-V con el tipo de licencia especificado en el archivo de customConfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>\server\Office2016\Customconfig.xml</strong></p></td>
   <td align="left"><p>pasa el archivo XML de configuración (en este caso customConfig) que se ha preparado para la fase de empaquetado.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>\server\share\Office 2016AppV</strong></p></td>
   <td align="left"><p>Especifica la ubicación del paquete de Office App-V recién creado.</p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2016 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note** To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. Compruebe que el paquete de Office 2016 App-V funciona correctamente:

   1.  Publique el paquete de App-V de Office 2016, creado globalmente, en un equipo de prueba y compruebe que aparecen los accesos directos de Office 2016.

   2.  Inicie algunas aplicaciones de Office 2016, como Excel o Word, para asegurarse de que el paquete funciona como se espera.

## <a href="" id="bkmk-pub-pkg-office"></a>Publicar el paquete de Office para App-V


Use la siguiente información para publicar un paquete de Office.

### Métodos para publicar paquetes de Office App-V

Implemente el paquete de App-V para Office 2016 con los mismos métodos que usa para cualquier otro paquete:

-   System Center Configuration Manager

-   Servidor de App-V

-   Independiente a través de los comandos de PowerShell

### Publicar requisitos y requisitos previos

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Requisito previo o requisito</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Habilitar scripting de PowerShell en los clientes de App-V</p></td>
<td align="left"><p>Para publicar paquetes de Office 2016, debe ejecutar un script.</p>
<p>Los scripts de paquetes están deshabilitados de forma predeterminada en los clientes de App-V. Para habilitar el scripting, ejecute el siguiente comando de PowerShell:</p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p>Publicar el paquete de Office 2016 globalmente</p></td>
<td align="left"><p>Los puntos de extensión del paquete de Office App-V requieren instalación en el nivel de equipo.</p>
<p>Al publicar en el nivel de un equipo, no es necesario realizar acciones previas ni redistribuibles, y el paquete de Office 2016 globalmente permite que sus aplicaciones funcionen como Office instalado de forma nativa, eliminando la necesidad de administradores para personalizar paquetes.</p></td>
</tr>
</tbody>
</table>



### Cómo publicar un paquete de Office

Ejecute el siguiente comando para publicar un paquete de Office de forma global:

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   Desde la consola de administración web en el servidor de App-V, puede Agregar permisos a un grupo de equipos en lugar de a un grupo de usuarios para permitir que los paquetes se publiquen globalmente en los equipos del grupo correspondiente.

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a>Personalizar y administrar paquetes de App-V de Office


Para administrar los paquetes de App-V de Office, use las mismas operaciones que usaría para cualquier otro paquete, pero hay algunas excepciones, como se describe en las secciones siguientes.

-   [Habilitar complementos de Office mediante grupos de conexión](#bkmk-enable-office-plugins)

-   [Deshabilitar aplicaciones de Office 2016](#bkmk-disable-office-apps)

-   [Deshabilitar los métodos abreviados de Office 2016](#bkmk-disable-shortcuts)

-   [Administración de actualizaciones de paquetes de Office 2016](#bkmk-manage-office-pkg-upgrd)

-   [Implementación de Visio 2016 y Project 2016 con Office](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a>Habilitar complementos de Office mediante grupos de conexión

Siga los pasos de esta sección para habilitar complementos de Office con su paquete de Office. Para usar complementos de Office, debe usar el secuenciador de App-V para crear un paquete independiente que contenga solo los complementos. No puede usar la herramienta de implementación de Office para crear el paquete de complementos. Después, cree un grupo de conexiones que contenga el paquete de Office y el paquete de complementos, tal y como se describe en los siguientes pasos.

**Para habilitar los complementos para los paquetes de Office App-V**

1.  Agregue un grupo de conexión a través de App-V Server, System Center Configuration Manager o un cmdlet de PowerShell.

2.  Ordene sus complementos con el secuenciador de App-V. Asegúrese de que Office 2016 está instalado en el equipo que se usa para secuenciar el complemento. Se recomienda usar las aplicaciones de Microsoft 365 para empresas (no virtuales) en el equipo de secuenciación al secuenciar los complementos de Office 2016.

3.  Crear un paquete de App-V que incluya los complementos que desee.

4.  Agregue un grupo de conexión a través de App-V Server, System Center Configuration Manager o un cmdlet de PowerShell.

5.  Agregue el paquete de aplicación de Office 2016 y el paquete de complementos que ha secuenciado al grupo de conexiones que ha creado.

    >**Importante** El orden de los paquetes en el grupo de conexión determina el orden en el que se fusiona el contenido del paquete. En el archivo descriptor de grupo de conexión, agregue en primer lugar el paquete de Office 2016 App-V y, a continuación, agregue el paquete de aplicación de complementos.



6.  Asegúrese de que ambos paquetes se publiquen en el equipo de destino y de que el paquete de complementos se publique globalmente para coincidir con la configuración global del paquete publicado de la aplicación de Office 2016.

7.  Compruebe que el archivo de configuración de implementación del paquete de complementos tiene la misma configuración que tiene el paquete de Office 2016 App-V.

    Dado que el paquete de Office 2016 App-V está integrado con el sistema operativo, la configuración del paquete de complementos debe coincidir. Puede buscar el archivo de configuración de implementación de "modo COM" y asegurarse de que el paquete de complementos tiene ese valor configurado como "integrado" y que tanto "InProcessEnabled" como "OutOfProcessEnabled" coinciden con la configuración del paquete de Office 2016 App-V publicado.

8.  Abra el archivo de configuración de la implementación y establezca el valor de los **objetos habilitados** en **falso**.

9.  Si ha realizado cambios en el archivo de configuración de la implementación después de la secuenciación, asegúrese de que el paquete de complemento se publique con el archivo.

10. Asegúrese de que el grupo de conexión que ha creado está habilitado en el equipo que desee. Es probable que el grupo de conexiones creado sea "pendiente" si el paquete de Office 2016 App-V está en uso cuando el grupo de conexión está habilitado. Si esto sucede, debe reiniciar para habilitar correctamente el grupo de conexiones.

11. Después de publicar correctamente ambos paquetes y habilitar el grupo de conexión, inicie la aplicación de Office 2016 de destino y compruebe que el complemento publicado y agregado al grupo de conexiones funciona como se espera.

### <a href="" id="bkmk-disable-office-apps"></a>Deshabilitar aplicaciones de Office 2016

Es posible que desee deshabilitar aplicaciones específicas en el paquete de Office App-V. Por ejemplo, puede deshabilitar el acceso, pero deje disponible el resto de la aplicación de Office Main. Al deshabilitar una aplicación, el usuario final ya no verá el acceso directo de esa aplicación. No es necesario volver a realizar la secuencia de la aplicación. Al cambiar el archivo de configuración de implementación una vez publicado el paquete de Office 2016 App-V, guardará los cambios, agregará el paquete de aplicación de Office 2016 y después lo volverá a publicar con el nuevo archivo de configuración de implementación para aplicar la nueva configuración a las aplicaciones de paquete de Office 2016 App-V.

>**Nota:** Para excluir determinadas aplicaciones de Office (por ejemplo, Access e InfoPath) al crear el paquete App-V con la herramienta de implementación de Office, use la configuración **ExcludeApp** .


**Para deshabilitar una aplicación de Office 2016**

1.  Abra un archivo de configuración de implementación con un editor de texto como **el Bloc de notas** y busque "aplicaciones".

2.  Busque la aplicación de Office que desea deshabilitar, por ejemplo, Access 2016.

3.  Cambie el valor de "habilitado" de "verdadero" a "falso".

4.  Guarde el archivo de configuración de implementación.

5.  Agregue el paquete Office 2016 App-V con el nuevo archivo de configuración de implementación.

    ```xml
    <Application Id="[{AppVPackageRoot}]\office16\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office16\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2016</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  Vuelva a agregar el paquete de Office 2016 App-V y, a continuación, vuelva a publicarlo con el nuevo archivo de configuración de implementación para aplicar la nueva configuración a las aplicaciones de paquete de Office 2016 App-V.

### <a href="" id="bkmk-disable-shortcuts"></a>Deshabilitar los métodos abreviados de Office 2016

Es posible que desee deshabilitar los métodos abreviados para determinadas aplicaciones de Office en lugar de anular la publicación o quitar el paquete. En el ejemplo siguiente se muestra cómo deshabilitar los métodos abreviados de Microsoft Access.

**Para deshabilitar los métodos abreviados de las aplicaciones de Office 2016**

1.  Abra un archivo de configuración de implementación en el Bloc de notas y busque "métodos abreviados".

2.  Para deshabilitar determinados métodos abreviados, elimine o comente los accesos directos específicos que no desee. Debe mantener el subsistema presente y habilitado. Por ejemplo, en el ejemplo siguiente, elimine los métodos abreviados de Microsoft Access, manteniendo intacto el método abreviado de subsistemas &lt; &gt; &lt; &gt; para deshabilitar el acceso directo de Microsoft Access.

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2016\Access 2016.lnk</File>
           <Target>[{AppvPackageRoot}])office16\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office16\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  Guarde el archivo de configuración de implementación.

4.  Vuelva a publicar el paquete de aplicación de Office 2016 con el nuevo archivo de configuración de implementación.

Muchas configuraciones adicionales se pueden cambiar con la modificación de la configuración de implementación para paquetes de App-V, por ejemplo, asociaciones de tipo de archivo, sistema de archivos virtual y más. Para obtener más información sobre cómo usar los archivos de configuración de implementación para cambiar la configuración de paquetes de App-V, consulte la sección recursos adicionales al final de este documento.

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a>Administración de actualizaciones de paquetes de Office 2016

Para actualizar un paquete de Office 2016, use la herramienta de implementación de Office. Para actualizar un paquete de Office 2016 implementado anteriormente, siga estos pasos.

**Cómo actualizar un paquete de Office 2016 implementado previamente**

1. Cree un nuevo paquete de Office 2016 mediante la herramienta de implementación de Office que usa el software de la aplicación Office 2016 más reciente. Los Office 2016 bits más recientes siempre pueden obtenerse a través de la fase de descarga de la creación de un paquete de App-V de Office 2016. El paquete de Office 2016 recién creado tendrá las actualizaciones más recientes y un nuevo identificador de versión. Todos los paquetes creados con la herramienta de implementación de Office tienen el mismo linaje.

   > **Nota:** Los paquetes de Office App-V tienen dos identificadores de versión:
   > <ul>
   > <li>Un identificador de versión de paquete de Office 2016 App-V que sea único en todos los paquetes creados con la herramienta de implementación de Office.</li>
   > <li>Un segundo identificador de versión de paquete de App-V, x. x. x, por ejemplo, en el manifiesto de AppX que solo cambiará si hay una nueva versión de Office. Por ejemplo, si hay disponible una nueva versión de Office 2016 con actualizaciones y se crea un paquete a través de la herramienta de implementación de Office para incorporar estas actualizaciones, el identificador de versión x. x. x cambiará para reflejar que la versión de Office en sí ha cambiado. El servidor de App-V usará el identificador de versión x. x. x. x para diferenciar este paquete y reconoceremos que contiene nuevas actualizaciones para el paquete publicado anteriormente, y, como resultado, la publicaremos como una actualización al paquete de Office 2016 existente.</li>
   > </ul>


2. Publique globalmente los paquetes de App-V de Office 2016 recién creados en equipos en los que desea aplicar las nuevas actualizaciones. Puesto que el nuevo paquete tiene el mismo linaje del paquete antiguo Office 2016 App-V, publicar el nuevo paquete con las actualizaciones solo aplicará los nuevos cambios en el paquete antiguo y, por lo tanto, será rápido.

3. Las actualizaciones se aplicarán de la misma manera que cualquier paquete de App-V publicado globalmente. Debido a que es probable que las aplicaciones estén en uso, las actualizaciones pueden retrasarse hasta que se reinicie el equipo.


### <a href="" id="bkmk-deploy-visio-project"></a>Implementación de Visio 2016 y Project 2016 con Office

En la tabla siguiente se describen los requisitos y las opciones para implementar Visio 2016 y Project 2016 con Office.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Detalles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>¿Cómo se empaquetan y publican Visio 2016 y Project 2016 con Office?</p></td>
<td align="left"><p>Debe incluir Visio 2016 y el proyecto 2016 en el mismo paquete de Office.</p>
<p>Si no está implementando Office, puede crear un paquete que contenga Visio o Project, siempre y cuando siga los requisitos de empaquetado, publicación e implementación descritos en este tema.</p></td>
</tr>
<tr class="even">
<td align="left"><p>¿Cómo puedo implementar Visio 2016 y Project 2016 en usuarios específicos?</p></td>
<td align="left"><p>Use uno de los métodos siguientes:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Si desea...</th>
<th align="left">... después, use este método</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Crear dos paquetes diferentes e implementar cada uno en un grupo de usuarios diferente</p></td>
<td align="left"><p>Cree e implemente los siguientes paquetes:</p>
<ul>
<li><p>Paquete que contiene solo Office-implementar en equipos cuyos usuarios solo necesitan Office.</p></li>
<li><p>Un paquete que contiene Office, Visio y Project-implementar en equipos cuyos usuarios necesitan las tres aplicaciones.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Si desea solo un paquete para toda la organización o si tiene usuarios que comparten equipos:</p></td>
<td align="left"><p>Siga estos pasos:</p>
<ol>
<li><p>Cree un paquete que contenga Office, Visio y Project.</p></li>
<li><p>Implementar el paquete para todos los usuarios.</p></li>
<li><p>Use <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> para evitar que usuarios específicos usen Visio y Project.</p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## Recursos adicionales


[Implementación de Microsoft Office 2013 mediante el uso de App-V](deploying-microsoft-office-2013-by-using-app-v.md)

[Implementación de Microsoft Office 2010 mediante el uso de App-V](deploying-microsoft-office-2010-by-using-app-v.md)

[Herramienta de implementación de Office 2016 para hacer clic y ejecutar](https://www.microsoft.com/download/details.aspx?id=49117)

**Grupos de conexión**

[Implementación de grupos de conexión en Microsoft App-V V5](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[Administración de grupos de conexión](managing-connection-groups.md)

**Configuración dinámica**

[Acerca de la configuración dinámica de App-V 5.1](about-app-v-51-dynamic-configuration.md)





