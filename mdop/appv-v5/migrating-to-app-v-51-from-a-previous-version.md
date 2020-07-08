---
title: Migrar a App-V 5.1 desde una versión anterior
description: Migrar a App-V 5.1 desde una versión anterior
author: dansimp
ms.assetid: e7ee0edc-7544-4c0a-aaca-d922a33bc1bb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb6ddbfed4f6fd1ae9613d2ee86361a51918a65
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813551"
---
# Migrar a App-V 5.1 desde una versión anterior


Con Microsoft Application Virtualization (App-V) 5,1, puede migrar la infraestructura de App-v 4,6 o App-V 5,0 existente a la infraestructura más flexible, integrada y más fácil de administrar de App-V 5,1.
Sin embargo, no puede migrar directamente de App-V 4. x a App-V 5,1, debe migrar a App-V 5,0 en primer lugar. Para obtener más información sobre cómo migrar de App-V 4. x a App-V 5,0, consulte [migrar desde una versión anterior](migrating-from-a-previous-version-app-v-50.md)  

**Nota:**  Los paquetes de App-V 5,1 son exactamente iguales a los de App-V 5,0. No se ha realizado ningún cambio en el formato de paquete entre las versiones y, por lo tanto, no es necesario convertir los paquetes de App-V 5,0 en paquetes de App-V 5,1.

Para obtener más información sobre las diferencias entre App-V 4,6 y App-V 5,1, consulte las **diferencias entre App-v 4,6 y la sección App-v 5,0** de [acerca de App-v 5,0](about-app-v-50.md).

 

## <a href="" id="bkmk-pkgconvimprove"></a>Mejoras en el convertidor de paquetes de App-V 5,1


Ahora puede usar el convertidor de paquetes para convertir paquetes de App-V 4,6 que contienen scripts y la información del registro y scripts de los archivos. OSD de origen se incluyen ahora en la salida del convertidor de paquetes.

También puede usar el `–OSDsToIncludeInPackage` parámetro con el `ConvertFrom-AppvLegacyPackage` cmdlet para especificar la información de los archivos. OSD que se convierte y se coloca en el nuevo paquete.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nuevo en App-V 5,1</th>
<th align="left">Antes de la aplicación-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Los archivos. XML nuevos se crean correspondientes a los archivos. OSD asociados a un paquete. Estos archivos incluyen la siguiente información:</p>
<ul>
<li><p>variables de entorno</p></li>
<li><p>abreviados</p></li>
<li><p>asociaciones de tipo de archivo</p></li>
<li><p>información del registro</p></li>
<li><p>scripts</p></li>
</ul>
<p>Ahora puede elegir agregar información de un subconjunto de los archivos. OSD en el directorio de origen al paquete mediante el <code>-OSDsToIncludeInPackage</code> parámetro.</p></td>
<td align="left"><p>La información del registro y los scripts incluidos en los archivos. OSD asociados a un paquete no se incluyeron en la salida del convertidor de paquetes.</p>
<p>El convertidor de paquetes rellenará el nuevo paquete con información de todos los archivos. OSD en el directorio de origen.</p></td>
</tr>
</tbody>
</table>

 

### Ejemplo de instrucción de conversión

Para comprender el nuevo proceso, revise el siguiente ejemplo de la `ConvertFrom-AppvLegacyPackage` instrucción del convertidor de paquetes.

**Si el directorio de origen (\\\\OldPkgStore\\ContosoApp) incluye lo siguiente:**

-   ContosoApp. SFT

-   ContosoApp.msi

-   ContosoApp. SPRJ

-   ContosoApp\_manifest.xml

-   X. OSD

-   Y. OSD

-   Z. OSD

**Y ejecuta este comando:**

``` syntax
ConvertFrom-AppvLegacyPackage –SourcePath \\OldPkgStore\ContosoApp\ 
-DestinationPath \\NewPkgStore\ContosoApp\
-OSDsToIncludeInPackage X.osd,Y.osd
```

**Se crea lo siguiente en el directorio de destino (\\\\NewPkgStore\\ContosoApp):**

-   ContosoApp. appv

-   ContosoApp.msi

-   ContosoApp\_DeploymentConfig.xml

-   ContosoApp\_UserConfig.xml

-   X\_Config.xml

-   Y\_Config.xml

-   Z\_Config.xml

