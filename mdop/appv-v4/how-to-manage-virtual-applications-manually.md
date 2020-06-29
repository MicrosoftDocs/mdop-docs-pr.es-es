---
title: Cómo administrar aplicaciones virtuales manualmente
description: Cómo administrar aplicaciones virtuales manualmente
author: dansimp
ms.assetid: 583c5255-d3f4-4197-85cd-2a59868d85de
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e8dd5bb9d62950ac1a03ad0ec14802d9e0ff56e8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10817111"
---
# <span data-ttu-id="38288-103">Cómo administrar aplicaciones virtuales manualmente</span><span class="sxs-lookup"><span data-stu-id="38288-103">How to Manage Virtual Applications Manually</span></span>


<span data-ttu-id="38288-104">Puede usar la consola de administración de clientes de Application Virtualization (App-V) para administrar aplicaciones virtuales en el cliente de escritorio de App-V o en el cliente de App-v para servicios de escritorio remoto (anteriormente servicios de Terminal Server).</span><span class="sxs-lookup"><span data-stu-id="38288-104">You can use the Application Virtualization (App-V) Client Management Console to manage virtual applications in the App-V Desktop Client or the App-V Client for Remote Desktop Services (formerly Terminal Services).</span></span> <span data-ttu-id="38288-105">Los administradores de App-V pueden usar realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="38288-105">App-V administrators can use perform the following tasks:</span></span>

## <span data-ttu-id="38288-106">Cómo cargar o descargar una aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-106">How to Load or Unload an App-V Application</span></span>


<span data-ttu-id="38288-107">Puede usar los procedimientos siguientes para cargar o descargar una aplicación de la caché, directamente desde el panel **resultados** del nodo de la **aplicación** en la consola de administración del cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="38288-107">You can use the following procedures to load or unload an application from the cache, directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="38288-108">Al seleccionar este nodo, el panel **resultados** muestra una lista de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="38288-108">When you select this node, the **Results** pane displays a list of applications.</span></span>

