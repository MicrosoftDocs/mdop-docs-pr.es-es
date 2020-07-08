---
title: Planificación de la capacidad de App-V 5.0
description: Planificación de la capacidad de App-V 5.0
author: dansimp
ms.assetid: 56f48b00-cd91-4280-9481-5372a0e2e792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9e828457a286f6f686c227a935828679514d87ad
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10814854"
---
# Planificación de la capacidad de App-V 5.0


Las siguientes recomendaciones se pueden usar como una línea de base para ayudar a determinar la información de planeación de capacidad adecuada para la infraestructura de App-V 5,0 de su organización.

**Importante**  Use la información de esta sección solo como guía general para planear la implementación de App-V 5,0. Los requisitos de capacidad del sistema dependerán de los detalles específicos de su entorno de hardware y de aplicación. Además, los números de rendimiento que se muestran en este documento son ejemplos y los resultados pueden variar.

 

## Determinar el ámbito del proyecto


Antes de diseñar la infraestructura de App-V 5,0, debe determinar el ámbito del proyecto. El ámbito consiste en determinar qué aplicaciones estarán disponibles de forma virtual e identificar los usuarios de destino y sus ubicaciones. Esta información le ayudará a determinar qué tipo de infraestructura de App-V 5,0 debe implementarse. Las decisiones sobre el ámbito del proyecto deben basarse en las necesidades específicas de su organización.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tarea</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Determinar el ámbito de la aplicación</p></td>
<td align="left"><p>En función de las aplicaciones que se vayan a virtualizar, la infraestructura de App-V 5,0 se puede configurar de diferentes maneras. La primera tarea es definir qué aplicaciones desea virtualizar.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Determinar el ámbito de ubicación</p></td>
<td align="left"><p>El ámbito de ubicación hace referencia a las ubicaciones físicas (por ejemplo, en toda la empresa o en una ubicación geográfica específica) donde tiene previsto ejecutar las aplicaciones virtualizadas. También puede hacer referencia a la población de usuarios (por ejemplo, un único departamento) que ejecutará las aplicaciones virtuales. Debe obtener un mapa de red que incluya las rutas de conexión, así como el ancho de banda disponible para cada ubicación y el número de usuarios que usan aplicaciones virtualizadas y la velocidad de vínculo de WAN.</p></td>
</tr>
</tbody>
</table>

 

## Determinar qué infraestructura de App-V 5,0 es necesaria


**Importante**  Los dos modelos siguientes requieren que el cliente de App-V 5,0 se instale en el equipo en el que se va a ejecutar aplicaciones virtuales.

También puede administrar el entorno de App-V 5,0 mediante una solución de distribución de software electrónico (ESD) como Microsoft Systems Center Configuration Manager. Para obtener más información [, consulte implementación de paquetes de App-V 5,0 mediante distribución electrónica de software (ESD)](deploying-app-v-50-packages-by-using-electronic-software-distribution--esd-.md).

 

-   **Modelo independiente** : el modelo independiente permite que las aplicaciones virtuales sean Windows Installer habilitadas para su distribución sin transmisión por secuencias. App-V 5,0 en modo autónomo consiste en el secuenciador y el cliente; no se necesitan componentes adicionales. Las aplicaciones se preparan para la virtualización mediante un proceso denominado secuencias. Para obtener más información, vea [planeación del secuenciador de aplicaciones-V 5,0 e implementación de clientes](planning-for-the-app-v-50-sequencer-and-client-deployment.md). Se recomienda usar el modelo independiente para los siguientes escenarios:

    -   Con usuarios remotos desconectados que no pueden conectarse a la infraestructura de App-V 5,0.

    -   Cuando esté ejecutando un sistema de administración de software, como Configuration Manager 2012.

    -   Cuando las limitaciones de ancho de banda de red impiden la distribución electrónica del software.

