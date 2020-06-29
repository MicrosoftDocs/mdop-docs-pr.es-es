---
title: Cómo configurar una memoria caché de solo lectura en el cliente App-V (RDS)
description: Cómo configurar una memoria caché de solo lectura en el cliente App-V (RDS)
author: dansimp
ms.assetid: b6607fe2-6f92-4567-99f1-d8e3c8a591e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a44844ae9ffc3497151be7713f6a43fda0ccd8fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817950"
---
# <span data-ttu-id="36b0f-103">Cómo configurar una memoria caché de solo lectura en el cliente App-V (RDS)</span><span class="sxs-lookup"><span data-stu-id="36b0f-103">How to Configure a Read-only Cache on the App-V Client (RDS)</span></span>


<span data-ttu-id="36b0f-104">**Importante**  Debe estar ejecutando App-V 4,6, SP1 para poder usar este procedimiento.</span><span class="sxs-lookup"><span data-stu-id="36b0f-104">**Important** You must be running App-V 4.6, SP1 to use this procedure.</span></span>

 

<span data-ttu-id="36b0f-105">Puede implementar el cliente de App-V mediante una memoria caché compartida que se rellena con todas las aplicaciones necesarias para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="36b0f-105">You can deploy the App-V client by using a shared cache that is populated with all the applications required for all users.</span></span> <span data-ttu-id="36b0f-106">A continuación, configure los clientes de servicios de escritorio remoto (RDS) de App-V para que usen el mismo archivo de caché.</span><span class="sxs-lookup"><span data-stu-id="36b0f-106">Then you configure the App-V Remote Desktop Services (RDS) Clients to use the same cache file.</span></span> <span data-ttu-id="36b0f-107">A los usuarios se les concede acceso a aplicaciones específicas mediante el proceso de publicación de App-V.</span><span class="sxs-lookup"><span data-stu-id="36b0f-107">Users are granted access to specific applications by using the App-V publishing process.</span></span> <span data-ttu-id="36b0f-108">Puesto que la memoria caché ya está cargada previamente con todas las aplicaciones, no se produce ninguna transmisión por secuencias cuando un usuario inicia una aplicación.</span><span class="sxs-lookup"><span data-stu-id="36b0f-108">Because the cache is already preloaded with all applications, no streaming occurs when a user starts an application.</span></span> <span data-ttu-id="36b0f-109">Sin embargo, los paquetes que se usan para rellenar previamente la memoria caché deben colocarse en un servidor de App-V que admita la transmisión por secuencias RTSP (Protocolo de transmisión en tiempo real) y que conceda permisos de acceso a los clientes de App-V.</span><span class="sxs-lookup"><span data-stu-id="36b0f-109">However, the packages used to prepopulate the cache must be put on an App-V server that supports Real Time Streaming Protocol (RTSP) streaming and that grants access permissions to the App-V Clients.</span></span> <span data-ttu-id="36b0f-110">Si publica las aplicaciones con un servidor de administración de App-V, puede usarla para proporcionar esta función de transmisión por secuencias.</span><span class="sxs-lookup"><span data-stu-id="36b0f-110">If you publish the applications by using an App-V Management Server, you can use it to provide this streaming function.</span></span>

<span data-ttu-id="36b0f-111">**Nota:**  Los detalles descritos en estos procedimientos están pensados únicamente como ejemplos.</span><span class="sxs-lookup"><span data-stu-id="36b0f-111">**Note** The details outlined in these procedures are intended as examples only.</span></span> <span data-ttu-id="36b0f-112">Puede usar diferentes métodos para completar el proceso general.</span><span class="sxs-lookup"><span data-stu-id="36b0f-112">You might use different methods to complete the overall process.</span></span>

 

## <span data-ttu-id="36b0f-113">Implementar el cliente de App-V en un escenario de RDS</span><span class="sxs-lookup"><span data-stu-id="36b0f-113">Deploying the App-V Client in an RDS Scenario</span></span>


<span data-ttu-id="36b0f-114">El proceso de implementación consta de cuatro tareas principales:</span><span class="sxs-lookup"><span data-stu-id="36b0f-114">The deployment process consists of four primary tasks:</span></span>

-   <span data-ttu-id="36b0f-115">Crear y rellenar el archivo de caché compartida Master</span><span class="sxs-lookup"><span data-stu-id="36b0f-115">Creating and populating the master shared cache file</span></span>