<span data-ttu-id="38288-109">**Nota:**  Al cargar o descargar un paquete, todas las aplicaciones del paquete se cargan o se quitan de la caché.</span><span class="sxs-lookup"><span data-stu-id="38288-109">**Note** When you load or unload a package, all the applications in the package are loaded into or removed from cache.</span></span> <span data-ttu-id="38288-110">Al cargar un paquete, si no tiene suficiente espacio en la caché para cargar las aplicaciones, aumente el tamaño de la caché.</span><span class="sxs-lookup"><span data-stu-id="38288-110">When loading a package, if you do not have adequate space in cache to load the applications, increase your cache size.</span></span> <span data-ttu-id="38288-111">Para obtener más información sobre el tamaño de la caché, consulte [Cómo cambiar el tamaño de la caché y la designación de letra de unidad](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span><span class="sxs-lookup"><span data-stu-id="38288-111">For more information about cache size, see [How to Change the Cache Size and the Drive Letter Designation](how-to-change-the-cache-size-and-the-drive-letter-designation.md).</span></span>

 

**<span data-ttu-id="38288-112">Para cargar una aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-112">To load an App-V application</span></span>**

1.  <span data-ttu-id="38288-113">Coloque el cursor en el panel de **resultados** , haga clic con el botón derecho en la aplicación deseada y seleccione **cargar** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="38288-113">Move the cursor to the **Results** pane, right-click the desired application, and select **Load** from the pop-up menu.</span></span>

2.  <span data-ttu-id="38288-114">La aplicación se carga automáticamente.</span><span class="sxs-lookup"><span data-stu-id="38288-114">The application is automatically loaded.</span></span> <span data-ttu-id="38288-115">Se realiza un seguimiento del progreso en la columna denominada **Package status**.</span><span class="sxs-lookup"><span data-stu-id="38288-115">The progress is tracked in the column labeled **Package Status**.</span></span> <span data-ttu-id="38288-116">Debe actualizar la vista para ver que la carga está completa o para ver el progreso.</span><span class="sxs-lookup"><span data-stu-id="38288-116">You must refresh the view to see that the load is complete or to see the progress.</span></span>

**<span data-ttu-id="38288-117">Para descargar una aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-117">To unload an App-V application</span></span>**

1.  <span data-ttu-id="38288-118">Coloque el cursor en el panel de **resultados** , haga clic con el botón derecho en la aplicación deseada y seleccione **Descargar** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="38288-118">Move the cursor to the **Results** pane, right-click the desired application, and select **Unload** from the pop-up menu.</span></span>

2.  <span data-ttu-id="38288-119">La aplicación se descarga automáticamente y la columna de **Estado del paquete** se actualiza para reflejar el cambio.</span><span class="sxs-lookup"><span data-stu-id="38288-119">The application is automatically unloaded, and the **Package Status** column is updated to reflect the change.</span></span>

## <span data-ttu-id="38288-120">Cómo borrar una aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-120">How to clear an App-V application</span></span>


<span data-ttu-id="38288-121">Puede borrar una aplicación de la consola directamente desde el panel de **resultados** del nodo de la **aplicación** en la consola de administración del cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="38288-121">You can clear an application from the console directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="38288-122">Al borrar una aplicación, el sistema quita la configuración, los accesos directos y las asociaciones de tipo de archivo que corresponden a la aplicación y también quita la aplicación de la lista de aplicaciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="38288-122">When you clear an application, the system removes the settings, shortcuts, and file type associations that correspond to the application and also removes the application from the user’s list of applications.</span></span>

<span data-ttu-id="38288-123">**Nota:**  Al borrar una aplicación de la consola, ya no podrá usarla.</span><span class="sxs-lookup"><span data-stu-id="38288-123">**Note** When you clear an application from the console, you can no longer use that application.</span></span> <span data-ttu-id="38288-124">Sin embargo, la aplicación permanece en la caché y sigue estando disponible para otros usuarios en el mismo sistema.</span><span class="sxs-lookup"><span data-stu-id="38288-124">However, the application remains in cache and is still available to other users on the same system.</span></span> <span data-ttu-id="38288-125">Después de una actualización de publicación, las aplicaciones desactivadas volverán a estar disponibles.</span><span class="sxs-lookup"><span data-stu-id="38288-125">After a publishing refresh, the cleared applications will again become available to you.</span></span> <span data-ttu-id="38288-126">Si hay varias aplicaciones en un paquete, la configuración del usuario no se quitará hasta que se borren todas las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="38288-126">If there are multiple applications in a package, the user's settings are not removed until all of the applications are cleared.</span></span>

 

**<span data-ttu-id="38288-127">Para borrar una aplicación de la consola</span><span class="sxs-lookup"><span data-stu-id="38288-127">To clear an application from the console</span></span>**

1.  <span data-ttu-id="38288-128">Coloque el cursor en el panel de **resultados** , haga clic con el botón derecho en la aplicación deseada y seleccione **Borrar** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="38288-128">Move the cursor to the **Results** pane, right-click the desired application, and select **Clear** from the pop-up menu.</span></span>

2.  <span data-ttu-id="38288-129">En el mensaje de confirmación, haga clic en **sí** para quitar la aplicación o en **no** para cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="38288-129">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="38288-130">Cómo reparar una aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-130">How to Repair an App-V application</span></span>


<span data-ttu-id="38288-131">Para reparar una aplicación seleccionada, puede realizar el siguiente procedimiento directamente desde el panel de **resultados** del nodo de la **aplicación** en la consola de administración del cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="38288-131">To repair a selected application, you can perform the following procedure directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span> <span data-ttu-id="38288-132">Al reparar una aplicación, se elimina la configuración de usuario personalizada y se restaura la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="38288-132">When you repair an application, you remove any custom user settings and restore the default settings.</span></span> <span data-ttu-id="38288-133">Esta acción no cambia ni elimina accesos directos ni asociaciones de tipos de archivo, y no quita la aplicación de la caché.</span><span class="sxs-lookup"><span data-stu-id="38288-133">This action does not change or delete shortcuts or file type associations, and it does not remove the application from cache.</span></span>

**<span data-ttu-id="38288-134">Para reparar una aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-134">To repair an App-V application</span></span>**

1.  <span data-ttu-id="38288-135">Mover el cursor al panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="38288-135">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="38288-136">Haga clic con el botón derecho en la aplicación que desee y seleccione **reparar** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="38288-136">Right-click the desired application, and select **Repair** from the pop-up menu.</span></span>

3.  <span data-ttu-id="38288-137">En el mensaje de confirmación, haga clic en **sí** para reparar la aplicación o en **no** para cancelar.</span><span class="sxs-lookup"><span data-stu-id="38288-137">At the confirmation prompt, click **Yes** to repair the application or **No** to cancel.</span></span>

## <span data-ttu-id="38288-138">Cómo importar una aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-138">How to import an App-V application</span></span>


<span data-ttu-id="38288-139">Puede usar el siguiente procedimiento para importar una aplicación a la caché directamente desde el panel **resultados** del nodo de la **aplicación** en la consola de administración del cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="38288-139">You can use the following procedure to import an application into the cache directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="38288-140">Para importar una aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-140">To import an App-V application</span></span>**

1.  <span data-ttu-id="38288-141">Coloque el cursor en el panel de **resultados** , haga clic con el botón derecho en la aplicación deseada y seleccione **importar** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="38288-141">Move the cursor to the **Results** pane, right-click the desired application, and select **Import** from the pop-up menu.</span></span>

2.  <span data-ttu-id="38288-142">En la ventana **examinar** , vaya a la ubicación del archivo de paquete para la aplicación que desee y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="38288-142">From the **Browse** window, navigate to the location of the package file for the desired application, and then click **OK**.</span></span>

    <span data-ttu-id="38288-143">**Nota:**  Si ya ha configurado una ruta de búsqueda de importación o si el archivo SFT se encuentra en la misma ruta que la última importación correcta, el paso 2 no es necesario.</span><span class="sxs-lookup"><span data-stu-id="38288-143">**Note** If you have already configured an import search path or if the SFT file is in the same path as the last successful import, step 2 is not required.</span></span>

     

## <span data-ttu-id="38288-144">Cómo bloquear o desbloquear una aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-144">How to lock or unlock an App-V application</span></span>


<span data-ttu-id="38288-145">Puede usar los procedimientos siguientes para bloquear o desbloquear cualquier aplicación en la memoria caché del cliente de escritorio de Application Virtualization o en el cliente para la caché de servicios de escritorio remoto (anteriormente Terminal Services).</span><span class="sxs-lookup"><span data-stu-id="38288-145">You can use the following procedures to lock or unlock any application in the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services (formerly Terminal Services) cache.</span></span> <span data-ttu-id="38288-146">No se puede quitar una aplicación bloqueada de la caché para hacer sitio para nuevas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="38288-146">A locked application cannot be removed from the cache to make room for new applications.</span></span> <span data-ttu-id="38288-147">Para quitar una aplicación bloqueada de la memoria caché del cliente de escritorio de Application Virtualization o del cliente para la memoria caché de servicios de escritorio remoto, primero debe desbloquearla.</span><span class="sxs-lookup"><span data-stu-id="38288-147">To remove a locked application from the Application Virtualization Desktop Client cache or the Client for Remote Desktop Services cache, you must first unlock it.</span></span>

**<span data-ttu-id="38288-148">Para bloquear una aplicación</span><span class="sxs-lookup"><span data-stu-id="38288-148">To lock an application</span></span>**

1.  <span data-ttu-id="38288-149">Mover el cursor al panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="38288-149">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="38288-150">Haga clic con el botón derecho en la aplicación que desee y seleccione **bloquear** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="38288-150">Right-click the desired application, and select **Lock** from the pop-up menu.</span></span> <span data-ttu-id="38288-151">La aplicación seleccionada está bloqueada en la caché.</span><span class="sxs-lookup"><span data-stu-id="38288-151">The selected application is locked in the cache.</span></span>

**<span data-ttu-id="38288-152">Para desbloquear una aplicación</span><span class="sxs-lookup"><span data-stu-id="38288-152">To unlock an application</span></span>**

1.  <span data-ttu-id="38288-153">Mover el cursor al panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="38288-153">Move the cursor to the **Results** pane.</span></span>

2.  <span data-ttu-id="38288-154">Haga clic con el botón derecho en la aplicación que desee y seleccione **desbloquear** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="38288-154">Right-click the desired application, and select **Unlock** from the pop-up menu.</span></span> <span data-ttu-id="38288-155">La aplicación seleccionada se desbloquea en la caché y se puede quitar.</span><span class="sxs-lookup"><span data-stu-id="38288-155">The selected application is unlocked in the cache and can be removed.</span></span>

## <span data-ttu-id="38288-156">Cómo eliminar una aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-156">How to delete an App-V application</span></span>


<span data-ttu-id="38288-157">Al seleccionar el nodo de la **aplicación** en la consola de administración de cliente de Application Virtualization, el panel **resultados** muestra una lista de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="38288-157">When you select the **Application** node in the Application Virtualization Client Management Console, the **Results** pane displays a list of applications.</span></span> <span data-ttu-id="38288-158">Puede usar el procedimiento siguiente para eliminar una aplicación del panel **resultados** , que también quita la aplicación de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="38288-158">You can use the following procedure to delete an application from the **Results** pane, which also removes the application from the cache.</span></span>

<span data-ttu-id="38288-159">**Nota:**  Al eliminar una aplicación, la aplicación seleccionada dejará de estar disponible para los usuarios de ese cliente.</span><span class="sxs-lookup"><span data-stu-id="38288-159">**Note** When you delete an application, the selected application will no longer be available to any users on that client.</span></span> <span data-ttu-id="38288-160">Los accesos directos y las asociaciones de los tipos de archivo están ocultos y la aplicación se elimina de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="38288-160">Shortcuts and file type associations are hidden, and the application is deleted from cache.</span></span> <span data-ttu-id="38288-161">Sin embargo, si otra aplicación hace referencia a datos en los datos de la caché del sistema de archivos de la aplicación seleccionada, estos elementos no se eliminarán.</span><span class="sxs-lookup"><span data-stu-id="38288-161">However, if another application refers to data in the file system cache data for the selected application, these items will not be deleted.</span></span>

<span data-ttu-id="38288-162">Después de una actualización de publicación, las aplicaciones eliminadas volverán a estar disponibles para usted.</span><span class="sxs-lookup"><span data-stu-id="38288-162">After a publishing refresh, the deleted applications will again become available to you.</span></span>

 

**<span data-ttu-id="38288-163">Para eliminar una aplicación</span><span class="sxs-lookup"><span data-stu-id="38288-163">To delete an application</span></span>**

1.  <span data-ttu-id="38288-164">Coloque el cursor en el panel de **resultados** , haga clic con el botón derecho en la aplicación deseada y seleccione **eliminar** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="38288-164">Move the cursor to the **Results** pane, right-click the desired application, and select **Delete** from the pop-up menu.</span></span>

2.  <span data-ttu-id="38288-165">En el mensaje de confirmación, haga clic en **sí** para quitar la aplicación o en **no** para cancelar la operación.</span><span class="sxs-lookup"><span data-stu-id="38288-165">At the confirmation prompt, click **Yes** to remove the application or click **No** to cancel the operation.</span></span>

## <span data-ttu-id="38288-166">Cómo cambiar un icono de aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-166">How to change an App-V application icon</span></span>


<span data-ttu-id="38288-167">Puede usar el siguiente procedimiento para cambiar un icono asociado a la aplicación seleccionada directamente desde el panel de **resultados** del nodo de la **aplicación** en la consola de administración del cliente de Application Virtualization.</span><span class="sxs-lookup"><span data-stu-id="38288-167">You can use the following procedure to change an icon associated with the selected application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="38288-168">Para cambiar el icono de una aplicación</span><span class="sxs-lookup"><span data-stu-id="38288-168">To change an application icon</span></span>**

1.  <span data-ttu-id="38288-169">Coloque el cursor en el panel **resultados** y haga clic con el botón secundario en la aplicación que desee.</span><span class="sxs-lookup"><span data-stu-id="38288-169">Move the cursor to the **Results** pane, and right-click the desired application.</span></span>

2.  <span data-ttu-id="38288-170">Seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="38288-170">Select **Properties**.</span></span>

3.  <span data-ttu-id="38288-171">En la pestaña **General** , haga clic en **Cambiar icono**.</span><span class="sxs-lookup"><span data-stu-id="38288-171">On the **General** tab, click **Change Icon**.</span></span>

4.  <span data-ttu-id="38288-172">Seleccione el icono que desee o busque otra ubicación para seleccionar el icono.</span><span class="sxs-lookup"><span data-stu-id="38288-172">Select the desired icon, or browse to another location to select the icon.</span></span> <span data-ttu-id="38288-173">Una vez que haya seleccionado el icono, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="38288-173">After you've selected the icon, click **OK**.</span></span> <span data-ttu-id="38288-174">El nuevo icono aparece en el panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="38288-174">The new icon appears in the **Results** pane.</span></span>

## <span data-ttu-id="38288-175">Cómo agregar una aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-175">How to add an App-V application</span></span>


<span data-ttu-id="38288-176">Puede usar el siguiente procedimiento para agregar una aplicación directamente desde el panel **resultados** del nodo de la **aplicación** en la consola de administración del cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="38288-176">You can use the following procedure to add an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="38288-177">Para agregar una aplicación</span><span class="sxs-lookup"><span data-stu-id="38288-177">To add an application</span></span>**

1.  <span data-ttu-id="38288-178">En el panel de **resultados** , haga clic con el botón derecho y seleccione **nueva aplicación** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="38288-178">In the **Results** pane, right-click and select **New Application** from the pop-up menu.</span></span>

2.  <span data-ttu-id="38288-179">En la página del asistente, puede realizar las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="38288-179">On the wizard page, you can perform the following tasks:</span></span>

    1.  <span data-ttu-id="38288-180">**Cambiar icono**: muestra un explorador de iconos estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="38288-180">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="38288-181">Busque y seleccione el icono que quiera.</span><span class="sxs-lookup"><span data-stu-id="38288-181">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="38288-182">**Ruta de acceso del archivo OSD o URL**: escriba una ruta de acceso absoluta local, una ruta de acceso UNC completa (archivo o directorio compartido en una red) o una dirección URL http.</span><span class="sxs-lookup"><span data-stu-id="38288-182">**OSD File Path or URL**—Enter a local absolute path, a full UNC path (shared file or directory on a network), or an HTTP URL.</span></span>

    3.  <span data-ttu-id="38288-183">**(Botón examinar de la OSD)**: muestra el cuadro de diálogo de **archivo abierto** estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="38288-183">**(OSD browse button)**—Displays the standard Windows **Open File** dialog box.</span></span> <span data-ttu-id="38288-184">Busque el archivo que desea encontrar.</span><span class="sxs-lookup"><span data-stu-id="38288-184">Browse to find the desired file.</span></span>

3.  <span data-ttu-id="38288-185">Haga clic en **Finalizar** para agregar la aplicación al panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="38288-185">Click **Finish** to add the application to the **Results** pane.</span></span>

## <span data-ttu-id="38288-186">Cómo publicar un acceso directo a la aplicación App-V</span><span class="sxs-lookup"><span data-stu-id="38288-186">How to publish an App-V application shortcut</span></span>


<span data-ttu-id="38288-187">Puede usar el procedimiento siguiente para publicar accesos directos a una aplicación directamente desde el panel **resultados** del nodo de la **aplicación** en la consola de administración del cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="38288-187">You can use the following procedure to publish shortcuts to an application directly from the **Results** pane of the **Application** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="38288-188">Para publicar accesos directos a aplicaciones</span><span class="sxs-lookup"><span data-stu-id="38288-188">To publish application shortcuts</span></span>**

1.  <span data-ttu-id="38288-189">Coloque el cursor en el panel de **resultados** , haga clic con el botón derecho en la aplicación deseada y seleccione **nuevo acceso directo** en el menú emergente para mostrar el Asistente para nuevo acceso directo.</span><span class="sxs-lookup"><span data-stu-id="38288-189">Move the cursor to the **Results** pane, right-click the desired application, and select **New Shortcut** from the pop-up menu to display the New Shortcut Wizard.</span></span>

2.  <span data-ttu-id="38288-190">En la primera página del Asistente para crear accesos directos, seleccione un icono y especifique un nombre para el acceso directo.</span><span class="sxs-lookup"><span data-stu-id="38288-190">On the first page of the New Shortcut Wizard, select an icon and specify a name for the shortcut.</span></span>

    1.  <span data-ttu-id="38288-191">**Cambiar icono**: muestra un explorador de iconos estándar de Windows.</span><span class="sxs-lookup"><span data-stu-id="38288-191">**Change Icon**—Displays a standard Windows icon browser.</span></span> <span data-ttu-id="38288-192">Busque y seleccione el icono que quiera.</span><span class="sxs-lookup"><span data-stu-id="38288-192">Browse to and select the desired icon.</span></span>

    2.  <span data-ttu-id="38288-193">**Título del acceso directo**: escriba el nombre que desea asignar al acceso directo.</span><span class="sxs-lookup"><span data-stu-id="38288-193">**Shortcut Title**—Enter the name you want to give the shortcut.</span></span> <span data-ttu-id="38288-194">El valor predeterminado de este campo es el nombre y la versión existentes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38288-194">This field defaults to the existing name and version of the application.</span></span>

3.  <span data-ttu-id="38288-195">En la segunda página del asistente, determine la ubicación del acceso directo publicado.</span><span class="sxs-lookup"><span data-stu-id="38288-195">On the second page of the wizard, determine the location of the published shortcut.</span></span>

    1.  <span data-ttu-id="38288-196">**El escritorio**: Seleccione esta casilla para publicar el acceso directo en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="38288-196">**The Desktop**—Select this check box to publish the shortcut to the desktop.</span></span>

    2.  <span data-ttu-id="38288-197">**La barra de herramientas de inicio rápido**: Seleccione esta casilla para publicar el acceso directo en la barra de herramientas Inicio rápido.</span><span class="sxs-lookup"><span data-stu-id="38288-197">**The Quick Launch Toolbar**—Select this check box to publish the shortcut to the Quick Launch toolbar.</span></span>

    3.  <span data-ttu-id="38288-198">**El menú enviar a**: Seleccione esta casilla para publicar el acceso directo en el menú **Enviar a** .</span><span class="sxs-lookup"><span data-stu-id="38288-198">**The Send To Menu**—Select this check box to publish the shortcut to the **Send To** menu.</span></span>

    4.  <span data-ttu-id="38288-199">**Programas en el menú Inicio**: cuando se activa la casilla de verificación **menú Inicio** , este campo se activa.</span><span class="sxs-lookup"><span data-stu-id="38288-199">**Programs in the Start Menu**—When you select the **Start Menu** check box, this field becomes active.</span></span> <span data-ttu-id="38288-200">Deje este campo en blanco para publicar el acceso directo directamente en la raíz de la carpeta programas o escriba un nombre de carpeta o jerarquía, por ejemplo, "My \ _Computer aplicaciones \\Office".</span><span class="sxs-lookup"><span data-stu-id="38288-200">Leave this field blank to publish the shortcut directly to the root of the Programs folder, or enter a folder name or hierarchy—for example, "My\_Computer\\Office Applications."</span></span> <span data-ttu-id="38288-201">Los accesos directos creados de esta manera solo están disponibles para el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="38288-201">Shortcuts created this way are available only for the current user.</span></span>

    5.  <span data-ttu-id="38288-202">**Otra ubicación** y botón **examinar** : al seleccionar la casilla **otra ubicación** , este campo se activa.</span><span class="sxs-lookup"><span data-stu-id="38288-202">**Another location** and **Browse** button—When you select the **Another location** check box, this field becomes active.</span></span> <span data-ttu-id="38288-203">Escriba cualquier ubicación válida en el equipo o cualquier ruta UNC disponible (archivo o directorio compartido en una red).</span><span class="sxs-lookup"><span data-stu-id="38288-203">Enter any valid location on the computer or any available UNC path (shared file or directory on a network).</span></span> <span data-ttu-id="38288-204">El botón **examinar** muestra un cuadro de diálogo estándar de **apertura de archivo** de Windows.</span><span class="sxs-lookup"><span data-stu-id="38288-204">The **Browse** button displays a standard Windows **File Open** dialog box.</span></span>

4.  <span data-ttu-id="38288-205">En la tercera página del asistente, escriba los parámetros de la línea de comandos que desee.</span><span class="sxs-lookup"><span data-stu-id="38288-205">On the third page of the wizard, enter desired command-line parameters.</span></span>

5.  <span data-ttu-id="38288-206">Haga clic en **Finalizar** para publicar los métodos abreviados y salir en el panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="38288-206">Click **Finish** to publish the shortcuts and exit to the **Results** pane.</span></span>

## <span data-ttu-id="38288-207">Cómo agregar una asociación de tipo de archivo para una aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-207">How to add a file type association for an App-V application</span></span>


<span data-ttu-id="38288-208">Puede usar el siguiente procedimiento para agregar una asociación de tipo de archivo mediante el nodo **asociaciones de tipo de archivo** de la consola de administración del cliente de virtualización de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="38288-208">You can use the following procedure to add a file type association, using the **File Type Associations** node in the Application Virtualization Client Management Console.</span></span>

**<span data-ttu-id="38288-209">Para agregar una asociación de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="38288-209">To add a file type association</span></span>**

1.  <span data-ttu-id="38288-210">Haga clic con el botón derecho en el nodo **asociaciones de tipo de archivo** y seleccione **nueva asociación** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="38288-210">Right-click the **File Type Associations** node, and select **New Association** from the pop-up menu.</span></span>

2.  <span data-ttu-id="38288-211">Complete el primer paso del cuadro de diálogo completando la información siguiente y, a continuación, haga clic en **siguiente**:</span><span class="sxs-lookup"><span data-stu-id="38288-211">Complete the first step of the dialog box by completing the following information, and then click **Next**:</span></span>

    1.  <span data-ttu-id="38288-212">**Extensión**: especifique una nueva extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="38288-212">**Extension**—Enter a new file name extension.</span></span> <span data-ttu-id="38288-213">De forma predeterminada, este campo está en blanco.</span><span class="sxs-lookup"><span data-stu-id="38288-213">This field is blank by default.</span></span>

    2.  <span data-ttu-id="38288-214">**Crear un nuevo tipo de archivo con esta descripción**: Seleccione este botón de radio para especificar una nueva descripción de tipo de archivo en el campo activo.</span><span class="sxs-lookup"><span data-stu-id="38288-214">**Create a new file type with this description**—Select this radio button to enter a new file type description in the active field.</span></span> <span data-ttu-id="38288-215">Este botón está seleccionado de forma predeterminada y el campo activo está en blanco.</span><span class="sxs-lookup"><span data-stu-id="38288-215">This button is selected by default, and the active field is blank.</span></span>

    3.  <span data-ttu-id="38288-216">**Aplicar este tipo de archivo a todos los usuarios**: Seleccione esta casilla cuando desee que esta asociación sea global para todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="38288-216">**Apply this file type to all users**—Select this check box when you want this association to be global for all users.</span></span> <span data-ttu-id="38288-217">De forma predeterminada, este cuadro está desactivado.</span><span class="sxs-lookup"><span data-stu-id="38288-217">By default, this box is cleared.</span></span>

    4.  <span data-ttu-id="38288-218">**Vincular esta extensión con un tipo de archivo existente**: Seleccione este botón de radio para asociar la extensión con un tipo de archivo existente.</span><span class="sxs-lookup"><span data-stu-id="38288-218">**Link this extension with an existing file type**—Select this radio button to associate the extension with an existing file type.</span></span> <span data-ttu-id="38288-219">Seleccione un tipo de archivo de la lista desplegable.</span><span class="sxs-lookup"><span data-stu-id="38288-219">Pick a file type from the drop-down list.</span></span> <span data-ttu-id="38288-220">Si elige esta opción, **Next** cambiará a **Finish**.</span><span class="sxs-lookup"><span data-stu-id="38288-220">When you choose this option, **Next** is changed to **Finish**.</span></span>

3.  <span data-ttu-id="38288-221">Complete el segundo paso del cuadro de diálogo completando la información siguiente y, a continuación, haga clic en **Finalizar** para volver a la consola de administración de cliente:</span><span class="sxs-lookup"><span data-stu-id="38288-221">Complete the second step of the dialog box by completing the following information, and then click **Finish** to return to the Client Management Console:</span></span>

    1.  <span data-ttu-id="38288-222">**Cambiar icono**: haga clic en este botón para cambiar el icono de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="38288-222">**Change Icon**—Click this button to change the application icon.</span></span> <span data-ttu-id="38288-223">Seleccione uno de los iconos disponibles, busque una nueva ubicación y seleccione un icono.</span><span class="sxs-lookup"><span data-stu-id="38288-223">Select one of the available icons, or browse to a new location and select an icon.</span></span>

    2.  <span data-ttu-id="38288-224">**Abrir archivos con la aplicación seleccionada**: Seleccione este botón de radio para abrir el archivo con una aplicación existente.</span><span class="sxs-lookup"><span data-stu-id="38288-224">**Open files with the selected application**—Select this radio button to open the file with an existing application.</span></span> <span data-ttu-id="38288-225">Elija una aplicación de la lista desplegable de aplicaciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="38288-225">Choose an application from the drop-down list of available applications.</span></span>

    3.  <span data-ttu-id="38288-226">**Abrir archivo con la asociación que se describe en este archivo OSD**: Seleccione este botón de radio para especificar un archivo de descriptor de software abierto (OSD) que determine la aplicación que se ha usado para abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="38288-226">**Open file with the association described in this OSD file**—Select this radio button to specify an Open Software Descriptor (OSD) file that determines the application used to open the file.</span></span> <span data-ttu-id="38288-227">Use el botón Examinar para seleccionar una ubicación existente o escriba una ruta de acceso o una dirección URL con formato HTTP en este campo.</span><span class="sxs-lookup"><span data-stu-id="38288-227">Use the browse button to select an existing location, or enter a path or HTTP-formatted URL in this field.</span></span>

## <span data-ttu-id="38288-228">Cómo eliminar una asociación de tipo de archivo para una aplicación de App-V</span><span class="sxs-lookup"><span data-stu-id="38288-228">How to delete a file type association for an App-V application</span></span>


<span data-ttu-id="38288-229">Puede usar el procedimiento siguiente para eliminar una asociación de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="38288-229">You can use the following procedure to delete a file type association.</span></span> <span data-ttu-id="38288-230">El nodo **asociaciones de tipo de archivo** está un nivel por debajo del nodo de **virtualización de aplicaciones** en el panel de **ámbito** .</span><span class="sxs-lookup"><span data-stu-id="38288-230">The **File Type Associations** node is one level below the **Application Virtualization** node in the **Scope** pane.</span></span> <span data-ttu-id="38288-231">Al seleccionar este nodo, el panel **resultados** muestra una lista de asociaciones de tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="38288-231">When you select this node, the **Results** pane displays a list of file type associations.</span></span>

**<span data-ttu-id="38288-232">Para quitar una asociación de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="38288-232">To remove a file type association</span></span>**

1.  <span data-ttu-id="38288-233">En el panel de **resultados** , haga clic con el botón secundario en la extensión de la Asociación de tipo de archivo que desea eliminar.</span><span class="sxs-lookup"><span data-stu-id="38288-233">In the **Results** pane, right-click the extension of the file type association you want to delete.</span></span>

2.  <span data-ttu-id="38288-234">Seleccione **eliminar** en el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="38288-234">Select **Delete** from the pop-up menu.</span></span>

3.  <span data-ttu-id="38288-235">Haga clic en **sí** para eliminar la asociación o en **no** para volver al panel **resultados** .</span><span class="sxs-lookup"><span data-stu-id="38288-235">Click **Yes** to delete the association, or click **No** to return to the **Results** pane.</span></span>

## <span data-ttu-id="38288-236">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38288-236">Related topics</span></span>


[<span data-ttu-id="38288-237">Cliente de virtualización de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="38288-237">Application Virtualization Client</span></span>](application-virtualization-client.md)

 

 





