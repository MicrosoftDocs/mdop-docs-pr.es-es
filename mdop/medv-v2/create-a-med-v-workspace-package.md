---
title: Crear un paquete de área de trabajo de MED-V
description: Crear un paquete de área de trabajo de MED-V
author: dansimp
ms.assetid: 3f75fe73-41ac-4389-ae21-5efb2d437f4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e20cf4cc9394c4a5e90178fff4fc36ed83c12d60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823261"
---
# Crear un paquete de área de trabajo de MED-V


Un área de trabajo de MED-V es el entorno de escritorio de Windows XP en el que los usuarios finales interactúan con la máquina virtual proporcionada por MED-V. El administrador crea y personaliza el área de trabajo de MED-V. El área de trabajo consta de una imagen y la Directiva de grupo que define las reglas y la funcionalidad del área de trabajo de MED-V.

Puede crear varias áreas de trabajo de MED-V, cada una personalizada con su propia configuración, configuración y reglas. Un usuario, grupo o varios usuarios o grupos pueden estar asociados a cada área de trabajo de MED-V. La personalización hace que el área de trabajo de MED-V solo esté disponible para ese usuario o grupo.

Use el **Empaquetador de área de trabajo de Med-v** para crear áreas de trabajo de Med-v. El **paquete del área de trabajo MED-V** se divide en dos secciones principales:

-   Panel principal que incluye tres botones que se usan para crear y administrar áreas de trabajo de MED-V. El botón **crear un paquete de área de trabajo Med-v** abre el **Asistente para crear un área de trabajo Med-v** que se usa para crear las áreas de trabajo de Med-v.

-   **Centro de ayuda** , situado en la parte derecha de la ventana, que proporciona información e instrucciones para ayudarle a crear, probar y administrar sus áreas de trabajo de MED-V.

**Importante**  
Para poder usar el **Empaquetador de área de trabajo de MED-V**, primero debe asegurarse de que la Directiva de ejecución de Windows PowerShell esté establecida en no restringido.

`Set-ExecutionPolicy Unrestricted`

Además, la Directiva SAN del equipo en el que se ejecuta el **paquete de área de trabajo MED-V** debe establecerse en "conectado a todos". Para comprobar la configuración de la Directiva SAN, ejecute los siguientes comandos en un símbolo del sistema con credenciales administrativas:

`diskpart.exe`

`DISKPART> san`

`DISKPART> exit`

Si es necesario, cambie la Directiva SAN a "en línea todo" escribiendo los siguientes comandos en el símbolo del sistema con credenciales administrativas:

`diskpart.exe`

`DISKPART> san policy=onlineall`

`DISKPART> exit`



**Importante**  
Si el software de cifrado de disco automático está instalado en el equipo que usa para montar el disco duro virtual y crear el paquete de área de trabajo MED-V, debe deshabilitar el software antes de empezar. De lo contrario, no puede usar el área de trabajo de MED-V en ningún otro equipo.



La información que proporcionamos aquí puede ayudarle a crear su paquete de implementación de área de trabajo de MED-V.

## <a href="" id="bkmk-prereq"></a>Requisitos previos


Antes de empezar a crear el paquete de implementación de área de trabajo de MED-V, compruebe que tiene acceso a los siguientes elementos:

-   **Una imagen de Windows XP preparada**

    Para obtener más información sobre cómo crear una imagen de Windows XP para usarla con MED-V, vea [preparar una imagen de Med-v](prepare-a-med-v-image.md).

-   **Un archivo de texto o lista que contiene información sobre el redireccionamiento de la dirección URL**

    La lista o archivo de texto de redirección de URL contiene las direcciones URL que desea que se redirijan desde el equipo host a Internet Explorer en el área de trabajo de MED-V. Cuando use el Asistente para empaquetar para crear el área de trabajo de MED-V, importe, escriba o copie y pegue esta información de redireccionamiento como uno de los pasos del proceso de creación del paquete.

    **Nota**  
    El redireccionamiento de direcciones URL en MED-V solo admite los protocolos HTTP y HTTPS. MED-V no proporciona soporte técnico para FTP ni para otros protocolos.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



