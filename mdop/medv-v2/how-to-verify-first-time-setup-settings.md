---
title: Cómo comprobar la configuración de instalación de primera vez
description: Cómo comprobar la configuración de instalación de primera vez
author: dansimp
ms.assetid: e8a07d4c-5786-4455-ac43-2deac4042efd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d859d627ec90fbc26d18019062d5e316f907cec6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10813023"
---
# <span data-ttu-id="d10b2-103">Cómo comprobar la configuración de instalación de primera vez</span><span class="sxs-lookup"><span data-stu-id="d10b2-103">How to Verify First Time Setup Settings</span></span>


<span data-ttu-id="d10b2-104">Mientras se ejecuta la prueba de la primera configuración o después de que finalice, puede comprobar la configuración que ha configurado en el área de trabajo de MED-V realizando las siguientes tareas.</span><span class="sxs-lookup"><span data-stu-id="d10b2-104">While your test of first time setup is running or after it finishes, you can verify the settings that you configured in your MED-V workspace by performing the following tasks.</span></span>

<span data-ttu-id="d10b2-105">**Nota:**  Para obtener información sobre cómo supervisar la finalización correcta de la configuración de la primera vez en su empresa después de la implementación, consulte [supervisión de implementaciones del área de trabajo de MED-V](monitoring-med-v-workspace-deployments.md).</span><span class="sxs-lookup"><span data-stu-id="d10b2-105">**Note** For information about how to monitor the successful completion of first time setup throughout your enterprise after deployment, see [Monitoring MED-V Workspace Deployments](monitoring-med-v-workspace-deployments.md).</span></span>

 

**<span data-ttu-id="d10b2-106">Para comprobar la configuración durante la configuración de la primera vez</span><span class="sxs-lookup"><span data-stu-id="d10b2-106">To verify settings during first time setup</span></span>**

1.  <span data-ttu-id="d10b2-107">Mientras se ejecuta la primera configuración, compruebe lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="d10b2-107">While first time setup is running, verify the following:</span></span>

    <span data-ttu-id="d10b2-108">Si especificó el modo **desatendido** , compruebe que la máquina virtual no aparece cuando se está ejecutando por primera vez la configuración.</span><span class="sxs-lookup"><span data-stu-id="d10b2-108">If you specified **Unattended** mode, verify that the virtual machine does not appear when first time setup is running.</span></span>

    <span data-ttu-id="d10b2-109">Si especificó el modo atendido, compruebe que aparece la máquina virtual y que se muestran todos los campos que requieren la entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="d10b2-109">If you specified attended mode, verify that the virtual machine appears and that all fields that require user input are displayed.</span></span>

