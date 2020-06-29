---
title: Cómo recuperar una unidad dañada
description: Cómo recuperar una unidad dañada
author: dansimp
ms.assetid: fa5b846b-dda6-4ae4-bf6c-39e4f1d8aa00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fd9fd8a65d57cbfe965197fa26b57319ee046784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822551"
---
# Cómo recuperar una unidad dañada


Puede usar este procedimiento con el sitio web de administración y supervisión (también se conoce como soporte técnico) para recuperar una unidad dañada que está protegida por BitLocker. Para ello, completará las tareas indicadas en la tabla siguiente.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Detalles y más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Para crear un archivo de paquete de claves de recuperación, acceda al <strong> </strong> área de recuperación de unidades del sitio web de administración y supervisión.</p></td>
<td align="left"><p>Para acceder al <strong> área de recuperación de unidades </strong> , debe tener asignado el rol de usuarios del Departamento de soporte técnico de MBAM o el rol de usuarios avanzados de soporte técnico de MBAM. Es posible que haya dado a estos roles nombres diferentes al crearlos. Para obtener más información, consulte <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)"> planificación de grupos y cuentas de MBAM 2,5 </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Copie el archivo de paquete en el equipo que contiene la unidad dañada.</p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Use el <code>repair-bde</code> comando para completar el proceso de recuperación.</p></td>
<td align="left"><p>Para evitar una posible pérdida de datos, se recomienda encarecidamente que revise el <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)"> comando Manage-BDE </a> antes de usarlo.</p></td>
</tr>
</tbody>
</table>

 

**Para recuperar una unidad dañada**

1.  Abra un explorador Web y vaya al **sitio web de administración y supervisión**.

2.  En el panel izquierdo, seleccione **recuperación de unidades** para abrir la página **recuperar el acceso a una unidad cifrada** .

3.  Escriba el nombre de usuario y el dominio de inicio de sesión de Windows del usuario final, el motivo por el que se desbloquea la unidad y el identificador de contraseña de recuperación del usuario final.

    **Nota:**  Si es miembro del grupo de acceso avanzado de usuarios del servicio de asistencia al usuario, no tiene que escribir el nombre de dominio o el nombre de usuario del usuario.

     

4.  Haz clic en **Enviar**. Se mostrará la clave de recuperación.

5.  Haga clic en **Guardar**y, a continuación, seleccione **paquete de claves de recuperación**. Se creará el paquete de claves de recuperación en el equipo.

6.  Copie el paquete de claves de recuperación en el equipo que tiene la unidad dañada.

7.  Abre un símbolo del sistema con privilegios elevados. Para ello, haga clic en **Inicio** y escriba `cmd` en el cuadro de texto **Buscar programas y archivos** . Haga clic con el botón derecho en **cmd.exe**y seleccione **Ejecutar como administrador**.

8.  En el símbolo del sistema, escriba lo siguiente:

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    **Nota:**  Reemplazar &lt; una *unidad fija* &gt; por una unidad de disco duro disponible que tenga un espacio libre igual o mayor que los datos de la unidad dañada. Los datos de la unidad dañada se recuperan y se mueven a la unidad de disco duro especificada.

     


## Temas relacionados


[Realización de la administración de BitLocker con MBAM 2.5](performing-bitlocker-management-with-mbam-25.md)

 
## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