## Empaquetar un área de trabajo de MED-V para un idioma distinto del idioma del equipo del paquete del área de trabajo MED-V


De forma predeterminada, el área de trabajo de MED-V admite caracteres en el idioma del equipo y en inglés. Para crear un área de trabajo de MED-V para un idioma distinto del que está instalado en el equipo, especifique **-Loc \ [locale \]** en el script de PowerShell (. PS1) después del nombre del área de trabajo MED-V.

Para crear un paquete de área de trabajo de MED-V en un idioma que no sea el predeterminado del equipo del paquete del área de trabajo MED-V, genere un script en el idioma predeterminado ejecutando el Empaquetador de área de trabajo MED-V y, a continuación, modifique la secuencia de comandos de salida según sea necesario para su configuración regional. El script se encuentra en el directorio de salida del área de trabajo de MED-V que se especificó durante el embalaje. Los nombres de la configuración regional están en el. WXL archivos en el siguiente directorio:

C:\\Archivos de escritorio de Programa\\microsoft Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale

## Crear un paquete de área de trabajo de MED-V


Para crear un paquete de área de trabajo de MED-V, siga estos pasos:

****

1.  Para abrir el **Empaquetador de área de trabajo de MED-V**, haga clic en **Inicio**, haga clic en **todos los programas**, en **Microsoft Enterprise Desktop Virtualization**y, a continuación, haga clic en **Empaquetador de área de trabajo de MED-V**.

2.  En el panel principal de **empaquetador del área de trabajo de Med-v** , haga clic en **crear un paquete de área de trabajo Med-v**.

    Aparecerá el **Asistente para crear paquete de área de trabajo** Med-v. El asistente consta de las siguientes páginas:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Información de paquete</strong></p></td>
    <td align="left"><p>Especifique un nombre para el área de trabajo de MED-V y seleccione una carpeta en la que se guarden los archivos de paquete del área de trabajo de MED-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Seleccionar imagen de Windows XP</strong></p></td>
    <td align="left"><p>Especifique su imagen de Virtual PC de Windows XP preparada.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Configuración de primera vez</strong></p></td>
    <td align="left"><p>Especificar el proceso de configuración que MED-V seguirá durante la configuración de la primera vez.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Mensajes MED-V</strong></p></td>
    <td align="left"><p>Especifique los mensajes y la dirección URL opcional de la información de ayuda que el usuario final verá durante la configuración primera vez.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Asignar nombres a equipos</strong></p></td>
    <td align="left"><p>Especifique cómo se denomina la máquina virtual de MED-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Copiar configuración del host</strong></p></td>
    <td align="left"><p>Especifique cómo se definen los valores para el área de trabajo de MED-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Inicio y redes</strong></p></td>
    <td align="left"><p>Especifique la configuración para iniciar el área de trabajo de MED-V, las redes y las credenciales de usuario.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Redireccionamiento web</strong></p></td>
    <td align="left"><p>Especifique un archivo de texto o una lista de las direcciones URL que desea redirigir a Internet Explorer en el área de trabajo de MED-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Resumen</strong></p></td>
    <td align="left"><p>Compruebe la configuración del área de trabajo de MED-V y empiece a crear su paquete de implementación de área de trabajo de MED-V.</p></td>
    </tr>
    </tbody>
    </table>



3.  En la página **información del paquete** , escriba un nombre para el área de trabajo de Med-v y seleccione una carpeta en la que se guarden los archivos de paquete del área de trabajo de Med-v.

    **Advertencia**  
    Debe nombrar el área de trabajo de MED-V y especificar una carpeta para continuar.



~~~
After you have finished, click **Next**.
~~~

4. En la página **seleccionar imagen de Windows XP** , especifique la ubicación de su imagen de Virtual PC de Windows XP de MED-V preparada (archivo. vhd).

   **Advertencia**  
   Debe especificar una imagen de VHD de Windows XP para continuar.



~~~
After you have finished, click **Next**.
~~~

