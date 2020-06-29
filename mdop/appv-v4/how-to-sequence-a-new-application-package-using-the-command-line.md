---
title: Cómo secuenciar un nuevo paquete de aplicación mediante la línea de comandos
description: Cómo secuenciar un nuevo paquete de aplicación mediante la línea de comandos
author: dansimp
ms.assetid: de72912b-d9e7-45b5-a601-12528f1a4cac
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2dd638a7e4765cedbf1d8050626fb8cc54b2ce8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816680"
---
# <span data-ttu-id="eba4c-103">Cómo secuenciar un nuevo paquete de aplicación mediante la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="eba4c-103">How to Sequence a New Application Package Using the Command Line</span></span>


<span data-ttu-id="eba4c-104">Puede usar una línea de comandos para ordenar una nueva aplicación.</span><span class="sxs-lookup"><span data-stu-id="eba4c-104">You can use a command line to sequence a new application.</span></span> <span data-ttu-id="eba4c-105">Usar una línea de comandos es útil cuando tiene que crear un gran número de aplicaciones virtuales o cuando necesita crear aplicaciones secuenciadas de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="eba4c-105">Using a command line is useful when you have to create a large number of virtual applications or when you need to create sequenced applications on a recurring basis.</span></span>

**<span data-ttu-id="eba4c-106">Importante</span><span class="sxs-lookup"><span data-stu-id="eba4c-106">Important</span></span>**  
<span data-ttu-id="eba4c-107">La secuencia de la línea de comandos solo permite la secuenciación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="eba4c-107">Command-line sequencing allows for default sequencing only.</span></span> <span data-ttu-id="eba4c-108">Si necesita cambiar la configuración de instalación predeterminada de la aplicación que está transformando, debe modificar manualmente la aplicación virtual o actualizar la aplicación virtual mediante el secuenciador de Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="eba4c-108">If you need to change default installation settings for the application you are sequencing, you must either manually modify the virtual application or update the virtual application by using the Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="eba4c-109">Para obtener más información sobre cómo actualizar una aplicación virtual mediante el secuenciador de App-V, vea [Cómo actualizar una aplicación virtual existente](how-to-upgrade-an-existing-virtual-application.md).</span><span class="sxs-lookup"><span data-stu-id="eba4c-109">For more information about updating a virtual application by using the App-V Sequencer, see [How to Upgrade an Existing Virtual Application](how-to-upgrade-an-existing-virtual-application.md).</span></span>



<span data-ttu-id="eba4c-110">Use el procedimiento siguiente para crear una aplicación virtual mediante la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="eba4c-110">Use the following procedure to create a virtual application by using the command line.</span></span>

**<span data-ttu-id="eba4c-111">Para ordenar una aplicación con la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="eba4c-111">To sequence an application by using the command line</span></span>**

1.  <span data-ttu-id="eba4c-112">En el equipo que ejecuta el secuenciador de App-V, abra el símbolo del sistema seleccionando **Inicio**, **Ejecutar**y, a continuación, escriba **cmd**.</span><span class="sxs-lookup"><span data-stu-id="eba4c-112">On the computer that is running the App-V Sequencer, open the command prompt by selecting **Start**, **Run**, and then type **cmd**.</span></span> <span data-ttu-id="eba4c-113">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="eba4c-113">Click **OK**.</span></span>

2.  <span data-ttu-id="eba4c-114">Use el símbolo del sistema para especificar la ubicación en la que se instalará el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="eba4c-114">Use the command prompt to specify the location of where the App-V Sequencer is installed.</span></span> <span data-ttu-id="eba4c-115">Por ejemplo, en el símbolo del sistema, puede escribir lo siguiente: **CD c:\\Archivos de la aplicación SPRJ de virtualización**.</span><span class="sxs-lookup"><span data-stu-id="eba4c-115">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="eba4c-116">En el símbolo del sistema, escriba el siguiente comando y reemplace el texto entre comillas por sus valores:</span><span class="sxs-lookup"><span data-stu-id="eba4c-116">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="eba4c-117">Nota</span><span class="sxs-lookup"><span data-stu-id="eba4c-117">Note</span></span>**  
    <span data-ttu-id="eba4c-118">Puede especificar parámetros adicionales mediante la línea de comandos, en función de la complejidad de la aplicación que esté transformando.</span><span class="sxs-lookup"><span data-stu-id="eba4c-118">You can specify additional parameters by using the command line, depending on the complexity of the application you are sequencing.</span></span> <span data-ttu-id="eba4c-119">Para obtener una lista completa de los parámetros que se pueden usar con el secuenciador de App-V, consulte [línea de comandos de Application Virtualization Sequencer](application-virtualization-sequencer-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="eba4c-119">For a complete list of parameters that are available for use with the App-V Sequencer, see [Application Virtualization Sequencer Command Line](application-virtualization-sequencer-command-line.md).</span></span>



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
<td align="left"><p><em>pathtoMSI</em></p></td>
<td align="left"><p>Specifies the Windows Installer or a batch file that will be used to install an application so that it can be sequenced.</p></td>
</tr>
<tr class="even">
<td align="left"><p><em>pathtopackageroot</em></p></td>
<td align="left"><p>Specifies the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="eba4c-120">Presione **entrar**.</span><span class="sxs-lookup"><span data-stu-id="eba4c-120">Press **Enter**.</span></span>

## <span data-ttu-id="eba4c-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eba4c-121">Related topics</span></span>


[<span data-ttu-id="eba4c-122">Cómo administrar aplicaciones virtuales con la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="eba4c-122">How to Manage Virtual Applications Using the Command Line</span></span>](how-to-manage-virtual-applications-using-the-command-line.md)









