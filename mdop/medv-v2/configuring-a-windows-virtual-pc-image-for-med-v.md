---
title: Configurar una imagen de Windows Virtual PC para MED-V
description: Configurar una imagen de Windows Virtual PC para MED-V
author: dansimp
ms.assetid: d87a0df8-9e08-4d1e-bfb0-9dc3cebf0d28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 340754b33576651c8ba89c85f369c48c0a0ab957
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826820"
---
# Configurar una imagen de Windows Virtual PC para MED-V


Una vez que haya instalado todo lo que desea incluir en la imagen de MED-V, puede configurar la imagen para usarla en Microsoft Enterprise Desktop Virtualization (MED-V) 2,0. En los temas de esta sección se proporcionan instrucciones para configurar la imagen de MED-V para que se ejecute por primera vez antes de crear el paquete de área de trabajo de MED-V.

La configuración primera prepara el área de trabajo de MED-V para un usuario final. El proceso crea una máquina virtual a partir de la imagen empaquetada en el área de trabajo de MED-V y, después, ejecuta la instalación mínima de Windows en la máquina virtual. Esto incluye la ejecución tanto de las secuencias de comandos de instalación personalizadas como de la aplicación de finalización de la instalación por primera vez FtsCompletion.exe.

Siga estos pasos para configurar su imagen de MED-V para ejecutar la configuración de primera vez:

1. Como opción, puede compactar el disco duro virtual (VHD) para recuperar espacio en disco vacío y reducir el tamaño del VHD antes de continuar con la configuración de la imagen de Windows Virtual PC. Para obtener más información, vea [compactar el disco duro virtual de MED-V](compacting-the-med-v-virtual-hard-disk.md).

2. Personalizar el proceso de configuración de la máquina virtual.

3. Selle la imagen de MED-V mediante el uso de Sysprep.

   **Personalizar el proceso de configuración de la máquina virtual**

4. Como parte de la preparación de la imagen para su uso con MED-V, puede configurar varias opciones en la máquina virtual, como especificar la configuración de la ejecución de Windows Update. Especifique la configuración de máquina virtual necesaria antes de crear el paquete de área de trabajo MED-V.

