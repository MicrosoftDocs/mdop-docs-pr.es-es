---
title: Cómo administrar la redirección de la dirección URL mediante el Empaquetador de área de trabajo de MED-V
description: Cómo administrar la redirección de la dirección URL mediante el Empaquetador de área de trabajo de MED-V
author: dansimp
ms.assetid: 1a8d25af-479f-42d3-bf5f-c7fd974bbf8c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 88167923e3bd47f2a3b0b3ada5e818715740dbe3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/26/2020
ms.locfileid: "10824820"
---
# <span data-ttu-id="389b8-103">Cómo administrar la redirección de la dirección URL mediante el Empaquetador de área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="389b8-103">How to Manage URL Redirection by Using the MED-V Workspace Packager</span></span>


<span data-ttu-id="389b8-104">Puede usar el Empaquetador de área de trabajo de MED-V para administrar el redireccionamiento de direcciones URL en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="389b8-104">You can use the MED-V Workspace Packager to manage URL redirection in the MED-V workspace.</span></span>

**<span data-ttu-id="389b8-105">Para administrar el redireccionamiento de direcciones web en un área de trabajo de MED-V</span><span class="sxs-lookup"><span data-stu-id="389b8-105">To manage web address redirection in a MED-V workspace</span></span>**

1.  <span data-ttu-id="389b8-106">Para abrir el **Empaquetador de área de trabajo de MED-V**, haga clic en **Inicio**, haga clic en **todos los programas**, en **Microsoft Enterprise Desktop Virtualization**y, a continuación, haga clic en **Empaquetador de área de trabajo de MED-V**.</span><span class="sxs-lookup"><span data-stu-id="389b8-106">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2.  <span data-ttu-id="389b8-107">En el panel principal de **empaquetador del área de trabajo de MED-V** , haga clic en **administrar redireccionamiento web**.</span><span class="sxs-lookup"><span data-stu-id="389b8-107">On the **MED-V Workspace Packager** main panel, click **Manage Web Redirection**.</span></span>

3.  <span data-ttu-id="389b8-108">En la ventana **administrar redireccionamiento web** , puede escribir, pegar o importar una lista de las direcciones URL que se redirigen a Internet Explorer en el área de trabajo de MED-V.</span><span class="sxs-lookup"><span data-stu-id="389b8-108">In the **Manage Web Redirection** window, you can type, paste, or import a list of the URLs that are redirected to Internet Explorer in the MED-V workspace.</span></span>

    **<span data-ttu-id="389b8-109">Nota</span><span class="sxs-lookup"><span data-stu-id="389b8-109">Note</span></span>**  
    <span data-ttu-id="389b8-110">El redireccionamiento de direcciones URL en MED-V solo admite los protocolos HTTP y HTTPS.</span><span class="sxs-lookup"><span data-stu-id="389b8-110">URL redirection in MED-V only supports the protocols HTTP and HTTPS.</span></span> <span data-ttu-id="389b8-111">MED-V no proporciona soporte técnico para FTP ni para otros protocolos.</span><span class="sxs-lookup"><span data-stu-id="389b8-111">MED-V does not provide support for FTP or any other protocols.</span></span>



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. <span data-ttu-id="389b8-112">Haga clic en **Guardar como...**</span><span class="sxs-lookup"><span data-stu-id="389b8-112">Click **Save as…**</span></span> <span data-ttu-id="389b8-113">para guardar los archivos de redireccionamiento de URL actualizados en la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="389b8-113">to save the updated URL redirection files in the specified folder.</span></span> <span data-ttu-id="389b8-114">MED-V crea un archivo de registro que contiene la información de redireccionamiento de la dirección URL actualizada.</span><span class="sxs-lookup"><span data-stu-id="389b8-114">MED-V creates a registry file that contains the updated URL redirection information.</span></span> <span data-ttu-id="389b8-115">Implemente la clave del registro actualizada con la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="389b8-115">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="389b8-116">Para obtener más información acerca de cómo usar la Directiva de grupo, consulte [instalación de software de directiva de grupo](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="389b8-116">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

   <span data-ttu-id="389b8-117">MED-V también crea un script de Windows PowerShell en la carpeta especificada que puede usar para volver a crear el paquete de área de trabajo de MED-V actualizado.</span><span class="sxs-lookup"><span data-stu-id="389b8-117">MED-V also creates a Windows PowerShell script in the specified folder that you can use to re-create the updated MED-V workspace package.</span></span>

## <span data-ttu-id="389b8-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="389b8-118">Related topics</span></span>


[<span data-ttu-id="389b8-119">Cómo agregar o quitar la información de redireccionamiento de dirección URL en un área de trabajo de MED-V implementada</span><span class="sxs-lookup"><span data-stu-id="389b8-119">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[<span data-ttu-id="389b8-120">Administrar la redirección de la dirección URL de MED-V</span><span class="sxs-lookup"><span data-stu-id="389b8-120">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)









