---
title: Solución de problemas de MED-V
description: Solución de problemas de MED-V
author: dansimp
ms.assetid: f43dae36-6485-4e06-9c66-0a646e27079d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38d13be699a92368ff258026acd8e0d5f0e28cd6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825861"
---
# Solución de problemas de MED-V


Esta sección proporciona información para ayudar a solucionar problemas generales con la virtualización de escritorio de Microsoft Enterprise (MED-V).

## Cambiar la resolución del host y, a continuación, maximizar el área de trabajo de MED-V hace que el escritorio aparezca en negro


Al trabajar en el modo de escritorio completo, si cambia la resolución del host y, a continuación, maximiza la ventana del área de trabajo de MED-V, el escritorio aparecerá en negro y el área de trabajo de MED-V podría no responder.

### Solución

Detenga y, a continuación, inicie el área de trabajo de MED-V.

## Iniciar un área de trabajo de MED-V con un adaptador de red deshabilitado y, posteriormente, habilitar el adaptador no restaura la conectividad de red


Si configura un área de trabajo de MED-V en modo puente y, a continuación, inicia el área de trabajo de MED-V mientras un adaptador de red está deshabilitado, si el adaptador está habilitado posteriormente, no se restaurará la conectividad de red a través de ese adaptador.

### Solución

Detenga y, a continuación, inicie el área de trabajo de MED-V.

## Solo un usuario de Windows por equipo puede usar una imagen


Una imagen del área de trabajo de MED-V solo la puede usar el usuario de Windows que haya descargado o importado la imagen. Este usuario es el único usuario aparte de los administradores que tienen permisos en la carpeta donde se encuentran las imágenes descargadas.

### Solución

Cambie manualmente la lista de control de acceso (ACL) en el almacén de imágenes.

## Al instalar MED-V mediante el administrador de configuración con derechos de usuario habilitados, se produce un error en la desinstalación


Si MED-V se instala con Microsoft System Center Configuration Manager y el modo de ejecución del paquete se establece en derechos de usuario, se producirá un error durante la desinstalación con un mensaje de error que indica que solo los usuarios administrativos pueden desinstalar MED-V.

### Solución

Al crear un paquete de Configuration Manager para MED-V, establezca el modo de ejecución en derechos administrativos.

## Al instalar MED-V mediante un sistema de implementación corporativa, si la instalación está configurada para ejecutar el cliente después de la instalación, no podrá ejecutar el cliente.


Si MED-V se instala mediante un sistema de implementación empresarial y el paquete de instalación está configurado para ejecutar el cliente de MED-V después de la instalación, después de que el cliente se esté ejecutando en la cuenta del sistema, no podrá ver que el cliente está ejecutándose (excepto en el área de notificación) y no podrá interactuar con él.

### Solución

Al instalar MED-V mediante un sistema de implementación corporativa, use el parámetro *iniciar \ _MEDV = 0* . msi.

## La imagen de prueba de MED-V no se inicia


Si una imagen de prueba de MED-V no se inicia, nunca se recuperará y se producirá un error en todas las iniciaciones futuras con el mensaje de error "GINA no se cargó".

### Solución

Elimine la imagen de prueba existente y, a continuación, vuelva a crearla.

## Después de intentar unirse a un dominio con las credenciales incorrectas, la imagen nunca se puede unir al dominio.


Si hay un error de configuración en el bloque de creación de dominio de unirse, que forma parte de la secuencia de comandos de configuración de primera hora de la máquina virtual, se produce un error en el área de trabajo de MED-V al intentar unirse a un dominio. Después de que se repare el error de configuración, la imagen incluida en el área de trabajo de MED-V no se puede unir al dominio.

### Solución

Si la imagen se ha implementado, redistribuya la imagen. Si la imagen era una imagen de prueba, vuelva a crear la imagen.

## MED-V no admite varios monitores


MED-V no admite la visualización de aplicaciones publicadas en varios monitores. Es posible que las aplicaciones publicadas y otras ventanas cliente se muestren en la pantalla incorrecta y, a veces, después de que una pantalla se desconecte, MED-V intenta enviar la pantalla al monitor para que el monitor conectado aparezca en blanco.

### Solución

Desconecte la pantalla adicional y reinicie el cliente.