5. Antes de crear el paquete de área de trabajo MED-V, le recomendamos que deshabilite los puntos de restauración en la máquina virtual para evitar que el disco de diferenciación crezca sin límites. Para obtener más información, consulte [Cómo desactivar y activar Restaurar sistema en Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .

   **Nota**  
   Puede configurar el archivo Sysprep. inf para deshabilitar los puntos de restauración cuando se ejecute la configuración por primera vez. Para obtener un ejemplo de la configuración de esta clave GuiRunOnce, vea el archivo Sysprep. inf de ejemplo más adelante en esta sección.



6. Configure el proceso de instalación para ejecutar el miniprograma de instalación en lugar de la bienvenida predeterminada de Windows. Debe ejecutar la herramienta Sysprep con el modificador **-mini** o activar la casilla **MiniSetup** en la interfaz gráfica de usuario. Para obtener más información, vea [Cómo sellar la imagen con Sysprep](#bkmk-seal).

   **Llamar al archivo de finalización de la primera instalación**

   1.  Un ejecutable denominado FtsCompletion.exe se incluye como parte de la instalación del agente invitado MED-V. De forma predeterminada, se encuentra en la unidad de sistema de su imagen de MED-V, en **archivos de programa, virtualización de escritorio de Microsoft Enterprise**.

       **Importante**  
       Debe ejecutar este programa ejecutable como paso final en el proceso de configuración por primera vez. El usuario para el que se llama el programa ejecutable debe ser miembro del grupo de administradores locales del invitado.



   2.  Puede decidir cómo desea llamar a este programa ejecutable, por ejemplo, a través de un script que se implementa con el área de trabajo de MED-V. Puede llamar a este archivo ejecutable como la última línea del archivo Sysprep. inf. Para obtener un ejemplo de cómo llamar a este programa ejecutable en el archivo Sysprep. inf, consulte el archivo de ejemplo más adelante en esta sección.

Una vez que haya completado la personalización de la imagen de MED-V, estará listo para sellar la imagen mediante el uso de Sysprep.

<a href="" id="bkmk-seal"></a>**Sellar la imagen de MED-V mediante el uso de Sysprep**

1.  La herramienta de preparación del sistema (Sysprep) es una tecnología que puede usar para realizar instalaciones basadas en imágenes en toda la red con la intervención mínima de un administrador o de un profesional de ti.

2.  En un entorno de MED-V, puede usar Sysprep para asignar identificadores de seguridad únicos (SID) y otras configuraciones a cada área de trabajo de MED-V la primera vez que se inician.

    **Nota**  
    Para obtener más información sobre cómo usar Sysprep, consulte [referencia técnica de Sysprep](https://go.microsoft.com/fwlink/?LinkId=195930) ( https://go.microsoft.com/fwlink/?LinkId=195930) .



~~~
**Caution**  
When you use non-ASCII characters in the Sysprep.inf file, you must save the file by using the encoding appropriate for the characters entered. Windows XP expects the Sysprep.inf file to be encoded by using the code page for the language that you are targeting.

You must also make sure that the System Locale of the computers to which the MED-V workspace is deployed is set to handle the language specific characters that might be present in the Sysprep.inf file. To change the settings for the System Locale, follow these steps:

1.  To open Region and Language, click **Start**, click **Control Panel**, and then click **Region and Language**.

2.  Click the **Administrative** tab, and then click **Change System Locale** under **Language for non-Unicode programs**.

    If you are prompted for an administrator password or confirmation, type the administrator password or provide confirmation.

3.  Select your preferred language and then click **OK**.



**To configure Sysprep on the MED-V Guest Computer**

1.  Create a folder named *Sysprep* in the root of the MED-V image system drive.

2.  Download the deploy.cab file. For more information, see [Windows XP Service Pack 3 Deployment Tools](https://go.microsoft.com/fwlink/?LinkId=195928) From the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195928).

3.  From the deploy.cab file, copy or extract the Setupmgr.exe, Sysprep.exe, and Setupcl.exe files to the Sysprep folder.

4.  In the Sysprep folder, run **Setup Manager** (Setupmgr.exe) to create a Sysprep.inf answer file.

    Or, you can create this file manually or use your company’s existing file. For more information, see [How to use the Sysprep tool to automate successful deployment of Windows XP](https://go.microsoft.com/fwlink/?LinkId=195929) (https://go.microsoft.com/fwlink/?LinkId=195929).

5.  Follow the **Setup Manager** wizard.

    **Important**  
    You must configure the MED-V guest to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.



    **Caution**  
    When you configure a proxy account for joining virtual machines to the domain, know that it is possible for an end user to obtain the proxy account credentials. Take all the necessary security precautions to minimize risk, such as limiting account user rights. For more information about security concerns when you configure a Windows Virtual PC image for MED-V, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).



    If end users must provide information during the first time setup process based on the parameters specified in the Sysprep.inf file, you must also specify that first time setup is run in **Attended** mode when you are creating your MED-V workspace package. If no information will be required from the end user, you can specify that first time setup is run in **Unattended** mode when you are creating your MED-V workspace package. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode. This requires that you provide all of the required settings information as you continue through the **Setup Manager** wizard.

    **Caution**  
    If you have set a local policy or registry entry to include a service level agreement (SLA) in your image (VHD), you must specify that first time setup is run in **Attended** mode or first time setup will fail. Or, a MED-V best practice is to enforce the SLA through Group Policy later so that the SLA is displayed to the end user after first time setup is finished.



    **Note**  
    You can configure the MED-V workspace to set certain Sysprep.inf settings based on the configuration of the host and the identity of the end user. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).



6.  Seal the MED-V image.

    **Important**  
    We recommend that you make a backup copy of the MED-V image before sealing it.



    After you have completed all the steps in the **Setup Manager** wizard, you are ready to run Sysprep to seal the MED-V image.

**To run Sysprep**

1.  Run the System Preparation Tool (Sysprep.exe) from the *Sysprep* folder that you created when you configured Sysprep in the MED-V virtual machine.

2.  In the warning message box that appears, click **OK**.

3.  In the **Options** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes. Also, make sure that the **Shutdown mode** box is set to **Shut down**.

4.  Click **Reseal**. This removes identity information and clears event logs to prepare for first time setup.

5.  If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and then change the selections.

6.  Click **OK** to complete the system preparation process.

After you have run Sysprep on your MED-V image, the virtual machine shuts down and is ready for use in creating a MED-V workspace.
~~~

## Ejemplo


Este es un ejemplo de un archivo Sysprep. inf.

``` syntax
;SetupMgrTag
[GuiUnattended]
    EncryptedAdminPassword=NO
    TimeZone=10
    OEMDuplicatorstring="MED_V v2 Host"
    AdminPassword="administrator"
    AutoLogon=Yes
    AutoLogonCount=1
    OEMSkipRegional=1
    OemSkipWelcome=1

[UserData]
    ProductKey=
    FullName="MED-V User"
    OrgName="Contoso"
    ComputerName=*

[Identification]
    JoinDomain=domain.corp.contoso.com
    DomainAdmin=UserName
    DomainAdminPassword=Password

[Networking]
    InstallDefaultComponents=Yes

[Branding]
    BrandIEUsingUnattended=Yes

[Proxy]
    Proxy_Enable=0
    Use_Same_Proxy=0

[Unattended]
    InstallFilesPath=C:\sysprep\i386
    TargetPath=\WINDOWS
    UpdateServerProfileDirectory=1
    OemSkipEula=Yes

[RegionalSettings]
    LanguageGroup=1
    Language=00000409

[GuiRunOnce]
    Command0="wmic /namespace:\\root\default path SystemRestore call Disable %SystemDrive%\"
    Command1="c:\Program Files\Microsoft Enterprise Desktop Virtualization\FtsCompletion.exe"

[sysprepcleanup]
```

## Temas relacionados


[Crear un paquete de área de trabajo de MED-V](create-a-med-v-workspace-package.md)

[Preparar una imagen de MED-V](prepare-a-med-v-image.md)