2.  <span data-ttu-id="d10b2-110">También puede supervisar el proceso completo de primera configuración visualizando la máquina virtual cuando se está ejecutando la primera configuración.</span><span class="sxs-lookup"><span data-stu-id="d10b2-110">You can also monitor the complete first time setup process by viewing the virtual machine when first time setup is running.</span></span> <span data-ttu-id="d10b2-111">Para ello, sigue estos pasos:</span><span class="sxs-lookup"><span data-stu-id="d10b2-111">To do this, follow these steps:</span></span>

    1.  <span data-ttu-id="d10b2-112">Abra la consola de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="d10b2-112">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="d10b2-113">Haga clic en **Inicio**, seleccione **todos los programas**, haga clic en **Windows Virtual PC**y, a continuación, haga clic en **Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="d10b2-113">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="d10b2-114">Inicie MED-V si aún no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="d10b2-114">Start MED-V if it is not already running.</span></span>

        <span data-ttu-id="d10b2-115">Si aún no está presente, en un breve período de tiempo, una máquina virtual con el nombre del área de trabajo de MED-V implementada aparece en la lista de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="d10b2-115">If not already present, in a short time, a virtual machine with the name of the deployed MED-V workspace appears in the list of virtual machines.</span></span>

    3.  <span data-ttu-id="d10b2-116">Haga doble clic en la máquina virtual de MED-V para abrirla.</span><span class="sxs-lookup"><span data-stu-id="d10b2-116">Double-click the MED-V virtual machine to open it.</span></span>

        <span data-ttu-id="d10b2-117">Puede observar la máquina virtual de MED-V cuando se está configurando y puede solucionar el problema del procedimiento de instalación mínima.</span><span class="sxs-lookup"><span data-stu-id="d10b2-117">You can observe the MED-V virtual machine when it is being set up, and you can troubleshoot the Mini-Setup procedure.</span></span> <span data-ttu-id="d10b2-118">Verifique la información de las distintas pantallas según vayan avanzando, como la configuración de redes, la información de unión al dominio del equipo, la configuración del agente invitado, la configuración de la configuración personal y el cierre.</span><span class="sxs-lookup"><span data-stu-id="d10b2-118">Verify the information in the different screens as they go by, such as configuring networking settings, computer domain join information, configuring of the Guest Agent, set up of personal settings, and shutdown.</span></span>

    4.  <span data-ttu-id="d10b2-119">La máquina virtual se cierra automáticamente cuando finaliza la configuración por primera vez.</span><span class="sxs-lookup"><span data-stu-id="d10b2-119">The virtual machine closes automatically when first time setup finishes.</span></span>

        <span data-ttu-id="d10b2-120">**Nota:**  Puede cerrar la ventana del equipo virtual en cualquier momento y la configuración de la primera vez que continúe.</span><span class="sxs-lookup"><span data-stu-id="d10b2-120">**Note** You can close the virtual machine window at any time and first time setup continues.</span></span>

         

**<span data-ttu-id="d10b2-121">Para comprobar la configuración la primera vez que finaliza la configuración</span><span class="sxs-lookup"><span data-stu-id="d10b2-121">To verify settings after first time setup finishes</span></span>**

1.  <span data-ttu-id="d10b2-122">Asegúrese de que la configuración de la primera vez se haya completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d10b2-122">Ensure that first time setup finished successfully.</span></span>

2.  <span data-ttu-id="d10b2-123">Compruebe que el área de trabajo de MED-V esté configurada correctamente.</span><span class="sxs-lookup"><span data-stu-id="d10b2-123">Verify that the MED-V workspace is set up correctly.</span></span>

    1.  <span data-ttu-id="d10b2-124">Abra la consola de Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="d10b2-124">Open the Windows Virtual PC Console.</span></span>

        <span data-ttu-id="d10b2-125">Haga clic en **Inicio**, seleccione **todos los programas**, haga clic en **Windows Virtual PC**y, a continuación, haga clic en **Windows Virtual PC**.</span><span class="sxs-lookup"><span data-stu-id="d10b2-125">Click **Start**, click **All Programs**, click **Windows Virtual PC**, and then click **Windows Virtual PC**.</span></span>

    2.  <span data-ttu-id="d10b2-126">Haga doble clic en el área de trabajo de MED-V instalada.</span><span class="sxs-lookup"><span data-stu-id="d10b2-126">Double-click your installed MED-V workspace.</span></span>

        <span data-ttu-id="d10b2-127">Si el área de trabajo de MED-V ya está ejecutando una aplicación virtual, es posible que se le pregunte si desea cerrar la aplicación antes de abrir la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d10b2-127">If the MED-V workspace is already running a virtual application, you might be prompted to close the application before you can open the virtual machine.</span></span>

    3.  <span data-ttu-id="d10b2-128">En el área de trabajo MED-V, haga clic con el botón secundario en **mi PC**y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="d10b2-128">In the MED-V workspace, right-click **My Computer**, and then click **Properties**.</span></span>

    4.  <span data-ttu-id="d10b2-129">Compruebe que el área de trabajo de MED-V se unió al dominio correcto.</span><span class="sxs-lookup"><span data-stu-id="d10b2-129">Verify that the MED-V workspace joined the correct domain.</span></span> <span data-ttu-id="d10b2-130">Si es aplicable a su organización, pruebe unirse a un dominio especificando dos dominios diferentes para comprobar que el dominio invitado es reemplazado por el dominio host.</span><span class="sxs-lookup"><span data-stu-id="d10b2-130">If applicable to your organization, test domain joining by specifying two different domains to verify that the guest domain is overridden by the host domain.</span></span>

    5.  <span data-ttu-id="d10b2-131">Compruebe que el área de trabajo de MED-V se unió a la unidad organizativa del dominio que especificó.</span><span class="sxs-lookup"><span data-stu-id="d10b2-131">Verify that the MED-V workspace joined the domain organizational unit that you specified.</span></span>

    6.  <span data-ttu-id="d10b2-132">Si especificó la máscara de nombre de equipo, compruebe que el nuevo nombre de equipo coincide con el que se especificó.</span><span class="sxs-lookup"><span data-stu-id="d10b2-132">If you specified the computer name mask, verify that the new computer name matches what was specified.</span></span>