-   **Modelo de infraestructura completa** : el modelo de infraestructura completo proporciona capacidades de distribución, administración y creación de informes de software; también incluye la transmisión de aplicaciones a través de la red. El modelo de infraestructura completa de App-V 5,0 consta de uno o varios servidores de administración de App-V 5,0. El servidor de administración se puede usar para publicar aplicaciones en todos los clientes. El proceso de publicación coloca los iconos de la aplicación virtual y los accesos directos en el equipo de destino. También puede transmitir aplicaciones a usuarios locales. Para obtener más información sobre cómo instalar el servidor de administración, consulte [planificación de la implementación del servidor de App-V 5,0](planning-for-the-app-v-50-server-deployment.md). Se recomienda el modelo de infraestructura completa para los siguientes escenarios:

    **Importante**  El modelo de infraestructura completa de App-V 5,0 requiere que Microsoft SQL Server almacene los datos de configuración. Para obtener más información [, consulte Configuraciones admitidas de App-V 5,0](app-v-50-supported-configurations.md).

     

    -   Cuando desee usar el servidor de administración para publicar la aplicación en equipos de destino.

    -   Para provisioning rápido de aplicaciones a equipos de destino.

    -   Cuando quiera usar informes de App-V 5,0.

## Guía de tamaño de servidor de principio a fin


En la siguiente sección, se proporciona información sobre el tamaño y la planeación de App-V 5,0. Para obtener información más específica, consulte las secciones siguientes.

**Nota:**  El tiempo de respuesta de ida y vuelta en el cliente es el tiempo que tarda el equipo que ejecuta el cliente de App-V 5,0 en recibir una notificación correcta del servidor de publicación. El tiempo de respuesta de ida y vuelta en el servidor de publicación es el tiempo que tarda el equipo que ejecuta el servidor de publicación para recibir una actualización de metadatos del paquete correcta del servidor de administración.

 

-   los clientes de 20.000 pueden dirigirse a un solo servidor de publicación para obtener la actualización del paquete en un tiempo de ida y vuelta aceptable. ( &lt; 3 segundos)

-   Un solo servidor de administración puede admitir hasta 50 servidores de publicación para actualizaciones de metadatos del paquete en un tiempo de ida y vuelta aceptable. ( &lt; 5 segundos)

## <a href="" id="---------app-v-5-0-management-server-capacity-planning-recommendations"></a> Recomendaciones de planeación de capacidad del servidor de administración de App-V 5,0


Los servidores de publicación de App-V 5,0 requieren el servidor de administración para las solicitudes de actualización de paquetes y las respuestas de actualización de paquetes. El servidor de Administración envía entonces la información a la base de datos de administración para recuperar la información. Para obtener más información sobre las configuraciones admitidas del servidor de administración de App-V 5,0, consulte [configuraciones admitidas de App-v 5,0](app-v-50-supported-configurations.md).

**Nota:**  El tiempo de actualización predeterminado en el servidor de publicación de App-V 5,0 es de diez minutos.

 

Cuando varios servidores de publicación simultáneos se pongan en contacto con un único servidor de administración de actualizaciones de metadatos del paquete, los tres factores siguientes influirán en el tiempo de respuesta de ida y vuelta en el servidor de publicación:

1.  Número de servidores de publicación que hacen solicitudes simultáneas.

2.  Número de grupos de conexión configurados en el servidor de administración.

3.  Número de grupos de acceso configurados en el servidor de administración.

La siguiente tabla muestra más información sobre cada factor que afecta al tiempo de recorrido de ida y vuelta.

**Nota:**  El tiempo de respuesta de ida y vuelta es el tiempo que tarda el equipo que ejecuta el servidor de publicación de App-V 5,0 para recibir una actualización de metadatos del paquete correcta del servidor de administración.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Factores que afectan al tiempo de respuesta de ida y vuelta</th>
<th align="left">Más información</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>El número de servidores de publicación que solicitan simultáneamente renovaciones de metadatos del paquete.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Un solo servidor de administración puede responder a un máximo de 320 servidores de publicación que solicitan metadatos de publicación al mismo tiempo.</p></li>
<li><p>El tiempo de respuesta de ida y vuelta para servidores pub 320 es de ~ 40 segundos.</p></li>
<li><p>Para &lt; los servidores de publicación de 50 que solicitan metadatos simultáneamente, el tiempo de respuesta de ida y vuelta es de &lt; 5 segundos.</p></li>
<li><p>De 50 a 320 servidores de publicación, el tiempo de respuesta aumenta linealmente (aproximadamente 2x).</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>El número de grupos de conexión configurados en el servidor de administración.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>En el caso de grupos de conexión de hasta 100, no hay ningún cambio significativo en el tiempo de respuesta de la acción de ida y vuelta en el servidor de publicación.</p></li>
<li><p>Para los grupos de conexiones 100-400, hay un aumento lineal menor en el tiempo de respuesta de la acción de ida y vuelta.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>El número de grupos de acceso configurados en el servidor de administración.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>En el caso de grupos de acceso de hasta 40, hay un aumento lineal (aproximadamente 3x) en el tiempo de respuesta de ida y vuelta en el servidor de publicación.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

