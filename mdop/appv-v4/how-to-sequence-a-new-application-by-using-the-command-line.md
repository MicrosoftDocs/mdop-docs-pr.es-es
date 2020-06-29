---
title: Cómo secuenciar una nueva aplicación mediante el uso de la línea de comandos
description: Cómo secuenciar una nueva aplicación mediante el uso de la línea de comandos
author: dansimp
ms.assetid: c3b5c842-6a91-4d0a-9a22-c7b8d1aeb09a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ea7b1222dc00a0a4649cb342ac1ba41338484889
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10816690"
---
# <span data-ttu-id="98d73-103">Cómo secuenciar una nueva aplicación mediante el uso de la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="98d73-103">How to Sequence a New Application by Using the Command Line</span></span>


<span data-ttu-id="98d73-104">Puede usar una línea de comandos para ordenar una nueva aplicación.</span><span class="sxs-lookup"><span data-stu-id="98d73-104">You can use a command line to sequence a new application.</span></span> <span data-ttu-id="98d73-105">Usar una línea de comandos es útil cuando tiene que crear un gran número de aplicaciones virtuales o cuando necesita crear aplicaciones secuenciadas de forma periódica.</span><span class="sxs-lookup"><span data-stu-id="98d73-105">Using a command line is useful when you have to create a large number of virtual applications or when you need to create sequenced applications on a recurring basis.</span></span>

**<span data-ttu-id="98d73-106">Importante</span><span class="sxs-lookup"><span data-stu-id="98d73-106">Important</span></span>**  
<span data-ttu-id="98d73-107">La secuencia de la línea de comandos solo permite la secuenciación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="98d73-107">Command-line sequencing allows for default sequencing only.</span></span> <span data-ttu-id="98d73-108">Si necesita cambiar la configuración de instalación predeterminada de la aplicación que está transformando, debe modificar manualmente la aplicación virtual o actualizar la aplicación virtual mediante el secuenciador de Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="98d73-108">If you need to change default installation settings for the application you are sequencing, you must either manually modify the virtual application or update the virtual application by using the Application Virtualization (App-V) Sequencer.</span></span> <span data-ttu-id="98d73-109">Para obtener más información sobre cómo actualizar una aplicación virtual mediante el secuenciador de App-V, vea [Cómo actualizar una aplicación virtual existente](how-to-upgrade-an-existing-virtual-application.md).</span><span class="sxs-lookup"><span data-stu-id="98d73-109">For more information about updating a virtual application by using the App-V Sequencer, see [How to Upgrade an Existing Virtual Application](how-to-upgrade-an-existing-virtual-application.md).</span></span>



<span data-ttu-id="98d73-110">Use el procedimiento siguiente para crear una aplicación virtual mediante la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="98d73-110">Use the following procedure to create a virtual application by using the command line.</span></span>

**<span data-ttu-id="98d73-111">Para ordenar una aplicación con la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="98d73-111">To sequence an application by using the command line</span></span>**

1.  <span data-ttu-id="98d73-112">En el equipo que ejecuta el secuenciador de App-V, abra el símbolo del sistema seleccionando **Inicio**, **Ejecutar**y, a continuación, escriba **cmd**.</span><span class="sxs-lookup"><span data-stu-id="98d73-112">On the computer that is running the App-V Sequencer, open the command prompt by selecting **Start**, **Run**, and then type **cmd**.</span></span> <span data-ttu-id="98d73-113">Haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="98d73-113">Click **OK**.</span></span>

2.  <span data-ttu-id="98d73-114">Use el símbolo del sistema para especificar la ubicación en la que se instalará el secuenciador de App-V.</span><span class="sxs-lookup"><span data-stu-id="98d73-114">Use the command prompt to specify the location of where the App-V Sequencer is installed.</span></span> <span data-ttu-id="98d73-115">Por ejemplo, en el símbolo del sistema, puede escribir lo siguiente: **CD c:\\Archivos de la aplicación SPRJ de virtualización**.</span><span class="sxs-lookup"><span data-stu-id="98d73-115">For example, at the command prompt, you could type the following: **cd C:\\Program Files\\Microsoft Application Virtualization Sequencer**.</span></span>

3.  <span data-ttu-id="98d73-116">En el símbolo del sistema, escriba el siguiente comando y reemplace el texto entre comillas por sus valores:</span><span class="sxs-lookup"><span data-stu-id="98d73-116">At the command prompt, type the following command, replacing the text in quotation marks with your values:</span></span>

    `SFTSequencer /INSTALLPACKAGE:"pathtoMSI" /INSTALLPATH:"pathtopackageroot" /OUTPUTFILE:"pathtodestinationSPRJ"`

    **<span data-ttu-id="98d73-117">Nota</span><span class="sxs-lookup"><span data-stu-id="98d73-117">Note</span></span>**  
    <span data-ttu-id="98d73-118">Puede especificar parámetros adicionales mediante la línea de comandos, en función de la complejidad de la aplicación que esté transformando.</span><span class="sxs-lookup"><span data-stu-id="98d73-118">You can specify additional parameters by using the command line, depending on the complexity of the application you are sequencing.</span></span> <span data-ttu-id="98d73-119">Para obtener una lista completa de los parámetros que se pueden usar con el secuenciador de App-V, consulta parámetros de la [línea de comandos Sequencer](sequencer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="98d73-119">For a complete list of parameters that are available for use with the App-V Sequencer, see [Sequencer Command-Line Parameters](sequencer-command-line-parameters.md).</span></span>



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
<td align="left"><p>Specify the package root directory.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><em>pathtodestinationSPRJ</em></p></td>
<td align="left"><p>Specifies the path and file name of the SPRJ file that will be created.</p></td>
</tr>
</tbody>
</table>
~~~



4. <span data-ttu-id="98d73-120">Presione **entrar**.</span><span class="sxs-lookup"><span data-stu-id="98d73-120">Press **Enter**.</span></span>

## <span data-ttu-id="98d73-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="98d73-121">Related topics</span></span>


[<span data-ttu-id="98d73-122">Cómo crear o actualizar aplicaciones virtuales con el secuenciador de App-V</span><span class="sxs-lookup"><span data-stu-id="98d73-122">How to Create or Upgrade Virtual Applications Using the App-V Sequencer</span></span>](how-to-create-or-upgrade-virtual-applications-using--the-app-v-sequencer.md)

[<span data-ttu-id="98d73-123">Códigos de error de línea de comandos de secuenciador</span><span class="sxs-lookup"><span data-stu-id="98d73-123">Sequencer Command-Line Error Codes</span></span>](sequencer-command-line-error-codes.md)

[<span data-ttu-id="98d73-124">Parámetros de línea de comandos del secuenciador</span><span class="sxs-lookup"><span data-stu-id="98d73-124">Sequencer Command-Line Parameters</span></span>](sequencer-command-line-parameters.md)









