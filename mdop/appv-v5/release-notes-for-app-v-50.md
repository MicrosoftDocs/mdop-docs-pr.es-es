---
title: Notas de la versión de App-V 5.0
description: Notas de la versión de App-V 5.0
author: dansimp
ms.assetid: 68a6a5a1-4b3c-4c09-b00c-9ca4237695d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e49f6072d738b45afe25de24f2ee9a2d09d64a2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813319"
---
# Notas de la versión de App-V 5.0


**Para buscar un problema específico en estas notas de la versión, presione CTRL + F.**

Lea estas notas de la versión minuciosamente antes de instalar App-V 5,0.

Estas notas de la versión contienen información necesaria para instalar correctamente App-V 5,0. Las notas de la versión también contienen información que no está disponible en la documentación del producto. Si hay una diferencia entre estas notas de la versión y otra documentación de App-V 5,0, el cambio más reciente debe considerarse autoritario. Estas notas de la versión reemplazan el contenido que se incluye con este producto.

## Acerca de la documentación del producto


Para obtener información sobre la documentación de App-V 5,0, consulte la página de inicio de App-V 5,0 en Microsoft TechNet.

## Enviar comentarios


Nos interesan tus comentarios en App-V 5,0. Puedes enviar tus comentarios a <mdopdocs@microsoft.com> .

**Nota:**  Esta dirección de correo electrónico no es un canal de soporte técnico, pero tus comentarios nos ayudarán a planificar futuros cambios en nuestra documentación y versiones de productos.

 

Para obtener la información más reciente acerca de MDOP y recursos de aprendizaje adicionales, consulte la página [experiencia de información de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Para obtener más información sobre las nuevas actualizaciones o para proporcionar comentarios, síganos en [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) o [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problemas conocidos con App-V 5,0


Esta sección contiene notas de la versión sobre los problemas conocidos con App-V 5,0.

### No se puede terminar de agregar paquetes al usar cmdlets de servidor de PowerShell

Al agregar un paquete con PowerShell, no hay ningún método para salir de la adición de paquetes nuevos.

SOLUCIÓN alternativa: para dejar de agregar paquetes, pulse **entrar** después de agregar el paquete final.

### <a href="" id="-------------app-v-5-0-client-rejects-packages-from-servers-whose-ssl-certificate-has-been-revoked"></a> El cliente de App-V 5,0 rechaza paquetes de servidores cuyo certificado SSL ha sido revocado

Al usar el protocolo HTTPS, el cliente de App-V 5,0 rechazará de forma predeterminada los paquetes de los servidores cuyo certificado SSL se haya revocado. Este comportamiento se puede desactivar mediante la configuración modificando la configuración **VerifyCertificateRevocationList** . La aplicación de una nueva configuración para esta configuración no surtirá efecto hasta que se reinicie el servicio App-V 5,0.

SOLUCIÓN alternativa: reinicie el servicio de 5,0 de App-V.

## Información de copyright de notas de versión


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune y WindowsPowerShell son marcas comerciales del grupo de empresas de Microsoft. El resto de marcas comerciales pertenecen a sus respectivos dueños.








## Temas relacionados


[Acerca de App-V 5.0](about-app-v-50.md)

 

 





