---
title: Crear o editar el archivo SMS \ _def. mof
description: Crear o editar el archivo SMS \ _def. mof
author: dansimp
ms.assetid: 0bc5e7d8-9747-4da6-a1b3-38d8f27ba121
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 272f597974e96efa0c742fecfe9488a4899fc695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10823200"
---
# <span data-ttu-id="3e302-103">Crear o editar el archivo SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="3e302-103">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="3e302-104">Para permitir que los equipos cliente informen detalles de compatibilidad con BitLocker a través de los informes de MBAM Configuration Manager, tiene que crear o editar el archivo SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="3e302-104">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span>

<span data-ttu-id="3e302-105">Si está usando SystemCenter2012 ConfigurationManager, debe crear el archivo.</span><span class="sxs-lookup"><span data-stu-id="3e302-105">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="3e302-106">Cree el archivo en el sitio de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="3e302-106">Create the file on the top-tier site.</span></span> <span data-ttu-id="3e302-107">Los cambios se replicarán en los otros sitios de su infraestructura.</span><span class="sxs-lookup"><span data-stu-id="3e302-107">The changes will be replicated to the other sites in your infrastructure.</span></span>

<span data-ttu-id="3e302-108">En el administrador de configuración 2007, el archivo ya existe, por lo que solo tiene que editarlo.</span><span class="sxs-lookup"><span data-stu-id="3e302-108">In Configuration Manager 2007, the file already exists, so you only have to edit it.</span></span> **<span data-ttu-id="3e302-109">No sobrescriba el archivo existente.</span><span class="sxs-lookup"><span data-stu-id="3e302-109">Do not overwrite the existing file.</span></span>**

<span data-ttu-id="3e302-110">En las siguientes secciones, complete las instrucciones que correspondan a la versión de Configuration Manager que está usando.</span><span class="sxs-lookup"><span data-stu-id="3e302-110">In the following sections, complete the instructions that correspond to the version of Configuration Manager that you are using.</span></span>

**<span data-ttu-id="3e302-111">Para crear el archivo SMS \ _def. mof para SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="3e302-111">To create the Sms\_def.mof file for SystemCenter2012 ConfigurationManager</span></span>**

1.  <span data-ttu-id="3e302-112">En el servidor de Configuration Manager, vaya a la ubicación en la que tiene que crear el archivo SMS \ _def. mof, por ejemplo, el escritorio.</span><span class="sxs-lookup"><span data-stu-id="3e302-112">On the Configuration Manager Server, browse to the location where you have to create the Sms\_def.mof file, for example, the Desktop.</span></span>

2.  <span data-ttu-id="3e302-113">Cree un archivo de texto denominado **SMS \ _def. mof** y copie el código siguiente para rellenar el archivo con el siguiente Sms \ _DEF. MBAM clases de MOF:</span><span class="sxs-lookup"><span data-stu-id="3e302-113">Create a text file called **Sms\_def.mof** and copy the following code to populate the file with the following Sms\_def.mof MBAM classes:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0")]
    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  <span data-ttu-id="3e302-114">Para importar el archivo de **SMS \ _def. mof** , haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3e302-114">Import the **Sms\_def.mof** file by doing the following:</span></span>

    1.  <span data-ttu-id="3e302-115">Abra la **consola SystemCenter2012 ConfigurationManager** y seleccione la ficha **Administration (administración** ).</span><span class="sxs-lookup"><span data-stu-id="3e302-115">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="3e302-116">En la pestaña **Administración** , seleccione **configuración de cliente**.</span><span class="sxs-lookup"><span data-stu-id="3e302-116">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="3e302-117">Haga clic con el botón derecho en **configuración de cliente predeterminada**y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="3e302-117">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="3e302-118">En la ventana **configuración predeterminada** , seleccione **inventario de hardware**.</span><span class="sxs-lookup"><span data-stu-id="3e302-118">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="3e302-119">Haga clic en **establecer clases**y, a continuación, en **importar**.</span><span class="sxs-lookup"><span data-stu-id="3e302-119">Click **Set Classes**, and then click **Import**.</span></span>

    6.  <span data-ttu-id="3e302-120">En el explorador que se abre, seleccione el archivo **. mof** y, a continuación, haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="3e302-120">In the browser that opens, select your **.mof** file, and then click **Open**.</span></span> <span data-ttu-id="3e302-121">Se abrirá la ventana **importar Resumen** .</span><span class="sxs-lookup"><span data-stu-id="3e302-121">The **Import Summary** window opens.</span></span>

    7.  <span data-ttu-id="3e302-122">En la ventana **importar Resumen** , asegúrese de que la opción para importar clases de inventario de hardware y configuración de clase está seleccionada y, a continuación, haga clic en **importar**.</span><span class="sxs-lookup"><span data-stu-id="3e302-122">In the **Import Summary** window, ensure that the option to import both hardware inventory classes and class settings is selected, and then click **Import**.</span></span>

    8.  <span data-ttu-id="3e302-123">Tanto en la ventana **clases de inventario de hardware** como en la ventana **configuración predeterminada** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="3e302-123">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