-   <span data-ttu-id="36b0f-116">Copiar el archivo de caché compartido en el almacenamiento del servidor</span><span class="sxs-lookup"><span data-stu-id="36b0f-116">Copying the shared cache file to the server storage</span></span>

-   <span data-ttu-id="36b0f-117">Configuración del software de cliente de App-V</span><span class="sxs-lookup"><span data-stu-id="36b0f-117">Configuring the App-V client software</span></span>

-   <span data-ttu-id="36b0f-118">Administrar el ciclo de implementación de actualizaciones para el archivo de caché compartido después de la implementación inicial</span><span class="sxs-lookup"><span data-stu-id="36b0f-118">Managing the update deployment cycle for the shared cache file after the initial deployment</span></span>

<span data-ttu-id="36b0f-119">Estas tareas requieren un planeamiento cuidadoso.</span><span class="sxs-lookup"><span data-stu-id="36b0f-119">These tasks require careful planning.</span></span> <span data-ttu-id="36b0f-120">Le recomendamos que prepare y documente un proceso metódico reproducible para que su organización siga.</span><span class="sxs-lookup"><span data-stu-id="36b0f-120">We recommend that you prepare and document a methodical, reproducible process for your organization to follow.</span></span> <span data-ttu-id="36b0f-121">Esto es especialmente importante para la preparación y la implementación del archivo de caché compartido maestro y para la administración continuada de las actualizaciones de la aplicación, cada una de las cuales requiere una actualización de la caché compartida maestra.</span><span class="sxs-lookup"><span data-stu-id="36b0f-121">This is especially important for the preparation and deployment of the master shared cache file, and for the ongoing management of application updates, each of which require an update to the master shared cache.</span></span> <span data-ttu-id="36b0f-122">Use los procedimientos siguientes para completar estas tareas principales.</span><span class="sxs-lookup"><span data-stu-id="36b0f-122">Use the following procedures to complete these primary tasks.</span></span>

<span data-ttu-id="36b0f-123">**Nota:**  Aunque puede publicar las aplicaciones con varios métodos diferentes, los procedimientos siguientes se basan en el uso de un servidor de administración de App-V para publicación.</span><span class="sxs-lookup"><span data-stu-id="36b0f-123">**Note** Although you can publish the applications by using several different methods, the following procedures are based on your using an App-V Management Server for publishing.</span></span>

 

**<span data-ttu-id="36b0f-124">Para configurar la caché de solo lectura para la implementación inicial</span><span class="sxs-lookup"><span data-stu-id="36b0f-124">To configure the read-only cache for initial deployment</span></span>**

1. <span data-ttu-id="36b0f-125">Configure y configure un servidor de administración de App-V para proporcionar compatibilidad de autenticación y publicación de usuarios.</span><span class="sxs-lookup"><span data-stu-id="36b0f-125">Set up and configure an App-V Management Server to provide user authentication and publishing support.</span></span>

2. <span data-ttu-id="36b0f-126">Rellene la carpeta de contenido de este servidor de administración con todos los paquetes de aplicaciones necesarios para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="36b0f-126">Populate the Content folder of this Management Server with all the application packages required for all users.</span></span>

3. <span data-ttu-id="36b0f-127">Configure un equipo de ensayo que tenga instalado el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="36b0f-127">Set up a staging computer that has the App-V Client installed.</span></span> <span data-ttu-id="36b0f-128">Inicie sesión en el equipo de ensayo con una cuenta que tenga acceso a todas las aplicaciones, de modo que el conjunto completo de aplicaciones se publique en el equipo y, a continuación, transmita las aplicaciones a la memoria caché para que se carguen por completo.</span><span class="sxs-lookup"><span data-stu-id="36b0f-128">Log on to the staging computer by using an account that has access to all applications so that the complete set of applications are published to the computer, and then stream the applications to cache so that they are fully loaded.</span></span>

   **<span data-ttu-id="36b0f-129">Importante</span><span class="sxs-lookup"><span data-stu-id="36b0f-129">Important</span></span>**  
   <span data-ttu-id="36b0f-130">El equipo de almacenamiento provisional debe usar el mismo tipo de sistema operativo y la misma arquitectura de sistema que usan las máquinas virtuales en las que se ejecutará el cliente de App-V.</span><span class="sxs-lookup"><span data-stu-id="36b0f-130">The staging computer must use the same operating system type and system architecture as those used by the VMs on which the App-V Client will run.</span></span>

     

