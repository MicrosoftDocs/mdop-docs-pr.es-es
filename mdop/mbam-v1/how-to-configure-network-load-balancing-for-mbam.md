---
title: Cómo configurar el equilibrio de carga de red para MBAM
description: Cómo configurar el equilibrio de carga de red para MBAM
author: dansimp
ms.assetid: df2208c3-352b-4a48-9722-237b0c8cd6a5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a04bc74a9dab7bfe18eed8e5a3c1b6ca64d88b5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10825511"
---
# Cómo configurar el equilibrio de carga de red para MBAM


Para comprobar que cumple los requisitos previos y los requisitos de hardware y software para instalar la característica servidor de administración y supervisión, consulte [MBAM 1,0 Deployment Prerequisites](mbam-10-deployment-prerequisites.md) y [MBAM 1,0 compatibles](mbam-10-supported-configurations.md).

**Nota:**  Para obtener los archivos de registro de configuración, debe instalar Microsoft BitLocker Administration and Monitoring (MBAM) mediante el paquete **msiexec** y la opción **/l** de la &lt; Ubicación &gt; . Los archivos de registro se crean en la ubicación que especifique.

Los archivos de registro de instalación adicionales se crean en la carpeta% Temp% del usuario que instala MBAM.

 

Los clústeres de equilibrio de carga de red (NLB) de la característica servidor de administración y supervisión proporcionan escalabilidad en MBAM y deben admitir más de 55.000 MBAM de equipos cliente.

**Nota:**  El equilibrio de carga de red de Windows Server distribuye las solicitudes de cliente a través de un conjunto de servidores que están configurados en un clúster de servidor único. Cuando el equilibrio de carga de red está instalado en cada uno de los servidores (hosts) de un clúster, el clúster presenta una dirección IP virtual o un nombre de dominio completo (FQDN) a las solicitudes de cliente. Las solicitudes de cliente iniciales van a todos los hosts del clúster, pero solo un anfitrión acepta y controla la solicitud.

Todos los equipos que formarán parte de un clúster NLB tienen los siguientes requisitos:

-   Todos los equipos del clúster NLB deben estar en el mismo dominio.

-   Cada equipo del clúster NLB debe usar una dirección IP estática.

-   Cada equipo del clúster NLB debe tener habilitado el equilibrio de carga de red.

-   El clúster NLB requiere una dirección IP estática y se debe crear un registro de host manualmente en el sistema de nombres de dominio (DNS).

 

## Configuración del equilibrio de carga de red para los servidores de supervisión y administración de MBAM


Los pasos siguientes describen cómo configurar un nombre virtual de clúster NLB y una dirección IP para dos servidores de supervisión y administración de MBAM, y cómo configurar los clientes de MBAM para que usen el clúster NLB.

Antes de empezar los procedimientos que se describen en este tema, debe tener la característica del servidor de administración y supervisión de MBAM instalada correctamente mediante el mismo enlace de puerto de IIS en dos equipos de servidor independientes que cumplan los requisitos previos para la instalación de características de servidor MBAM y la configuración de clúster de NLB.