En la tabla siguiente se muestran valores de ejemplo para cada uno de los factores anteriores. En cada variación, los paquetes de 120 se actualizan desde el servidor de administración de App-V 5.0.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Escenario</th>
<th align="left">Variación</th>
<th align="left">Número de grupos de conexión</th>
<th align="left">Número de grupos de acceso</th>
<th align="left">Número de servidores de publicación</th>
<th align="left">Tipo de conexión de red servidor de publicación/servidor de administración</th>
<th align="left">Tiempo de respuesta de ida y vuelta en el servidor de publicación (en segundos)</th>
<th align="left">Uso de la CPU en el servidor de administración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Publicar servidores de forma simultánea en el servidor de administración para publicar metadatos.</p></td>
<td align="left"><p>Número de servidores de publicación</p></td>
<td align="left"><p></p>
<ul>
<li><p>,0</p></li>
<li><p>,0</p></li>
<li><p>,0</p></li>
<li><p>,0</p></li>
<li><p>,0</p></li>
<li><p>,0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>uno</p></li>
<li><p>uno</p></li>
<li><p>uno</p></li>
<li><p>uno</p></li>
<li><p>uno</p></li>
<li><p>uno</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>50</p></li>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>300</p></li>
<li><p>315</p></li>
<li><p>320</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>4</p></li>
<li><p>base10</p></li>
<li><p>19</p></li>
<li><p>32</p></li>
<li><p>0,30</p></li>
<li><p>37</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>apartado</p></li>
<li><p>apartado</p></li>
<li><p>apartado</p></li>
<li><p>4,5</p></li>
<li><p>apartado</p></li>
<li><p>4,5</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Los metadatos de publicación contienen grupos de conexión</p></td>
<td align="left"><p>Número de grupos de conexión</p></td>
<td align="left"><p></p>
<ul>
<li><p>base10</p></li>
<li><p>50</p></li>
<li><p>100</p></li>
<li><p>150</p></li>
<li><p>300</p></li>
<li><p>400</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>uno</p></li>
<li><p>uno</p></li>
<li><p>uno</p></li>
<li><p>uno</p></li>
<li><p>uno</p></li>
<li><p>uno</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>base10</p></li>
<li><p>once</p></li>
<li><p>once</p></li>
<li><p>apartado</p></li>
<li><p>23</p></li>
<li><p>veinticinco</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>apartado</p></li>
<li><p>19</p></li>
<li><p>23</p></li>
<li><p>19</p></li>
<li><p>veinte</p></li>
<li><p>veinte</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Los metadatos de publicación contienen grupos de acceso</p></td>
<td align="left"><p>Número de grupos de acceso</p></td>
<td align="left"><p></p>
<ul>
<li><p>,0</p></li>
<li><p>,0</p></li>
<li><p>,0</p></li>
<li><p>,0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>uno</p></li>
<li><p>base10</p></li>
<li><p>veinte</p></li>
<li><p>40</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>base10</p></li>
<li><p>43</p></li>
<li><p>153</p></li>
<li><p>535</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>apartado</p></li>
<li><p>26</p></li>
<li><p>veinticuatro</p></li>
<li><p>veinticuatro</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

La utilización de la CPU del equipo que ejecuta el servidor de administración es de aproximadamente 25%, independientemente del número de servidores de publicación destinados a él. Las transacciones de la base de datos de Microsoft SQL Server/sec, las solicitudes de lotes/s y las conexiones de usuario son idénticas independientemente del número de servidores de publicación. Por ejemplo: transacciones/seg es ~ 30, solicitudes por lotes ~ 200 y User Connect ~ 6.

