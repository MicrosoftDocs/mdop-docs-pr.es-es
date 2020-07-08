---
title: Creación de una imagen de Virtual PC para MED-V
description: Creación de una imagen de Virtual PC para MED-V
author: dansimp
ms.assetid: 5e02ea07-25b9-41a5-a803-d70c55eef586
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 84e45f9ff7213abdd6288bcd750238436d3ab68c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823661"
---
# Creación de una imagen de Virtual PC para MED-V


Para crear una imagen de Virtual PC (VPC) para MED-V, debe hacer lo siguiente:

1.  [Cree una imagen de VPC](#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc).

2.  [Instale el paquete de área de trabajo. msi MED-V en la imagen VPC](#bkmk-howtoinstallthemedvworkspacemsipackage).

3.  [Ejecute la herramienta de requisitos previos de las máquinas virtuales MED-V en la imagen de VPC](#bkmk-howtorunthevirtualmachineprerequisitestool).

4.  [Configure manualmente los requisitos previos de las máquinas virtuales en la imagen de VPC](#bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites).

5.  [Configurar Sysprep para imágenes de MED-V](#bkmk-howtoconfiguresysprepformedvimages) (opcional).

6.  [Desactive Microsoft Virtual PC](#bkmk-turningoffmicrosoftvirtualpc).

## <a href="" id="bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc"></a>Creación de una imagen de Virtual PC con Microsoft Virtual PC


Para crear una imagen de Virtual PC con Microsoft Virtual PC, consulte la documentación de Virtual PC.

Para obtener más información, consulte:

-   [Ayuda de Windows Virtual PC](https://go.microsoft.com/fwlink/?LinkId=182378)

-   [Crear una máquina virtual e instalar un sistema operativo invitado](https://go.microsoft.com/fwlink/?LinkId=182379)

## <a href="" id="bkmk-howtoinstallthemedvworkspacemsipackage"></a>Cómo instalar el paquete de área de trabajo. msi de MED-V


Después de crear la imagen de Virtual PC, instale el paquete de área de trabajo. msi de MED-V en la imagen.

**Para instalar la imagen del área de trabajo de MED-V**

1.  Inicie la máquina virtual y copie el paquete de área de trabajo. msi de MED-V en el interior.

    El paquete de área de trabajo. msi MED-V se llama *MED-V\_workspace\_x.msi*, donde *x* es el número de versión.

    Por ejemplo, *MED-V\_workspace\_1.0.65.msi*.

2.  Haga doble clic en el paquete de área de trabajo. msi de MED-V y siga las instrucciones del Asistente para instalación.

    **Nota**  
    Cuando se publique una nueva versión de MED-V y se actualice una imagen de Virtual PC existente, desinstale el paquete. msi del área de trabajo de MED-V existente, reinicie el equipo e instale el nuevo paquete de área de trabajo de MED-V. msi.



~~~
**Note**  
After the MED-V workspace .msi package is installed, other products that replace GINA cannot be installed.
~~~



## <a href="" id="bkmk-howtorunthevirtualmachineprerequisitestool"></a>Cómo ejecutar la herramienta de requisitos previos para máquinas virtuales


La herramienta de requisitos previos de la máquina virtual (VM) es un asistente que automatiza varios de los requisitos previos.

**Nota**  
Aunque muchos parámetros se pueden configurar en el asistente, no se pueden configurar las propiedades necesarias para el funcionamiento correcto de MED-V.



**Para ejecutar la herramienta de requisitos previos de la máquina virtual**

1.  Después de instalar el paquete de área de trabajo de MED-V. msi, en el menú **Inicio** de Windows, seleccione **herramienta de &gt; &gt; requisitos previos de los programas MED-v VM**.

    **Nota**  
    El usuario que ejecuta la herramienta de requisitos previos de las máquinas virtuales debe tener derechos de administrador local y debe ser el único usuario que haya iniciado sesión.



~~~
The **MED-V VM Prerequisite Wizard Welcome** page appears.
~~~

2. Haz clic en **Siguiente**.

3. En la página **configuración de Windows** , en las siguientes propiedades configurables, seleccione las que desea configurar:

   -   **Borrar la información del historial personal de los usuarios**

   -   **Borrar directorio temporal de perfiles locales**

   -   **Deshabilitar sonidos en los siguientes eventos de Windows: Inicio, Inicio de sesión y cierre de sesión**

   **Nota**  
   No habilitar el protector de páginas de Windows en una directiva de grupo.



4. Haz clic en **Siguiente**.

5. En la página **configuración de Internet Explorer** , en las siguientes propiedades configurables, seleccione las que desea configurar:

   -   **No uses características de autocompletar**

   -   **Deshabilitar la reutilización de Windows para iniciar accesos directos**

   -   **Borrar el historial de navegación**

   -   **Habilitar la exploración por pestañas en Internet Explorer 7**

6. Haz clic en **Siguiente**.

7. En la página **servicios de Windows** , en las siguientes propiedades configurables, seleccione las que desea configurar:

   -   **Servicio centro de seguridad**

   -   **Servicio Programador de tareas**

   -   **Servicio actualizaciones automáticas**

   -   **Servicio de restaurar sistema**

   -   **Servicio de Index Server**

   -   **Configuración inalámbrica rápida**

   -   **Compatibilidad con la conmutación rápida de usuarios**

8. Haz clic en **Siguiente**.

9. En la página de **Inicio de sesión automático de Windows** , haga lo siguiente:

   1.  Active la casilla de verificación **Habilitar el inicio de sesión automático de Windows** .

   2.  Asigne un **nombre de usuario** y una **contraseña**.

10. Haga clic en **aplicar**y, en el cuadro de confirmación que aparece, haga clic en **sí**.

11. En la página **Resumen** , haga clic en **Finalizar** para salir del asistente

**Nota**  
Compruebe que las directivas de grupo no sobrescriben la configuración obligatoria establecida en la herramienta requisitos previos.



## <a href="" id="bkmk-howtoconfiguremedvvirtualmachinemanualinstallationprerequisites"></a>Cómo configurar los requisitos previos de instalación manual de máquinas virtuales de MED-V


Algunas de las configuraciones no se pueden configurar a través de la herramienta de requisitos previos de máquina virtual y se deben realizar de forma manual.

-   Configuración de la máquina virtual

    Se recomienda configurar las siguientes opciones de la máquina virtual en la consola de Microsoft Virtual PC:

    -   Deshabilitar unidades de disquete.

    -   Deshabilitar deshacer discos (**configuración &gt; , deshacer-discos**).

    -   Asegúrese de que la imagen tiene solo una CPU virtual.

    -   Elimine las interacciones entre la máquina virtual y el usuario, donde no están relacionadas con las aplicaciones publicadas (como los mensajes que requieren la intervención del usuario).

-   Configuración de imagen

    Configure las siguientes opciones de configuración manuales dentro de la imagen:

    1.  En la ventana de **propiedades de opciones de energía** , deshabilite la hibernación y la suspensión.

    2.  Aplique las actualizaciones más recientes de Windows.

    3.  En el cuadro de diálogo **Inicio y recuperación de Windows** , en la sección **error del sistema** , desactive la casilla **reiniciar automáticamente** .

    4.  Asegúrese de que la imagen use una clave de licencia VLK.

-   Instalar complementos de VPC

    En el menú **acción** , seleccione **instalar o actualizar Virtual Machine Additions**.

-   Configuración de la impresión

    Puede configurar la impresión desde el área de trabajo MED-V de una de las siguientes maneras:

    -   Agregue una impresora a la máquina virtual.

    -   Permitir la impresión con impresoras que estén configuradas en el equipo host.

## <a href="" id="bkmk-howtoconfiguresysprepformedvimages"></a>Cómo configurar Sysprep para imágenes de MED-V


En un área de trabajo de MED-V, se puede configurar Sysprep para asignar un identificador de seguridad único (SID), especialmente cuando se ejecutan varias áreas de trabajo de MED-V en un solo equipo. No se recomienda usar Sysprep para unirse a un dominio; en su lugar, use la acción de script de dominio de combinación MED-V, como se describe en [Cómo configurar acciones de script](how-to-set-up-script-actions.md).

**Nota**  
Sysprep es la utilidad de preparación del sistema de Microsoft para el sistema operativo Windows.



**Para configurar Sysprep en un área de trabajo de MED-V**

1.  Cree un directorio en la raíz de la unidad del sistema denominada *Sysprep*.

2.  Desde el CD de instalación de Windows, extraiga *deploy.cab* a la raíz de la unidad del sistema o descargue la actualización más reciente de las herramientas de implementación desde el sitio web de Microsoft.

    -   Para Windows 2000, consulte [actualización de las herramientas de implementación para windows 2000](https://go.microsoft.com/fwlink/?LinkId=143001).

    -   Para Windows XP, consulte [actualización de las herramientas de implementación para Windows XP](https://go.microsoft.com/fwlink/?LinkId=143000).

3.  Ejecute el **Administrador de instalación** (setupmgr.exe).

4.  Siga los instrucciones del Asistente para administración de instalación.

Una vez que se ha configurado Sysprep y creado el área de trabajo de MED-V, debe ejecutarse Sysprep.

**Para ejecutar Sysprep**

1.  Desde la carpeta Sysprep ubicada en la raíz de la unidad del sistema, ejecute la herramienta de preparación del sistema (Sysprep.exe).

2.  En el cuadro de mensaje de advertencia que aparece, haga clic en **Aceptar**.

3.  En el cuadro de diálogo **propiedades de Sysprep** , active las casillas **de verificación no restablecer período de gracia para activación** y uso de la **instalación mínima** .

4.  Haga clic en volver a **sellar**.

5.  Si no está satisfecho con la información que se muestra en el cuadro de mensaje de confirmación que aparece, haga clic en **Cancelar** y cambie las selecciones.

6.  Haga clic en **Aceptar** para completar el proceso de preparación del sistema.

## <a href="" id="bkmk-turningoffmicrosoftvirtualpc"></a>Desactivar Microsoft Virtual PC


Después de instalar y configurar todos los componentes, cierre Microsoft Virtual PC y seleccione **desactivar**.

## Temas relacionados


Creación de una imagen de MED-V [Cómo configurar acciones de script](how-to-set-up-script-actions.md)









