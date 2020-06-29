---
title: Instalación de software de servidor MBAM 2.5
description: Instalación de software de servidor MBAM 2.5
author: dansimp
ms.assetid: b9dbe697-5400-4bac-acfb-ee6dc6586c30
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6612bf52aa53ae693694d7ac02c5cab212d4e24f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823391"
---
# Instalación de software de servidor MBAM 2.5


En este tema se describe cómo instalar el software de servidor de administración y supervisión de Microsoft BitLocker (MBAM) 2,5 mediante el Asistente de configuración de administración y supervisión de Microsoft BitLocker o mediante parámetros de la línea de comandos. Repita el proceso de instalación del servidor para cada servidor en el que esté configurando las características de servidor de MBAM 2,5. Una vez finalizada la instalación, consulte Configuración de las [características de servidor de MBAM 2,5](configuring-the-mbam-25-server-features.md) para conocer los pasos para configurar las características de servidor.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Antes de empezar</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Revisar la información de planificación de MBAM 2,5</p></td>
<td align="left"><ul>
<li><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</a></p></li>
<li><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configuraciones admitidas de MBAM 2.5</a></p></li>
<li><p><a href="high-level-architecture-for-mbam-25.md" data-raw-source="[High-Level Architecture for MBAM 2.5](high-level-architecture-for-mbam-25.md)">Arquitectura de alto nivel de MBAM 2.5</a></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Leer cómo obtener archivos de registro</p></td>
<td align="left"><p>De forma predeterminada, los archivos de registro se crean en la carpeta% Temp% del equipo local. Para escribir los archivos de registro en una ubicación específica en lugar de en la <strong> carpeta% Temp </strong> %, use el <strong> </strong> &lt; <em> argumento/log ubicación </em> &gt; .</p>
<p>Es posible que se registren eventos adicionales en el visor de eventos de los <strong> nodos MBAM-Setup </strong> o <strong> MBAM-Web </strong> en <strong> las aplicaciones y servicios de &gt; Microsoft &gt; Windows </strong> . Por ejemplo, Si desinstala MBAM, el desinstalador también desinstalará los registros MBAM-setup y MBAM-Web en EventViewer.</p></td>
</tr>
</tbody>
</table>

 

## Instalar el software de servidor MBAM 2,5 con el Asistente para la configuración de administración y supervisión de Microsoft BitLocker


Siga estos pasos para instalar el software de servidor MBAM mediante el Asistente para la configuración de supervisión y administración de Microsoft BitLocker.

**Para instalar el software de servidor MBAM 2,5 con el asistente**

1.  En el servidor en el que desea instalar MBAM, ejecute **MBAMserversetup.exe** para iniciar el Asistente para la configuración de administración y supervisión de Microsoft BitLocker.

2.  En la página **principal** , haga clic en **siguiente**.

3.  Lea y acepte el contrato de licencia de software de Microsoft y, a continuación, haga clic en **siguiente** para continuar con la instalación.

4.  Elija si desea usar Microsoft Update cuando busque actualizaciones y, a continuación, haga clic en **siguiente**.

5.  Elija si desea participar en el programa para la mejora de la experiencia del usuario y, a continuación, haga clic en **siguiente**.

6.  Para iniciar la instalación, haga clic en **instalar**.

7.  Para configurar las características de servidor cuando termine de instalarse el software del servidor MBAM, seleccione la casilla **ejecutar la configuración del servidor después de que se cierre el asistente** . Como alternativa, puede configurar MBAM más adelante con el método abreviado de **configuración del servidor de MBAM** que la instalación del servidor crea en el menú **Inicio** .

8.  Haz clic en **Finalizar**.

## Instalar el software de servidor MBAM 2,5 mediante una ventana de símbolo del sistema


En un símbolo del sistema, escriba un comando similar al siguiente para instalar el software de servidor MBAM.

``` syntax
MbamServerSetup.exe MBAMServerInstall.log
CEIPENABLED=True OPTIN_FOR_MICROFOST_UPDATES=True INSTALLDIR=c:\mbaminstall
```

En la siguiente tabla se describen los parámetros de la línea de comandos para instalar el software de servidor MBAM 2,5.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Parámetro</th>
<th align="left">Valor del parámetro</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CEIPENABLED</p></td>
<td align="left"><p>Verdadero falso</p></td>
<td align="left"><p>Participe en el programa de mejora de la experiencia del cliente, que ayuda a que Microsoft Identifique qué características de MBAM mejorar.</p>
<p>Falso: no participe en el programa de mejora de la experiencia del cliente.</p></td>
</tr>
<tr class="even">
<td align="left"><p>OPTIN_FOR_MICROSOFT_UPDATES</p></td>
<td align="left"><p>Verdadero falso</p></td>
<td align="left"><p>True: Use Microsoft Update para mantener su equipo seguro y actualizado para Windows y otros productos de Microsoft, incluido MBAM.</p>
<p>Falso: no use Microsoft Update</p></td>
</tr>
<tr class="odd">
<td align="left"><p>INSTALLDIR</p></td>
<td align="left"><p>&lt;Ruta de acceso&gt;</p></td>
<td align="left"><p>Ubicación en la que desea instalar MBAM.</p>
<p>Por ejemplo:</p>
<p>INSTALLDIR = c:\mbaminstall</p></td>
</tr>
<tr class="even">
<td align="left"><p>FORCE_UNINSTALL</p></td>
<td align="left"><p>Verdadero falso</p></td>
<td align="left"><p>True: continúa con el proceso de desinstalación de MBAM, incluso si no se pueden quitar las características.</p>
<p>Falso (valor predeterminado) si la acción personalizada de desinstalación no puede quitar una característica de servidor de MBAM agregada, se produce un error en la desinstalación y MBAM permanece instalado.</p>
<p>En ambos casos, cualquier característica que se haya eliminado correctamente durante el intento de desinstalar MBAM se mantendrá eliminada.</p></td>
</tr>
</tbody>
</table>

 



## Temas relacionados


[Implementación de MBAM 2.5](deploying-mbam-25.md)

[Configuración de funciones de servidor MBAM 2.5](configuring-the-mbam-25-server-features.md)

 

## ¿Tiene una sugerencia para MBAM?
- Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring). 
- Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





