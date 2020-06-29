---
title: Elementos de archivo OSD
description: Elementos de archivo OSD
author: dansimp
ms.assetid: 8211b562-7549-4331-8321-144f52574e99
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a8e3ebcf53ff39ecd2ef7ad0feec0bbbcae199db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816110"
---
# Elementos de archivo OSD


El directorio de instalación del secuenciador contiene un archivo de esquema XML, **Softricity. xsd**, que define la estructura válida de un archivo descriptor de software abierto (OSD). A continuación se muestran algunos de los elementos de la OSD más usados.

<a href="" id="softpkg"></a>SOFTPKG  
El elemento raíz del archivo OSD que contiene todos los elementos que definen el paquete de software.

<a href="" id="codebase"></a>TE  
Información sobre el archivo. SFT de este paquete, incluidos los atributos HREF, FILENAME y GUID. Puede editar el atributo HREF si cambia el punto de distribución de este paquete en particular.

<a href="" id="os"></a>Sistema operativo  
Define en qué sistemas operativos se puede ejecutar esta aplicación en función de los valores establecidos inicialmente en el Asistente de secuencias. Este valor solo puede contener los valores definidos en **Softricity. xsd**.

<a href="" id="local-interaction-allowed"></a>\ _INTERACTION \ _ALLOWED LOCAL  
Si se establece en TRUE, se habilita la creación de objetos con nombre (eventos, exclusiones mutuas, semáforos, asignaciones de archivos y procesadores de datos) y objetos COM en el espacio de nombres global, en lugar de aislados en un entorno virtual en particular, lo que permite que las aplicaciones virtuales interactúen con las aplicaciones del sistema operativo host.

Ejemplo: &lt; implementación de SOFTPKG &gt; &lt;&gt;

&lt;directivas de VIRTUALENV &gt; &lt;&gt;

&lt;LOCAL \ _INTERACTION \ _ALLOWED &gt; verdadero

&lt;/LOCAL\ _INTERACTION \ _ALLOWED&gt;

&lt;/POLICIES &gt; &lt; /VIRTUALENV&gt;

&lt;/IMPLEMENTATION &gt; &lt; /SOFTPKG&gt;

<a href="" id="dependencies"></a>DEPENDENCIAS  
Define la composición dinámica de conjuntos (dependencias en otros paquetes) mediante una etiqueta codebase de otro paquete.

Ejemplo: &lt; dependencias de &gt; &lt; código base href = "rtsps://Server/package.SFT" GUID = "7579F4DF-2461-4219-BD43-494E1FDC69E3" SYSGUARDFILE = "pkg. 1 \ \ osguard. CP" size = "6572748" mandato = "false"/ &gt; &lt; /DEPENDENCIES&gt;

<a href="" id="package-name"></a>NOMBRE DEL PAQUETE  
Nombre común del paquete especificado en la página de información del **paquete** del asistente de secuenciación, que permite especificar un nombre único para una aplicación de secuencia que contiene varias aplicaciones.

<a href="" id="title"></a>CORTESÍA  
Nombre descriptivo opcional de la aplicación que va a secuenciar.

<a href="" id="abstract"></a>EXTRACCIÓN  
Descripción breve del paquete de software introducido en el campo **comentarios** en la página de **información** del asistente de secuencias. Un procedimiento recomendado es especificar información como el sistema operativo y el nivel de Service Pack de la estación de trabajo del secuenciador, la versión del secuenciador y el nombre del ingeniero de secuencias.

<a href="" id="script"></a>SECUENCIAS  
Define eventos específicos con scripts que se producirán durante el inicio, el apagado o la transmisión por secuencias.

<a href="" id="mgmt-shortcutlist"></a>ADMIN \ _SHORTCUTLIST  
Lista de todos los métodos abreviados definidos en el asistente.

<a href="" id="mgmt-fileassociations"></a>ADMIN \ _FILEASSOCIATIONS  
Lista de los tipos de archivo especificados en el asistente.

## Temas relacionados


[Acerca de la pestaña OSD](about-the-osd-tab.md)

 

 





