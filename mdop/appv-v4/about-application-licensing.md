---
title: Acerca de las licencias de aplicaciones
description: Acerca de las licencias de aplicaciones
author: dansimp
ms.assetid: 6b487641-1627-4e91-b829-04f001008176
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 546bc630b95fe52f960c7bdfb771d3e2561f9318
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10820100"
---
# Acerca de las licencias de aplicaciones


Puede administrar las licencias de aplicación directamente desde la consola de administración de Application Virtualization Server.

## Tipos de licencia


El sistema de virtualización de System Center Application es compatible actualmente con los siguientes tipos de licencias:

-   **Licencia ilimitada**: permite el acceso a la aplicación por parte de cualquier número de usuarios simultáneos. Este método de licencias es adecuado cuando desea asociar una licencia de toda la empresa con una aplicación.

-   **Licencia concurrente**: le permite definir la cantidad máxima de usuarios simultáneos que pueden usar la aplicación.

-   **Licencia con nombre**: le permite asignar una licencia a un usuario individual. Una licencia con nombre se puede usar para asegurarse de que un usuario determinado siempre pueda ejecutar la aplicación.

Puede combinar licencias simultáneas y con nombre para la misma aplicación.

La licencia está deshabilitada de forma predeterminada, pero puede habilitarla desde la pestaña **canalización del proveedor** del cuadro de diálogo **propiedades del proveedor** . Para obtener más información sobre cómo habilitar y deshabilitar licencias, consulte [Cómo configurar o deshabilitar licencias de aplicaciones](how-to-set-up-or-disable-application-licensing.md).

## Directivas de proveedor


Las directivas de proveedor se han desarrollado para el modelo de proveedor de servicios de aplicaciones (ASP). En este modelo, un único ASP puede hospedar un único sistema de virtualización de aplicaciones para varios clientes, en el que cada cliente debe permanecer aislado. Los clientes pueden tener muy diversos requisitos, por ejemplo, un cliente puede requerir autenticación, mientras que otro no. Puede usar directivas de proveedor para asociar permisos con clientes para que solo los usuarios autorizados puedan tener acceso a cada aplicación virtual o paquete de aplicación virtual.

Para el cliente empresarial, puede usar esta característica cuando tenga requisitos de licencia estrictos para una o más aplicaciones. En esta situación, el componente de licencias está deshabilitado en la pestaña **canalización del proveedor** del cuadro de diálogo **propiedades del proveedor** .

La ficha **proveedor de proveedores** también tiene casillas para habilitar la autenticación, autorización (**exigir permisos de acceso a la configuración**) y medición (**información sobre el uso de registros**). Si su configuración tiene requisitos especiales, puede escribir sus propios componentes de canalización y agregarlos al sistema haciendo clic en el botón **avanzadas** .

## Autoridades de cuenta


La autoridad de cuentas es el dominio en el que está instalado el servidor de virtualización de aplicaciones. A medida que avance por la instalación del servidor, se le pedirá que proporcione un nombre de dominio; el dominio en el que está instalado el equipo se detecta y se usa de forma predeterminada. Cuando los usuarios intentan iniciar sesión en el sistema, se les pide sus credenciales para poder acceder a ese dominio.

El sistema de virtualización de aplicaciones admite varios dominios. Puede conceder acceso a la aplicación a grupos de usuarios en otros dominios si se establece una relación de confianza entre dominios. Los usuarios deben proporcionar credenciales reconocidas por cada dominio.

En la consola de administración de Application Virtualization Server, puede cambiar el dominio principal (autoridad de cuentas) y las credenciales que se usan para obtener acceso a él.

## Autenticación


La autenticación es el mecanismo que se usa para confirmar la identidad de un usuario. Cualquier usuario con un nombre de usuario y contraseña reconocidos tiene acceso.

En el sistema de virtualización de aplicaciones, puede habilitar o deshabilitar la autenticación mediante una casilla de verificación en la pestaña **proveedor de canalizaciones** . De forma predeterminada, la autenticación de Windows está habilitada.

## Authorization


La autorización es el proceso que se usa para confirmar la identidad de un usuario. Después de confirmar la identidad del usuario, el sistema determina si se le ha concedido acceso al usuario al sistema y a qué aplicaciones se les ha concedido acceso. La consola de administración de Application Virtualization Server tiene una casilla de verificación **exigir permisos de acceso** en la pestaña **canalización del proveedor** para habilitar o deshabilitar la autorización.

En el sistema de virtualización de aplicaciones, el acceso se concede a un grupo de usuarios, no a usuarios individuales.

## Temas relacionados


[Cómo administrar licencias de aplicaciones en la consola de administración de servidor](how-to-manage-application-licenses-in-the-server-management-console.md)

[Cómo configurar o deshabilitar las licencias de aplicaciones](how-to-set-up-or-disable-application-licensing.md)

[Consola de administración de servidor: Nodo de directivas de proveedor](server-management-console-provider-policies-node.md)

 

 