## Es posible que el área de trabajo de MED-V no se inicie si el host se bloquea durante el inicio del área de trabajo de MED-V


Si el host se bloquea durante el proceso de inicio del área de trabajo de MED-V y aparece un mensaje de error que dice "falta el elemento raíz", el área de trabajo de MED-V puede agregar datos a un archivo de configuración de máquina virtual (VMC) vacío, lo que provocará errores en el proceso de inicio.

### Solución

Reemplace el archivo VMC vacío por un archivo VMC de la imagen base.

## El teclado no responde en las ventanas de la aplicación publicadas


En un área de trabajo de MED-V, si presiona la tecla del logotipo de Windows cuando una aplicación publicada está en el foco, el teclado ya no responde en las ventanas de la aplicación publicadas.

### Solución

Presione la tecla del logotipo de Windows mientras una aplicación publicada está en el foco.

## Un área de trabajo de dominio MED-V no actualiza las credenciales de dominio


Al usar un área de trabajo de MED-V persistente en un entorno de dominio, si cambia la contraseña de dominio, el cliente de MED-v no actualiza las credenciales de dominio del área de trabajo de MED-V. Cuando una aplicación publicada intenta acceder a un recurso de red, recibirá un mensaje de error que le notificará que sus credenciales han expirado.

### Solución

Reinicie el sistema operativo de área de trabajo MED-V.

## Las ventanas de aplicaciones publicadas maximizadas cubren la barra de tareas del anfitrión


Si maximiza una ventana publicada de la aplicación a pantalla completa, puede que cubra la barra de tareas host.

### Solución

Realiza una de las siguientes acciones:

Minimice la ventana publicada de la aplicación para obtener acceso al área de notificación y reinicie el área de trabajo de MED-V.

Minimice la ventana publicada de la aplicación y, a continuación, restaure la ventana a su estado maximizado.

## No funciona la adición de usuarios o grupos en el administrador de configuración de servidor de MED-V


Al agregar usuarios o grupos en el cuadro de diálogo **Seleccionar usuarios o grupos** , los usuarios o grupos seleccionados no se agregan a la lista de control de acceso en el administrador de configuración de MED-V Server.

### Solución

Agregue usuarios o grupos mediante el cuadro de diálogo **Escriba los nombres de usuario o grupo** . Para obtener información detallada, vea [Cómo instalar y configurar el componente de servidor MED-V](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).

## MED-V no funciona en equipos con Windows Virtual PC para Windows 7 instalado


MED-V requiere PC2007 virtual de Windows. Windows Virtual PC para Windows7 y virtual PC2007 SP1 no se puede instalar en el mismo equipo.

### Solución

Desinstale Virtual PC para Windows7 antes de instalar virtual PC2007 SP1 y MED-V.

## <a href="" id="med-v-does-not-support-virtual-pc-and-windows-xp-mode-images-"></a>MED-V no admite imágenes de modo virtual PC y WindowsXP


MED-V 1.0 SP1 no admite imágenes creadas por Windows Virtual PC para Windows7. Si se usa una imagen de Virtual PC para Windows7, se producirá un error en el cliente durante el inicio.

### Solución

Cree imágenes de MED-V mediante el uso de virtual PC2007 SP1.

## Firewall de Windows bloquea la actividad de red de virtual PC2007 SP1


De forma predeterminada, Firewall de Windows bloquea la actividad de red de virtual PC2007 SP1 y, cuando virtual PC2007 SP1 se inicia en el equipo cliente, hay un mensaje de firewall que bloquea su secuencia de inicio y todo el acceso a la red.

### Solución

Actualice la excepción del firewall mediante la Directiva de grupo antes de que el usuario final use el MED-V.

## Al actualizar al cliente, aparece un mensaje de error


Al actualizar el cliente de MED-V 1.0 a MED-V 1.0 SP1, puede que aparezca un mensaje que le notifique que no se ha definido ningún área de trabajo de MED-V.

### Solución

Cierre el cliente y reinícielo.

## Temas relacionados


[Notas de la versión de MED-V 1.0](med-v-10-release-notesmedv-10.md)

[MED-V 1.0 SP1 y notas de la versión de SP2](med-v-10-sp1-and-sp2-release-notesmedv-10-sp1.md)

 

 





