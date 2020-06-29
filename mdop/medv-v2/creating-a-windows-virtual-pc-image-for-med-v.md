---
title: Crear una imagen de Windows Virtual PC para MED-V
description: Crear una imagen de Windows Virtual PC para MED-V
author: dansimp
ms.assetid: fd7c0b1a-0769-4e7b-ad1a-dad19cca081f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: f947479776e84a4c54edb10d583dd21d7ccf6f43
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812686"
---
# Crear una imagen de Windows Virtual PC para MED-V


Antes de poder enviar un área de trabajo de MED-V a los usuarios, primero debe preparar un disco duro virtual que use para crear el paquete del instalador de área de trabajo de MED-V para virtualización de escritorio de Microsoft Enterprise (MED-V) 2,0. Para preparar el disco duro virtual necesario, debe crear una imagen de Windows Virtual PC que contenga el sistema operativo, las actualizaciones y el software necesarios para poder implementar más tarde la información de redireccionamiento de direcciones URL y las aplicaciones para los usuarios. Esta sección proporciona instrucciones sobre cómo crear el disco duro virtual.

Para crear una imagen virtual para MED-V, debe seguir estos pasos.

1.  [Crear una imagen de Windows Virtual PC](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc)

2.  [Instalar Windows XP en la imagen](#bkmk-installingwindowsxpontovpc)

3.  [Instalar .NET Framework en la imagen](#bkmk-installingnet)

4.  [Aplicar actualizaciones a la imagen](#bkmk-applypatchestovpc)

5.  [Instalar componentes de integración](#bkmk-installintegration)

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a>Crear una imagen de Windows Virtual PC


Para crear una imagen de Windows Virtual PC, consulte la documentación de Windows Virtual PC:

-   [Página principal de Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=148103) ( https://go.microsoft.com/fwlink/?LinkId=148103) .

-   [Ayuda de Virtual PC de Windows](https://go.microsoft.com/fwlink/?LinkId=182378) ( https://go.microsoft.com/fwlink/?LinkId=182378) .

Como alternativa, si ya tiene un archivo de imágenes de Windows (WIM) que desea usar como base para la imagen virtual, puede convertirlo en un VHD que use para crear el área de trabajo de MED-V. Para obtener más información sobre cómo convertir un WIM en un disco duro virtual, consulte [compatibilidad nativa de VHD en Windows 7](https://go.microsoft.com/fwlink/?LinkId=195922) ( https://go.microsoft.com/fwlink/?LinkId=195922) .

**Importante**  MED-V solo admite un disco duro virtual por máquina virtual y solo una partición en cada disco virtual.

 

Una vez que haya creado el disco duro virtual, instale Windows XP en la imagen.

## <a href="" id="bkmk-installingwindowsxpontovpc"></a>Instalar Windows XP en una imagen de Windows Virtual PC


MED-V requiere que Windows XP SP3 esté instalado en la imagen de Windows Virtual PC antes de crear el área de trabajo de MED-V.

Para obtener más información sobre cómo instalar Windows XP, consulte [crear una máquina virtual e instalar un sistema operativo invitado](https://go.microsoft.com/fwlink/?LinkId=182379) ( https://go.microsoft.com/fwlink/?LinkId=182379) .

## <a href="" id="bkmk-installingnet"></a>Instalar .NET Framework 3,5 SP1 en una imagen de Windows Virtual PC


Debe instalar manualmente .NET Framework 3,5 SP1 y la actualización KB959209 en la imagen de Windows Virtual PC que preparará para usar con MED-V. La actualización [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) (se https://go.microsoft.com/fwlink/?LinkId=204950) ocupa de varios problemas de compatibilidad de aplicaciones conocidos.

## <a href="" id="bkmk-applypatchestovpc"></a>Aplicación de actualizaciones a la imagen de Windows Virtual PC


Una vez que haya instalado Windows XP en la máquina virtual, instale las actualizaciones de Windows XP necesarias en la imagen, como SP3. También puede instalar ciertas actualizaciones opcionales para mejorar el rendimiento.

**Importante**  MED-V requiere que el SP3 de Windows XP se ejecute en el sistema operativo invitado.

 

**ADVERTENCIA**  Al instalar actualizaciones de Windows XP, asegúrese de que permanece en la versión de Internet Explorer en el invitado que desea usar en el área de trabajo de MED-V. Por ejemplo, si tiene previsto ejecutar Internet Explorer 6 en el área de trabajo de MED-V, asegúrese de que las actualizaciones que instale ahora no incluyan Internet Explorer 7 o Internet Explorer 8. Además, le recomendamos que configure el registro para evitar que actualizaciones automáticas se actualice en Internet Explorer.

 

### Instalar una actualización de rendimiento opcional

Aunque es opcional, le recomendamos que instale la siguiente actualización para la [revisión KB972435](https://go.microsoft.com/fwlink/?LinkId=201077) ( https://go.microsoft.com/fwlink/?LinkId=201077) . Esta actualización aumenta el rendimiento de las carpetas compartidas en una sesión de servicios de Terminal Server:

**Nota:**  La actualización está disponible públicamente. Sin embargo, es posible que se le pida que acepte un contrato de servicios de Microsoft. Siga las indicaciones en las páginas web sucesivas para recuperar este Hotfix.

 

### Configuración de una actualización de rendimiento de directiva de grupo

De forma predeterminada, la Directiva de grupo se descarga en un equipo de un byte cada vez. Esto provoca retrasos mientras se une MED-V al dominio. Para aumentar el rendimiento de la Directiva de grupo, establezca el siguiente valor de clave del registro en el registro:

Subclave del registro: HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Winlogon

Entrada: BufferPolicyReads

Tipo: DWORD

Valor: 1

## <a href="" id="bkmk-installintegration"></a>Instalar componentes de integración


Windows Virtual PC incluye el paquete de componentes de integración. Esto proporciona características que mejoran la interacción entre el entorno virtual y el equipo físico. Por ejemplo, el paquete de componentes de integración permite que el ratón se mueva entre el host y los equipos invitados.

**Importante**  MED-V requiere la instalación del paquete de componentes de integración.

 

Al configurar la imagen virtual para que funcione con MED-V, debe instalar manualmente el paquete de componentes de integración en el sistema operativo invitado para que las características de integración estén disponibles.

Para obtener más información sobre cómo instalar y usar el paquete de componentes de integración, vea lo siguiente:

-   [Instalar o actualizar el paquete de componentes de integración](https://go.microsoft.com/fwlink/?LinkId=195923) ( https://go.microsoft.com/fwlink/?LinkId=195923) .

-   [Acerca de las características de integración](https://go.microsoft.com/fwlink/?LinkId=195924) ( https://go.microsoft.com/fwlink/?LinkId=195924) .

### Instalar la actualización de RemoteApp

Después de instalar el paquete de componentes de integración, se le pedirá que instale la siguiente actualización: "actualización para Windows XP SP3 para habilitar RemoteApp". Este es un componente obligatorio para MED-V.

**Importante**  Si no se le pide que instale la actualización de RemoteApp, debe descargarla e instalarla manualmente. Para obtener más información e instrucciones sobre cómo descargar esta actualización, consulte [actualización para Windows XP SP3 para habilitar RemoteApp](https://go.microsoft.com/fwlink/?LinkId=195925) ( https://go.microsoft.com/fwlink/?LinkId=195925) .

 

### Habilitar el escritorio remoto

De forma predeterminada, el escritorio remoto está habilitado después de instalar el paquete de componentes de integración. Para que MED-V funcione, asegúrese de que el escritorio remoto está habilitado y no distribuya ninguna directiva de grupo que la deshabilite.

Para obtener información sobre cómo habilitar el escritorio remoto, consulte [habilitar o deshabilitar el escritorio remoto](https://go.microsoft.com/fwlink/?LinkId=201162) ( https://go.microsoft.com/fwlink/?LinkId=201162) .

## Personalizar Internet Explorer con el kit de administración de Internet Explorer


Si lo desea, puede usar el kit de administración de Internet Explorer para personalizar Internet Explorer en el sistema operativo invitado. Para obtener más información, consulte la [Guía de implementación y el kit de administración de Internet Explorer 6](https://go.microsoft.com/fwlink/?LinkId=200007) (http://go.Microsoft.com/fwlink/?LinkId=200007).

**ADVERTENCIA**  Debe tener en cuenta las preocupaciones de seguridad relacionadas con la personalización de Internet Explorer en el área de trabajo de MED-V. Para obtener más información, vea [procedimientos recomendados de seguridad para las operaciones de MED-V](security-best-practices-for-med-v-operations.md).

 

Una vez instalado el disco duro virtual con un sistema operativo invitado actualizado, puede instalar aplicaciones en la imagen.

## Temas relacionados


[Instalar aplicaciones en una imagen de Windows Virtual PC](installing-applications-on-a-windows-virtual-pc-image.md)

[Configurar una imagen de Windows Virtual PC para MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

 

 