4. <span data-ttu-id="36b0f-131">Reinicie el equipo de ensayo en modo seguro para asegurarse de que los drivers no se han iniciado, ya que esto bloquearía el archivo de caché.</span><span class="sxs-lookup"><span data-stu-id="36b0f-131">Restart the staging computer in safe mode to make sure that the drivers are not started, because this would lock the cache file.</span></span>

   **<span data-ttu-id="36b0f-132">Nota</span><span class="sxs-lookup"><span data-stu-id="36b0f-132">Note</span></span>**  
   <span data-ttu-id="36b0f-133">O bien, puede detener y deshabilitar el servicio de virtualización de aplicaciones y, a continuación, reiniciar el equipo.</span><span class="sxs-lookup"><span data-stu-id="36b0f-133">Or, you can stop and disable the Application Virtualization service, and then restart the computer.</span></span> <span data-ttu-id="36b0f-134">Una vez que se haya copiado el archivo, recuerde habilitar e iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="36b0f-134">After the file is copied, remember to enable and start the service again.</span></span>

     

5. <span data-ttu-id="36b0f-135">Copie el archivo de la caché Sftfs. FSD a una SAN en la que todos los servidores RDS puedan tener acceso a él, por ejemplo, en una carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="36b0f-135">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="36b0f-136">Establezca los permisos de acceso de la carpeta en solo lectura para el grupo todos y en control total para los administradores que administrarán las actualizaciones de archivos de caché.</span><span class="sxs-lookup"><span data-stu-id="36b0f-136">Set the folder access permissions to Read-only for the group Everyone and to Full Control for administrators who will manage the cache file updates.</span></span> <span data-ttu-id="36b0f-137">La ubicación del archivo de la caché se puede obtener en el registro del AppFS\\FileName.</span><span class="sxs-lookup"><span data-stu-id="36b0f-137">The location of the cache file can be obtained from the registry AppFS\\FileName.</span></span>

   **<span data-ttu-id="36b0f-138">Importante</span><span class="sxs-lookup"><span data-stu-id="36b0f-138">Important</span></span>**  
   <span data-ttu-id="36b0f-139">Debe colocar el archivo FSD en una ubicación que tenga la capacidad de respuesta y la confiabilidad iguales al rendimiento del almacenamiento conectado localmente, por ejemplo, un SAN.</span><span class="sxs-lookup"><span data-stu-id="36b0f-139">You must put the FSD file in a location that has the responsiveness and reliability equal to locally attached storage performance, for example, a SAN.</span></span>

     

