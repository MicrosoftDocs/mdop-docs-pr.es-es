---
title: Compactación de disco duro Virtual MED-V
description: Compactación de disco duro Virtual MED-V
author: dansimp
ms.assetid: 5e6122d1-9847-4b33-adab-594919eec3c5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f71aefb1e4e901078b4d0a421065b7bd5acdf0ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823280"
---
# Compactación de disco duro Virtual MED-V


Aunque es opcional, puede compactar el disco duro virtual (VHD) para recuperar espacio en disco vacío y reducir el tamaño del VHD antes de configurar la imagen de Windows Virtual PC.

**Importante**  Antes de continuar, cree una copia de seguridad de la imagen de Windows XP.

 

**Preparando el disco duro virtual**

1.  Abra la imagen de Windows XP.

    Haga clic en **Inicio**, haga clic en **todos los programas**, en **Windows Virtual PC**, en **Windows Virtual PC**y, a continuación, haga doble clic en la imagen de Windows XP.

2.  Borrar la caché de DLL.

    1.  En un símbolo del sistema de la máquina virtual, escriba **SFC/CacheSize = 1**.

    2.  Reinicie la máquina virtual.

    3.  En un símbolo del sistema de la máquina virtual, escriba **SFC/Purgecache**.

3.  Elimine los archivos innecesarios, como desinstaladores, archivos temporales, archivos de registro, archivos de paginación, carpetas compartidas, etc.

4.  Desactive Restaurar sistema. También puede especificar este paso en el archivo Sysprep. inf.

    1.  En el **Panel de control**, haga doble clic en **sistema**y, a continuación, seleccione la pestaña **Restaurar sistema** .

    2.  Seleccione **Desactivar Restaurar sistema**y, a continuación, haga clic en **Aceptar**.

5.  Establezca los tamaños máximos del registro de eventos y borre todos los eventos.

    1.  Abra el visor de eventos.

        Haga clic en **Inicio**, haga clic en **Panel de control**, haga doble clic en **herramientas administrativas**y, a continuación, haga doble clic en **visor de eventos**.

    2.  Haga clic con el botón secundario en la **aplicación**y haga clic en **propiedades**.

    3.  En el área **tamaño del registro** , establezca **el tamaño máximo del registro** en 512 KB y, después, seleccione **sobrescribir eventos cuando sea necesario**.

    4.  Haga clic en **Borrar registro**. En el cuadro de diálogo **visor de eventos** que aparece, haga clic en **no**.

    5.  En la ventana **propiedades** , haga clic en **Aceptar**.

    6.  Repita los pasos del a al e para los registros de **seguridad** y **del sistema** .

6.  Ejecute la herramienta liberador de espacio en disco.

    Haga clic en **Inicio**, seleccione **todos los programas**, **accesorios**, **herramientas del sistema**y, a continuación, haga clic en **liberador de espacio en disco**.

7.  Configure el archivo de paginación según sea necesario para las aplicaciones.

    1.  En el **Panel de control**, haga doble clic en **sistema**y, a continuación, seleccione la pestaña **avanzado** .

    2.  En el área **rendimiento** , haga clic en **configuración**.

    3.  En el área **memoria virtual** , haga clic en **cambiar**.

    4.  Configure la configuración del archivo de página.

8.  Cierre la imagen de Windows XP.

**Desfragmentar y precompactar el disco duro virtual**

1.  En el **Panel de control** del equipo host que ejecuta Windows 7, haga clic en **herramientas administrativas**, haga doble clic en **Administración de equipos**y, a continuación, haga clic en administración de **discos**.

2.  Con la consola de administración de discos, adjunte (Monte) el disco duro virtual y, a continuación, desfragmente el disco.

3.  Mediante una herramienta de extracción ISO, extraiga el precompacto. ISO que se encuentra en la carpeta \\Archivos de Files\\Windows virtual PC\\Integration componentes.

4.  Use el programa precompact.exe para comprimir el disco duro virtual de Windows XP.

5.  Con la consola de administración de discos, desconecte el disco duro virtual.

**Compactando el disco duro virtual**

1.  Abra Windows Virtual PC.

    Haga clic en **Inicio**, seleccione **todos los programas**, haga clic en **Windows Virtual PC**y, a continuación, haga clic en **Windows Virtual PC**.

2.  Haga clic con el botón derecho en la imagen de Windows XP y seleccione **configuración**.

3.  Haga clic en **disco duro** para el que corresponde a la imagen de Windows XP y, a continuación, haga clic en **modificar**.

4.  Haga clic en **compactar disco duro virtual**.

5.  Haga clic en **compactar** y en **Aceptar**.

Cree una copia de seguridad de su disco duro virtual compactado.

## Temas relacionados


[Configurar una imagen de Windows Virtual PC para MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

[Referencia técnica de MED-V](technical-reference-for-med-v.md)

 

 