Con una implementación geográfica distribuida, en la que el servidor de administración & los servidores de publicación utilizan una red de vínculo de baja velocidad entre ellos, el tiempo de respuesta de ida y vuelta en los servidores de publicación se encuentra dentro de los límites de tiempo aceptables ( &lt; 5 segundos), incluso para solicitudes simultáneas de 100 en un solo servidor de administración.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Escenario</th>
<th align="left">Variación</th>
<th align="left">Número de grupos de conexión</th>
<th align="left">Número de grupos de acceso</th>
<th align="left">Número de servidores de publicación</th>
<th align="left">Tipo de conexión de red servidor de publicación/servidor de administración</th>
<th align="left">Tiempo de respuesta de ida y vuelta en el servidor de publicación (en segundos)</th>
<th align="left">Uso de la CPU en el servidor de administración</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Conexión de red entre el servidor de publicación y el servidor de administración</p></td>
<td align="left"><p>Red de vínculo lento de 1,5 Mbps</p></td>
<td align="left"><p></p>
<ul>
<li><p>,0</p></li>
<li><p>,0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>uno</p></li>
<li><p>uno</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>50</p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Cable de 1,5 Mbps DSL</p></li>
<li><p>Cable de 1,5 Mbps DSL</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>cuatro</p></li>
<li><p>4</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>uno</p></li>
<li><p>1</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Conexión de red entre el servidor de publicación y el servidor de administración</p></td>
<td align="left"><p>Red de área local o WIFI</p></td>
<td align="left"><p></p>
<ul>
<li><p>,0</p></li>
<li><p>,0</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>uno</p></li>
<li><p>uno</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Wi-Fi</p></li>
<li><p>Wi-Fi</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>once</p></li>
<li><p>veinte</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>4,5</p></li>
<li><p>apartado</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

Ya sea que el servidor de administración y los servidores de publicación estén conectados a través de una red de vínculo de baja velocidad o una red de alta velocidad, el servidor de administración puede controlar aproximadamente 15.000 solicitudes de actualización de paquetes en 30 minutos.

## <a href="" id="---------app-v-5-0-reporting-server-capacity-planning-recommendations"></a> Recomendaciones de planeación de capacidad del servidor de creación de informes de App-V 5,0


Los clientes de App-V 5,0 envían datos de informes al servidor de informes. El servidor de informes registra la información en la base de datos de Microsoft SQL Server y devuelve una notificación correcta al equipo que ejecuta el cliente de App-V 5,0. Para obtener más información sobre las configuraciones admitidas de App-V 5,0 Server, consulte [configuraciones admitidas de App-v 5,0](app-v-50-supported-configurations.md).

**Nota:**  El tiempo de respuesta de ida y vuelta es el tiempo que tarda el equipo que ejecuta el cliente de App-V 5,0 para enviar la información de informes al servidor de informes y recibir una notificación correcta desde el servidor de informes.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Escenario</th>
<th align="left">Resumen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Varios clientes de App-V 5,0 envían información de informes al servidor de informes de forma simultánea.</p></td>
<td align="left"><p></p>
<ul>
<li><p>El tiempo de respuesta de ida y vuelta del servidor de informes es de 2,6 segundos para clientes de 500.</p></li>
<li><p>El tiempo de respuesta de ida y vuelta del servidor de informes es de 5,65 segundos para clientes de 1000.</p></li>
<li><p>El tiempo de respuesta de ida y vuelta aumenta de forma lineal dependiendo de la cantidad de clientes.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Solicitudes por segundo procesadas por el servidor de informes.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>Un único servidor de creación de informes y una única base de datos pueden procesar un máximo de 139 solicitudes por segundo. El promedio es solicitudes de 121/segundo.</p></li>
<li><p>Al usar dos servidores de informes en la misma base de datos de Microsoft SQL Server, el promedio de solicitudes/segundo es similar a un único servidor de informes = ~ 127, con un máximo de 278 solicitudes/segundo.</p></li>
<li><p>Un único servidor de informes puede procesar 500 conexiones simultáneas/activas.</p></li>
<li><p>Un único servidor de informes puede procesar un máximo de 1500 conexiones simultáneas.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Base de datos de informes.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>La contención de bloqueo en el equipo que ejecuta Microsoft SQL Server es el factor que limita la solicitud por segundo.</p></li>
<li><p>El rendimiento y el tiempo de respuesta son independientes del tamaño de la base de datos.</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Calculando retraso aleatorio**:

La demora aleatoria especifica el retraso máximo (en minutos) para que los datos se envíen al servidor de informes. Cuando se inicia la tarea programada, el cliente genera una demora aleatoria entre **0** y **ReportingRandomDelay** , y esperará la duración especificada antes de enviar los datos.

Retraso aleatorio = 4 \ * número de clientes/solicitudes promedio por segundo.

Ejemplo: para clientes de 500, con solicitudes de 120 por segundo, el retraso aleatorio es 4 \ * 500/120 = ~ 17 minutos.

## <a href="" id="---------app-v-5-0-publishing-server-capacity-planning-recommendations"></a> Recomendaciones de planeación de capacidad del servidor de publicación de App-V 5,0


Los equipos que ejecutan el cliente de App-V 5,0 se conectan al servidor de publicación de App-V 5,0 para enviar una solicitud de actualización de publicaciones y recibir una respuesta. El tiempo de respuesta de ida y vuelta se mide en el equipo que ejecuta el cliente de App-V 5,0. El tiempo de procesador se mide en el servidor de publicación. Para obtener más información sobre las configuraciones admitidas de App-V 5,0 Server, consulte [configuraciones admitidas de App-v 5,0](app-v-50-supported-configurations.md).

**Importante**  En la siguiente lista se muestran los principales factores que se deben tener en cuenta al configurar el servidor de publicación de App-V 5,0:

-   El número de clientes que se conectan simultáneamente a un único servidor de publicación.

-   El número de paquetes de cada actualización.

-   El ancho de banda de red disponible en su entorno entre el cliente y el servidor de publicación de App-V 5,0.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Escenario</th>
<th align="left">Resumen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Varios clientes de App-V 5,0 se conectan a un único servidor de publicación de forma simultánea.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Un servidor de publicación que ejecute procesadores de doble núcleo puede responder a la mayoría de los clientes de 5000 que soliciten una actualización de forma simultánea.</p></li>
<li><p>Para los clientes de 5000-10000, el servidor de publicación requiere un mínimo de cuatro núcleos.</p></li>
<li><p>Para los clientes de 10000-20000, el servidor de publicación debe tener dos núcleos cuádruples para que los tiempos de respuesta sean más eficientes.</p></li>
<li><p>Un servidor de publicación con un núcleo cuádruple puede actualizar paquetes de 10000 en 3 segundos. (Compatible con 10000 clientes simultáneos)</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Número de paquetes en cada actualización.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>El aumento de la cantidad de paquetes incrementará el tiempo de respuesta ~ 40% (hasta 1000 paquetes).</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Red entre el cliente de App-V 5,0 y el servidor de publicación.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>En una red de baja velocidad (1,5 Mbps de ancho de banda), se produce un aumento de 97% en el tiempo de respuesta en comparación con la LAN (hasta 1000 usuarios).</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

