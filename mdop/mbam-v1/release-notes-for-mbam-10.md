---
title: Notas de la versión de MBAM 1.0
description: Notas de la versión de MBAM 1.0
author: dansimp
ms.assetid: d82fddde-c360-48ef-86a0-d9b5fe066861
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 705fd1b936da1454081dd14a7f075f642fc4a405
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826030"
---
# Notas de la versión de MBAM 1.0


**Para buscar un problema específico en estas notas de la versión, presione CTRL + F.**

Lea estas notas de la versión minuciosamente antes de instalar la administración y supervisión de Microsoft BitLocker (MBAM).

Estas notas de la versión contienen información necesaria para instalar MBAM correctamente. Las notas de la versión también contienen información que no está disponible en la documentación del producto. Si hay una diferencia entre estas notas de la versión y otra documentación de MBAM, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## Acerca de la documentación del producto


Para obtener información sobre la documentación de MBAM, consulte la página de inicio de MBAM en Microsoft TechNet.

Para obtener una copia descargable de la documentación de MBAM, consulte <https://go.microsoft.com/fwlink/p/?LinkId=225356> en el centro de descarga de Microsoft.

## Enviar comentarios


Nos interesan tus comentarios en MBAM. Puedes enviar tus comentarios a <mdopdocs@microsoft.com> .

**Nota:**  Esta dirección de correo electrónico no es un canal de soporte técnico, pero tus comentarios nos ayudarán a planificar futuros cambios en nuestra documentación y versiones de productos.

 