**En el ejemplo anterior:**

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Estos archivos de directorio de origen...</th>
<th align="left">... se convierten en estos archivos de directorio de destino...</th>
<th align="left">... y contendrá estos elementos</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><ul>
<li><p>X. OSD</p></li>
<li><p>Y. OSD</p></li>
<li><p>Z. OSD</p></li>
</ul></td>
<td align="left"><ul>
<li><p>X_Config.xml</p></li>
<li><p>Y_Config.xml</p></li>
<li><p>Z_Config.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Variables de entorno</p></li>
<li><p>Abreviados</p></li>
<li><p>Asociaciones de tipo de archivo</p></li>
<li><p>Información del registro</p></li>
<li><p>Scripts</p></li>
</ul></td>
<td align="left"><p>Cada archivo. OSD se convierte en un archivo. xml independiente y correspondiente que contiene los elementos que se enumeran aquí en el formato de configuración de implementación de App-V 5,1. Estos elementos se pueden copiar desde estos archivos. XML y colocarlos en la configuración de implementación o los archivos de configuración de usuario según sea necesario.</p>
<p>En este ejemplo, hay tres archivos. XML, que corresponden a los tres archivos. OSD del directorio de origen. Cada archivo. xml contiene las variables de entorno, los accesos directos, las asociaciones de tipos de archivo, la información del registro y las secuencias de comandos en su archivo. OSD correspondiente.</p></td>
</tr>
<tr class="even">
<td align="left"><ul>
<li><p>X. OSD</p></li>
<li><p>Y. OSD</p></li>
</ul></td>
<td align="left"><ul>
<li><p>ContosoApp. appv</p></li>
<li><p>ContosoApp_DeploymentConfig.xml</p></li>
<li><p>ContosoApp_UserConfig.xml</p></li>
</ul></td>
<td align="left"><ul>
<li><p>Variables de entorno</p></li>
<li><p>Abreviados</p></li>
<li><p>Asociaciones de tipo de archivo</p></li>
</ul></td>
<td align="left"><p>La información de los archivos. OSD especificados en el <code>-OSDsToIncludeInPackage</code> parámetro se convierten y se colocan dentro del paquete. A continuación, el convertidor rellena el archivo de configuración de implementación y el archivo de configuración de usuario con el contenido del paquete, del mismo modo que el secuenciador de App-V realiza al secuenciar un nuevo paquete.</p>
<p>En este ejemplo, las variables de entorno, los accesos directos y las asociaciones de tipo de archivo incluidos en X. OSD e y. OSD se han convertido y colocado en el paquete de App-V, y parte de esta información también se incluyó en la configuración de implementación y en los archivos de configuración de usuario. X. OSD e y. OSD se usaron porque se incluyeron como argumentos para el <code>-OSDsToIncludeInPackage</code> parámetro. No se incluyó información de Z. OSD en el paquete porque no se incluyó como uno de estos argumentos.</p></td>
</tr>
</tbody>
</table>

 

## Conversión de paquetes creados con una versión anterior de App-V


Use la utilidad de conversión de paquetes para actualizar paquetes de aplicaciones virtuales creados con versiones de App-V anteriores a App-V 5,0. El convertidor de paquetes usa PowerShell para convertir paquetes y puede ayudar a automatizar el proceso si tiene muchos paquetes que requieren conversión.

**Importante**  Después de convertir un paquete existente, debe probar el paquete antes de implementar el paquete para asegurarse de que el proceso de conversión se realizó correctamente.

 

**Qué debe saber antes de convertir paquetes existentes**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Problema</th>
<th align="left">Solución alternativa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Los paquetes virtuales que usan DSC no se vinculan después de la conversión.</p></td>
<td align="left"><p>Vincule los paquetes usando grupos de conexión. Consulte <a href="managing-connection-groups51.md" data-raw-source="[Managing Connection Groups](managing-connection-groups51.md)"> Administración de grupos de conexión </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Los conflictos de variables de entorno se detectan durante la conversión.</p></td>
<td align="left"><p>Resuelva los conflictos en el <strong> archivo. OSD asociado </strong> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Las rutas de código no modificables se detectan durante la conversión.</p></td>
<td align="left"><p>Las rutas de código no modificables son difíciles de convertir correctamente. El convertidor de paquetes detectará y devolverá paquetes con archivos que contienen rutas de código no modificables. Visualice el archivo con la ruta de acceso del código y determine si el paquete necesita el archivo. En ese caso, se recomienda volver a crear el paquete.</p></td>
</tr>
</tbody>
</table>

 

