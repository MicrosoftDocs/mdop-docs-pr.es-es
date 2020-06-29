---
title: Cómo administrar la compatibilidad de hardware
description: Cómo administrar la compatibilidad de hardware
author: dansimp
ms.assetid: c74b96b9-8161-49bc-b5bb-4838734e7df5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cf9e2c5b2b33ea93d9834a81700bd2be8a9b9757
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812983"
---
# <span data-ttu-id="4df5e-103">Cómo administrar la compatibilidad de hardware</span><span class="sxs-lookup"><span data-stu-id="4df5e-103">How to Manage Hardware Compatibility</span></span>


<span data-ttu-id="4df5e-104">Administración y supervisión de Microsoft BitLocker (MBAM) puede recopilar información sobre el fabricante y el modelo de equipos cliente después de implementar la Directiva de grupo permitir comprobación de la compatibilidad del hardware.</span><span class="sxs-lookup"><span data-stu-id="4df5e-104">Microsoft BitLocker Administration and Monitoring (MBAM) can collect information about the manufacturer and model of client computers after you deploy the Allow Hardware Compatibility Checking Group Policy.</span></span> <span data-ttu-id="4df5e-105">Si configura esta Directiva, el agente de MBAM notifica la marca del equipo y la información del modelo al servidor de MBAM cuando se implementa el cliente MBAM en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="4df5e-105">If you configure this policy, the MBAM agent reports the computer make and model information to the MBAM Server when the MBAM Client is deployed on a client computer.</span></span>

<span data-ttu-id="4df5e-106">La característica compatibilidad de hardware es útil cuando la organización tiene equipos o hardware de equipos antiguos que no son compatibles con los chips del módulo de plataforma segura (TPM).</span><span class="sxs-lookup"><span data-stu-id="4df5e-106">The Hardware Compatibility feature is helpful when your organization has older computer hardware or computers that do not support Trusted Platform Module (TPM) chips.</span></span> <span data-ttu-id="4df5e-107">En estos casos, puede usar la característica compatibilidad de hardware para asegurarse de que el cifrado de BitLocker solo se aplica a los modelos de equipo que lo admiten.</span><span class="sxs-lookup"><span data-stu-id="4df5e-107">In these cases, you can use the Hardware Compatibility feature to ensure that BitLocker encryption is applied only to computer models that support it.</span></span> <span data-ttu-id="4df5e-108">Si todos los equipos de su organización van a admitir BitLocker, no tiene que usar la característica de compatibilidad de hardware.</span><span class="sxs-lookup"><span data-stu-id="4df5e-108">If all computers in your organization will support BitLocker, you do not have to use the Hardware Compatibility feature.</span></span>

<span data-ttu-id="4df5e-109">**Nota:**  De forma predeterminada, la característica de compatibilidad de hardware de MBAM no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="4df5e-109">**Note** By default, MBAM Hardware Compatibility feature is not enabled.</span></span> <span data-ttu-id="4df5e-110">Para habilitarlo, seleccione la característica **compatibilidad de hardware** en la característica servidor de **Administración y supervisión** durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="4df5e-110">To enable it, select the **Hardware Compatibility** feature under the **Administration and Monitoring Server** feature during setup.</span></span> <span data-ttu-id="4df5e-111">Para obtener más información sobre cómo configurar y configurar la compatibilidad de hardware, consulte [implementación de la infraestructura de servidor de MBAM 1,0](deploying-the-mbam-10-server-infrastructure.md).</span><span class="sxs-lookup"><span data-stu-id="4df5e-111">For more information about how to set up and configure Hardware Compatibility, see [Deploying the MBAM 1.0 Server Infrastructure](deploying-the-mbam-10-server-infrastructure.md).</span></span>

 

<span data-ttu-id="4df5e-112">La característica compatibilidad de hardware funciona de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="4df5e-112">The Hardware Compatibility feature works in the following way.</span></span>

****

1.  <span data-ttu-id="4df5e-113">El agente de cliente de MBAM descubre información básica del equipo, como el fabricante, el modelo, el creador de BIOS, la versión de BIOS, el creador de TPM y la versión de TPM y, a continuación, pasa esta información al servidor de MBAM.</span><span class="sxs-lookup"><span data-stu-id="4df5e-113">The MBAM client agent discovers basic computer information such as manufacturer, model, BIOS maker, BIOS version, TPM maker, and TPM version, and then passes this information to the MBAM server.</span></span>

