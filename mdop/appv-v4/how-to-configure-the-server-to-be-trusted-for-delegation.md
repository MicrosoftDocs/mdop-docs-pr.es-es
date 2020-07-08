---
title: Cómo configurar el servidor para que sea de confianza para delegación
description: Cómo configurar el servidor para que sea de confianza para delegación
author: dansimp
ms.assetid: d8d11588-17c0-4bcb-a7e6-86b5e4ba7e1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7164b3046671853216b870d68e651fed4fd84695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817750"
---
# Cómo configurar el servidor para que sea de confianza para delegación


Al instalar el software servidor de administración de Microsoft Application Virtualization (App-V), puede elegir instalarlo mediante una arquitectura de sistema distribuido. Si instala la consola, el servicio Web de administración y la base de datos en diferentes equipos, debe configurar el servidor de Internet Information Services (IIS) para que sea de confianza para la delegación. Esto es necesario porque el servicio Web de administración intentará conectar con el almacén de datos de App-V usando las credenciales del administrador de App-V que usa la consola. El servidor de base de datos en el que está instalado el almacén de datos no aceptará las credenciales del administrador del servidor IIS a menos que el servidor IIS esté configurado para ser de confianza para la delegación, por lo que el servicio Web de administración no podrá conectarse al almacén de datos de App-V.

**Nota:**  Si instala el software de servidor de administración de App-V en un solo servidor y coloca el almacén de datos en un servidor independiente, hay una situación en la que debe configurar el servidor para que sea de confianza para la delegación, aunque el servicio Web de administración y la consola de administración estén en el mismo servidor. Esta situación se produce si necesita conectarse al servicio Web de administración en la consola con la opción **usar credenciales alternativas** .

 

El tipo de delegación que puede usar depende del nivel funcional del dominio que haya configurado en la infraestructura de los servicios de dominio de Active Directory (ADDS). En la siguiente tabla se enumeran los tipos de delegación que se pueden configurar para cada nivel funcional de dominio de App-V. Instrucciones detalladas a continuación de la tabla.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nivel funcional del dominio</th>
<th align="left">Niveles de delegación disponibles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows 2000 nativo</p></td>
<td align="left"><ul>
<li><p>Sin delegación (predeterminado)</p></li>
<li><p>Delegación sin restricciones</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server 2003, Windows Server 2008 o Windows Server 2008 R2</p></td>
<td align="left"><ul>
<li><p>Sin delegación (predeterminado)</p></li>
<li><p>Delegación sin restricciones ¹</p></li>
<li><p>Delegación restringida (usar solo protocolos Kerberos)</p></li>
<li><p>Delegación restringida (usar cualquier protocolo de autenticación) ¹</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

¹ no recomendado.

## Para configurar la delegación no restringida cuando el nivel funcional del dominio es Windows 2000 nativo


En el controlador de dominio del dominio del servidor Web, complete los pasos siguientes.

****

1.  Haga clic en **Inicio**, **herramientas administrativas**y **usuarios y equipos de Active**Directory.

2.  Expanda dominio y, a continuación, expanda la carpeta equipos.

3.  En el panel derecho, haga clic con el botón secundario en el nombre del equipo del servidor Web y, a continuación, haga clic en **propiedades**.

4.  En la pestaña **General** , asegúrese de que la casilla **confiar en el equipo para la delegación** está activada.

5.  Haga clic en **Aceptar**.

## Para configurar la delegación no restringida cuando el nivel funcional del dominio es Windows Server 2003, Windows Server 2008 o Windows Server 2008 R2


En el controlador de dominio del dominio del servidor Web, complete los pasos siguientes.

****

1.  Haga clic en **Inicio**, seleccione **herramientas administrativas**y, a continuación, haga clic en **usuarios y equipos de Active**Directory.

2.  Expanda dominio y expanda la carpeta equipos.

3.  En el panel derecho, haga clic con el botón secundario en el nombre del equipo del servidor Web, seleccione **propiedades**y, a continuación, haga clic en la pestaña **delegación** .

4.  Haga clic para seleccionar **confiar en este equipo para la delegación a cualquier servicio (solo Kerberos)**.

5.  Haga clic en **Aceptar**.

## Para configurar la delegación restringida cuando el nivel funcional del dominio es Windows Server 2003, Windows Server 2008 o Windows Server 2008 R2


En el controlador de dominio del dominio del servidor Web, complete los pasos siguientes.

****

1.  Haga clic en **Inicio**, seleccione **herramientas administrativas**y, a continuación, haga clic en **usuarios y equipos de Active**Directory.

2.  Expanda dominio y, a continuación, expanda la carpeta equipos.

3.  En el panel derecho, haga clic con el botón secundario en el nombre del equipo del servidor Web, seleccione **propiedades**y, a continuación, haga clic en la pestaña **delegación** .

4.  Haga clic para seleccionar **confiar en este equipo para la delegación solo a los servicios especificados**.

5.  Asegúrese de que la selección de **usar solo Kerberos** está seleccionada y, a continuación, haga clic en **Aceptar**.

6.  Haga clic en el botón **Agregar** . En el cuadro de diálogo **Agregar servicios** , haga clic en **usuarios o equipos**y, a continuación, busque o escriba el nombre del Microsoft SQL Server que tiene el almacén de datos de App-V y para recibir las credenciales de usuario de IIS. Haga clic en **Aceptar**.

7.  En la lista **available Services** , seleccione el servicio MSSQLSvc que indica el número de puerto en el que Microsoft SQL Server acepta conexiones para la base de datos de App-V (el puerto predeterminado es 1433). Haga clic en **Aceptar**.

### Pasos adicionales para configurar IIS 7 para la delegación restringida

Si está ejecutando el servicio Web de administración en un servidor IIS 7, debe completar los siguientes pasos para establecer la variable *useAppPoolCredentials* de IIS 7 en true.

1.  Abra una ventana de símbolo del sistema con privilegios elevados. Para abrir una ventana de símbolo del sistema con privilegios elevados, haga clic en **Inicio**, seleccione **todos los programas**, **accesorios**, haga clic con el botón derecho en **símbolo del sistema**y seleccione **Ejecutar como administrador**.

2.  Vaya a%WINDIR%\\system32\\inetsrv.

3.  Escriba **appcmd.exe set config-Section: System. WebServer/Security/Authentication/windowsAuthentication-useAppPoolCredentials: true**y, a continuación, presione Entrar.

 

 





