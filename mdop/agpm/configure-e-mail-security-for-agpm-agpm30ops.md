---
title: Configurar la seguridad del correo electrónico para AGPM
description: Configurar la seguridad del correo electrónico para AGPM
author: dansimp
ms.assetid: 4850ed8e-a1c6-43f0-95c5-853aa66a94ae
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3694662fd0ed81edacd16cf55ac9760b1be2ba97
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10818990"
---
# <span data-ttu-id="b2f3a-103">Configurar la seguridad del correo electrónico para AGPM</span><span class="sxs-lookup"><span data-stu-id="b2f3a-103">Configure E-Mail Security for AGPM</span></span>


<span data-ttu-id="b2f3a-104">De forma predeterminada, las notificaciones por correo electrónico enviadas a causa de las acciones de administración avanzada de directivas de grupo (AGPM) no se cifran y se envían a través del puerto SMTP 25.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-104">By default, e-mail notifications sent because of actions in Advanced Group Policy Management (AGPM) are not encrypted and are sent through SMTP port 25.</span></span> <span data-ttu-id="b2f3a-105">Sin embargo, puede configurar la seguridad del correo electrónico para AGPM mediante la configuración del registro para especificar si se usa el cifrado de capa de sockets seguros (SSL) y el puerto SMTP que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-105">However, you can configure e-mail security for AGPM by using registry settings to specify whether to use Secure Sockets Layer (SSL) encryption and which SMTP port to use.</span></span>

<span data-ttu-id="b2f3a-106">Al cifrar las notificaciones de correo electrónico de AGPM, puede proteger mejor las personas que podrían revelar información confidencial sobre la seguridad de la organización.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-106">By encrypting AGPM e-mail notifications, you can better protect those that could reveal sensitive information about your organization’s security.</span></span> <span data-ttu-id="b2f3a-107">El cifrado de notificaciones por correo electrónico es recomendable cuando se retransmiten a través de servidores de correo remoto y es posible que se lo exija alguna normativa de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-107">Encrypting e-mail notifications is recommended when they are being relayed through remote mail servers, and may be required by some compliance regulations.</span></span>

<span data-ttu-id="b2f3a-108">**PRECAUCIÓN**  La edición incorrecta del registro puede dañar gravemente el sistema.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-108">**Caution** Incorrectly editing the registry may severely damage your system.</span></span> <span data-ttu-id="b2f3a-109">Antes de realizar cambios en el registro, debe hacer una copia de seguridad de los datos valiosos del equipo.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-109">Before making changes to the registry, you should back up any valued data on the computer.</span></span>

 

<span data-ttu-id="b2f3a-110">Una cuenta de usuario que tenga el rol de administrador (control total) AGPM, la cuenta de usuario del aprobador que creó el objeto de directiva de grupo (GPO) que se usó en estos procedimientos, o una cuenta de usuario que tenga los permisos necesarios en AGPM, se necesita para completar estos procedimientos.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-110">A user account that has the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account that has the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="b2f3a-111">Revise los detalles en "consideraciones adicionales" en este tema.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-111">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="b2f3a-112">Para configurar la seguridad del correo electrónico para AGPM con preferencias de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="b2f3a-112">To configure e-mail security for AGPM by using Group Policy preferences</span></span>**

1.  <span data-ttu-id="b2f3a-113">En el árbol de **consola de administración de directivas de grupo** , edite un GPO que se aplica a todos los servidores de AGPM para los que desea configurar la seguridad del correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-113">In the **Group Policy Management Console** tree, edit a GPO that is applied to all AGPM Servers for which you want to configure e-mail security.</span></span> <span data-ttu-id="b2f3a-114">(Para obtener más información, consulte [edición de un GPO](editing-a-gpo-agpm30ops.md)).</span><span class="sxs-lookup"><span data-stu-id="b2f3a-114">(For more information, see [Editing a GPO](editing-a-gpo-agpm30ops.md).)</span></span>

2.  <span data-ttu-id="b2f3a-115">En la **ventana Editor de administración de directivas de grupo** , expanda la configuración del **equipo**, las **preferencias**, la **configuración de Windows**y las carpetas **del registro** .</span><span class="sxs-lookup"><span data-stu-id="b2f3a-115">In the **Group Policy Management Editor** window, expand the **Computer Configuration**, **Preferences**, **Windows Settings**, and **Registry** folders.</span></span>

3.  <span data-ttu-id="b2f3a-116">En el árbol de consola, haga clic con el botón derecho en **registro**, seleccione **nuevo**, haga clic en **elemento de recopilación**y escriba **seguridad de correo electrónico de AGPM**.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-116">In the console tree, right-click **Registry**, point to **New**, click **Collection Item**, and type **AGPM e-mail security**.</span></span>