6. <span data-ttu-id="36b0f-140">Instale el cliente de aplicación-V RDS en cada servidor RDS y, a continuación, configúrelo para usar la caché de solo lectura agregando los siguientes valores de clave del registro a la clave AppFS en el cliente.</span><span class="sxs-lookup"><span data-stu-id="36b0f-140">Install the App-V RDS Client on each RDS server, and then configure it to use the read-only cache by adding the following registry key values to the AppFS key on the client.</span></span> <span data-ttu-id="36b0f-141">La clave AppFS se encuentra en HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS en los equipos de 32 bits y en HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS para equipos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="36b0f-141">The AppFS key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\]Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 32-bit computers and at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS for 64-bit computers.</span></span>

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left"><span data-ttu-id="36b0f-142">Tecla</span><span class="sxs-lookup"><span data-stu-id="36b0f-142">Key</span></span></th>
   <th align="left"><span data-ttu-id="36b0f-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="36b0f-143">Type</span></span></th>
   <th align="left"><span data-ttu-id="36b0f-144">Valor</span><span class="sxs-lookup"><span data-stu-id="36b0f-144">Value</span></span></th>
   <th align="left"><span data-ttu-id="36b0f-145">Propósito</span><span class="sxs-lookup"><span data-stu-id="36b0f-145">Purpose</span></span></th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="36b0f-146">FileName</span><span class="sxs-lookup"><span data-stu-id="36b0f-146">FileName</span></span></p></td>
   <td align="left"><p><span data-ttu-id="36b0f-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="36b0f-147">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="36b0f-148">Ruta de FSD</span><span class="sxs-lookup"><span data-stu-id="36b0f-148">path of FSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="36b0f-149">Especifica la ruta de acceso al archivo de la caché compartida, por ejemplo, \RDSServername\Sharefolder\SFTFS. FSD (obligatorio).</span><span class="sxs-lookup"><span data-stu-id="36b0f-149">Specifies the path of the shared cache file, for example, \RDSServername\Sharefolder\SFTFS.FSD (Required).</span></span></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><span data-ttu-id="36b0f-150">ReadOnlyFSD</span><span class="sxs-lookup"><span data-stu-id="36b0f-150">ReadOnlyFSD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="36b0f-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="36b0f-151">DWORD</span></span></p></td>
   <td align="left"><p><span data-ttu-id="36b0f-152">uno</span><span class="sxs-lookup"><span data-stu-id="36b0f-152">1</span></span></p></td>
   <td align="left"><p><span data-ttu-id="36b0f-153">Configura el cliente para que funcione en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="36b0f-153">Configures the client to operate in Read-Only mode.</span></span> <span data-ttu-id="36b0f-154">Esto garantiza que el cliente no intentará transmitir las actualizaciones a la caché del paquete.</span><span class="sxs-lookup"><span data-stu-id="36b0f-154">This ensures that the client will not try to stream updates to the package cache.</span></span> <span data-ttu-id="36b0f-155">(Necesario)</span><span class="sxs-lookup"><span data-stu-id="36b0f-155">(Required)</span></span></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><span data-ttu-id="36b0f-156">ErrorLogLocation</span><span class="sxs-lookup"><span data-stu-id="36b0f-156">ErrorLogLocation</span></span></p></td>
   <td align="left"><p><span data-ttu-id="36b0f-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="36b0f-157">String</span></span></p></td>
   <td align="left"><p><span data-ttu-id="36b0f-158">Ruta de acceso del archivo de registro de errores (. ETL)</span><span class="sxs-lookup"><span data-stu-id="36b0f-158">path of error log (.etl) file</span></span></p></td>
   <td align="left"><p><span data-ttu-id="36b0f-159">Entrada usada para especificar la ruta de acceso del registro de errores.</span><span class="sxs-lookup"><span data-stu-id="36b0f-159">Entry used to specify the path of the error log.</span></span> <span data-ttu-id="36b0f-160">Práctica.</span><span class="sxs-lookup"><span data-stu-id="36b0f-160">(Recommended.</span></span> <span data-ttu-id="36b0f-161">Use una ruta local, como C:\Logs\Sftfs.etl).</span><span class="sxs-lookup"><span data-stu-id="36b0f-161">Use a local path such as C:\Logs\Sftfs.etl).</span></span></p></td>
   </tr>
   </tbody>
   </table>

     

7. <span data-ttu-id="36b0f-162">Configure cada servidor RDS de la granja para usar el servidor de publicación y para usar la actualización de publicación cuando los usuarios inicien sesión.</span><span class="sxs-lookup"><span data-stu-id="36b0f-162">Configure each RDS server in the farm to use the publishing server and to use publishing update when users log on.</span></span> <span data-ttu-id="36b0f-163">A medida que los usuarios inician sesión en los servidores de RDS, se produce un ciclo de actualización de publicación y se publican todas las aplicaciones para las que su cuenta está autorizada.</span><span class="sxs-lookup"><span data-stu-id="36b0f-163">As users log on to the RDS servers, a publishing update cycle occurs and publishes all the applications for which their account is authorized.</span></span> <span data-ttu-id="36b0f-164">Estas aplicaciones se ejecutan desde la memoria caché compartida.</span><span class="sxs-lookup"><span data-stu-id="36b0f-164">These applications are run from the shared cache.</span></span>

**<span data-ttu-id="36b0f-165">Para configurar el cliente de RDS para la actualización de paquetes</span><span class="sxs-lookup"><span data-stu-id="36b0f-165">To configure the RDS client for package upgrade</span></span>**

1.  <span data-ttu-id="36b0f-166">Complete la actualización y las pruebas del paquete de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="36b0f-166">Complete the upgrade and testing of the application package.</span></span>