Al convertir un paquete, comprobar si hay errores en los archivos o en los accesos directos. Busque el elemento en el paquete de App-V 4,6. Puede ser una ruta de acceso no modificable. Convertir la ruta de acceso.

**Nota:**  Se recomienda usar el secuenciador App-V 5,1 para convertir aplicaciones críticas o aplicaciones que necesiten aprovechar las características. Vea [Cómo secuenciar una nueva aplicación con App-V 5,1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md).

Si un paquete convertido no se abre después de convertirlo, también se recomienda que vuelva a realizar la secuencia de la aplicación con el secuenciador de aplicaciones-V 5,1.

 

[Cómo convertir un paquete creado en una versión anterior de App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

## Migrar clientes


En la tabla siguiente se muestra el método recomendado para actualizar clientes.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Actualizar el entorno a la versión más reciente de App-V 4.6</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Implementación de virtualización de aplicaciones y consideraciones de actualización </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Instale el cliente de App-V 5,1 con la coexistencia habilitada.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md" data-raw-source="[How to Deploy the App-V 4.6 and the App-V 5.1 Client on the Same Computer](how-to-deploy-the-app-v-46-and-the-app-v--51-client-on-the-same-computer.md)">Cómo implementar el cliente de App-V 4,6 y App-V 5,1 en el mismo equipo </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Secuencia y lanzamiento de paquetes de aplicaciones-V 5,1. Según sea necesario, vuelva a publicar los paquetes de App-V 4,6.</p></td>
<td align="left"><p><a href="how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md" data-raw-source="[How to Sequence a New Application with App-V 5.1](how-to-sequence-a-new-application-with-app-v-51-beta-gb18030.md)">Cómo secuencia una nueva aplicación con App-V 5,1 </a> .</p></td>
</tr>
</tbody>
</table>

 

**Importante**  Debe estar ejecutando la última versión de App-V 4.6 para usar el modo de coexistencia. Además, al secuenciar un paquete, debe configurar la configuración de la autoridad de administración, que se encuentra en la **configuración del usuario** , en la sección **configuración de usuario** .

 

## Migrar la infraestructura completa de App-V 5,1 Server


No hay ningún método directo para actualizar a una infraestructura completa de App-V 5,1. Use la información de la siguiente sección para obtener información sobre cómo actualizar el servidor de App-V.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Actualiza tu entorno a la versión más reciente de App-V 4.6.</p></td>
<td align="left"><p><a href="../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md" data-raw-source="[Application Virtualization Deployment and Upgrade Considerations](../appv-v4/application-virtualization-deployment-and-upgrade-considerations-copy.md)">Implementación de virtualización de aplicaciones y consideraciones de actualización </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Implemente la versión de App-V 5,1 del cliente.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-client-51gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-51gb18030.md)">Cómo implementar el cliente de App-V </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Instale App-V 5,1 Server.</p></td>
<td align="left"><p><a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)">Cómo implementar el servidor de App-V 5,1 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Migrar paquetes existentes.</p></td>
<td align="left"><p>Consulte la <strong> sección convertir paquetes creados con una versión anterior de App-V </strong> de este artículo.</p></td>
</tr>
</tbody>
</table>

 

## Tareas adicionales de migración


También puede realizar tareas adicionales de migración, como cambiar la configuración de los extremos, así como abrir un paquete creado con una versión anterior en un equipo que ejecute el cliente de App-V 5,1. Los vínculos siguientes proporcionan más información sobre cómo realizar estas tareas.

[Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a un paquete de App-V 5.1 convertido para todos los usuarios de un equipo específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

[Cómo migrar puntos de extensión desde un paquete de App-V 4.6 a App-V 5.1 para un usuario específico](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

[Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para todos los usuarios de un equipo específico](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Cómo revertir puntos de extensión desde un paquete App-V 5.1 a un paquete de App-V 4.6 para un usuario específico](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)







## Otros recursos para realizar tareas de migración de App-V


[Operaciones de App-V 5.1](operations-for-app-v-51.md)

[Un procedimiento simplificado para la actualización del servidor de administración de Microsoft App-V 5,1](https://go.microsoft.com/fwlink/p/?LinkId=786330)

 

 