**Nota:**  En este tema se describe el proceso básico de uso del administrador de equilibrio de carga de red para crear un clúster NLB. Los pasos exactos para configurar un servidor Windows como parte de un clúster NLB dependen de la versión de Windows Server en uso.. Para obtener más información sobre cómo crear NLBs en WindowsServer2008, consulte [creación de clústeres de equilibrio de carga de red](https://go.microsoft.com/fwlink/?LinkId=197176) en la biblioteca de TechNet de Server2008 de Windows.

 

**Para configurar un nombre virtual de clúster NLB y una dirección IP para dos servidores de supervisión y administración de MBAM**

1.  Haga clic en **Inicio**, en **todos los programas**, en **herramientas administrativas**y, por último, en **Administrador de equilibrio de carga de red**.

    **Nota:**  Si el administrador de NLB no está presente, puede instalarlo como una característica de WindowsServer. Debe instalar esta característica en los servidores de supervisión y administración de MBAM si desea configurarlo en el clúster NLB.

     

2.  En la barra de menús, haga clic en **cluster**y, a continuación, haga clic en **nuevo** para abrir el cuadro de diálogo **parámetros de clúster** .

3.  En el cuadro de diálogo **parámetros de clúster** , escriba la información para la configuración IP del clúster de NLB:

    -   **Dirección IP:** Dirección IP del clúster NLB registrada en DNS

    -   **Máscara de subred:** Máscara de subred de la dirección IP del clúster NLB registrada en DNS

    -   **Nombre completo de Internet:** FQDN del nombre de clúster NLB registrado en DNS

4.  Asegúrese de que **unidifusión** está seleccionado en el **modo de operación de clúster**y, a continuación, haga clic en **siguiente**.

5.  En la página **direcciones IP del clúster** , haga clic en **siguiente**.

6.  En la página **reglas de Puerto** , haga clic en **Editar** para definir los puertos a los que responderá el clúster NLB y configure los puertos que se usan para la comunicación del sistema entre el cliente y la definición del sitio, o haga clic en **siguiente** para habilitar la dirección IP del clúster NLB para responder a todos los puertos TCP/IP.

    **Nota:**  Asegúrese de que **affinity** es **Single**.

     

7.  En la página **Connect** , escriba un nombre de host de instancia de servidor de supervisión y administración de MBAM que formará parte del clúster NLB en **host**y, a continuación, haga clic en **conectar**.

8.  En las **interfaces disponibles para configurar un nuevo clúster**, seleccione la interfaz de red que se configurará para responder a la comunicación del clúster NLB y, a continuación, haga clic en **siguiente**.

9.  En la página **parámetros de host** , revise la información que se muestra para asegurarse de que la configuración de **IP dedicada** muestra la configuración de IP de host dedicada para el host de clúster NLB correcto, compruebe que el estado **predeterminado** del host es **iniciado**y, a continuación, haga clic en **Finalizar**.

    **Nota:**  La página de **parámetros de host** también muestra la prioridad de host de clúster de NLB, que es de 1 a 32. A medida que se agregan nuevos hosts al clúster NLB, la prioridad del host debe ser diferente de la de los hosts agregados anteriormente. La prioridad se incrementa automáticamente al usar el administrador de equilibrio de carga de red.

     

10. Haga clic en ** &lt; nombre &gt; del clúster NLB** y asegúrese de que el **Estado** de la interfaz del host NLB está **convergido** antes de continuar. Es posible que este paso requiera que actualice la pantalla del clúster NLB como la configuración TCP/IP del host modificada por el administrador de NLB.

11. Para agregar hosts adicionales al clúster NLB, haga clic con el botón secundario en ** &lt; &gt; nombre del clúster NLB**, haga clic en **Agregar host al clúster** y, a continuación, repita los pasos del 7 al 10 para cada sistema de sitio que formará parte del clúster NLB.

12. En un equipo que tenga instalada una plantilla de directiva de grupo de MBAM, modifique la configuración de directiva de grupo de MBAM para configurar los puntos de conexión de servicios de MBAM para usar el nombre de clúster NLB y el enlace de Puerto IIS adecuado para acceder a las características de servidor de administración y supervisión de MBAM que se instalan en los equipos del clúster de NLB. Para obtener más información sobre cómo editar la configuración de GPO de MBAM, vea [Cómo editar la configuración de GPO de MBAM 1,0](how-to-edit-mbam-10-gpo-settings.md). Si los servidores de administración y supervisión de MBAM son nuevos en su entorno, asegúrese de que las pertenencias a grupos de seguridad local obligatorias se hayan configurado correctamente. Para obtener más información sobre los requisitos de los grupos de seguridad, consulte [roles de planificación de MBAM 1,0](planning-for-mbam-10-administrator-roles.md).

13. Cuando se complete la configuración del clúster NLB, le recomendamos que valide que el clúster NLB de administración y supervisión de MBAM es funcional. Para ello, abra un explorador Web en un equipo distinto de los servidores que están configurados en el NLB y asegúrese de que puede obtener acceso al sitio web de supervisión y administración de MBAM con el FQDN de NLB.

## Temas relacionados


[Implementación de la infraestructura de servidor de MBAM 1.0](deploying-the-mbam-10-server-infrastructure.md)

 

 