2.  <span data-ttu-id="36b0f-167">Actualice el paquete en el servidor de App-V.</span><span class="sxs-lookup"><span data-stu-id="36b0f-167">Upgrade the package on the App-V server.</span></span> <span data-ttu-id="36b0f-168">A continuación, publique y transmita la nueva versión de las aplicaciones al cliente en el equipo de ensayo para que se carguen por completo en la caché.</span><span class="sxs-lookup"><span data-stu-id="36b0f-168">Then, publish and stream the new version of the applications to the client on the staging computer so that they are fully loaded into cache.</span></span>

3.  <span data-ttu-id="36b0f-169">Reinicie el equipo de ensayo en modo seguro para asegurarse de que los drivers no se han iniciado.</span><span class="sxs-lookup"><span data-stu-id="36b0f-169">Restart the staging computer in safe mode to ensure the drivers are not started.</span></span>

    <span data-ttu-id="36b0f-170">**Nota:**  También puede detener y, a continuación, deshabilitar el servicio de virtualización de aplicaciones en Services. msc y reiniciar el equipo.</span><span class="sxs-lookup"><span data-stu-id="36b0f-170">**Note** Or, you can first stop and then disable the Application Virtualization service in the Services.msc, and restart the computer.</span></span> <span data-ttu-id="36b0f-171">Una vez que se haya copiado el archivo, recuerde habilitar e iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="36b0f-171">After the file has been copied, remember to enable and start the service again.</span></span>

     

4.  <span data-ttu-id="36b0f-172">Copie el archivo de la caché Sftfs. FSD a una SAN en la que todos los servidores RDS puedan tener acceso a él, por ejemplo, en una carpeta compartida.</span><span class="sxs-lookup"><span data-stu-id="36b0f-172">Copy the Sftfs.fsd cache file to a SAN where all the RDS servers can access it, such as in a shared folder.</span></span> <span data-ttu-id="36b0f-173">Puede usar un nombre de archivo diferente, por ejemplo, SFTFS \ _V2. FSD, para distinguir la nueva versión.</span><span class="sxs-lookup"><span data-stu-id="36b0f-173">You can use a different file name, for example, SFTFS\_V2.FSD, to distinguish the new version.</span></span>

5.  <span data-ttu-id="36b0f-174">Para configurar el cliente de App-V RDS en cada servidor RDS de la granja para usar el archivo de caché compartido actualizado, cambie el valor del nombre de archivo de la clave de registro AppFS para que apunte a la ubicación del archivo actualizado, por ejemplo, \\\\RDSServername\\Sharefolder\\SFTFS\ _V2. FSD.</span><span class="sxs-lookup"><span data-stu-id="36b0f-174">To configure the App-V RDS Client on each RDS server in the farm to use the updated shared cache file, change the AppFS registry key FILENAME value to point to the location of the updated file, for example, \\\\RDSServername\\Sharefolder\\SFTFS\_V2.FSD.</span></span> <span data-ttu-id="36b0f-175">Esto garantiza que cada servidor RDS recibirá la copia actualizada de la memoria caché cuando se reinicien los drivers de App-Vclient.</span><span class="sxs-lookup"><span data-stu-id="36b0f-175">This guarantees that each RDS server receives the updated copy of the cache when the App-Vclient drivers restart.</span></span>

    <span data-ttu-id="36b0f-176">**Importante**  Debe reiniciar los servidores de RDS para poder usar el archivo de caché compartido actualizado.</span><span class="sxs-lookup"><span data-stu-id="36b0f-176">**Important** You must restart the RDS servers in order to use the updated shared cache file.</span></span>

     

## <span data-ttu-id="36b0f-177">Cómo usar vínculos simbólicos al actualizar la caché</span><span class="sxs-lookup"><span data-stu-id="36b0f-177">How to Use Symbolic Links when Upgrading the Cache</span></span>


