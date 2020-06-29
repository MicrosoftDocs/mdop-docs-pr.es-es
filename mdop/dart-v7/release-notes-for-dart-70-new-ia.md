---
title: Notas de la versión de DaRT 7.0
description: Notas de la versión de DaRT 7.0
author: dansimp
ms.assetid: fad227d0-5c22-4efd-9187-0e5922f7250b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5114acfe5a46a2c78f722a2bb6394c0dbef55dd4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10822761"
---
# Notas de la versión de DaRT 7.0


**Para buscar estas notas de la versión, presione CTRL + F.**

Lea estas notas de la versión minuciosamente antes de instalar Microsoft Diagnostics and Recovery Toolset (DaRT) 7.

## Acerca del conjunto de herramientas de diagnóstico y recuperación de Microsoft 7,0


Estas notas de la versión contienen información necesaria para instalar DaRT7 correctamente y contienen información que no está disponible en la documentación del producto. Si hay una diferencia entre estas notas de la versión y otra documentación de la plataforma DaRT, el último cambio debe considerarse autoritario. Estas notas de la versión reemplazan al contenido incluido en este producto.

## Acerca de la documentación del producto


La documentación de Microsoft Diagnostics and Recovery Toolset (DaRT) 7 se distribuye con el producto y en el sitio de Connect.

Para obtener ayuda detallada sobre cómo usar las herramientas de DaRT7, vea el archivo de ayuda disponible en el menú conjunto de herramientas de **diagnóstico y recuperación** .

## Comentarios


Nos interesan tus comentarios en DaRT7. Puedes enviar tus comentarios a dart7feedback@microsoft.com. Esta dirección de correo electrónico no es un canal de soporte técnico, pero sus comentarios nos ayudarán a planear los cambios futuros de estas herramientas para que le resulten más útiles en el futuro.

## Protegerse contra virus y vulnerabilidades de seguridad


Para ayudarle a protegerse contra virus y vulnerabilidades de seguridad, le recomendamos que instale las últimas actualizaciones de seguridad disponibles para cualquier software nuevo que se instale. Para obtener más información, consulte [seguridad de Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Problemas conocidos con DaRT 7,0


### No se puede iniciar el examen de SFC si el sistema de limpieza independiente está abierto

Si el sistema de limpieza independiente se está ejecutando, el examen de SFC no puede iniciarse ni ejecutarse debido a un conflicto de recursos entre las dos herramientas.

**Solución alternativa:** Cierre el sistema independiente de limpieza antes de intentar abrir o ejecutar la herramienta de análisis de SFC.

### Es posible que los caracteres Unicode no se muestren en los nombres de archivo

Si elimina un archivo que tiene caracteres Unicode en el nombre de archivo e intenta restaurar el archivo con la herramienta de restauración de archivos, no se encuentra el archivo. Esto solo se produce cuando usa caracteres de un idioma distinto del idioma del DVD de Windows que se usó para crear la imagen de recuperación.

**Solución alternativa:** Asegúrese de que el idioma que usa DaRT coincida con el idioma que usa el sistema operativo desde el que está intentando restaurar los archivos.

### La instalación de la línea de comandos de DaRT puede fallar silenciosamente

Se produce un error en la instalación de línea de comandos de DaRT si se ejecuta con el modo silencioso, a menos que se ejecute con permisos de administrador elevados.

**Solución alternativa:** Ejecute la instalación de línea de comandos con permisos elevados de administrador. La instalación de DaRT es compatible con las opciones típicas de Windows Installer para la instalación desde la línea de comandos. Para obtener más información sobre los distintos modificadores disponibles, consulte [las opciones](https://go.microsoft.com/fwlink/?LinkId=160689) de la línea de comandos de Windows Installer.

### La búsqueda de archivos no puede mover una carpeta a un volumen diferente

El movimiento de carpetas entre volúmenes no es compatible con la aplicación de búsqueda de archivos. Si intenta mover una carpeta a un volumen diferente en la búsqueda de archivos, se devuelve el siguiente error: "se ha producido un error al escribir el * &lt; nombre &gt; *de archivo del archivo. Asegúrese de que la unidad tiene suficiente espacio y que la ruta de destino es accesible.

**Solución alternativa:** Use el explorador para mover una carpeta a un volumen diferente.

### Es posible que algunos datos no estén disponibles en los equipos en los que se reasignan las letras de unidad

Este problema puede ocurrir en equipos habilitados para BitLocker y equipos de inicio múltiple. Esto se debe a que parte de la información del registro sin conexión tiene Letras de unidad no modificables y DaRT usa diferentes letras para los mismos volúmenes. Entre los efectos típicos se incluyen no tener acceso a determinadas cuentas de usuario locales en el editor del registro. Además, es posible que algunas herramientas no puedan obtener propiedades que dependan de la resolución de rutas de archivo.

**Solución alternativa:** Use la opción para reasignar las letras de unidad como se inicia DaRT. Normalmente, esto alinea las letras de unidad típicas con lo que se espera.

### Es posible que el Hotfix desinstalado no desinstale determinadas actualizaciones

Algunas actualizaciones y Service Packs no se pueden desinstalar porque están marcados como desinstalables o porque es necesario desinstalarlos en Windows 7. En estos casos, la herramienta de desinstalación de Hotfix puede indicar que estas actualizaciones se han desinstalado, aunque no se hayan realizado.

**Solución alternativa:** Desinstale estas actualizaciones problemáticas de Windows 7.

### Borrado de disco: no se pueden eliminar los discos con volúmenes distribuidos, volúmenes seccionados ni volúmenes reflejados

El borrado de disco no es compatible con la eliminación de discos distribuidos, reflejados o particionados en uno o más volúmenes.

**Solución alternativa:** Seleccione y elimine cada disco del volumen por separado.

## Información de copyright de notas de versión


Este documento se proporciona "tal cual". La información y las vistas expresadas en este documento, incluidas las direcciones URL y otras referencias a sitios web de Internet, pueden cambiar sin previo aviso. Usted asume el riesgo de su uso.

Algunos ejemplos que se describen en este artículo se proporcionan solo para la ilustración y son ficticios.No se pretende ni se debe deducir ninguna asociación o conexión real.

Este documento no le proporciona derechos legales sobre ninguna propiedad intelectual en ningún producto de Microsoft. Este documento es confidencial y propiedad de Microsoft. Se revela y se puede usar únicamente en virtud de un contrato de no divulgación.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, WindowsServer y Windows Vista son marcas comerciales del grupo de compañías Microsoft.

El resto de marcas comerciales pertenecen a sus respectivos dueños.

## Temas relacionados


[Acerca de DaRT 7.0](about-dart-70-new-ia.md)

 

 





