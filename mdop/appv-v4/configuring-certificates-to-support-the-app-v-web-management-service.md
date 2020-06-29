---
title: Configuración de certificados para admitir el servicio de administración web de App-V
description: Configuración de certificados para admitir el servicio de administración web de App-V
author: dansimp
ms.assetid: b7960161-2c19-4cbf-a98a-d4b06f547dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 23839e6fad79c1f10eb2416941396ad3c6f04d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10821890"
---
# Configuración de certificados para admitir el servicio de administración web de App-V


El servicio de administración web de App-V debe estar configurado para admitir conexiones basadas en SSL para ayudar a proteger la comunicación. Este proceso requiere que el servidor web o el equipo en el que está instalado el servicio de administración tenga un certificado emitido para el servicio o equipo.

En los siguientes escenarios se muestra cómo obtener un certificado para este propósito:

1.  La infraestructura de la empresa ya tiene una infraestructura de clave pública (PKI) que emite automáticamente certificados para los equipos.

2.  La infraestructura de la compañía ya tiene una PKI vigente, aunque no emite automáticamente certificados para equipos.

3.  La infraestructura de la compañía no tiene ninguna PKI vigente.

En cada uno de los escenarios anteriores, el método para obtener un certificado es diferente, pero el resultado final es el mismo. El administrador debe asignar un certificado al sitio web predeterminado de IIS y configurar el servicio de administración web de App-V para requerir comunicaciones seguras.

**Importante**  El nombre del certificado debe coincidir con el nombre del servidor. Es recomendable usar nombres de dominio completos (FQDN) para el nombre común del certificado.

 

App-V puede usar servidores IIS para admitir diferentes configuraciones de infraestructura. Para obtener más información sobre cómo configurar los servidores IIS para que admitan HTTPS, consulte <https://go.microsoft.com/fwlink/?LinkId=151972> .

## Temas relacionados


[Cómo instalar y configurar la consola de administración de App-V para un entorno más seguro](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)

 

 