<span data-ttu-id="36b0f-178">En lugar de cambiar el valor del nombre de archivo de la clave AppFS cada vez que se implementa un nuevo archivo de caché que contiene paquetes nuevos o actualizados, puede usar un vínculo simbólico en los siguientes sistemas operativos: Windows Vista, Windows 7 y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="36b0f-178">Instead of changing the AppFS key FILENAME value every time that a new cache file is deployed that contains new or upgraded packages, you can use a symbolic link in the following operating systems: Windows Vista, Windows 7, and Windows Server 2008.</span></span> <span data-ttu-id="36b0f-179">Para obtener más información sobre los vínculos simbólicos, consulte [vínculos simbólicos](https://go.microsoft.com/fwlink/?LinkId=157626) ( https://go.microsoft.com/fwlink/?LinkId=157626) .</span><span class="sxs-lookup"><span data-stu-id="36b0f-179">For more information about symbolic links, see [Symbolic Links](https://go.microsoft.com/fwlink/?LinkId=157626) (https://go.microsoft.com/fwlink/?LinkId=157626).</span></span> <span data-ttu-id="36b0f-180">Por el contrario, Windows XP no admite el uso de vínculos simbólicos y, en su lugar, debe usar puntos de Unión.</span><span class="sxs-lookup"><span data-stu-id="36b0f-180">In contrast, Windows XP does not support the use of symbolic links, and you must use junction points instead.</span></span> <span data-ttu-id="36b0f-181">Para obtener más información acerca de las uniones, consulte el [artículo 205524](https://go.microsoft.com/fwlink/?LinkId=182553) en Microsoft Knowledge base ( https://go.microsoft.com/fwlink/?LinkId=182553) y también la herramienta Unión de la versión [v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) ( https://go.microsoft.com/fwlink/?LinkId=182554) .</span><span class="sxs-lookup"><span data-stu-id="36b0f-181">For more information about junctions, see [article 205524](https://go.microsoft.com/fwlink/?LinkId=182553) in the Microsoft Knowledge Base (https://go.microsoft.com/fwlink/?LinkId=182553), and also the tool [Junction v1.05](https://go.microsoft.com/fwlink/?LinkId=182554) (https://go.microsoft.com/fwlink/?LinkId=182554).</span></span>

**<span data-ttu-id="36b0f-182">Para configurar un vínculo simbólico para que haga referencia a la caché</span><span class="sxs-lookup"><span data-stu-id="36b0f-182">To configure a symbolic link to reference the cache</span></span>**

1.  <span data-ttu-id="36b0f-183">Durante la fase de implementación inicial, abra una ventana del símbolo del sistema como administrador local en el sistema operativo host del servidor RDS.</span><span class="sxs-lookup"><span data-stu-id="36b0f-183">During the initial deployment stage, open a Command Prompt window as a local administrator on the RDS server host operating system.</span></span>

2.  <span data-ttu-id="36b0f-184">Cree un vínculo simbólico mediante el comando MKLINK y, a continuación, configúrelo para que apunte al archivo Sftfs. FSD.</span><span class="sxs-lookup"><span data-stu-id="36b0f-184">Create a symbolic link by using the MKLINK command, and then configure it to point to the Sftfs.fsd file.</span></span>

    **     <span data-ttu-id="36b0f-185">mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd</span><span class="sxs-lookup"><span data-stu-id="36b0f-185">mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd</span></span>**

3.  <span data-ttu-id="36b0f-186">En la imagen de VM maestra de VDI, abra una ventana del símbolo del sistema con la opción **Ejecutar como administrador** y otorgue permisos de vínculos remotos para que la máquina virtual pueda acceder al vínculo simbólico en el sistema operativo host de VDI.</span><span class="sxs-lookup"><span data-stu-id="36b0f-186">On the VDI Master VM Image, open a Command Prompt window by using the **Run as administrator** option and grant remote link permissions so that the VM can access the symbolic link on the VDI Host operating system.</span></span> <span data-ttu-id="36b0f-187">De forma predeterminada, los permisos de vínculos remotos están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="36b0f-187">By default, remote link permissions are disabled.</span></span>

    **<span data-ttu-id="36b0f-188">fsutil Behavior Set SymlinkEvaluation R2R: 1</span><span class="sxs-lookup"><span data-stu-id="36b0f-188">fsutil behavior set SymlinkEvaluation R2R:1</span></span>**

    <span data-ttu-id="36b0f-189">**Nota:**  En el servidor de almacenamiento, los permisos de vínculo apropiados deben estar habilitados.</span><span class="sxs-lookup"><span data-stu-id="36b0f-189">**Note** On the storage server, appropriate link permissions must be enabled.</span></span> <span data-ttu-id="36b0f-190">Según la ubicación del vínculo y el archivo Sftfs. FSD, los permisos son **L2L: 1** o **L2R: 1** o **R2L: 1** o **R2R: 1**.</span><span class="sxs-lookup"><span data-stu-id="36b0f-190">Depending on the location of link and the Sftfs.fsd file, the permissions are **L2L:1** or **L2R:1** or **R2L:1** or **R2R:1**.</span></span>

     

4.  <span data-ttu-id="36b0f-191">Cuando configures el cliente de usuario de App-V, establece el valor de nombre de archivo de la clave AppFS igual a la ruta de acceso UNC del archivo FSD que usa el vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="36b0f-191">When you configure the App-V RDS Client, set the AppFS key FILENAME value equal to the UNC path of the FSD file that is using the symbolic link.</span></span> <span data-ttu-id="36b0f-192">Por ejemplo, establezca el nombre de archivo en \\\\VDIHostserver\\Symlinkname.</span><span class="sxs-lookup"><span data-stu-id="36b0f-192">For example, set the file name to \\\\VDIHostserver\\Symlinkname.</span></span> <span data-ttu-id="36b0f-193">Cuando el cliente de App-V accede por primera vez a la caché, el vínculo simbólico pasa al cliente un identificador para el archivo de la caché.</span><span class="sxs-lookup"><span data-stu-id="36b0f-193">When the App-V client first accesses the cache, the symbolic link passes to the client a handle to the cache file.</span></span> <span data-ttu-id="36b0f-194">El cliente continúa usando ese identificador siempre que se esté ejecutando el cliente.</span><span class="sxs-lookup"><span data-stu-id="36b0f-194">The client continues to use that handle as long as the client is running.</span></span> <span data-ttu-id="36b0f-195">El valor del vínculo simbólico puede actualizarse de forma segura incluso si los clientes existentes tienen la caché compartida antigua abierta.</span><span class="sxs-lookup"><span data-stu-id="36b0f-195">The value of the symbolic link can safely be updated even if existing clients have the old shared cache open.</span></span>

5.  <span data-ttu-id="36b0f-196">Cuando deba actualizar un paquete o agregar un nuevo paquete a la caché, siga los pasos 1 a 4 del procedimiento de actualización.</span><span class="sxs-lookup"><span data-stu-id="36b0f-196">When you must upgrade a package or to add a new package to the cache, follow steps 1 through 4 of the upgrade procedure.</span></span> <span data-ttu-id="36b0f-197">A continuación, elimine el vínculo simbólico y vuelva a crearlo para que apunte a la nueva versión del archivo de caché compartido.</span><span class="sxs-lookup"><span data-stu-id="36b0f-197">Then, delete the symbolic link and re-create it to point to the new version of the shared cache file.</span></span> <span data-ttu-id="36b0f-198">Esto garantiza que cada servidor RDS recibirá la copia actualizada de la caché cuando se reinicien los drivers del cliente App-V.</span><span class="sxs-lookup"><span data-stu-id="36b0f-198">This guarantees that each RDS server receives the updated copy of the cache when the App-V client drivers restart.</span></span> <span data-ttu-id="36b0f-199">Cuando se reinicia el servidor RDS, el cliente de App-V recibe un identificador de la copia actualizada de la caché porque el cliente usa la ruta de acceso que contiene el vínculo simbólico actualizado.</span><span class="sxs-lookup"><span data-stu-id="36b0f-199">When the RDS server is restarted, the App-V client receives a handle to the updated copy of the cache because the client uses the path that contains the updated symbolic link.</span></span> <span data-ttu-id="36b0f-200">A continuación, los usuarios tienen acceso a las aplicaciones nuevas y actualizadas.</span><span class="sxs-lookup"><span data-stu-id="36b0f-200">Then, the users have access to the new and updated applications.</span></span>

## <span data-ttu-id="36b0f-201">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="36b0f-201">Related topics</span></span>


[<span data-ttu-id="36b0f-202">Cómo instalar el servidor de administración de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="36b0f-202">How to Install Application Virtualization Management Server</span></span>](how-to-install-application-virtualization-management-server.md)

[<span data-ttu-id="36b0f-203">Cómo instalar manualmente el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="36b0f-203">How to Manually Install the Application Virtualization Client</span></span>](how-to-manually-install-the-application-virtualization-client.md)

[<span data-ttu-id="36b0f-204">Cómo instalar el cliente mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="36b0f-204">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