**Nota:**  El uso de la CPU de Publishing Server siempre es alto durante el intervalo de tiempo, cuando tiene que procesar solicitudes simultáneas ( &gt; 90% en la mayoría de los casos). El servidor de publicación puede controlar ~ 1500 solicitudes de cliente en 1 segundo.

 

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Escenario</th>
<th align="left">Variación</th>
<th align="left">Número de clientes de App-V 5,0</th>
<th align="left">Cantidad de paquetes</th>
<th align="left">Configuración del procesador en el servidor de publicación</th>
<th align="left">Servidor de publicación de tipo de conexión de red/App-V 5,0 cliente</th>
<th align="left">Tiempo de ida y vuelta en el cliente de App-V 5,0 (en segundos)</th>
<th align="left">Uso de la CPU en el servidor de publicación (en%)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>El cliente de App-V 5,0 envía la solicitud de actualización &amp; de publicaciones y recibe una respuesta, cada solicitud con paquetes de 120</p></td>
<td align="left"><p>Cantidad de clientes</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>1000</p></li>
<li><p>5000</p></li>
<li><p>10000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Doble núcleo</p></li>
<li><p>Doble núcleo</p></li>
<li><p>Núcleo cuádruple</p></li>
<li><p>Núcleo cuádruple</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>uno</p></li>
<li><p>1</p></li>
<li><p>1</p></li>
<li><p>2</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>99</p></li>
<li><p>89</p></li>
<li><p>77</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Varios paquetes en cada actualización</p></td>
<td align="left"><p>Cantidad de paquetes</p></td>
<td align="left"><p></p>
<ul>
<li><p>1000</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>500</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Núcleo cuádruple</p></li>
<li><p>Núcleo cuádruple</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>1</p></li>
<li><p>2</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>92</p></li>
<li><p>91</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Red entre el cliente y el servidor de publicación</p></td>
<td align="left"><p>red de vínculo lento de 1,5 Mbps</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>500</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>120</p></li>
<li><p>120</p></li>
<li><p>120</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Núcleo cuádruple</p></li>
<li><p>Núcleo cuádruple</p></li>
<li><p>Núcleo cuádruple</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Red intracontinental de 1,5 Mbps</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>2</p></li>
<li><p>10 (con tasa de error de 0,2%)</p></li>
<li><p>17 (con tarifa de error de 1%)</p></li>
</ul></td>
<td align="left"><p></p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="---------app-v-5-0-streaming-capacity-planning-recommendations"></a> Recomendaciones de planeación de capacidad de streaming de App-V 5,0


Los equipos que ejecutan el cliente de App-V 5,0 transmiten el paquete de aplicación virtual desde el servidor de transmisión. El tiempo de respuesta de ida y vuelta se mide en el equipo que ejecuta el cliente de App-V 5,0 y es el tiempo que se tarda en transmitir por secuencias todo el paquete.

**Importante**  En la siguiente lista se identifican los principales factores que se deben tener en cuenta al configurar el servidor de streaming de App-V 5,0:

-   El número de clientes que transmiten paquetes de aplicaciones de forma simultánea desde un único servidor de transmisión.

-   El tamaño del paquete que se está transmitiendo.

-   El ancho de banda de red disponible en su entorno entre el cliente y el servidor de transmisión.

 

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Escenario</th>
<th align="left">Resumen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Varios clientes de App-V 5,0 transmiten aplicaciones desde un único servidor de transmisión de forma simultánea.</p></td>
<td align="left"><p></p>
<ul>
<li><p>Si aumenta la cantidad de clientes que se transmiten simultáneamente desde el mismo servidor, existe una relación lineal con el tiempo de descarga/transmisión del paquete.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Tamaño del paquete que se está transmitiendo.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>El tamaño del paquete tiene un impacto significativo en el tiempo de transmisión y transferencia para paquetes más grandes con un tamaño de aprox. de 1 GB. En el caso de los tamaños de paquetes comprendidos entre 3 MB y 100 MB, los intervalos de tiempo de streaming van de 20 segundos a 100 segundos, con 100 clientes simultáneos.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Red entre el cliente de App-V 5,0 y el servidor de transmisión.</p>
<p></p></td>
<td align="left"><p></p>
<ul>
<li><p>En una red de baja velocidad (1,5 Mbps de ancho de banda), se produce un aumento de 70-80% en el tiempo de respuesta en comparación con la LAN (hasta 100 usuarios).</p></li>
</ul></td>
</tr>
</tbody>
</table>

 