5. En la página **primera configuración** , seleccione si quiere que la configuración se ejecute por primera vez durante la versión atendida o desatendido y si desea que el área de trabajo de MED-V se use por separado o que todos los usuarios finales usen un equipo compartido.

   Si selecciona la **instalación desatendida, sin ninguna notificación**, no se informa al usuario final antes de ejecutar la configuración por primera vez y la máquina virtual no se muestra al usuario final durante la configuración de la primera vez. Además, la página de **mensajes de MED-V** del asistente se oculta porque no se necesitan mensajes si la primera vez se ejecuta el programa de instalación en modo desatendido.

   Si selecciona la **configuración desatendida, pero notificar a los usuarios finales antes de que empiece la configuración por primera vez**, se informa al usuario final antes de ejecutar la instalación por primera vez. Sin embargo, la máquina virtual no se muestra al usuario final durante la configuración de la primera vez.

   Seleccione **configuración atendida** si el usuario final debe especificar la información durante la configuración por primera vez.

   El comportamiento predeterminado es la **configuración desatendida, pero notifica a los usuarios finales antes de que empiece la configuración por primera vez**.

   **Actúe**  
   Si creó el archivo Sysprep. inf para que la instalación mínima requiera que se complete la entrada del usuario, debe seleccionar la **configuración atendida** o los problemas pueden producirse durante la configuración de la primera vez.



~~~
You can also specify how a MED-V workspace is used on computers that are shared by multiple end users. You can decide that you want to create a unique MED-V workspace for each end user or that you want the MED-V workspace made available to all end users who share the computer. The default is that the MED-V workspace is unique for each end user.

**Important**  
We recommend that you disable the fast user switching feature in Windows if you configure the MED-V workspace to be accessed by all users on a shared computer. Problems can occur if an end user logs on by using the fast user switching feature in Windows when another user is still logged on.



**Tip**  
When you create a name mask for the MED-V workspace on the **Naming Computers** page, make sure that each virtual machine on a shared computer has a unique computer name.



You can also specify whether the MED-V workspace is added to the Administrators group or administrator credentials are managed outside MED-V. By default, the MED-V workspace is not automatically added to the Administrators group.

After you have finished, click **Next**.
~~~

6. En la página **mensajes de MED-V** , especifique los siguientes mensajes que el usuario final verá durante la configuración de primera vez:

   -   Mensaje que el usuario final ve cuando comienza la configuración por primera vez.

   -   Mensaje que verá el usuario final si se produce un error al configurar por primera vez o se produce un error.

   **Nota**  
   La página de **mensajes de MED-V** del asistente está oculta si seleccionó la **instalación desatendida, sin ninguna notificación** en la primera página de **configuración** .



~~~
You can also specify an optional URL location for help information that is provided to the end user when first time setup is running.

For example, the URL can point to an internal IT webpage with answers to questions such as "How long will this take and how will I know when it has completed?" or "What do you do if you get an error message?"

**Note**  
If you specify a URL, a link is shown during first time setup that points the end user to this help information. If you do not specify a URL, no link is provided.



After you have finished, click **Next**.
~~~

7. En la página de **nombres de equipos** , puede especificar si los nombres de los equipos son administrados por MED-V o por una herramienta de administración del sistema, como Sysprep. La opción predeterminada es que la asignación de nombres de equipos sea administrada por una herramienta de administración del sistema.

   Si especifica que MED-V administra la asignación de nombres de equipos, seleccione una Convención de nomenclatura de equipos predefinida (máscara) en la lista desplegable. Aparece una vista previa del nombre de un equipo de muestra que se basa en el equipo que está usando para crear el paquete de área de trabajo MED-V.

   Si selecciona una de las convenciones de nomenclatura personalizadas, los campos que puede especificar se limitan a los siguientes caracteres:

   -   Los campos prefijo y sufijo se limitan a los caracteres a-Z, a-z, 0-9 y los caracteres especiales. @ \ # $% ^ & ()-\ _ ' {}. y ~.

   -   Los campos hostname y username se limitan a los dígitos del 0 al 9.

   **Importante**  
   Los nombres de equipo deben ser únicos y estar limitados a un máximo de 15 caracteres. Cuando decida el método de asignación de nombres de equipos, considere la posibilidad de que los usuarios finales tengan varios equipos o que compartan un equipo, y evite usar máscaras de nombre de equipo que puedan causar colisiones en la red.



