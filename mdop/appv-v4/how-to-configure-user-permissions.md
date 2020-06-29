---
title: Cómo configurar los permisos de usuario
description: Cómo configurar los permisos de usuario
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817731"
---
# <span data-ttu-id="8635e-103">Cómo configurar los permisos de usuario</span><span class="sxs-lookup"><span data-stu-id="8635e-103">How to Configure User Permissions</span></span>


<span data-ttu-id="8635e-104">Puede habilitar y deshabilitar algunas acciones para los usuarios que no tienen derechos administrativos modificando los valores de clave en la clave del registro de **permisos** (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions).</span><span class="sxs-lookup"><span data-stu-id="8635e-104">You can enable and disable some actions for users who do not have administrative rights by editing the key values under the **Permissions** registry key (HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions).</span></span> <span data-ttu-id="8635e-105">Esta clave se ha diseñado principalmente para ayudar a evitar que los usuarios hagan errores en lugar de proporcionar seguridad especial, ya que los usuarios con derechos administrativos pueden modificar cualquiera de estos valores de clave.</span><span class="sxs-lookup"><span data-stu-id="8635e-105">This key is primarily designed to help prevent users from making mistakes rather than to provide any special security, because users with administrative rights can edit any of these key values.</span></span> <span data-ttu-id="8635e-106">Los procedimientos siguientes son ejemplos de cómo cambiar los valores de las claves.</span><span class="sxs-lookup"><span data-stu-id="8635e-106">The following procedures are examples of how to change the key values.</span></span> <span data-ttu-id="8635e-107">Para obtener más información sobre los valores y las claves de registro del cliente de Application Virtualization (App-V), consulte <https://go.microsoft.com/fwlink/?LinkId=121528> .</span><span class="sxs-lookup"><span data-stu-id="8635e-107">For more information about the Application Virtualization (App-V) Client registry keys and values, see <https://go.microsoft.com/fwlink/?LinkId=121528>.</span></span>

**<span data-ttu-id="8635e-108">Para cambiar los permisos de usuario</span><span class="sxs-lookup"><span data-stu-id="8635e-108">To change user permissions</span></span>**

1.  <span data-ttu-id="8635e-109">Para permitir que los usuarios elijan ejecutar el cliente en el modo sin conexión, establezca el valor de clave siguiente en 1:</span><span class="sxs-lookup"><span data-stu-id="8635e-109">To enable the users to choose to run the client in offline mode, set the following key value to 1:</span></span>

    <span data-ttu-id="8635e-110">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode</span><span class="sxs-lookup"><span data-stu-id="8635e-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode</span></span>

2.  <span data-ttu-id="8635e-111">Para permitir que los usuarios vean todas las aplicaciones a través de la interfaz de usuario, establezca el valor de clave siguiente en 1.</span><span class="sxs-lookup"><span data-stu-id="8635e-111">To enable the users to view all applications through the user interface, set the following key value to 1.</span></span> <span data-ttu-id="8635e-112">Establecer el valor en 0 (cero) permite a los usuarios ver solo las aplicaciones que están disponibles.</span><span class="sxs-lookup"><span data-stu-id="8635e-112">Setting the value to 0 (zero) allows the users to see only the applications that are available to them.</span></span>

    <span data-ttu-id="8635e-113">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications</span><span class="sxs-lookup"><span data-stu-id="8635e-113">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications</span></span>

## <span data-ttu-id="8635e-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8635e-114">Related topics</span></span>


[<span data-ttu-id="8635e-115">Cómo establecer la configuración de registro del cliente de App-V mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="8635e-115">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[<span data-ttu-id="8635e-116">Permisos de acceso de usuario en el cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="8635e-116">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





