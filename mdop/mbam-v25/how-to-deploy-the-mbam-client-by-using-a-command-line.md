---
title: Cómo implementar el cliente de MBAM mediante el uso de una línea de comandos
description: Cómo implementar el cliente de MBAM mediante el uso de una línea de comandos
author: dansimp
ms.assetid: ac1d4ffe-c26d-41c9-9737-a4f2b37fde24
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 416d76ad876c5114e3a8764111b6a15c879b13b5
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824490"
---
# <span data-ttu-id="08452-103">Cómo implementar el cliente de MBAM mediante el uso de una línea de comandos</span><span class="sxs-lookup"><span data-stu-id="08452-103">How to Deploy the MBAM Client by Using a Command Line</span></span>


<span data-ttu-id="08452-104">Puede usar una línea de comandos para implementar el software de cliente de supervisión y administración de Microsoft BitLocker (MBAM).</span><span class="sxs-lookup"><span data-stu-id="08452-104">You can use a command line to deploy the Microsoft BitLocker Administration and Monitoring (MBAM) Client software.</span></span>

## <span data-ttu-id="08452-105">Línea de comandos para implementar el software de cliente de MBAM</span><span class="sxs-lookup"><span data-stu-id="08452-105">Command Line to deploy the MBAM Client software</span></span>


<span data-ttu-id="08452-106">Escriba el siguiente comando en el símbolo del sistema para aceptar automáticamente el contrato de licencia para el usuario final al implementar el software de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="08452-106">Type the following command at the command prompt to automatically accept the end user license agreement when deploying the MBAM Client software.</span></span>

**<span data-ttu-id="08452-107">MBAMClientSetup.exe/acceptEula = Yes</span><span class="sxs-lookup"><span data-stu-id="08452-107">MBAMClientSetup.exe /acceptEula=Yes</span></span>**

<span data-ttu-id="08452-108">**Nota:**  Las opciones de línea de comandos **/Ju** y **/JM** no se admiten y no se pueden usar para instalar el software de cliente de MBAM.</span><span class="sxs-lookup"><span data-stu-id="08452-108">**Note** The **/ju** and **/jm** command-line options are not supported and cannot be used to install the MBAM Client software.</span></span>

 

<span data-ttu-id="08452-109">Escriba el siguiente comando en el símbolo del sistema para extraer e instalar el MSP:</span><span class="sxs-lookup"><span data-stu-id="08452-109">Type the following command at the command prompt to extract and install the MSP:</span></span>

**<span data-ttu-id="08452-110">MBAMClientSetup.exe la &lt; ruta de acceso/Extract para extraer MSI &gt; /AcceptEula = Yes</span><span class="sxs-lookup"><span data-stu-id="08452-110">MBAMClientSetup.exe /extract &lt;path to extract MSI&gt; /acceptEula=Yes</span></span>**

<span data-ttu-id="08452-111">Después, instale el MSI silenciosamente ejecutando el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="08452-111">Then, install the MSI silently by running the following command:</span></span>

**<span data-ttu-id="08452-112">msiexec/i &lt; ruta para extraído MSI &gt; /qb ALLUSERS = 1 REBOOT = ReallySuppress</span><span class="sxs-lookup"><span data-stu-id="08452-112">msiexec /i &lt;path to extracted MSI&gt; /qb ALLUSERS=1 REBOOT=ReallySuppress</span></span>**

<span data-ttu-id="08452-113">**Nota:**  A partir de MBAM 2,5 SP1, ya no se incluye un MSI aparte con el producto MBAM.</span><span class="sxs-lookup"><span data-stu-id="08452-113">**Note** Beginning in MBAM 2.5 SP1, a separate MSI is no longer included with the MBAM product.</span></span> <span data-ttu-id="08452-114">Sin embargo, puede extraer el MSI del archivo ejecutable (. exe) que se incluye con el producto, después de aceptar el CLUF.</span><span class="sxs-lookup"><span data-stu-id="08452-114">However, you can extract the MSI from the executable file (.exe) that is included with the product, after accepting the EULA.</span></span>

 

## <a href="" id="optin-for-microsoft-updates-1-command-line-option"></a><span data-ttu-id="08452-115">OPTIn \ _FOR \ _MICROSOFT \ _UPDATES = 1 opción de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="08452-115">OPTIN\_FOR\_MICROSOFT\_UPDATES=1 command-line option</span></span>


<span data-ttu-id="08452-116">Opcionalmente, puede especificar la opción de línea de comandos `OPTIN_FOR_MICROSOFT_UPDATES=1` durante la instalación del software cliente para instalar automáticamente las actualizaciones de Microsoft en equipos cliente.</span><span class="sxs-lookup"><span data-stu-id="08452-116">You can optionally specify the command-line option `OPTIN_FOR_MICROSOFT_UPDATES=1` during the Client software installation to automatically install Microsoft Updates on client computers.</span></span> <span data-ttu-id="08452-117">Al especificar esta opción, Microsoft Update se inicia automáticamente y busca las actualizaciones disponibles para instalarlas una vez finalizada la instalación del software cliente.</span><span class="sxs-lookup"><span data-stu-id="08452-117">Specifying this option makes Microsoft Update automatically start and search for available updates to install after the Client software installation finishes.</span></span>

<span data-ttu-id="08452-118">Puede usar esta opción de línea de comandos con cualquiera de los siguientes métodos de instalación.</span><span class="sxs-lookup"><span data-stu-id="08452-118">You can use this command-line option with either of the following installation methods.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="08452-119">Instale el software de cliente de MBAM con</span><span class="sxs-lookup"><span data-stu-id="08452-119">Install the MBAM Client software by using</span></span></th>
<th align="left"><span data-ttu-id="08452-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="08452-120">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="08452-121">MBAMClientSetup.exe</span><span class="sxs-lookup"><span data-stu-id="08452-121">MBAMClientSetup.exe</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="08452-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="08452-122">MbamClientSetup.exe OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="08452-123">msiexec/i MBAMClient.msi</span><span class="sxs-lookup"><span data-stu-id="08452-123">msiexec /i MBAMClient.msi</span></span></strong></p></td>
<td align="left"><p><strong><span data-ttu-id="08452-124">msiexec/i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES = 1</span><span class="sxs-lookup"><span data-stu-id="08452-124">msiexec /i MBAMClient.msi OPTIN_FOR_MICROSOFT_UPDATES=1</span></span></strong></p></td>
</tr>
</tbody>
</table>

 


## <span data-ttu-id="08452-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08452-125">Related topics</span></span>


[<span data-ttu-id="08452-126">Implementación de cliente de MBAM 2.5</span><span class="sxs-lookup"><span data-stu-id="08452-126">Deploying the MBAM 2.5 Client</span></span>](deploying-the-mbam-25-client.md)

 

 
## <span data-ttu-id="08452-127">¿Tiene una sugerencia para MBAM?</span><span class="sxs-lookup"><span data-stu-id="08452-127">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="08452-128">Agregue o vote por sugerencias [aquí](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span><span class="sxs-lookup"><span data-stu-id="08452-128">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="08452-129">Para problemas de MBAM, usa el [Foro de TechNet de MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="08452-129">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




