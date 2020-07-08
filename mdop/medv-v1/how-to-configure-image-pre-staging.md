---
title: Cómo configurar un ensayo previo de imagen
description: Cómo configurar un ensayo previo de imagen
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826410"
---
# Cómo configurar un ensayo previo de imagen


**Nota:**  La preprueba previa de imagen solo es útil para la descarga de imagen inicial. No es compatible con la actualización de la imagen.

 

## Cómo configurar un ensayo previo de imagen


**Para configurar el ensayo previo de la imagen**

1.  En el equipo cliente, en el directorio del almacén de imágenes, cree una carpeta para la imagen de preensayo y asígnele el nombre *imágenes de MED-V*.

    **Nota:**  Esta carpeta debe llamarse *imágenes de MED-V*.

     

2.  En la carpeta imágenes de MED-V, cree una subcarpeta y asígnele el nombre *PrestagedImages*.

    **Nota:**  Esta carpeta debe llamarse *PrestagedImages*.

     

3.  Para aplicar la seguridad de las listas de control de acceso (ACL) a la carpeta *imágenes de MED-V* , establezca la siguiente ACL:

    **Usuarios de NT AUTHORITY\\Authenticated: (OI) (CI) (acceso especial:)**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 ARCHIVO \ _APPEND \ _DATA**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **NT AUTHORITY\\SYSTEM: (OI) (CI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **Nota:**  Se recomienda aplicar la seguridad de ACL a la carpeta de *imágenes de MED-V* .

     

4.  Para aplicar la seguridad de la ACL a la carpeta *PrestagedImages* , establezca la siguiente ACL:

    **Usuarios de NT AUTHORITY\\Authenticated: (OI) (CI) (acceso especial:)**

    **LEER \ _CONTROL**

    **REALIZA**

    **ARCHIVO \ _GENERIC \ _READ**

    **ARCHIVO \ _READ \ _DATA**

    **ARCHIVO \ _READ \ _EA**

    **ARCHIVO \ _READ \ _ATTRIBUTES**

    **NT AUTHORITY\\SYSTEM: (OI) (CI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **Nota:**  Se recomienda aplicar la seguridad de ACL a la carpeta *PrestagedImages* .

     

5.  Inserta los archivos de imagen (CKM y los archivos de índice) en la carpeta *PrestagedImages*

    **Nota:**  Una vez que los archivos de imagen se hayan insertado en la carpeta prestage, se recomienda ejecutar una comprobación de integridad de datos y marcar los archivos como de solo lectura.

     

6.  Incluya el siguiente parámetro en la instalación del cliente MED-V: *Client.MSI VMSFOLDER = "C:\\MED-V imágenes"*.

## Cómo actualizar la ubicación previa a la fase


**Para actualizar la ubicación previa a la fase**

1.  La clave del registro *PrestagedImagesPath*, señala a la ubicación predeterminada de la imagen. Se encuentra en el siguiente directorio:

    -   En un procesador x86 `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   En un x64 `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  Si la imagen está en una ubicación diferente, cambie la ruta de acceso.

 

 