Para obtener la información más reciente acerca de MDOP y recursos de aprendizaje adicionales, consulte la página [experiencia de información de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Para obtener más información sobre las nuevas actualizaciones o para proporcionar comentarios, síganos en [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problemas conocidos con MBAM 1,0


Esta sección contiene notas de la versión sobre problemas conocidos relacionados con la instalación y la instalación de MBAM.

### <a href="" id="if-you-select-the--use-a-certificate-to-encrypt-the-network-communication--option-during-setup--existing-database-connections-and-dependent-applications-can-stop-functioning-"></a>Si selecciona la opción "usar un certificado para cifrar la comunicación de red" durante la configuración, las conexiones de base de datos existentes y las aplicaciones dependientes pueden dejar de funcionar

Puede configurar MBAM para la **comunicación cifrada de red** después de instalar la base de datos de recuperación y de hardware o las características de la base de datos de estado de cumplimiento. Si opta por configurar MBAM para la comunicación cifrada de la red, MBAM configuración configura la instancia del motor de base de datos de SQL Server para usar la capa de sockets seguros (SSL) para la comunicación entre la base de datos aplicable y el servidor de administración y las características de servidor de informes de cumplimiento y de cumplimiento.

-   Si la instancia del motor de base de datos de SQL Server aún no está configurada para usar SSL, el programa de instalación de MBAM la configura para hacerlo. Esto puede impedir que las aplicaciones que intentan usar bases de datos que no sean de MBAM en la instancia del motor de base de datos de SQL Server se comuniquen con sus bases de datos.

-   Si la instancia del motor de base de datos de SQL Server ya está configurada para usar SSL, está configurada para usar el certificado seleccionado por el usuario durante la instalación. Si este certificado difiere del que ya estaba en uso, puede impedir que se ejecuten las aplicaciones que usan bases de datos de SQL Server en la instancia del motor de base de datos de SQL Server.

**Solución alternativa:** Nada

### Se produce un error en la instalación de MBAM durante la instalación cuando usa una cuenta de administrador local

MBAM se produce un error al usar una cuenta de administrador local. El archivo de registro contiene la siguiente información:

``` syntax
Locating group 'MBAM Report Users'
Adding <GUID>' to group 'MBAM Report Users'
Locating group 'MBAM Recovery and Hardware DB Access'
Adding 'S-1-5-20' to group 'MBAM Recovery and Hardware DB Access'
Exception: A new member could not be added to a local group because the member has the wrong account type.
 
  StackTrace:    at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SDSUtils.ApplyChangesToDirectory(Principal p, StoreCtx storeCtx, GroupMembershipUpdater updateGroupMembership, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.Update(Principal p)
   at Microsoft.Windows.Mdop.BitlockerManagement.Setup.Groups.CreateGroupsDeferred(Session session)
  InnerException:Exception: A new member could not be added to a local group because the member has the wrong account type.
 
    InnerException:StackTrace:    at System.DirectoryServices.AccountManagement.UnsafeNativeMethods.IADsGroup.Add(String bstrNewItem)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
CustomAction MbamCreateGroupsDeferred returned actual error code 1603 (note this may not be 100% accurate if translation happened inside sandbox)
Action ended 11:41:29: InstallExecute. Return value 3.
```

**Solución alternativa:** Use una cuenta de dominio con credenciales administrativas en el equipo servidor cuando instale MBAM.

### El programa de instalación de MBAM reconfigura la instancia del motor de base de datos de SQL Server para que no use SSL si selecciona "do not Cifre Network Communication"

Al instalar la base de datos de recuperación y de hardware o la base de datos de estado de cumplimiento, puede usar el programa de instalación al seleccionar **comunicación de red cifrada**. Si decide no cifrar la comunicación de red, el programa de instalación de MBAM vuelve a configurar la instancia del motor de base de datos de SQL Server para que no use SSL.

-   Si la instancia del motor de base de datos de SQL Server ya está configurada para usar SSL, el programa de instalación de MBAM deshabilita SSL en la instancia del motor de base de datos de SQL Server. Esto cambia la seguridad de la comunicación entre las aplicaciones que usan bases de datos que no están relacionadas con bases de datos de MBAM en la instancia del motor de base de datos de SQL Server.

**Solución alternativa:** Nada

### Falta el requisito previo de las secuencias de comandos de administración de Internet Information Services (IIS) y las características de servidor Web

El programa de instalación de MBAM depende de la característica de servidor Web de scripts y herramientas de administración de IIS, pero no es un requisito previo obligatorio. La configuración del servidor le permite instalar MBAM cuando falta esta característica. Sin embargo, esto hará que el servicio de copia de seguridad MBAM VSS Writer se inicie y se detenga, ya que no puede ubicar el instrumental de administración de Windows (WMI) ni el proveedor de servicios de Internet Information Server (IIS). No hay ningún mensaje de error para esta condición, excepto el que aparece en el registro de eventos. La instalación de MBAM sin scripts de administración y herramientas de administración de IIS hace que las operaciones de copia de seguridad no se ejecuten para MBAM.

**Solución alternativa:** Asegúrese de que la característica de servidor Web herramientas y scripts de administración de IIS esté instalada antes de iniciar la instalación de MBAM.

### <a href="" id="mbam-setup-stops-responding-during-the--installing-selected-features--phase-when-setup-is-configured-to-use-a-certificate"></a>El programa de instalación de MBAM deja de responder durante la fase "instalar las características seleccionadas" cuando la configuración está configurada para usar un certificado

El programa de instalación de MBAM deja de responder durante la fase de instalación de **las características seleccionadas** de la instalación. Esto se produce durante la instalación de la base de datos de recuperación y hardware o de la base de datos de estado de cumplimiento, después de seleccionar la opción **usar un certificado para cifrar la comunicación de red** . Además, el programa de instalación de MBAM deja de responder si la instancia del motor de base de datos de SQL Server no puede acceder al certificado que se especificó durante la instalación.

**Solución alternativa:** Actualice los permisos del certificado para que el servicio de Windows para la instancia aplicable del motor de base de datos de SQL Server pueda obtener acceso al certificado. También puede cambiar la cuenta en la que se ejecuta la instancia del motor de base de datos de SQL Server para que el motor de base de datos use el certificado. Para determinar los permisos para el certificado, escriba el siguiente comando en el símbolo del sistema: **certutil-v-Store My**

### El programa de instalación de MBAM se detiene durante la instalación de SQL Server Reporting Services

Durante la instalación de MBAM, al seleccionar una instancia de SQL Server Reporting Services (SSRS) y la instancia de SSRS no está disponible, la configuración de MBAM puede detenerse durante un minuto mientras intenta comunicarse con la instancia de SSRS.

**Solución alternativa:** Espere al menos un minuto para que la configuración de MBAM se reanude mientras el programa de instalación intente ponerse en contacto con la instancia de SSRS.

### <a href="" id="administration-and-monitoring-server-does-not-run-after-setup-"></a>El servidor de administración y supervisión no se ejecuta después de la instalación

Después de que el programa de instalación de MBAM instale correctamente la característica de servidor de administración y supervisión, MBAM mostrará mensajes de error cuando intente acceder al sitio web del administrador de MBAM. Este problema se produce por uno de los siguientes motivos:

-   Una o más de las condiciones previas del servidor de administración y supervisión se quitaron después de la instalación de MBAM.

-   Se instalaron uno o varios requisitos previos en el servidor y posteriormente se quitaron antes de ejecutar el programa de instalación de MBAM.

**Solución alternativa:** Revise la documentación de MBAM y confirme que todos los requisitos previos de MBAM estén instalados.

### Al hacer clic en los vínculos de documentación durante la instalación se produce un error de aplicación después de finalizar la instalación

Al hacer clic en un vínculo de documentación durante la instalación y cerrar el programa de instalación haciendo clic en **Cancelar** o **Finalizar** después de que el programa de instalación haya finalizado correctamente, aparece un mensaje de error de la aplicación. El problema se debe a un error de infracción de acceso en el programador de tareas de Windows.

**Solución alternativa:** Nada. Puede ignorar este error.

### Error de MBAM el programa de instalación no quita nuevas bases de datos

Si se produce un error en el programa de instalación de MBAM, es posible que el programa de instalación no quite las bases de datos recién creadas. Esto puede provocar errores durante las instalaciones posteriores.

**Solución alternativa:** Elija un nombre diferente para la instancia de la base de datos durante la instalación posterior.

### El programa de instalación de MBAM no reconoce certificados de clúster válidos de equilibrio de carga de red

Durante la instalación del servidor de administración y supervisión de MBAM con la opción cifrado de red seleccionada, el certificado de clúster no se reconoce como un certificado válido. Se reconoce como válido cuando el certificado para la comunicación con la base de datos está instalado, pero es rechazado por el clúster de equilibrio de carga.

**Solución alternativa:** Confirme que la lista de revocación de certificados (CRL) asociada al certificado sea accesible o use un certificado que no requiera validación con la CRL.

## Información de copyright de notas de versión


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune y WindowsPowerShell son marcas comerciales del grupo de empresas de Microsoft. El resto de marcas comerciales pertenecen a sus respectivos dueños.



## Temas relacionados


[Acerca de MBAM 1.0](about-mbam-10.md)

 

 