3.  <span data-ttu-id="d10b2-133">Compruebe que la configuración regional que especificó es correcta.</span><span class="sxs-lookup"><span data-stu-id="d10b2-133">Verify that the locale settings that you specified are correct.</span></span>

    1.  <span data-ttu-id="d10b2-134">En el área de trabajo de MED-V, haga clic en **Inicio** y, después, en **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="d10b2-134">In the MED-V workspace, click **Start** and then click **Control Panel**.</span></span>

    2.  <span data-ttu-id="d10b2-135">Compruebe la configuración especificada, por ejemplo, la **fecha y la hora** y la configuración **regional y de idioma**.</span><span class="sxs-lookup"><span data-stu-id="d10b2-135">Verify your specified configuration settings, for example, **Date and Time** and **Regional and Language**.</span></span>

<span data-ttu-id="d10b2-136">**Nota:**  Si encuentra algún problema al comprobar la configuración de la primera vez que se configura, consulte [operaciones de solución de problemas](operations-troubleshooting-medv2.md).</span><span class="sxs-lookup"><span data-stu-id="d10b2-136">**Note** If you encounter any problems when verifying your first time setup settings, see [Operations Troubleshooting](operations-troubleshooting-medv2.md).</span></span>

 

<span data-ttu-id="d10b2-137">Después de comprobar que la configuración de la primera configuración es correcta, puede probar otras configuraciones del área de trabajo de MED-V para comprobar que funcionan como se pretende, como la publicación de aplicaciones y el redireccionamiento de direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="d10b2-137">After you have verified that your first time setup settings are correct, you can test other MED-V workspace configurations to verify that they function as intended, such as application publishing and URL redirection.</span></span>

<span data-ttu-id="d10b2-138">Una vez que haya completado todas las pruebas de su paquete de área de trabajo de MED-V y haya comprobado que funciona como se espera, puede implementar el área de trabajo de MED-V en su empresa.</span><span class="sxs-lookup"><span data-stu-id="d10b2-138">After you have completed all testing of your MED-V workspace package and have verified that it is functioning as intended, you can deploy the MED-V workspace to your enterprise.</span></span>

## <span data-ttu-id="d10b2-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d10b2-139">Related topics</span></span>


[<span data-ttu-id="d10b2-140">Cómo probar la publicación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d10b2-140">How to Test Application Publishing</span></span>](how-to-test-application-publishing.md)

[<span data-ttu-id="d10b2-141">Cómo comprobar el redireccionamiento de la dirección URL</span><span class="sxs-lookup"><span data-stu-id="d10b2-141">How to Test URL Redirection</span></span>](how-to-test-url-redirection.md)

[<span data-ttu-id="d10b2-142">Implementación del paquete del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="d10b2-142">Deploying the MED-V Workspace Package</span></span>](deploying-the-med-v-workspace-package.md)

[<span data-ttu-id="d10b2-143">Administrar la configuración del área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="d10b2-143">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





