---
title: Cómo actualizar un paquete de aplicaciones secuenciadas mediante la línea de comandos
description: Cómo actualizar un paquete de aplicaciones secuenciadas mediante la línea de comandos
author: dansimp
ms.assetid: 682fac46-c71d-4731-831b-81bfd5032764
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: eade2ced43852419176f635918f0a6b7c3444aee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816490"
---
# <span data-ttu-id="6caf8-103">Cómo actualizar un paquete de aplicaciones secuenciadas mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="6caf8-103">How to Upgrade a Sequenced Application Package Using the Command Line</span></span>


<span data-ttu-id="6caf8-104">Use el siguiente procedimiento para actualizar una aplicación virtual mediante una línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="6caf8-104">Use the following procedure to upgrade a virtual application by using a command line.</span></span> <span data-ttu-id="6caf8-105">Al actualizar un paquete de aplicación virtual existente mediante la línea de comandos, se elimina la versión original del archivo. SFT.</span><span class="sxs-lookup"><span data-stu-id="6caf8-105">When you upgrade an existing virtual application package by using the command line, the original version of the .sft file is deleted.</span></span> <span data-ttu-id="6caf8-106">Debe realizar una copia de seguridad del archivo. SFT asociado antes de actualizar el paquete mediante la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="6caf8-106">You should back up the associated .sft file before upgrading the package by using the command line.</span></span>

**<span data-ttu-id="6caf8-107">Para actualizar una aplicación virtual</span><span class="sxs-lookup"><span data-stu-id="6caf8-107">To upgrade a virtual application</span></span>**

1.  <span data-ttu-id="6caf8-108">En el equipo que ejecuta el secuenciador de Application Virtualization (App-V), para abrir el símbolo del sistema, seleccione **Inicio**, **Ejecutar**y escriba **cmd**.</span><span class="sxs-lookup"><span data-stu-id="6caf8-108">On the computer that is running the Application Virtualization (App-V) Sequencer, to open the command prompt, select **Start**, **Run**, and type **cmd**.</span></span> <span data-ttu-id="6caf8-109">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6caf8-109">Click **OK**.</span></span>

2.  <span data-ttu-id="6caf8-110">En el símbolo del sistema, especifique la ubicación donde está instalado el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="6caf8-110">At the command prompt, specify the location where the App-V Sequencer is installed.</span></span> <span data-ttu-id="6caf8-111">Por ejemplo, en el símbolo del sistema, puede escribir lo siguiente: **CD c:\\Archivos de la aplicación SPRJ de virtualización**.</span><span class="sxs-lookup"><span data-stu-id="6caf8-111">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="6caf8-112">En el símbolo del sistema, escriba el siguiente comando y reemplace el texto entre comillas por sus valores:</span><span class="sxs-lookup"><span data-stu-id="6caf8-112">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /UPGRADE:"pathtosourceSPRJ" /INSTALLPACKAGE:"pathtoUpgradeInstaller" /DECODEPATH:"pathtodecodefolder" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="6caf8-113">Nota</span><span class="sxs-lookup"><span data-stu-id="6caf8-113">Note</span></span>**  
    <span data-ttu-id="6caf8-114">Puede especificar parámetros adicionales mediante la línea de comandos, en función de la complejidad de la aplicación que esté actualizando.</span><span class="sxs-lookup"><span data-stu-id="6caf8-114">You can specify additional parameters by using the command line, depending on the complexity of the application you are upgrading.</span></span> <span data-ttu-id="6caf8-115">Para obtener una lista completa de los parámetros que se pueden usar con el secuenciador de App-V, consulte [parámetros de la línea de comandos](command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="6caf8-115">For a complete list of parameters that are available for use with the App-V Sequencer, see [Command-Line Parameters](command-line-parameters.md).</span></span>



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



4. <span data-ttu-id="6caf8-116">Presione **entrar**.</span><span class="sxs-lookup"><span data-stu-id="6caf8-116">Press **Enter**.</span></span>

## <span data-ttu-id="6caf8-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6caf8-117">Related topics</span></span>


[<span data-ttu-id="6caf8-118">Cómo administrar aplicaciones virtuales con la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="6caf8-118">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)









