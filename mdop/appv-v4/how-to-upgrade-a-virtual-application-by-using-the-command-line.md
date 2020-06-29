---
title: Cómo actualizar una aplicación virtual mediante el uso de la línea de comandos
description: Cómo actualizar una aplicación virtual mediante el uso de la línea de comandos
author: dansimp
ms.assetid: 83c97767-6ea1-42aa-b411-ccc9fa61cf81
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8612deb31a1692dd85cfee88ca4b18cbc5ac2ab2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816461"
---
# <span data-ttu-id="fe2a0-103">Cómo actualizar una aplicación virtual mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="fe2a0-103">How to Upgrade a Virtual Application by Using the Command Line</span></span>


<span data-ttu-id="fe2a0-104">Use el siguiente procedimiento para actualizar una aplicación virtual mediante una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-104">Use the following procedure to upgrade a virtual application by using a command line.</span></span>

**<span data-ttu-id="fe2a0-105">Para actualizar una aplicación virtual</span><span class="sxs-lookup"><span data-stu-id="fe2a0-105">To upgrade a virtual application</span></span>**

1.  <span data-ttu-id="fe2a0-106">En el equipo que ejecuta el secuenciador de Application Virtualization (App-V), para abrir el símbolo del sistema, seleccione **Inicio**, **Ejecutar**y escriba **cmd**.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-106">On the computer that is running the Application Virtualization (App-V) Sequencer, to open the command prompt, select **Start**, **Run**, and type **cmd**.</span></span> <span data-ttu-id="fe2a0-107">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-107">Click **OK**.</span></span>

2.  <span data-ttu-id="fe2a0-108">En el símbolo del sistema, especifique la ubicación donde está instalado el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-108">At the command prompt, specify the location where the App-V Sequencer is installed.</span></span> <span data-ttu-id="fe2a0-109">Por ejemplo, en el símbolo del sistema, puede escribir lo siguiente: **CD c:\\Archivos de la aplicación SPRJ de virtualización**.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-109">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="fe2a0-110">En el símbolo del sistema, escriba el siguiente comando y reemplace el texto entre comillas por sus valores:</span><span class="sxs-lookup"><span data-stu-id="fe2a0-110">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="fe2a0-111">Nota</span><span class="sxs-lookup"><span data-stu-id="fe2a0-111">Note</span></span>**  
    <span data-ttu-id="fe2a0-112">Puede especificar parámetros adicionales mediante la línea de comandos, en función de la complejidad de la aplicación que esté actualizando.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-112">You can specify additional parameters by using the command line, depending on the complexity of the application you are upgrading.</span></span> <span data-ttu-id="fe2a0-113">Para obtener una lista completa de los parámetros que se pueden usar con el secuenciador de App-V, consulta parámetros de la [línea de comandos Sequencer](sequencer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="fe2a0-113">For a complete list of parameters that are available for use with the App-V Sequencer, see [Sequencer Command-Line Parameters](sequencer-command-line-parameters.md).</span></span>



~~~
Use the value descriptions in the following table to help you determine the actual text you will use in the preceding command.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><em>pathtosourceSPRJ</em></p></td>
<td align="left"><p>Specifies the directory location of the virtual application to be upgraded.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtoUpgradeInstaller</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an upgrade to the application.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodecodefolder</em></p></td>
<td align="left"><p>Specify the directory in which to unpack the SFT file.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="fe2a0-114">Presione **entrar**.</span><span class="sxs-lookup"><span data-stu-id="fe2a0-114">Press **Enter**.</span></span>

## <span data-ttu-id="fe2a0-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fe2a0-115">Related topics</span></span>


[<span data-ttu-id="fe2a0-116">Cómo crear o actualizar aplicaciones virtuales con el secuenciador de App-V</span><span class="sxs-lookup"><span data-stu-id="fe2a0-116">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[<span data-ttu-id="fe2a0-117">Códigos de error de línea de comandos de secuenciador</span><span class="sxs-lookup"><span data-stu-id="fe2a0-117">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

[<span data-ttu-id="fe2a0-118">Parámetros de línea de comandos del secuenciador</span><span class="sxs-lookup"><span data-stu-id="fe2a0-118">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)