~~~
**Caution**  
The computer name settings that you specify on this page override those specified in the Sysprep.inf answer file.



After you have finished, click **Next**.
~~~

8. En la página **copiar configuración de host** , puede seleccionar la configuración siguiente para especificar cómo se configura el área de trabajo de MED-V:

   **Actúe**  
   La configuración que especifique en esta página que se copia del equipo host al área de trabajo MED-V reemplaza a las especificadas en el archivo de respuesta Sysprep. inf.



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Copy regional settings</strong></p></td>
<td align="left"><p>Select this check box to copy the regional settings from the host computer to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[RegionalSettings]
Language
SystemLocale
UserLocale
UserLocale_DefaultUser
InputLocale
InputLocale_DefaultUser
</code></pre></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy user settings</strong></p></td>
<td align="left"><p>Select this check box to copy certain user settings, such as user name and company name, from the host to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[UserData]
OrgName
FullName</code></pre>
<div class="alert">
<strong>Note</strong>  
<p>Personal settings, such as Internet browsing history, are not copied over to the MED-V workspace.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain name</strong></p></td>
<td align="left"><p>Select this check box to let the guest join the same domain as the host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><div class="alert">
<strong>Important</strong>  
<p>The MED-V guest must be configured to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain organizational unit</strong></p></td>
<td align="left"><p>Select this check box to copy the domain organizational unit from the host computer to the MED-V workspace. This check box is only enabled if you select to copy the domain name from the host computer.</p></td>
</tr>
</tbody>
</table>



After you have finished, click **Next**.
~~~

9. En la página **Inicio y redes** , puede cambiar el comportamiento predeterminado de las siguientes opciones:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Iniciar área de trabajo MED-V</strong></p></td>
   <td align="left"><p>Elija si desea iniciar el área de trabajo de MED-V al iniciar sesión de usuario, al utilizar por primera vez, o para que el usuario final decida cuándo se inicia el área de trabajo de MED-V.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>El área de trabajo de MED-V se inicia de una de estas dos maneras: cuando el usuario final inicia sesión o cuando inicia por primera vez una acción que requiere MED-V, como abrir una aplicación publicada o especificar una dirección URL que requiere redireccionamiento.</p>
   <p>Puede definir esta configuración para el usuario final o permitir que el usuario final controle el inicio de MED-V.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Si especifica que el usuario final decide, el comportamiento predeterminado que experimentan es que el área de trabajo de MED-V se inicia cuando inicia sesión. Pueden cambiar el valor predeterminado haciendo clic con el botón derecho en el icono MED-V en el área de notificación y seleccionando <strong> configuración de usuario de Med-v </strong> . Si define esta configuración para el usuario final, no podrá cambiar el modo en que se inicia MED-V.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Redes</strong></p></td>
   <td align="left"><p>Seleccione <strong> compartido </strong> o <strong> con puente </strong> para su configuración de red. El valor predeterminado es <strong> Shared </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong>Compartido </strong> - el área de trabajo de MED-V usa la traducción de direcciones de red (NAT) para compartir el host&#39;s IP para el tráfico saliente.</p>
   <p><strong>Con puente </strong> - el área de trabajo de MED-V tiene su propia dirección de red, que normalmente se obtiene a través de DHCP.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Almacenar credenciales</strong></p></td>
   <td align="left"><p>Elija si desea almacenar las credenciales de usuario final.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>El comportamiento predeterminado es que el almacenamiento de credenciales está deshabilitado para que el usuario final se autentique cada vez que inicie sesión.</p>
   <div class="alert">
   <strong>Importante</strong><br/><p>Aunque el almacenamiento en caché de las credenciales del usuario final proporciona la mejor experiencia del usuario, debe tener en cuenta los riesgos implicados.</p>
   <p>La credencial de dominio del usuario final se almacena en un formato reversible en el administrador de credenciales de Windows. Como resultado, un atacante podría escribir un programa que recupere la contraseña y podría obtener acceso a las credenciales del usuario. Solo puede reducir este riesgo deshabilitando el almacenamiento de credenciales de usuario final.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



