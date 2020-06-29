---
title: Procedimientos recomendados de seguridad para las operaciones de MED-V
description: Procedimientos recomendados de seguridad para las operaciones de MED-V
author: dansimp
ms.assetid: 231e2b9a-8b49-42fe-93b5-2ef12fe17bac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4353a15c756dba8cf44f530c2077546e3f9288cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825400"
---
# Procedimientos recomendados de seguridad para las operaciones de MED-V


Como administrador autorizado, usted es responsable de proteger la información de los usuarios y de mantener la seguridad de su organización durante y después de la implementación de áreas de trabajo de MED-V. En particular, tenga en cuenta los siguientes problemas:

**Personalizar Internet Explorer en el área de trabajo de MED-V**. Las versiones anteriores del sistema operativo Windows y de Internet Explorer no son tan seguras como las versiones actuales. Por lo tanto, Internet Explorer en el área de trabajo de MED-V está configurado para evitar la navegación y otras actividades que pueden suponer riesgos de seguridad. Además, la configuración de la zona de seguridad de Internet para Internet Explorer en el área de trabajo de MED-V se establece en el nivel más alto. De forma predeterminada, estas dos configuraciones se establecen en el paquete del área de trabajo de MED-V al crear el paquete del área de trabajo de MED-V.

Al usar el kit de administración de Internet Explorer (IEAK) o cambiar los valores predeterminados en el Empaquetador de área de trabajo de MED-V, puede personalizar Internet Explorer en el área de trabajo de MED-V. Sin embargo, tenga en cuenta que si Personaliza Internet Explorer en el área de trabajo de MED-V de modo que sea menos seguro, puede exponer su organización a los riesgos de seguridad presentes en las versiones anteriores de Internet Explorer.

Desde una perspectiva de seguridad, los procedimientos recomendados para administrar Internet Explorer en el área de trabajo de MED-V son los siguientes:

-   Al crear el paquete de área de trabajo de MED-V, deje los valores predeterminados para que Internet Explorer en el área de trabajo de MED-V se configure para evitar la navegación y otras actividades que pueden suponer riesgos de seguridad.

-   Al crear el paquete de área de trabajo de MED-V, deje los valores predeterminados de forma que la configuración de seguridad de la zona de seguridad de Internet se mantenga en el nivel más alto.

-   Configure el proxy de empresa o el asesor de contenido de Internet Explorer para bloquear dominios que estén fuera de la intranet de la empresa.

**Configurar un área de trabajo de MED-V para todos los usuarios de un equipo compartido.** Al configurar un área de trabajo de MED-V para que todos los usuarios puedan obtener acceso a ella en un equipo compartido, tenga en cuenta que la máquina virtual invitada (VHD) se coloca en una ubicación que concede acceso de lectura y escritura a todos los usuarios de ese sistema.

**Configuración de una cuenta de proxy para unirse a un dominio.** Al configurar una cuenta de proxy para unir máquinas virtuales al dominio, debe saber que un usuario final puede obtener las credenciales de la cuenta de proxy. Por lo tanto, deben tomarse precauciones, como limitar los derechos de usuario de la cuenta, para evitar que un usuario final pueda usar las credenciales para causar daños.

**Configuración de Sysprep.** Aunque el archivo Sysprep. inf está cifrado de forma predeterminada, su contenido puede ser descifrado y leído por cualquier usuario final determinado que pueda iniciar sesión correctamente en la máquina virtual. Esto provoca problemas de seguridad porque el archivo Sysprep. inf puede contener credenciales además de una clave de producto de Windows.

Puede reducir este riesgo configurando una cuenta limitada para unir máquinas virtuales al dominio y especificando las credenciales para esa cuenta cuando configure Sysprep. Como alternativa, también puede configurar Sysprep y la primera instalación para que se ejecute en modo **atendido** y para que los usuarios finales proporcionen sus credenciales para unirse a la máquina virtual en el dominio.

Una práctica recomendada de MED-V es especificar que FtsCompletion.exe se ejecuta en una cuenta que proporciona al usuario final derechos para conectarse al invitado a través del cliente de conexión de escritorio remoto (RDC).

**Autenticación de usuario final.** Habilitar el almacenamiento en caché de las credenciales del usuario final proporciona la mejor experiencia de usuario de MED-V, pero crea la posibilidad de que alguien pueda obtener acceso a las credenciales del usuario final. La única forma de reducir este riesgo es especificando en el **paquete del área de trabajo MED-V** que las credenciales de usuario final no se almacenan. Para obtener más información sobre la autenticación de usuarios finales, consulte [autenticación de usuarios finales de MED-V](authentication-of-med-v-end-users.md).

## Temas relacionados


[Solución de problemas de operaciones](operations-troubleshooting-medv2.md)

[Microsoft Enterprise Desktop Virtualization 2,0](index.md)

 

 