4.  <span data-ttu-id="3e302-124">Habilite la clase **Win32 \ _Tpm** de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="3e302-124">Enable the **Win32\_Tpm** class as follows:</span></span>

    1.  <span data-ttu-id="3e302-125">Abra la **consola SystemCenter2012 ConfigurationManager** y seleccione la ficha **Administration (administración** ).</span><span class="sxs-lookup"><span data-stu-id="3e302-125">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="3e302-126">En la pestaña **Administración** , seleccione **configuración de cliente**.</span><span class="sxs-lookup"><span data-stu-id="3e302-126">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="3e302-127">Haga clic con el botón derecho en **configuración de cliente predeterminada**y seleccione **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="3e302-127">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="3e302-128">En la ventana **configuración predeterminada** , seleccione **inventario de hardware**.</span><span class="sxs-lookup"><span data-stu-id="3e302-128">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="3e302-129">Haga clic en **establecer clases**.</span><span class="sxs-lookup"><span data-stu-id="3e302-129">Click **Set Classes**.</span></span>

    6.  <span data-ttu-id="3e302-130">En la ventana principal, desplácese hacia abajo y seleccione la clase **TPM (Win32 \ _Tpm)** .</span><span class="sxs-lookup"><span data-stu-id="3e302-130">In the main window, scroll down, and then select the **TPM (Win32\_Tpm)** class.</span></span>

    7.  <span data-ttu-id="3e302-131">En **TPM**, asegúrese de que la propiedad **SpecVersion** está seleccionada.</span><span class="sxs-lookup"><span data-stu-id="3e302-131">Under **TPM**, ensure that the **SpecVersion** property is selected.</span></span>

    8.  <span data-ttu-id="3e302-132">Tanto en la ventana **clases de inventario de hardware** como en la ventana **configuración predeterminada** , haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="3e302-132">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

**<span data-ttu-id="3e302-133">Para editar el archivo SMS \ _def. mof para Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="3e302-133">To edit the sms\_def.mof file for Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="3e302-134">En el servidor de Configuration Manager, vaya a la ubicación del archivo **SMS \ _def. mof** :</span><span class="sxs-lookup"><span data-stu-id="3e302-134">On the Configuration Manager Server, browse to the location of the **sms\_def.mof** file:</span></span>

    <span data-ttu-id="3e302-135">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="3e302-135">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="3e302-136">En una instalación predeterminada, la ubicación de instalación es% SystemDrive% \\Archivos de programa (x86) \\Microsoft Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="3e302-136">On a default installation, the installation location is %systemdrive% \\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="3e302-137">Copie el código siguiente y, a continuación, agréguelo al archivo **SMS \ _def. mof** para agregar al archivo las siguientes clases MBAM necesarias:</span><span class="sxs-lookup"><span data-stu-id="3e302-137">Copy the following code, and then append it to **Sms\_def.mof** file to add the following required MBAM classes to the file:</span></span>

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=32|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=64|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy_64: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;
        
        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;
        
        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser; 
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  <span data-ttu-id="3e302-138">Modifique la clase \**_Tpm de Win32 \** de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="3e302-138">Modify the **Win32\_Tpm** class as follows:</span></span>

    -   <span data-ttu-id="3e302-139">Establezca **SMS \ _REPORT** en **true** en los atributos de la clase.</span><span class="sxs-lookup"><span data-stu-id="3e302-139">Set **SMS\_REPORT** to **TRUE** in the class attributes.</span></span>

    -   <span data-ttu-id="3e302-140">Establezca **SMS \ _REPORT** en **true** en el atributo de la propiedad **SpecVersion** .</span><span class="sxs-lookup"><span data-stu-id="3e302-140">Set **SMS\_REPORT** to **TRUE** in the **SpecVersion** property attribute.</span></span>

    <span data-ttu-id="3e302-141">**¿Tiene una sugerencia para MBAM**?</span><span class="sxs-lookup"><span data-stu-id="3e302-141">**Got a suggestion for MBAM**?</span></span> <span data-ttu-id="3e302-142">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="3e302-142">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> <span data-ttu-id="3e302-143">**¿Tienes un problema de MBAM**?</span><span class="sxs-lookup"><span data-stu-id="3e302-143">**Got a MBAM issue**?</span></span> <span data-ttu-id="3e302-144">Usar el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="3e302-144">Use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="3e302-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3e302-145">Related topics</span></span>


[<span data-ttu-id="3e302-146">Requisitos previos de servidor MBAM 2.5 que se aplican solo a la topología de integración de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="3e302-146">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)

[<span data-ttu-id="3e302-147">Editar el archivo Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="3e302-147">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

[<span data-ttu-id="3e302-148">Requisitos previos de servidor MBAM 2.5 para topologías de integración independiente y de Administrador de configuración</span><span class="sxs-lookup"><span data-stu-id="3e302-148">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

 

 
## <span data-ttu-id="3e302-149">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="3e302-149">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="3e302-150">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="3e302-150">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="3e302-151">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="3e302-151">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