4.  <span data-ttu-id="b2f3a-117">Crear un elemento de preferencias del registro para activar el cifrado:</span><span class="sxs-lookup"><span data-stu-id="b2f3a-117">Create a Registry preference item to turn on encryption:</span></span>

    1.  <span data-ttu-id="b2f3a-118">En el árbol de consola, haga clic con el botón secundario en **seguridad de correo electrónico de AGPM**, seleccione **nuevo**y, después, haga clic en **elemento de registro**.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-118">In the console tree, right-click **AGPM e-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="b2f3a-119">En el cuadro de diálogo **nuevas propiedades del registro** , seleccione la acción de **actualización** .</span><span class="sxs-lookup"><span data-stu-id="b2f3a-119">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="b2f3a-120">Para **subárbol**, seleccione **HKEY \ _LOCAL \ _MACHINE**.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-120">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="b2f3a-121">En **ruta**de la clave, escriba **SOFTWARE\\Microsoft\\AGPM**.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-121">For **Key Path**, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="b2f3a-122">En **nombre del valor**, escriba **EncryptSmtp**.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-122">For **Value name**, type **EncryptSmtp**.</span></span>

    6.  <span data-ttu-id="b2f3a-123">En **tipo de valor**, seleccione **reg \ _DWORD**.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-123">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="b2f3a-124">En **base**, seleccione **decimal**y, para **datos de valor**, escriba **1** para usar el cifrado SSL o **0** para permitir que el correo electrónico se envíe sin cifrar.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-124">For **Base**, select **Decimal**, and for **Value data**, type **1** to use SSL encryption, or **0** to let e-mail to be sent without encryption.</span></span> <span data-ttu-id="b2f3a-125">De forma predeterminada, el correo electrónico se envía sin cifrado.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-125">By default, e-mail is sent without encryption.</span></span>

    8.  <span data-ttu-id="b2f3a-126">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-126">Click **OK**.</span></span>

5.  <span data-ttu-id="b2f3a-127">Cree un elemento de preferencias del registro para especificar el puerto SMTP:</span><span class="sxs-lookup"><span data-stu-id="b2f3a-127">Create a Registry preference item to specify the SMTP port:</span></span>

    1.  <span data-ttu-id="b2f3a-128">En el árbol de consola, haga clic con el botón secundario en **seguridad de correo electrónico de AGPM**, seleccione **nuevo**y, después, haga clic en **elemento de registro**.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-128">In the console tree, right-click **AGPM E-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="b2f3a-129">En el cuadro de diálogo **nuevas propiedades del registro** , seleccione la acción de **actualización** .</span><span class="sxs-lookup"><span data-stu-id="b2f3a-129">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="b2f3a-130">Para **subárbol**, seleccione **HKEY \ _LOCAL \ _MACHINE**.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-130">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="b2f3a-131">En el cuadro de diálogo ruta de la **clave** , escriba **SOFTWARE\\Microsoft\\AGPM**.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-131">For **Key Path** dialog box, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="b2f3a-132">En **nombre del valor**, escriba **SmtpPort**.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-132">For **Value name**, type **SmtpPort**.</span></span>

    6.  <span data-ttu-id="b2f3a-133">En **tipo de valor**, seleccione **reg \ _DWORD**.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-133">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="b2f3a-134">En **base**, seleccione **decimal**y, para **información del valor**, escriba un número de puerto para el puerto SMTP.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-134">For **Base**, select **Decimal**, and for **Value data**, type a port number for the SMTP port.</span></span> <span data-ttu-id="b2f3a-135">De forma predeterminada, el puerto SMTP es el puerto 25 si el cifrado no está habilitado o el puerto 587 si el cifrado SSL está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-135">By default, the SMTP port is port 25 if encryption is not enabled or port 587 if SSL encryption is enabled.</span></span>

    8.  <span data-ttu-id="b2f3a-136">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-136">Click **OK**.</span></span>

6.  <span data-ttu-id="b2f3a-137">Cierre la ventana del **Editor de administración de directivas de grupo** y, a continuación, proteja e implemente el GPO.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-137">Close the **Group Policy Management Editor** window, and then check in and deploy the GPO.</span></span> <span data-ttu-id="b2f3a-138">Para obtener más información, consulte [implementar un GPO](deploy-a-gpo-agpm30ops.md).</span><span class="sxs-lookup"><span data-stu-id="b2f3a-138">For more information, see [Deploy a GPO](deploy-a-gpo-agpm30ops.md).</span></span>

### <span data-ttu-id="b2f3a-139">Consideraciones adicionales</span><span class="sxs-lookup"><span data-stu-id="b2f3a-139">Additional considerations</span></span>

-   <span data-ttu-id="b2f3a-140">Debe poder editar e implementar un GPO para establecer la configuración del registro mediante preferencias de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-140">You must be able to edit and deploy a GPO to configure registry settings by using Group Policy Preferences.</span></span> <span data-ttu-id="b2f3a-141">Consulte [editar un GPO](editing-a-gpo-agpm30ops.md) e [implementar un GPO](deploy-a-gpo-agpm30ops.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="b2f3a-141">See [Editing a GPO](editing-a-gpo-agpm30ops.md) and [Deploy a GPO](deploy-a-gpo-agpm30ops.md) for additional detail.</span></span>

### <span data-ttu-id="b2f3a-142">Referencias adicionales</span><span class="sxs-lookup"><span data-stu-id="b2f3a-142">Additional references</span></span>

-   [<span data-ttu-id="b2f3a-143">Configuración de Administración avanzada de directivas de grupo</span><span class="sxs-lookup"><span data-stu-id="b2f3a-143">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management.md)

 

 