~~~
After you have finished, click **Next**.
~~~

10. En la página de **redireccionamiento web** , puede escribir, pegar o importar una lista de las direcciones URL que se redirigen a Internet Explorer en el área de trabajo de MED-V. Para obtener más información sobre cómo configurar la información de redireccionamiento de la dirección URL, consulte [requisitos previos](#bkmk-prereq).

   También puede especificar cómo está configurado Internet Explorer en el área de trabajo de MED-V para los usuarios finales. De forma predeterminada, el nivel de seguridad de la zona de Internet está establecido en alto. Además, se eliminan ciertas capacidades de exploración predeterminadas, como la barra de direcciones. Esta configuración predeterminada de Internet Explorer en el área de trabajo de MED-V proporciona un entorno de exploración más seguro para los usuarios finales.

   **Actúe**  
   Al cambiar la configuración predeterminada, puede personalizar Internet Explorer en el área de trabajo de MED-V. Sin embargo, tenga en cuenta que si cambia la configuración predeterminada para que sea menos segura, puede exponer su organización a los riesgos de seguridad presentes en las versiones anteriores de Internet Explorer. Para obtener más información, vea [procedimientos recomendados de seguridad para las operaciones de MED-V](security-best-practices-for-med-v-operations.md).



~~~
After you have finished, click **Next**.
~~~

11. En la página de **Resumen** , puede revisar la configuración de empaquetado de este área de trabajo de MED-V. Si desea cambiar la configuración, haga clic en el botón **anterior** para volver a la página correspondiente. Cuando haya terminado de revisar la configuración, haga clic en **crear**.

   Se abrirá la página de **finalización** del **Asistente crear paquete de área de trabajo MED-V** para mostrar el progreso de la creación del paquete.

   **Nota**  
   El proceso de creación del paquete del área de trabajo de MED-V puede demorar varios minutos en completarse, según el tamaño del VHD especificado.



~~~
If the MED-V workspace package is created successfully, the **Completion** page displays a list of the files that you created and their respective locations. The following is a list of the files that are created and their descriptions:

-   **setup.exe**—an installation program that you deploy and run on end-user computers to install the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.msi**—an installer file that you deploy to the end-user computers. The setup.exe file will run this file to install the MED-V workspaces.

-   **&lt;*vhd\_name*&gt;.medv**—a compressed VHD file that you deploy to the end-user computers. The setup.exe file uses it when it installs the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.reg**—the configuration settings that are installed when the setup.exe, &lt;*workspace\_name*&gt;.msi, and &lt;*vhd\_name*&gt;.medv files are deployed and setup.exe is run.

-   **&lt;*workspace\_name*&gt;.ps1**—a Windows PowerShell script that you can use to rebuild the registry file and re-build the MED-V workspace package.

    **Important**  
    Before deployment, you can edit configuration settings by updating the .ps1 file that has your preferred method of script editing, such as Windows PowerShell. After you change the .ps1 file, use that file to rebuild the MED-V workspace package that you deploy to your enterprise. For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

    However, after the MED-V workspace is deployed, you must edit configuration settings through the registry. For a list and description of the configuration settings, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).
~~~



12. Haga clic en **cerrar** para cerrar el Asistente para empaquetar y volver al **Empaquetador de área de trabajo MED-V**.

El paquete de área de trabajo de MED-V ya está listo para realizar pruebas antes de la implementación.

## Temas relacionados


[Establecimiento de la configuración avanzada con Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md)

[Probar el paquete de área de trabajo de MED-V](testing-the-med-v-workspace-package.md)

[Preparar una imagen de MED-V](prepare-a-med-v-image.md)









