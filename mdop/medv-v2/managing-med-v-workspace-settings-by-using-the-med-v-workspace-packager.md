---
title: Administrar la configuración de área de trabajo de MED-V mediante el uso del empaquetador de área de trabajo de MED-V
description: Administrar la configuración de área de trabajo de MED-V mediante el uso del empaquetador de área de trabajo de MED-V
author: dansimp
ms.assetid: e4b2c516-b9f8-44f9-9eae-caac6c2af3e7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9905c8da0f1f0678cce9587296526e8f04493c20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10826121"
---
# Administrar la configuración de área de trabajo de MED-V mediante el uso del empaquetador de área de trabajo de MED-V


Puede usar el Empaquetador de área de trabajo de MED-V para administrar determinadas opciones de configuración en el área de trabajo de MED-V.

**Para administrar la configuración de un área de trabajo de MED-V**

1. Para abrir el **Empaquetador de área de trabajo de MED-V**, haga clic en **Inicio**, haga clic en **todos los programas**, en **Microsoft Enterprise Desktop Virtualization**y, a continuación, haga clic en **Empaquetador de área de trabajo de MED-V**.

2. En el panel principal de **empaquetador del área de trabajo de MED-V** , haga clic en **Administrar configuración**.

3. En la ventana **Administrar configuración** , puede configurar las siguientes opciones del área de trabajo de MED-V:

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
   <td align="left"><p>El área de trabajo de MED-V se inicia de una de estas dos maneras: cuando el usuario final inicia sesión o cuando realiza una acción que requiere MED-V, como abrir una aplicación publicada o especificar una dirección URL que requiere redireccionamiento.</p>
   <p>Puede definir esta configuración para el usuario final o permitir que el usuario final controle el inicio de MED-V.</p>
   <div class="alert">
   <strong>Nota</strong><br/><p>Si especifica que el usuario final decide, el comportamiento predeterminado que experimentan es que el área de trabajo de MED-V se inicia cuando inicia sesión. Pueden cambiar el valor predeterminado haciendo clic con el botón derecho en el icono MED-V en el área de notificación y seleccionando <strong> configuración de usuario de Med-v </strong> . Si define esta configuración para el usuario final, no puede cambiar la forma en que se inicia MED-V.</p>
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
   <p>La credencial de dominio del usuario final se almacena en un formato reversible en el administrador de credenciales de Windows. Un atacante podría escribir un programa que recupere la contraseña y, por lo tanto, obtuviera acceso a las credenciales del usuario. Solo puede reducir este riesgo deshabilitando el almacenamiento de las credenciales de usuario final.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



4. Haga clic en **Guardar como...** para guardar los valores de configuración actualizados en la carpeta especificada. MED-V crea un archivo de registro que contiene la configuración actualizada. Implemente el archivo de registro actualizado mediante una directiva de grupo. Para obtener más información acerca de cómo usar la Directiva de grupo, consulte [instalación de software de directiva de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .

   MED-V también crea un script de Windows PowerShell en la carpeta especificada que puede usar para volver a crear este archivo de registro actualizado.

## Temas relacionados


[Administrar opciones de configuración de área de trabajo de MED-V](managing-med-v-workspace-configuration-settings.md)

[Administrar la configuración del área de trabajo de MED-V](manage-med-v-workspace-settings.md)









