---
title: Novedades de UE-V 2.1
description: Novedades de UE-V 2.1
author: dansimp
ms.assetid: 7f385183-7d97-4602-b19a-baa710334ade
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7816fc8309a29347048172b2104750140c483587
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826261"
---
# Novedades de UE-V 2.1


Virtualización de la experiencia del usuario 2,1 ofrece estas nuevas características y funcionalidades comparadas con UE-V 2,0. Las [notas de la versión de virtualización de la experiencia del usuario de Microsoft (UE-V) 2,1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md) proporcionan más información sobre la versión de UE-v 2,1.

## Plantilla de ubicación de configuración de Office 2013


UE-V 2,1 incluye la plantilla de ubicación configuración de Microsoft Office 2013, con compatibilidad de firma de Outlook mejorada. En UE-V 2,1, los datos de firma se sincronizan entre los dispositivos de usuario. Hemos agregado la sincronización de la configuración de firma predeterminada para mensajes de correo electrónico nuevos, de respuesta y reenviados. Los clientes ya no tienen que elegir la configuración de firma predeterminada.

**Nota:**  Debe crearse un perfil de Outlook para cualquier dispositivo en el que un usuario desee sincronizar su firma de Outlook. Si el perfil aún no se ha creado, el usuario puede crear uno y, a continuación, reiniciar Outlook en ese dispositivo para habilitar la sincronización de firmas.

 

Anteriormente UE-V incluía plantillas de ubicación de configuración de Microsoft Office 2010 que se distribuyeron automáticamente y se registraron en el agente de UE-V. UE-V 2,1 funciona con Office 365 para determinar si la configuración de Office 2013 se ha desplazado con Office 365. Si la configuración se mueve con Office 365, no se desplazará con UE-V. [Información general sobre la configuración de usuario y de itinerancia de Office 2013](https://go.microsoft.com/fwlink/p/?LinkID=391220) proporciona más información.

Para habilitar la sincronización de configuración mediante UE-V 2,1, realice una de las siguientes acciones:

-   Usar una directiva de grupo para deshabilitar la sincronización de Office 365

-   No habilite la experiencia de sincronización de Office 365 durante la instalación de Office 2013

UE-V 2,1 incluye [plantillas de office 2013 y office 2010](https://technet.microsoft.com/library/dn458932.aspx#autosyncsettings). Esta versión elimina las plantillas de Office 2007. Los usuarios pueden seguir usando las plantillas de Office 2007 de UE-V 2,0 o versiones anteriores y aún así pueden obtener las plantillas de la galería de plantillas de UE-V que se encuentran [aquí](https://go.microsoft.com/fwlink/p/?LinkID=246589).

## Corrección para los usuarios del espacio de nombres del sistema de archivos distribuido


UE-V ha mejorado la compatibilidad con el espacio de nombres del sistema de archivos distribuido (DFSN) agregando una configuración de UE-V llamada SyncProviderPingEnabled. Si deshabilita esta configuración con PowerShell o WMI, los usuarios podrán deshabilitar el ping de UE-V. La versión de ping de UE-V causa un error al usar servidores de DFSN porque estos servidores no responden a los ping. La no respuesta impide que UE-V sincronice la configuración. Deshabilitar el ping de UE-V permite que la sincronización de UE-V funcione con normalidad.

Para deshabilitar UE-V ping, use este cmdlet de PowerShell:

``` syntax
Set-UevConfiguration -DisableSyncProviderPing
```

## Sincronización de credenciales


UE-V 2,1 ofrece a los clientes la posibilidad de sincronizar credenciales y certificados almacenados en el administrador de credenciales de Windows. Este componente está deshabilitado de forma predeterminada. Habilitar este componente permite a los usuarios mantener sus credenciales de dominio y certificados sincronizados. Los usuarios pueden iniciar sesión una vez en un dispositivo y estas credenciales se transferirán a ese usuario en todos los dispositivos habilitados para UE-V. [Administrar credenciales con UE-V 2,1](https://technet.microsoft.com/library/dn458932.aspx#creds) proporciona más información.

**Nota:**  En Windows 8 y versiones posteriores, el administrador de credenciales contiene credenciales Web. Estas credenciales no se sincronizan entre los dispositivos de los usuarios.

 

## UE-V y sincronización de cuentas de Microsoft


UE-V detecta si "configuración de sincronización con OneDrive", también conocida como sincronización de cuenta Microsoft, está activada. Si la cuenta Microsoft no está configurada para sincronizar la configuración, UE-V sincroniza las aplicaciones de Windows, los paquetes AppX y la configuración del escritorio de Windows entre los dispositivos. Esto permite que los usuarios tengan acceso a sus aplicaciones de la tienda, música, imágenes y otras aplicaciones habilitadas para la cuenta de Microsoft sin sincronizar fuera del firewall de la empresa. UE-V comprueba si la Directiva de grupo dejará de sincronizar la configuración con OneDrive o si el usuario deshabilita la **sincronización de la configuración en este equipo** en los controles de usuario.

## Compatibilidad con el SyncMethod externo


Una nueva [configuración de SyncMethod](https://technet.microsoft.com/library/dn554321.aspx) denominada **externo** especifica que, si se escribe la configuración de UE-V en una carpeta local en el equipo del usuario, cualquier motor de sincronización externo (como OneDrive para la empresa, carpetas de trabajo, SharePoint o Dropbox) se puede usar para aplicar esta configuración a los diferentes equipos a los que los usuarios tienen acceso.

## Compatibilidad mejorada para el modo VDI


UE-V 2,1 incluye [soporte técnico para las sesiones de VDI](https://technet.microsoft.com/library/dn458932.aspx#vdi) que se comparten entre los usuarios finales. Como administrador, puede registrar y configurar una plantilla especial de VDI, que garantiza que UE-V mantiene todas sus funciones intactas para las sesiones de VDI no persistentes.

**Nota:**  Si no habilita el modo VDI para las sesiones de VDI no persistentes, algunas características no funcionan, como la copia de seguridad o la restauración y LKG.

 

## Copia de seguridad y restauración administrativas


Puede restaurar la configuración adicional cuando un usuario adopta un nuevo dispositivo colocando una plantilla de ubicación de configuración en un perfil de **copia de seguridad** o **roaming (predeterminado)** con el cmdlet de PowerShell Set-UevTemplateProfile. Esto permite sincronizar la configuración del equipo con el nuevo equipo, además de la configuración del usuario. Se realiza una copia de seguridad de las plantillas asignadas al perfil de copia de seguridad para ese dispositivo y configuradas para cada dispositivo. [Administrar copias de seguridad y restauraciones administrativas en UE-V 2. x](manage-administrative-backup-and-restore-in-ue-v-2x-new-topic-for-21.md) proporciona más información.

## Sincronización de configuración adicional de Windows


UE-V sincroniza ahora la personalización del teclado táctil, el diccionario ortográfico y habilita la sincronización de la aplicación para las aplicaciones recientes y la configuración del borde de la pantalla entre Windows 8 y los dispositivos Windows 8,1.






## Temas relacionados


[Introducción a UE-V 2.x](get-started-with-ue-v-2x-new-uevv2.md)

[Preparar una implementación de UE-V 2. x](prepare-a-ue-v-2x-deployment-new-uevv2.md)

[Notas de la versión de Virtualización de la experiencia del usuario de Microsoft (UE-V) 2.1](microsoft-user-experience-virtualization--ue-v--21-release-notesuevv21.md)

 

 





