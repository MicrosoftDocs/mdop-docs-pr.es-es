---
title: Cómo instalar el cliente de App-V mediante el uso de Setup.msi
description: Cómo instalar el cliente de App-V mediante el uso de Setup.msi
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817331"
---
# Cómo instalar el cliente de App-V mediante el uso de Setup.msi


En este tema se describe cómo instalar el cliente de App-V con el programa setup.msi. Antes de instalar el cliente de App-V con el programa setup.msi, primero debe determinar si debe instalarse algún software previo y, después, debe instalarlo. Para instalar el software necesario, consulte la sección [instalación de software necesario](#prereq-sw) de este tema. Para instalar el software de cliente, vea el tema sobre cómo [instalar el cliente de App-V en la sección Setup.msi programa](#msi-setup) de este tema.

## <a href="" id="prereq-sw"></a>Instalar el software necesario


Puede usar los procedimientos siguientes para instalar el software necesario. Puede crear un archivo de comandos y ejecutar los comandos desde el símbolo del sistema, o bien puede usar un lenguaje de scripts, como VBScript o Windows PowerShell, para ejecutar los comandos.

**Nota:**  Las versiones x86 del siguiente software son necesarias para las versiones x86 y x64 del cliente de App-V.

 

**Para instalar Microsoft VisualC + + 2005SP1 Redistributable Package (x86)**

1. Descargue el paquete de software [Microsoft Visual C++ 2005 SP1 Redistributable Package (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) desde el centro de descarga de Microsoft ( <https://go.microsoft.com/fwlink/?LinkId=119961> ). \ [Valor del token de plantilla \] para la versión 4,5 SP2 y posteriores del cliente de App-V, descargue vcredist\_x86.exe de la [actualización de seguridad ATL del paquete redistribuible de Microsoft Visual C++ 2005 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [valor de token de plantilla \]

2. Para instalar silenciosamente, use la opción de línea de comandos "/Q" con vcredist\_x86.exe, por ejemplo, **vcredist\_x86.exe/q**.

3. Para instalar el software mediante el archivo vcredist\_x86.msi, use la opción de la línea de comandos "/C/T: &lt; fullpathtofolder &gt; " para extraer los archivos vcredist.msi y vcredis1.cab de vcredist\_x86.exe a una carpeta temporal. Para instalar silenciosamente, use la opción de línea de comandos/Quiet, por ejemplo, **msiexec/i vcredist.msi** /quiet.

### Para instalar Microsoft VisualC + + 2008SP1 Redistributable Package (x86)

**Importante**  Para la versión 4.6 y posteriores del cliente de App-V, también debe instalar la actualización de seguridad ATL del paquete redistribuible Microsoft Visual C++ 2008 Service Pack 1.

 

****

1.  Descargue el paquete de software de la [actualización de seguridad ATL del paquete redistribuible del Service Pack 1 de Microsoft Visual C++ 2008](https://go.microsoft.com/fwlink/?LinkId=150700) en el centro de descarga de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=150700) .

2.  Para instalar silenciosamente, use la opción de línea de comandos "/Q" con vcredist\_x86.exe, por ejemplo, **vcredist\_x86.exe/q**.

### Para instalar Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)

****

1.  Descargue el paquete de software [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) en el centro de descarga de Microsoft ( https://go.microsoft.com/fwlink/?LinkId=63266) .

2.  Para instalar silenciosamente, use la opción de línea de comandos/Quiet, por ejemplo, **msiexec/i msxml6\_x86.msi/Quiet**.

### Para instalar informes de errores de aplicaciones de Microsoft

Al instalar informes de errores de aplicaciones de Microsoft, debe usar el parámetro *APPGUID* para especificar el código de producto de App-V. El código de producto es único para cada tipo de cliente de App-V y versión. Seleccione el código de producto correcto en la tabla siguiente.

**Importante**  Para App-V 4.6 SP2 y versiones posteriores, ya no necesita instalar informes de errores de aplicaciones de Microsoft (dw20shared.msi). App-V ahora usa informe de errores de Microsoft.

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Versión</th>
<th align="left">Código de producto para cliente de escritorio</th>
<th align="left">Código de producto para el cliente para servicios de escritorio remoto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4,5 CU1</p></td>
<td align="left"><p>FE495DBC-6D42-4698-B61F-86E655E0796D</p></td>
<td align="left"><p>8A97C241-D92A-47DC-B360-E716C1AAA929</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,5 SP1</p></td>
<td align="left"><p>93468B43-C19D-44F9-8BCC-114076DB0443</p></td>
<td align="left"><p>0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,5 SP2</p></td>
<td align="left"><p>C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</p></td>
<td align="left"><p>ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86</p></td>
<td align="left"><p>9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</p></td>
<td align="left"><p>439FAC21-B423-41D4-8126-54F9FCB70039</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64</p></td>
<td align="left"><p>E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</p></td>
<td align="left"><p>D2977C18-D88A-47CB-AFD8-652DD36F4D0D</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86 ¹</p></td>
<td align="left"><p>40C3258B-F9D1-46DF-AE97-72C1F86F2427</p></td>
<td align="left"><p>9915D911-CC73-4122-AF4F-564F89454655</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64 ¹</p></td>
<td align="left"><p>1650E31F-23B8-40B5-A60A-C5934F557E3B</p></td>
<td align="left"><p>7580D918-C621-49E7-9877-3CC59F9BD1DA</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86 SP1</p></td>
<td align="left"><p>DB9F70CD-29BC-480B-8BA2-C9C2232C4553</p></td>
<td align="left"><p>1354855A-2298-4C73-9022-EF0686C65991</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64 SP1</p></td>
<td align="left"><p>342C9BB8-65A0-46DE-AB7A-8031E151AF69</p></td>
<td align="left"><p>B2C6C8D5-FE76-4056-A326-EE5D633EA175</p></td>
</tr>
</tbody>
</table>

 

¹ versión de "idiomas" de aplicación-V.

**Nota:**  Si necesita encontrar el código de producto, puede usar el Orca.exe editor de bases de datos o una herramienta similar para examinar los archivos de Windows Installer para buscar el valor de la propiedad *ProductCode* . Para obtener más información sobre cómo usar Orca.exe, consulte [herramientas de desarrollo de Windows Installer](https://go.microsoft.com/fwlink/?LinkId=150008) ( https://go.microsoft.com/fwlink/?LinkId=150008) .

 

****

1.  Busque el programa de instalación informes de errores de aplicaciones de Microsoft, dw20shared.msi, que se encuentra en la carpeta **Support\\Watson** de los medios de publicación.

2.  Para instalar el software, ejecute el siguiente comando:

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a>Instalar el cliente de App-V con el programa Setup.msi


Use el siguiente procedimiento para instalar el cliente de App-V. Asegúrese de que se ha instalado todo el software necesario. \ [Valor del token de plantilla \] para la versión 4.6 y posteriores del cliente de App-V, el programa de setup.msi comprueba el sistema y si no está instalado el software necesario, genera un mensaje de error que indica que la instalación no puede continuar. \ [Valor del token de plantilla \]

**Para instalar el cliente de virtualización de aplicaciones con Setup.msi**

1.  Asegúrese de que ha iniciado sesión con una cuenta que tiene derechos de administrador en el equipo.

2.  Abra una ventana del símbolo del sistema con derechos elevados y, a continuación, cambie el directorio a la carpeta que contiene los archivos de instalación. Al instalar la versión 4.6 o una versión posterior del cliente de App-V, debe usar el instalador correcto para el sistema operativo del equipo, 32 bits o 64 bits. La instalación no se realizará y aparecerá un mensaje de error si usa el instalador equivocado.

3.  Escriba la cadena de comando de instalación en el símbolo del sistema. Como alternativa, puede crear un archivo de comandos y ejecutarlo desde el símbolo del sistema. También puede usar un lenguaje de scripts, como VBScript o Windows PowerShell, para ejecutar el comando.

4.  En el siguiente ejemplo de línea de comandos se muestra cómo se puede usar setup.msi con un número de parámetros opcionales. Para obtener más información sobre estos parámetros, consulte [parámetros de la línea de comandos del instalador del cliente de virtualización de aplicaciones](application-virtualization-client-installer-command-line-parameters.md).

    **msiexec.exe/i "setup.msi" SWICACHESIZE = "10.240" SWIPUBSVRDISPLAY = "sistema de producción" SWIPUBSVRTYPE = "HTTP/Secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "/AppVirt/appsntype.xml" SWIPUBSVRREFRESH = "ON" SWIGLOBALDATA = "D:\\AppVirt\\Global", "=" "."}**

    **Importante**  
    -   El modificador de Windows Installer "**/q**" se usa para hacer que esta sea una instalación silenciosa.

    -   Los caracteres "" **%** en "**% HomeDrive%**" deben ir precedidos del **^** carácter de escape "". En caso contrario, el shell de comandos de Windows establece el valor en el del usuario que realiza la instalación.

    -   Para activar el registro de instalación, use el modificador msiexec **/l\ * v nombrearchivo. log**.

     

## Temas relacionados


[Cómo instalar el cliente mediante el uso de la línea de comandos](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