En la siguiente tabla se muestran valores de ejemplo para cada uno de los factores de la lista anterior:

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Escenario</th>
<th align="left">Variación</th>
<th align="left">Número de clientes de App-V 5,0</th>
<th align="left">Tamaño de cada paquete</th>
<th align="left">Tipo de conexión de red de Streaming Server/App-V 5,0 Client</th>
<th align="left">Tiempo de ida y vuelta en el cliente de App-V 5,0 (en segundos)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Varios clientes de App-V 5,0 que transmiten paquetes de aplicaciones virtuales desde un servidor de transmisión.</p></td>
<td align="left"><p>Número de clientes.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>1000</p></li>
<li><p></p></li>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p>1000</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3,5 MB</p></li>
<li><p>3,5 MB</p></li>
<li><p>3,5 MB</p></li>
<li><p></p></li>
<li><p>5 MB</p></li>
<li><p>5 MB</p></li>
<li><p>5 MB</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p></p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>32</p></li>
<li><p>39</p></li>
<li><p>391</p></li>
<li><p></p></li>
<li><p>35</p></li>
<li><p>68</p></li>
<li><p>461</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Tamaño de cada paquete que se está transmitiendo.</p></td>
<td align="left"><p>Tamaño de cada paquete.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p>200</p></li>
<li><p></p></li>
<li><p>100</p></li>
<li><p>200</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>21 MB</p></li>
<li><p>21 MB</p></li>
<li><p></p></li>
<li><p>109</p></li>
<li><p>109</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
<li><p></p></li>
<li><p>LAN</p></li>
<li><p>LAN</p></li>
</ul></td>
<td align="left"><p></p>
<p>33</p>
<p>83</p>
<p></p>
<p>100</p>
<p>160</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Conexión de red entre el cliente y el servidor de streaming de App-V 5,0.</p></td>
<td align="left"><p>red de vínculo lento de 1,5 Mbps.</p></td>
<td align="left"><p></p>
<ul>
<li><p>100</p></li>
<li><p></p></li>
<li><p>100</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>3,5 MB</p></li>
<li><p></p></li>
<li><p>5 MB</p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Red intracontinental de 1,5 Mbps</p></li>
</ul></td>
<td align="left"><p></p>
<p>102</p>
<p></p>
<p>121</p></td>
</tr>
</tbody>
</table>

 

Cada servidor de streaming de App-V 5,0 debe poder administrar un mínimo de 200 clientes que transmitan simultáneamente aplicaciones virtualizadas.

**Nota:**  El tiempo real que se tardará en transmitirse se determina principalmente por el número de clientes que se transtransmiten simultáneamente, el número de paquetes, el tamaño del paquete, la actividad de la red del servidor y las condiciones de la red.

 

Por ejemplo, un usuario promedio puede transmitir un paquete de 100 MB en menos de 2 minutos, cuando se están transmitiendo 100 clientes simultáneos desde el servidor. Sin embargo, un paquete de tamaño de 1 GB podría demorar hasta 30 minutos. En la mayoría de los entornos del mundo real, la demanda por streaming no se distribuye uniformemente, necesitará comprender los requisitos aproximados de transmisión por secuencias máximas presentes en su entorno para ajustar correctamente el número de servidores de streaming requeridos.

El número de clientes que un servidor de streaming puede mejorar puede aumentar significativamente y los requisitos de transmisión por secuencias máximas disminuyeron si se preguardan las aplicaciones. También puede aumentar el número de clientes que un servidor de transmisión puede admitir mediante la entrega de flujo a petición y los paquetes optimizados por secuencias.

## Aplicación de los roles de servidor de App-V 5,0


Descuentos en los requisitos de escala y tolerancia a errores, la cantidad mínima de servidores necesarios para una ubicación con conectividad a Active Directory es una. Este servidor hospedará el servidor de administración, el servicio servidor de administración y los roles de Microsoft SQL Server. Los roles de servidor, por lo tanto, se pueden organizar en cualquier combinación deseada, ya que no entran en conflicto entre sí.

Si se omiten los requisitos de escala, la cantidad mínima de servidores necesarios para proporcionar una implementación tolerante a errores es de cuatro. El servidor de administración y la compatibilidad con los roles de Microsoft SQL Server se colocan en configuraciones tolerantes a errores. El servicio servidor de administración se puede combinar con cualquiera de los roles, pero sigue siendo un punto único de error.

Aunque hay varias estrategias y tecnologías de tolerancia a errores disponibles, no todas son aplicables a un servicio determinado. Además, si se combinan los roles de 5,0 de App-V, es posible que determinadas opciones de tolerancia a errores dejen de aplicarse debido a incompatibilidades.






## Temas relacionados


[Consideraciones compatibles con App-V 5.0](app-v-50-supported-configurations.md)

[Planeación para la alta disponibilidad con App-V 5.0](planning-for-high-availability-with-app-v-50.md)

[Planificación de la implementación de App-V](planning-to-deploy-app-v.md)

 

 