2.  <span data-ttu-id="4df5e-114">El servidor de MBAM genera una lista de las funciones y los modelos de equipos cliente que permiten diferenciar entre los que pueden o no son compatibles con BitLocker</span><span class="sxs-lookup"><span data-stu-id="4df5e-114">The MBAM server generates a list of client computer makes and models to enable you to differentiate between those that can or cannot support BitLocker</span></span>

3.  <span data-ttu-id="4df5e-115">Los agentes de cliente de MBAM que se implementan en la empresa actualizan automáticamente esta lista con todos los nuevos equipos y los modelos que se detectan con un estado de **desconocido**.</span><span class="sxs-lookup"><span data-stu-id="4df5e-115">The MBAM client agents that are deployed in the enterprise automatically update this list with all new computer makes and models that are discovered with a state of **Unknown**.</span></span> <span data-ttu-id="4df5e-116">Un administrador puede usar el sitio web de administración de MBAM para cambiar las entradas de la lista y especificar una marca y un modelo de equipo determinado como **compatible** o **incompatible**.</span><span class="sxs-lookup"><span data-stu-id="4df5e-116">An administrator can then use the MBAM administration website to change list entries to specify a particular computer make and model as **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="4df5e-117">Antes de que el agente de cliente de MBAM empiece a cifrar una unidad, el agente verifica primero la compatibilidad de cifrado de BitLocker del hardware en el que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="4df5e-117">Before the MBAM client agent begins encrypting a drive, the agent first verifies the BitLocker encryption compatibility of the hardware it is running on.</span></span>

    -   <span data-ttu-id="4df5e-118">Si el hardware está marcado como compatible, el proceso de cifrado de BitLocker se inicia.</span><span class="sxs-lookup"><span data-stu-id="4df5e-118">If the hardware is marked as compatible, the BitLocker encryption process starts.</span></span> <span data-ttu-id="4df5e-119">MBAM también volverá a comprobar el estado de compatibilidad de hardware del equipo una vez al día.</span><span class="sxs-lookup"><span data-stu-id="4df5e-119">MBAM will also recheck the hardware compatibility status of the computer one time per day.</span></span>

    -   <span data-ttu-id="4df5e-120">Si el hardware se marca como incompatible, el agente registra un evento y pasa un estado de "hardware exento" como parte de los informes de cumplimiento normativo.</span><span class="sxs-lookup"><span data-stu-id="4df5e-120">If the hardware is marked as incompatible, the agent logs an event and passes a “hardware exempted” state as part of compliance reporting.</span></span> <span data-ttu-id="4df5e-121">El agente verifica cada siete días para ver si el estado ha cambiado a "compatible".</span><span class="sxs-lookup"><span data-stu-id="4df5e-121">The agent checks every seven days to see whether the state has changed to “compatible.”</span></span>

    -   <span data-ttu-id="4df5e-122">Si el hardware está marcado como desconocido, el proceso de cifrado de BitLocker no se iniciará.</span><span class="sxs-lookup"><span data-stu-id="4df5e-122">If the hardware is marked as unknown, the BitLocker encryption process will not begin.</span></span> <span data-ttu-id="4df5e-123">El agente de cliente de MBAM volverá a comprobar el estado de compatibilidad de hardware del equipo una vez al día.</span><span class="sxs-lookup"><span data-stu-id="4df5e-123">The MBAM client agent will recheck the hardware compatibility status of the computer one time per day.</span></span>

<span data-ttu-id="4df5e-124">**ADVERTENCIA**  Si el agente de cliente de MBAM intenta cifrar un equipo que no es compatible con el cifrado de unidad BitLocker, existe la posibilidad de que se dañe el equipo.</span><span class="sxs-lookup"><span data-stu-id="4df5e-124">**Warning** If the MBAM client agent tries to encrypt a computer that does not support BitLocker drive encryption, there is a possibility that the computer will become corrupted.</span></span> <span data-ttu-id="4df5e-125">Asegúrese de que la característica compatibilidad de hardware esté correctamente configurada cuando su organización tenga hardware antiguo que no sea compatible con BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4df5e-125">Ensure that the hardware compatibility feature is correctly configured when your organization has older hardware that does not support BitLocker.</span></span>

 

**<span data-ttu-id="4df5e-126">Para administrar la compatibilidad de hardware</span><span class="sxs-lookup"><span data-stu-id="4df5e-126">To manage hardware compatibility</span></span>**

1.  <span data-ttu-id="4df5e-127">Abra un explorador Web y navegue al sitio web de supervisión y administración de Microsoft BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4df5e-127">Open a web browser and navigate to the Microsoft BitLocker Administration and Monitoring website.</span></span> <span data-ttu-id="4df5e-128">Seleccione **hardware** en la barra de menús de la izquierda.</span><span class="sxs-lookup"><span data-stu-id="4df5e-128">Select **Hardware** in the left menu bar.</span></span>

2.  <span data-ttu-id="4df5e-129">En el panel derecho, haga clic en **búsqueda avanzada**y, a continuación, en filtrar para mostrar una lista de todos los modelos de equipos que tienen el estado de **capacidad** de **desconocido**.</span><span class="sxs-lookup"><span data-stu-id="4df5e-129">On the right pane, click **Advanced Search**, and then filter to display a list of all computer models that have a **Capability** status of **Unknown**.</span></span> <span data-ttu-id="4df5e-130">Se muestra una lista de modelos de equipo que coinciden con los criterios de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4df5e-130">A list of computer models matching the search criteria is displayed.</span></span> <span data-ttu-id="4df5e-131">Los administradores pueden agregar, editar o quitar nuevos tipos de equipos de esta página.</span><span class="sxs-lookup"><span data-stu-id="4df5e-131">Administrators can add, edit, or remove new computer types from this page.</span></span>

3.  <span data-ttu-id="4df5e-132">Revise cada configuración de hardware desconocida para determinar si la configuración debe establecerse en **compatible** o **incompatible**.</span><span class="sxs-lookup"><span data-stu-id="4df5e-132">Review each unknown hardware configuration to determine whether the configuration should be set to **Compatible** or **Incompatible**.</span></span>

4.  <span data-ttu-id="4df5e-133">Seleccione una o más filas y, a continuación, haga clic en **establecer compatible** o **establecer como incompatible** para establecer la compatibilidad de BitLocker, según corresponda, para los modelos de equipos seleccionados.</span><span class="sxs-lookup"><span data-stu-id="4df5e-133">Select one or more rows, and then click either **Set Compatible** or **Set Incompatible** to set the BitLocker compatibility, as appropriate, for the selected computer models.</span></span> <span data-ttu-id="4df5e-134">Si se establece en **compatible**, BitLocker intenta forzar la Directiva de cifrado de unidad en los equipos que coinciden con el modelo admitido.</span><span class="sxs-lookup"><span data-stu-id="4df5e-134">If set to **Compatible**, BitLocker tries to enforce drive encryption policy on computers that match the supported model.</span></span> <span data-ttu-id="4df5e-135">Si se establece en **incompatible**, BitLocker no aplicará la Directiva de cifrado de unidad en esos equipos.</span><span class="sxs-lookup"><span data-stu-id="4df5e-135">If set to **Incompatible**, BitLocker will not enforce drive encryption policy on those computers.</span></span>

    <span data-ttu-id="4df5e-136">**Nota:**  Después de configurar un modelo de equipo como compatible, el cliente de MBAM puede tardar más de veinticuatro horas en iniciar el cifrado de BitLocker en los equipos que coincidan con ese modelo de hardware.</span><span class="sxs-lookup"><span data-stu-id="4df5e-136">**Note** After you set a computer model as compatible, it can take more than twenty-four hours for the MBAM Client to begin BitLocker encryption on the computers matching that hardware model.</span></span>

     

5.  <span data-ttu-id="4df5e-137">Los administradores deben supervisar regularmente la lista de compatibilidad de hardware para revisar los nuevos modelos detectados por el agente de MBAM y, después, actualizar su configuración de compatibilidad a **compatible** o **incompatible** , según corresponda.</span><span class="sxs-lookup"><span data-stu-id="4df5e-137">Administrators should regularly monitor the hardware compatibility list to review new models that are discovered by the MBAM agent, and then update their compatibility setting to **Compatible** or **Incompatible** as appropriate.</span></span>

## <span data-ttu-id="4df5e-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4df5e-138">Related topics</span></span>


[<span data-ttu-id="4df5e-139">Administración de funciones de MBAM 1.0</span><span class="sxs-lookup"><span data-stu-id="4df5e-139">Administering MBAM 1.0 Features</span></span>](administering-mbam-10-features.md)

 

 





